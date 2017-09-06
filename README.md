# BusinessTitleChange
The purpose of this reference application is to show how to initiate a Studio via a post to the listener service via REST API. The Studio integration system initiates the "Title Change" business process. In GMS, approval is required by Logan McNeil for business title changes.

### Technical Details
* Workday Studio Listener API
* Workday Studio
* Workday SOAP API

## Installation Instructions
- Import the .clar file into Workday Studio and deploy to the target tenant.
- Expand the BusinessTitleChange.zip file
  - Open project in IntelliJ and push to the target tenant
- In the tenant:
  - Access the "Create Custom Task" task:
    - Title: Change Business Title
    - Business Object: Employee
    - Application: BusinessTitleChangeApp
    - Site: BusinessTitleChangeSite
    - Route Path:/home?workerId={customTaskObjectId}

## How to use this application?
- Log in to the target tenant as a manager, ex. "Logan McNeil"
- Search for a worker, ex. "Ethan Kelly"
- Select the related action off the worker, Employee > Change Business Title
- The worker's current business title is displayed
- Enter the new business title and click OK
- "Business Title Change Submitted" appears indicating the change has been submitted and the Studio integration invoked
- Progress of the integration system can be monitored via "Process Monitor"
- Once the integration system is complete, login as an Approver to the "Title Change" business process for the target worker
  - Access the supervisor's inbox and "Approve" the business title change
- Access the target employee, the business title has been changed.
