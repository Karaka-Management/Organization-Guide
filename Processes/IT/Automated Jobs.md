# Automated Jobs

| Type / Description                  | Interval | Start | Comment                        |
| ----------------------------------- | -------- | ----- | ------------------------------ |
| Backup to NAS                       | Daily    | 02:00 |                                |
| Test backup to NAS                  | Daily    | 02:25 | Depends on previous backup job |
| Backup to remote server             | Daily    | 02:30 | Depends on previous backup job |
| Test backup to remote server        | Daily    | 03:05 | Depends on previous backup job |
| Push master branch to remote server | Daily    | 03:00 |                                |
| Demo application setup              | Daily    | 03:00 |                                |

2022-01-01 - Version 1.0
