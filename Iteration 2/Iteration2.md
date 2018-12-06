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
|BrowserUI|Encapsulates the entire frontend of web application this includes the login interface and Web Client interface|
|BrowerUIController|Responsibile for aqquiring user input data and providing the prensentation layer with necessary information |
|Request Manager|Responisble for communication with the server side |
|Request Services|Responsible for recieve requests for the client side|
|Login Controller|Controls business logic related to user logins|
|Course Controller|Controls business logic related to searching, course creation/deletion|
|AccessModule|Responible for Accessing data based on Controllers in Business Logic Server Side|
|TimeServer| Responsible for persistent operations related to time servers|  
  
UC-1 - Login
The below diagram shows the sequence of components for UC-1 where the user logs in to the system  
![Sequence Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%202/UC-1%20-%20sequence%20diagram.jpg)

Browser UI  
* Boolean Initilize() - Opens the network representation so the user can interact with it  
* Validity DisplayLogin() - returns a page based on the validity of the login  

BrowserUIController  
* Validity Login(User,Pass) - Returns the reference based on the user input  

RequestManager 
* Response SendRequest() - Request the login validity from the root region  

RequestService  
* Validity requestLogin(User,Pass) - This method recieves a request, and access the service interface  

LoginController  
* Validity ValidId() -  returns the validity of the login based on the info given  

### Step 7 - Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
|Not Addressed| Partially Addressed|Completly Addressed|Design Made during Iteration|
|---|---|---|---|
|  |  | UC-1 | Modules across the layers and the preliminary interfaces to support this use case has been indentified |
|  |  | UC-2 | Modules across the layers and the preliminary interfaces to support this use case has been indentified |
|  |  | UC-4 | Modules across the layers and the preliminary interfaces to support this use case has been indentified  |
|  |  | UC-5 | Modules across the layers and the preliminary interfaces to support this use case has been indentified |
|  | QA-1 |  | The elements that support the associated Use case has been identified |
|  | QA-2 |  | The elements that support the associated Use case has been identified |
|  | QA-3 |  | The elements that support the associated Use case has been identified |
|  | CON-1 |  | No relevant decisions were made |
| CON-2 |  |  | No Relevant decisions were made |
| CON-4 |  |  | No Relevant Decision were made |
| CON-5 |  |  | No Relevant Decision were made |
|  | CRN-2 |  | New Modules that have been considered requires the knowledge of the developers |
| CRN-3 |  |  | No Relevant Decision was made |
