---
layout: page
title: Reading the Medical History tree
nav_order: 2
parent: Medical history
---

# Reading the Medical History tree

The client needs to call GetMedicalHistoryTreeNode first time without parameters to get a root node. The root node may or may not contains all nodes of tree. It always contains top level nodes and may contains children of some nodes.

The server doesn’t always return all nodes fully loaded to ensure the response is not excessively large or for performance reasons. If the client needs to show any nodes that is not fully loaded the client needs to call GetMedicalHistoryTreeNode with requested node path.

## Example

The first client request is:

URL: /patientportalapi/medical-history/node

JavaScript: ```patientportal.medicalHistory.getMedicalHistoryTreeNode();```

The response (root node) looks like

```
{

"DataType": 1,

"Label": "Medical History",

"Path": "/",

"Loaded": true,

"Children": \[

{

"DataType": 1,

"Label": "Medical examinations",

"Details": "",

"Path": "/appointment",

"Loaded": true,

"Children": \[

{

"DataType": 1,

"Label": "Full medical test",

"Details": "25/05/2013",

"Path": "/appointment/2556",

"Loaded": false &lt; The server doesn’t return the whole node for performance reasons (e.g. Children, Data fields are not included). There will be a many child nodes (Preface – Letter, Body Composition, etc.). To get a full node the client must request this specific node using the path ‘/appointment/2556’. &gt;

},

{

"DataType": 1,

"Label": "Blood test",

"Details": "16/04/2013",

"Path": "/appointment/5526",

"Loaded": true, &lt; The children contains only a few nodes so the server returns it straight away. &gt;

"Children": \[

{

"DataType": 2,

"Loaded": true,

"Data": "&lt;p&gt;Dear John, it was pleasure to see you...&lt;/p&gt;"

},

{

"DataType": 3,

"Label": "Last blood test result",

"Loaded": true,

"Data": {

"Size": "1256856", &lt; The file size in bytes. &gt;

"MIMEType": "image/jpeg",

"Url": "<https://images.meddbase.com/image.jpg>"

}

}

\]

}

\]

},

{

"DataType": 1,

"Label": "Documents",

"Details": "",

"Path": "/document",

"Loaded": true,

"Children": \[

{

"DataType": 2,

"Label": "Pathology result",

"Details": "Result from 04/07/2013. Requested by Dr. House",

"Path": "/document/12345",

"Loaded": false

}

_...&lt; There is a lot of big HTML documents. The server doesn’t return it because it would be excessively large. The client should show only a list of documents to the patient and requests a specific document using the node’s ‘Path’ when the patient chooses one. &gt;..._

\]

},

{

"DataType": 1,

"Label": "Numerical data",

"Details": "",

"Path": "/num-data",

"Loaded": true,

"Children": \[

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

_...&lt; There is a lots of numerical data. The server doesn’t return fully loaded nodes because it would be excessively large and for performance reasons. The client should show only a list and let the patient choose one. The client use the node’s ‘Path’ to get graph’s data. &gt;..._

\]

}

\]

}
```

Let’s imagine the patient wants to see BMI graph. She chooses ‘Numerical data’ and after that she chooses ‘BMI Graph’. The client doesn’t have appropriate node fully loaded (Loaded=False) so it requests this node using the path ‘/num-data/12’. The request URL looks like:

Url: /patientportalapi/medical-history/node/num-data/12

JavaScript: ```patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/num-data/12”});```

The response from the server:

```
{

"DataType": 4,

"Label": "BMI graph",

"Details": "",

"Path": "/num-data/12",

"Loaded": true,

"Data": {

"XAxis": {

"Title": "Years",

"Data": \[2011, 2012, 2013\]

},

"Series": \[

{

"Title": "Sarah",

"Data": \[25.4, 30.4, 27.6\]

}

\]

}

}
```

If she wants to see full medical test the client use path ‘/appointment/2556’. The URL:

Url: /patientportalapi/medical-history/tree/appointment/2556

JavaScript: ```patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/appointment/2556”});```

The response from the server:

```
{

"DataType": 1,

"Label": "Full medical test",

"Details": "25/05/2013",

"Path": "/appointment/2556",

"Loaded": true,

"Children": \[

{

"DataType": 1,

"Label": "Preface - letter",

"Details": "",

"Path": "/appointment/2556/letter",

"Loaded": false,

},

{

"DataType": 1,

"Label": "Body Composition",

"Details": "",

"Path": "/appointment/2556/body",

"Loaded": false,

},

{

"DataType": 1,

"Label": "Cardiovascular Assessment",

"Details": "",

"Path": "/appointment/2556/ca",

"Loaded": false,

},

{

"DataType": 1,

"Label": "Diabetes Assessment",

"Details": "",

"Path": "/appointment/2556/letter",

"Loaded": false,

}

\]

}
```

If she wants to see the ‘Preface – letter’ the client use path ‘/appointment/2556/letter’. The URL:

Url: /patientportalapi/medical-history/tree/appointment/2556/letter

JavaScript: ```patientportal.medicalHistory.getMedicalHistoryTreeNode({nodePath: “/appointment/2556/letter”});```

The response from the server:

```
{

"DataType": 1,

"Label": "Preface - letter",

"Details": "",

"Path": "/appointment/2556/letter",

"Loaded": true,

"Children": \[

{

"DataType": 2,

"Data": "&lt;p&gt;Date: 01/01/2013&lt;br/&gt;Subject: Medical Examination&lt;br/&gt;Ref/nr: ABC-1231243&lt;br/&gt;&lt;br/&gt;Name: John&lt;br/&gt;Age: 30&lt;br/&gt;Gender: Male&lt;/p&gt;

},

{

"DataType": 2,

"Data": "&lt;p&gt;Dear John&lt;/p&gt;&lt;p&gt;&lt;/p&gt;&lt;p&gt;It was a pleasure to see you for your medical examination on the 1st of January 2013 and as promised, I enclose a copy of your results...&lt;/p&gt;

}

\]

}
```
