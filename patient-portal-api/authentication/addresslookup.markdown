---
layout: page
title: \[DEPRECATED\] AddressLookup
nav_order: 22
parent: Authentication
---

# \[DEPRECATED\] AddressLookupThis method has been deprecated, please use the [Address Finder](#_Address_Finder) section instead. Returns a number of possible address for the postcode.## JavaScript library method```patientportal.auth.addressLookup({postcode: &lt;postcode&gt;, house: &lt;house&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/address-lookup## URL Parameters| postcode | string | Case-insensitive postcode without space (e.g. N70NH or n70nh). || --- | --- | --- || house | string (optional) | House name or house number. |## ReturnsAddressData\[\]