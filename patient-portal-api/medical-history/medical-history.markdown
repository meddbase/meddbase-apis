---
layout: page
title: Medical history
nav_order: 15
parent: Patient Portal API
---

# Medical history
This section provides methods for reading the patient’s medical history.The patient’s medical history is stored in the Medical History tree. This tree looks like://appointment/appointment/122/appointment/526/appointment/526/conclusion/numeric-data/numeric-data/weight/numeric-data/height/numeric-data/BMI/document/document/5865/document/5996Each node can consist from one or more another nodes. The tree is dynamically created by the server and it may change from time to time. The client shouldn't cache the tree for more than an hour at a time. The client should always request the root node and let patient browse through tree dynamically.The client can split history-item paths on the forward-slash character to aid parent-node navigation.Each method in this section needs the client to provide the ASP.NET_SessionId key in a cookie (see Login).