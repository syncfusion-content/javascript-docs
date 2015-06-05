---
layout: post
title: Paging
description: paging
platform: js
control: Grid
documentation: ug
---

# Paging

Paging is a powerful technique in **Grid** that is used to navigate from one page to another. Using this pager, you can implement load on demand concept that loads only required data to **Grid**. To enable paging in **Grid** set **allowPaging** as **True** at **Grid Initialize**.

## Default Paging

When the **allowPaging** property is set as **True**, the properties in the page****settings take the following default values.

* pageSize-12

* pageCount – 8

* currentPage-1

The following code example is for the **Grid** with default options.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
<script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
              **allowPaging: true,**

            });
        });
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Paging_images/Paging_img1.png" Caption="Paging"%}

## External Paging

In this section, you can see how to use external paging. The following code example is for external paging. Using **gotoPage** public api to reach the particular page.

{% highlight html %}

**[JS]**
    <div id="Grid"></div><br />
    <div class="row">
        <div class="col-md-3"></div>
        <div class="col-md-1">
            Go To Page
        </div>
        <div class="col-md-3">
            <input type="text" id="sendpage" />
        </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
                allowPaging: true,

            });
            $("#sendpage").ejNumericTextbox({ value: 1, minValue: 1, maxValue: 10, change: "onChange" });
        });
        function onChange(args) {
            var gridobj = $("#Grid").data("ejGrid");
            gridobj.**goToPage**(args.value);
        }
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Paging_images/Paging_img2.png" Caption="External Paging"%}

## Pager Templates

**Pager Templates** feature provide support to render a specific custom template to a **Grid pager** using **enableTemplates** and **template** properties of **pageSettings**. **showDefaults** property is used to show/hide default pager for **Grid**.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
<script type="text/javascript">
         $(function () {
            var data = ej.DataManager(window.gridData).executeLocal(ej.Query().take(50));
            $("#Grid").ejGrid({
                dataSource: data,
                pageSettings: { **enableTemplates: true, template: "#template", showDefaults: false** },
                columns: ["OrderID "," CustomerID "," EmployeeID "," Freight ","       
                         OrderDate"]
            });
        });
    </script> 
    <script type="text/x-jsrender" id="template">
        <a id="prev" value="Prev">Prev</a>
        <input type="text"/>
        <input type="button" value="Go"/>
        <a>Next</a>
    </script>   


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Paging_images/Paging_img3.png" Caption="Pager Template"%}

## Methods

The following are the public methods of pager.

* gotoPage

* refreshPager

In this section, you can see how to use paging methods in **Grid** control. The following code example is for paging methods. 

{% highlight html %}

**[JS]**

  <div id="Grid"></div><br />
    <div class="row">
        <div class="col-md-1"></div>
        <div class="col-md-1">
            goto
        </div>
        <div class="col-md-2">
            <input type="text" id="goto" />
        </div>
        <div class="col-md-1">
            Page Count
        </div>
        <div class="col-md-2">
            <input type="text" id="pageCount" />
        </div>

        <div class="col-md-1">
            Page Size
        </div>
        <div class="col-md-2">
            <input type="text" id="PageSize" />
        </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
              **allowPaging: true,**
                pageSettings: { pageSize: 5 },

            });
            $("#goto").ejNumericTextbox({ value: 1, minValue: 1, change: "pageChange" });
            $("#pageCount").ejNumericTextbox({ value: 1, minValue: 1, maxValue: 10, change: "pageCountChange" });
            $("#PageSize").ejNumericTextbox({ value: 12, minValue: 1, maxValue: 10, change: "pageSizeChange" });
        });
        function pageChange(args) {
            $("#Grid").ejGrid("getPager").ejPager("**goToPage**", args.value);
        }
        function pageCountChange(args) {
            $("#Grid").ejGrid({ "pageSettings": { pageCount: parseInt(args.value) } });
        }
        function pageSizeChange(args) {
            $("#Grid").ejGrid({ "pageSettings": { pageSize: parseInt(args.value) } });
        }
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Paging_images/Paging_img4.png" Caption="Paging Methods"%}

## Localization for paging

Localization is the process of customizing the user interface (**UI**) as locale-specific, inorder to display regional data. With this feature, data can be displayed in a language and culture specific to a particular country or region. The **JavaScript Grid** control provides inherent support to localize its **UI**.

The following **UIs** are provided to localize based on culture. The default English localization **UIs** are as follows.

{% highlight html %}

pagerInfo: "{0} of {1} pages ({2} items)",
firstPageTooltip: "Go to first page",
lastPageTooltip: "Go to last page",
nextPageTooltip: "Go to next page",
previousPageTooltip: "Go to previous page ",
nextPagerTooltip: "Go to next pager",
previousPagerTooltip: "Go to previous pager "


{% endhighlight %}



In this section, you can see how to use Globilzation in Grid pager. The following code example is for pager localization in German and Spanish. 

{% highlight html %}

**[JS]**

  <div id="Grid"></div>
    <div>
        <select id="language">
            <option value="en-US">English</option>
            <option value="de-DE">German</option>
            <option value="es-ES">Spanish</option>
        </select>
    </div>
    <script type="text/javascript">
        ej.Pager.locale["en-US"] = {
            pagerInfo: "{0} of {1} pages ({2} items)",
            firstPageTooltip: "Go to first page",
            lastPageTooltip: "Go to last page",
            nextPageTooltip: "Go to next page",
            previousPageTooltip: "Go to previous page ",
            nextPagerTooltip: "Go to next pager",
            previousPagerTooltip: "Go to previous pager "
        };
        ej.Pager.locale["de-DE"] = {
            pagerInfo: "{0} von {1} Seiten ({2} Beiträgee)",
            firstPageTooltip: "Zur ersten Seite",
            lastPageTooltip: "gehen Zur letZten Seite",
            nextPageTooltip: "Zur nächsten Seite",
            previousPageTooltip: "Zuruck Zur letZten Seite",
            nextPagerTooltip: "genhen Sie Zum nächsten pager ",
            previousPagerTooltip: "Zur vorherigen pager"
        };
        ej.Pager.locale["es-ES"] = {
            pagerInfo: "{0} de {1}páginas ({2} artículos)",
            firstPageTooltip: "Ir a la primera página",
            lastPageTooltip: "Ir a la última páginas",
            nextPageTooltip: "Ir a la página siguiente",
            previousPageTooltip: "Ir a la página anterior",
            nextPagerTooltip: "Ir a la siguiente pager",
            previousPagerTooltip: "Ir al localizador anterior"
        }
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
                allowPaging: true,
                pageSettings: { pageSize: 6 },
                locale: $("#lan").val(),
            });
            $("#language").ejDropDownList({ width: "120px", "change": "onChange" , selectedItemIndex: 1 })
        });
        function onChange(args) {
            $("#Grid").ejGrid("model.locale", args.value);
        }
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Paging_images/Paging_img5.png" Caption="Pager Localization"%}

