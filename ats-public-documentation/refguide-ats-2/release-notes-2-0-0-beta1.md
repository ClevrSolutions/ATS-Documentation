Date: September 18, 2017

## More Platform Integration

Getting started with ATS has never been easier. We've invested to make the onboarding for new users a smooth experience. Existing users can enjoy zero maintenance and a well-known user interface.

We did so by providing a single, multi-tenant SaaS instance of ATS in the Mendix cloud. This instance comes with the same styling and usability as the Mendix cloud portals.

No one wants to spend time on setting up and configuring an application before using it.

### Application Test Suite as a Service

ATS is now offered as a service. There's a single, multi-tenant instance in the Mendix cloud to serve all customers: 

<http://testing.mendix.com>

This instance is operated and maintained by Mansystems and Mendix. As a customer you enjoy the typical SaaS benefits.  Mansystems and Mendix deliver maintenance, updates, and fixes faster than ever. You can access new features as soon as we publish a new release.

All customers can use this instance without affecting each others work. Data is strictly separated per app. Every user can only access data from his apps.

### SSO and App Synchronization

You don't want to spend time on setting up and configuring an application before using it the first time? We agree!

As soon as you open testing.mendix.com you will be automatically signed in with your Mendix account. 

After login the ATS dashboard shows all your licensed apps. From here you will select one of your apps and start testing.

### A Mendix UI and Rebuild Pages

When you open the new ATS it will look very familiar.

Earlier this year Mendix has released a restyled version of their cloud portal. We liked it so much that we decided to adopt it for ATS.

But there's more than only a new styling. We've simplified the navigation structure and reduced the number of screens. Finally the most important screens have been completely rebuild:

Dashboard:

The first screen you see when you open your app in ATS. It shows you all test results and statistics on one page (exportable into a pdf).

We have improved the load time of the dashboard by precalculating all required data. It updates as soon as a job has finished.

Repository data browser (navigatable via "Test Cases")

Test case editing

Results and logs

- new UI
- autocomplete function to search for actions, test cases or values
- complete rebuild: repository, results, logs details and test case/action edit page
- centralized settings page per app
- drag and drop
- Unique icons with tooltips
- Description texts on many pages

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

## Introducing an API for Continuous Delivery & Deployment

Do you plan or already do practice DevOps in your team? Then you'll want to put in place continous delivery or even continuous deployment. To do so you'll need to automate as much as possible. Also the testing. Not only by automating the tests itself, but by automating the whole process. From triggering the test run to checking the results. With ATS this is now possible.

We've extended ATS with a new simple API. Via this API you can start your automated tests in ATS from any external tool. A good option for such a tool is Jenkins. We've documented how to setup Jenkins with ATS in a how to.

## More Changes

* All changes from 1.8 releases
* new reference guide
* Scheduled cleanup of logs
* Items of the same name in one folder are no longer possible
* improved performance via optimize security rules
* Drop-downs can now be configured directly within your parameter
* drop-down entries are checked to be unique

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

Some of above described changes made existing functionality obsolete so we could remove it.

- Datatypes: DateTime, Float and Currency
- tenant config removed
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

Many bugfixes and small changes, including everything from the 1.8 branch. Please check the release notes from 1.8 for these changes.
