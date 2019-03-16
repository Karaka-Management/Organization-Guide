# Executive Summary

# Organization

The Orange Management organization is located Germany and founded in November 2015 by Dennis Eichhorn for developing the Orange Management application and sub-components which incorporates functions such as CRM, SRM, CMS, Shop and many more.

The main goal of the organization is to create solutions for companies and organizations of all sizes which allow them to seamless manage their operations from one application and interconnect them.

## SWOT

### Strengths

#### Customer

* Everything in one application. Organizations and businesses no longer have to use multiple services from different providers and potentially integrate them into their existing applications
* Cheap for the customer compared to many other solutions
* Easy to use with modern visuals and layouts.
* Good performance
* Modular. The customer can decide which modules he needs
* Solves real problems. Features are drafted and tested by business specialists in the respective fields.
* Optimized for mobile and desktop
* Flexible setup (local or remote)
* Regular updates. Either manually or automatically
* Large amount of modules

#### Technical

* Modular structure is designed in a very scalable way
* Multiple database support (mssql, mysql, postgresql)
* Multiple cache support (file, memcache, redis)

### Weaknesses

#### Customer

* Installation for non-tech people is "difficult" (not the actual app installation but the WAMP or LAMP installation)

#### Technical

* Request based code execution. Database and cache connection is request based and not persistent etc.
* Concurrency is difficult to solve due to the request based code execution

### Opportunities

* Continuous digitalization and need to keep up with it
* Price attractiveness for all sizes of organizations and businesses
* Public free software tests (without registration)
* Growing demand for managing data (also for small businesses)

#### Technical

* Programming language performance improvement through JIT implementation
* Programming language performance improvement through usage of typehints during compilation

### Threats

#### External

* Regulations. There are many different regulations for different regions and business fields that must be upheld
* Small customers still want to own software and not rent it and pay for it every year.

#### Internal

* Own organization size/workload. A large amount of modules and tools are required to reach the critical size to make a product which is beneficial for a large amount of organizations and businesses

## Strategy & Vision

### Vision

Orange Management tools are used by at least 1.000 organizations in 2023

#### Goal

1. Focus on the solution of the problem
2. Financially attractiveness for as many end-users as possible
3. Solve a wide range of problems
4. Integrate solutions for seamless workflows
5. Accessible for everyone (desktop, tablet, phone, for disabled people, online/offline)
6. Fast user interface feedback and good performance

#### How To Achieve?

1. Use it during development incl. user feedback
2. Modular system and fair pricing
3. Speak to users and implement common workflows
4. One philosophy and one core system for every module
5. Put the user experience above ease of implementation
6. Custom and specialized software implementations instead of generalized solutions.

### Strategy

#### Initial Phase

##### Customer

In the beginning the goal is to reach a large amount of organizations no matter the size. As it is easier to address smaller organizations since they usually are less invested in existing software solutions they will be the initial target group. For them no customization will be done unless they can be integrated for everyone.

For these customers the following points are most important:

1. Price
2. Ease of use
3. Key modules

###### Price

The price should be very competitive. This could be achieved by providing a cheap basic package which includes the essentials for most organizations with a licence for up to **5** users. There could be different packages for different types of organizations. However a small organization should look at a package and immediately recognize that this basically contains everything they need. Small organizations need to have trust in a product without having to understand all the technical details of functionality which may be required for larger organizations.

At the same time the customer needs to be informed, that he can customize his package if he wants to (e.g. add additional modules). Only after providing these information the customer needs to be informed that he can also completely customize his modules if he so desires without a basic package. For mid- to large sized organizations other price strategies could be better.

A basic package should not cost more than 10 EUR per month as this is comparable to other competitors. Competitors offer overall much less but compared to the basic package they are similar features.

###### Ease of use

Ease of use needs to be visible to the customer even before he purchases a package. In order portray that of course the modules themselves have to be designed in a very intuitive way but also the available documentation has to be very easy to understand. Very often documentations expect a certain amount of pre-knowledge which confuses new users if they try to follow a documentation step-by-step. At the same time videos are very important for small organizations as they may rather watch a video than read through the documentation.

The videos should not have a long introduction and an outro which are very annoying if you want to go through some videos very fast and have to waste your time on intros and outros. The solution will be to only show a 3 sec image or splash screen as intro and an 3 sec outro image with contact, website and documentation details.

The videos should be around 5 - 15 minutes long. Shorter than 5 minutes will lead to a large amount of videos which take time to search through and longer than 15 minutes will discourage users since they might not want to invest the time.

###### Key modules

The key modules in one package must give the user the impression that this includes all the basics he needs to manage the organization.

Recommended modules for businesses are:

* Admin
* Organization
* Media
* Tasks
* Media
* Calendar
* Accounting
* P&L
* ClientManagement
* SupplierManagement
* Invoicing
* Payment reminder
* CashManagement
* Banking (FinTS/HBCI, EBICS)
* ItemManagement
* VoucherManagement
* TaxManagement

With these modules almost every small business could operate. Smart advertisements could help to sell extending modules such as charting, balancing, cost center accounting, cost object accounting, warehousing etc.

# Products & Services

## Products

1. CRM
2. SRM
3. ERP
4. Intranet
5. Shop
6. CMS

# Business Decissions

## Programming Language

In the following a ranking of numbers (1-10) will be used where 10 is the highest and 1 the lowest value. Many of these evaluations are pure subjective and based on the personal experiences made by the organization founder in 2018.

| Description                             | PHP        | C/C++     | C#         | GO        | Java       | Rust      | NodeJS     | Python     |
| --------------------------------------- | ---------- | --------- | ---------- | --------- | ---------- | --------- | ---------- | ---------- |
| Language experience                     | 10         | 4         | 6          | 1         | 3          | 2         | 2          | 1          |
| Performance (runtime)                   | 5          | 10        | 9          | 9         | 9          | 10        | 7          | 3          |
| Web integration (tools, api, libs)      | 10         | 4         | 10         | 9         | 9          | 4         | 10         | 9          |
| Package management system               | 10         | 4         | 7          | ?         | 4          | 7         | 5          | ?          |
| Webserver, Vserver, Rootserver support  | 10         | 7         | 7          | 7         | 7          | 7         | 7          | 8          |
| Concurrency                             | "no"       | yes       | yes        | yes       | yes        | yes       | yes        | "no"       |
| Community size for web applications     | 10         | 3         | 7          | 6         | 6          | 2         | 8          | 8          |
| Community momentum                      | decreasing | stable    | increasing | stable    | decreasing | stable    | increasing | decreasing |
| Code execution                          | request    | running   | running    | running   | running    | running   | running    | request    |
| Code quality tools                      | 10         | ?         | ?          | ?         | ?          | ?         | ?          | ?          |
| Availability of libs (e.g. pdf, excel)  | 10         | ?         | ?          | ?         | ?          | ?         | ?          | ?          |
| Easy to install on own server/pc        | no         | yes       | yes        | yes       | yes        | yes       | no         | no         |
| Availability on third party hosts       | 10         | 7         | 7          | 7         | 7          | 7         | 8          | 9          |

The decision why Orange Management decided to use PHP came down to the following points:

1. Since the web applications are supposed to run on all sizes of organizations and businesses PHP has the advantage with availability on simple (cheap) webservers.
2. The request based code execution makes it less susceptible against errors (re-starting and monitoring the application etc.) and therefore better for non-tech people.

# Action Plan

1. First real world tests on testing company (admin, organization, task & helper module)
2. Create reports for the helper module for the testing company
3. Test importer module and import testing company data into application
4. Let modules display imported data (read-only) (customers, suppliers, accounts, cost centers, cost objects, articles, invoices)
5. Create reports based on exiting data
6. Implement modify and create functionality for the above mention imported modules (data)
7. Further implement basic modules (news, profile, wiki, kanban, Q&A, calendar, messaging)
8. Create new design
