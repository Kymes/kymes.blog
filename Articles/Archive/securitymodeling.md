Security Modeling
=================

A great way to think about security modeling in Salesforce is to imagine layers of protection to data. Security modeling in Salesforce allows access controls to be configured on a macro-level on the org itself all the way down to field access of an individual record of an object within the org.

#### The four levels of security modeling are:

*   Org Access
*   Object Access
*   Record Access
*   Field Access

### Org-Level Security

For the first level of the security model, the User object will be the main source to set up the data security for users attempting to access the org itself. With the User object an Admin/App Builder can customize password parameters for specific profiles, as well as set login hours with allowable IP ranges for login.

### Record-Level Security:

Record-Level Security deals with record sharing and is where data access becomes more granular. Using profiles and permissions Record-Level Security specifies how a user can both view and share object records with other users of the org. As such there are more tools available to customize a user’s access to records and allow appropriate sharing capabilities the user profile may need. The first and most restrictive tool to be utilized are Organization-wide defaults or OWD. OWD defines the access a user has to records they do not own and is the starting point for further Sharing Settings, basic default options are:

*   Private: user cannot see record unless owned by that user, when owned the record cannot be seen by other users.
*   Public Read: any user can see the record but cannot edit it.
*   Public Read/Write: any user can see and edit a record.

With these default sharing options in place a user’s role is used to extend record access when OWD has been set to anything more restrictive than Public Read/Write.

Before continuing it’s important to remember that the Role Hierarchy is a data access hierarchy, not an organizational hierarchy.

Role Hierarchy displays the organization of and specifies data access by profile. Role Hierarchy overrides OWD and opens record access vertically to allow profiles above the record owner to access those records.

Sharing Rules on the other hand allow users at the same profile level in role hierarchy to be able to see each other’s records laterally (based on criteria and/or record owner). Finally, Manual Sharing is a tool that allows a record owner to grant access to records they own to other users.

### Field-Level Security

In a nutshell, Field Level Security refers to the ability to restrict, hide, and/or encrypt certain fields on an object record page/record type according to the user accessing the record. Field accessibility can be handled at the profile level but for full control of field access, these fields are also configured from the Page Layout Editor and through assignment of record types to specific profiles.

### Closing:

This article went through 4 layers of data security, ranging from the broadest, org-wide access options to the more granular. Salesforce provides plenty of other options for data security, but this article is meant to “scratch the surface” and show basically what Security Modeling entails with an overview of which tools fit into which level of data management.
