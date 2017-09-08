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

### New Style and Improved Usability

When you open the new ATS it will look very familiar.

Earlier this year Mendix has released a restyled version of their cloud portal. We liked it so much that we decided to adopt it for ATS.

But there's more than only a new styling. We've simplified the navigation structure and reduced the number of screens. Finally the most important screens have been completely rebuild:

#### Dashboard

This is the first screen you see when you open your app in ATS. It shows you all test results and statistics on one page (exportable into a pdf).

We have improved the load time of the dashboard by precalculating all required data. It updates as soon as a job has finished.

#### Repository

Via the repository you can browser all your data: folders, actions, test cases and test suites. We've introduced a new layout on this page that is very much like file system explorers. You can perform actions on a single or many items at once. The powerful search-on-type function will search within subfolders.

#### Test case editing

Editing test cases is one of the main tasks in ATS. We've listened to your feedback to improve this page. Test cases can become very large, so we use the same list-like view as in the repository to show all test steps. When you click a step it will expand and expose all details for you to edit. Click again to collapse. Reordering of steps has been a pain and is now a joy. We give you drag and drop!

#### Results and logs

Browsing jobs results and logs is another common task. Again we're making use of the same list-view as in repository. Not only to be consistent, but to provider similar functions. Also all jobs are now updated in real-time down to the test case level. Run a big test suite and drill down into the job to see the live status and results of all contained items.

#### More

- improved log output (better readable)
- autocomplete function to search for actions, test cases or values
- complete rebuild: repository, results, logs details and test case/action edit page
- centralized settings page per app
- Unique icons with tooltips
- Description texts on many pages

## Faster Test Execution

A new hope... err test runner. The core component of ATS is the test runner. It interprets your test cases, test suites and actions, executes them and returns a result. We've rebuilt it from scratch with a single purpose in mind: performance.

We achieved to reduce the execution of test cases by 50% and more. This enables you to do more testing in less time.

Running test cases in parallel is another way to speed up execution time. While this was already possible before we've optimized it. The runner can now retrieve the supported concurrency level from your Selenium provider. It's no longer up to the user to configure this.

### Test suite execution type to deal with test case dependencies

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
* reliable job cancelling

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
- new statuses and results

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
