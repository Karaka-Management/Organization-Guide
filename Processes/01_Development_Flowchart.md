# Development Flowchart

```mermaid
graph TD;
    SETUP_DEV_ENV([Dev: Setup Dev Environment])-->HAS_ACCESS{Has code access?};
    HAS_ACCESS-- YES -->FORK[Dev: Fork or Pull];
    HAS_ACCESS-- NO -->REQUEST_ACCESS[Dev: Request access via mail];
    FORK-->NEW_BRANCH[Dev: Create new branch];
    REQUEST_ACCESS--1-->HAS_ACCESS;
    NEW_BRANCH-->CHANGE[Dev: Make changes];
    CHANGE-->HAS_BUILD_CHANGES{Has SCSS/JS changes?};
    HAS_BUILD_CHANGES-- YES -->BUILD[Dev: Build SCSS/JS];
    HAS_BUILD_CHANGES-- NO -->TEST_CHANGE[Dev: Test changes locally];
    BUILD-->TEST_CHANGE;
    TEST_CHANGE-->IS_SUCCESSFUL{Is successful?};
    IS_SUCCESSFUL-- YES -->PULL_REQUEST[Dev: Pull request];
    IS_SUCCESSFUL-- NO -->FIX[Dev: Fix errors];
    FIX-->TEST_CHANGE;
    PULL_REQUEST-->AUTOMATIC_CHECKS[System: Automatic checks]
    AUTOMATIC_CHECKS-->MANUAL_CHECKS[Reviewer: Manual checks]
    MANUAL_CHECKS-->IS_ACCEPTED{Is accepted?};
    IS_ACCEPTED-- YES -->MERGE([Reviewer: Merge]);
    IS_ACCEPTED-- NO -->FIX;
    FIX-->TEST_CHANGE;
```

2022-01-01 - Version 1.0
