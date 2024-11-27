---
layout: page
title: Response data format
nav_order: 3
parent: Communication overview
---

# Response data format
All response data is formatted in the JSON data format. The server response is an envelope that always looks like this example:

```javascript
{
    'status': 'ok|error'
    'result': {
        // result object according to the method called
    },
    'error': {
        // a ServiceExceptionData object
    }
}
```

The response envelope includes:

- status – `ok` for successful response or `error` when an exception throws.
- result – returns object from the server within successful response.
- error – a [ServiceExceptionData](../objects-and-data-types/serviceexceptiondata) object that provides information about an exception that was thrown.

{: .note }
> The JavaScript API library wraps the response envelope into 'done' and 'fail' methods with an appropriate result/error object. Any client that uses the JavaScript API library need not consider this envelope.
