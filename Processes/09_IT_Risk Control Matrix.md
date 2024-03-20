# IT Risk Control Matrix

| No.  | R                    | Category              | Risk Event                                                   | L    | C    | F      | Cause | Mitigation Type     | Mitigation Strategy                                          | L*   | C*   | Changes | Comments | ES   | EY   | Evidences |
| ---- | -------------------- | --------------------- | ------------------------------------------------------------ | ---- | ---- | ------ | ----- | ------------------- | ------------------------------------------------------------ | ---- | ---- | ------- | -------- | ---- | ---- | --------- |
| 1    | CTO                  | Operational Risk (IT) | Data loss                                                    | 3    | 5    | Daily  |       | Preventing (System) | Automatic daily local backups                                | 1    | 1    |         |          | YES  | YES  | [Cron](https://github.com/Karaka-Management/Build/blob/master/Backup/cron.sh) |
| 2    | CTO                  | Operational Risk (IT) | Data loss                                                    | 3    | 5    | Daily  |       | Preventing (System) | Automatic daily backups to external/remote service providers | 1    | 1    |         |          | YES  | YES  | [Cron](https://github.com/Karaka-Management/Build/blob/master/Backup/cron.sh) |
| 3    | CTO                  | Operational Risk (IT) | Data loss                                                    | 3    | 5    | Daily  |       | Preventing (Manual) | Quarterly manual backups for long-term storage               | 1    | 3    |         |          | YES  | YES  |           |
| 4    | CTO                  | Operational Risk (IT) | Corrupted backup data                                        | 2    | 3    | Daily  |       | Revealing (System)  | Automatic data integrity validation of daily backups         | 1    | 3    |         |          | YES  | YES  | [Cron](https://github.com/Karaka-Management/Build/blob/master/Backup/cron.sh) |
| 5    | HOD, head of IT, CTO | Operational Risk (IT) | Emplyees have access to files or functions outside of their competencies | 4    | 4    | Daily  |       | Preventing (Manual) | Employee permissions are defined in a general Permission List. Deviations must be approved | 1    | 4    |  |          | YES  | YES  | [Permission List](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/IT/Permission%20List.md) |
| 6    | head of IT, CTO      | Operational Risk (IT) | Software causes problems                                     | 3    | 3    | Weekly |       | Preventing (Manual) | New software and software updates must be tested in a sandbox environment | 1    | 1    |         |          | YES  | YES | [Third Party Software Validation - New](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/IT/Third%20Party%20Software%20Validation%20-%20New.md)<br />[Third Party Software Validation - Update](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/IT/Third%20Party%20Software%20Validation%20-%20Update.md) |
| 7    | HOD, head of IT, CTO | Operational Risk (IT) | Unauthorized software.                                       | 3    | 5    | Weekly |       | Preventing (Manual) | New software must be approved                                | 1    | 2    |         |          | YES  | YES  | [Third Party Software Validation - New](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/IT/Third%20Party%20Software%20Validation%20-%20New.md) |

## Abbreviations

* R: Responsible

* L: Likelihood (1-5)

* C: Consequence (1-5)

* L\*/C\*: Likelihood and Consequence after mitigation

* F: Frequency (many times a day, daily, weekly, monthly, annually)

* ES: Effective

* EY: Efficient

2022-01-01 - Version 1.0
