---
title: "CI/CD API"
space: "ATS Add-On"
category: "Reference Guide 2.0"
---
## CI/CD API
With the CI/CD API you can easily integrate ATS into your automated deployment workflow. You can run a test according to predefined templates or you can retrieve the status of already finished tests. To use the CI/CD API you will need a special webservice user, which will be used for authentication. For more informations on how to integrate ATS into your CI/CD workflow read the [How-To ATS CI/CD](/link-to-howto).

## CI/CD Templates
CI/CDTemplates are predefined configurations for a remote job run, which can be triggered via the run job webservice. Every CI/CD Template consists of the job configuration, an associated Testcase or Testsuite and a generated unique ID. This ID identifies the CI/CD template. An overview of all existing CI/CD Templates can be found on the **CI/CD Templates tab** on the Test Runs page. 

![](/refguide-ats-2/attachments/ci_cd/CICD_JobTemplateOverview.png)
 
| Name | Description |
|------|-------------| 
| Type Icon | Testcase, Testsuite |
| Name | Test Case Name, Test Suite Name or Custom Name|
| Browser | Firefox, Chrome |
| UID | The ID which identifies the CI/CD Template |

New CI/CD Templates can be added by clicking **Add Testcase** or **Add Testsuite**. A dialog will open, where the Testcase or Testsuite for the CI/CD Template can be selected. After that, the **Edit CI/CD Template** dialog will open.  

![](/refguide-ats-2/attachments/ci_cd/CICD_JobTemplateNewEdit.png)  

Following options can be configured on the **Edit CI/CD Template** dialog:

 | Name | Description |
|------|-------------| 
| Name | Default: Name of the Testcase/Testsuite. Can be customized |
| Environment | Environment which will be testet |
| Selenium Hub | The selenium hub, where the test will run|
| Browser | The browser, which will be used for the test. Chrome or Firefox|

For supported selenium hubs, like Browserstack, further options are available. More informations on supported selenium hub provider can be found [here](/refguide-ats-2/supported-selenium-hub-provider.md).


## API
The ATS CI/CD API is based on the SOAP webservice protocol. Currently there are two services available, **Run Job** and **Get Job Status**. The following sections shows the structures of the request and response messages of these services.  
### Run Job
#### URL
```
https://ats100.mendixcloud.com/ws/RunJob
```
#### Request
Following informations have to be included into the request.

| Name | Description |
| --- | --- |
| username | Username of the webservice user|
| password | Password of the webservice user |
| AppAPIToken | Key for the CI/CD API. Can be generated on the **Test Settings** page |
| AppID | The ID of your Mendix APP |
| JobTemplateID | The unique ID of the CI/CD Template |

##### Example
```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:men="http://www.mendix.com/">
  <soap:Header>
    <tns:authentication>
      <username>exampleUser</username>
      <password>examplePassword</password>
    </tns:authentication>
  </soap:Header>
  <soap:Body>
    <tns:RunJob>
      <TestRun>
        <AppAPIToken>exampleString</AppAPIToken>
        <AppID>exampleString</AppID>
        <JobTemplateID>exampleString</JobTemplateID>
      </TestRun>
    </tns:RunJob>
  </soap:Body>
</soapenv:Envelope>
```
#### Response
The following table shows the data contained in the response of the **Run Job** service:

| Name | Description |
| --- | --- |
| Started | True, if the test has already started. False otherwise.  |
| ErrorMessage | Contains the error message, if test failed to start. Is empty, if the test started succesfully. |
| JobID | The unique ID of the job. This ID can be used to retrieve the result of the test with the **Get Job Status** service |

##### Example
```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:men="http://www.mendix.com/">
  <soap:Body>
    <tns:RunJobResponse>
      <RunJob>
        <Started>false</Started>
        <ErrorMessage>exampleString</ErrorMessage>
        <JobID>exampleString</JobID>
      </RunJob>
    </tns:RunJobResponse>
  </soap:Body>
</soapenv:Envelope>
```
### Get Job Status
#### URL
```
https://ats100-test.mendixcloud.com/ws/GetJobStatus
```

#### Request
Following informations have to be included into the request.

| Name | Description |
| --- | --- |
| username | Username of the webservice user|
| password | Password of the webservice user |
| AppAPIToken | Key for the CI/CD API. Can be generated on the **Test Settings** page |
| JobID| The unique ID of the Job returned by the **Run Job** service |
| AppID | The ID of your Mendix APP |

##### Example
```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:men="http://www.mendix.com/">
  <soap:Header>
    <tns:authentication>
      <username>exampleUser</username>
      <password>examplePassword</password>
    </tns:authentication>
  </soap:Header>
  <soap:Body>
    <tns:GetTestRun>
      <TestRun>
        <AppAPIToken>exampleString</AppAPIToken>
        <JobID>exampleString</JobID>
        <AppID>exampleString</AppID>
      </TestRun>
    </tns:GetTestRun>
  </soap:Body>
</soapenv:Envelope>
```

#### Response
The following table shows the data contained in the response of the **Get Job Status** service:

| Name | Description |
| --- | --- |
| ExecutionStatus| Status of the Execution: **Running** or **Queued**|
| ExecutionResult| Contains the error message, if test failed to start. Is empty, if the test started succesfully. |
| JobID | The unique ID of the job. This ID can be used to retrieve the result of the test with the **Get Job Status** service |


```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:men="http://www.mendix.com/">
  <soap:Body>
    <tns:GetTestRunResponse>
      <TestRun>
        <ExecutionStatus>[key]</ExecutionStatus>
        <ExecutionResult>[key]</ExecutionResult>
        <ErrorMessage>exampleString</ErrorMessage>
      </TestRun>
    </tns:GetTestRunResponse>
  </soap:Body>
</soapenv:Envelope>
```