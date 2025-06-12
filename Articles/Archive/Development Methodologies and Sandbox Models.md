Development Methodologies and Sandbox Models
============================================

Application Lifecycle Management at its most basic is a way to manage change of a Production Org. Salesforce provides dedicated development environments known as Sandboxes. Salesforce also offers three different development methodologies designed to scale by project complexity, development team size, and the metadata being worked on.

### Change Set Development:

Change Set development is a declarative development option allowing the deployment of metadata only changes from Sandbox to Production. Any data changes are handled with a Data Loader tool. This development model is suitable for solo low-code developers or small development teams making simple changes.

### There are two types of Change Sets, Outbound and Inbound:

Outbound: OB change sets are created from the org/sandbox where changes have been made and sent out to the org where changes are supposed to take place.

Inbound: IB change set is what shows up on the org/sandbox that the changes are supposed to take place.

### Org Development:

Org development is used for mid-size development teams working on more complex development projects. Org development methodology specifies the use of a Version Control System (VCS) such as Git as a form of source control. Org Development is meant to streamline development and reduce the chances that developers overwrite/duplicate each other’s work before deployment to the production org.

### Package Development:

Package Development is an extension of Org Development. The Org Development model is utilized by teams of developers to create self-contained applications or packages. These packages can then be used by other teams as part of a larger build or deployed to production.

### Two types of packages are used for this type of development methodology:

Unmanaged: Unmanaged packages are used to transport unrelated components and modules between orgs/sandboxes, other developers can view the code, and edit components.

Managed: With Managed Packages a user cannot view the code or edit components. The code can only be edited by the source organization and is typically used by Salesforce AppExchange partners to distribute apps to their customers.

Sandbox Modelling:
------------------

With an understanding of Salesforce Development methodologies, it is important to also understand how the data moves through development environments to deployment. Sandbox modeling provides that framework.

A Sandbox model is a framework of tiers with the different sandboxes acting as nodes which correspond to the steps of development typical of SDLC management:

Develop and Build: This foundational tier of a Sandbox model is where the most isolated development takes place. Salesforce offers the Developer sandbox environment as a way for users to complete assigned customizations before being transferred to the testing tier.

Build and Test: For the second tier, two sandboxes are utilized. The Developer Pro sandbox has a higher storage capacity than the Developer edition and is used to aggregate the work completed from the first tier. A Partial sandbox template is used for testing customizations before data is moved to the final tier.

Test, Train, and Deploy: For the final tier of the sandbox model a Full sandbox copy of the production org is used to test and stage the final build before deployment to the production org.

This article shows both how a sandbox environment is constructed and how data moves through those models.

Development and Sandboxes models work together to form a well-built framework for development. Utilizing these two tools a single developer or multiple teams of developers can create a multitude of apps on Salesforce.
