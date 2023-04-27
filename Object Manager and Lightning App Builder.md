<h1 style="text-align: center; font-size: 40px">Object Manager and Lightning App Builder</h1>

# Standard Object Architecture and Relationship Model
There are two types of objects: Standard and Custom. 

## Standard Objects
These come with the Salesforce Org. 

## Data Model
There are two types of relationships that can be created between objects: Master Detail and Lookup. These relationships can be made so we can see data that is related in records. 

Master Detail has a parent-child relationship and can be one-to-one, one-to-many, or many-to-many.

Lookup has a loose relationship between objects. Links objects so users can see related items from one object to another. Can be one-to-one, one-to-many, self, external, indirect, or hierarchical. 

Standard objects have relationships with other standard objects. The Account object is a parent object of Contact, Opp, and Case. Account -> Contact has one-to-many relationship, hava a lookup relationship, and holds master-detail characteristics. 

A Lead can be converted into an Account, Contact, and optionally an Opportunity. Custom fields on the Account, Contact, or Opportunity can be mapped to custom fields on the Lead object. 

A Campaign can have many Campaign Members. 

The main objects in Sales Cloud have a default rlationship model. Schema builder can be ued to view the data model as well as create objects, fields, and relationships quickly. 

## Object Relationship
Used when there is a need to relate records in one objeect with a different object. Related records from a lookup/master-detail rlationship can be seen through related lists on the page layout. 

A self-relationship would be creating a lookup from one ACcount to another Account field.

Hierarchical Relationships are only available on the USER object.

Master-Detail Relationship:
    - The object with the lookup must have a prent. 
    - If a master record is deleted, all detail records are also deleted, unless the 'Allow Reparenting' setting is enabled which allows a detail record to be associated with another master record. 
    - Child obj inherits sharing/security settings.
    - Standard obj must be on the master-side of the relationship with a custom obj. 
    - Master-detail may be between two custom objects.

The OWNER field does not exist for a child object. 

A JUNCTION OBJECT allows for many-to-many relationships. This object sits between the other 2 objects and has a master-detail relationship with both. 

## Record Types
Record types can be used to:
    - diplay picklist values
    - display page layouts
    - support business processes

Custom record types can be grantedd access iwth permissison sets. 

# Create, Delete, and Customize Fields and Page Layouts
All objects come with some standard fields. The admin can customize these.

## Standard and Custom Fields


## Cutom Field Creation
## Picklist
## Roll-Up Summary Fieldss
## Formula Fields
## Custom Objects
## Apps and Tabs
## Page Layouts