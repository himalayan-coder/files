## Page 1

Lab Manual

# SECTION 1: SOFTWARE ENGINEERING LAB

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

<table>
<thead>
<tr>
<th></th>
<th></th>
<th>Page Nos.</th>
</tr>
</thead>
<tbody>
<tr>
<td>1.0</td>
<td>Introduction</td>
<td>1</td>
</tr>
<tr>
<td>1.1</td>
<td>Objectives</td>
<td>1</td>
</tr>
<tr>
<td>1.2</td>
<td>Software Project Management</td>
<td>1</td>
</tr>
<tr>
<td>1.3</td>
<td>Working with Requirements</td>
<td>3</td>
</tr>
<tr>
<td></td>
<td>1.3.1 Feasibility Report</td>
<td></td>
</tr>
<tr>
<td></td>
<td>1.3.2 Software Requirement Specifications</td>
<td></td>
</tr>
<tr>
<td>1.4</td>
<td>Design Document</td>
<td>10</td>
</tr>
<tr>
<td>1.5</td>
<td>Testing</td>
<td>12</td>
</tr>
<tr>
<td>1.6</td>
<td>Implementation</td>
<td>13</td>
</tr>
<tr>
<td>1.7</td>
<td>List of Problems</td>
<td>13</td>
</tr>
<tr>
<td>1.8</td>
<td>Summary</td>
<td>14</td>
</tr>
</tbody>
</table>

## 1.0 INTRODUCTION

Software Engineering relates to the process of development of quality software. Normally, Software is the singlemost expensive item in a computer system. During the life time of a system , about 95% of the cost is incurred on software and only 5% on hardware. Computer AidedSoftware Engineering (CASE) tools help in many software engineering tasks with thehelp of the information created using the computer. CASE tools support software engineering tasks for the different phases of Software Development Life Cycle (SDLC). MCS-0213 discusses various aspects of Software Enginerring in detail. You must go through this course before taking the practical in this lab. The lab sessions in this unit revolve around various phases of software development.

This lab is an attempt to help you practice proper software development methodology. You must do these software development activities (lab sessions) with the help of suitable tools, preferably.

## 1.1 OBJECTIVES

After going through and working with the problems given in this section, you should be able to:

*   Develop plan for a Software Project;
*   Develop test cases;
*   Reengineer the Software;
*   Prepare and implement change requests and
*   Develop Software with good quality.

## 1.2 SOFTWARE PROJECT MANAGEMENT

The software project management tools support project planning and scheduling. Some of the sample information that you can produce using these tools are:

### A Sample Partial Project Plan

#### Overall Goal of the Project

&lt;page_number&gt;1&lt;/page_number&gt;

---


## Page 2

Software Engineering
Lab

The proposed software system should be able to:

*   read the structured data available in the Excel files and store it in a Database system.
*   validate data of the database on the basis of predefined business rules.
*   prepare reports on data that is found to be in error during validation.
*   prepare MIS reports from the validated data.

**The Primary Data**

The Primary data in the system is the employee data of the participantcompanies.

**Delivery Deadlines**

6 months from the date of Approval.

**PROJECT PLAN**

**1 OBJECTIVES**

The objective of the system can be defined here as:

*   The proposed system should be able to read the data from Excel files andstore validated data in the Database.
*   ................................................

**2 SPECIFIC PRODUCTS TO BE DELIVERED**

The products that will be delivered (You need not include all):

*   The tested system and Network
*   Client Workstations
*   A robust Database Management Server
*   Any other third party software.

**3 ACTIVITIES AND MILESTONES**

The activities in the system, after including the provisions for security, are:

*   Verification of the Users
*   Migration of the Excel data
*   Validation of the the migrated data
*   ............................................

The milestones in the system are:

*   Start of the Project : 1st June, 2006
*   SRS Completion : 28th June, 2006
*   Requiements finalization : 1st July, 2006
*   ............................................

**4 RESOURCE REQUIREMENT**

The Hardware, Software, and Tools are required for the three different environments, viz., Development environment, Quality Control environment, and Deployment environment. These resources may be documented accordingly.

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;2&lt;/page_number&gt;

---


## Page 3

Lab Manual

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

# 5 SCHEDULING

## GANTT Chart

A very elementary Gantt or Timeline Chart for the development plan is given below.
The plan explains the tasks versus the time they will take to complete.

<table>
<thead>
<tr>
<th></th>
<th>Jun</th>
<th>Jul</th>
<th>Aug</th>
<th>Sep</th>
<th>Oct</th>
<th>Nov</th>
</tr>
</thead>
<tbody>
<tr>
<td>Requirement Gathering</td>
<td colspan="2"></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Design</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Test Cases</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Coding</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Quality Assurance</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Testing</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Build</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## PERT Chart

A suitable PERT Chart for the development plan can be given here.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

# 6 BUDGETARY ESTIMATES

The whole budgetary estimates may be divided into resource procurement and software development costs. The software development efforts and cost may be estimated with the help of COCOMO or any other model used by the organization.

# 7 Summary

Please provide the summary here.

---

# 1.3 WORKING WITH REQUIREMENTS

Some of the activities that you can do with the help of tools are:

*   Cost Estimation
*   Creation of SRS
*   Traceability of requirements
*   Non-ambiguous requirements document
*   Creation of Models

Some of the partial samples for some of the above are illustrated here:

## 1.3.1 Feasibility Report

You may include contents as per the following table. A sample is shown after the table.

<table>
<thead>
<tr>
<th>Topic</th>
<th>Some of the contents of the topic</th>
</tr>
</thead>
<tbody>
<tr>
<td>Introduction</td>
<td>Include the project background and report layout here.</td>
</tr>
<tr>
<td>Terms of Reference</td>
<td>Define the expectations of the project, the Time Frame and Available Resources</td>
</tr>
<tr>
<td>Existing System</td>
<td>Include the results of Fact Finding, working of the Current System andthe problems in the Current System</td>
</tr>
</tbody>
</table>

&lt;page_number&gt;3&lt;/page_number&gt;

---


## Page 4

<table>
  <tr>
    <td>System Requirements</td>
    <td>Include the system requirements after discussion with the system user</td>
  </tr>
  <tr>
    <td>Proposed System</td>
    <td>Define the outline of the Proposed System, Input and Output</td>
  </tr>
  <tr>
    <td>Development Plan, Economic Feasibility and other feasibilities</td>
    <td>Include the Gantt Chart, Pert Chart, Cost estimation, etc.</td>
  </tr>
</table>

# INTRODUCTION

## Background of the Project

The basic requirement of the user and working of the system are:
* The Client should be able to upload the available data in Excel files into the Database.
* This data is then validated by the software called VALIDITY CHECKER. This software contains the basic business rules and also produces error reports
* ...

## Report Layout

Give the information about the layout of the report here.

## TERMS OF REFERENCE

### What is expected?

The expected system works by processing the employee data of an organization. The data is to be stored securely in the database. Statistical operations are done on the data to produce reports as desired by the client company.

### Time Frame

The delivery deadline for the system is 6 months from the date of start of theproject.

### What resources are available?

The resources that are available are.
* Personnel (however , they need training)
* Linux Operating System
* Networked systems
* Servers and Database Management System

## EXISTING SYSTEM

### Working of the Current System

You can write this topic only after doing the requirement analysis. Information from the requirements gathering phase that includes outcomes of interviews of the users, questionnaires filled by them and workflows that are currently functioning. In the example , the current system
* reads the data from Excel files and stores them into the database.
* validates the data on the basis of business rules and generate reports to show the errors in data.
* enables for correction of data
* creates MIS reports

### Problems in the Current System

The problems of the current system are:

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;4&lt;/page_number&gt;

---


## Page 5

Lab Manual

* For every data collection cycle , new Excel-based system needs to be developed.
* All the functions take a lot of time to complete.
* .........................................

## SYSTEM REQUIREMENTS

The following types of requirements can be freezed:

* The system should be able to read the data from Excel files and store it inthe Database.
* .........................................

## PROPOSED SYSTEM

### Project Outline

You may give the outline of the Proposed System here. Explain the terms anddata references in the data dictionary.

## DATA DICTIONARY

Some sample terms that are used in the documents :

<table>
  <tr>
    <th>Name</th>
    <th>Expansion of Name</th>
    <th>Where used</th>
    <th>Additional Description</th>
  </tr>
  <tr>
    <td>CLIENT</td>
    <td></td>
    <td>In Functional Diagrams and Class Diagrams</td>
    <td>This is an Object</td>
  </tr>
  <tr>
    <td>Excel Data Files</td>
    <td></td>
    <td>In Class Diagrams</td>
    <td>This is an Object</td>
  </tr>
  <tr>
    <td>Verify username & password</td>
    <td></td>
    <td>In Functional Diagrams</td>
    <td>This is a Process</td>
  </tr>
  <tr>
    <td>Data Validation</td>
    <td></td>
    <td>In Functional Diagrams</td>
    <td>This is a Process</td>
  </tr>
  <tr>
    <td>Generate Internal Reports</td>
    <td></td>
    <td>In Functional Diagrams</td>
    <td>This is a Process</td>
  </tr>
  <tr>
    <td>c_number</td>
    <td>Client Number</td>
    <td>In Class Diagrams</td>
    <td>This is an attribute of Client. It is a Unique field</td>
  </tr>
  <tr>
    <td>client_name</td>
    <td>Client Name</td>
    <td>In Class Diagrams</td>
    <td>This is an attribute of Client</td>
  </tr>
  <tr>
    <td>client_phnumber</td>
    <td>Client Phone Number</td>
    <td>In Class Diagrams</td>
    <td>This is an attribute of Client</td>
  </tr>
  <tr>
    <td>report number</td>
    <td>Report Number</td>
    <td>In Class Diagrams</td>
    <td>This is an attribute of Report</td>
  </tr>
  <tr>
    <td>........................................</td>
    <td>........................................</td>
    <td>........................................</td>
    <td>........................................</td>
  </tr>
</table>

### 1.3.2 Software Requirement Specification (SRS)

Normally IEEE standard is followed. A typical format of SRS is as follows:

**TABLE OF CONTENTS**

**Introduction**
* Purpose
* Scope
* Definition

&lt;page_number&gt;5&lt;/page_number&gt;

---


## Page 6

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Software Engineering Lab

*   Product and its function
*   Benefits and Goals
*   Overview

Overall Description

*   Product Description
*   Product Functioning
*   Functions of Project
*   Users of Project
*   Assumptions made

Specific Requirements

*   Interface Requirements
*   User Requirements
*   Hardware Requirements
*   Software Requirements
*   Logical Database Requirements

Basic Processing Actions of the System

Appendices

*   Input/Output Formats
*   Instruction for Security
*   Results of Fact Finding
*   Data Model
*   Functional Model
*   Process Specification.

A sample portion of SRS is given below:

**INTRODUCTION**

**Purpose**

SRS contains details of the proposed software system for the designers to design the system. Thus, SRS is a means of communicating the findings of the analysis stage to the design stage. The SRS includes .

*   Interface
*   Logical Database
*   Hardware
*   Performance and other constraints.

It also contains the assumptions made by the analyst and any systemic dependency.

**Scope**

The scope of SRS contains all the areas related to the project. The scope of SRS includes.

*   Proposed software description
*   Users of the proposed software
*   Functional requirements of the software
*   Assumptions and dependencies in the system
*   Constraints

**Definition**

.............................................
**Product and its**
**functions**
.............................................

&lt;page_number&gt;6&lt;/page_number&gt;

---


## Page 7

Lab Manual

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

**Benefits and Goals**

**Overview**

**OVERALL DESCRIPTION**

**Product Description**
The Client should be able to upload the raw data in Excel files into the Database. The raw data is then validated using .........

**Product Functioning**
*   The Raw data from the Clients is put into the database.

**Functions in the Project**
There are five functions of the system.
*   User Verification
    The User is asked to enters the Username and Password. The system checks the validity of Username and Password, otherwise the User is asked to do so again. A maximum of three valid attempts are given to the user.
*   Upload Raw Data
*   Validate Data
*   Put the Validated Data
*   Generating Reports

**Users of the Product**

**Assumptions**

**SPECIFIC REQUIREMENTS**

**Interface Requirements**
The Interface requirements include.
*   Easy to follow Interface
*   Very less graphics
*   No hidden buttons
*   Relevant error messages

**User Requirements**
After a careful study of the requirements of the Client, analysts have come up with a set of requirements.

**Hardware and Software Requirements**
There are three environments that have been created for the project, viz.,
*   Development environment
*   Quality Control environment
*   Production environment

The hardware requirements for all the platforms may be indicated here.

&lt;page_number&gt;7&lt;/page_number&gt;
&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 8

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Software Engineering Lab

## Logical database Requirements
The following information is to be stored in the database:.

*   The Clients Raw data
*   The Clients Validated data
*   Username and Password.

## BASIC PROCESSING ACTIONS OF THE SYSTEM
The basic processing actions of the system are.

*   Verification of the User
*   Upload Data

## APPENDICES
APPENDIX A
## INPUT / OUTPUT FORMATS
The input formats for the system contains the following screens.The convention used while making the input formats are.

☐ Square box is used for user input
☐ Rounded Square box is used for system display

## Login screen
The following screen that inputs the Username and Password from the Userfor authentication of the User to the system is.

<table>
  <tr>
    <td>Login Id</td>
    <td>____________</td>
  </tr>
  <tr>
    <td>Password</td>
    <td>____________</td>
  </tr>
  <tr>
    <td>Close</td>
    <td>Login</td>
  </tr>
</table>

APPENDIX B
## INSTRUCTIONS FOR SECURITY
Security is an integral part of any system. Clients send their confidential data with trust and it is our foremost duty to protect the security and privacy of the data of the Clients.

APPENDIX C
## RESULTS OF FACT FINDING
Working of the Current System and its Problems

APPENDIX D
## DATA MODEL
### Classes involved in the Project
*   Clients
*   Excel Data Files
*   Reports

&lt;page_number&gt;8&lt;/page_number&gt;

---


## Page 9

Lab Manual

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

**Association between the classes**
* Clients fill data in the Excel Data Files (M .. M)
* Clients generate Reports (M ... M)

**E-R/Object Diagram for the system**

<mermaid>
graph LR
    A[CLIENTS] -->|creates| B[REPORTS]
    C[EXCEL DATA FILES] -->|fills data| A
</mermaid>

**Attributes of the Entities are**

<table>
  <tr>
    <th>Object Classes</th>
    <th>Attribute</th>
  </tr>
  <tr>
    <td>Clients</td>
    <td>
      number<br>
      name<br>
      address<br>
      phone number<br>
      fax<br>
      email
    </td>
  </tr>
  <tr>
    <td>Excel data Files</td>
    <td>
      excel file number<br>
      client number
    </td>
  </tr>
  <tr>
    <td>Reports</td>
    <td>
      report number<br>
      report name<br>
      client number
    </td>
  </tr>
</table>

APPENDIX E

**FUNCTIONAL MODEL**

One sample DFD at level 1 is containing the processes:
* Username and Password verificaiton
* Data Migration
* Validation of Migrated data
* Generate Reports

You can make various levels of DFDs

<mermaid>
graph TD
    subgraph Level 1
        A[Username & password] --> B(Username & password verification)
        C[Excel data file] --> D(Data Migration)
        B --> E(Validation)
        D --> F(Generate Reports)
        E --> G(Generate Reports)
        F --> H[Raw Data Storage]
        B -- "Bad password & username" --> I[ ]
        C -- "Password & Username OK" --> H
        H -- "Errors and data" --> G
        G -- "Reports" --> H
    end
</mermaid>

&lt;page_number&gt;9&lt;/page_number&gt;

---


## Page 10

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Software Engineering
Lab

# PROCESS SPECIFICATION

Let us give one sample process verification.

**Process:** Username and Password Verification
**Input:** Username & Password
**Output:** Access grant or denied message

*Processing*
The Client enters the Username and Password and clicks the Login button.

The system connects with the DBMS and verifies them in the related database. If both are valid: allow user to enter the system with the allowed access rights for that user. Otherwise prompt wrong Username-Password message and take the user to the screen where s/he can re-enter the Username-Password.

*Interface Description*
The interface contains the text boxes where the user can enter Username andPassword. It also contains a Login button for login and a Close button on closing the application.

*Internal Data Structure*
The process uses the encrypted username and password table that alsocontains information about the access permissions.

---

## 1.4 DESIGN DOCUMENT

### SCOPE
Define the System Objectives here
............

### Architecture Design
Give the architecture of the system based on the analysis and flow models.

### DATA DESIGN
Refine the E-R diagram if needed and make one table for each entry and datastore and table for all M.M relationships.

For example, the Client table may be:

<table>
  <thead>
    <tr>
      <th>COLUMN HEADING</th>
      <th>CONSTRAINTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>client_no</td>
      <td>Primary Key</td>
    </tr>
    <tr>
      <td>client_number</td>
      <td>Not Null</td>
    </tr>
    <tr>
      <td>client_addr</td>
      <td>Not Null</td>
    </tr>
  </tbody>
</table>

### INTERFACE DESIGN

#### Human-Machine Interface Design Rules
Follow the basis rules for the interface design. These can be classified intothree main types:
* External Interface design
* Interface to the External Data
* Interface to the external system or devices

#### External Interface Design
* Easy to follow Interface
* Zero or very less graphics as not being used commercially

&lt;page_number&gt;10&lt;/page_number&gt;

---


## Page 11

Lab Manual

*   No hidden buttons
*   Proper error messages

**Interface to the External Data**

The system has to use proper external data. The system makes a connection with the DBMS to do so. The rules that have to be followed while interfacing with the external data are:

*   You must do the type checking.
*   Field overrun that is maximum size should be enough to accommodate the largest data of that type
*   It is always better to encrypt the data and then store it in the database.

**Interface to the External System or Device**

**PROCEDURAL DESIGN**

**Verification of the User**

*Algorithm*
Input: ..........
Output: ..........
STEPS

Ask the Client to enter Username-Password.

Check Username and Password combination in the encrypted database.
If the Username and Password is correct then give permission with allowedaccess rights.

Else, access is denied and the enter Username and Password screen isshown again. This cycle will be done a maximum of three times

*Flow Chart*

<mermaid>
graph TD
    A([START]) --> B[Enter Username and Password]
    B --> C[Verify from Database]
    C --> D{Is Correct?}
    D -- Yes --> E[Allow permission as per access rights]
    D -- No --> F[Print bad Username and Password]
    F -->|Maximum 3 chances| B
    E --> G([STOP])
</mermaid>

&lt;page_number&gt;11&lt;/page_number&gt;

---


## Page 12

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Software Engineering
Lab

# INTERFACE DESIGN

## Login Screen

&lt;img&gt;Login Screen Screenshot&lt;/img&gt;

# OUTPUT / REPORTS DESIGN

Design your output reports

# DATA SECURITY AND RIGHTS

Security is the integral part of any system. You can use encryption and authentication or any other security mechanism as the need may be.

# 1.5 TESTING

A sample test case may be:

## Login Screen

<table>
<thead>
<tr>
<th>S.No.</th>
<th>Test Case ID</th>
<th>Do</th>
<th>Expected Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>1.</td>
<td>QT1-001</td>
<td>Enter user id in the text box specified.<br>User id must not be more than 510 characters and it should not contain any special char and no spaces including in the start.<br>Enter password in the text box specified. Password must not be more than 10 characters<br>Click on the Login button.</td>
<td>Successful login in to the system if the values are found in the database</td>
</tr>
<tr>
<td>....</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

&lt;page_number&gt;12&lt;/page_number&gt;

---


## Page 13

Lab Manual

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

# TEST LOG

<table>
  <thead>
    <tr>
      <th>Function</th>
      <th>Purpose of Set of Test Cases per Area</th>
      <th>Test Case ID(s)</th>
      <th>No of Test Cases run</th>
      <th>Number of Test Cases Successful</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Login</td>
      <td>The verificaiton of username and password</td>
      <td>QT1-001</td>
      <td>8</td>
      <td>100%</td>
    </tr>
    <tr>
      <td>.....</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

---

## 1.6 IMPLEMENTATION

It must contain the proper comments. The coding should be structured as per software architecture.

### VALIDATION CHECKS

#### Verification of the User

*   Both User Id and Password are mandatory
*   The size of User Id must be 10 characters long

### ERROR AND EXCEPTION HANDLING

A proper mechanism of Error Handling is necessary in any system.

### COMMENTS

Comments are an integral part of any system. Like any properly developed and maintained system with high quality, this system too has sufficient comments and description of the processes, functions, classes, and data structures.

### CODING STANDARDS

The defined coding standards of the software developers may be followed. A sample clause in coding standard may be: “A consistent naming pattern is one of the most important elements of predictability and discoverability in a managed code. For each type, you must follow the defined capitalization styles, case sensitivity and word choice.

---

## 1.7 LIST OF PROBLEMS

The following is the list of problems that are to be attempted during the prescribed lab sessions.

### Project Planning

Session 1: Suppose that you need to build software for a Railway Reservation System. Write a statement of scope that describes the software.

Session 2: Estimate the effort and cost required to build the above software. Use any estimation technique.

### Requirements Analysis

Session 3: Develop SRS (Software Requirements Specification) for the Railway Reservation System (RRS).

Session 4: (a) Draw DFDs up to appropriate levels for the RRS.
(b) Draw ERDs for the RRS. Describe the relationships between different entities.
(c) Design Data Dictionary for RRS.

&lt;page_number&gt;13&lt;/page_number&gt;

---


## Page 14

&lt;watermark&gt;ignou THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Software Engineering Lab

## Design
Session 5: Develop a modular design for RRS.
Session 6: Develop user interface design for RRS.

## Testing
Session 7: Write a program in ‘C’ language for the multiplication of two matrices . using pointers.
Session 8: Develop a set of test cases that will completely test the program in session 7. The test case should be separately developed for Unit testing, Module testing and Integration testing.

## Web Software Engineering
Session 9: Design a web page that accepts a matrix as input and computes its transpose. The web page should have two text boxes and a submit button labelled as **Input Elements**. After entering the number of rows of the input matrix in the first text box and number of columns of the input matrix in the second text box of the web page, SUBMIT button should be clicked. Once clicked, a number of text boxes which are equivalent to the number of elements in the matrix will appear along with a submit button at the bottom labelled as **Compute Transpose**. When the **Compute Transpose** button is clicked, the transpose of the input matrix has to be displayed.
Session 10: Develop test cases for the web pages of 9(a). Then, develop test report after testing using the test cases developed.

## Software Quality
Session 11: Write a Program that is correct but of not good quality. Justify your answer.
Make necessary assumptions.
Session 12: Write a Program that is correct but still not reliable. Justify your answer. Make necessary assumptions.

## Software Change Management
Session 13: Develop “Railway Reservation System” as per specifications given in Sessions 1, 3, 4,5 and 6.
Session 14 : Demonstrate the Software developed in Session 13 to any other person and make a list of Changes suggested by him/her. Implement changes in Software following the Change Control process and demonstrate the updated Software to the same person.

## Advanced Software Engineering
Session 15 : Select a software that you use regularly such as MS-office, Gmail, MS-Excel etc. Create a set of usage scenarios for the software.
Session 16 : Select a small portion of any program written by you. Check if the portion of code selected by you is having constructs that violate the structured programming paradigm. If yes, then rewrite the code to conform to structured programming paradigm. If no, check another portion of code.
Sessions 17 and 18 : Have a look at the output of any program that was not written by you. Preferably, look at an application that is not developed by you and write the program for the development of that application or a portion of that application.
Sessions 19 and 20 : Assume that you interested in developing a “Library Information System (LIS)”. Visit any Library. As a visitor of Library, make a list of requirements that need to be fulfilled by LIS. Now, develop Software for LIS. Ensure yourself that LIS developed by you is fulfilling the requirements. Preferably, try to obtain requirements for LIS from any person who visits a library, develop LIS and then get it

---


## Page 15

validated by him/her.

## 1.8 SUMMARY

This section provides an introduction to software engineering lab in action. In this lab section, we provide some basic information on how one can prepare the project plan, Data dictionary, software requirement specification, Data model, functional model, different kinds of design tools, data analysis, testing. You can find more details on these topics in the MCS-213 : Software Engineering course. A learner should solve the problems given in this section with the help of CASE/software tools to get the best benefits from this section.

&lt;page_number&gt;14&lt;/page_number&gt;