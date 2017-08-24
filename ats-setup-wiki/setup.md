This chapter describes the necessary steps after installation to complete the setup of ATS.

# User Accounts and License
Basic account creation and license.

1. Login as MxAdmin
1. Navigate to 'Accounts'
1. Create a new system administrator account ('SysAdmin').
1. Create a new tenant administrator account ('Admin') for the default tenant.
1. Navigate to 'License' and enter a valid license key. If you don't have a license, use the 'Mail License Request' button to request one.
1. Login as Admin
1. Create a new user account ('User')

# Data Import
## Core Actions
1. Login as Admin
1. Navigate to projects
1. Create two new libraries, 'Core' and 'Mendix' and give User the "Project Administrator" permission within the libraries
1. Login as User
1. Switch to Core library
1. Navigate to import page
1. Import the Core*.xml
1. Switch to Mendix library
1. Navigate to import page
1. Import the Mendix*.xml
1. Login as SysAdmin
1. Move both the 'Core' and 'Mendix' libraries from the 'Default' tenant to the 'Shared Core' tenant.

## Recorder Mappings
1. Login as SysAdmin
1. Navigate to Recorder Config
1. Import the Recorder_Config*.xml

# Create User Project
We now create a project that holds the test cases for the customer's app.

1. Login as user
1. Create a new project that includes the 'Mendix' library
1. Navigate to configuration
1. In the Selenium section, create a new record for your Selenium hub (local or somewhere in the cloud). Enter a name and the URL to the Selenium hub.
1. Under 'Applications' create a new record for your app's test environment. Enter name and URL.

<div class="alert alert-info">
For Browserstack you should add a custom string capability to your Selenium configuration:
 **Key**: *browserstack.selenium_version*, **Value**: *2.53.0*
</div>
