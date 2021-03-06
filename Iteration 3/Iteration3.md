# Iteration 3
### Step 1 & 2 - Establish Iteration Goal by Selecting Drivers
For this Iteration we have chosen to focus on QA-2 - New courses and departments are added to the systems static database. The additions are added successfully with minimum 4 hours downtime of the server/month, And QA-3 - system crashes. The system creates back-ups of the entire system to restore partial and complete backups of a specific date
### Step 3 - Choose One of More Elements of the System to Refine
The elements to be refined are below  
* Course creation element
* Course information and system storage element
### Step 4 - Choose One of More Design Concepts That Satisfy the Selected Drivers
|Design Decisions and Location|Rationale and Assumptions|
|---|---|
|Introduce a create course interface module for users with appropiate premissions| By creating a course creation module, the system will be able to directly add courses into the system while experiencing minimum down time |
| Backup module | Introduce a module that will periodcally create a backup of the system or before an update is scheduled, to combat critical errors and minimum down time|
| System Monitoring module | Monitors the system to ensure it is running without any problems|
|Back up Servers | Servers that are ready incase other servers are down|

### Step 5 - Instantiate the Architectural Elements, Allocate Responsibilities and Define Interfaces

|Design Decisions and Location|Rationale|
|---|---|
|Create Course Module|Deploying this module as an extension |
| System Monitoring module | Will scan the system, and servers and detect causes of concern. Depending on the concern the module will either initiate back up servers to handle the error, or  reload using the systems backups generated|

### Step 6 - Sketch Views and Record Design Decisions
Refined Domain Diagram

![Refined Domain Diagram](https://github.com/SOFE3650F18/project-group-24/blob/master/Iteration%203/RefinedInitial.png)


### Step 7 - Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
|Not Addressed| Partially Addressed|Completly Addressed|Design Made during Iteration|
|---|---|---|---|
| QA-1 | | |No Relevant Decision was made|
|  | |QA-2 | Introduction of the Create course interface module completley addresses the creation of new courses and departments|
|  | | QA-3| Introduction of the System Monitoring module completley addresses downtime restrictions and system overloads and crashes|
| CON-2 |  |  | No Relevant Decision was made|
| CON-5 |  |  | No Relevant Decision was made|
|  | CRN-2 |  | Modules that have been considered requires the knowledge of developers|
| CRN-3 |  |  | No Relevant Decision was made|

