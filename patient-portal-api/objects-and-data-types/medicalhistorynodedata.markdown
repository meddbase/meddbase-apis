---
layout: page
title: MedicalHistoryNodeData
nav_order: 46
parent: Objects and data types
---

# MedicalHistoryNodeData

Provide information about one node of the Medical History tree.

## Properties

<table><tbody><tr><th><p>DataType</p></th><th><p>int</p></th><th><p>Type of data:</p><ul><li>0 = Text</li><li>1 = Group (can contain child nodes)</li><li>2 = HTML</li><li>3 = Document</li><li>4 = Graph</li></ul></th></tr><tr><td><p>Label</p></td><td><p>string</p></td><td><p>Labe of the current node.</p></td></tr><tr><td><p>Detail</p></td><td><p>string</p></td><td><p>Detail of the current node.</p></td></tr><tr><td><p>Path</p></td><td><p>string</p></td><td><p>Path of the current node. Can be null or empty if it is fully loaded (Loaded property is True) and it is not possible to request this node alone. It is usually for Separator, HTML, Title or Text data types.</p></td></tr><tr><td><p>Loaded</p></td><td><p>bool</p></td><td><p>True if Data and Children properties are fully loaded.</p><p>The server doesn’t always return a Children and Data properties fully loaded. It happens when the response would be excessively large or for performance reasons. The server doesn’t return it so the client has a faster response. If the patient wants to see it the client must request the specific node using GetMedicalHistoryTreeNode and pass the Path property as the NodePath.</p></td></tr><tr><td><p>Data</p></td><td><p>object</p></td><td><p>Contains data of the node. Specific for every DataType. See all examples below to find out how data looks.</p></td></tr><tr><td><p>Children</p></td><td><p>MedicalHistoryNodeData[]</p></td><td><p>Children of the current node.</p><p>Only Group data type item has children.</p></td></tr></tbody></table>

## JSON Example for Text data

```
{

"DataType": 0,

"Loaded": true,

"Data": "Date: 01/01/2013\\r\\nSubject: Medical Examination\\r\\nRef/nr: ABC-1231243\\r\\n\\r\\nName: Mister X\\r\\nAge: 30\\r\\n\\r\\nGender: Male"

}
```

## JSON Example for not fully loaded Group data

```
{

"DataType": 1,

"Label": "Full medical test",

"Details": "16/4/2013",

"Path": "/appointment/2756",

"Loaded": false

}
```

## JSON Example for fully loaded Group data

```
{

"DataType": 1,

"Label": "Full medical test",

"Details": "16/4/2013",

"Path": "/appointment/2756",

"Loaded": true,

"Children": \[

{

"DataType": 0,

"Loaded": true,

"Data": "Dear John, there is your blood test result."

},

{

"DataType": 3,

"Label": "Blood test result",

"Loaded": true,

"Data": {

"Size": "1256856", &lt; The file size in bytes. &gt;

"MIMEType": "image/jpeg",

"Url": "<https://images.meddbase.com/image.jpg>"

}

},

{

"DataType": 0,

"Loaded": true,

"Data": "And there is your BMI graph."

},

{

"DataType": 4,

"Label": "BMI Graph",

"Details": "",

"Path": "/appointment/2756/bmi-graph",

"Loaded": false

}

\]

}
```

## JSON Example for HTML data

```
{

"DataType": 2,

"Loaded": true,

"Data": "&lt;p&gt;Date: 01/01/2013&lt;br/&gt;Subject: Medical Examination&lt;br/&gt;Ref/nr: ABC-1231243&lt;br/&gt;&lt;br/&gt;Name: Mister X&lt;br/&gt;Age: 30&lt;br/&gt;Gender: Male&lt;/p&gt;&lt;hr/&gt;&lt;table&gt;&lt;tr&gt;&lt;td&gt;Table&lt;/td&gt;&lt;td&gt;Example&lt;/td&gt;&lt;/tr&gt;&lt;/table&gt;"

}
```

## JSON Example for Document data

```
{

"DataType": 3,

"Label": "Blood test result",

"Loaded": true,

"Data": {

"Size": "48123", &lt; The file size in bytes. &gt;

"MIMEType": "image/jpeg",

"Url": "<https://images.meddbase.com/image.jpg>"

}

}
```

Note: The client must provide ASP.NET_SessionId key in the cookie to receive the file.

## JSON Example for Document data

```
{

"DataType": 3,

"Label": "Pathology result",

"Loaded": true,

"Data": {

"Size": "1256856", &lt; The file size in bytes. &gt;

"MIMEType": "application/pdf",

"Url": "<https://docs.meddbase.com/pathology-result.pdf>"

}

}
```

Note: The client must provide ASP.NET_SessionId key in the cookie to receive the file.

## JSON Example for Graph data

```
{

"DataType": 4,

"Label": "BMI Graph",

"Details": "",

"Path": "/num-data/123",

"Loaded": true,

"Data": {

"XAxis": {

"Title": "Years",

"Data": \[2011, 2012, 2013\]

},

"Series": \[

{

"Title": "John",

"Data": \[25.4, 30.4, 27.6\],

"Color": "Red"

}

\]

}

}
```
