How does the Salesforce data model work?
========================================

Data Modeling is central to data management in Salesforce and gives an overall impression of how data moves through an application.

Salesforce provides several core objects with customizable fields for use in application building. Fortunately, Salesforce also provides pre-built, fully customizable, standard applications. In this article, the standard Sales application will be discussed as a starting point for data model creation.

To build a simple data model in the standard Salesforce Sales application, 4 objects can be used to manage record data, moving a potential client to a paying client. The 4 objects needed are Leads, Accounts, Contacts, and Opportunities.

The next section reviews how record data moves through a simple data model and the different options a user has to manage data.

### Lead Object:

The first part of data modeling starts with record creation/import. For the Lead object, records can be imported with a Data Import Wizard or captured electronically through a Web-To-Lead form submitted by a potential lead. Validation rules are used to ensure data integrity before lead record information can be saved and leads are then Assigned (through Assignment rules) to end-user queues for lead conversion to a Contact/Account.

### Contact and Account objects:

By default, the Contact and Account objects are related through a Lookup relationship (one-to-many relationship). This means that although Account and Contact are two different objects, the contact information can be viewed in the Contact field of the Account object, and each contact can be associated with many accounts.

Accounts can be created either manually (as a business or person account) or through Lead conversion and are the ideal starting point for sales opportunities.

### Opportunities:

The final object of this data model is where “process meets product”. The Opportunity object is where the sales status is tracked. An important field on the Opportunity object is the Stage field. The Stage field status is a picklist field, visually displayed as a component that can be added to the Opportunity object page through the Lightning App Builder. Picklist choices can be edited, added, or removed to fully customize the Sales process.

### Closing:

This shows a basic data model as a foundation for a basic sales process from first pitch (Leads) to final sale (Opportunities). While this is rudimentary, Salesforce offers other core objects to add functionality. For example, if a company wants to create marketing/sales campaigns, Salesforce provides a fully customizable Campaign object for that purpose. Or if a company needs to keep an eye on any issues with a sale and needs to keep track of the solution, Salesforce offers a Case object for that purpose.

Although this article only covered 4 of the core objects offered by Salesforce, the ability to customize and personalize the fields and relationships between objects makes Salesforce an ideal tool for data management.
