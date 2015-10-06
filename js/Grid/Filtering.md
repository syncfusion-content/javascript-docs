---
layout: post
title: Filtering
description: filtering
platform: js
control: Grid
documentation: ug
---

# Filtering

Filtering is used to filter particular or related records in **Grid** to review details of records. To enable filtering behavior in **Grid** you can add [`allowFiltering`](/js/api/ejgrid#members:allowfiltering "allowFiltering") property at **Grid** initialize. There are three types of filtering features in grid. They are

* Filter menu
* Filter Bar
* Excel styled menu

## Filter Menu 

After you enable **Filter Menu** in **Grid**, it shows filter menu to filter records. This menu contains filtering options based on column type.

**Filter menu types**

* String menu filtering 
* Numeric menu filtering
* Date menu filtering
* Boolean menu filtering

Filter menus are a good **UI** based filtering option. It visibly denotes filtering option and is flexible to filter records. In String menu filtering, [**ejAutoComplete** ](/js/autocomplete/overview "ejAutoComplete") is used as default control to filter; in Numeric menu filtering,[**ejNumericTextbox**](/js/currency/overview "ejNumericTextbox") is used as default control to filter. In Date menu filtering, [**ejDatePicker**](/js/datepicker/overview' "ejDatePicker") control is used as default control to filter and in Boolean menu filtering, [**ejCheckBox**](/js/checkbox/overview "ejCheckBox") is used for filtering. 

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowFiltering: true,
          filterSettings: { filterType: "menu" },
          allowPaging: true,
      });
  });
  
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Filtering_images/Filtering_img1.png"%}

## Filter Bar

[**Filter bar**](/js/api/ejgrid#members:filtersettings-filterbarmode "Filter bar") is one of the types of filtering. It is otherwise called **text filtering** as filter bar working is based on text boxes. Through this you can filter records. [**Filter bars**](/js/api/ejgrid#members:filtersettings-filterbarmode "Filter bar") have expression to filter records. They are based on type of column. 

_List of Filter Bar Expressions_

<table>
<tr>
<td rowspan = "4">
Numeric column</td><td>
N> value</td><td rowspan = "4">
To filter numeric column. You can use these expressions.</td></tr>
<tr>
<td>
< value</td></tr>
<tr>
<td>
= value</td></tr>
<tr>
<td>
!= value</td></tr>
<tr>
<td>
String</td><td>
startsWith</td><td>
By default, string filtering works starts with operator</td></tr>
<tr>
<td>
Date</td><td>
Equal</td><td>
By default, date filter bar matches records with same date value</td></tr>
<tr>
<td>
Boolean</td><td>
Equal</td><td>
Boolean filter bar works with either <b>true</b> or <b>false</b>.</td></tr>
</table>


{% highlight javascript %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowFiltering: true,
          filterSettings: { filterType: ej.Grid.FilterType.FilterBar },
          allowPaging: true,
      });
  });
  
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Filtering_images/Filtering_img2.png"%}

## Excel styled menu

You can enable the Excel like filter menu by setting the [`filterType`](/js/api/ejgrid#members:filtersettings-filtertype "filterType") as “excel” of the [`filterSettings`](/js/api/ejgrid#members:filtersettings "filterSettings") property. The filter menu is displayed after clicking the filter icon in the column headers. 

The filter menu contains options such as Sorting, Clear filter, submenu for the advanced filter options, 

### Checkbox list

The Checkbox list is available in the menu that contains the possible filter value for the column. It shows the list of possible filter values with the checkbox. The filter value can be selected by clicking the checkbox corresponding to that value. By clicking the **Ok** button, the column is filtered based on the values checked in the checkbox list. The **SelectAll** checkbox is also present in the checkbox list that allows either select or deselect all the checkboxes.

The output of the excel like filterin as shown as below.

{% include image.html url="/js/Grid/Filtering_images/Filtering_img3.png"%}

A Search box is available at the top of the check box list that is used to search the possible filter choices. The number of possible filter choices are restricted by the setting the [`maxFilterChoices`](/js/api/ejgrid#members:filtersettings-maxfilterchoices "maxFilterChoices") property of the [`filterSettings`](/js/api/ejgrid#members:filtersettings "filterSettings"). 

### Advanced Filter

The Submenu items in the filter menu provide the advanced filtering options for end users. When selecting a sub menu item, a separate dialog box opens and displays an advanced filter drop-down that lists the available filter operators for the respective filtering column. The filtering is performed by clicking the **Ok** button.

The ourput of the custom filter menu was showed in below screenshot.

{% include image.html url="/js/Grid/Filtering_images/Filtering_img4.png"%}

{% include image.html url="/js/Grid/Filtering_images/Filtering_img5.png"%}

{% highlight html %}




<div id="Filtering"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Filtering").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowFiltering: true,
          filterSettings: { filterType: "excel", maxFilterChoices:100,enableCaseSensitivity:false },
          allowPaging: true,
          columns: [
              { field: "OrderID", headerText: "Order ID", textAlign: "right" },
              { field: "CustomerID", headerText: "Customer ID" },
              { field: "OrderDate", headerText: "Order Date", format: "{0:MM/dd/yy}" },
              { field: "EmployeeID", headerText: "Employee ID", textAlign: "right" },
              { field: "ShipCity", headerText: "Ship City" },
              { field: "Verified", headerText: "Verified" }
          ]
      });
  });
</script>



{% endhighlight %}

## Filter operators

**ejGrid** uses filter operators from [ej**DataManager**](/js/datamanager/filtering "ejDataManager"), that are used at the time of filtering. Filter operators are used to denote filtering type.

_List of Column type and Filter operators_

<table>
<tr>
<th>
<b>Column type</b></th><th>
<b>Filter operators</b></th></tr>
<tr>
<td>
Number</td><td>
ej.FilterOperators.greaterThan<br/>
ej.FilterOperators.greaterThanOrEqual<br/>
ej.FilterOperators.lessThan<br/>
ej.FilterOperators.lessThanOrEqual<br/>
ej.FilterOperators.equal</td></tr>
<tr>
<td>
String</td><td>
ej.FilterOperators.startsWith<br/>
ej.FilterOperators.endsWith<br/>
ej.FilterOperators.contains<br/>
ej.FilterOperators.equal<br/>
ej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Boolean</td><td>
ej.FilterOperators.equal<br/>
ej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Date</td><td>
ej.FilterOperators.greaterThan<br/>
ej.FilterOperators.greaterThanOrEqual<br/>
ej.FilterOperators.lessThan<br/>
ej.FilterOperators.lessThanOrEqual<br/>
ej.FilterOperators.equal</td></tr>
</table>
## External Filtering

**ejGrid** contains an **API** to do filtering dynamically after **Grid** initialize, without the use of **User Interaction**. It is useful to do filtering dynamically.

{% highlight html %}



<div>
  <div class="row">
    <div class="col-md-1">
      Columns
    </div>
    <div class="col-md-1">
      <select id="columns">
        <option value="OrderID">Order ID</option>
        <option value="CustomerID">Customer ID</option>
        <option value="EmployeeID">Employee ID</option>
        <option value="ShipCity">Ship City</option>
        <option value="Verified">Verified</option>
      </select>
    </div>
  </div>
  <br />
  <div class="row">
    <div class="col-md-1">
      Operator
    </div>
    <div class="col-md-1">
      <select id="operator">
        <option value="contains">Contains</option>
        <option value="endswith">Endswith</option>
        <option value="equal">Equal</option>
        <option value="greaterthan">Greaterthan</option>
        <option value="greaterthanorequal">GreaterThanOrEqual</option>
        <option value="lessthan">LessThan</option>
        <option value="lessthanorequal">LessThanOrEqual</option>
        <option value="notequal">NotEqual</option>
        <option value="startswith">StartsWith</option>
      </select>
    </div>
  </div>
  <br />
  <div class="row">
    <div class="col-md-1">
      Value
    </div>
    <div class="col-md-1">
      <input type="text" class="e-ejinputtext" id="value" style="width: 143px;height:26px" />
    </div>
  </div>
  <br />
  <div class="row">
    <div class="col-md-2">
      <input type="button" id="filter" value="filter" />
    </div>
  </div>
</div>
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowFiltering: true,
          filterSettings: { filterType: ej.Grid.FilterType.Menu },
          allowPaging: true,                                     
      });
      $("#columns,#operator").ejDropDownList();
      $("#filter").ejButton({
          click: function (args) {
              $("#Grid").ejGrid("filterColumn", $("#columns").ejDropDownList("getSelectedValue"), $("#operator").ejDropDownList("getSelectedValue"), $("#value").val(),"and");
          }
      });
  });
  
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Filtering_images/Filtering_img6.png"%}

