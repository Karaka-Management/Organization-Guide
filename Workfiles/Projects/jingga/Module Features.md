# Module Features

This document contains a short overview of planned features and functions for the different modules.

[TOC]

## General Modules

### Organization

The organization module provides basic structures such as units, departments and positions which are helpful to manage organizations and companies. These structures can be used by other modules for additional more detailed structures and functionalities.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Units                   | Create units and sub-unites to manage large organizations (e.g. company with multiple subsidiaries) |
| Departments (Teams)     | Allow more detailed structuring of units                     |
| Positions               | Assign functions and positions to users (job positions/titles) |

#### Ideas (won't exist for a long time)

| Functionality / Feature | Description                                             |
| ----------------------- | ------------------------------------------------------- |
| Organizational chart    | Automatically generate a versioned organizational chart |

### Tag

The tag module provides global and user defined tags which help to categorize content throughout the entire application. Tags make it possible to group information from many different modules under one key word/key phrase (e.g. news article, tasks, media files, contracts, promotions, etc. referencing the same event).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Global tag              | Tags which can be used by all users and modules              |
| User defined tag        | Users may define their own tags to categorize their private data |
| Search                  | Content can be searched by tag name throughout all modules   |
| Structure               | Tags can have a custom color, an icon and localizations for different languages |

### Media

The media module is a important core module since it manages all media files (e.g. images, text files, videos, ...). All modules who deal with files use this module to manage media files. 

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Upload                  | Upload media files by Drag&Drop and file selector            |
| Download                | Download files and directories (including virtual directories) |
| Media storage           | Show media files in lists similar to an explorer view on an operating system |
| File preview            | Show media content for many file types online (e.g. PDF, images, ...) |
| Drag and Drop           | Drag & Drop file movement similar to local file management   |
| Virtual files           | Similar to links to files in other directories to reduce storage needs and to allow referencing the same file |
| Password protection     | Protect files with a user defined password                   |
| Encryption              | Encrypt files for additional protection (e.g. useful for personnel contracts) |
| User files              | Every user has his own directory in which their files can be stored |
| Module files            | Modules can have their own directory to store module specific files |
| Local files             | Files on the server can get included by referencing the file path or directory path |
| Remote files            | Files available on the web can be included and shown similar to local/uploaded files |
| Permissions             | Files and directories can have permission settings limiting the interaction from different users/groups |
| Tags                    | Media files can have tags                                    |

#### Ideas (won't exist for a long time)

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Pausable uploads        | Uploads can be paused and continued later (e.g. for large files or bad Internet connection) |
| Online drives           | Online drives (e.g. dropbox, google drives, AWS) can be included and shown |

### Workflows

The workflow module lets an organization define processes which help to standardize work practices, reduce mistakes and help to monitor the progress of these processes. Such workflows can be for example sales approval, quality control, product introduction, ...

| Functionality / Feature  | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| Module workflows         | Module interactions can trigger functions of other modules based on specific criteria |
| Custom workflow template | Templates to visualize a process (e.g. progress status and input fields to directly input data required for the workflow) |

## General Business Modules

### Kanban

The kanban module implements a kanban board.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Structure               | A kanban board can have multiple columns, each column can have cards and each card can have comments |
| Board design            | Boards can have custom backgrounds (colors or images)        |
| Card design             | Cards can have different colors                              |
| Card types              | Cards can be text (incl. images), tasks, events, calendars, progress status |
| Media files             | Cards and comments can have references to media files        |
| Tags                    | Boards can have tags                                         |

### Contract Management

The contract management module handles contracts.

| Functionality / Feature |                                                              |
| ----------------------- | ------------------------------------------------------------ |
| Responsibilities        | Define users or user groups who are responsible for certain contracts |
| Reminder                | Send reminders for terminating contracts                     |
| Multiple documents      | Assign multiple documents and contract versions to a contract |
| Preview                 | Preview PDF scans                                            |
| Categories              | Assign contracts to different categories                     |
| Contract data           | Store and analyze contract data (e.g. costs, earnings, risk protection, ...) |
| Units                   | Contracts can be assigned to different units                 |
| Accounts                | Contracts can be assigned to different accounts (e.g. customer/supplier) |

### Q&A

The question and answer (Q&A) module lets users create questions which other users can answer.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Voting                  | Users can vote on questions and answers                      |
| Media files             | Questions and answers can have media files                   |
| Comments                | Questions and answers can have comments                      |
| Applications            | There can be different Q&A applications to separate communities (e.g. employees, customers, specific topics, ...) |
| Tags                    | Questions can have tags                                      |

### Knowledgebase

The knowledgebase module is a place where articles can be published to document process, explain organization structures, explain products, etc. This module is similar to a wiki (e.g. wikipedia).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Categories              | Knowledgebase articles can get categorized                   |
| Media files             | Articles can have media files                                |
| Versioned               | Articles can have versions                                   |
| Applications            | There can be different knowledgebase applications to separate communities (e.g. employees, customers, ...) |
| Tags                    | Articles can have tags                                       |

### Helper

The helper module lets authorized users upload self-coded scripts which make use of the application functions, application database, external api or whatever you can imagine.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Templates               | Helpers always have a base template which provides the core functionality and core resources |
| Instances               | Instances of a helper make use of the base template in combination with new input data and store this output |
| Standalone templates    | Templates can be standalone, which means they don't need a instance which makes use of them |
| Export templates        | Allow different export templates to export the helper output as PDF, word, print, csv or powerpoint |
| Tags                    | Scripts can have tags                                        |

Examples:

* Business reports (the base template defines how the business report looks like but the instance allows you to upload new data e.g. csv files which then is used to create a new business report)
* Design a newsletter template once with text input fields can be changed to create a new newsletter but always with the same design
* Create a training certificate template for customers for your products once with input fields for the customer name which then can get exported as PDF (or print)

> Since you can upload whatever script you want this function should only be given to authorized people (e.g. only administrators).
>
> In order to create such helpers one must be able to program in php. 

### Checklist

The checklist module lets users create checklists.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Templates               | Checklists templates can be defined in the application (task description, allowed input e.g. checkbox, text field etc.). |
| Instances               | Checklists instances can be manually created or automatically at a specific point in time (e.g. monthly) |
| Media files             | Checklists can have media files                              |
| Versioned               | Checklists are versioned                                     |
| Export                  | Checklists can be exported (pdf or printed)                  |
| Tasks                   | Checklists can create tasks (optional) which automatically check off checklists elements upon completion |
| Instance interaction    | Instead of interacting through tasks with the checklists user may also directly interact with the checklist (optional) |
| Tags                    | Checklists can have tags                                     |

### Tasks

The tasks module is for creating and solving tasks/todos. Tasks can be given from users to oneself or other users. Modules can also create tasks (e.g. checklist module, workflow module, ...). 

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Groups/Accounts         | Tasks can be created for groups and single accounts/users (users may also create tasks for themselves) |
| CC                      | Tasks can be sent to users by CC allowing them to see the task progression |
| Priority                | Tasks can have different priorities to sort them             |
| Due                     | Tasks can have a due date                                    |
| Forward                 | Tasks can be forwarded to other users/groups (e.g. if someone else should continue with the task) |
| Analysis                | Tasks can be analyzed (amount of tasks created, finished, time needed to solve them, ...) |
| Media files             | Tasks can have media files                                   |
| Tags                    | Tasks can have tags                                          |

## Userspace Modules

### Dashboard

The dashboard module provides a customizable front page for the user where information from many modules can be shown (e.g. new tasks, new messages, top news, ...).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Customizable            | Users may change which information are displayed and how they are shown |

### Profile

The profile module handles users who can login into the application and provides a profile page for every user where basic information about this user are shown, the user can change the account settings and some of their data is shown.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| User data               | Shows user data such as contact details, addresses data, job title, ... |
| Module data             | Modules can add custom information belonging to the user to a profile page (e.g. show media files uploaded by the user) |
| Account settings        | The user can change their account settings (e.g. localization, address, ...) |

#### Ideas (won't exist for a long time)

| Functionality / Feature  | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| User defined information | Let the user decide which information should and shouldn't get shown (e.g. hide address but show birthday) |

### News

The news module is for creating and displaying news articles (for organizational purposes such to employees e.g. company events or for public purposes e.g. news for customers).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Articles                | Users can create news articles incl. inline images, videos, media attachments and special elements (events, tasks, ...) |
| Publish date            | Articles can have a publish date on which the article should be shown |
| Media files             | News articles can have media files                           |
| Tags                    | News articles can have tags                                  |

#### Ideas (won't exist for a long time)

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Applications            | There can be different applications to separate communities (e.g. employees, customers, ...) |

### Editor

The editor module is for creating text documents for internal purposes (e.g. notes, transcripts, ...).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Markdown                | Documents are created from a extended markdown format        |
| Styling tools           | Text can be styled by typing markdown or by using the styling tools which perform these tasks in the background |
| Media files             | Documents can have media files                               |
| Tags                    | Documents can have tags                                      |

#### Ideas (won't exist for a long time)

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Wysiwyg                 | A wysiwyg editor like [Typora](https://typora.io/)           |
| Inline charts           | Allow inline charts (e.g. [Mermaid](https://github.com/mermaid-js/mermaid) and [Toast UI Chart](https://github.com/nhn/tui.chart)) |
| Inline math formulas    | Allow inline math formulas (e.g. [Katex](https://katex.org/)) |

### Calendar

The calendar module provides a calender for creating and managing events, appointments, meetings, daily tasks, ...

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Public/private          | Calendar entries can be public or private                    |
| User access permissions | Users can be given read and write permissions to a calendar  |
| Multiple layouts        | Calendars can have multiple layouts (annual, monthly, weekly and daily) |
| Calendar comparison     | Multiple calendars can be shown and compared at the same time |
| Scheduling              | Events can be schedules across multiple calendars (find and fix conflicts) |
| Markdown                | Calendar entries use markdown for styling                    |
| Media files             | Calendar entries can have media files                        |
| Tags                    | Calendar entries can have tags                               |
| Import                  | Multiple calendar formats can be imported (outlook, google)  |

### Messages

The editor module is for creating text documents for internal purposes (e.g. notes, transcripts, ...).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Email                   | Messages can be emails                                       |
| Rooms                   | Message rooms can be created where users can join and see all messages (similar to a chat but persistent) |
| Database archiving      | Emails can be archived in the application database           |
| Media files             | Documents can have media files                               |
| Tags                    | Messages can have tags                                       |

## Sales, Purchasing & Warehousing Modules

### Client Management

The client management module is for handling client data for companies.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Profile                 | Client profile view showing customer data                    |
| Analysis                | Sales analysis (sales, profit, cross selling potential, purchasing behavior, ...) |
| Accounts                | Accounts can be assigned to clients which allows a client to manage its own data to an extend (e.g. download invoices) |
| References              | Create references to other clients/suppliers                 |
| Attributes              | Custom attributes which can be created and filled (optional or mandatory) |

### Supplier Management

The supplier management module is for handling supplier data for companies.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Profile                 | Supplier profile view showing supplier data                  |
| Analysis                | Purchase analysis (costs, profit with purchased goods, prize increases, purchasing behavior, ...) |
| Accounts                | Accounts can be assigned to suppliers which allows a supplier to manage its own data to an extend |
| References              | Create references to other clients/suppliers                 |
| Attributes              | Custom attributes which can be created and filled (optional or mandatory) |

### Item Management

The item management module is for handling item/article data for companies.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Profile                 | Item profile view showing item data                          |
| Analysis                | Item analysis (sales, costs, prize increases, purchasing behavior, ...) |
| Parent items            | Parent items allow to share files across child items without duplicating the files (e.g. data sheets) |
| Part list               | Items used by/for this article (e.g. for production)         |
| Machine list            | Machines assigned for production/processing                  |
| Process list            | Create process/production steps to be followed               |
| Lot/SN                  | Items may have a LOT/SN and version (e.g. for documents)     |
| Garbage                 | Information about the materials used for the product (e.g. for disposal regulations) |
| Attributes              | Custom attributes which can be created and filled (optional or mandatory) |

### Warehouse Management

The warehouse management module is for handling stocks for companies.

| Functionality / Feature  | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| Stocks                   | Create and manage different stocks (e.g. main stock, quarantine stock, customer stock, supplier stock, ...) |
| Stock locations          | Create and manage different stock locations (e.g. local storage, external storage) |
| Shelfs                   | Shelfs in a stock location                                   |
| 2D warehouse structure   | 2D image of the warehouse structure with the different shelfs |
| LOT/SN                   | Items can have lot numbers or serial numbers or none. A item can have a external and internal LOT/SN. |
| Track quantities         | Items can be tracked by stock amount or defined to have no stock amount (e.g. for services) |
| Quantity modification    | Quantities can be manually changed in addition to invoices/delivery notes. |
| Picking list generation  | Generate picking lists from invoices with optimal walking distances |
| Picking map              | Show walking map for more details (e.g. for new employees who need to see where the shelf is) |
| Label scanning           | Document picking by scanning items (automatically documents and checks the correct item + lot + quantity) |
| Incoming goods checklist | Check incoming goods by quantity, time, type and quality (e.g. packaging damaged, ...) + customizable checks that need to be done |
| Incoming documentation   | Document incoming goods with images + driver signature       |
| Scan incoming goods      | Use supplier label to scan goods                             |
| Show free shelf          | Show free shelfs where to put incoming goods (optionally show map where to find that shelf) |
| Incoming documents       | Scan all documents attached to the shipment (e.g. delivery note, ...) |

### Stocktaking Module

The stocktaking module is for performing the stocktaking process.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Counting lists          | Print or create digital counting lists based on stock/shelf locations. The digital counting lists allows to input the items and quantities directly in the application (e.g. use a cellphone). You may define further limitations of which items should be part of the stocktaking process (e.g. only articles in a specific product segment, only articles with LOT numbers, ...) |
| Label scanning          | Optionally scan labels during the counting process instead of manually selecting the item and LOT/SN |
| Analysis                | Show significant deviations to the expected result based on custom limits (e.g. quantities, value, product type, ...). Create end of stocktaking analysis of deviations. Show stock movement between stocktaking and a defined date. |
| Re-counting             | Generate re-counting lists (e.g. in case of significant differences) |
| Random stocktaking      | Random item counting lists can be generated with defined parameters (e.g. quantity) for perpetual stocktaking or random tests |
| Overwrite               | Overwrite old stock with stock from stocktaking              |

### Labeling

The labeling module is for creating labels for items, assets, etc.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Label design            | Design labels in a drag and drop user interface              |
| Reference fields        | Reference existing fields from items or assets to automatically print on the label (e.g. lot number, shelf life time, asset number, ...) |
| Custom fields           | Create custom fields to be filled during the label printing process |

### Billing

The billing module allows users to create ingoing and outgoing bills (e.g. invoices, delivery notes, ...).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Write bills             | Write bills for customers, internal bills for supplier invoices, stock movements, internal uses (e.g. to other departments for profit centers) |
| Bill types              | Create multiple bill types which can have different layouts (e.g. outgoing invoice, delivery note, ...) |
| Media                   | Bills can have additional media files attached (e.g. signed contract, phone note, ...) |

### Purchasing

The purchasing module is for grouping together and providing purchasing activities.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Order suggestion        | Create order suggestion based on historic usage and pre-defined parameters (stock value, seasonal usage, minimum quantities, ...) |
| Item analysis           | Purchase price development, out of stock, delivery delay, delivery reliability, order behaviour, total purchase development |
| Supplier analysis       | Purchase price development, out of stock, delivery delay, delivery reliability, order behaviour, total turnover development |

### Sales

The sales module is for grouping together and providing purchasing activities.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Item analysis           | Total, regional, client, sales rep: Sales price development, margin development , sales development, customer count, customer distribution, new customers, lost customers, top customers, potential customers |
| Client analysis         | Total, item/segment: Sales price development, margin development , sales development, item count, item distribution, new items, lost items, top items, potential items |

### Support / Ticket Management

The support module is for handling support/ticket requests either for internal (e.g. tickets for IT team) or external purposes (e.g. customer support/tickets).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Custom fields           | Custom fields for data entry                                 |
| Custom account info     | Custom account fields (e.g. customer has maintenance contract) |
| Analysis                | Person, category: Ticket development, response time, success rate, rating development, time until solved, ticket time |
| Tasks                   | The module uses internally the tasks module and therefore provides most of the tasks functionality |

## Marketing Modules

### Promotion Management

The promotion module is for defining and controlling marketing promotions.

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Promotion information   | Basic promotion information (e.g. promotion code(s), responsible person, promotion description, responsible person, start/end, ...) |
| Participants            | Accounts who participated in the promotion                   |
| Milestones/progress     | Define milestones (e.g. manual value, based on time, based on tasks, based on earnings) |
| Budget                  | Define a budget for costs and earnings                       |
| Calendar                | Promotions can have a calendar assigned                      |
| Tasks                   | Promotions can have tasks assigend                           |
| Kanban                  | Promotions can have a kanban board assigned                  |
| Media                   | Promotions can have additional media files attached (e.g. signed contract, phone note, ...) |
| Accounting              | Promotions can show costs and earnings through cost objects  |

### Event Management

The event module is for defining and controlling events (e.g. sales events, marketing events, seminars, ...).

| Functionality / Feature | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Promotion information   | Basic event information (e.g. promotion code(s), responsible person, promotion description, responsible person, start/end, ...) |
| Participants            | Accounts who participated in the promotion                   |
| Milestones/progress     | Define milestones (e.g. manual value, based on time, based on tasks, based on earnings) |
| Budget                  | Define a budget for costs and earnings                       |
| Calendar                | Events can have a calendar assigned                          |
| Tasks                   | Events can have tasks assigend                               |
| Kanban                  | Events can have a kanban board assigned                      |
| Media                   | Events can have additional media files attached (e.g. signed contract, phone note, ...) |
| Accounting              | Events can show costs and earnings through cost objects      |

## QM, R&D and QS Modules

## Finance Modules

## Administration Modules

### Admin

AAAAAAAAAAAAAAAAAAA

| Functionality / Feature | Description |
| ----------------------- | ----------- |
|                         |             |
|                         |             |
|                         |             |

### Jobs

AAAAAAAAAAAAAAAAAAA

| Functionality / Feature | Description |
| ----------------------- | ----------- |
|                         |             |
|                         |             |
|                         |             |

### Exchange

AAAAAAAAAAAAAAAAAAA

| Functionality / Feature | Description |
| ----------------------- | ----------- |
|                         |             |
|                         |             |
|                         |             |

### Monitoring

AAAAAAAAAAAAAAAAAAA

| Functionality / Feature | Description |
| ----------------------- | ----------- |
|                         |             |
|                         |             |
|                         |             |

### Auditor

AAAAAAAAAAAAAAAAAAA

| Functionality / Feature | Description |
| ----------------------- | ----------- |
|                         |             |
|                         |             |
|                         |             |