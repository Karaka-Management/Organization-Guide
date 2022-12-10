# IT General Controls (ITGC)

## Abbreviations

* No.: Number
* A: Application
* OS: Operating System
* DB: DBMS
* N: Network
* O: Others

## General

| No.  | Component | Control Area | Question                                                     | Answer                                                       | Evidences                                       |
| ---- | --------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------- |
| 1    | IT        | IT Strategy  | Do you have a IT investment strategy or plan?                | Yes, investments are evaluated at least annually during the budget process. Additionally, resources are also checked regularly (e.g. executive committee meeting). | Budget<br />Executive Committee Meeting Minutes |
| 2    | IT        | IT Strategy  | Are the IT investment strategies or plans reviewed and approved by the management? | Yes, during the budget process and if outside the budget in the executive committee meeting. | Budget<br />Executive Committee Meeting Minutes |

## System Development and Maintenance

### Points to consider

| Overview             | Component | Situation                                                    | Evidences                          |
| -------------------- | --------- | ------------------------------------------------------------ | ---------------------------------- |
| Frequency of changes | A         | Often changes are required for various reasons (e.g. functionality enhancement changes in business processes, etc.) | CHANGELOG<br />Software validation |
| Frequency of changes | OS, DB    | Changes are made for each release of security patches/upgrades | Software validation                |
| Frequency of changes | N, O      | Changes are made for each release of patches/upgrades        | Software validation                |

### Assessment of Design Effectiveness

| No.  | Question                                                     | Component       | Situation                                                    | Evidences                                                    |
| ---- | ------------------------------------------------------------ | --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | How are policies and procedures for development and maintenance prepared? | A, OS, DB, N, O | Policies and procedures for development and maintenance are described in a formal way. Documentations are prepared by the IT team and authorized by the head of IT | Process: Development<br />Process: Support & Service<br />Policies: IT |
| 2    | How are roles and responsibilities concerning development and maintenance defined? | A, OS, DB, N, O | Roles and responsibilities concerning development and maintenance are clearly defined in the IT process and policies. IT personnel incl. service vendors perform changes | Process: Development<br />Process: Support & Service<br />Organigram |
| 3    | How are changes tested and their results approved?           | A, OS, DB, N, O | Before updates for third party software are performed on the servers they are tested in a testing environment. Self-developed software changes are tested according the development process. | Third party: Software validation<br />Process: Development<br />Internal: Test protocols |
| 4    | How are changes approved for their migration to the production environment? | A, OS, DB, N, O | The change in the production environment is approved by the head of IT for third party software and for self-developed changes according the development process. | Third party: Software validation<br />Process: Development<br />Internal: Merge protocol |
| 5    | What procedures are in place for preventing/detecting unauthorized changes to the production environment? | A, OS, DB, N, O | Only the head of IT can install updates on the servers. Only the head of IT has the necessary IT authentication and IT permission. For self-developed changes all changes, merges can only be performed from authorized personnel and all merges are logged in merging protocols. | Permission List                                              |

## System Security (Access Control)

### Points to consider

| Question                                                     | Component    | Situation                                                    | Evidences                       |
| ------------------------------------------------------------ | ------------ | ------------------------------------------------------------ | ------------------------------- |
| What is the number of user?                                  | A            | Large number of users in large number of user locations/departments | Organigram<br />Permission List |
| What is the number of user?                                  | OS, DB, N, O | Number of users and user locations/departments is limited    | Organigram<br />Permission List |
| Frequency of "direct data change"<br /><br />(*"direct data change" means to change data with the utilities such as SQL software*) | N            | No direct change to data has been required since its implementation, as the system has been in stable operation |                                 |

### Assessment of Design Effectiveness

| No.  | Question                                                     | Component       | Situation                                                    | Evidences                                                    |
| ---- | ------------------------------------------------------------ | --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | Describe the user authentication process.                    | A, OS, DB, N, O | User-ID and password are assigned on an individual basis and necessary for accessing digital data. | Application login screen<br />OS login screen<br />DB login screen<br />Server login screen |
| 2    | How are user and access rights granted to each user documented? | A               | A list of users is prepared with the rights granted to each user. This list is generated from the system | Application permission List                                  |
| 2    | How are user and access rights granted to each user documented? | OS, DB, N, O    | A list of users is prepared with the rights granted to each user | Permission List                                              |
| 3    | Do you have policies and procedures for user-ID administration? | A, OS, DB, N, O | Policies and procedures for user-ID administration (add, change, remove, and periodic user validation) are described in an authorized  documentation. The documentation is prepared and authorized by the head of IT |                                                              |
| 4    | How do you perform user validation?                          | A, OS, DB, N, O | Periodic user validation is performed, this means each user's access rights are reviewed on a periodic basis. Performed both in terms of existence of user and the detailed access rights granted to each user-ID on an annual basis by the head of IT |                                                              |
| 5    | How are user-ID administration requests approved?            | A, OS, DB, N, O | User-ID administration requests are approved by managers in user dpt. and/or IT dpt, as appropriate. Records are maintained in the change management |                                                              |
| 6    | How do you handle access to IT functions?                    | A, OS, DB, N, O | Access to privileged IT functions is restricted to appropriate personnel. Logs of the use of such privileged user-IDs are reviewed annually |                                                              |
| 7    | Describe the password/authentication complexity.             | A, OS, DB, N, O | Password complexity is configured based on a minimum length of 8, at least one upper case letter, at least one lower case letter, at least one special character and at least one numeric value. Password changes must happen every 3 months |                                                              |
| 8    | Which policies and procedures for direct change to data do you have? | DB              | Only the head of IT may perform and authorize direct changes to the data |                                                              |
| 9    | How do you handle direct data changes?                       | DB              | Direct changes to data must be authorized by the head of IT. No direct changes to data where made |                                                              |
| 10   | Do you test data after direct changes?                       | DB              | Direct change to data are tested and documented. No direct changes to data where made |                                                              |
| 11   | How do you restrict direct data changes?                     | DB              | Only the head of IT has write/change permissions to the DB   |                                                              |
| 12   | How do you restrict access to applications and OS?           | A, OS           | Data and programs on a stand-alone PC are in control of the user. User permissions for applications, data on the server and OS are restricted appropriately. |                                                              |
| 12   | How do you restrict access to server hardware and databases? | DB              | Server(s) are located in a machine room with appropriate physical access control. |                                                              |

## System Operation and Administration

### Points to consider

| Question                              | Situation                                                    | Evidences |
| ------------------------------------- | ------------------------------------------------------------ | --------- |
| Frequency of problems/incidents       | Material failure such as miscalculation or malfunction of the system has not occurred. |           |
| Frequency of changes to job schedules | Changes to job schedules occur frequently but most of them are those in execution date |           |
| Frequency of Non/Scheduled job        | Non/Scheduled job is required in some cases but its frequency is low |           |

### Assessment of Design Effectiveness

| No.  | Question                                                     | Situation                                                   | Evidences |
| ---- | ------------------------------------------------------------ | ----------------------------------------------------------- | --------- |
| 1    | Do you have policies and procedures for backups?             | Exists                                                      |           |
| 2    | How do you ensure the completion of backups?                 | All backup job records are reviewed by monitoring personnel |           |
| 3    | How do you test backups?                                     | Every backup is automatically tested                        |           |
| 4    | Which policies and procedures for job operation do you have? |                                                             |           |
| 5    | How are job schedule changes approved?                       |                                                             |           |
| 6    | How do you prevent/detect unauthorized changes to job schedules? |                                                             |           |
| 7    | How is the completion of job execution ensured?              |                                                             |           |
| 8    | Requests for non-scheduled job execution are authorized      |                                                             |           |
| 9    | Which policies and procedures for identifying, resolving, reviewing, and analyzing IT operations problems or incidents exist? |                                                             |           |
| 10   | How are IT operations problems or incidents identified, resolved, reviewed, analyzed, and follow-ups evidenced? |                                                             |           |

## Outsourcing Contract Management

### Points to consider

| Question                      | Situation                                                    | Evidences                 |
| ----------------------------- | ------------------------------------------------------------ | ------------------------- |
| What services are outsourced? | Some of the services are outsourced concerning development/maintenance related to ITGCs | Software vendor contracts |

### Assessment of Design Effectiveness

| No.  | Question                                                     | Situation                                                    | Evidences |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------- |
| 1    | Which outsourced IT services exist and how are they documented? | Outsourced service are clearly defined and agreed with the service vendor in writing e.g. in contract and/or SLA |           |
| 2    | How do you ensure the compliance of vendors?                 | Service vendor's compliance to the service level is periodically reviewed |           |
| 3    | How do you ensure the quality of the service vendors?        | Regular review of service vendors is conducted in terms of appropriateness of the services defined, service vendor's ability to render the required service level, etc. |           |

2022-01-01 - Version 1.0
