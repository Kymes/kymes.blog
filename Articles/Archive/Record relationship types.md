Record Relationship Types
=========================

Salesforce provides options for standard and custom objects to facilitate record creation and cataloguing. But with a collection of objects all storing record data, shouldn’t there be a way to just view the object data in one place?

This is where object relationships come in handy. With object relationships, record data can be connected loosely, directly, the record data can refer to another record on the same object and record data can even be referenced externally outside of the immediate application.

### The Relationship Types are:

*   Lookup
*   Master-Detail
*   Junction Object
*   Self-Relationship
*   Hierarchical Relationship
*   Indirect Relationship
*   External Relationship

### Lookup Relationship

The first connection between objects is referred to as a Lookup relationship also known as a “one-to-many" relationship.

This relationship loosely relates record data of two objects to one another, meaning that both objects have their own record sharing settings and if one record is deleted the other object record is unaffected.

An object can have up to 40 Lookup relationships and record details for related record can be viewed on the related tab of the object record page.

### Master-Detail Relationship

For a stronger relationship between objects Salesforce offers another “one-to-many" relationship referred to as Master-Detail relationship.

This relationship establishes dependencies between the two object records and as the name implies, there is a parent and a child record.

The child record inherits the sharing and profile object permission settings of the Master record. If the parent record is deleted the child record is deleted as well.

An important capability that a Master Detail relationship has is to create a roll-up summary field. A roll-up summary field is a read-only field on the parent record used to aggregate information from the detail records as a COUNT, SUM, MIN, or MAX setting.

Any one object can have up to two master-detail relationships

And standard object records cannot be on the detail side of a roll-up summary field.

### Junction Object

Just as Lookup and Master-Detail relationships allow a “one-to-many” relationship between objects, a “many-to-many" relationship can also be established using a Junction object.

A Junction object is an intermediate object that allows the association of a child record to multiple parent records and vice-versa using two Master-Detail relationships on that single Junction object.

As you’ve seen, using relationships in Salesforce can connect records of different objects. Salesforce also offers an option to connect records within the same object.

### Self-Relationship

Self-Relationship is a lookup relationship which connects two different records on the same object. The self-relationship is used to create hierarchies of the Campaign, Case or Account objects. For example, a case record can also have a Parent Case record displayed as a field value.

### Hierarchical Relationship

Like the Self-Relationship, the Hierarchical Relationship is used to create user hierarchies on the User object only.

Unlike a user role chart which specifies data access by profile, the Hierarchical relationship is used to build and store an organizational chart. For example, an employee record can have a custom lookup field displaying supervisor with option to expand to show full organization hierarchy (no effect on data access).

Salesforce provides the ability to link internal records to each other even if they are located within two different objects. Establishing connections to external records is also possible.

### Indirect Relationship

Salesforce allows the access and utilization of record data from external databases. The Indirect Lookup relationship allows the Salesforce object - acting as the parent - to connect to an external child object for record viewing on the parent object.

### External Relationship

Salesforce also provides an inverse relationship option to the Indirect Lookup. For any external parent object an External Lookup relationship can be created to connect the external parent object to either another external child object or a Salesforce child object.

Salesforce provides a plethora of different options for connecting records together for better data access.
