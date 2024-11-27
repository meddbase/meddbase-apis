---
layout: page
title: DateTime
nav_order: 27
parent: Objects and data types
---

# DateTime

DataTime format uses standard ISO 8601: `yyyy-MM-ddTHH:mm:ss.ffffff±HH:mm`.

If off-set is not specified the MedDBase servers use GMT in the winter time (UTC+00:00) and BST summer time (UTC+01:00)

## Examples

1. 8th January 2013 = `2013-01-08T00:00:00`
2. 1st February 2013, 13:2:25 = `2013-02-01T13:02:25`
3. 1st August 2013, 18:25:5.9525711 = `2013-08-01T18:25:05.9525711`
4. 1st August 2013, 18:25:5.9525711 = `2013-08-01T18:25:05.9525711+01:00`
    - Note: case 3 and 4 are the same because in summer time the default offset for the Meddbase servers is +01:00
