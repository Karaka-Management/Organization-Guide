# Developer Onboarding: Cheat-Sheet

**How to initially setup the codebase?**

* run: `git clone -b develop https://github.com/Karaka-Management/Karaka.git`
* run: `git submodule update --init --recursive`
* run: `git submodule foreach git checkout develop`

**How to (re-)setup the demo application?**

* run: `php demoSetup/setup.php`

**Testing tools**

php: PHPUnit

* php setup run: `composer install` (requires composer to be installed)

js: Jasmine

**How to run unit/integration tests?**

* php:
  * run in main directory: `php -d pcov.enabled=1 vendor/bin/phpunit -c tests/phpunit_no_coverage.xml `
  * also possible for submodules if you want to test only a specific submodule (e.g. phpOMS)
* js:

**How to run code inspection?**

* run phpstan + phpcs + eslint: `Build/Helper/testreport.sh`
* run phpstan: `php vendor/bin/phpstan analyse --autoload-file=phpOMS/Autoloader.php -l 8 -c Build/Config/phpstan.neon ./`
* run phpcs: `php vendor/bin/phpcs ./ --standard="Build/Config/phpcs.xml" -s --report-junit=Build/test/junit_phpcs.xml`
* run eslint: `npx eslint jsOMS/ -c Build/Config/.eslintrc.json`



2022-01-01 - Version 1.0

