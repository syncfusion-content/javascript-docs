---
layout: post
title: Print-Grid
description: print grid
platform: js
control: Grid
documentation: ug
---

# Print Grid

Printing is easy with **Grid** control by using **Print Grid** feature. Toolbar has the **Print** icon, it allows to print the **Grid** records. When you click the **Print** icon, it internally calls the public **print()** method of **Grid** object to print the **Grid**. You can also use **print()** method manually to print.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
<script type="text/javascript">
         $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,  				     
                toolbarSettings:{showToolbar:true,toolbarItems: [**ej.Grid.ToolBarItems.PrintGrid**]},
                columns: ["OrderID "," CustomerID "," EmployeeID "," Freight”
                        ," ShipCity” ," Verified”]]
            });
        });
    </script>    


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Print-Grid_images/Print-Grid_img1.png" Caption="Print Grid"%}

