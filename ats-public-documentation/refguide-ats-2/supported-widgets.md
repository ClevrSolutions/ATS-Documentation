---
title: Supported Widgets
space: ATS Add-On
category: Reference Guide 2.0
---

## Supported Widgets


DataGrid

| Action                           | Description                              |
| -------------------------------- | ------------------------------------------------------------------------ |
| Click DataGrid Row               | Click a DataGrid Row by Column Value     |
| Find/Assert DataGrid Row         | Find/Assert a DataGrid Row by a certain Column Value |
| Find Item/Row                    | Find a Row/Item in a DataGrid, TemplateGrid or ListView by Index |
| Find Item/Row (by child element) | Finds Item or Row of a TemplateGrid, DataGrid or ListView containing a specified element |
| Find Selected Item/Row           | Returns first selected Item/Row object   |
| Get Item/Row Index               | Gets the Index of a row in a Datagrid, or an item in a TemplateGrid or ListView |
| Get Row Cell Value               | Gets the Cell Value of a DataGrid row    |
| Get Total Item/Row Count         | Gets the total grid count from the paging status |
| Get Visible Item/Row Count       | Returns number of currently visible Items/Rows in a TemplateGrid, DataGrid or ListView |
| Set Row Cell Value               | Sets the Cell Value in a DataGrid row    |
| Sort DataGrid                    | Sorts DataGrid by given Column           |

TemplateGrid
| Find Item/Row                    | Find a Row/Item in a DataGrid, TemplateGrid or ListView by Index |
| Find Item/Row (by child element) | Finds Item or Row of a TemplateGrid, DataGrid or ListView containing a specified element |
| Find Selected Item/Row           | Returns first selected Item/Row object   |
| Get Item/Row Index               | Gets the Index of a row in a Datagrid, or an item in a TemplateGrid or ListView |
| Get Total Item/Row Count         | Gets the total grid count from the paging status |
| Get Visible Item/Row Count       | Returns number of currently visible Items/Rows in a TemplateGrid, DataGrid or ListView |

ListView
| Find Item/Row                    | Find a Row/Item in a DataGrid, TemplateGrid or ListView by Index |
| Find Item/Row (by child element) | Finds Item or Row of a TemplateGrid, DataGrid or ListView containing a specified element |
| Find Selected Item/Row           | Returns first selected Item/Row object   |
| Get Item/Row Index               | Gets the Index of a row in a Datagrid, or an item in a TemplateGrid or ListView |
| Get Total Item/Row Count         | Gets the total grid count from the paging status |
| Get Visible Item/Row Count       | Returns number of currently visible Items/Rows in a TemplateGrid, DataGrid or ListView |
| Set ListView Search              | Sets the ListView Search Text            |
| Click Widget Button       	   | Refresh Button / Loadmore / ClearSearchField (ListView) Goto, / Add (ReferenceSelector) |

File Manager
| Set File Manager | Set a file manager to the given file path to upload a file |

GroupBox
| Close GroupBox        | Close a groupbox                         |
| GroupBox is Collapsed | Get GroupBox Collapsed state: true if collapsed, otherwise false |
| Open GroupBox         | Open a groupbox                          |

ConfirmationDialog
| Cancel Dialog           | Click Cancel on a Confirmation Dialog    |
| Close Dialog            | Click X Button on a Confirmation, Error, Warning or Info Dialog |
| Confirm Dialog          | Click Proceed/Ok Button on a Confirmation, Error, Warning or Info Dialog |
| Find/Assert Dialog      | Find/Assert a Dialog by Title or Type    |
| Get Dialog Message Text | Get the text from message and confirmation dialogs |

Window
| Close Dialog            | Click X Button on a Confirmation, Error, Warning or Info Dialog |
| Find/Assert Dialog      | Find/Assert a Dialog by Title or Type    |

A _Window_ is rendered when a page is opened as a popup.

DialogMessage
| Close Dialog            | Click X Button on a Confirmation, Error, Warning or Info Dialog |
| Confirm Dialog          | Click Proceed/Ok Button on a Confirmation, Error, Warning or Info Dialog |
| Find/Assert Dialog      | Find/Assert a Dialog by Title or Type    |
| Get Dialog Message Text | Get the text from message and confirmation dialogs |

Show message actions in microflows result in _DialogMessage_ widgets.

ReferenceSelector
| Click Widget Button   | Refresh Button / Loadmore / ClearSearchField (ListView) Goto, / Add (ReferenceSelector) |
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Dropdown has Option   | Returns true if value is available in dropdown |
| Get Index             | Get index of selected value in a dropdown, e.g. an EnumSelect or ReferenceSelector |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |
| Set Value (by index)  | Set the value of a dropdown by index, e.g. EnumSelect or ReferenceSelector |

CheckBox
| Assert Checkbox Value | Assert the value of a Checkbox           |
| Get Checkbox Value    | Returns true if the Checkbox is checked  |
| Set Checkbox Value    | Sets the value of a Checkbox             |
| Toggle Checkbox Value | Click on a Checkbox to toggle its value  |

TextBox
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

TextArea
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

DatePicker
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

DropDown
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Dropdown has Option   | Returns true if value is available in dropdown |
| Get Index             | Get index of selected value in a dropdown, e.g. an EnumSelect or ReferenceSelector |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |
| Set Value (by index)  | Set the value of a dropdown by index, e.g. EnumSelect or ReferenceSelector |

RadioButton
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

SearchInput Text
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

SearchInput DropDown
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Dropdown has Option   | Returns true if value is available in dropdown |
| Get Index             | Get index of selected value in a dropdown, e.g. an EnumSelect or ReferenceSelector |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |
| Set Value (by index)  | Set the value of a dropdown by index, e.g. EnumSelect or ReferenceSelector |

Label
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |

OnChange Inputbox
| Assert Value          | Assert the text value from a Textbox, Textarea, Dateinput |
| Get Value             | Get the text value from a Textbox, Textarea, Dateinput, RadioButton, Dropdowns |
| Set Value             | Set the text value of a Textbox, Textarea, Dateinput, Reference Selector, Enum Selector |

NavigationTree
| Click Menu Item       | Click on a Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |
| Find/Assert Menu Item | Find/Assert a visible Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |

MenuBar
| Click Menu Item       |  Click on a Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |
| Find/Assert Menu Item | Find/Assert a visible Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |

SimpleMenuBar
| Click Menu Item       | Click on a Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |
| Find/Assert Menu Item | Find/Assert a visible Menu Item in a Navigation Tree, Menu Bar and Simple Menu Bar |

TabContainer
| Assert Active Tab Caption | Assert a certain value for the caption of the active tab page |
| Get Active Tab Caption    | Returns the caption of the active tab page |

Boolean Slider
| Assert BooleanSlider Value | Asserts the value of the BooleanSlider Appstore Widget (String) |
| Get BooleanSlider Value 	 | Returns the current active text value from the BooleanSlider Appstore Widget |
| Set BooleanSlider Value 	 | Sets the given text as active value for the BooleanSlider appstore widget |
| Toggle BooleanSlider Value | Clicks the BooleanSlider widget to toggle its value. This will invert the current value of the BooleanSlider |

BootstrapRTE
| Assert BootstrapRTE Value  | Asserts that the BootstrapRTE value is equal to the given value |
| Get BootstrapRTE Value 	 | Returns the current BootstrapRTE value as an HTML string |
| Set BootstrapRTE Value 	 | Sets the given value as current value for the BootstrapRTE value. Strings can be formatted via HTML code |

Checkbox Set Selector
| Assert Checkbox Set Selector Value | Finds the check box by the column caption and its cell value and asserts that the check box is set to the given value |
| Find Checkbox Set Selector | Finds the select all check box |
| Find Checkbox Set Selector (All) | Finds a check box by given cell value and column caption. Returns the first match |
| Get Checkbox Set Selector Value | Finds the check box via the column caption and cell value. Returns its value |
| Get Checkbox Set Selector Value (All) | Returns the "select all" check box value |
| Set Checkbox Set Selector Value | Finds check box by column caption and cell value. Sets its value to checked |
| Set Checkbox Set Selector Value (All) | Clear/check the "select all" check box |
| Toggle Checkbox Set Selector Value | Finds the check box via the column caption and cell value. Inverts the value |
| Toggle Checkbox Set Selector Value (All) | Finds check box by given entity attribute and inverts the value |

CK Editor
| Assert CKEditor Value | Compares the CKEditor value with the given value |
| Get CKEditor Value | Returns the CKEditor value as HTML code |
| Set CKEditor Value | Sets the given value as current value for the CKEditor value. The value can be formatted via HTML code |

Dropdown Div Converter
| Click Drop-Down div Converter Drop-Down Button | Clicks the dropdown button of the drop-down div converter to expand the drop-down menu |
| Click Drop-Down div Converter Split Button | Clicks the split button of the drop-down div converter |

Grid Selector
| Assert Grid Selector Value | Asserts the value of the check box and the radio button inside the Grid Selector Widget |
| Find Grid Selector Box | Find check box and radio button by column and row caption |
| Get Grid Selector Box Value | Returns the current check box and radio button value |
| Set Checkbox Set Selector Value | Finds the check box by column and row caption. Sets its value to the given checked parameter |
| Set Grid Selector RadioButton Value | Finds the radio button by column and row caption. Sets it to be checked |
| Toggle Grid Selector Checkbox Value | Inverses the check box found by the given column and row caption |

Input Reference Selector
| Assert InputReferenceSelector Value | Asserts that the InputReferenceSelector has the given value |
| Get InputReferenceSelector Value | Returns the current value of the InputReferenceSelector |
| Set InputReferenceSelector Value | Set the InputReferenceSelector to the given value |

Simple Checkbox Set Selector
| Assert Simple Checkbox Set Selector Value | Asserts that the check box found by the given value is checked or cleared |
| Find Simple Checkbox Set Selector | Finds the check box by the given value |
| Get Simple Checkbox Set Selector Value | Returns the current value of the found check box |
| Set Simple Checkbox Set Selector Value | Checks or clears the check box found by the given value connected to the check box |
| Toggle Simple Checkbox Set Selector Value | Inverts the value of the check box found by the given value connected to the check box |
