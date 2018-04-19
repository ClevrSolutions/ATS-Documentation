---
title: "Creating maintainable test cases"
parent: "bp-version-2"
---

## 1 Introduction

Each sprint new functionality is added to an application. This functionality can be tested with new test cases, after which it can be tested with running the regression test suite. However, each sprint also other changes, like bug fixes, are made. This and the new functionality can break other test cases. So, each test case you have created likely needs maintenance time somewhere during the application life cycle. 

Another example is when the password of a user changes. In case you have 50 test cases that all login as that user, each with the login action, than you need to change the password in 50 test cases. As this is time consuming you would like to have maintaianble test cases, so that you only have to change the password, or something else, in one location and not in different test cases.

This document described how you can create maintanable test cases in ATS. 

**The different categories to create a maintainable test case:**
* Create reusable actions
* Reduce test case dependencies
* Create a logical sctructure in the repository
* Create a clear naming structure
* Create for each test situation a separate test case
* Make use of descriptions
* Using Environment URL


## 2 Create reusable actions

Refer to create extracted actions docs

## 3. Reduce test case dependencies

To make your test cases more maintainable it is advised to reduce test case dependencies as much as possible. For more information read: [test case dependencies](../../bestpractices/bp-version-2/test-case-dependencies-2).

## 4   Make use of descriptions

In each test case, test suite, action, input parameter and test step ATS has a **Description** field. We advice to make use of these field and give a clear description. For example in a test case you can enter what is validated in the test case. For a test suite you can enter when the test suite is scheduled and what type of test cases are added in the test suite. Making use of the description helps everybody that is working in the same ATS project to understand the different items. 

## 5. Using Environment URL
