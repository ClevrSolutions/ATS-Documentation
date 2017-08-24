<div class="alert alert-warning">
When upgrading, you must always upgrade to the next higher version. You cannot skip a release when upgrading. Downgrading is not possible.
</div>

The simplified general upgrade procedure for ATS consists of the following steps:

1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS
1. Import the latest Core and Mendix actions
1. Import the latest recorder mappings
1. In case of local Selenium: Replace other ATS components with latest versions (Selenium, IEDriver, Chromedriver)

For detailed upgrade procedure consult the following chapters.

# Database shrinking
Upgrades can result in increased disk usage by the database while the database actually didn't grow. To shrink the database you have to create a backup and restore this backup. The restore process will free disk space.
More detailed information on this issue: [Here](https://support.mendix.com/hc/en-us/articles/206793070-Database-maintenance-size-reduction) and [here](https://forum.mendixcloud.com/link/questions/8816)

Apply this procedure to shrink the database:

1. Finish upgrade procedure and start ATS app
1. Stop ATS app
1. Backup database
1. Restore database
1. Start ATS app

# 1.7 to 1.8
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS

## Update Actions
1. Login as Tester with access to the libraries
1. Switch to library with Core actions
1. Import the latest Core actions
1. Switch to library with Mendix actions
1. Import the latest Mendix actions

## Update Mappings
1. Login as system administrator
1. Navigate to "System Administration" to the tab "Recorder"
1. Import latest recorder mappings

# 1.6 to 1.7
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS

<div class="alert alert-info">
The first startup will take a couple of minutes since a data transformation is taking place.
</div>

## Create a system administrator account
1. Login as MxAdmin
1. Navigate to Accounts
1. Create a new account with "System Administrator" permissions

## Update Actions
1. Login as Tester with access to the libraries
1. Switch to library with Core actions
1. Import the latest Core actions
1. Switch to library with Mendix actions
1. Import the latest Mendix actions

## Update Mappings
1. Login as system administrator
1. Navigate to the tab "Recorder"
1. Import latest recorder mappings

# 1.5 to 1.6
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS

<div class="alert alert-info">
The first startup will take a couple of minutes since a data transformation is taking place.
</div>

## Update Actions & Mappings
1. Login as Administrator
1. Import the latest Core actions
1. Import the latest Mendix actions
1. Import latest recorder mappings

<div class="alert alert-info">
1.6 has a new file format for exported repository data. Since the file format is not backwards compatible, you cannot import 1.6 files on previous versions of ATS. You can however always import data from previous ATS releases.
</div>

# 1.4 to 1.5
## Replace Components
1. In case of local Selenium: Replace other ATS components with latest versions (Selenium, IEDriver, Chromedriver)
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS

## Change User Accounts
All existing users will be administrators by default. We want to change this.

1. Login as an administrator and navigate to Accounts
1. Convert all personal user accounts to type 'User' by clicking the 'Convert to User' button in the edit dialog.
1. There should be at least one admin account left. Create one if there is none.

## Data Separation
On first start, ATS will create a single project and move all data into this project. We want to separate this data and put it into different projects and libraries.

### Create Libraries
We will create one library for core actions, one library for the old and one library for the new mendix actions.

1. Login as administrator and navigate to projects
1. Create a new action library 'Core' and add one user as project administrator
1. Create a new action library 'Mendix (old)' and add one user as project administrator
1. In the library 'Mendix (old)' include the action library 'Core' by setting the checkbox
1. Create a new action library 'Mendix (new)' and add one user as project administrator
1. In the library 'Mendix (new)' include the action library 'Core' by setting the checkbox
1. In the library 'Mendix (new)' set 'Include by default in new projects' to 'Yes'

### Create Projects
We will create one project for all existing test cases/suites and one project for new test cases/suites.

1. Login as administrator and navigate to projects
1. Create a new project '<appname> (old)' and add one user as project administrator
1. Include the library 'Mendix (old)' in this project
1. Create a new project '<appname> (new)' and add one user as a project administrator
1. Include the library 'Mendix (new)' in this project


### Move Data into Libraries
1. Login as administrator and navigate to repository
1. Open the folder 'Repository' which still contains all data
1. Open the folder 'MTF Core'
1. Select all items and move them into the 'Core' project
1. Navigate to repository and open the 'Repository' folder
1. Open the folder 'Mendix'
1. Select all items and move them into the 'Core' project

### Move Data into Project
1. Login as administrator and navigate to repository
1. Open the folder 'Repository'
1. Move your test cases/suites, custom actions, enumerations and folders into the project '<appname> (old)'

## Update Actions
1. Login as project administrator and open the 'Core' library
1. Import the latest Core actions
1. Login as project administrator and open the 'Mendix (new)' library
1. Import the latest Mendix actions
1. Login as administrator
1. Import latest recorder mappings

## Fix Project Settings
1. Login as project administrator of '<appname> (old)' and add the settings for the application
1. Login as administrator and set the checkbox 'All projects' for your Selenium hub

# 1.3 to 1.4
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS
1. Import the latest xml package files, either
	-  Import the combined package (ATS Core and Mendix) or
	-  Import first the ATS Core package and second the Mendix package
1. Replace other ATS components with latest versions (Selenium, IEDriver, Chromedriver)

# 1.2 to 1.3
It should be noted that this upgrade results in a loss of all previous test results. No other data is lost.

1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS
1. Import the latest xml package files, either
	-  Import the combined package (ATS Core and Mendix) or
	-  Import first the ATS Core package and second the Mendix package
1. Replace other ATS components with latest versions (Selenium,IEDriver, Chromedriver)

# 1.1 to 1.2
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS
1. Import the latest xml package files, either
	-  Import the combined package (ATS Core and Mendix) or
	-  Import first the ATS Core package and second the Mendix package
1. Replace other ATS components with latest versions (Selenium,IEDriver, Chromedriver)

# 1.0 to 1.1
1. Stop current ATS instance (Mendix server)
1. Create a database dump of your ATS database (as a backup)
1. Import the latest ATS deployment package
1. Start ATS
1. Import the latest xml package files, either
	-  Import the combined package (ATS Core and Mendix) or
	-  Import first the ATS Core package and second the Mendix package
1. Replace other ATS components with latest versions (Selenium,IEDriver, Chromedriver)
