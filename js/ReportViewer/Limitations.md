---
layout: post
title: Limitations | Report Viewer | JavaScript | Syncfusion
description: limitations
platform: js
control: Report Viewer
documentation: ug
---

# Limitations

## RDL Specification
The Report Viewer control does not support RDL Specification for SQL Server 2000 and SQL Server 2005.

## Report Layout
1.	Vertical alignment in the text box report item is not supported in web rendering.
2.	In the Tablix cell split layout process when the table cell width value exceeds the page width, the entire cell moves to the next page to display the complete cell items. 

## Expressions
The object function and VB function do not have complete support.

## SSRS
The SSRS Report Server does not provide options to get credential information of the report data source deployed on the server. If the report has any data source that uses credentials to connect with the database, then you must specify the data source credentials for each report data source to establish database connection.
