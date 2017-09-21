---
title: "Upload a file in your app using ATS"
category: "How-To's 1.8"
description: "Describes how to upload a file in your app using ATS and the restrictions it has."
tags: ["ATS", "testing"]
---

## 1 Introduction

This how-to explains how to upload a file in your app using ATS. You have some test situations in which you must upload a file to finish that test situation. During manual testing, you upload this file from your local computer into your app. ATS works similar, the only difference is that the local computer is your selenium hub.

This is regarding file uploads by ATS.

Quick summary:

| Selenium Set Up | Uploading your own file | Uploading a file | Uploading possible? |
| :-------------- | :---------------------- | :--------------- | :------------------ |
| Local Selenium  | ![](attachments/upload-file-using-ats-1/green.png) Yes | ![](attachments/upload-file-using-ats-1/green.png) Yes | ![](attachments/upload-file-using-ats-1/green.png) Yes |
| Local Selenium Server (Docker) | ![](attachments/upload-file-using-ats-1/grey.png) Limited<sup>1</sup> | ![](attachments/upload-file-using-ats-1/green.png) Yes | ![](attachments/upload-file-using-ats-1/green.png) Yes |
| BrowserStack | ![](attachments/upload-file-using-ats-1/red.png) No | ![](attachments/upload-file-using-ats-1/green.png) Yes | ![](attachments/upload-file-using-ats-1/green.png) Yes |
| SauceLabs | ![](attachments/upload-file-using-ats-1/red.png) No | ![](attachments/upload-file-using-ats-1/red.png) No | ![](attachments/upload-file-using-ats-1/red.png) No |

<sup>1</sup> This only possible when you prepare your own files on that server.

**This how-to will teach you how to do the following:**

* Understand why it is difficult to upload files in your app using automated testing.
* Uploading a file using ATS
* The approach for each selenium set-up.

## 2 Prerequisites

Before starting with this how-to, make sure you have the following prerequisites in place:

* Complete [How to Create a Test Case](create-a-test-case)
* Know your selenium set-up. (A provider like Browsertack, Local server etc.)

## 3 The process of uploading a file

### 3.1 Introduction

To upload a file in your app, ATS must have access to that file. Selenium simulates a user on a local computer. When ATS gives the command to upload a file, it provides a file path to the file you want to upload. Since there are three different selenium setups there are also three different situations.

1. You use selenium on your local computer. This means selenium has access to the files on your computer and can set the file path to a local file and find it.

2. You use selenium on a local server. This means selenium has no access to your local files. But you can add these files to the server or create a set of generic test files for that server.

3. You use Selenium SaaS. This means selenium has no access to your local files unless you use an agent. When you use the agent, situation 1 applies. If you do not use an agent the selenium SaaS creates a VM session for each test case you run. This means there are no constant values like on your local selenium server. Some Selenium SaaS providers upload a generic set of test files into each VM session that you can use in your test case. In the quick summary in the [Introduction](#1Introduction) chapter you see which selenium SaaS provides these files.

### 3.2 Uploading a file using ATS

ATS

## 4 Uploading a file using Local Selenium