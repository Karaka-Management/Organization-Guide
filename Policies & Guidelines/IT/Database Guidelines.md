# Database Guidelines

## Access permissions

Access permissions to the databases must be defined as granular as reasonably possible.

* Admin: Only for Head of IT and CTO
  * This account however must only be used in exceptional situations
* Application specific user and permission settings:
  * some applications need one main user with admin permissions on a specific table
  * some application need multiple users where the different users have different permissions
* All other database users must only be have read-only permissions 

## Direct data changes

No direct data changes are allowed in the databases. All changes in the database must be performed by the applications managing the database. 

## Logging

Logging must be always enabled for errors and warnings. Additional logging can be enabled if deemed helpful by the Head of IT or CTO. Error or warning logs must be sent to the head of IT and CTO on a daily basis, if any occurred. The head of IT or CTO must take appropriate steps to solve the errors and warnings in a timely manner.



2022-01-01 - Version 1.0

