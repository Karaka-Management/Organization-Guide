# Permission Change Management

Permission changes are sometimes necessary if a role of an employee changes or if the employee has to take over additional tasks. Such permission requests must get approved by the respective HOD and verified by the IT department. If the change request is justified the IT department changes the permissions for the employee.

Permissions should always be defined as low as possible and only get expanded if required. The IT department can decide to reject a permission change if they consider the request inappropriate.

## Flowchart

```mermaid
graph TD;
  REQUEST_HOD([Request from HOD])--->IT_CHECKS{IT: Other approvals necessary?};
  REQUEST_STAFF([Request from employee])-->APPROVAL_HOD[Approval by HOD];
  APPROVAL_HOD-->IT_CHECKS;
  IT_CHECKS--Yes-->FORWARD[IT: Forward request];
  FORWARD-->APPROVAL_RESPONSIBLE[Approval by responsible person];
  APPROVAL_RESPONSIBLE-->VALIDATE{IT: Is approved and appropriate?};
  IT_CHECKS--No-->VALIDATE;
  VALIDATE--Yes-->IMPLEMENT[IT: Implement permission changes];
  VALIDATE--No-->INFORM([IT: Inform employee and HOD]);
  IMPLEMENT-->INFORM;
```

2022-01-01 - Version 1.0

