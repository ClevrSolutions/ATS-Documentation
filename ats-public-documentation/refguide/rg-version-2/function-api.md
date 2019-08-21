# Function API

The Function API is a REST API that allows ATS functions to be called from any testing tool or programing environment.
The function is executed against a selenium session that is specified in the request.

Lets illustrate this with a simple example of using the *Get Value* function.
To run this functions one needs to send a POST request to the endpoint `http://ats100.mendixcloud.com/function` with the following body:

```json
{
    "remoteSeleniumDriver": {
        "url"      : "https://selenium.com/wd/hub",
        "sessionId": "00bef045-e9c9-4677-8cc1-e084bab7476b"
    },
    "functionToExecute": {
        "key": "GetValue",
        "values": [
            {
                "key"  : "WidgetName",
                "value": "widget1"
            }
        ]
    }
}
```
where

**_remoteSeleniumDriver_** - is a reference to a remote selenium session that consists of a selenium driver URL (which needs to be publicly accessible) and a session id.
ATS will use this session to execute the function specified under

**_functionToExecute_** - defines which ATS function to execute. The function and values are identified by their key (guaranteed to be unique) that can be found [here](functions_api_reference.md).
The order of the values is not relevant and optional parameter (default to null) unless a values is specified.

If the function execution was successful ATS will respond with

```json
{
   "result"     : "PASSED",
   "returnValue": "Lorem ipsum"
}
```

###  Authentication

Uses the [Basic auth](https://tools.ietf.org/html/rfc7617) with the project id as username and an API key as password. 

### Schemas

* [Request](../function-api-reference/functions_api_request.schema.json)
* [Response](../function-api-reference/functions_api_response.schema.json)

### Passing web elements

Web elements are passed by their internal Selenium ID which is in essence a string. To indicate that a parameter or a return value is a web element and not a string the flag `isWebElement` needs to be set to true.

## Clients

Clients are available for the function API for the following tools:

* java
* Katalon

The clients allow one to use the function API via a simplified interface without having to deal with parsing and formatting json and building http requests.

#### Java

Add `ats.jar` to the project's buildpath. Optionally, configure source and javadoc. Here is a simple example:

```java

ATSSettings atsSettings = new ATSSettings(projectId, apiKey);
ATSRunner ats = new ATSRunner(atsSettings , driver);

ats.Mendix.OpenMendixApplication("https://www.example.com");

ats.Widget_Set.SetValue("textBox1", "Lorem ipsum", null);

```

#### Katalon

Add `ats.jar` to the plugins folder. The ATS functions are available as custom keywords and in groovy. The authentication can be configured under ATS Settings.

```groovy
WebUI.openBrowser('')

// ATS functions called as custom keyword
CustomKeywords.'ats.Mendix.OpenMendixApplication'('https://www.example.com')
CustomKeywords.'ats.Widget_Set.SetValue'('textBox1', 'Lorem ipsum', null)

// ATS function called as groovy function
ats.Widget_Set.SetValue("textBox1", "Lorem ipsum", null);
```