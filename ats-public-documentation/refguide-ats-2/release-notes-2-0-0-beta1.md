Date: January 06, 2017

## Changes

* All changes from 1.8 releases
* new reference guide
* updated security \(better performance\)
* Scheduled cleanup of logs
* Items of the same name in one folder are no longer possible

### Platform Integration

No one wants to spend time on setting up and configuring an application before using it.

* SSO with Mendix account
* projects are automatically synced from sprintr
* project administration permission is set for user if he is administrator of the sprintr project
* deeplink to open project directly \(triggers SSO automatically\)

* improved performance via optimize security rules

* new link to open sprintr project directly from within ATS project
* domain: testing.mendix.com

### Cross-Platform Testing

* OS and browser are now shown in the logs
* support for selecting the OS when running a test

* responsive testing \(select screen size when running test

### Terminology

* Package --&gt; Folder
* Datatypes
  * Integer --&gt; Number
  * String --&gt; Text
  * Enumeration --&gt; Drop-Down
  * Web Element --&gt; Page Element
  * Undefined --&gt; Any
  * Boolean --&gt; Boolean
* project --&gt; app

### Usability

* new UI
* autocomplete function to search for actions, test cases or values
* complete rebuild: repository, results, logs details and test case/action edit page
* simplified navigation structure
* centralized settings page per app
* Unique icons with tooltips
* Description texts

## Removals

* tenant config
* TenantAdministrator role
* libraries/projects/accounts can no longer be created in ATS
  * projects and accounts are synced from sprintr
  * libraries have been removed
* Folder visibility
* custom error message removed
* action type attribute no longer visible
* parameter type attribute no longer visible

### Bugfixes

Many :\)



