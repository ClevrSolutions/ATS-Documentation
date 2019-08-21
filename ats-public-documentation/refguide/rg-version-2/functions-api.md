# Functions API

The Functions API is a REST API that allows ATS functions to be called from any testing tool or programing environemnt.
The function is executed against a selenium session that is specified in the request.

Lets illustrate this with a simple example of using the *Get Value* function.
To run this functions one needs to send a POST request to the ATS functions api endpoint `http://ats100.mendixcloud.com/function` with the following body:

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

**_remoteSeleniumDriver_** - is a reference to the remote selenium session that constists of a selenium driver url (which needs to be publicly accesible) and a session id.
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

##  Authentication

Uses the [Basic auth](https://tools.ietf.org/html/rfc7617) with the project id as username and an api key as password. 

## Schemas

* Request
* Response
