# Layout
 
- [ ] Change to flexbox 

# Framework

## L11nManager

- [ ] It is only a LanguageManager actually! => Rename to LanguageManager!
- [ ] Localization should not have it's own language array and rather use the "L11nManager/LanguageManager"

## Request

- [x] Constructor should contain the request?
- [x] Root path should be a setter?
- [x] Sanitize javascript always - STUPID, just drop if db insert
- [x] Modify so that it can be used to create a request not just for parsing incoming requests

## Button injection

- [ ] Fix button injection (e.g. report export to excel)

## ModuleFactory, ModuleManager & Dispatcher

- [ ] Don't store modules in every class put them only in one and share them? Dispatcher may need them?

## Localization

- [ ] Move language array to separate language manager? or move to account? But at the same time language is also application bound? Not every account needs same language over and over

## Datamapper

- [ ] Cleanup
- [x] Newest should support limit and return array
- [ ] Datamapper should consider permissions (optional parameter? or query as optional parameter)
- [ ] Split relation get from normal get. This way it's possible to fill the relation later on
- [x] Support serializable. Same as Json just calling a serialize and unserialize function on insert/select

## Uri

- [x] Http uri reverse set and constcruct parameter. Set root path and pass uri in construct (optional)

## Rest

- [x] Pass Request and Uri to class

## Response 

- [ ] Should not have head as member since response doesn't necessarily have a html head!

## Log 

- [ ] Implement verbose parameter for all log functions
- [ ] Create database logger

## QueryBuilder & Grammar

- [ ] Implement joins

# Modules

Uninstalling with constraints is rather difficult. need to remove constraints from all modules if there are any before 
table drop is possible.

- [ ] Install for navigation should have an interface? Or a global module interface for this
- [ ] Navigation needs a uninstall directory in order to not only install navigation elements but also remove them. Actually navigation can do this on it's own but other modules might not be able!

## Business

- [ ] Fix positions
- [x] Rename to Organization
- [ ] Maybe make Departments, Units, Positions as madules???

## Production

- [ ] Add articles view (list & create)

## Tasks

- [x] Adjust Tasks tables
- [x] Create datamapper
- [ ] Tasks should support cron like schedules?!

## PersonnelTimeManagement

- [ ] Adjust tables
- [ ] Create datamapper

## Charts

### Charts types

- [ ] Pie Chart
- [ ] Area Chart
- [ ] Stacked Chart
- [ ] Mixed Chart
- [ ] Bar Chart
- [ ] Column Chart
- [ ] Bubble Chart

### Features

- [ ] Create chart based on settings
- [ ] Auto-resize chart (careful there are different types of resizes, not all need to result in a window resize)

## Reporter

- [ ] Newest should be overwritten in Reporter mapper (newest by template)

## Media

- [ ] Don't return uploaded id. Return full object (__toString())

# Tests

- [ ] Implement code coverage with xdebug

## Framework

- [ ] Create Math test
- [x] Model test
- [x] Module test
- [ ] Remove almost all createdAt setters. Testing should use reflection!!!

# Dev splash screen

- LOC chart
- LOC coverage in % chart (stacked)
- phpcpd chart
- PhpMetrics chart (maintainability, accessibility, simplicity, volume, reducing bugs)
- Todos, fixme, bugs etc chart
- Linting errors
- CS violations
- Security issues
- Mess detections

# Highscore

- LOC month 
- Issues fixed
- Issues opened

