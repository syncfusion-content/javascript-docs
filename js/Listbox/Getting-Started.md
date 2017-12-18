---
layout: post
title: Getting-Started
description: getting started
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Getting Started

This section helps to understand the getting started of the ListBox widget with the step-by-step instructions.

## Script/CSS reference

Create a new HTML file and include the below code

{% highlight html %}

<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8"/>
    <title></title>
</head>
<body>

</body>
</html>


{% endhighlight %}



Add link to the CSS file from the specific [theme](https://help.syncfusion.com/js/theming-in-essential-javascript-components) folder to your HTML file within the head section. Refer the built-in theme which is mentioned [here](https://help.syncfusion.com/js/theming-in-essential-javascript-components). 

{% highlight html %}

    <meta charset="utf-8" />
    <title>Getting Started - ListBox </title>
    <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />


{% endhighlight %}



Add links to the [CDN](https://help.syncfusion.com/js/cdn) Script files with dependencies to the head section.

{% highlight html %}


    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js"></script>


{% endhighlight %}

### See Also

[Custom Script Generator](https://csg.syncfusion.com/)


 N> To reduce the file size further please use  [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) compression in your server.

## Create ListBox

Create UL and LI elements and add in the &lt;body&gt; tag.

Initialize the ListBox widget as below.

{% tabs %}
{% highlight html %}

               <div>
                    <ul id="listbox">
                        <li>Audi A4</li>
                        <li>Audi A5</li>
                        <li>Audi A6</li>
                        <li>Audi A7</li>
                        <li>Audi A8</li>
                        <li>BMW 501</li>
                        <li>BMW 502</li>
                        <li>BMW 503</li>
                        <li>Batch</li>
                        <li>BMW 507</li>
                        <li>BMW 3200</li>
                        <li>Cut</li>
                    </ul>
                </div>


{% endhighlight %}

{% highlight javascript %}


      $(function () {
        $("#listbox").ejListBox();
      });



{% endhighlight %}
{% endtabs %}


![Alt text](Getting-Started_images\Getting-Started_img1.png)

## Data binding

We can populate data in the ListBox widget using [dataSource](https://help.syncfusion.com/api/js/ejlistbox#members:datasource) and [fields](https://help.syncfusion.com/api/js/ejlistbox#members:fields) properties. 

{% seealso %} [Data binding](https://help.syncfusion.com/js/listbox/databinding). {% endseealso %}

{% highlight html %}


 <ul id="listbox"></ul>

    <script type="text/javascript">
        jQuery(function ($) {


            bikeList = [
                { bikeId: "bk1", bikeName: "Apache RTR" }, 
                { bikeId: "bk2", bikeName: "CBR 150-R" }, 
                { bikeId: "bk3", bikeName: "CBZ Xtreme" },
                { bikeId: "bk4", bikeName: "Discover" }, 
                { bikeId: "bk5", bikeName: "Dazzler" }, 
                { bikeId: "bk6", bikeName: "Flame" },
                { bikeId: "bk7", bikeName: "Fazer" }, 
                { bikeId: "bk8", bikeName: "FZ-S" }, 
                { bikeId: "bk9", bikeName: "Pulsar" },
                { bikeId: "bk10", bikeName: "Shine" }, 
                { bikeId: "bk11", bikeName: "R15" }, 
                { bikeId: "bk12", bikeName: "Unicorn" }
            ];
            $("#listbox").ejListBox({
                dataSource: bikeList,
                fields: { 
                     id: "bikeId", 
                     text: "bikeName" 
                }
            });
        });

    </script> 



{% endhighlight %}

![Databinding Listbox](Getting-Started_images\Getting-Started_img2.png)

## Selection

The ListBox widget supports item selection using [selectedIndex](https://help.syncfusion.com/api/js/ejlistbox#members:selectedindex) and [selectedIndices](https://help.syncfusion.com/api/js/ejlistbox#members:selectedindices) property. 

{% seealso %} [Selection](https://help.syncfusion.com/js/listbox/selection) {% endseealso %}

{% highlight javascript %}


        jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    selectedIndex: 2
                });
        });




{% endhighlight %}





![Selection Listbox](Getting-Started_images\Getting-Started_img3.png)

