---
layout: post
title: WCF reference for ejService related controls
description: WCF reference for ejService related controls
documentation: ug
platform: js
---

# WCF reference for ej Controls

The details of WCF Service reference has been shown in the below table.

### Northwind Data Service

|  WCF | Description  |
|---|---|
|[Northwind Data Service for Grid](WCF\Northwind#Grid)|It is used to retrieve the records from “Orders” and "Customers" table in Remote Data Service.|
|[Northwind Data Service for Kanban](WCF\Northwind#Kanban)|It is used to retrieve the records from “Tasks” table in Remote Data Service.|

### PivotChart (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\RelationalChart#Initialize)|It fetches the Relational data required to initialize the PivotChart from server-end.|
|[Drill](WCF\RelationalChart#Drill)|It fetches the drilled Relational data required to render the PivotChart control from server-end.|

### PivotChart (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\OlapChart#Initialize)|It fetches the OLAP data required to initialize the PivotChart from server-end.|
|[Drill](WCF\OlapChart#Drill)|It fetches the drilled OLAP data required to render the PivotChart control from server-end.|
|[Export](WCF\OlapChart#Export)|It exports the PivotChart control at the instant to the specified format.|

### PivotClient (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\RelationalClient#Initialize)|It fetches the data required to initialize the control.|
|[FetchMembers](WCF\RelationalClient#FetchMembers)|It fetches the details of the members in the selected field on opening member editor.|
|[DrillChart](WCF\RelationalClient#DrillChart)|It fetches the drilled data required to render the control on performing drilldown in PivotChart.|
|[Filtering](WCF\RelationalClient#Filtering)|It fetches the data required to render the control on performing filtering.|
|[DropNode](WCF\RelationalClient#DropNode)|It fetches the data required to render the control on performing node drop action.|
|[ToolbarOperations](WCF\RelationalClient#ToolbarOperations)|It fetches the data required to render the control on performing toolbar operations.|
|[SaveReportToDB](WCF\RelationalClient#SaveReportToDB)|It saves the current report to database with the specified name.|
|[Export](WCF\RelationalClient#Export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[FetchReportListFromDB](WCF\RelationalClient#FetchReportListFromDB)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WCF\RelationalClient#LoadReportFromDB)|It loads the report with specified name from the database to the control.|

### PivotClient (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\OlapClient#Initialize)|It fetches the data required to render the PivotClient control initially.|
|[InitializeGrid](WCF\OlapClient#InitializeGrid)|It fetches the data required to render the PivotGrid control inside PivotClient.|
|[InitializeChart](WCF\OlapClient#InitializeChart)|It fetches the data required to render the PivotChart control inside PivotClient.|
|[InitializeTreeMap](WCF\OlapClient#InitializeTreeMap)|It fetches the data required to render the PivotTreeMap control inside PivotClient.|
|[DrillChart](WCF\OlapClient#DrillChart)|It fetches the drilled data required to render the PivotChart on drilling.|
|[DrillTreeMap](WCF\OlapClient#DrillTreeMap)|It fetches the drilled data required to render the PivotTreeMap on drilling.|
|[DrillGrid](WCF\OlapClient#DrillGrid)|It fetches the drilled data required to render the PivotGrid on drilling.|
|[FilterElement](WCF\OlapClient#FilterElement)|It fetches the filtered data required to render the control after performing filtering.|
|[RemoveSplitButton](WCF\OlapClient#RemoveSplitButton)|It fetches the drilled data required to render the PivotChart on removing an item from report.|
|[FetchMemberTreeNodes](WCF\OlapClient#FetchMemberTreeNodes)|It fetches the details of the members to render the member editor dialog.|
|[DropNode](WCF\OlapClient#DropNode)|It fetches the data required to render the control after drag and drop action.|
|[CubeChange](WCF\OlapClient#CubeChange)|It fetches the data required to render the control on changing the cube.|
|[MeasureGroup](WCF\OlapClient#MeasureGroup)|It fetches the data required to render the control on changing the measure group.|
|[ToolbarOperations](WCF\OlapClient#ToolbarOperations)|It fetches the data required to render the control on performing toolbar operations.|
|[ExpandMember](WCF\OlapClient#ExpandMember)|It fetches the children nodes on expanding a node in Member Editor.|
|[UpdateReport](WCF\OlapClient#UpdateReport)|It updates the report in server side.|
|[SaveReportToDB](WCF\OlapClient#SaveReportToDB)|It saves the current report to database with the specified name.|
|[FetchReportListFromDB](WCF\OlapClient#FetchReportListFromDB)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WCF\OlapClient#LoadReportFromDB)|It loads the report with specified name from the database to the control.|
|[GetMDXQuery](WCF\OlapClient#GetMDXQuery)|It retrieves the MDX query formed to fetch the data at that instant.|
|[ToggleAxis](WCF\OlapClient#ToggleAxis)|It fetches the data after interchanging the elements in row and column axes.|

### PivotGauge (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\RelationalGauge#Initialize)|It fetches the Relational data required to render the PivotGauge control from server-end.|

### PivotGauge (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\OlapGauge#Initialize)|It fetches the OLAP data required to render the PivotGauge control from server-end.|

### PivotGrid (Relational)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\RelationalGrid#Initialize)|It fetches the data required to render the PivotGrid initially.|
|[FetchMembers](WCF\RelationalGrid#FetchMembers)|It fetches the members of the selected field to render the member editor tree.|
|[Filtering](WCF\RelationalGrid#Filtering)|It fetches the data required to render the PivotGrid control on performing filtering action.|
|[ModifyNodeState](WCF\RelationalGrid#ModifyNodeState)|It fetches the relational data required to render the PivotGrid control on selecting/unselecting fields in Field list.|
|[DropNode](WCF\RelationalGrid#DropNode)|It fetches the relational data required to render the PivotGrid control on node drop action.|
|[Sorting](WCF\RelationalGrid#Sorting)|It fetches the sorted data to render the PivotGrid control on performing sorting.|
|[CalculatedField](WCF\RelationalGrid#CalculatedField)|It forms a calculated field in values area and fetches the data along with it to render the PivotGrid control.|
|[Export](WCF\RelationalGrid#Export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WCF\RelationalGrid#SaveReport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WCF\RelationalGrid#LoadReportFromDB)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WCF\RelationalGrid#DeferUpdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[CellEditing](WCF\RelationalGrid#CellEditing)|It rewrites the content of database on editing a cell.|

### PivotGrid (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\OlapGrid#Initialize)|It fetches the OLAP data required to render the PivotGrid initially from server-end.|
|[Drill](WCF\OlapGrid#Drill)|It fetches the OLAP data required to render the PivotGrid control after drilling it.|
|[DropNode](WCF\OlapGrid#DropNode)|It fetches the data required to render the control after performing node drop operation.|
|[Filtering](WCF\OlapGrid#Filtering)|It fetches the OLAP data required to render the control after performing filtering.|
|[FetchMembers](WCF\OlapGrid#FetchMembers)|It fetches the members of the selected hierarchy to render the member editor.|
|[Paging](WCF\OlapGrid#Paging)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[RemoveButton](WCF\OlapGrid#RemoveButton)|It fetches the data required to render the control after removing a button.|
|[ExpandMember](WCF\OlapGrid#ExpandMember)|It fetches the data to render children nodes of a member in Member Editor Tree.|
|[Export](WCF\OlapGrid#Export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WCF\OlapGrid#SaveReport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WCF\OlapGrid#LoadReportFromDB)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WCF\OlapGrid#DeferUpdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|

### PivotTreeMap (OLAP)

|  WCF | Description  |
|---|---|
|[Initialize](WCF\OlapTreeMap#Initialize)|It fetches the OLAP data required to render the PivotTreeMap control from server-end.|
|[Drill](WCF\OlapTreeMap#Drill)|It fetches the OLAP data required to render the drilled PivotTreeMap.|

