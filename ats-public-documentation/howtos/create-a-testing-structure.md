### How to create a testing structure

All objects tab

The first tab inside the repository has been explained. In that tab you could make a test case or a test suite. The next tab is the All objects tab. This tab includes all options to create a testing structure. Here you can move test cases, test suites or actions to folders so that dependencies and testing scenarios are easily combined.

Click **Add item** to display the dialog box _Create new_. The menu shows the following options: _Folder, Action_ and _Enumeration_. If you check the checkbox at the end of the row, two more options appear: _Duplicate items_ and _Move to folder_. The default setting is  _Folder_.

**Create a Folder**

_**Folders**_ can be used to structure your testing. Here you can create folders, move items to a folder or create a folder within a folder. You can structure, _**Folder structure, **\_your testing efforts in multiple ways i.e. by functionality or type of test. We advice you to make a clear structure for your test cases and test suites. When the items grow in number you need a system to keep everything separated. If you check the checkbox of an item, the option_ \_**Duplicate items **appears. The duplicate option creates a new item with a new identifier but containing the same values. ATS uses identifiers when importing or exporting items. Duplicating is a way to make sure that ATS recognizes it as a new item. ???

**Create an action**

The actions you create here are called custom actions. Unlike the standard actions, created custom actions are located in the repository under the **All objects **tab and can also be structured in folders. In most cases your custom actions are saved with the test case that uses it or when you have created a more generic custom action you can create a folder just for these type of actions.

A custom action can be separated in two topics:

| Combining standard actions for easy use | to use when you want to combine multiple steps into one action |
| :--- | :--- |
| Creating an action because the standard set does not work | to build your own custom action i.e. for a custom widget. For more information on how to build your own custom action, go to..... |

_**Combining standard actions for easy use**_

You can create the action from scratch here, but in practice you will want to combine steps that are already in your test case. In that case you may want to go inside your test case and use **Extract Action **to combine steps.

1. Multi-select the steps you want to combine in one action and click **Extract Action**. 
2. The dialog _Action-Set details_ appears.
3. Enter the name, description and input parameters for your action.
4. Click close to close the dialog box.
5. Select your action and click open. The screen functions the same as that of a test case.
6. Go to the tab **Settings** to define and set unique elements to your action. 
7. Set the input and output parameters. More information can be found....

**Enumeration**

The enumeration is used as an input parameter. It allows you to set a caption and connect a value to that caption. More information can be found here.....



