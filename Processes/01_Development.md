# Development

| Key Objective                    | Target                                                         | Achieved |
| -------------------------------- | -------------------------------------------------------------- | -------- |
| Tasks & todos get solved         | > 100 tasks/todos get solved per year (if available)           | YES      |
| Milestones are completed on time | > 80% of all milestones are completed with less than 20% delay | YES      |
| Consistent code style            | < 10 code style errors exist in the latest release version     | YES      |
| Code is tested                   | > 90% code coverage is achieved                                | YES      |
| Code tests are successfull       | 100% of all tests are successful (no errors or failures)       | YES      |

## Development environment

The setup and configuration of the development environment is in the hands of every developer themselves. However, it is recommended to follow the setup instructions in the [Developer-Guide](https://github.com/Karaka-Management/Developer-Guide/blob/develop/general/setup.md).

## Code of conduct

Every organization member and contributor to the organization must follow the [Code of Conduct](../Policies%20&%20Guidelines/Code%20of%20Conduct.md).

## Becoming a contributor

For public repositories you can immediately start by creating forks and pull requests. For private repositories which are necessary to setup the complete developer environment, feel free to request access. Please not that we may not immediately give you access to private repositories and instead will give you smaller tasks regarding public repositories. Please contact info@jingga.app for more details. (**R1**)

For all contributions our [Contributor License Agreement "CLA"](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/HR/Hiring/Individual%20Contributor%20License%20Agreement.md) comes into effect. (**R2**)

## Code changes

### Topics / Tasks / Todos

Generally, the development philosophy is result orientated. This means that anyone can propose tasks, pick up existing tasks or right away implement their code changes. However, implementing code changes without consulting with a senior developer in advance has a much higher risk of code changes not getting acepted. The easiest way to discuss a code change idea in advance are the github [issues](https://github.com/Karaka-Management/Karaka/issues) or [discussions](https://github.com/Karaka-Management/Karaka/discussions).

Developers are encouraged to pick open tasks with high priorities according to their own skill level. Senior developers may  directly assign tasks to developers based on their importance. New developers may find it easier to start with a task that has a low  priority as they often also have a lower difficulty.

Open tasks can be found in the project overview: [Todos](https://github.com/orgs/Karaka-Management/projects/10)

The open tasks are reviewed once a month by a senior developer. The senior developer updates the project overview if necessary and requests feedback regarding development status of important tasks under development. During this process important tasks may also get directly assigned to developers. This review is performed on a  judgmental basis by the senior developers.

### Quality

#### Code style

Code changes must follow the [style guidelines](https://github.com/Karaka-Management/Developer-Guide/tree/develop/standards) (**R3**). Additionally, the automatic code style inspection tools must return no errors, failures or warnings. Developers should test their changes with inspection tools and configurations mentioned in the [inspection documentation](https://github.com/Karaka-Management/Developer-Guide/blob/develop/quality/inspections.md) in advance before submitting them for review. (**R4**)

In rare cases errors, failures or warnings during the automatic inspection are acceptable. Reasons can be for example special cases which are difficult to automatize or must be individually configured in the inspection settings. If errors, failures or warnings for a code change are acceptable or if inspection configuration changes are necessary is decided by the senior developer performing the code review. (**R5**)

Automated checks which are run during the review process (**R4**):

```sh
php ./vendor/bin/phpcs ./ --standard="Build/Config/phpcs.xml"
php ./vendor/bin/php-cs-fixer fix ./ --config=Build/Config/.php-cs-fixer.php --allow-risky=yes
php ./vendor/bin/phpcbf --standard=Build/Config/phpcs.xml ./
php ./vendor/bin/rector process --dry-run --config Build/Config/rector.php ./
npx eslint ./ -c ./Build/Config/.eslintrc.json
find . -regex '.*\.\(cpp\|h\)' -exec clang-format -style=file:Build/Config/.clang-format -i {} \;
```

#### Tests

Code changes must follow the inspection guidelines (i.e. code coverage) mentioned in the [inspection documentation](https://github.com/Karaka-Management/Developer-Guide/blob/develop/quality/inspections.md) (**R6**). Developers should test their changes with inspection tools and configurations mentioned in the [inspection documentation](https://github.com/Karaka-Management/Developer-Guide/blob/develop/quality/inspections.md) in advance before submitting them for review. (**R7**)

In rare cases it might be not possible to follow the inspection guidelines. In such cases the senior developer performing the code review may decide if the code change still gets accepted. (**R8**)

Automated tests which are run during the review process (**R7**):

```sh
php ./vendor/bin/phpunit -c tests/PHPUnit/phpunit_default.xml
php ./vendor/bin/phpstan analyse --no-progress -l 9 -c Build/Config/phpstan.neon ./
./Build/Config/jasmine_build.sh && npx jasmine --config=Build/Config/jasmine.json
./cOMS/tests/test.sh
```

Additional inspections which are run but might be ignored during the review depending on the use case are mentioned in the [inspection documentation](https://github.com/Karaka-Management/Developer-Guide/blob/develop/quality/inspections.md) as other checks. (**R7**)

##### End-To-End tests

End-To-End tests simulate the user interaction with the application in the browser. These tests can be found in `tests/Web` and can only be run on a machine with `Chrome` and a window manager installed (these tests don't run in a pure CLI environment). Currently, these tests can only be run manually and are optional.

```sh
node test/Web/Backend/Install.js
```

#### Performance

Developers should occasionaly check performance statistics. At this point no target metrics are defined.

Since the primary application is a web based application a similar tool as the Google lighthouse tool can be used to inspect the application for best practicies which can significantly improve the application performance. The sitespeed.io tool shows potential performance improvements and slow pages. With the php trace and profiler enabled in the `php.ini` file the VM automatically generates profiling and trace reports for every web request. These can be found in the webgrind logs directory and inspected in webgrind and dropped into the trace visualizer for a flame chart visualization. With mysqldumpslow you can inspect slow sql queries which may need optimization.

1. Automatic trace and benchmark generation with every web request in `/var/www/html/webgrind/Logs`
2. Webgrind view `http://vm_ip:82`
3. Trace visualization `http://vm_ip:81`
   1. Download the latest trace from `http://vm_ip:82/Logs`
   2. Drag and drop that downloaded `*.xt` file in the trace visualizer
4. `sitespeed.io ./Build/Helper/Scripts/sitespeedDemoUrls.txt -b chrome --outputFolder /var/www/html/sitespeed`
5. Slow query inspection.

```sh
mysqldumpslow -t 10 /var/log/mysql/mysql-slow.log
mysqldumpslow -t 10 -s l /var/log/mysql/mysql-slow.log
```

#### Code review

In addition to the automatic code review performed by the various inspection tools such as (phpcs, phpstan, phpunit, eslint and custom scripts) a senior developer must check the proposed code change before it is merged with the respective `develop` branch. Only upon the approval by the reviewer a code change requests gets merged as no other developers have permission in the software to make such code merges.

In case a code change request is not approved the reviewer states the reason for the decision, this may include some tips and requests which will allow the contributor to make improvements so that the code change may get approved.

If the code reviewer only finds minor issues with the proposed code change the reviewer may make small changes to the proposed code change and inform the contributor to speed up the implementation process. Code reviewers are encouraged to do this with new contributors to avoid long iteration processes and to not discourage new developers. However, communication is key and severe issues with code change requests or if the contributor already made multiple code change requests in the past the reviewer should not implement the improvements by himself and rather decline the code change requests with his reasoning. (**R5**+**R8**)

#### UI tests

While UI tests can be part of unit, integration or system tests the `cssOMS` repository also includes a simple test suit at [http://127.0.0.1/cssOMS/tests/app](http://127.0.0.1/cssOMS/tests/app) which allows developers to manually test UI elements and check how they work.

In the demo application it is possible to highlight html and css warnings (e.g. missing attributes, deprecated tags, inline styles, ...). In order to activate the live debugging add `&debug=true` to the end of your url.

In the demo application it is also possible to generate a list of html and css warnings by running a script which automatically traverses the application and searches for potentially bad html or css.

1. Open the website in your browser
2. Log into the (demo) application
3. Copy the entire content of `tests/Web/Backend/Debug.js`
4. Paste the content into the console in your browser and press enter
5. Wait until the browser is done loading all the pages (see limit pageLimit)
6. At the end of the console output you should find a table with stats regarding potentially problematic html/css

#### Demo

Some code changes may also require changes or extensions in the demo setup scripts. The demo setup script tries to simulate a "real world" use case by generating and modifying mostly random data. This is also a good way to setup and “manually” test the code changes in a larger picture. The demo setup script can be found in the [demoSetup](https://github.com/Karaka-Management/demoSetup) repository. The demo setup script takes a long time due to the large amount of user input simulated data which is generated. Therefore it is recommended to run this only sporadically. (**R9**)

```sh
sudo -u www-data php -dxdebug.remote_enable=1 -dxdebug.start_with_request=yes -dxdebug.mode=coverage,develop,debug demoSetup/setup.php
```

#### Test Classification

```mermaid
quadrantChart;
    x-axis Low Level --> High Level;
    y-axis Low Importance --> High Importance;
    PHPStan: [0.2, 0.5];
    *UI tests: [0.8, 0.05];
    Code Style: [0.1, 0.1];
    PHPUnit: [0.5, 0.75];
    cOMS/tests.sh: [0.2, 0.2];
    Jasmine: [0.3, 0.5];
    *Selenium: [0.9, 0.9];
    *Sitespeed: [0.75, 0.25];
    *Demo: [0.95, 0.95];
    *Other: [0.3, 0.05];
```

\* Optional and/or manual

#### Documentation

Occasionally new code or code changes also require new documentation or documentation changes. Developers should make sure that the new code is also reflected in the existing documentation ([Developer-Guide](https://github.com/Karaka-Management/Developer-Guide), [User-Guide](https://github.com/Karaka-Management/User-Guide) and/or module documentation) or if additional documentation is necessary.

#### Improvements, features, bugs

If a developer (or employee in general) has an idea for an improvement, feature or finds a potential bug it should be reported at [https://github.com/Karaka-Management/Karaka/issues](https://github.com/Karaka-Management/Karaka/issues). A senior developer has to check these issues and decide how to proceed with them. The decision how to proceed with the issue must be explained by the senior developer as a response in the issue. Possible steps are:

* Accept the issue and put the task into the [Todos](https://github.com/orgs/Karaka-Management/projects/10)
* Dismiss the issue with an explanation

### Release flow

In case SCSS/CSS or JS files got changed they must get re-built locally before comitting the code change:

```sh
npm build release # or npm build develop during testing
npm build scss
```

Code changes must be performed in a new branch. A new branch can be created with:

```sh
git checkout -b new-branch-name
```

The name of the branch can be chosen freely however, it is recommended to follow the following branch naming conventions:

* `feature-*` for feature implementations
* `hotfix-*` for security related fixes/improvements
* `bug-*` for bug fixes
* `security-*` for security related fixes/improvements
* `general-*` for general improvements (i.e. documentation, code style & performance improvements)

```mermaid
%%{init: { 'gitGraph': {'mainBranchName': 'master'}} }%%
    gitGraph
       commit
       branch hotfix-xxx
       commit
       checkout master
       branch develop
       checkout master
       merge hotfix-xxx
       checkout develop
       branch bug-xxx
       commit
       commit
       checkout hotfix-xxx
       commit
       checkout master
       merge hotfix-xxx
       checkout develop
       merge bug-xxx
       commit
       checkout develop
       branch feature-xxx
       commit
       commit
       commit
       checkout develop
       merge feature-xxx
       checkout master
       merge develop
       checkout develop
       branch general-xxx
       commit
       checkout develop
       merge general-xxx
       branch security-xxx
       commit
       commit
       checkout develop
       merge security-xxx
       checkout master
       merge develop
       
```

The senior developer who performs the code review merges the change request into the `develop` branch after their successful code review. Unsuccessful reviews lead to change requests by the original developer, other developers who can make the requested changes, changes by the senior developer who performed the review, or dismissal of the changed code. (**R10**)

## Approved dependencies

### Customer dependencies

Developers may only rely on the dependencies defined in [Approved Customer Software](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/Support/Approved%20Customer%20Software.md) when developing a solution. If new software should be added to this list or a different version is required developers should make a request with their team leader/head of department who forwards this requests if appropriate to the CTO and explain the reasoning for the different dependency needs. The CTO can decide if the dependency will be accepted. (**R11**)

### Developer dependencies

Developers may only rely on the dependencies defined in [IT Equipment & Software](https://github.com/Karaka-Management/Organization-Guide/blob/master/Processes/IT/IT%20Equipment%20%26%20Software.md). If new software should be added to this list or a different version is required developers should make a request with their team leader/head of department who forwards this requests if appropriate to the CTO and explain the reasoning for the different dependency needs. The CTO can decide if the dependency will be accepted. Changing the package managers such as `composer.json` or `package.json` is not allowed by anyone else than the CTO. (**R12**)

## Other related documents

* [Confidentiality Policy](../Policies%20&%20Guidelines/Confidentiality%20Policy.md)
* [Organization Activity Policy](../Policies%20&%20Guidelines/Organization%20Activity%20Policy.md)
* [Tutorials](./Development/Tutorials)

2024-03-20 - Version 2.0
