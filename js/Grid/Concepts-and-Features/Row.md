---
layout: post
title: Row
description: row
platform: js
control: Grid
documentation: ug
---

# Row

## Details Template

**Details Template** feature provides a detailed view about additional information of each row. If you want to view the detailed information, you can expand a row.We are able to set the detail template content using **detailsTemplate** property.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script id="tabGridContents" type="text/x-jsrender">
      <div id="contact{{:EmployeeID}}" style="font-weight:bold; padding:5px;">
      <div id="cont">
                contact:**{{:**Address**}}**<br />
                city:**{{:**City**}}**<br />
                Country:**{{:**Country**}}**<br />
                phone:**{{:**HomePhone**}}**<br />
            </div>
        </div>
    </script>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.employeeView" is referred from jsondata.min.js
                dataSource: ej.DataManager(window.employeeView).executeLocal(ej.Query().take(9)),
**detailsTemplate**: "#tabGridContents", // detail template
            });
        });
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Row_images/Row_img1.png" Caption="Details Template"%}

## Hierarchy

In this section, you can learn how to use the **Hierachy****tree** in **Grid****View**. The following code example is of **Hierachy****Grid**.

{% highlight html %}

**[JS]**

 <div id="Grid"></div>

    <script id="tabGridContents" type="text/x-jsrender">
        <div class="tabcontrol" id="Test">
                <div id="detailGrid">
            <label id="employeeDet" style="display: none">{{:EmployeeID}}</label>
        </div>
    </script>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.employeeView" is referred from jsondata.min.js
                dataSource: ej.DataManager(window.employeeView).executeLocal(ej.Query().take(9)),
**detailsTemplate**: "#tabGridContents",
                detailData: "detailGridData",
            });
        });
        function detailGridData(e) {
            var filteredData = e.detailsElement.find("#employeeDet").text();
            // the datasource "window.ordersView" is referred from jsondata.min.js
            var data = ej.DataManager(window.ordersView).executeLocal(ej.Query().where("EmployeeID", "equal", parseInt(filteredData), true));
            e.detailsElement.find("#detailGrid").ejGrid({
                dataSource: data,
            });            
        }
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Row_images/Row_img2.png" Caption="Hierachy"%}

## Row Template

**Row template** is used to render your template in every row. It is used to place elements inside **Grid** rows. This feature makes it easier to customise **Grid** rows with **HTML** elements. We are able to set the detail template content using **rowTemplate** property.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
<script id="templateData" type="text/x-jsrender">
<tr>
<td class="photo">
<img style="width:130px;height: 160px" src="http://js.syncfusion.com/demos/web/themes/images/Employees//{{:EmployeeID}}.png" alt="{{:EmployeeID}}" />
</td>
<td class="details">
<table class="CardTable" cellpadding="3" cellspacing="6">
<colgroup>
<col width="50%">
<col width="50%">
</colgroup>
<tbody>
<tr>
<td class="CardHeader" >First Name: </td>
<td style="padding:20px">{{:FirstName}} </td>
</tr>
<tr>

<td class="CardHeader">
Birth Date:
</td>
<td style="padding:20px">
{{:BirthDate.toLocaleDateString()}}
</td>
</tr>
<tr>

<td class="CardHeader">
Hire Date:
</td>
<td style="padding:20px">
{{:HireDate.toLocaleDateString()}}
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</script>
<style>
.CardHeader {
font-weight:bold;
font-size:14px;
padding:20px;
}
</style>
<script type="text/javascript">
$(function () {
$("#Grid").ejGrid({
// the datasource "window.employeeData" is referred from templatelocaldata.js
dataSource: window.employeeView,
allowScrolling: true,
scrollSettings: { height: 480, width: 500 },
**rowTemplate**: "#templateData",   // row template
columns: [
{ headerText: "Photo", width: 30 },
{ headerText: 'Employee Details', width: 70 }
]
});
});
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Row_images/Row_img3.png" Caption="Row Template"%}

## Customize Hover and AltRow 

**enableAltRow** and **enableRowHover** are graphical features in **Grid** that are used to enable alternate row color in **Grid** and enable hover effects while hovering over row cells. By default, these two features are enabled in **Grid**. In this section, you can learn how to cutomize alternative rows color and hover color in the **ejGrid** controls.

{% highlight html %}

**[JS]**

<style>
        .e-grid .e-alt_row {
            background-color: lightgreen !important;
        }

        .e-grid .e-hover {
            background: black !important;
        }
    </style>
<body>
    <div id="Grid"></div>
    <script type="text/javascript">
        $(function(){
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
                **enableRowHover: true,**
                **enableAltRow: true,**
                allowPaging: true,
                pageSettings: { pageSize: 5 },
            });
        });
    </script>
</body>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Row_images/Row_img4.png" Caption="Customize hover and altrow"%}

