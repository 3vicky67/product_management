# product_management
a way to learn about sap working

Project Description: Cinema Celebrities and Their Passions Management System using SAP RAP
1. Overview

This project is developed using the SAP RESTful ABAP Programming Model (RAP) to create a business application that manages information about cinema celebrities and their passions. The system stores, retrieves, and manages celebrity details and their personal interests using SAP Core Data Services (CDS), Behavior Definitions, and Database Tables.

The main objective of this project is to demonstrate how SAP RAP can be used to build a transactional business application with proper database structure, business logic, and service exposure.

2. Objective of the Project

The main objectives are:

To store and manage cinema celebrity information

To store and manage their passions or interests

To establish relationships between celebrities and their passions

To implement business logic using RAP Behavior Definition and Implementation

To expose the data for external access using Service Definition and Service Binding

3. Project Architecture

This project follows the three-layer architecture of SAP RAP:

3.1 Database Layer

This layer contains the physical database tables:

ZCIT_CELEB – Celebrity Detail Table

This table stores basic information about celebrities such as:

Celebrity ID

Celebrity Name

Age

Profession

Industry

ZCIT_PASSN – Celebrity Passion Table

This table stores information about passions such as:

Passion ID

Passion Name

Related Celebrity ID

This creates a relationship between celebrity and passion.

3.2 CDS Layer (Core Data Services)

CDS Views act as an interface between database and business logic.

CDS Views Created:

ZR_CIT_CELEB

Interface View

Used to access celebrity data

ZC_CIT_CELEB

Projection View

Used for UI and service exposure

ZR_CIT_PASSN

Interface View for passion data

ZC_CIT_PASSN

Projection View for passion

These CDS views help in:

Data abstraction

Data modelling

Secure data access

3.3 Behavior Layer

This layer defines business logic.

Behavior Definitions:

ZR_CIT_CELEB

Defines operations such as:

Create celebrity

Update celebrity

Delete celebrity

ZR_CIT_PASSN

Defines operations such as:

Create passion

Update passion

Delete passion

3.4 Behavior Implementation Class

Classes created:

ZBP_C_CIT_CELEB

Implements business logic for celebrity.

ZBP_R_CIT_CELEB

Handles RAP transactional behavior.

These classes control:

Data validation

Business rules

Transaction management

3.5 Metadata Extension

Metadata extensions:

ZME_CIT_CELEB

ZME_CIT_PASSN

These are used to:

Define field labels

Improve UI appearance

Add annotations

3.6 Service Layer

This layer exposes data as a service.

Service Definition

Defines which CDS Views are exposed.

Service Binding

Makes the service available as:

OData Service

For SAP Fiori applications

4. How the System Works

Step-by-Step Process:

User enters celebrity details

Data is stored in ZCIT_CELEB table

User enters passion details

Data is stored in ZCIT_PASSN table

CDS Views retrieve the data

Behavior Definition controls operations

Service Binding exposes data

Data can be viewed in SAP Fiori

5. Technologies Used
Technology	Purpose
SAP ABAP	Programming
SAP RAP	Application Development
CDS Views	Data Modelling
Database Tables	Data Storage
Behavior Definition	Business Logic
Service Binding	OData Service
Metadata Extension	UI Enhancement
6. Advantages of this Project

• Follows modern SAP RAP architecture
• Clean separation of layers
• Secure data access
• Easy to extend
• Supports SAP Fiori

7. Real-World Use Case

This type of system can be used in:

Film Industry Management

Celebrity Management Systems

Talent Management Systems

8. Conclusion

This project successfully demonstrates the implementation of a Cinema Celebrity and Passion Management System using SAP RAP. It shows how database tables, CDS views, behavior definitions, and service bindings work together to create a complete business application.

The system is scalable, maintainable, and follows SAP best practices.
