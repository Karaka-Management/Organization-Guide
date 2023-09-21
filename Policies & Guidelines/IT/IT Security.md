# IT Security

## Goal

These security guidelines and policies should reduce the risk of a unauthorized data and hardware access, data and hardware manipulation, data loss and damages to hardware in order to ensure smooth IT operations.

## Implementation

### Password

#### Format

Passwords protect confidential company data, as well as customer and supplier data. The length and the combination of different character types (i.e. lower case letters, upper case letters, numeric and special characters) can have a significant impact on the strength of a password. For this reason the IT department should configure the password settings if possible in such a way that the following format must be used:

* At least 8 character length
* At least one upper case letter
* At least one lower case letter
* At least one special character
* At least one numerical character

#### Change interval

Additionally, if it is possible to define a password change interval it should be set to once a year. This way passwords don't become stale and in case of a password leak get rotated out. Shorter password change intervals could lead to friction for the employees resulting in a security fatigue.

### Access Restrictions

Every user must have their own user-ID and authentication. The user can be assigned to multiple groups. Permissions can be granted for groups and individual users.

In general only whitelist user access permissions instead of blacklisting them. In other words don't be afraid to create multiple accounts or user groups for single applications and only give them reading/writing/execution permissions to directories and files they need access to.

#### Physical Server access

The servers are located in a locked server room. Only the IT department has access to this room. Additionally, the server room has a camera recording the access.

#### Remote Server access

For remote server access ssh keys must be used instead of passwords. In addition, these ssh keys should be password protected according to the above mentioned format specifications. If possible second factor authentication should be enabled for direct server access. This second factor authentication should be bound to the owner of the ssh key (i.e. SMS authentication, app authentication, ...)

Sometimes it becomes necessary for third party partners to access the servers (i.e. maintenance or support), in such a case second factor authentication is mandatory. The second factor authentication for third parties must be configured in such a way that only the head of IT can approve the access.

### Permissions

Permissions should always be defined as low as possible and only get expanded if required. The IT department can decide to reject a permission change if they consider the request inappropriate.

The general permission structure is defined in the Permission List.

User and group permissions must be reviewed annually by the head of IT ensuring that they are appropriately defined. This process also includes the verification of inactive users or users which should no longer be active in the system (i.e. former employees).

It is strongly recommended to use the basic organization schematic and job description for every area as a basis to define user permissions. Based on the job descriptions and user tasks, groups should be generated with the appropriate permissions. The permission management through groups is preferred since it's much more verbose and shows a clear structure. While permissions on user basis are in some cases more convenient for quick permission handling they indicate that the actual job function compared to the organization layout is not coherent with the actual tasks that person is performing. Permission handling on user level is strongly advised against and re-structuring groups and creating new groups is much cleaner even if in some cases a group only has one account assigned. Permissions for accounts should also get re-evaluated on a regular basis in order to prevent non-active accounts or accounts whose job description changed to have permissions they no longer need.

### Updates

Updates are very important not only to implement the newest features but also to close potential security vulnerabilities. This doesn't only apply for the operating system but also all the other software you may be running. Updates should be tested in a testing environment and then migrated to the live environment.

### HTTPS

The server must use HTTPS for its internal and external communication.

### Security software

Security software which must be used on the main server are:

* Iptables
* Monitoring software (not defined)
* fail2ban
* Firewall (not defined)
* Intrusion detection system (not defined)

### Server logs

All bash commands from users on the server must be logged and backed up during the backup process.

```bash
# .bash_profile
export PROMPT_COMMAND='if [ "$(id -u)" -ne 0 ]; then echo "$(date "+%Y-%m-%d.%H:%M:%S") $(pwd) $(history 1)" >> /var/www/html/backup/bash/$(date "+%Y-%m-%d").log; fi'
```

## Responsible

The responsibility for the IT security lies with the head of IT. Other IT employees may only take over these tasks if the head of IT considers these employees sufficiently trained in this area.

2022-01-01 - Version 1.0
