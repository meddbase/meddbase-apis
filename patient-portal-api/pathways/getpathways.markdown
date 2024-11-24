---
layout: page
title: GetPathways
nav_order: 2
parent: Pathways
---

# GetPathwaysReturns the list of pathways shared with the currently logged-in patient.## JavaScript library method```patientportal.pathways.getPathways ({pageSortColumn: &lt;page-sort-column&gt;,pageSortDescending: &lt;page-sort-descending&gt;,pageNumber: &lt;page-number&gt;,pageSize: &lt;page-size&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/pathways/pathways## URL Parameters<table><tbody><tr><th><p>page-sort-column</p></th><th><p>int (optional)</p></th><th><p>The column index to sort the result:</p><ul><li>0 – Last modified</li><li>1 – Pathway ID</li><li>3 – Due date</li><li>4 – Pathway name</li></ul><p>Default: 0</p></th></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>## Returned JSON```{"Items": \[&lt;list of PathwayOverviewData&gt;\]"TotalCount":24,"CurrentPage":1,"PageSize":10}```