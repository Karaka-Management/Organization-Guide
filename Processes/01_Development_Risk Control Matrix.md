# Development Risk Control Matrix

| No.  | R                 | Category                       | Risk Event                                                   | L    | C    | F                 | Cause                         | Mitigation Type              | Mitigation Strategy                                          | L*   | C*   | Changes | Comments                                                     | ES   | EY   | Evidences |
| ---- | ----------------- | ------------------------------ | ------------------------------------------------------------ | ---- | ---- | ----------------- | ----------------------------- | ---------------------------- | ------------------------------------------------------------ | ---- | ---- | ------- | ------------------------------------------------------------ | ---- | ---- | --------- |
| 1    | CTO               | Operational Risk (Development) | Unauthorized source code and development asset access.       | 1    | 1    | Many times a day  | Unmanaged access permissions. | Preventing (System & Manual) | Only authorized people gain access to confidential source code and development assets. | 1    | 1    |         | Not all source code and development assets are considered confidential and may be publicly accessible. The confidential aspects are determined by the CTO. | yes  | yes  |           |
| 2    | CTO               | Operational Risk (Development) | Undefined terms of intellectual property for code contributions. | 1    | 3    | Many times a day  |                               | Preventing (Manual)          | The terms of intellectual property for all contributions are well defined. | 1    | 1    |         |                                                              | yes  | yes  |           |
| 3    | Developer         | Operational Risk (Development) | Inconsistent code styles (which increases frictions between developers) | 5    | 1    | Many times a day  |                               | Preventing (Manual)          | Code style definitions are publicly available.               | 2    | 1    |         |                                                              | yes  | yes  |           |
| 4    | CTO/Code reviewer | Operational Risk (Development) | Inconsistent code styles (which increases frictions between developers) | 5    | 1    | Many times a day  |                               | Preventing (System & Manual) | Code styles are automatically tested with code style checkers. Optionally on the developer side but mandatory  and automatic during the code merging. | 2    | 1    |         |                                                              | yes  | yes  |           |
| 5    | CTO/Code reviewer | Operational Risk (Development) | Inconsistent code styles (which increases frictions between developers) | 5    | 1    | Many times a day  |                               | Preventing (Manual)          | Code styles are checked which allows  handling exceptions and special cases. | 2    | 1    |         | Not all code style options can be reasonably checked and defined. In some cases it's also possible to have false positive code style violations for edge cases. Manual checks during the code review by the responsible person may lead to additional code style changes or ignoring some code style "violations" if deemed reasonable. | yes  | yes  |           |
| 6    | Developer         | Operational Risk (Development) | Faulty code due to code changes, additions, removal.         | 5    | 1    | Many times a day  |                               | Preventing (Manual)          | Code testing definitions are publicly available. Minimum line coverage forces developers to write at least a certain amount of tests to check their code. | 2    | 1    |         |                                                              | yes  | yes  |           |
| 7    | CTO/Code reviewer | Operational Risk (Development) | Faulty code due to code changes, additions, removal.         | 5    | 3    | Many times a day  |                               | Preventing (System & Manual) | Code tests are automatically run with testing tools. Optionally on the developer side but mandatory  and automatic during the code merging. This includes static tests which require no self-written tests and developer written tests. | 2    | 1    |         |                                                              | yes  | yes  |           |
| 8    | CTO/Code reviewer | Operational Risk (Development) | Faulty code due to code changes, additions, removal.         | 5    | 3    | Many times a day  |                               | Preventing (Manual)          | Code tests are manually checked and performed which allows handling exceptions and special cases. | 2    | 1    |         |                                                              | yes  | yes  |           |
| 9    | CTO/Code reviewer | Operational Risk (Development) | Faulty code due to code changes, additions, removal.         | 5    | 4    | Many times  a day |                               | Preventing (Manual)          | A demo application allows code reviewer to test code changes from a end-user point of view in conjunction with the whole application, other modules and dummy data. | 2    | 1    |         |                                                              | yes  | yes  |           |
| 10   | CTO/Code reviewer | Operational Risk (Development) | Unauthorized code gets accepted.                             | 5    | 5    | Many times  a day |                               | Preventing (System & Manual) | Manual and automatic code checks/tests and manual review by authorized and qualified developers ensures high quality and that only code authorized by these developers gets accepted. Developers who can accept code changes are carefully selected and their permissions are handled in the version control software. | 1    | 5    |         |                                                              | yes  | yes  |           |

## Abbreviations

* R: Responsible

* L: Likelihood (1-5)

* C: Consequence (1-5)

* L\*/C\*: Likelihood and Consequence after mitigation

* F: Frequency (many times a day, daily, weekly, monthly, annually)

* ES: Effective

* EY: Efficient

2022-01-01 - Version 1.0
