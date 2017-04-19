---
layout: post
title: Data-Exploration
description: data exploration
platform: js
control: PivotClient
documentation: ug 
api: /api/js/ejpivotclient
---

# Data Exploration

## Filtering

### Filtering by Member

By clicking the Split Button of a field, Member Editor dialog opens through which members are filtered by checking and unchecking the check boxes corresponding to the members.  

![](Data-Exploration_images/relational-filterbymember.png)

On clicking the "OK" button, based on the selected members in the Member Editor dialog, PivotReport gets updated and refreshes the PivotGrid and PivotChart controls.  The "Cancel" button is used to cancel the selection.

![](Data-Exploration_images/relational-filter-grouping.png) 

The above filter illustrates that the members 'Canada' and 'Germany' are alone included in the Grid and Chart controls.

## Grouping

The data can be grouped when more than one field is added to columns or rows in Axis Element Builder.  Based on the order of addition, data is grouped and the report is updated. In the following example, the **Date** field values get grouped, with respect to **Country** field values.  Likewise multiple field members can be grouped by dragging the fields from pivot fields list to Axis Element Builder.

![](Data-Exploration_images/relational-grouping.png)

## Searching

Members can be searched and displayed from the members list inside the Member Editor dialog.

![](Data-Exploration_images/relational-search-grouping.png)