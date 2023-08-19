# phase 3 python command line project notes

## Project Requirement


- [Phase 3 Project Requirements](https://my.learn.co/courses/653/pages/phase-3-project-cli?module_item_id=95439)

## TO DO LIST

 - [ ]


### the minimum requirements
*  
   
- [ ] A CLI application 
   - [ ] that solves a real-world problem 
   - [ ] ? and adheres to best practices.
- [ ] A database created SQLAlchemy
   - [ ]  modified with SQLAlchemy ORM
   - [ ]  2+ related tables.
- [ ] A well-maintained virtual environment using Pipenv.
- [ ]  ? Proper package structure in your application.
- [ ] Use of lists 
- [ ] Use of dictionaries

### stretch goals 
- A database created and modified with SQLAlchemy ORM with 3+ related tables.
- Use of many-to-many relationships with SQLAlchemy ORM.
- Use of additional data structures, such as ranges and tuples.

   ### A rubric for this project 


## Project proposal


### Idea 1

House

#### Main idea

House window shopping App, for user to go and look at house they like and save them to a list of favorites

#### User story

- Users will look at a list of House and details
- Users will save a House to their favorites 
- Users can see 1 House
- Users can see their list of favorites
- Users can remove a House from their favorites


#### How I will use the concepts I recently learned to meet the project requirements

-  Object Oriented Python 
  - Class for House with attributes
  - Class for User with attributes
-  Database Tables 
  -  Describe how you will use SQLAlchemy to create and interact with 2 or more related database tables
  - Table: Users
     - id
     - email
  - Table: Houses
     - id
     - address
     - bedrooms
     - bathrooms
  - Table: (many to many) User-Houses == "List of Favourite Houses"
     - id
     - house id
     - user who favorites it id


-  Object Relationships 
  - Describe the types of relationships your different classes and tables will have with each other
  - User can have many favorite houses
  - House can be favorited by many users
  - Users to houses = many-to-many
    - with join table user-liked-houses

-  Aggregate and Association Methods 
  - CRUD
  - Create
    - Create a list of liked houses
  - Read
    - Read All
       - Display all houses
       - Display liked houses for user
    - Read 1
       - Display 1 house by ID

    - Update
       - Remove house from list of liked houses

    - Delete           
-  Use of Data Structures 
  - Describe how you plan on using data structures like lists and dictionaries in your project
  - Single Source of Truth
  - LIST: User could have a list of houses as ID's
    - ? is this the join table
  - DICTIONARY: House has set of attributes and values  

#### What area I think will be most challenging
 - Describe which aspect of the project you think will present the greatest challenge, or the topic that you feel least familiar with at present.

- Deciding how the data works with the join table

### Idea 2

  Car

 Main idea
  Car window shopping App, for user to go and look at Car they like and save them to a list of favorites

 User story
 Users will look House

 Main idea
  House window shopping App, for user to go and look at house they like and save them to a list of favorites

 User story
  Users will look at a list of House and details
  Users will save a House to their favorites
  Users can see 1 House
  Users can see their list of favorites
  Users can remove a House from their favorites
 How I will use the concepts I recently learned to meet the project requirements
 Object Oriented Python

 Class for House with attributes

 Class for User with attributes

 Database Tables

 Describe how you will use SQLAlchemy to create and interact with 2 or more related database tables

 Table: Users

 id
 email
 Table: Houses

 id
 address
 bedrooms
 bathrooms
 Table: (many to many) User-Houses == "List of Favourite Houses"

 id
 house id
 user who favorites it id
 Object Relationships

Describe the types of relationships your different classes and tables will have with each other

User can have many favorite houses

House can be favorited by many users

Users to houses = many-to-many

with join table user-liked-houses
Aggregate and Association Methods

CRUD

Create

Create a list of liked houses
Read

Read All

Display all houses
Display liked houses for user
Read 1

Display 1 house by ID
Update

Remove house from list of liked houses
Delete

Use of Data Structures

Describe how you plan on using data structures like lists and dictionaries in your project

Single Source of Truth

LIST: User could have a list of houses as ID's

? is this the join table
DICTIONARY: House has set of attributes and values

What area I think will be most challenging
Describe which aspect of the project you think will present the greatest challenge, or the topic that you feel least familiar with at present.

Deciding how the data works with the join tableat a list of Car and details
Users will save a Car to their favorites
Users can see 1 Car
Users can see their list of favorites
Users can remove a Car from their favorites
How I will use the concepts I recently learned to meet the project requirements
Object Oriented Python

Class for Car with attributes

Class for User with attributes

Database Tables

Describe how you will use SQLAlchemy to create and interact with 2 or more related database tables

Table: Users

id
email
Table: Cars

id
year
make
model
color

Table: (many to many) User-Cars == "List of Favourite Cars"

id
Car id
user who favorites it id
Object Relationships

Describe the types of relationships your different classes and tables will have with each other

User can have many favorite Cars

Car can be favorited by many users

Users to Cars = many-to-many

with join table user-liked-Cars
Aggregate and Association Methods

CRUD

Create

Create a list of liked Cars
Read

Read All

Display all Cars
Display liked Cars for user
Read 1

Display 1 Car by ID
Update

Remove Car from list of liked Cars
Delete

Use of Data Structures

Describe how you plan on using data structures like lists and dictionaries in your project

Single Source of Truth

LIST: User could have a list of Cars as ID's

? is this the join table
DICTIONARY: Car has set of attributes and values

What area I think will be most challenging
Describe which aspect of the project you think will present the greatest challenge, or the topic that you feel least familiar with at present.

Deciding how the data works with the join table

## Database Design


###  Database Tables 


#### Users
many to many relationship Houses

   - ID: INTEGER NOT NULL PRIMARY KEY AUTO INCREMENT
   - email: STRING NOT NULL UNIQUE

#### Houses
many to many relationship Users

   - ID: INTEGER NOT NULL PRIMARY KEY AUTO INCREMENT
   - address: STRING NOT NULL UNIQUE
   - bedrooms: INTEGER NOT NULL
   - bathrooms: FLOAT NOT NULL

#### Users liked Houses (join table)

   - ID: INTEGER NOT NULL PRIMARY KEY AUTO INCREMENT
   - house ID : INTEGER NOT NULL 
   - user who liked  it ID : INTEGER NOT NULL


