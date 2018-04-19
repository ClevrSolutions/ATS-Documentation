---
title: "General"
parent: "rg-version-2"
---

## Introduction

Mobile testing in ATS is an experimental feature and only available to closed beta testers.

### Compatibility

| Aspect | Supported |
| ------ | --------- |
| Mobile Operating System | Android 6.0 "Mashmallow" |
| Selenium Provider | Sauce Labs (via TestObjects) |
| Test Browser | Chrome |
| Recorder | Chrome (via a custom mobile device profile) |
| ATS Helper | Chrome (via a custom mobile device profile) |
| Application type | Web applications with mobile view |

## Preparations

Some preparations are required before you can start to test on mobile devices.

### Creating a Mobile Device Profile

In order to enable a proper working of the recorder and ATS Helper we need to create a custom mobile device profile in Chrome.

Follow stese steps:

1. Open Chrome
2. Press **F12** to open the DevTools
3. Press **F1** to open the settings dialog
4. Select the **Devices** tab

    ![](/refguide-ats-2/attachments/mobile/chrome-settings-1.png)
6. Select **Add custom device**
7. Set the following properties
    * **Device name** to *ATS mobile*
    * **Width** to *540*
    * **Height** to *960*
    * **Device type** to *Mobile (no touch)*
8. Select **Add**

    ![](/refguide-ats-2/attachments/mobile/chrome-settings-2.png)
9. Close the settings and the DevTools by clicking the **x** button in the top right corner twice

### Creating a TestObjects Account

Running a test on a mobile device requires an account with TestObjects (part of Sauce Labs). They offer a free account for 1 concurrent test.
Follow these steps:

1. Go to [TestObjects website](https://app.testobject.com/#/signup/)
2. Sign up and confirm via the email you receive from TestObjects
3. Go to [TestObjects](https://app.testobject.com/#/) and login with your new account
4. Click **New App**
5. Click **Mobile Website**
6. Set random values for **Website URL**, **Website name** and **Version** and save
7. Save the device settings by clicking **Save**
8. Hover the button **AUTOMATED TESTING** and select **APPIUM**
9. Click on **Get Started**
10. Write down the API Key, you'll need it later

### Configuring TestObjects in ATS

You'll need to configure your TestObjects as a Selenium endpoint in ATS. To do so, follow these steps:

1. Open ATS and switch to one of your apps
2. Navigate to the Settings by selecting **Show Test Settings** in the profile menu
3. In the section **Selenium hubs** click **New**
4. Set **Name** to *TestObjects* and **URL** to *https://eu1.appium.testobject.com/wd/hub*
5. Under **Custom Capabilities** click **New**
6. Set **Key** to *testobject_api_key*, **Type** to *String* and **Value** to the API key that you've written down
7. Save the capability
8. Save the Selenium hub

## Creating Mobile Test Cases

After preparations are finished we can start to create our mobile tests.
Creating a mobile test is very straightforward. There are only a few differences that you should understand. They are described in the next sections.

### Activating the Mobile Device View

In order to see the mobile screens of your app in Chrome, you need to enable the mobile device view. In this mode you'll also be able to use the ATS Helper and Recorder.

Follow these steps:

1. Open Chrome
2. Press **F12** to open the DevTools
3. The the DevTools switch to the tab **Sources**
4. Press **CTRL+F8** to deactivate breakpoints (breakpoints would prevent proper use of the Recorder and ATS Helper)
5. Press **CTRL+SHIFT+M** to enable the mobile device toolbar
6. In the mobile device toolbar select the new device profile **ATS Mobile**

    ![](/refguide-ats-2/attachments/mobile/chrome-settings-3.png)

### Using the ATS Helper and Recorder

Enable and use the ATS Helper and Recorder as usual as long as the mobile device profile is enabled.

### Native Dialogs

Usually a web application is used on a mobile device, the devices adds native dialogs in some places to improve usability.
These places are:

1. In dropdowns
2. In date fields
3. In time fields
4. In date time fields

All standard actions should also work on a mobile device. Also in places where native dialogs are used. The actions simply work around these dialogs and set the values directly.
In order to make the testing more realistic you can even automate the native dialogs. In order to do this, make use of the following mobile specific actions:

| Scenario | Standard Action | Mobile Action |
| -------- | --------------- | --------------|
| Setting a time field | Set Value | Set TimePicker |
| Setting a date field | Set Value | Set DatePicker |
| Setting a date time field | Set Value | Set DateTime Picker |
| Setting a drop-down field | Set Value | Set DropDown Value |

### Recording

The recorder does not know the new mobile actions. It will always return a mapping to the non-mobile actions. You can later exchange recorded steps and use a new mobile action.

## Running a Test Case on a Mobile Device

Once you've created a test case for mobile you'll want to run it.
This is what you have to do:

1. Open your test case 
2. Click **Run** and then **Edit Run Configuration**.
3. Select *TestObjects* as **Selenium hub**
4. Enable the new checkbox **Mobile testing**
5. Click **Run**
![](/refguide-ats-2/attachments/mobile/run-configuration.png)

## Known Limitations

* Using touch ations in the mobile device profile is not possible. The ATS Helper and Recorder are not compatible with touch actions.
* Only devices with english language setting are supported
* It's not possible for the user to select the mobile device type. It defaults to Motorola Moto E (2nd gen).

| Type | Description |
| --- | --- |
| Device | Motorola Moto E (2nd gen) |
| Platform | Android |
| Version | 6.0 |
| API level | 23 |
| Resolution | 540x960 px / 4.5" |
| CPU | ARM quad-core 1200 MHz |
| RAM | 1024 MB |
| Browser | Google Chrome |