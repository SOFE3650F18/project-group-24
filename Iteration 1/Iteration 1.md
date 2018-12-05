# Iteration 1
### Step 1 - Review Inputs
| Category | Details |
|---|---|
| Design Purpose | This is a greenfield system from a mature domain |
| Primary Functional Requiremenst | UC-1, UC-2, UC-4, UC-5 |
#### Quality Attribute scenarios
|Scenario ID| Importance to User| Diccuulty of Implementation|
|---|---|---|
|QA-1|High|Easy|
|QA-2|High|Hard|
|QA-3|High|Medium|
|QA-4|High|Easy|
|QA-5|Medium|Easy|
|QA-6|Low|Hard|

QA-1, QA-2, QA-3 are included as drivers
#### Constraints
All Constraints listed in Assignment2/Con.md are included as drivers
#### Architectural Concerns
All architectural concerns are included as drivers
### Step 2 - Establish Iteration Goal by Selecting Drivers
The iteration goal is to achieve CNR-1  
![Context Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%201/Context%20Diagram%20for%20CM%20system.PNG)

### Step 3 - Choose one or more Elements to refine
The element to refine is the entire CMS system, this is due to the fact that the system to be developed is a greenfield system

### Step 4 - Choose one or more design concepts to work with
| Design Decisions and Location | Rationale |
|---|---|
| Logically structure the client part of the system using Web application |This was chosen due to the fact that web applications are easier to develop, easily accessible on multiple devices, scalable and maintainble  |
| Logically structure the server part of the system using service application | This was chosen due to the fact that the alternatives would not meet the requirements when it comes to service applications  |
| Physically structure the application using the three tiered deployment pattern | Due to the fact that the system involves a user accessing a browser and through that to access a data base it was found that the three tier deployment pattern is ideal |

### Step 5 - Instantiate Architectural Elements, Allocate Responsibilities
| Design Decisions and Location | Rationale |
|---|---|
| Create a user interface | This will help the completion of QA-1 |
| Create a module dedicated to accessing time servers | This will help the completion of QA-3 |
| Create a database to store course information | This will help the completion of QA-1 and QA-2 |

### Step 6 - Sketch Views and record design decisions
![Views](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%201/Layer.png)

| Element | Responsibility |
|---|---|
|Client Prensentation|This layer contains the modules that control the UI|
|Business Logic CS|This layer contains the modules that perform business logic on the client side|
|Data Layer CS|This layer contains the modules responisble for communication with the server|
|Browser| this layer allows user interaction |
|Browser Process Module| this module is responsible for control flow of the system |
|Login CS| this layer contains a module used for login on the client side |
|Search CS| this layer contains a module used for search of courses on the client side |
|Create CS| this layer contains a module used for creation of courses on the client side |
|Communcation Moudle| this module is used to connect the client side to the server side |
|Services SS|This layer contains the modules that controls the interactions with the server|
|Business Logic SS|This layer contains the modules that perform business logic on the server side|
|Data Layer SS|This layer contains the modules responisble for accessing data and communication with the time server|
|Service Interface| allows the server modules to interact with the client side |
|Login SS| this layer contains a module used for login on the client side |
|Search SS| this layer contains a module used for search of courses on the client side |
|Create SS| this layer contains a module used for creation of courses on the client side |
|Access Module| this module access the database insuring that the database is accessed correctly |
|Time Server Access Module| this module is responsible with communicating with the time servers |
|Secruity| insures the security of the server side |
|Operation Management Module| This module insures the operations done by the client are handled correctly |

![Deployment Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%201/Deploy.png)

| Element | Responsibility |
|---|---|
|User Workspace| The users device that accesses the client side logic of the website|
|Application Server|Hosts the server side logic of the web application|
|Database Server| Contains the relation database of the system|
|Time Server| External Time Servers|

| Relationship | Description |
|---|---|
| Between Application Server and Database server|  Communication with the data base will be conductied using MySQL|
|Between Application Server and Time Server| Uses the Simple Network Management Protocol (SNMP) | 


### Step 7 - Perform Analysis of current Iteration

|Not Addressed| Partially Addressed|Completly Addressed|Design Made during Iteration|
|---|---|---|---|
|  | QA-1 |  |  |
|  | QA-2 |  |  |
|  | QA-3 |  |  |
|  | CON-1 |  |  |
| CON-2 |  |  |  |
|  | CON-3 |  |  |
| CON-4 |  |  |  |
| CON-5 |  |  |  |
|  |  | CRN-1 |  |
|  | CRN-2 |  |  |
| CRN-3 |  |  |  |
