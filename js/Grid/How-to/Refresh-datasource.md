---
layout: post
title: Refresh-datasource
description: refresh datasource
platform: js
control: Grid
documentation: ug
---

### Refresh datasource

**ejGrid** allows you to refresh datasource dynamically after **Grid** **initialization**. It is useful to refresh **Grid** **data** **source**.

{% highlight html %}


<input type="button" id="refresh" value="Refresh" name="refresh"/>
<div id="Grid"></div>
<script type="text/javascript">
    $(function () {// Document is ready.
        // Data for grid.
        window.gridData = [
          { firstName: "John", lastName: "Beckett", email: "john@syncfusion.com" },
          { firstName: "Ben", lastName: "Beckett", email: "ben@syncfusion.com" },
          { firstName: "Andrew", lastName: "Beckett", email: "andrew@syncfusion.com" }
        ];

        $("#refresh").ejButton();
        $("#Grid").ejGrid({
            dataSource: window.gridData,
            columns: [
                     { field: "firstName" , headerText:"First Name" },
                     { field: "lastName", headerText: "Last Name" },
                     { field: "email", headerText: "Email" }
            ]
        });
       // new data source
        var newData = [
          { firstName: "Carter", lastName: "Beckett", email: "carter@syncfusion.com" },
          { firstName: "Joe", lastName: "Beckett", email: "joe@syncfusion.com" },
          { firstName: "Sam", lastName: "Beckett", email: "sam@syncfusion.com" }
        ];
        $("#refresh").click(function() {
            $("#Grid").ejGrid("dataSource", newData);
        });
    });
</script>


{% endhighlight %}



The following screenshot displays the **Grid** data source before refreshing.

![]("/js/Grid/How-to/Refresh-datasource_images/Refresh-datasource_img1.png" Caption="Before Refreshing")

The following screenshot displays the **Grid** data source after refreshing.

![]("/js/Grid/How-to/Refresh-datasource_images/Refresh-datasource_img2.png" Caption="After Refreshing")

