# Business Plan

## Organization

The Karaka organization is located in Germany and founded in November 2015 by Dennis Eichhorn for developing the Karaka application and sub-components which incorporates solutions such as CRM, SRM, CMS, ERP, Shop and many more.

The main goal of the organization is to create solutions for companies and organizations of all sizes which allow them to seamless manage their operations from one application.

### SWOT

See [SWOT](SWOT.md).

## Business model canvas

See [Business Model Canvas](Business%20Model%20Canvas.md)

## Products & Services

### Products

Key solutions (consisting of multiple modules) which must be available are:

* CRM
* SRM
* ERP
* Intranet
* Shop
* CMS
* BI
* Office

### Services

Key services that should be implemented are:

Early:
* Initial consulting
* Setup
* Support & maintenance

Mid:
* Hosting
* Pre-configured server
* Customization (for large customers)

Late:
* Migration of existing data

## Business Decisions

### Programming Language

In the following a ranking of numbers (1-10) will be used where 10 is the highest and 1 the lowest value. Many of these evaluations are pure subjective and based on the personal experiences made by the organization founder.

| Description                            | PHP       | C/C++   | C#         | GO      | Java       | Rust    | NodeJS     | Python     |
| -------------------------------------- | --------- | ------- | ---------- | ------- | ---------- | ------- | ---------- | ---------- |
| Language experience                    | 10        | 4       | 6          | 1       | 3          | 1       | 1          | 2          |
| Performance (runtime)                  | 5         | 10      | 9          | 9       | 9          | 10      | 7          | 3          |
| Web integration (tools, api, libs)     | 10        | 4       | 10         | 9       | 9          | 4       | 10         | 9          |
| Package management system              | 10        | 4       | 7          | ?       | 4          | 7       | 5          | ?          |
| Webserver, Vserver, Rootserver support | 10        | 7       | 7          | 7       | 7          | 7       | 7          | 8          |
| Concurrency                            | "no"      | yes     | yes        | yes     | yes        | yes     | yes        | "no"       |
| Community size for web applications    | 10        | 3       | 8          | 6       | 6          | 2       | 9          | 7          |
| Community momentum                     | stable    | stable  | increasing | stable  | decreasing | stable  | increasing | decreasing |
| Code execution                         | "request" | running | running    | running | running    | running | running    | "request"  |
| Code quality tools                     | 10        | ?       | ?          | ?       | ?          | ?       | ?          | ?          |
| Availability of libs (e.g. pdf, excel) | 10        | ?       | 10         | ?       | ?          | ?       | 10         | ?          |
| Easy to install on own server/pc       | no        | yes     | yes        | yes     | yes        | yes     | no         | no         |
| Availability on third party hosts      | 10        | 7       | 7          | 7       | 7          | 7       | 8          | 9          |

The decision why Karaka decided to use PHP came down to the following points:

1. Since the web applications are supposed to run on all sizes of organizations and businesses PHP has the advantage with availability on simple (cheap) webservers.
2. The request based code execution makes it less susceptible against errors (re-starting and monitoring the application etc.) and therefore better for non-tech people.
   1. Multi-threading can be still solved through other means

## Action Plan

1. First real world tests on testing company (admin, organization, task & helper module)
2. Create reports for the helper module for the testing company
3. Test importer module and import testing company data into application
4. Let modules display imported data (read-only) (customers, suppliers, accounts, cost centers, cost objects, articles, invoices)
5. Create reports based on exiting data
6. Implement modify and create functionality for the above mention imported modules (data)
7. Further implement basic modules (news, profile, wiki, kanban, Q&A, calendar, messaging)
8. Create new design

2022-01-01 - Version 1.0
