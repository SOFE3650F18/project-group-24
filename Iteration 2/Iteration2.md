# Iteration 2
### Step 1 & 2 - Establish Iteration Goal by Selecting Drivers

The goal of this iteration 2 is to address the gengeral architectural concerns to support primary functionality of CMS
The primary Use Cases will be considered in this iteration:

  UC-1
  UC-2
  UC-4
  UC-5
  
### Step 3 - Choose One of More Elements of the System to Refine

The elements of system that this iteration will refine are the modules identified in the reference architectures in the previous interation

### Step 4 - Choose One of More Design Concepts That Satisfy the Selected Drivers
|Design Decisions and Location|Rationale and Assumptions|
|---|---|
|Create a Domain Model for the application| Creating a domain model will illustrate and identifity the important entities and relastionships in the system |
|Identifiy domain objects of function requirements| Each distinct Functional object will be encapsulated in a domain object|
| Convert Domain Objects into Components | Domain objects represent a set of Functional objects |

### Step 5 - Instantiate the Architectural Elements, Allocate Responsibilities and Define Interfaces
|Design Decisions and Location|Rationale|
|---|---|
| Create a initial domain model | The entities that relate to the use cases will be indentified and modelled, to create a initial domain model |
| Map the domain objects to the use cases| Analyze the use cases to find which domain objects are in relation to which use case |
| Place domain objects in the different layers of the system | This will be done to insure that the functionalities of each module is identified and that the module is placed in the correct layer of the system |
| Associate Modules to the data layer | Mapping the modules to the data layer encapsulating the functionality |
### Step 6 - Sketch Views and Record Design Decisions

![Initial Domain Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%202/Domian.png)

Figure 2.0

|Element|Responsibility|
|---|---|
|User| User login interface|
|WebClient| Specific User Interface loaded for different types of Users( Student,Lecturer,Administrator)|
|WebServer| Backend Services of the web application, responisble for handling security, hanlding time, and handling user inputs|
|Database|Stores Data|
|Security| Insures application is secure and user type and permissions are valid|

![Context Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%202/Domain%20Objects.png)

Figure 2.1

![Context Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%202/LayerB.png)

Figure 2.2

|Element|Responsibility|
|---|---|
|BrowserUI||
|BrowerUIController||
|Request Manager||
|Request Services||
|Login Controller||
|Course Controller||
|EventDataMapper||
|TimeServer||

### Step 7 - Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
