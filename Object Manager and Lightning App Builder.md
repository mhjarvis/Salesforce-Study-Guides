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
## Record Types