# IT Security

## Password

### Format

Passwords protect confidential company data, as well as customer and supplier data. The length and the combination of different character types (i.e. lower case letters, upper case letters, numerics and special characters) can have a significant impact on the strength of a password. For this reason the IT department should configure the password settings if possible in such a way that the following format must be used:

* At least 8 character length
* At least one upper case letter
* At least one lower case letter
* At least one special character
* At least one numerical character

### Change interval

Additionally, if it is possible to define a password change interval it should be set to once a year. This way passwords don't become stale and in case of a password leak get rotated out. Shorter password change intervals could lead to friction for the employees resulting in a security fatigue. 

### Additional protection

For direct server access ssh keys must be used instead of passwords. In addition, these ssh keys should be password protected according to the above mentioned format specifications. If possible second factor authentication should be enabled for direct server access. This second factor authentication should be bound to the owner of the ssh key (i.e. SMS authentication, app authentication, ...)

Sometimes it becomes necessary for third party partners to access the servers (i.e. maintenance or support), in such a case second factor authentication is mandatory. The second factor authentication for third parties must be configured in such a way that only the head of IT can approve the access.

## Permissions

It is strongly recommended to use the basic organization schematic and job description for every area as a basis to define user permissions. Based on the job descriptions and user tasks, groups should be generated with the appropriate permissions. The permission management through groups is preferred since it's much more verbose and shows a clear structure. While permissions on user basis are in some cases more convenient for quick permission handling they indicate that the actual job function compared to the organization layout is not coherent with the actual tasks that person is performing. Permission handling on user level is strongly advised against and re-structuring groups and creating new groups is much cleaner even if in some cases a group only has one account assigned. Permissions for accounts should also get re-evaluated on a regular basis in order to prevent non-active accounts or accounts whose job description changed to have permissions they no longer need.

## Updates

Updates are very important not only to implement the newest features but also to close potential security vulnerabilities. Updates should be tested in a testing environment and then migrated to the live environment.

2022-01-01 - Version 1.0

