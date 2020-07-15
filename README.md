# ms3-api

This repository is a result of the Mulesoft coding exercise. It contains  Mule application developed in Mule 3.xx runtime using 6.X Anypoint Studio version. The Mule Application is deployed on Cloudhub.

MS3-APi application is built for user to do the POST,PUT,GET,DELETE operation for the employee data to the mysql database

The Employee API is used to Insert, Update, Delete and Read the data in the database.

ID field in the database is the PRIMARY Field and is common in all the tables to match the data

There are also Micro services for the given data. which are Identification APi, Address API, Communication API. all these API's are built to perform the  CRUD operation

************************************** EMPLOYEE API *****************************************

Employee API to Insert employee details for given data is                     "http://ms3-api.us-e2.cloudhub.io/api/v1/employee" with POST Operation. (BODY mandatory)

Employee API to Get the data for all the employee's is                        "http://ms3-api.us-e2.cloudhub.io/api/v1/employee" with GET Operation.

Employee API to Get the data for given ID(Query Parameter)                    " http://ms3-api.us-e2.cloudhub.io/api/v1/employee?ID=4" with GET Operation

Employee API to Update the data for given data is                             "  http://ms3-api.us-e2.cloudhub.io/api/v1/employee?ID=4" with PUT operation (BODY mandatory)

Employee API to Delete the data for given Id(Query Parameter)                 " http://ms3-api.us-e2.cloudhub.io/api/v1/employee?Id=4" with PUT operation (Query parameter required)

************************************* IDENFICATION API **************************************

Identification API to Insert employee's Identification details for given data is  "http://ms3-api.us-e2.cloudhub.io/api/v1/Identification" with POST Operation. (BODY mandatory)

Identification API to Get the Identification data for all the employee's is     "http://ms3-api.us-e2.cloudhub.io/api/v1/Identification" with GET Operation.

Identification API to Get the Identification data for given ID(Query Param)     " http://ms3-api.us-e2.cloudhub.io/api/v1/Identification?ID=1" with GET Operation

Identification API to Update the Identification data for given data is          "http://ms3-api.us-e2.cloudhub.io/api/v1/Identification?ID=1" with PUT operation (BODY mandatory)

Identification API to Delete the data for given Id(Query Parameter)            "http://ms3-api.us-e2.cloudhub.io/api/v1/Identification?Id=1" with PUT operation (Query param required)


************************************* Address API **************************************
 
Address API to Insert employee's Address details for given data is           "http://ms3-api.us-e2.cloudhub.io/api/v1/Address" with POST Operation. (BODY mandatory)

Address API to Get the Address data for all the employee's is                "http://ms3-api.us-e2.cloudhub.io/api/v1/Address" with GET Operation.

Address API to Get the Address data for given ID(Query Parameter)            " http://ms3-api.us-e2.cloudhub.io/api/v1/Address?ID=1" with GET Operation

Address API to Update the Address data for given data is                     "http://ms3-api.us-e2.cloudhub.io/api/v1/Address?ID=1" with PUT operation (BODY mandatory)

Address API to Delete the data for given Id(Query Parameter)                 "http://ms3-api.us-e2.cloudhub.io/api/v1/Address?Id=1" with PUT operation (Query param required)


************************************* Communication API **************************************

Communication API to Insert employee' Communication details for given data is  "http://ms3-api.us-e2.cloudhub.io/api/v1/Communication" with POST Operation. (BODY mandatory)

Communication API to Get the Communication data for all the employee's is      "http://ms3-api.us-e2.cloudhub.io/api/v1/Communication" with GET Operation.

Communication API to Get the Communication data for given ID(Query Parameter)  " http://ms3-api.us-e2.cloudhub.io/api/v1/Communication?ID=1" with GET Operation

Communication API to Update the Communication data for given data is           "http://ms3-api.us-e2.cloudhub.io/api/v1/Communication?ID=1" with PUT operation (BODY mandatory)

Communication API to Delete the data for given Id(Query Parameter)             "http://ms3-api.us-e2.cloudhub.io/api/v1/Communication?Id=1" with PUT operation (Query param required)


********************************* DATABASE QUERIES***************************

The query for the employee table is Below

CREATE TABLE  employee (
    ID int NOT NULL AUTO_INCREMENT,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    DOB DATETIME,
    Gender VARCHAR(12),
    Title VARCHAR(70),
    Address_type VARCHAR(50),
    Address_number VARCHAR(123450),
    Address_street VARCHAR(50),
    Address_Unit VARCHAR(50),
    Address_City VARCHAR(50),
    Address_State VARCHAR(50),
    Address_zipcode VARCHAR(50),
    Communication_type VARCHAR(50),
    Communication_value VARCHAR(50),
    Communication_preferred VARCHAR(50),
    PRIMARY KEY (ID)
);

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

The query for the Identification table is Below

CREATE TABLE  Identification (
    ID int NOT NULL AUTO_INCREMENT,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    DOB DATETIME,
    Gender VARCHAR(12),
    Title VARCHAR(70),
    PRIMARY KEY (ID)
);

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>


The query for the Addeess table is Below

CREATE TABLE  Addeess (
    ID int NOT NULL AUTO_INCREMENT,
    Address_type VARCHAR(50),
    Address_number VARCHAR(123450),
    Address_street VARCHAR(50),
    Address_Unit VARCHAR(50),
    Address_City VARCHAR(50),
    Address_State VARCHAR(50),
    Address_zipcode VARCHAR(50),
    PRIMARY KEY (ID)
);


>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>


The query for the Communication table is Below

CREATE TABLE  Communication (
    ID int NOT NULL AUTO_INCREMENT,
    Communication_type VARCHAR(50),
    Communication_value VARCHAR(50),
    Communication_preferred VARCHAR(50),
    PRIMARY KEY (ID)
);
