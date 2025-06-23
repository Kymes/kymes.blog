Prework, Profiles, and Picklists 
================================ 

Now that I had a direction, I needed to take the first steps. 

The Salesforce motto: “Objects, Fields, and Relationships” for me has always been unclear. If Objects are related through fields, isn’t the relationships' part redundant? My approach to building this CRM is closer to Objects, Fields, and Customization. It’s still the same idea but (for me) a little clearer. 

In the past when attempting to build apps, I always ran into the issue of needing “this” before “that”. Meaning that there are certain aspects to an application that need to be built first before building its core functionality. An example is building a controlling picklist before adding a dependent picklist to an object record. 

This aspect of an application build would always cause me to lose where I was in the overall process. And builds would never function correctly. 

It was like I knew the cart never went before the horse, but I didn’t understand how to build the cart in the first place. 

Getting Started with Profiles 
----------------------------- 

For this project I knew that I needed to get the planning correct before moving forward. Fortunately, for this build I wanted to keep things very simple, so the pre-work was also simple. 

After setting up org security on a generic Trailhead org, I began to set up the profile, picklist, and record type framework. Starting with the user profiles, I ran into my first issue. 

My original plan was to clone Standard User profiles and assign my two starting users. A limitation of generic Trailhead orgs is that they only come with two Standard User licenses. For each profile, there needs to be a single license assigned, and for the two users I wanted to set up I didn’t have enough licenses, especially since I (using the system administrator profile) was using one of them. 

After some research – and a few failed attempts at a solution - I discovered that the Salesforce Platform license (3 are included with the generic org) is very similar to the Standard User license, so I set up the user profiles with the Platform licenses. 

It was a small issue but still important to understand. 

Beginning to build the Picklists 
-------------------------------- 

For the next phase of pre-work, I knew I needed to work on the controlling picklist so that it would be available for the dependent picklist when building the core CRM. 

For the CRM build, it was crucial that correct vehicle/record information was entered with the least amount of confusion. With the sheer amount of both domestic and foreign vehicle makes available along with even more models, I thought the best to have the vehicle makes as controlling for the model names as a dependent picklist. 

This also opens the door for record types, but more on that later. 

To build the controlling “vehicle make” picklist, I used the Picklist Value Set option in Setup. I found a list online and used most of it to create the value set. Later I will connect the vehicle models to each appropriate vehicle make. 

The next steps 
-------------- 

So, with the pre-work out of the way (to the best of my knowledge) I will move on to the main build work to make the CRM perform is main, core function which is to both record new vehicle information and use that information to set up repair records. I have the idea to set up a third Supervisor user along with roles to reflect the hierarchy. 

I was thinking that I could have the mechanic profile submit records for approval after completing work on the vehicle as a quality control measure to ensure complete repair service. 
