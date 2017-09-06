Date: September 18, 2017

## More Platform Integration

No one wants to spend time on setting up and configuring an application before using it.

* SSO with Mendix account
* projects are automatically synced from sprintr
* project administration permission is set for user if he is administrator of the sprintr project
* deeplink to open project directly \(triggers SSO automatically\)
* domain: testing.mendix.com

### A Mendix UI and Rebuild Pages

- new UI
- autocomplete function to search for actions, test cases or values
- complete rebuild: repository, results, logs details and test case/action edit page
- simplified navigation structure
- centralized settings page per app
- Unique icons with tooltips
- Description texts on many pages
- Drop-downs can now be configured directly within your parameter
  - drop-down entries are checked to be unique
- Dashboard
  - improved performance by precalculating all data
  - updated after every job
  - Dashboard calculations have changed​

## Test Runner

A new hope... äh test runner.

You can't see it, but you'll feel it.

* new test runner
  - improved performance
  - automatic determination of possible concurrency
  - live progress update with drill-down up to test case level
  - improved log output \(better readable\)
  - reliable job cancelling
  - new statuses and results
* Test suite execution type to deal with test case dependencies
### Cross-Platform Testing

* OS and browser are now shown in the logs
* support for selecting the OS when running a test

* responsive testing \(select screen size when running test

## Continuous Delivery

* CI/CD API
  - templates
  - WS interface

## More Changes

* All changes from 1.8 releases
* new reference guide
* Scheduled cleanup of logs
* Items of the same name in one folder are no longer possible
* improved performance via optimize security rules

### Terminology

- Package --&gt; Folder
- project --&gt; app
- Datatypes
  - Integer --&gt; Number
  - String --&gt; Text
  - Enumeration --&gt; Drop-Down
  - Web Element --&gt; Page Element
  - Undefined --&gt; Any
  - Boolean --&gt; Boolean
- job

### Removals

Best code is no code. And the best functionality is the one that you don't need.

- Datatypes: DateTime, Float and Currency
- tenant config
- TenantAdministrator role
- libraries/projects/accounts can no longer be created in ATS
  - projects and accounts are synced from sprintr
  - libraries have been removed
- Folder visibility
- custom error message removed
- action type attribute no longer visible
- parameter type attribute no longer visible
- proxy settings
- concurrency limit on selenium endpoint \(no longer required\)
- log depth settings removed, we now log every step down to core actions
- enable screenshot \(both on job config and test step config\)
- quick-run

### Minors

Many bugfixes and small changes, including everything from the 1.8 branch.

