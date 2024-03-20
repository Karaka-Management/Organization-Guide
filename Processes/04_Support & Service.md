# Support & Service

Support or any other software related services are only allowed if the customer has signed the [Customer Data Protection Policy](./Sales/Customer%20Data%20Protection%20Policy.md) (**R1**) and the [Customer Service Agreement](./Sales/Customer%20Service%20Agreement.md) (**R2**). This ensures that customer data access is legally and contractually covered. The customer Customer Service Agreement regulates the responsibilities and liabilities.

| Key Objective               | Target | Achieved |
| --------------------------- | ------ | -------- |
| Great customer satisfaction (CSAT) | >= 4.0 | YES      |

In general, only people authorized by the customer are allowed to make any support or service requests. Authorized persons are defined in the Customer Service Agreement and can only be adjusted by the respective persons int the Customer Service Agreement. (**R3**)

## Data migration

The customer and the support employee need to define the exact goals, data structure and migration strategy before it can be executed. These definitions must be put on the offer for the customer including a cost evaluation based on the time needed to perform the data migration and the complexity of the data migration. The cost, time and complexity estimation must only be done/approved by a senior employee (employee with more than 3 years of experience in the Support & Service department), team leader in the Support & Service department or HOCS. (**R4a**) (**R4b**)

Only after the binding approval in writing of the offer by the customer the order confirmation will be created (see sales process) and then the data migration can be performed. (**R5**)

## Setup & configuration

The software environment setup can be done by either the customer themselves or by an employee in the Support & Service department. The employee in the Support & Service department must be a senior employee in this department, team leader or the HOCS. (**R6**)

In case the customer requests a custom installation (not virtualized) or a custom configured virtualized environment the support & service employee must only do this together with the responsible person for IT on the customer side (e.g. Head of IT). (**R7**)

Under no circumstances is the employee allowed to alter any permissions, change software or hardware settings on the servers of the customer or provide IT support/consultation which is unrelated to the setup of the software environment or third party software and not approved in the [Approved Customer Software]() (**R8**). Only the CTO is allowed to approve new customer software after testing, the testing is documented with the [Third Party Software Validation - New]() and [Third Party Software Validation - Update](). (**R9**).

### Environment

The easiest way is to provide the customer with the default virtualized environment image and the configuration details. Default images are available for VirtualBox, VMWare and Hyper-V. The recommended configuration options can be found in the [System Requirements](https://github.com/Karaka-Management/User-Guide/blob/develop/setup/install.md#server-recommendations). (**R10**)

The customer is required to provide the necessary permissions to install and prepare the environment or perform these tasks under the guidance of the support & service employee. 

**No data (incl. passwords) from the customer must be stored by the support & service employee.** (**R11**)

### Software installation and configuration

Only the following software components can be installed and configured by the support & service employee:

* PHP incl. the required and recommended extensions
* Webserver (nginx or apache2)
* Databases (Postgresql, MariaDB, SQLSrv, Sqlite)
* Cache (Redis or Memcached)
* Third party software which is required by the core application or official modules

The software to be installed must be ordered by the customer, the support & service employee cannot install software which the customer didn't request previously.

> By default all offers for setup & configuration include PHP, Apache2 and MariaDB.

If the customer requests additional software to be installed and/or configured this is only possible for software related to the application and if the effort to install the software is reasonable compared to the previously accepted offer from the customer. In such a case the customer (must be a authorized person from the customer) can send a simple email requesting the additional software setup & configuration. (**R5**) Example:

> Dear Sir or Madam,
>
> I herewith request the additional setup and configuration of the software XXX during the installation and configuration.
>
> Best regards,
>
> YYY 

### Main application & modules

During the application installation the support & service employee has to perform the tasks defined in the [Application Install Checklist](./Support/Application%20Install%20Checklist.md). The checklist form can only get changed by the CTO. (**R12**)

## Customization

The customer and the support employee need to define the exact goals before it can be implemented. These definitions must be put on the offer for the customer including a cost evaluation based on the time needed to perform the customization and the complexity of the customization. The cost, time and complexity estimation must only be done/approved by a senior employee (employee with more than 3 years of experience in the Support & Service department), team leader in the Support & Service department or HOCS. (**R4a**) (**R4b**)

Only after the binding approval in writing of the offer by the customer the order confirmation will be created (see sales process) and then the customization can be performed. (**R5**)

## Training

The training depends on the needs of the trainee. The following training programs exist:

* Customer administrator / Key-User
* End-User
* Third party developer

The different training programs put focus on different aspects of the application. The general training program defined by the CTO can be found in the [Training Manuals](./Support/Training%20Manuals). (**R13**)

## Maintenance

Customer maintenance is performed once a year per customer with a maintenance contract. The Support & Service department schedules the maintenance with the customer. The maintenance tasks to be performed are defined by the CTO in the [Maintenance Checklist](./Support/Maintenance%20Checklist.md). (**R14**)

The customer receives a copy of the maintenance report after it is completed from the support & service employee.

Customers without a maintenance contract can also schedule a maintenance but have to pay higher fees according to the prices are defined in the [Pricing Policy]()

## Support

All customer support requests must be documented as customer tickets in the IT system. Customer requests are reviewed and categorized according to their content and priority. This task is performed by senior employees in the Support & Service department, team leaders in this department or the HOCS. (**R15**)

Every closed support ticked gets followed up with a automatic email which asks the customer to rate his satisfaction with the support. (**R16**)

2024-03-20 - Version 2.0
