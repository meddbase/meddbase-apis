---
layout: page
title: JavaScript API library
nav_order: 5
parent: Communication overview
---

# JavaScript API library
The client can use a JavaScript API library provided to the client. The JavaScript library wraps all methods described by this API for the client. The library also manages the token management for the client.

The JavaScript library is provided at: <https://api.meddbase.com/scripts/patientportalapi-1.1.js>

The JavaScript library uses the jQuery, so the client must include the jQuery script to the client’s html output. The jQuery version must be at least 1.8.

## CORS policy

The client must ask our support team to include their domain in our CORS policy. For testing purposes, we recommend you to setup \*.meddbase.com domain on your PC. You can use the hosts file to set up DNS for your local testing domain.

## Working with library

To use the JavaScript library the client must create a new instance of the PatientPortalAPI object:

```javascript
patientportal = new PatientPortalAPI();
```

All function calls follow this form:

```javascript
patientportal.SECTION.METHOD_NAME({
    param1: value1,
    paramN: valueN
})
.done(function (receivedData) {
    // do something
})
.fail(function (receivedError) {
    // do something
});
```

Where:

- `SECTION` – The name of the section in the API that the method belongs to (e.g. ‘auth’, ‘patient’, ‘finance’, ‘appointment’, ‘prescription’, ‘feed, ‘medicalHistory’). You can find the section name within the method description.
- `METHOD_NAME` – A name of the method as provided by this API in camel-case (e.g. ‘login’, ‘logout’, ‘getAllowedTitles’, etc.). You can find the method name within the method description.
- `paramN: valueN` – List of parameters. The list of parameters and their possible values are enumerated within the method description. Certain parameters are required while some are optional. Some methods don’t require any parameters.
- `done(function(receiveData){})` – A callback function that is executed if the request succeeds (ends with a HTTP status code 200).
  - `receivedData` – The data that the server returns. You can find the type of the data within the method description.
- `fail(function(receivedError))` – A callback function to be called if the request fails (ends with a HTTP status code other than 200).
  - `receivedError` – The [ServiceExceptionData](../objects-and-data-types/serviceexceptiondata) that the server throws.

## Example of using the JavaScript library

This example shows calling of the Login method and the UpdateDemographicData method.

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
<script src="https://api.meddbase.com/scripts/patientportalapi-1.1.js"></script>
<script type="text/javascript">
   // create a new instance of PatientPortalAPI object
   patientportal = new PatientPortalAPI();

   // set the client identification key
   patientportal.setClientKey('a2gft68m-5d8b');

   function Login() {
       // Calling the API method
       patientportal.auth.login({
           username: 'my name',
           password: 'my password',
       })
       .done(function (receivedData) {
           // callback function that is executed if the user is logged in successfully
           alert('User logged in. SessionID is ' + receivedData.SessionID);
       })
       .fail(function (receivedError) {
           // callback function that is called if the user is not logged in
           alert('User not logged in: ' + receivedError.Message);
       });
   }

   function UpdateDemographicData() {
       // Calling the API method
       patientportal.patient.updateDemographicData({
           password: 'my password',
           demog: {
               Name: 'James'
           }
       })
       .done(function (receivedData) {
           // callback function that is executed if patient's demographic data was updated
           alert('Data updated successfully.');
       })
       .fail(function (receivedError) {
           // callback function that is called if patient's demographic data wasn't updated
           alert('Update failed: ' + receivedError.Message);
       });
   }
</script>
<button onclick="Login();return false;">login</button>
<button onclick="UpdateDemographicData();return false;">update patient's data</button>
```
