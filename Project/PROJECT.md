# Project Status and Tasks

- [Summary](#summary)
- [Milestones](#milestones)
- [Todos](#todos)
- [Features](#features)
- [Bugs](#bugs)
- [Drafts, concepts & ideas](#drafts-concepts-ideas)
- [Most recent changelog](#most-recent-changelog)

## Summary

Last update of this file: 2021.11.20

### Timeline

### Key changes this month

### Challenges & problems

### Next steps

Continue with milestone task implementation.

Continue with increasing the test coverage of the modules.

## Milestones

Based on the pilot candidate with whom the functionality will be implemented.

| Deadline | Done | Milestone                                              | Costs          | Value          |
| -------- | ---- | ------------------------------------------------------ | -------------- | -------------- |
|          |      | Replace ticket system from Z*                          | 7,200 EUR      | 8,000 EUR      |
|          |      | Replace document/contract management from CRM          | 3,000 EUR      | 6,000 EUR      |
|          |      | Implement invoice management process                   | 0 EUR          | 5,000 EUR      |
|          |      | Replace QM from CRM                                    | 700 EUR        | 1,500 EUR      |
|          |      | Replace workflows from CRM                             | 1,000 EUR      | 3,000 EUR      |
|          |      | Move sales reps from CRM                               | 3,000 EUR      | 6,000 EUR      |
|          |      | Replace Marketing events, seminars, shop data from CRM | 1,500 EUR      | 2,000 EUR      |
|          |      | Sales analysis (replace D* from G*)                    | 1,000 EUR      | 2,000 EUR      |
|          |      | Digitalizing human resource Human Resource Management  | 0 EUR          | 500 EUR        |
|          |      | Replace billing from G*                                | 15,000 EUR     | 20,000 EUR     |
|          |      | Replace stock from G*                                  | 7,500 EUR      | 8,000 EUR      |
|          |      | Replace inventory from G*                              | 500 EUR        | 1,000 EUR      |
|          |      | Replace manufacturing from G* + R&D + Quality control  | 500 EUR        | 10,000 EUR     |
|          |      | Replace accounting from G*                             | 10,000 EUR     | 12,000 EUR     |
|          |      | Replace asset management from G* EUR                   | 500 EUR        | 500 EUR        |
|          |      | Replace reporting from L*                              | 4,200 EUR      | 5,000 EUR      |
|          |      |                                                        | **55,600 EUR** | **90,500 EUR** |

*The annual value is the relative value for the pilot candidate based on the current cost structure.*

### Cost basis

The estimated annual costs in the milestones are based on the total annual costs from the software from the pilot candidate. These total costs are then subjectively distributed to the different software aspects.

| Type      | License        | Customization  | Total          |
| --------- | -------------- | -------------- | -------------- |
| Z*        | 7,200 EUR      |                | 7,200 EUR      |
| G*        | 26,600 EUR     | 8,400 EUR      | 35,000 EUR     |
| L*        | 4,200 EUR      |                | 4,200 EUR      |
| CRM       |                | 9,200 EUR      | 9,200 EUR      |
| **Total** | **38,000 EUR** | **17,600 EUR** | **55,600 EUR** |

*Website costs are not included, they can be estimated at another 30,000 EUR per year*

### Tasks & decisions

| Deadline   | Done | Task                                                         |
| ---------- | ---- | ------------------------------------------------------------ |
| 2022.08.27 |      | **Define scope**<br />Which modules should be developed first<br />Which features must be part of the modules at the start<br />What is the expected timeline for the different modules |
|            |      | **Navigation**<br />Allow to hide navigation elements even if the module is installed.<br />Also disable routing for front end. This way only the functionality is available (API). |
|            |      | **Customer Management**<br />Names<br />Address<br />Contact elements<br />Custom fields<br />Contract import from CRM system (maintenance contract)? *(SD specific)* |
|            |      | **Job**<br />Manage jobs<br />Consider to combine Job and Workflow (e.g. job only schedule + cmd, workflow is the script to execute) |
|            |      | **Exchange** (Importer/Exporter)<br />GSD import script for customers (new entries and changed entries) *(SD specific)*<br />GSD import script for customer addresses (new entries and changed entries) *(SD specific)*<br />Allow to define exchange scripts as auto-run with a interval |
|            |      | **Permission**<br />Better permission handling (only show tickets the user is allowed to see) **difficult**<br />When returning models (backend and API requests) the permission should be checked (all modules)<br />After completely figuring out permissions every API function needs to be checked if it behaves correctly depending on the different permissions (e.g. user created the model, user who is allowed to access the model but not change it, ...) |
|            |      | **Admin**<br />[UI] Add user & group settings<br />[UI] Add account/group removal from each other<br />[UI] Add permission removal from accounts/groups<br />[UI] Add permission modification for accounts/groups<br />Create API key/token permissions<br />Create API key/token handling<br />Handle logging for API keys/tokens<br />Handle "login" for API keys/tokens (maybe create dummy account for that?) |
|            |      | **Support** (Tickets)<br />Ticket creation<br />Ticket response<br />Status update via email<br />Feedback/rating via email click (using time limited hash) **difficult**<br />Response from customer via email (using time limited hash) . Requires ticket email address, maybe create one per app?**difficult**<br />Upload files to random support directory<br />Allow ticket creation from external sources (e.g. website) by using an api key. Allow custom fields as well. |
|            |      | **Media**<br />Drag and drop upload<br />Ctrl+C/Ctrl+V upload<br />Move files and directories to subdirectories<br />Bulk actions (move, delete, download, ..)<br />Better file and directory permissions. Similar problem applies to permissions. **difficuly due to subdirs**<br />Implement download of directory<br />Add password support for directories.<br />    > Difficult because of subdirectories<br />Allow to actually replace media files (same DB id but replaced the file on the hard drive)<br />Allow links as media files (e.g. use path). If a link is detected it should forward to that link, this would also allow other modules to create pseudo media elements e.g. helper/editor. Upon clicking on it e.g. the editor is opened. This would mean the editor needs to create this media model whenever the user creates a document. The path needs to be the same as in the moduel itself e.g. Accounts/... or whatever the user defined as path in the module itself. The url should be relative e.g. /editor?id={id} which makes it domain name independent.<br />Allow to create a collection when uploading multiple files |
|            |      | **Contract Management**<br />Show contracts after clicking on document list in contract<br />Create task/message if a contracts term runs out<br />Create job which informs people about contract end of life<br />Setting to change responsible person/group A to B (e.g. person leaves company)<br />Implement directory view for contracts |
|            |      | **System**<br />Create frontend event which checks for server messages regularly (e.g. server goes into maintenance/read-only mode) |
|            |      | **Workflow**<br />Individual UI templates incl. styles<br />Script management<br />Allow email message and response (text+time limited links via hash) |
|            |      | **Invoice Management**<br />OCR<br />Auto content recognition (supplier, articles, costs, taxes, payment terms)<br />Define approval workflow<br />Allow notes<br />Allow questions to other users (reference tasks and or media messages)<br />Allow to add additional documents<br />Allow PDF modifcation (allow notes on pdf, approval stamps) **difficult**<br />   > This requires a JS live preview for adding this at a specific position (maybe PDFJSAnnotate, maybe customize pdf.js)<br />Job/Schedule which checks unhandled invoices<br />Hooks/Workflows for invoices |
|            |      | **Quality Management**<br />Create quality issue (for account, article, other?)<br />Define workflow based on report type?<br />Statistics????<br />Export list to excel<br />Export based on filter to pdf<br />Expand GSD Exchange importer *a lot of work* *(SD specific)* |
|            |      | **Workflow** (implement some scripts)<br />Remove article (SD specific). How to handle data (custom database table?)<br />Create article (SD specific). How to handle data (custom database table?) |
|            |      | **Customer Management** (SD specific)<br />Expand GSD Exchange importer to also import customer files from CRM (files, emails)<br />Expand GSD Exchange importer to also import customer notes (notes, visitor reports) |
|            |      | **Sales**<br />Create easy way to create quick visitor reports (= maybe use notes for this with a type 'visit')<br />Allow to create visitor report on cell phone by using location matching (geolocation)<br />Analyze reports per sales rep (e.g. use filter for export?) |
|            |      | **Item Management**<br />Names<br />Base data<br />Media files<br />Expand GSD Exchange importer to also import articles *(SD specific)* |
|            |      | **Billing** (only data for upcoming modules)<br />Basic invoice data (no stock movement)<br />Expand GSD Exchange importer to bills as well *(SD specific)*<br />Bill expenses such as insurance, freight, etc. also need VAT percentages. Best would be to create cost types, this would allow to add multiple freight expenses and print them below the invoice<br />Show invoice pdf in preview on change |
|            |      | **Sales**<br />Sales rep ranking<br />Individual rep sales analysis (e.g. top customers, sales by product group, lost customers, ...) |
|            |      | **Customer Management**<br />Customer sales info/statistics (total sales, invoices, articles, groups)<br />Invoice pdf importer from hard drive (without using the Exchange module) *(SD specific)*<br />Create a view where you can see all bills of the customer<br />Create a view where you can see all items of the customer |
|            |      | **Sales**<br />Sales analysis reports                        |
|            |      | **Sales Analysis** (client sales analysis)<br />Sales + Gross profit<br />Quantity orders + quantity articles<br />Segment sales<br />Top articles<br />Cross selling (bought as well)<br />Amount of invoices<br />Amount of different articles |
|            |      | **Sales Analysis** (item sales analysis)<br />Sales + gross profit<br />quantity sales, quantity customers<br />Cross selling<br />Top customers<br />Amount of customers<br />Amount of article sales<br />Amount of new customers<br />Cross selling articles |
|            |      | **Job**<br />Create job which can automatically create checklists (e.g. end of month checklists) |
|            |      | **Checklist**<br />Create module<br />Checklists can create tasks<br />Allow to define recurring date time |
|            |      | **Marketing**<br />Create promotions (incl. basic info)<br />Promotion type (somehow use for cost center)<br />Create events (incl. basic info)<br />Event type (somehow use for cost center) |
|            |      | **Human Resource Management**<br />Handle staff information (encrypted)<br />Handle staff positions<br />Manage documents (encrypted)<br />Manage contracts (encrypted)<br />Manage salary (encrypted)<br />List of assets and documents handed over to employees (to be returned on leave) |
|            |      | **Item Management**<br />Add an area for markers (e.g. not sold for a x month, not purchased for x month, bad margin... etc.)  Similar to an alarm system (maybe green, yellow, red markers?)<br />Consider to use name for attribute identification (currently only used for localization). Is this really required?id might be fine?<br />Add an area for markers (e.g. not sold for a x month, not purchased for x month, bad margin... etc.) Similar to an alarm system (maybe green, yellow, red markers?)<br />Create a second optional list view where the item is shown at the bottom of the list which allows the user to the the item list at the top and the item itself below. Either create a custom view or somehow append an iframe below the list which is loaded based on the selected item |
|            |      | **Human Resource Clocking**<br />Basic clocking (browser + hardware)<br />Hardware needs to make web requests for the chip clocking<br />Clocking overview for employees<br />Vacation / absence management for employees<br />Clocking overview/analysis for managers/hr<br />Vacation / absence overview/analysis for managers/hr<br />Vacation approval workflow<br />Clocking change approval<br />Export of clocking times (hr)<br />Export of vacations, sickness, ... (hr) |
|            |      | **Dashboard**<br />Drag&Drop element sometimes disappear on drop<br />Create default dashboard templates which can be used by users, changing them copies it for this user<br />Allow people to modify a dashboard and automatically save it / reload it<br />Implement a way for other modules to provide dashboard components (allow modules to register themselves in a database table) |
|            |      | **Billing** (additional features)<br />Only create pdf preview if preview is visible?<br />[Analysis] Gross profit (total bill and elements)<br />Show bill relations (on tab which shows all related bills)<br />Create send as email button inside the bill. this opens the send email view where the email is pre-written with the attached pdf<br />In the supplier and client view you should be able to select multiple bills and click print for printing<br />In the supplier and client view you should be able to select multiple bills and click send as email for email sending<br />The send bill as email should have a global settings where you can either define a global email or empty = user specific email<br />Sending emails should have a default email format and a default invoice naming convention, additionally there should be the option to define a user specific email text and pdf naming convention<br />Clients should have a invoice_email address which is stored in the client |
|            |      | **Billing** (full implementation)<br />Allow to define re/usable templates (e.g. recurring invoices)<br />Allow to define re/usable texts<br />Automatic email invoice after finishing if user wants to use that<br />Batch print/export invoices based on filter<br />Bill element sorting should have a small bar at the beginning of every element which allows the user to drag/drop the element up or down. Of course the up/down arrows which are currently implemented should remain.<br />Forward bills to sales rep (if bill > X EUR or specific type)<br />Implement approval concept for invoices and invoice elements (e.g. price, tax, margin etc.). The problem is that different changes may require different responsible people to approve this,  this means you would need some indication which shows which approval is still outstanding. Of course a less detailed visual indication would be a red, yellow, green marker at the beginning of the invoice/element or background highlight<br />Allow to import existing bills (e.g. order -> invoice, offer -> confirmation -> delivery note ...)<br />Share media files between imported bills for easier searching. Maybe do this by creating a root element which all bills reference and show files of this root bill?<br />Show list for recommended purchase items + type tags e.g. re-order because empty, cross selling, promotion (if promotion already used, don't offer any longer) |
|            |      | **Warehouse Management**<br />Implement stock GSD stock importer *(SD specific)* |
|            |      | **Purchasing**<br />Create item list for purchasing          |
|            |      | **Accounting**<br />Implement GSD accounting importer *(SD specific)*<br />Print receivable of customer (also allow to do this from the client view in the Client Management) |
|            |      | **Client Management** (additional feature implementation)<br />Add list for top articles on profile page... important for customer calls<br />Add list for recommended purchase items + type tags e.g. re-order because empty, cross selling, promotion (if promotion already used, don't offer any longer)<br />Create a simple button to send an email to a customer, this also should have the option to change the mail address (e.g. drop down with all available email addresses and option to manually write it)<br />Add a geo map of the customers location (either on a real map or on the already added SVG maps) |
|            |      | **Client Management** (nice to have)<br />Create a map of all customers (maybe as data points or as heat maps)<br />Create a map of sales (maybe as data points or as heat maps)<br />Create default letter Doc (with/without letter head)<br />Make customers only visible/readable to authorized people (e.g. sales rep may only see his own clients)<br />Client view should be customizable since different groups have different interests and read permissions (e.g. sales reps, finance, etc.)<br />Allow to specify the accounting account (e.g. a customer who is a supplier may have the same account) |
|            |      | **Accounting Analysis**<br />Create different P&L structures<br />Create different balance structures<br />Create cash analysis structure<br />Create asset/depreciation structure<br />Create comparison feature for the above mentioned structures (budget, IFRS, ...) |

#### Archived

| Deadline | Done       | Task                                                         |
| -------- | ---------- | ------------------------------------------------------------ |
|          | 2021.11.14 | **Admin**<br />Implement password reset<br />Implement email sending<br />Implement global email server definition |
|          | 2021.11.14 | **Customer Management**<br />Add note types (e.g. phone, email, meeting, ...). Maybe similar to MediaType? |
|          | 2021.11.14 | **Job**<br />Created a job which runs exchange scripts<br />Create jobs |
|          | 2021.11.15 | **System**<br />Implement maintenance mode where no one can edit anything. |
|          | 2021.11.15 | **System**<br />*Duplicate:* Implement API only mode for modules, which disables UI interaction with a module completely (no navigation, no templates, ...) *solved with the navigation module settings incl. disabling routes* |
|          | 2021.11.16 | **ContractManagement**<br />Create a new media type "contract" |
|          | 2021.11.19 | **ContractManagement**<br />Contracts can have a different date of expiration and last renewal. (e.g. renewal needs to happen 1 month before contract end)<br />Define custom info deadline (global and optionally for a single contract)<br />Contracts can be assigned to a unit. |
|          | 2021.11.19 | **Billing**<br />Save original net value and discounted net value (currently only discounted net value is stored)<br />Save discounts |
|          | 2021.11.20 | **Media**<br />Create custom media types (e.g. contract) with l11n text/description<br />Create admin setting for handling media_type specifications |
|          | 2021.11.20 | **Billing**<br />Save number-format and the rendered number in the bill, currently only the format is saved and rendered on the fly which is bad for searching and performance. Maybe even ONLY save the number? |

## Todos

Todos/tasks which are not important enough to be part of the milestones.

| Priority | Done | Task                                                         |
| -------- | ---- | ------------------------------------------------------------ |
| high     |      | **Search**<br />Implement a tag search hook which finds content based on tags<br />Implement module specific search (e.g. :tasks title ...)<br />Implement global search hook (every module performs a search based on the search)<br />Create a api search filter which allows to search in a specific module only (e.g. in the shop app only search the shop, in the QA app only search in QA) |
| high     |      | **UI input**<br />In the AdvancedInput, implement predefined values (e.g. predefined/default tags)<br />In the AdvancedInput, implement mandatory predefined values (e.g. tags which cannot be deleted)<br />Implement AdvancedSelect (with auto filtering, none-element, multi-select, default-selects, must-have selects)<br />![Advanced select](img/todo/dropdown.png) |
| high     |      | **UI change**<br />Find a way to load a different page after a successful form result (e.g. reload account creation page) |
| high     |      | **Table**<br />Implement drag sortable table rows (https://htmldom.dev/drag-and-drop-table-row/). Implement the same concept for other elements, maybe abstract it straight away! |
| high     |      | **Table**<br />Implement export (local=visible data, external=all data)<br />Implement filtering (local=visible data, external=all data)<br />Highlight filtering of the filtered columns |
| high     |      | **Forms**<br />On change highlight the data/element that got changed<br />Invalid API responses should undo the UI changes<br />Removing a form from the DOM should unbind it<br />Adding a template to the DOM should modify its id/generate a custom/random id for the added element<br />Add/bind UI elements after adding them to the DOM<br />Consider to allow multiple/different add buttons which behave a little bit different<br />If a form has unsaved content the browser should ask if the user really wants to change the page or close it ("beforeunload"-Event) |
| medium   |      | **Logs**<br />Immediately send errors also via email to the admin/server email address if it is configured that way. |
| medium   |      | **Registration**<br />Allow users to register by themselves<br />Send a email after creating a profile/self-registration with login information |
| medium   |      | **Url format**<br />Change the url format in most modules from query parameter to path (e.g. /module/profile?id=Admin to /module/Admin/profile) |
| medium   |      | **Modules**<br />Many models would benefit from unit and app association. Sometimes models should only be available/associated with a specific unit (e.g. news article for website, backend, shop etc.) |
| medium   |      | **DataMapper**<br />The ::with() function uses blacklisting it should be changed to whitelisting for relations |
| medium   |      | **DataMapper**<br />This is useful for Item profile, Customer profile, Supplier profile etc. Alternatively find a way to implement it in `::withConditionals` ?! Or do we need a new function `::withParameters('memberName/columnName`?', [options]). Or just a `::with()` function which we also need  to specify for the future for which relations need to be loaded at all e.g. `::with('files', ['limit' => 5, 'sortBy' => 'createdAt', 'sortOrder' => 'ASC'], [Client::class])` I think the ::with(...) makes the most sense. Maybe this can also be combined with the withConditional. This way we can remove/merge withConditional. There is one problem, maybe we need a `::onlyWith` function, because we don't want to load all relations |
| medium   |      | **ActionManager**<br />Implement listeners for child elements if the selector is specified |
| medium   |      | **Action**<br />Create a action which adds/removes DOM elements<br />Log DOM changes to the user |
| medium   |      | **Modules**<br />Find a way to handle optional modules (e.g. comment module in the news module) in the past the Mapper was modified (comments were removed) if the comment module was installed. Somehow this is no longer available but maybe another solution could be a different Mapper which is replaced if the comment module is installed. But instead of replacing a complete file, a diff should be generated between the files and the ADDED lines should be merged. How to handle uninstall because here it doesn't work? I would need to know exactly what to remove. |
| medium   |      | **DataMapper**<br />In the DataMapper implement iterable fetch. Currently all models are returned in one go, additionally an iterator should be returned for iterable access in case of MANY results (e.g. Exchange module) |
| low      |      | **Email**<br />Continue implementation of email sending and receiving. |
| low      |      | **ER diagrams**<br />Checklist<br />Contact<br />DatabaseEditor<br />Draw<br />Messages<br />Monitoring<br />Shop |
| low      |      | **UI tabs**<br />[Template] Fix tab indices's. On many pages the tab indices's are broken (tabs, table/list, links, forms) |
| low      |      | **Surveys**<br />Currently the demo (demoSetup/\*) only uses one language (en). Generate surveys with multiple langauges similar to other module demos (e.g. Wiki, News). In that case also prefix the text with the language so it's easy to see which language is loaded e.g. `EN:` (like in the tag module demo)<br />Consider to add a closing paragrah. The description comes at the end, but maybe a paragraph at the end of the survey should be added?! |
| low      |      | **Modules**<br />The modules use the module name for identification in many places where the module id should be used for performance reasons |
| low      |      | **Modules/permissions**<br />In many places where permissions are used bad and different names are used. Sometimes the term "type" is used, sometimes the term "state" (PermissionState). Both actually represent a superficial category every module can define for permissions. (e.g. a state could be account, task, profile, tag, ...). The term "state" makes no sense since it isn't a state. The term "type" is also bad because in another place it is used to define (read, write, change, ...). Maybe we should simply call it PermissionCategory/category?! (files to change: NavElement, PermissionAbstract, PermissionState) |
| low      |      | **Graph**<br />Implement missing functionality:<br />Find cycles using graph coloring<br />Find a negative cycle<br />Find cycles with n length<br />Find cycles with odd length<br />Find islands<br />Check if strongly connected<br />Find longest path<br />Get the girth<br />Get the circuit rank<br />Get the node connectivity<br />Get the edge connectivity<br />Check if bipartite<br />Check if triangle free |
| low      |      | **QueryBuilder**<br />Implement missing functions such as sum, count, ... |
| low      |      | **DataMapper**<br />Reconsider the order of the `get(*)` parameters (e.g. depths/fill) |
| low      |      | **General**<br />Once read only variables become available many models can remove getter/setter function (e.g. ApplicationAbstract, ConnectionAbstract and various models) |
| low      |      | **DataMapper**<br />In the DataMapper when using getQuery() and then making a ->where(...) the where will often fail because the table name is suffixed with an integer e.g. `_3`. This means you need to know the depth of the query in order to manually write it. The query builder should figure this out by himself. It knows the `_INT` value from the `FROM` clause and should just overwrite in the where clause where needed. See the GSD Importer from the exchange module for reference. |
| low      |      | **DataMapper**<br />Only update changed relations (e.g. allow coder to tell the DataMapper what changed) |
| low      |      | **DataMapper**<br />Implement get() where the coder can tell the DataMapper which fields and relations to fill (this might be solved with a better `::with()` function. |
| low      |      | **Grammar**<br />Implement schema modification grammar (alter tables) |
| low      |      | **Router, EventManager, Hook**<br />Instead of doing 100% regex matching, combine it with a tree search, this should be faster |
| low      |      | **Text search algorithm**<br />Implement a decent full text search for files/variables which finds texts that are similar (e.g. similar spelling, only some words in between, maybe different word order, etc.) |
| low      |      | **OAuth2**<br />Implement client<br />Implement server       |
| low      |      | **ServiceWorkers**<br />Implement caching and responding     |
| low      |      | **Code**<br />Implement QR code creation<br />Implement QR code reader<br />Implement data matrix creation<br />Implement data matrix reader<br />Implement various bar code readers |
| low      |      | **Speech recognition**<br />Remove the speech recognition wrapper once it becomes standard |
| low      |      | **Voice commands**<br />Implement table/link navigation      |
| low      |      | **Input validation**<br />Implement nicer input validation (e.g. show check mark and x in the input fields / optionally)<br />![Input validation](img/todo/input_validation.png) |
| low      |      | **jsOMS Framework**<br />Consider to create a library function which finds the nearest element based on a select (horizontal and vertical search, `*.nearest()` does not work this way) |
| low      |      | **jsOMS UriFactory**<br />Consider to parse EVERY URL with the Uri factory. This however might cause double parsing and therefore bugs |
| low      |      | **Tabs**<br />The frontend loads the correct tab based on the provided fragment, but it is slow. Doing this in the backend can already fix this but the frontend implementation should be fixed, because this should be the job of the frontend. |
| low      |      | **Build process/website module display**<br />Text file with all the module git links<br />Download and install<br />Default inspections/tests (unit tests, info.json, language files used, language files in all languages same content, amount of languages, routes in controller available, dependencies valid, code coverage, phpstan, phpcs)<br />Add to database |
| low      |      | **Logs**<br />The "Log" tabs in many models should have a separate permission which hides them. Maybe a user needs to have read permissions of the monitoring module in order to see them? Alternatively it could be a *_MONITOR permission for the specific model in every module. This is a little bit finer but also expands the permission complexity |
| low      |      | **UI sections/portlets**<br />sections/portlets with a footer sometimes have problems with floated elements. e.g. a right floated button will break the layout if the left element(s) are too long causing wrapping.<br />> Solution: create flexbox with margin |
| low      |      | **Admin: Settings template**<br />In the Settings->Localization->Numeric the number format (decimal, thousands) don't have a spacer in between. Margin left doesn't work. |
| low      |      | **Admin**<br />The default Account mapper should not have a password reference, there should be a AccountLoginMapper which is used if anything needs to be done regarding the account password. Alternatively, think about a private field modifier which requires the programmer to specifically request the read/write permission for that field (password field). The reason for this is that otherwise the password hash might be dumped in case of an error |
| low      |      | **Auditor**<br />Consider to create foldable/tree view for json logs e.g. https://www.cssscript.com/json-data-tree-view/<br />Implement blockchain for the auditor. This either requires database locking (slow),modification of audit logs after inserts (slow) or a background process which calculates theblockchain (OK).<br />Create printable reports based on specific changes |
| low      |      | **Database Editor**<br />Implement basic functionality / queries in UI |
| low      |      | **Fleet Management**                                         |
| low      |      | **Helper**<br />Implement direct print instead of opening a new window with `document.getElementById('iHelperFrame').contentWindow.print();` |
| low      |      | **Investments**<br />Approval<br />Comparison/calculations   |
| low      |      | **Labeling**<br />Create default label layout for items      |
| low      |      | **Item Management**<br />ItemAttributeTypes should specify which datatype they expect. The ApiController needs to validate if a value can be created for an attribute type (check validation pattern, datatype, is required)<br />Show additional important item information for sales/purchase, currently too controlling/stats focused<br />Define some attributes mandatory (e.g. HC-code/tariff code number) |
| low      |      | **Kanban**<br />Implement card status (archive, public, inactive)<br />Implement unread cards/comments notification/highlight<br />Highlight card with new comments (e.g. make comment count background red?)<br />Consider to replace card comments with normal comments from the Comments module |
| low      |      | **Knowledgebase**<br />Implement category create/edit view<br />Implement doc create/edit view (similar to news/editor)<br />Add category back/up button when in a subcategory |
| low      |      | **Monitoring**<br />Implement integrity check based on installed version and remote hash list (see monitoring-security.tpl.php) |
| low      |      | **Messages**<br />Implement email sending/receiving<br />Implement internal message/conversion storage<br />Implement global messaging to users/groups in the app as notification. Allow to define which users and or groups to message, also define multiple localization if needed. Allow to create template messages (e.g. Server is going into maintenance in X minutes) |
| low      |      | **Organigram**<br />Create better organigram (better grouping, maybe as SVG)<br />Make the organigram printable<br />Make the organigram versioned/approved (e.g. for ISO) |
| low      |      | **Profile**<br />Define a default image for new profiles. However, don't create a new media file whenever a new profile is created but instead define one global image which than is loaded for all profiles which don't have a custom image. This makes it easy to replace the default image for all existing profiles and saves a lot of space. |
| low      |      | **Quality Assurance**                                        |
| low      |      | **QA**<br />Implement voting<br />Implement accepting answers<br />Implement question create view<br />Add question answer component/like comment in question<br />Make votes contain for who the vote is, this way the vote score sum for accounts is MUCH easier and faster<br />Create QA app with login |
| low      |      | **Supplier**<br />Create a view where you can see all bills of the supplier<br />Create a view where you can see all items of the supplier<br />[Doc] Create default letter Doc (with/without letter head)<br />[Payable] Print payable<br />[Analysis] Purchase EUR + gross profit<br />[Analysis] Quantity order, quantity articles<br />[Analysis] Segment purchase<br />[Analysis] Top articles<br />[Analysis] Cross selling<br />Allow to specify the accounting account (e.g. a customer who is a supplier may have the same account) |
| low      |      | **Tasks**<br />[Analyzer] Implement analyzing functionality (tasks created, answered, time required to finish task, always in time?)<br />Instead of hiding (or as an additional type) tasks created from other modules (e.g. support) make them link to the UI where it can be handled (e.g. ticket)<br />Make answer box on the right scroll down with the content, this way you can immediately respond without scrolling.<br />Attach custom event, if status is changed (e.g. trigger checklist event). Maybe don't do it, maybe other modules should instead check the status of the task!!!<br />Implement email notification on progress/changes (new task, forwarded, ...)<br />The unread task count is currently not really correct and needs to be fixed<br />Allow batch handling of tasks in the dashboard/overview for faster interaction (e.g. select and close)<br />Create a user calender for tasks which only shows when tasks are due<br />Don't show Tasks in dashboard which are far into the future, maybe create another list for this?<br />Implement has seen and unseen (use system where every task has a seen flag for a user if it is seen) |
| low      |      | **Calendar**<br />Load events back to a fixed amount of months (e.g. current month, previous month and next month)<br />Implement event popup in the UI on click<br />Create different interval templates (year, quarter, month, week, day)<br />Allow user to define the start of the week (e.g. Sunday, Monday)<br />Implement gantt chart<br />Create iCal parser/reader and builder<br />Create database, models and mappers |
| low      |      | **CMS**<br />Make file content view 100% container height<br />Allow content changes and saving<br />Ideas for applications based on modules (e.g. monitor/log dashboard, sales dashboard, calendar, support/ticket, clocking, Q&A, Wiki, shop)<br />Implement line numbers in code view<br />Implement code formatting / syntax highlighting<br />Allow different content types (e.g. pages, posts, ...) with individual templates |
| low      |      | **Workflow**<br />Implement an approval module which only runs a module/user specific action once it is approved. This functionality might be part of the workflow module or at least smoothly interact with this module. Additionally, it should probably make use of the Tasks module.<br />New customer is created (approve)<br />New bill is created (approve, validate)<br />New supplier is created (approve) |
| low      |      | **ReadOnly**<br />Find a way to implement a read only setting. This could be helpful for maintenance times. |
| low      |      | **UriFactory**<br />Consider to use `\urlencode()` on every query parameter in the UriFactory. |
| low      |      | **ModuleMapper**<br />Implement module description, name, createdAt in the database table and use them. Currently they are available in the model but not yet implemented in the database schema. |
| low      |      | **Templates**<br />In some forms there are 2 buttons which a user shouldn't accidentally press (a save and create button or delete button). Position them far apart by using flexbox positioning (e.g. Module->Support->Settings). |
| low      |      | **ModuleMapper**<br />Create a `::limit()` function which is similar in concept to the existing function `::sortBy()`. As a result the limit can be removed from most other functions. |
| low      |      | **ModuleInstaller**<br />In most module *Installer.php* scripts the `installExternal()` re-implements Api functionality. Instead of creating new functions maybe the installer scripts should mock the API requests? (e.g. CMS is using the API while Media is re-implementing many functions) |
| low      |      | **CMS**<br />Make pages editable<br />Make posts editable    |
| low      |      | **UI Slider**<br />Create a slider element with two elements which the user can slide (optionally also only one slider should be possible)<br />![Slider](img/todo/slider.png) |
| low      |      | **Demo setup - Billing**<br />Improve customer order randomization (types, dates) in the demo setup file `setupBillingClients.php`.<br />Create text lines in bills, currently no text lines are created only entries with items, but sometimes you want to write some text in an invoice |
| low      |      | **Billing**<br />Costs such as shipping, insurance etc. should not be hard coded but customizable costs stored in a separate table. |
| low      |      | **Demo setup - Support**<br />Use default values for ticket attribute types in some cases instead of always using custom values |
| low      |      | **Update**<br />Create update logic for application, resources, modules, ... in the Admin/ApiController (`apiCheckForUpdates`) |
| low      |      | **Billing**<br />Create setting for bill format per bill type (e.g. invoice, order, ...). NO! This should be handled with the different bill types! The bill types should also have a format defined and a default template. |
| low      |      | **Billing**<br />The bill archive should store the customer/supplier localized version since this is the official document. |
| low      |      | **Billing**<br />Customers and suppliers should have default invoice and delivery addresses which should be used if no other address or custom input is used. |
| low      |      | **Editor**<br />The tools above should directly insert the markdown into the textarea. |
| low      |      | **Kanban**<br />The kanban board currently assumes up to 4 columns, however there should be a layout which allows more than 4 columns. Don't use flexbox but min-width and max-width combined with a horizontal scrollable board content. |
| low      |      | **Media**<br />Find a way to allow file edits if the file is not in the database but just in the file directory. At the same time this should not be possible for database files. |
| low      |      | **DataMapperAbstract**<br />The SQL query building seems to bee too complicated in some cases including unnecessary joins (e.g. see `TagMapper::get()`) |
| low      |      | **DataMapperAbstract**<br />Implement data binding           |
| low      |      | **DataMappers**<br />Use `Mapper::TABLE` or string names in the mappers. At the moment both can be found. This is not concise. The `Mapper::TABLE` name is preferred in case of name changes. |
| low      |      | **Email**<br />Find a way to localize some hard coded email content. Pass localization array? Manually overwrite email body if a hard coded/default message should be returned (maybe by checking for a flag/status code)? |
| low      |      | **Temp directory**<br />Consider to create a temp directory in the main directory (Orange-Management) which can be used by all modules etc. Alternatively create this temp directory in `Modules/Media/Files` |

#### Archived

| Priority | Done       | Task                                                         |
| -------- | ---------- | ------------------------------------------------------------ |
| medium   | 2021.11.14 | **Code cleanup**<br />Many modules still have unnecessary getters/setters. This should be replaced with puplic members. Check the Developer-Guide on when to use getters/setters. |
| medium   | 2021.11.20 | **QA**<br />Make Questions QA App specific (check out WikiDoc)<br />Create different QA Apps (check out WikiApp) |
| low      | 2021.11.20 | **Code Coverage**<br />Adding `pathCoverage="true"` to the PHPUnit `.xml` file for path and branch coverage causes a memory overflow. Fix it. *Solution: Create separate .cov files and combine them. However, this will not be implemented as default due to much slower testing* |

## Features

Features to be implemented at a later stage *nice to haves*.

### Tasks & decisions

| Priority | Done | Task                                                         |
| -------- | ---- | ------------------------------------------------------------ |
| medium   |      | **Editor**<br />Create immediate text preview similar to a rich text editor or Typora. |
| medium   |      | **Admin**<br />Create a view where it's possible to create/activate, change and delete/deactivate hooks for events. |
| low      |      | **Editor**<br />Create special markdown content (calendar, chart, task, news, comment, media, ...)<br />Allow download as markdown, text, PDF, word<br />Implement versioning. |
| low      |      | **Event Management**<br />Implement goal definition. Goals could be based on tasks (every completed task represents x%), linear time line (every day represents x%), value based (a calculated value represents x%), manual input based (the user decides the completion %)<br />Add milestones |
| low      |      | **Project Management**<br />Implement goal definition. Goals could be based on tasks (every completed task represents x%), linear time line (every day represents x%), value based (a calculated value represents x%), manual input based (the user decides the completion %)<br />Add milestones |
| low      |      | **Promotion**<br />Implement goal definition. Goals could be based on tasks (every completed task represents x%), linear time line (every day represents x%), value based (a calculated value represents x%), manual input based (the user decides the completion %) |
| low      |      | **Finance**<br />Implement accounting forensics (Benfords Law, cent value distribution analysis, amount of bookings between specific amounts, amount * bookings between specific amounts, etc.) |
| low      |      | **Item Management**<br />Item view should be customizable since different groups have different interests and read permissions (e.g. sales reps, finance, etc.)<br />Show different prices on item profile frontpage (e.g. domestic, export, quantity discount) |
| low      |      | **Purchase**<br />Consider to add a purchased analysis, used analysis and manufactured analysis (currently only sales focused). Examples items delivered in time, bad quality ratio) |
| low      |      | **Kanban**<br />Allow board templates? maybe at least colors?<br />Allow card templates? maybe at least colors? |
| low      |      | **Billing**<br />Automatically create recurring bills (invoices, delivery notes, etc.) if a customer wants to receive items automatically |
| low      |      | **Media**<br />Create preview option for images (e.g. ctrl+mouse hover or a different "list-view" like in explorer)<br />Validate file size on the frontend before uploading<br />Automatically change the file encoding of text files<br />Enable image interlacing (in the past there was a bug)<br />Implement media encryption/decryption (optionally)<br />Implement media password protection for read (optionally)<br />Implement resumable uploads<br />Implement path changes in the frontend<br />Allow the modification of collections<br />Implement external resources (URLs, dropbox, aws, ...)<br />Allow to edit the breadcrumbs, which replaces them with a text field which can be changed then than automatically loads the new path<br />Implement temporary file storage (very useful for making files downloadable for a limited time). Maybe create a new temp file directory or database collection where a available_until timedate gets defined (must be handled in the database). The biggest problem is how to delete them, this requires a background process/task scheduler. Additionally, these files must have permissions because they may be only for one user or a group of users. |
| low      |      | **Messages**<br />Allow to transform a message as task<br />Implement push notification<br />Users may be invited to old conversations |
| low      |      | **Navigation**<br />Improve goto command to match based on proximity and only based on visible links<br />Consider to create on navigation language file (same as routing files) during the installation process<br />Create settings page which allows to modify the navigation in the module settings<br />Consider to implement child elements on hover (sidebar and content) |
| low      |      | **News**<br />Implement email/message notification on create |
| low      |      | **Profile**<br />Find a way to hide some contact/address information for some modules. Some information are only meant for specific modules (e.g. private address, phone number e.g. HR module) The reason why this is difficult is that this information should not be part of the model table but in the relation (many-to-many). At the moment the information in the relation table is not used apart from the relations it self. A solution could be to specify a filter in the relation in the mapper. Empty = all relations, filter = only populate the model array with relations which match the filter. |
| low      |      | **Support**<br />Allow support/tickets to be transformed to Q&A question and answers<br />Allow Q&A to be transformed to support<br />Create support app with login<br />TicketAttributeTypes should specify which datatype they expect. The ApiController needs to validate if a value can be created for an attribute type (check validation pattern, datatype, is required) |
| low      |      | **Tag**<br />Create settings with a set of default colors    |
| low      |      | **Settings**<br />Implement a setting which lets users see all content no matter the content language (e.g. all News) |
| low      |      | **Templates, Controllers, Views and Models**<br />Allow custom templates, controllers, views and models, which don't get replaced during updates (e.g. for ItemManagement, CustomerManagement, HR, ...). These should be stored in a directory called `Customized` in the parent directories *Controller*, *Themes*, *Views* and *Models*. Whenever a custom controller is uploaded/changed the routes of all the applications need to be checked and adjusted. |

#### Archived

| Priority | Done       | Task                                                         |
| -------- | ---------- | ------------------------------------------------------------ |
| low      | 2021.11.15 | **Tag**<br />*Not implemented:* Create a hook which gets triggered if a group is created. This hook also creates a tag. *Tags and groups are very different, this actually is a bad idea* |
| low      | 2021.11.20 | **Navigation**<br />Consider to implement tabs in the side bar. *Decision: No! There are already too many menus/tabs. This becomes too complicated/confusing.* |

## Bugs

### Tasks & decisions

| Priority | Done | Task                                                         |
| -------- | ---- | ------------------------------------------------------------ |
| high     |      | **DataMapper**<br />In some cases the array is required in the `::withConditional()` function. This seems to be the case if a model doesn't have the condition but a sub-model has it. The mapper should simply not use the conditional if it doesn't exist in the mapper (see `ItemManagement::BackendController` or `ClientManagement::BackendController` with the BillMapper, this is a stupid fix) |
| medium   |      | **Human Resource Management**<br />Fix employee list (see comment at the bottom, query builder bug) |
| low      |      | **KMeans**<br />In some weird cases the Cluster test fails. This happens approximately 5 / 100 test runs (invalid center coordinate value) |
| low      |      | **Dashboard**<br />Why does admin not have a dashobard? Everyone should have it! |
| low      |      | **Table**<br />The table overflow was fixed with putting them in a scrollable container (in the portlet). This broke the `.sticky` head, since the table no longer knows the head is out of view. Since it's in an overflow container it doesn't know about its changed scroll position. If this cannot be solved don't revert back because overflowing tables are much worse! |
| low      |      | **Rest**<br />There is a weird bug where the `multipart/form-data` cannot use the normal `boundary=` header to define the boundary. If this *correct* format is used the server somehow cannot populate the `php://input` correctly. If we move the `=` to a different position e.g. `bound=ary` this works fine. Currently this is solved by not using a `=` sign but `/`. This requires further inspections later on and could result in a bug with a different webserver (e.g. nginx). |

#### Archived

| Priority | Done       | Task                                                         |
| -------- | ---------- | ------------------------------------------------------------ |
| low      | 2021.11.14 | **FileLogger**<br />The logger is somehow *sometimes* logging in the main directory of OMS. Why? Debug it! |

### Details

#### Joins on same tables

Problem if joins on same tables (e.g. staff-list)

The tabbed join is the problem, the second query is the solution. The problem is that you need a different alias which is hard to created since th alias usually is suffixed with the depths which is a problem in this case since the alias has nothing to do with the depth.

A solution could be to index the joins by depths+join count e.g. account_2_1, account_2_2

```sql
SELECT `account_2`.`account_name1` as account_name1_2, `account_2`.`account_name2` as account_name2_2, `account_2`.`account_name3` as account_name3_2
FROM `hr_staff` as hr_staff_4
LEFT JOIN `media` as media_3 ON `hr_staff_4`.`hr_staff_image` = `media_3`.`media_id`
LEFT JOIN `profile_account` as profile_account_3 ON `hr_staff_4`.`hr_staff_profile` = `profile_account_3`.`profile_account_id`
        LEFT JOIN `account` as account_2 ON `media_3`.`media_created_by` = `account_2`.`account_id`
        AND `profile_account_3`.`profile_account_account` = `account_2`.`account_id`
LEFT JOIN `l11n` as l11n_1 ON `account_2`.`account_localization` = `l11n_1`.`l11n_id`
LEFT JOIN `media` as media_2 ON `profile_account_3`.`profile_account_image` = `media_2`.`media_id`
LEFT JOIN `account` as account_1 ON `media_2`.`media_created_by` = `account_1`.`account_id`;
```

```sql
SELECT `account_2`.`account_name1` as account_name1_2, `account_2`.`account_name2` as account_name2_2, `account_2`.`account_name3` as account_name3_2
FROM `hr_staff` as hr_staff_4
LEFT JOIN `media` as media_3 ON `hr_staff_4`.`hr_staff_image` = `media_3`.`media_id`
LEFT JOIN `profile_account` as profile_account_3 ON `hr_staff_4`.`hr_staff_profile` = `profile_account_3`.`profile_account_id`
    LEFT JOIN `account` as account_3 ON `media_3`.`media_created_by` = `account_3`.`account_id`
    LEFT JOIN `account` as account_2 ON `profile_account_3`.`profile_account_account` = `account_2`.`account_id`
LEFT JOIN `l11n` as l11n_1 ON `account_2`.`account_localization` = `l11n_1`.`l11n_id`
LEFT JOIN `media` as media_2 ON `profile_account_3`.`profile_account_image` = `media_2`.`media_id`
LEFT JOIN `account` as account_1 ON `media_2`.`media_created_by` = `account_1`.`account_id`;
```

The problem is that every object needs to have a unique id so we could do this like `_d3_o5` as alias.
The problem with that however is that this would work for the getQuery() function but in the populateAbstract we don't know the object id. But maybe we can solve it by also passing the object ID here?
This seems like a full weekend test!!! Better focus on other things first.

## Drafts, concepts & ideas

Drafts, concepts & ideas which are more complex or require more explanation.

### Invoice OCR

Steps:

1. Turn into image if it isn't image
2. Modify image (grayscale, remove noise, thresholding, dilate, erode, opening/morphology, canny, skew correction/deskew, rotate e.g. upside down or slanted)
3. Extract text (maintain layout)
4. Get all suppliers and match against invoice (find name, alternatively try `invoice match_code`)
5. Has supplier template defined? Find custom areas. Sometimes a page 2 template must be defined if the second page looks different.
6. Match template areas to invoice (consider slanted invoice, longer text etc.), extract partial images.
   1. Template areas should ideally contain a keyword and the actual value.
7. Parse partial images
8. Match according to `regex`
9. Find item list area from template (recurring elements unless only one element is defined)
   1. Start should be defined by keywords (e.g. table headline)
   2. Create sub definitions such as quantity/unit, single price, total price, ...
   3. How to identify end of list?
   4. How to handle multiline line elements (e.g. detailed article/service description)
   5. How to automatically find account (e.g. article number, description, template definition)? 

Software:

1. Tesseract + OpenCV + above mentioned steps
2. Some Api (e.g. google vision ai, amazon textract, amazon recognition)

### Database permission handling

#### Option 1

```sql
select ...
from ...
where ...
  (
    account_permission_account = ACCOUNT
    AND (account_permission_unit IS NULL OR account_permission_unit = 'UNIT')
    AND (account_permission_app IS NULL OR account_permission_app = 'APP')
    AND (account_permission_module IS NULL OR account_permission_module = 'MODULE')
    AND (account_permission_type IS NULL OR account_permission_type = 'TYPE')
    AND (account_permission_element IS NULL OR account_permission_element = 'THIS_ID')
    AND (account_permission_component IS NULL OR account_permission_component = 'COMPONENT')
    AND account_permission_permission = ???
  )
  OR
  (
    group_permission_group IN (...)
    AND (group_permission_unit IS NULL OR group_permission_unit = 'UNIT')
    AND (group_permission_app IS NULL OR group_permission_app = 'APP')
    AND (group_permission_module IS NULL OR group_permission_module = 'MODULE')
    AND (group_permission_type IS NULL OR group_permission_type = 'TYPE')
    AND (group_permission_element IS NULL OR group_permission_element = 'THIS_ID')
    AND (group_permission_component IS NULL OR group_permission_component = 'COMPONENT')
    AND group_permission_permission = ???
  )
```

#### Option 2

1. Check if general permission exists -> just do query
2. Check for specific element exists -> just do query but with column_id IN (... elements ...)

```php
::with(PermissionAbstractMapper::class, $permissions)
// this will create a where condition generated by the PermissionAbstractMapper::class e.g. call PermissionAbstractMapper::createWith($query)
```

### New DataMapper structure

```php
TestMapper::getAll()
    ->with('profiles', limit: 10, sortBy: 'id', sortOrder: SortOrder::ASC)
    ->with('profils/account')
    ->limit(TestMapper::class, 5)
    ->sortBy('id', SortOrder::ASC)
    ->execute();

TestMapper::getAll()
	->depth(3)
	->execute();

abstract class DataMapperAbstract
{
	protected object $mapper;

	protected static array $cache = [];

	protected int $type = 0;

	protected int $depth = 0;

	public static function clear()
	{
		self::$cache = [];
	}

	public function __construct(object $mapper)
	{
		$this->mapper = $mapper;
	}

	abstract function execute();
}

class ReadMapper extends DataMapperAbstract
{
	private $members = [];

	public function with(string $variable, int $limit = 0, $sortBy = '', $sortOrder = SortOrder::DESC) : self
	{
		// $split = \explode('/', $variable);
		// maybe> $members[$split[0]] = [\implode('/', $split[1..n], $limit, $sortBy, $sortOrder];
	}

	public function get()
	{
		$this->type = MapperType::GET;
	}

	public function execute()
	{
		switch($this->type) {
			case MapperType::GET:
				return $this->executeGet();
				break;
		}
	}
}

abstract class DataMapperFactory
{
	public const COLUMNS = [];

	public static function get()
	{
		return (new ReadMapper(static))->get();
	}

	public static function getAll()
	{
		return (new ReadMapper(static))->getAll();
	}

	public static function update()
	{
		return (new UpdateMapper(static))->update();
	}

	public static function delete()
	{
		return (new DeleteMapper(static))->delete();
	}
}

class TestMapper extends DataMapperFactory
{
	public const COLUMNS = [];
}
```

## Most recent changelog

### November 2021

#### New

##### Framework

* Sending basic emails with `mail`, `sendmail` and `SMTP` is possible
* Sending signed emails is possible.
* Reading and creating mailboxes with `IMAP` is possible
* Reading mailboxes with `POP3` is possible

##### Frontend

* Frontend messages can be manually closed with a close button (x)
* Frontend messages can be defined sticky
* Frontend messages may omit the title

##### Admin

* Implemented basic server/admin email settings
* Implemented password reset with reset emails
* Implemented read-only/maintenance mode (configurable in the `Admin` settings)

##### Billing

* Bill can have notes (very helpful for additional remarks later on e.g. from accounting/sales/purchasing)
* Bills have net/gross profit, sales, costs and discount as unnormalized values
* Bills store the bill number and the number format in the model

##### ContractManagement

* Create a new media type "contract" during installation
* Contracts can have  a renewal time in months set when the contract renewal must be done (latest).
* Contracts can have a flag which indicates if the contract auto renews.
* Added a global warning deadline until when users are informed before the renewal deadline runs out.
* Contracts can be assigned to a unit.

##### Editor

* Implemented editor doc types (similar to media types)

##### EventManagement

* Events have planned and actual costs/earnings.
* Accounts can be assigned to events with different purposes.
* Events can have attributes (incl. default attributes)

##### Job

* Jobs can be created in the Job module
* Created three jobs which run `monthly`, `weekly` and `daily` and execute some default tasks (e.g. email error logs to admin). These also have placeholders to run additional tasks (e.g. run exchange scripts)

##### Marketing

* Promotions have planned and actual costs/earnings.
* Accounts can be assigned to promotions with different purposes.
* Promotions can have attributes (incl. default attributes)

##### ProjectManagement

* Projects have planned and actual costs/earnings
* Projects can have attributes (incl. default attributes)

#### Bug fixes

* Fixed a bug where the tests created a log file in the main directory
* Fixed a bug where changing headers during the rendering process would conflict with already sent header information in the `WebApplication`. The response is now rendered independently, without sending it (first render data, then push the headers, then send the response).

##### QA

* Fixed a bug where the question and answer content where shorter than the score content on the side resulting in portlets without background color.

#### Other

* Removed many unnecessary getters and setters

##### Tests

* The overall code coverage improved to 91.8% (mid of November, this will go down as now additional functionality will be implemented)