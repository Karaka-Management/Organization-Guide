# HR Flowchart

## Hiring

```mermaid
graph TD;
    IDENTIFY([Identify need for new position])-->APPROVAL[Position Approval];
    APPROVAL-->APPROVAL_SEARCH{Is approved?};
    APPROVAL_SEARCH--YES-->SEARCH[Search];
    SEARCH-->CHECK_APPLICATION{Application fits?};
    CHECK_APPLICATION--YES-->SKIP_FIRST{Is manager?};
    SKIP_FIRST--YES-->INTERVIEW_1[First interview];
    SKIP_FIRST--NO-->INTERVIEW_2;
    CHECK_APPLICATION--NO-->REJECT[Reject application];
    INTERVIEW_1-->CHECK_INTERVIEW_1{Interview was good?};
    CHECK_INTERVIEW_1--YES-->INTERVIEW_2[Second interview];
    CHECK_INTERVIEW_1--NO-->REJECT;
    INTERVIEW_2-->CHECK_INTERVIEW_2{Interview was good?};
    CHECK_INTERVIEW_2--YES-->CHECK_REFERENCES{Valid references?};
    CHECK_REFERENCES--YES-->INTERVIEW_3[Third interview];
    CHECK_REFERENCES--NO-->REJECT;
    CHECK_INTERVIEW_2--NO-->REJECT;
    INTERVIEW_3-->CHECK_INTERVIEW_3{Interview was good?};
    CHECK_INTERVIEW_3--NO-->REJECT;
    CHECK_INTERVIEW_3--YES-->VOTE{Vote hiring?}
    VOTE--YES-->SIGN_CONTRACT[Sign contract];
    VOTE--NO-->REJECT
    SIGN_CONTRACT-->TRAIN([Train employee])
```



2022-01-01 - Version 1.0

