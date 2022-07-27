# Organigram

```mermaid
flowchart TD;
    subgraph CTO
        DEVELOPMENT[Development\nCTO *ECM];
        DEVELOPMENT---TEAM_LEADER[Team Leader];
        TEAM_LEADER---SENIOR_DEVELOPER[Senior Developer &\nCode Reviewer];
        TEAM_LEADER---DEVELOPER[Developer];
        SUPPORT_SERVICE[Support & Service\nHOCS];
        SUPPORT_SERVICE---TEAM_LEADER_SUPPORT[Team Leader];
        TEAM_LEADER_SUPPORT---SENIOR_SUPPORT[Senior Consultant & Support];
        TEAM_LEADER_SUPPORT---SUPPORT[Consultant & Support];
        IT[IT\nHead of IT];
        IT---IT_DEVOPS[DEVOPS];
        IT---IT_CLERK[IT Clerk];
    end
    MANAGEMENT[Management\nCEO *ECM]---CTO;
    subgraph CFO
        FINANCE[Finance\nCFO *ECM];
        FINANCE---CHIEF_ACCOUNTANT[Chief Accountant];
        FINANCE---ACCOUNTS_RECEIVABLES[Accounts Receivables];
        FINANCE---ACCOUNTS_PAYABLE[Accounts Payables];
        HR[HR\nDHR *ECM];
        HR---PAYROLL[Payroll]
        HR---HR_CLERK[HR Clerks];
        PURCHASE[Purchase\nHOP];
        PURCHASE---PURCHASE_CLERK[Purchase Clerk];
    end
    MANAGEMENT---CFO;
    subgraph CSO
        SALES[Sales\nCSO *ECM];
        SALES---SALES_REP[Sales Reps];
        SALES---SALES_BACKOFFICE[Sales Backoffice];
        MARKETING[Marketing\nHOM];
        MARKETING---MARKETING_CLERK[Marketing Clerk]
    end
    MANAGEMENT---CSO;
    MANAGEMENT---QM[Quality Management\nDQM *ECM];
    QM---QM_CLERK[QM Clerk];
```

\*E: Executive Committee Member

## Key Functions

| Title                         | Name(s) |
| ----------------------------- | ------- |
| CEO                           |         |
| DQM                           |         |
| CTO                           |         |
| HOCS                          |         |
| Head of IT                    |         |
| CFO                           |         |
| DHR                           |         |
| HOP                           |         |
| CSO                           |         |
| HOM                           |         |
| Export Control Officer        |         |
| Fleet Manager                 |         |
| QMR                           |         |
| Emergency Responder           |         |
| Work Safety Officer           |         |
| Safety Officer                |         |
| Data Protection Officer       |         |
| Company Physician             |         |
| Waste Management Officer      |         |
| Fire Prevention Officer       |         |
| Equal Opportunities Officer   |         |
| Ladder Officer                |         |
| Officer for Severely Disabled |         |
| Internal Auditor              |         |
| Compliance Manager            |         |

## Responsibilities

Additional responsibilities are defined in the respective process documentation, [Document Owners](./Document%20Owner.md) and individual employee contracts.



2022-01-01 - Version 1.0

