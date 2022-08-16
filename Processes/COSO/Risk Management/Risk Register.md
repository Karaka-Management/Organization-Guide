# Risk Register

The risk register is a central repository to describe and track risks as well as record actions. It includes information for each risk such as risk category, likelihood, consequence, mitigation measures, risk owner and documentation of changes. Additional risks can be found in the corresponding **Risk Control Matrix** of every process.

| No. | R    | Category         | Risk Event                                                   | L    | C    | O    | Cause                      | Mitigation Type                           | Mitigation Strategy                                          | L*   | C*   | Changes | Comments                                                     | ES   | EY   | Evidences |
| -------- | ---- | ---------------- | ------------------------------------------------------------ | ---- | ---- | ---- | ------------------------------------------------------------ | ---- | ---- | ------- | ------------------------------------------------------------ | ---- | ---- | ---- | ---- | ---- |
| 1        | DE   | Operational Risk | Loss of source code                                          | 1    | 5    |      |  |  | Avoiding: Store source code in cloud (github). At least one local developer PC and project server. |      |      |         |                                                              | yes  | yes  |   |
| 2        | DE   | Operational Risk | Source code leak                                             | 5    | 1    |      |  |  | Controlling: The programming language is compiled at runtime. The value of the software lies in the updates, support and licenses. |      |      |         | Many companies transferred the revenue model to subscriptions (e.g. Adobe, Microsoft) in order to avoid similar problems. | yes  | yes  |   |
| 3        | DE   | Operational Risk | User acquires additional permissions without authorization (every software which uses permissions) | 2    | 5    |      |  |  | Avoiding: Permissions can only be granted by users which have received the permissions to do so. Users which can change permissions may also only have the permission to change specific users/permissions (single application elements, not the whole application.). We provide a documentation on who to manage permissions incl. best practices. Customers with a maintenance contract also receive additional advice based on their account permission handling. We also check regularly if features can be used by default without the necessary permissions. |      |      |         | The consequences or severities depend on the permissions which can be acquired. | yes  | yes  |   |
| 4        | DE   | Operational Risk | User code execution (every software which allows data upload/input) | 3    | 5    |      |  |  | Avoiding: User provided code is a critical part of some modules (e.g. Helper, Job). These modules provided by OMS execute code user code in iframes. We provide guidelines regarding this sensitive topic which explains that only developers in a company should have access to such functionalities. |      |      |         |                                                              | yes  | yes  |   |
| 5        | DE   | Operational Risk | Data leak (e.g. database data, file uploads) (every software which stores data) | 2    | 5    |      |  |  | Avoiding: We regularly check if users have access to data without the necessary permissions. Our modules may use encryption for extremely sensitive data. Media files are only accessible through the media module which allows to check the necessary reading permissions. We also provide a general policy for customers who to secure and maintain their servers. |      |      |         | This is a big problem for almost every company working with data. The biggest known leaks happened among others to Adobe, ebay, Equifax, LinkedIn, Yahoo, ... | yes  | yes  |   |
| 6        | DE   | Operational Risk | Corrupt/malicious data injection (every software which accepts data input) | 3    | 3    |      |  |  | Avoiding: Data is validated client side (minimal protection) and server side. Generally, user input is only accepted if it matches the specified allowed format. Data is usually not sanitized to avoid mistakes during the sanitizing process. Database query statements are prepared and encoded. |      |      |         |                                                              | yes  | yes  |   |

## Abbreviations

* R: Responsible
* L: Likelihood (1-5)
* C: Consequence (1-5)
* L\*/C\*: Likelihood and Consequence after mitigation
* O: Occurrence (many times a day, daily, weekly, monthly, annually)
* ES: Effective
* EY: Efficient

## Responsible

* DE: Dennis Eichhorn



2022-01-01

