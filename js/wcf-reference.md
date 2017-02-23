---
layout: post
title: wcf reference for ejService related controls
description: wcf reference for ejService related controls
documentation: ug
platform: js
---

# WCF reference for ej Controls

The details of WCF Service reference has been shown in the below table.

### Northwind Data Service

|  WCF | Description  |
|---|---|
|[Northwind Data Service for Grid](WCF/Northwind#grid)|It is used to retrieve the records from “Orders” and "Customers" table in Remote Data Service.|
|[Northwind Data Service for Kanban](WCF/northwind#kanban)|It is used to retrieve the records from “Tasks” table in Remote Data Service.|

### PivotChart (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/RelationalChart#initialize)|It fetches the Relational data required to initialize the PivotChart from server-end.|
|[Drill](WCF/RelationalChart#drill)|It fetches the drilled Relational data required to render the PivotChart control from server-end.|

### PivotChart (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/OlapChart#initialize)|It fetches the OLAP data required to initialize the PivotChart from server-end.|
|[Drill](WCF/OlapChart#drill)|It fetches the drilled OLAP data required to render the PivotChart control from server-end.|
|[Export](WCF/OlapChart#export)|It exports the PivotChart control at the instant to the specified format.|

### PivotClient (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/RelationalClient#initialize)|It fetches the data required to initialize the control.|
|[FetchMembers](WCF/RelationalClient#fetchmembers)|It fetches the details of the members in the selected field on opening member editor.|
|[DrillChart](WCF/RelationalClient#drillchart)|It fetches the drilled data required to render the control on performing drilldown in PivotChart.|
|[Filtering](WCF/RelationalClient#filtering)|It fetches the data required to render the control on performing filtering.|
|[DropNode](WCF/RelationalClient#dropnode)|It fetches the data required to render the control on performing node drop action.|
|[ToolbarOperations](WCF/RelationalClient#toolbaroperations)|It fetches the data required to render the control on performing toolbar operations.|
|[SaveReportToDB](WCF/RelationalClient#savereporttodb)|It saves the current report to database with the specified name.|
|[Export](WCF/RelationalClient#export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[FetchReportListFromDB](WCF/RelationalClient#fetchreportlistfromdb)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WCF/RelationalClient#loadreportfromdb)|It loads the report with specified name from the database to the control.|

### PivotClient (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/OlapClient#initialize)|It fetches the data required to render the PivotClient control initially.|
|[InitializeGrid](WCF/OlapClient#initializegrid)|It fetches the data required to render the PivotGrid control inside PivotClient.|
|[InitializeChart](WCF/OlapClient#initializechart)|It fetches the data required to render the PivotChart control inside PivotClient.|
|[InitializeTreeMap](WCF/OlapClient#initializetreemap)|It fetches the data required to render the PivotTreeMap control inside PivotClient.|
|[DrillChart](WCF/OlapClient#drillchart)|It fetches the drilled data required to render the PivotChart on drilling.|
|[DrillTreeMap](WCF/OlapClient#drilltreemap)|It fetches the drilled data required to render the PivotTreeMap on drilling.|
|[DrillGrid](WCF/OlapClient#drillgrid)|It fetches the drilled data required to render the PivotGrid on drilling.|
|[FilterElement](WCF/OlapClient#filterelement)|It fetches the filtered data required to render the control after performing filtering.|
|[RemoveSplitButton](WCF/OlapClient#removesplitbutton)|It fetches the drilled data required to render the PivotChart on removing an item from report.|
|[FetchMemberTreeNodes](WCF/OlapClient#fetchmembertreenodes)|It fetches the details of the members to render the member editor dialog.|
|[DropNode](WCF/OlapClient#dropnode)|It fetches the data required to render the control after drag and drop action.|
|[CubeChange](WCF/OlapClient#cubechange)|It fetches the data required to render the control on changing the cube.|
|[MeasureGroup](WCF/OlapClient#measuregroup)|It fetches the data required to render the control on changing the measure group.|
|[ToolbarOperations](WCF/OlapClient#toolbaroperations)|It fetches the data required to render the control on performing toolbar operations.|
|[ExpandMember](WCF/OlapClient#expandmember)|It fetches the children nodes on expanding a node in Member Editor.|
|[UpdateReport](WCF/OlapClient#updatereport)|It updates the report in server side.|
|[SaveReportToDB](WCF/OlapClient#savereporttodb)|It saves the current report to database with the specified name.|
|[FetchReportListFromDB](WCF/OlapClient#fetchreportlistfromdb)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WCF/OlapClient#loadreportfromdb)|It loads the report with specified name from the database to the control.|
|[GetMDXQuery](WCF/OlapClient#getmdxquery)|It retrieves the MDX query formed to fetch the data at that instant.|
|[ToggleAxis](WCF/OlapClient#toggleaxis)|It fetches the data after interchanging the elements in row and column axes.|

### PivotGauge (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/RelationalGauge#initialize)|It fetches the Relational data required to render the PivotGauge control from server-end.|

### PivotGauge (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/OlapGauge#initialize)|It fetches the OLAP data required to render the PivotGauge control from server-end.|

### PivotGrid (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/RelationalGrid#initialize)|It fetches the data required to render the PivotGrid initially.|
|[FetchMembers](WCF/RelationalGrid#fetchmembers)|It fetches the members of the selected field to render the member editor tree.|
|[Filtering](WCF/RelationalGrid#filtering)|It fetches the data required to render the PivotGrid control on performing filtering action.|
|[ModifyNodeState](WCF/RelationalGrid#modifynodestate)|It fetches the relational data required to render the PivotGrid control on selecting/unselecting fields in Field list.|
|[DropNode](WCF/RelationalGrid#dropnode)|It fetches the relational data required to render the PivotGrid control on node drop action.|
|[Sorting](WCF/RelationalGrid#sorting)|It fetches the sorted data to render the PivotGrid control on performing sorting.|
|[CalculatedField](WCF/RelationalGrid#calculatedfield)|It forms a calculated field in values area and fetches the data along with it to render the PivotGrid control.|
|[Export](WCF/RelationalGrid#export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WCF/RelationalGrid#savereport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WCF/RelationalGrid#loadreportfromdb)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WCF/RelationalGrid#deferupdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[CellEditing](WCF/RelationalGrid#cellediting)|It rewrites the content of database on editing a cell.|

### PivotGrid (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/OlapGrid#initialize)|It fetches the OLAP data required to render the PivotGrid initially from server-end.|
|[Drill](WCF/OlapGrid#drill)|It fetches the OLAP data required to render the PivotGrid control after drilling it.|
|[DropNode](WCF/OlapGrid#dropnode)|It fetches the data required to render the control after performing node drop operation.|
|[Filtering](WCF/OlapGrid#filtering)|It fetches the OLAP data required to render the control after performing filtering.|
|[FetchMembers](WCF/OlapGrid#fetchmembers)|It fetches the members of the selected hierarchy to render the member editor.|
|[Paging](WCF/OlapGrid#paging)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[RemoveButton](WCF/OlapGrid#removebutton)|It fetches the data required to render the control after removing a button.|
|[ExpandMember](WCF/OlapGrid#expandmember)|It fetches the data to render children nodes of a member in Member Editor Tree.|
|[Export](WCF/OlapGrid#export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WCF/OlapGrid#savereport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WCF/OlapGrid#loadreportfromdb)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WCF/OlapGrid#deferupdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|

### PivotTreeMap (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF/OlapTreeMap#initialize)|It fetches the OLAP data required to render the PivotTreeMap control from server-end.|
|[Drill](WCF/OlapTreeMap#drill)|It fetches the OLAP data required to render the drilled PivotTreeMap.|

