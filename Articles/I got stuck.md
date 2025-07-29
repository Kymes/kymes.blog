I finally got stuck
===================

Well, it had to happen eventually - I got stuck. I got unstuck eventually, but getting there was messy.

For the next step, my original plan was to begin getting records organized by building out record types and making sure the infrastructure was there to continue iterating.

After finishing the skeleton of the CRM the first issue I wanted to correct were the listviews of both objects. The listviews showed a list of Vehicle numbers on the Vehicl object and Service Request numbers on the Service Requests object with no additional information.

Working under the System Administrator profile, I added Name, Email, Phone Number, along with vehicle information from the List View Controls on each of the objects and saved the listviews – simple enough with no issues.

Something told me to make sure that all profiles could see the new listview, and that’s were things got “hairy”.

I returned to Setup, searched Login Access Policies and enabled “Login-as-user”. I then searched for Security Controls in Session Settings and unchecked “Force Re-Login after login-as-user”. I went to the User screen to verify that I could login as the users under both profiles.

I decided to work on the Front Desk profile first because that profile needed the most access.

I selected the Front Desk profile, logged in and immediately realized that I missed a step somewhere.

For both the Front Desk and Mechanic users I could login and access the CRM itself but where there should have been a tab for each object, there was only one tab labeled “No Items”.

I was stuck.

### Working on getting unstuck

I went about isolating the issue to find a solution and guessed that record access was the problem, I checked OWD in the Session Settings menu page and found that it was set to “Private”. For OWD, to make sure I was able to see the records no matter what, I set access level to Public Read/Write for both the Vehicle and Service Request objects. I checked the logins again and saw no change for both users.

Next, I checked Assigned Apps on the Profiles page for both profiles and saw that Visible was Selected but greyed out and default checkbox wasn’t checked. I then went to the Object Settings in the Profile menu and found that all the objects were set to “No Access”. I set the access level for the Front Desk profile to Create, Read, Edit for both objects and set the Mechanic profile’s access to “Read” for the Service Request object only, I then went back to Assigned Apps and set the Car Care Garage app to default.

My results were successful and for both user profiles, I could see the necessary objects for each user/profile but not all of the records created under the System Administrator profile were showing up on the listviews.

In hindsight, I think I solved the issue of object access backwards, I should have checked App access before record access.

### Stuck Again but fixed one issue I didn’t think about

And then I got stuck again. When logged in as the Front Desk user, I could see the System Administrator records on the Vehicle object but no records were showing up on the Service Request object. I logged in as the Mechanic user and got the same result in the Service Request object, no records showing.

As an experiment, I logged back in as the Front Desk user and tried to create a record on the Vehicle object and was successful. I tried to create a record on the Service Request object using the Vehicle ID# from the record just created and discovered no access to the Vehicle ID# field to relate to the Service Request record.

Isolating the solution was easy enough.

I went back to the Setup menu, into Field Permissions and added Edit access to the Vehicle ID# field for the Front Desk profile.

Problem solved, I could add and access records created by the Front Desk user on the Service Request object and the records were able to be related to Vehicle ID#’s.

However, the Front Desk user still couldn’t see the System Admin’s records on the Service Request object and for some reason the System Administrator couldn’t see the records on the Vehicle object that were created by the Front Desk user - which really stood out to me. Also the Mechanic user still couldn’t access any records at all on the Service Request object which also stood out but I was thinking the issue may be related.

### Finally fixed it, solution was in a complete other direction

I wasn’t sure what to isolate in terms of a solution, at this point, what I needed was for all records to be accessible to all users on the objects they have access to with the Mechanic user only being able to view the Service Request records (for now).

I took a step back to assess the issue that needed to be solved. The OWD set to Public Read/Write, and the CRED settings for both objects were correct for what I needed for both users. While researching, I realized that both users were not set up with roles. I remember reading that roles add another layer of record security and shows the Salesforce platform who can share what with whom.

I created a small role hierarchy with Owner, Garage Manager, and Garage Associate listed. I set up both Front Desk and Mechanic users as Garage Associates and logged in as the Mechanic user again with no change to record access.

At this point, I was no longer sure the problem was about record sharing. I took a moment to look at all elements of the issue. What I was trying to do is get records to show up on a listview and be accessible to all users, if sharing configuration isn’t stopping that, then it must be a listview issue.

I logged back in as the System Administrator, went to the Service Requests object and looked around the listview icons until I came to the listview filters, I noticed that the listview filter was set to “Filter by Owner – My service requests”, I changed it to “Filter By Owner – All Service Requests”.

As soon as I saved filter parameters, all of the records created by the Front Desk user appeared on the listview as I was logged in as the System Administrator.

I changed the filter parameters on the Vehicle object.

I logged in as the Mechanic user and found the correct listview on the Service request object, logged in as the Front Desk user and found the same correct listview with all records included.

### Closing

So the issue was resolved and all users are able to see all records and also (more importantly) access them.

Because of that nature of the CRM, I don’t see a reason as to why there would be a reason to close off OWD access to anything besides Public Read/Write because (hypothetically) this is a CRM for a small garage with only a front desk user and mechanic to perform repairs. As the (hypothetical) garage grows that could easily change, but for right now I’m building the “infrastructure” to make further iterations easier.
