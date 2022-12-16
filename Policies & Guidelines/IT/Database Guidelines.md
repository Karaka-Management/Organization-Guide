# Database Guidelines

The databases contain critical organization, customer and supplier data. In most cases data is created, deleted and manipulated through software which provide a workflow with data validation to ensure the correctness of the change. Manual changes, damages and unprofessional interaction with a database may cause severe damage for the organization.

## Goal

Manual interaction with any database must be kept at a minimum. Strict limitations are necessary to ensure the data integrity in the database. 

## Implementation

### Access permissions

Access permissions to the databases must be defined as granular as reasonably possible.

* Admin: Only for Head of IT and CTO
  * This account however must only be used in exceptional situations
* Application specific user and permission settings:
  * some applications need one main user with admin permissions on a specific table
  * some application need multiple users where the different users have different permissions
* All other database users must have read-only permissions 

### Direct data changes

No direct data changes are allowed in the databases. All changes in the database must be performed by the applications managing the database. 

In case they are absolutely necessary direct data changes must only be performed by the head of IT or by the third party software provider and supervised by the head of IT. Direct data changes must be tested and documented by the head of IT.

### Logging

Logging must be always enabled for errors and warnings. Additional logging can be enabled if deemed helpful by the Head of IT or CTO. Error or warning logs must be sent to the head of IT and CTO on a daily basis, if any occurred. The head of IT or CTO must take appropriate steps to solve the errors and warnings in a timely manner.

## Responsible

The responsibility for the database lies with the head of IT. No other employee may directly interact witht the database except for backups and restarting the database in case of failures.

2022-01-01 - Version 1.0

