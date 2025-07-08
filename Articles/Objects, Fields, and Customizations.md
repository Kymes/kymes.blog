Objects, Fields, and Customizations 
=================================== 

With the pre-work done (to the best of my knowledge) I’m moving on to the actual application build. 

Again, in the interest of simplicity and flexibility, I’m creating two custom objects, one to hold the customer and vehicle record information and a second custom object to hold the service records for the vehicle records of the first object, then I must connect them to get them functioning correctly. 

Building the Data Model 
----------------------- 

For the first object, I knew that that would hold the customer information along with vehicle information. For the vehicle object I knew one of the crucial pieces of information that needed to be recorded is the make and model of the vehicle attached to the customer/owner. 

For this, I used the existing “vehicle make” picklist created in the pre-work phase of the application build as a controlling picklist, I then added another picklist of model names so that when a representative or customer adds account information they can only have model names based on the make of vehicle they enter. 

That vehicle information along with customer name, email, and phone number completed the vehicle object, ensuring correct information is entered. 

Next, I built the Service object, for this object I wanted to ensure that the correct information from the vehicle object was carried over with the ability to pass along service information to the mechanic profile. 

Bringing the objects together 
----------------------------- 

For this object I ran into another knowledge gap, namely the difference between a lookup relationship and a formula field. 

The original plan for moving the information from the vehicle object entailed me using a lookup relationship to the vehicle object from the service object. While testing, I was required to re-enter the information from the vehicle object and when the information was entered, I noticed plenty of related list views based on a plethora of fields from the vehicle object, and none of them made sense. 

Head-scratcher moments like these are where the most learning comes from. Not fully understanding what may have happened, I clearly wasn’t getting the results I wanted. 

At first, I was able to bring the contact information over without any issues using formulas, but the real issues started when I tried to bring over the field information from the make model and year picklists. 

This is where I finally understood functions. Formulas were one thing, I understood (in theory) how Validation rules worked as they had to represent what a field couldn’t be to be as solid as possible, but functions always fell under that original question of “Where would I use this?” 

Using the TEXT() function, I was able to bring over the field information for the make, model, and year picklist fields of the vehicle object. 

With these changes, overall, everything worked as it should in testing. When a customer or desk representative enters new information for the vehicle and contact information for a new customer, that information can then be used to create a service record with additional information for the mechanic profile. 

Next I’m building record types for the profiles for data hygiene and maybe some fields being available to different profiles. I’m also toying with the idea of adding a third user as a supervisor where the mechanic must submit their work for approval for even more data hygiene 
