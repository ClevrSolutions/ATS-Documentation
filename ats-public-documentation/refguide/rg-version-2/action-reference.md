---
title: "Function Reference"
parent: "rg-version-2"
---

## 1 Introduction

The tables below list all the built-in functions of ATS. There is one table per category. 

## 2 Widget - Set

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Set BooleanSlider Value          | BooleanSlider                    | *Deprecated in favor of **Set Value**<br />*Checks if the given value is available for the BooleanSlider and sets the value. |
| Set BootstrapRTE Value           | BootstrapRTE                     | *Deprecated in favor of **Set Value**<br />*Sets the given value as current value for the BootstrapRTE value. Strings can be formatted via html-code. |
| Set Checkbox Set Selector Value  | Checkbox Set Selector            | Checks/clears the **Select all** check box. |
| Set Checkbox Set Selector Value (all) | Checkbox Set Selector       | Checks/clears the **Select all** check box. |
| Set Checkbox Value               | Checkbox                         | Sets the value of a check box. |
| Set CKEditor Value               | CKEditor                         | *Deprecated in favor of **Set Value**<br />*Sets the CKEditor content value. |
| Set File Manager                 | FileManager                      | Sets the file manager to the given file path to upload a file. |
| Set Grid Selector Checkbox Value | Grid Selector                    | Checks/clears the check box. |
| Set Grid Selector Radiobutton checked  | Grid Selector              | Selects the radio button for the given column and row caption. |
| Set InputReferenceSelector Value | InputReferenceSelector            | *Deprecated in favor of **Set Value**<br />*Sets the input reference selector to the given value. |
| Set Row Cell Value               | DataGrid                         | Set the cell value in a data grid row. |
| Set Simple Checkbox Set Selector Value | Simple Checkbox Set Selector | Checks/clears the check box found by a given entity attribute value. |
| Set Value | Standard widgets: <br />TextBox, TextArea, DropDown, RadioButton, DatePicker, ReferenceSelector, SearchInput Text, SearchInput DropDown <br /><br />App store widgets: OnChange Inputbox, BooleanSlider, Bootstrap Wysiwyg Editor (Bootstrap RTE), CK Editor For Mendix, Input Reference Selector, Radiobutton List | Sets the value of all supported widgets. <br /> |
| Set Value (by index) | Drop Down, Reference Selector, Search Input Drop Down | Set the value of all supported drop-down widgets by index |


## 3 Widget - Get

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Get Active Tab Caption  | TabContainer                       | Returns the caption of the active tab page. |
| Get BooleanSlider Value | BooleanSlider                      | *Deprecated in favor of **Get Value**<br />*Returns the current value of the BooleanSlider as a string. |
| Get BootstrapRTE Value | BootstrapRTE | *Deprecated in favor of **Get Value**<br />*Returns the current BootstrapRTE value as an HTML string. |
| Get Checkbox Set Selector Value | Checkbox Set Selector | Finds the check box by column caption and cell value and returns its value. |
| Get Checkbox Set Selector Value (all) | Checkbox Set Selector | Returns the **Select all** check box value. |
| Get Checkbox Value | Checkbox | Returns true if the check box is checked. |
| Get CKEditor Value | CKEditor | *Deprecated in favor of **Get Value**<br />*Returns the CKEditor value. |
| Get Dialog Message Text | ConfirmationDialog, DialogMessage | Get the text from message and confirmation dialogs. |
| Get Grid Selector Box Value | Grid Selector Box | Returns the current check box/radio button value. |
| Get Index | DropDown, ReferenceSelector, SearchInput DropDown | Gets the index of selected values in a drop-down menu (for example, an EnumSelect or ReferenceSelector). |
| Get InputReferenceSelector Value | InputReferenceSelector | *Deprecated in favor of **Get Value**<br />*Returns the current value of the InputReferenceSelector. |
| Get Item/Row Index | DataGrid, TemplateGrid, ListView | Gets the index of a row in a data grid or an item in a template grid or list view. |
| Get Row Cell Value | DataGrid | Gets the cell value of a data grid row. |
| Get Simple Checkbox Set Selector Value | Simple Checkbox Set Selector | Returns the current value of the check box found by the entity attribute value. |
| Get Total Item/Row Count | DataGrid, TemplateGrid, ListView | Gets the total grid count from the paging status. |
| Get Validation Message | All widgets | Returns the validation message of a widget. |
| Get Value | Standard widgets: <br />TextBox, TextArea, DropDown, RadioButtons, DatePicker, ReferenceSelector, SearchInput Text, SearchInput DropDown, Label <br /><br />App store widgets: OnChange Inputbox, BooleanSlider, BootstrapWysiwygEditor (Bootstrap RTE), CKEditor For Mendix, InputReferenceSelector, RadiobuttonList |Returns the current value of all supported widgets.|
| Get Visible Item/Row Count | DataGrid, TemplateGrid, ListView | Returns the number of currently visible items/rows in a template grid, data grid, or list view. |
| Groupbox is Collapsed | GroupBox | Gets the group box collapsed state: true if collapsed, otherwise false. |



## 4 Widget - Assert

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Assert Active Tab Caption | TabContainer | Assert a certain value for the caption of the active tab page |
| Assert BooleanSlider Value | BooleanSlider | *Deprecated in favor of **Assert Value**<br />*Asserts that the BooleanSlider is set to the given value |
| Assert BootstrapRTE Value | BootstrapRTE | *Deprecated in favor of **Assert Value**<br />*Asserts that the BootstrapRTE value is equal to the given value |
| Assert Checkbox Set Selector Value | Checkbox Set Selector | Finds the checkbox by entity attribute and asserts that the checkbox is set to the given value |
| Assert Checkbox Value | CheckBox | Assert the value of a Checkbox |
| Assert CKEditor Value | CKEditor | *Deprecated in favor of **Assert Value**<br />*Compares the CKEditor value with the given Value |
| Assert Grid Selector Value | Grid Selector | Asserts the value of checkbox/radiobutton |
| Assert InputReferenceSelector Value | InputReferenceSelector | *Deprecated in favor of **Assert Value**<br />*Asserts that the InputReferenceSelector has the given value |
| Assert Simple Checkbox Set Selector Value | Simple Checkbox Set Selector | Asserts that the checkbox found by given entity attribute value is checked/unchecked |
| Assert Validation Message | All widgets | Asserts a validation message with a certain text |
| Assert Value | Standard widgets: <br />Text Box, Text Area, Drop Down, Radio Buttons, Date Picker, Reference Selector, Search Input Text, Search Input Drop Down, Label <br /><br />App store widgets: OnChange Inputbox, Boolean Slider, Bootstrap Wysiwyg Editor (Bootstrap RTE), CK Editor For Mendix, Input Reference Selector, Radiobutton List | Assert the current value of all supported widgets |
| Dropdown has Option | DropDown, ReferenceSelector, SearchInput DropDown | Returns true if value is available in dropdown |

## 5 Widget - Find

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Find/Assert DataGrid Row | DataGrid | Find/Assert a DataGrid Row by certain column value(s) |
| Find/Assert Dialog | Window, DialogMessage, ConfirmationDialog | Find/Assert a Dialog by Title or Type |
| Find/Assert Menu Item | NavigationTree, MenuBar, SimpleMenuBar | Find/Assert a visible Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |
| Find/Assert Widget | All widgets | Find/Assert a Mendix Widget by its given Name. It is possible to use a sequence of names as a path (separated by space) |
| Find Checkbox Set Selector | Checkbox Set Selector | Finds a checkbox by given cell value and column caption. Returns first match |
| Find Checkbox Set Selector (all) | Checkbox Set Selector | Returns 'select all' checkbox |
| Find Grid Selector | Grid Selector | Find checkbox/radiobutton by column and row caption |
| Find Item/Row | DataGrid, TemplateGrid, ListView | Find a Row/Item in a DataGrid, TemplateGrid or ListView by Index |
| Find Item/Row (by child element) | DataGrid, TemplateGrid, ListView | Finds Item or Row of a TemplateGrid, DataGrid or ListView containing a  specified element |
| Find Selected Item/Row | DataGrid, TemplateGrid, ListView | Returns first selected Item/Row object |
| Find Simple Checkbox Set Selector | Simple Checkbox Set Selector | Finds the checkbox by given value |
| Find Widget Child Node | All widgets | Find a Node within a Mendix Widget. Also matches the widget node itself. The function is limited to search in only within widgets that are visible |

## 6 Widget - Other

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Cancel Dialog | ConfirmationDialog | Click Cancel on a Confirmation Dialog |
| Click DataGrid Row | DataGrid | Click a DataGrid Row by Column Value |
| Click Dropdown Div Converter dropdown button | Dropdown Div Converter | Clicks the dropdown div converter dropdown button |
| Click Dropdown Div Converter split button | Dropdown Div Converter | Clicks the dropdown div converter split button |
| Click Menu Item | NavigationTree, MenuBar, SimpleMenuBar | Click a Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |
| Click Widget | All widgets | Click on a Mendix Widget (e.g. Button, Link, Image) by its Name |
| Click Widget Button | ListView, ReferenceSelector | Refresh Button / Loadmore / ClearSearchField (ListView) Goto, / Add (ReferenceSelector) |
| Close Dialog | Window, DialogMessage, ConfirmationDialog | Click X Button on a Confirmation, Error, Warning or Info Dialog |
| Close GroupBox | GroupBox | Close a groupbox |
| Confirm Dialog | ConfirmationDialog, DialogMessage | Click Proceed/Ok Button on a Confirmation, Error, Warning or Info Dialog |
| Open GroupBox | GroupBox | Open a groupbox |
| Sort DataGrid | DataGrid | Sort DataGrid by given Column |
| Toggle BooleanSlider Value | BooleanSlider | Toggles the value of the Booleanslider |
| Toggle Checkbox Set Selector | Checkbox Set Selector | Finds checkbox by given entity attribute and inverses the value |
| Toggle Checkbox Set Selector (all) | Checkbox Set Selector | Inverse 'select all' checkbox |
| Toggle Checkbox Value | Checkbox | Click on a Checkbox to toggle its value |
| Toggle Grid Selector Checkbox Value | Grid Selector | Inverse the checkbox found by given column and  row caption |
| Toggle Simple Checkbox Set Selector Value | imple Checkbox Set Selector | Inverses the value of the checkbox found by given entity attribute value |
| Set ListView Search | ListView | Sets the ListView Search Text |

## 7 Mendix

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Assert Current Page | N/A | Asserts that a certain Page is open, by checking the current page title. Note that the page title may depend on the users language! For dialogs use the Find/Assert Dialog function. |
| Get Current Page Title | N/A | Returns the Current Page/Form Title |
| Login | Standard login page | Login to Mendix Application with standard login page or on Cloud using MxID |
| Logout | N/A | Trigger logout/logoff from application via client API. Use this keyword in teardown of your test cases to end the user session. This will work regardless of the UI state |
| Mendix wait | N/A | Inject Mendix Scripts and Wait |
| Open Mendix Application | N/A | Opens a Mendix application at [Website URL] in a browser with Mendix specific settings |

## 8 Web

| Function         | Description                              |
| ---------------- | ---------------------------------------- |
|Assert Element Attribute Equals|Asserts that an attribute of the given element equals the specified value|
| Assert Element matches Selector | Mx4/Mx5 - Returns whether given element matches the selector |
| Close Window | Closes currently active window. Does not switch to another window automatically |
| Close Window & Auto-Switch | Closes currently active window and automatically switches to the next one |
| Element matches Selector | Returns whether given element matches the selector |
| Execute Javascript Integer | Execute javascript snippet. Runs asynchronous when Timeout is set. Returns an Integer |
| Execute Javascript String | Execute javascript snippet. Runs asynchronous when Timeout is set. Returns a String |
| Execute Javascript WebElement | Execute javascript snippet. Runs asynchronous when Timeout is set. Returns a WebElement |
| Find Element | Find a web element. Optionally restrict search to the specified SearchContext element. Occurrence lets you specify which element to fetch from the result-list, starting at 1 for the first element (defaults to the first element) |
| Find Element by CSS | Find a web element by CSS. Optionally restrict search to the specified SearchContext element. Occurrence lets you specify which element to fetch from the result-list, starting at 1 for the first element (defaults to the first element) |
| Find Element by ID | Find a web element by ID. Optionally restrict search to the specified SearchContext element. Occurrence lets you specify which element to fetch from the result-list, starting at 1 for the first element (defaults to the first element) |
| Find Element by Sizzle | Find a web element by Sizzle. Optionally restrict search to the specified SearchContext element. Occurrence lets you specify which element to fetch from the result-list, starting at 1 for the first element (defaults to the first element) |
| Get Current Window Handle | Returns handle (i.e. identifier) of currently active window |
| Get Property Value | Returns property value from web element. (Does not have access to dojo widget properties) |
| Get Selected Option Index   ||
| Get Selected Option Text | |
| Get Selected Option Value | |
| Get Text | |
| Is Element Displayed | Returns true if supplied element is displayed (visible) |
| Is Selected | Check whether Checkbox is selected |
| Maximize | Maximize the current browser window |
| Open Application | *Deprecated in favor of **Open Mendix Application**<br />*Opens an application at [ApplicationURL] in a browser |
| Open Website | *Deprecated in favor of **Open Mendix Application**<br />* |
| Select Option | *Deprecated in favor of **Select Option by Index**, **Select Option by Text** and **Select Option by Value**<br />* |
| Select Option by Index | |
| Select Option by Text | |
| Select Option by Value | |
| Set Browser Dimensions | *Deprecated in favor of **Set Size**<br />* |
| Set Page Load Timeout | |
| Set Size | Set size of browser window |
| Switch to Default Frame | |
| Switch to Frame | |
| Switch to Next Window | Switch to the next open window. An error is thrown if there is only one window. Returns the window handle (i.e. identifier) of the new active window |
| Switch to Window | Switch to window via its identifier. An error is thrown if the window is not found |
| Unfocus WebElement | |
| Wait for Condition | |
| Wait for Condition JS | Wait until the given expression returns true |


## 9 Mouse & Keyboard

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Accept Browser Alert | N/A | Accepts the alert available |
| Clear WebElement | WebElement | Clear a webelement (input or textarea) |
| Click | WebElement | Clicks in the middle of the given element. |
| Click/Doubleclick | All web elements | Perform a Click or Doubleclick and wait for Mendix activities |
| Click Coordinates | N/A | Clicks on the given point on the page, described by X and Y Offset. If no reference element is given, the upper left corner of the page is used as point of origin for calculating the desired point. Otherwise the upper left corner of the reference element is used |
| Dismiss Browser Alert | N/A | Dismisses the alert available |
| Doubleclick | WebElement | Perform a Click or Doubleclick and wait for Mendix activities |
| Focus and Clear Element Value | WebElement | Set an input element to an empty string |
| Focus WebElement | WebElement | Focus WebElement and perform a Mendix wait afterwards |
| Focus WebElement | WebElement | |
| Hover | WebElement | Hover a web element |
| Send Enter | N/A                  | Simulates pressing Enter in [Element] |
| Send Keys | N/A                  | Simulates typing [Text] into the [Element] |


## 10 Logic

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Assert | N/A | *Deprecated<br />*Hamcrest assert |
| Assert 1 | N/A | *Deprecated in favor of **Assert equalTo**<br />*Asserts that the value is 1. ([null]=0) |
| Assert all not null | N/A | Fails if one of the objects is  null |
| Assert at least one not null | N/A | Fails if all objects are null |
| Assert Both not null | N/A | Fails if one or both objects are  null |
| Assert Condition Fails | N/A | This assert always fails. If an attached condition fails, it is simply not executed (and thus this keyword does not fail). (Use this keyword to assert that another keyword fails |
| Assert containsNoString | N/A | Asserts false that Subject contains string that is equal to Matcher Parameter (e.g. testcasetool contains case, it fails case) |
| Assert containsString | N/A | Asserts that Subject contains string that is equal to Matcher Parameter (e.g. testcasetool contains case) |
| Assert endsWith | N/A | Asserts that Subject ends with string that is equal to Matcher Parameter (e.g. testcase ends with case) |
| Assert Equals | N/A | *Deprecated in favor of **Assert equalTo**<br />*Assert that two values are equal |
| Assert equalTo | N/A | Asserts that Subject is equal to MatcherParameter (e.g. 100 is equal to 100 or house is equal to house) |
| Assert equalToIgnoringCase | N/A | Asserts that Subject is equal to Matcher Parameter while ignoring case (e.g. house is equal to House) |
| Assert equalToIgnoringWhiteSpace | N/A | Asserts that Subject is equal to Matcher Parameter while ignoring whitespaces (e.g. testcase is equal to ' testcase ') |
| Assert false | N/A | *Deprecated in favor of **Assert equalTo**<br />*Assert boolean value to be false |
| Assert greaterThan | N/A | Asserts that Subject is greater than Matcher Parameter (e.g. 1000 is greater than 100) |
| Assert greaterThanOrEqualTo | N/A | Asserts that Subject is either greater than or equal to Matcher Parameter (e.g. 1000 is greater than 100 or 1000 is equal to 1000) |
| Assert lessThan | N/A | Asserts that Subject is less than Matcher Parameter (e.g. 100 is less than 1000) |
| Assert lessThanOrEqualTo | N/A | Asserts that Subject is either less than or equal to Matcher Parameter (e.g. 100 is less than 1000, 1000 is equal to 1000) |
| Assert not equals | N/A | Asserts that two values are not equal |
| Assert not false | N/A | |
| Assert not true | N/A | Either false or [null] |
| Assert null | N/A | Fails if object is not null |
| Assert null (internal) | N/A | The internal Assert null functions that allows a boolean parameter to invert the result |
| Assert Property Value | N/A | *Deprecated in favor of **Assert element attribute equals**<br />*Get Property/Attribute from web Element and assert that it equals the given value |
| Assert startsWith | N/A | Asserts that Subject starts with string that is equal to Matcher Parameter (e.g. testcase starts with test) |
| Assert true | N/A | *Deprecated in favor of **Assert equalTo**<br />* |
| Assert XML equivalent | N/A | Assert that two XMLs are equivalent |
| Concatenate String | String | Concatenate strings |
| If Null Then 0 (Integer) | N/A | *Deprecated*<br />*Checks the input value and set it to 0, if it is null* |
| Is not Null | N/A | Returns true if object is not null, false otherwise |
| *Push ATS Scripts* | *N/A* | *Deprecated as it only served an internal purpose<br />*Push generic ats scripts to the client (jQuery, helpers functions) |
| RegExp Match | String | Return the n'th match of the given Regular Expression in the Search String (Uses JS string.match) |
| Return First Valid Boolean | Boolean | Returns the first boolean from the parameter list which is not null |
| Return First Valid Integer | Integer | Returns the first integer from the parameter list which is not null |
| Return First Valid String | String | Returns the first string from the parameter list which is not null |
| Return First Valid WebElement | WebElement | Returns the first webelement from the parameter list which is not null |
| Set Implicit Wait | N/A | *Deprecated as it only served an internal purpose* |
| Set Return Value | N/A | |
| Sleep | N/A | Wait 'Sleep time' milliseconds |


## 11 Generators

| Function         | Supported Widgets | Description                              |
| ---------------- | ----------------- | ---------------------------------------- |
| Generate GUID | N/A | Generates and returns a GUI |
| Get Current DateTime String | N/A | Returns the current date and time in supplied format (java date format) e.g. 'yyyy-MM-dd HH:mm:ss' |
| Random Number | N/A | Creates a random Integer using: 'Math.floor(Math.random() * (max - min)) + min', You need to define the min(included) and max (excluded) |
| Random String | N/A | Creates a random alphanumeric String using: 'Math.random().toString(36).slice(2,8)' - Optionally allows to add a Prefix or Postfix |
