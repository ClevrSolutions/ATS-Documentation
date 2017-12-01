---
title: "Use the execute JavaScript action"
parent: "ht-version-2"
description: "Describes how to use the execute JavaScript actions in ATS."
tags: ["ATS", "testing"]
---

## 1 Introduction

There are many Mendix and core actions in ATS. But not everything you want to test in your application under test (AUT) might be possible with those actions. To make it possible to extend the testing possibilities of ATS the **Execute JavaScript** action is provided. 

Examples of what you can do with the **Execute JavaScript are:

* Create actions that can calculate
* Create actions to scroll on your page
* Create actions to log into your application if your application doesn't use the standard Mendix login page
* Create actions that interact with webelements on your page

This how-to described how to use the **Execute Javascript**.

**This how-to will teach you how to do the following**

* Use the execute JavaScript actions

## 2 Prerequisites

Before starting this how-to, make sure you have completed the following prerequisite:

* Read [How to Create a Test Case](create-a-test-case-2)
* Have basic JavaScript knowledge
* Have basic JQuery knowledge

## 3 Using the execute JavaScript actions

ATS provides three different Execute JavaScript actions:

* [Execute Javascript Integer](/refguide/rg-version-1/execute-javascript-integer)
* [Execute Javascript String](/refguide/rg-version-1/execute-javascript-string)
* [Execute Javascript WebElement](/refguide/rg-version-1/execute-javascript-webelement)

The difference between these actions is the item ATS returns:

| JavaScript action | Returns | Examples |
| :--- | :--- | :--- |
| **Execute JavaScript Integer**| Integer |  "2", "-50"|
| **Execute JavaScript String** | String | "ATS123", "Helloworld!"|
| **Execute JavaScript WebElement** | Web element | Checkbox, Dialog |

So if you want to return a String with your action, you should use the **Execute JavaScript String** action etc.

base on example of clicking in the middel of a button? 

How do do it in the debugger -> translate this to ats with arguments


