---
layout: page
title: DateTime
nav_order: 27
parent: Objects and data types
---

# DateTime

DataTime format uses standard ISO 8601: "yyyy-MM-ddTHH:mm:ss.ffffff±HH:mm".

If off-set is not specify the Meddbase servers uses London’s offset what is 00:00 in winter time, +01:00 in summer time.

## Examples

1. 8\. January 2013 = "2013-01-08T00:00:00"
2. 1\. February 2013, 13:2:25 = "2013-02-01T13:02:25"
3. 1\. August 2013, 18:25:5.9525711 = "2013-08-01T18:25:05.9525711"
4. 1\. August 2013, 18:25:5.9525711 = "2013-08-01T18:25:05.9525711+01:00"
    - Note: case c) and d) are same because in summer time the default offset for the Meddbase servers is +01:00
