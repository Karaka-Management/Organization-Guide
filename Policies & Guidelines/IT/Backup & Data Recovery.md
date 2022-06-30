# Backup & Data Recovery

The loss of data can have detrimental effects on the activities of the organization. Additionally, there are mandatory rules and regulations regarding data storage, which must be upheld. There are many possible reasons for data loss. Some could be:

* Faulty data storage device
* Accedential deletion or modification of files/data
* Malicious deletion or modification of files/data
* Force majeure
* Malware

## Goal

A complete mitigation of the risks is almost impossible. However, measures must be implemented which mitigate the risks as low as reasonably possible. Data backup should allow the organization to resume its activities as quickly as possible (ideally within 1-2 hours) without substential loss of data. 

## Implementation

The organization performs 3 types of backups:

* Backup to external data storage (NAS RAID 5 System): Daily
* Backup to an external service provider: Daily
* Manual backup (cloning): Quarterly

In addition to the above mentioned backup methods the server file system also uses RAID 5 providing additional redundancy in case of data storage failure. With raid 5 it's possible for 1 drive to fail without interupting the file storage.

Another data redundancy is implemented for the most valuable aspect of the organization, the source code. All source code is additionally stored at github.com which can be accessed globally and organization members may continue to work on the source code by pulling the latest version of the source code from this service provider.

### External data storage

A backup of the entire data is done to external data carriers (NAS RAID 5 System) in the server room. The backup software used is Borg. The software allows among other to encrypt the backup data and upload it to a remote server. The backup runs fully automated and time-controlled through cron jobs. This type of backup is conducted outside of the hours with the highest activity (2:00 am). The data recovery is possible at any time.

This type of backup is done incrementally, meaning only changes are stored.

### External service provider

In addition to the local backup a remote backup protects against local disasters such as a fire which could also destroy the local backup systems. The backup software used is Borg. The backup runs fully automated and time-controlled through cron jobs. This type of backup is conducted outside of the hours with the highest activity (2:00 am). The data recovery is possible at any time with some added delay due to download latency from the remote server.

This type of backup is done incrementally, meaning only changes are stored.

### Manual backup

Once a quarter a full data backup (clone) is created and stored on an external hard drive. The purpose of these backups are to provide long term backups which are not replaced/overwritten. Additionally, these backups provide some fall back solution for sleeper malware or malware which encrypts backup files. Only 4 quarters at a maximum are allowed to be stored on the same hard drive. The backup is stored in a separate building than the main backup or in a bank vault. 

## Responsibility

The responsibility for the data backup lies with the head of IT. Other IT employees may only take over these tasks if the head of IT consideres these employees sufficiently trained in this area. The responsible employees must control the data integrity of the backups once a quarter.

## Data storage

The data should be stored in such a way that only authorized personnel has access to the backup files. Authorized in this case means IT department and management. The data backups should be marked or labelled so that it is easily possible to identify the contents of the backup (i.e. Backup 2022-01.01 2:00:01).

## Reconstruction

The data reconstruction is documented in a reconstruction tutorial in the IT processes. During the reconstruction it may be necessary to put a higher priority on files and data which are more important for the ongoing organization activities (e.g. customer data, source code data). 
