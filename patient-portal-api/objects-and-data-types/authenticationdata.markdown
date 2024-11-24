---
layout: page
title: AuthenticationData
nav_order: 13
parent: Objects and data types
---

# AuthenticationDataContains the information about current authenticated security context.## Properties| SessionID | string | Identifies the existing security context. || --- | --- | --- || Config | ConfigData | Defines that the patient should be forced to set up their contact options. || Token | string | The current token. See Authentication Token. || Require2FA | Boolean | True if the profile requires 2FA (see Send2faCode). False if the profile does not require 2FA. |## JSON Example```{"SessionID": "4oytawakgy0njpaajyliq3md","Config": "&lt;see ConfigData&gt;","Token": "7a413802-f186-42c6-ae92-646531749624","Require2FA": "true"}```