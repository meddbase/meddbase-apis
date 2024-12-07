---
layout: page
title: Reading the Medical History tree
nav_order: 2
parent: Medical history
---

# Reading the Medical History tree

The client needs to call [GetMedicalHistoryTreeNode](../medical-history/getmedicalhistorytreenode) first time without parameters to get a root node. The root node may or may not contains all nodes of tree. It always contains top level nodes and may contains children of some nodes.

The server doesn’t always return all nodes fully loaded to ensure the response is not excessively large or for performance reasons. If the client needs to show any nodes that is not fully loaded the client needs to call [GetMedicalHistoryTreeNode](../medical-history/getmedicalhistorytreenode) with requested node path.

## Example

The first client request is:

URL: `/patientportalapi/medical-history/node`

JavaScript:
```javascript
patientportal.medicalHistory.getMedicalHistoryTreeNode();
```

The response (root node) looks like

```json
{
    "DataType": 1,
    "Label": "Medical History",
    "Path": "/",
    "Loaded": true,
    "Children": [
        {
            "DataType": 1,
            "Label": "Medical examinations",
            "Details": "",
            "Path": "/appointment",
            "Loaded": true,
            "Children": [
                {
                    "DataType": 1,
                    "Label": "Full medical test",
                    "Details": "25/05/2013",
                    "Path": "/appointment/2556",
                    "Loaded": false /* The server doesn’t return the whole node for performance reasons (e.g. Children, Data fields are not included). There will be a many child nodes (Preface – Letter, Body Composition, etc.). To get a full node the client must request this specific node using the path ‘/appointment/2556’. */
                },
                {
                    "DataType": 1,
                    "Label": "Blood test",
                    "Details": "16/04/2013",
                    "Path": "/appointment/5526",
                    "Loaded": true, /* The children contains only a few nodes so the server returns it straight away. */
                    "Children": [
                        {
                            "DataType": 2,
                            "Loaded": true,
                            "Data": "<p>Dear John, it was pleasure to see you...</p>"
                        },
                        {
                            "DataType": 3,
                            "Label": "Last blood test result",
                            "Loaded": true,
                            "Data": {
                                "Size": "1256856", /* The file size in bytes. */
                                "MIMEType": "image/jpeg",
                                "Url": "https://images.meddbase.com/image.jpg"
                            }
                        }
                    ]
                }
            ]
        },
        {
            "DataType": 1,
            "Label": "Documents",
            "Details": "",
            "Path": "/document",
            "Loaded": true,
            "Children": [
                {
                    "DataType": 2,
                    "Label": "Pathology result",
                    "Details": "Result from 04/07/2013. Requested by Dr. House",
                    "Path": "/document/12345",
                    "Loaded": false
                }
                /* There is a lot of big HTML documents. The server doesn’t return it because it would be excessively large. The client should show only a list of documents to the patient and requests a specific document using the node’s ‘Path’ when the patient chooses one. */
            ]
        },
        {
            "DataType": 1,
            "Label": "Numerical data",
            "Details": "",
            "Path": "/num-data",
            "Loaded": true,
            "Children": [
                {
                    "DataType": 4,
                    "Label": "BMI Graph",
                    "Details": "",
                    "Path": "/num-data/12",
                    "Loaded": false
                },
                {
                    "DataType": 4,
                    "Label": "Height",
                    "Details": "",
                    "Path": "/num-data/13",
                    "Loaded": false
                },
                {
                    "DataType": 4,
                    "Label": "Width",
                    "Details": "",
                    "Path": "/num-data/14",
                    "Loaded": false
                }
                /*There is a lots of numerical data. The server doesn’t return fully loaded nodes because it would be excessively large and for performance reasons. The client should show only a list and let the patient choose one. The client use the node’s ‘Path’ to get graph’s data. */
            ]
        }
    ]
}
```

Let’s imagine the patient wants to see BMI graph. She chooses ‘Numerical data’ and after that she chooses ‘BMI Graph’. The client doesn’t have appropriate node fully loaded (Loaded=False) so it requests this node using the path `/num-data/12`. The request URL looks like:

URL: `/patientportalapi/medical-history/node/num-data/12`

JavaScript:
```javascript
patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/num-data/12”});
```

The response from the server:
```json
{
    "DataType": 4,
    "Label": "BMI graph",
    "Details": "",
    "Path": "/num-data/12",
    "Loaded": true,
    "Data": {
        "XAxis": {
            "Title": "Years",
            "Data": [
                2011,
                2012,
                2013
            ]
        },
        "Series": [
            {
                "Title": "Sarah",
                "Data": [
                    25.4,
                    30.4,
                    27.6
                ]
            }
        ]
    }
}
```

If she wants to see full medical test the client use path `/appointment/2556`. The URL:

URL: `/patientportalapi/medical-history/tree/appointment/2556`

JavaScript:
```javascript
patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/appointment/2556”});
```

The response from the server:
```json
{
    "DataType": 1,
    "Label": "Full medical test",
    "Details": "25/05/2013",
    "Path": "/appointment/2556",
    "Loaded": true,
    "Children": [
        {
            "DataType": 1,
            "Label": "Preface - letter",
            "Details": "",
            "Path": "/appointment/2556/letter",
            "Loaded": false
        },
        {
            "DataType": 1,
            "Label": "Body Composition",
            "Details": "",
            "Path": "/appointment/2556/body",
            "Loaded": false
        },
        {
            "DataType": 1,
            "Label": "Cardiovascular Assessment",
            "Details": "",
            "Path": "/appointment/2556/ca",
            "Loaded": false
        },
        {
            "DataType": 1,
            "Label": "Diabetes Assessment",
            "Details": "",
            "Path": "/appointment/2556/letter",
            "Loaded": false
        }
    ]
}
```

If she wants to see the ‘Preface – letter’ the client use path `/appointment/2556/letter`. The URL:

URL: `/patientportalapi/medical-history/tree/appointment/2556/letter`

JavaScript:
```javascript
patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/appointment/2556/letter”});
```

The response from the server:
```json
{
    "DataType": 1,
    "Label": "Preface - letter",
    "Details": "",
    "Path": "/appointment/2556/letter",
    "Loaded": true,
    "Children": [
        {
            "DataType": 2,
            "Data": "<p>Date: 01/01/2013<br/>Subject: Medical Examination<br/>Ref/nr: ABC-1231243<br/><br/>Name: John<br/>Age: 30<br/>Gender: Male</p>"
        },
        {
            "DataType": 2,
            "Data": "<p>Dear John</p><p></p><p>It was a pleasure to see you for your medical examination on the 1st of January 2013 and as promised, I enclose a copy of your results...</p>"
        }
    ]
}
```
