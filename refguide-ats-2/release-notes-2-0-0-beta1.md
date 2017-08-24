
Date: January 06, 2017

## Changes
* SSO with Mendix account
* projects are automatically synced from sprintr
* project administration permission is set for user if he is administrator of the sprintr project
* deeplink to open project directly (triggers SSO automatically)
* OS and browser are now shown in the logs
* support for selecting the OS when running a test
* responsive testing (select screen size when running test)
* improved performance via optimize security rules
* new link to open sprintr project directly from within ATS project

## Removals
* tenant config
* TenantAdministrator role
* libraries/projects/accounts can no longer be created in ATS
    * projects and accounts are synced from sprintr
    * libraries have been removed
