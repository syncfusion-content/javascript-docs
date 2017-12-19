---
layout: post
title: Features
description: Print features for Essential JS
platform: js
control: Print
documentation: ug
---

# Print options

The Print widget comes with other enhanced options to exclude specific elements on a page before printing, print the content on a new window and includes external styles to the page before printing, thus allowing appearance customization to be applied on the printed page.

## Printing specific elements

It is possible to print a particular element alone from a page. For this, you need to pass that particular element into the `print` method.

{% highlight html %}

    <div id="control">
        <div id='Grid'></div>
        <br />
        <div class="control2">
            <b>Note</b>:Grid control rendered with local data
        </div>
        <button class="button" id="print">Print</button>
    </div>
   

{% endhighlight %}

To print the grid layout alone excluding other items from a web page, refer the below code example.

{% highlight javascript %}

        $(function () {
            $('#Grid').ejGrid({
                dataSource: shipDetails
            });
            $("#print").ejButton({
                size: "normal", width: "113px", click: "onPrint"
            });
        })
        var shipDetails = [
              { Name: 'Hanari Carnes', City: 'Brazil' },
              { Name: 'Split Rail Beer & Ale', City: 'USA' },
              { Name: 'Ricardo Adocicados', City: 'Brazil' }
        ];
        function onPrint(e) {
            var elem = $("#Grid");
            if (!elem.hasClass("e-print")) {
                $("#Grid").ejPrint();
            } else {
                obj = $("#Grid").ejPrint("instance");
                obj.print(".control2");
            }
        }
        
{% endhighlight %}


## Printing entire page

It is possible to print the entire web page by calling the `ejPrint` on document body, which is depicted in the below code example. Here, the entire page including all the items on the page will be printed.

{% highlight javascript %}

        function onPrint(e) {
            var elem = $(document.body);
            if (!elem.hasClass("e-print")) {
                $(document.body).ejPrint();
            } else {
                obj = $(document.body).ejPrint("instance");
                obj.print();
            }
        }
          

{% endhighlight %}


## Excluding specific elements

It is possible to exclude specific selectors from a page or from specific component before printing it. This can be achieved by using the `excludeSelector` property.

The below code example depicts the way to print the grid control excluding specific elements with the class name 'e-row' from it.

{% highlight javascript %}

        function onPrint(e) {
            var elem = $("#Grid");
            if (!elem.hasClass("e-print")) {
                $("#Grid").ejPrint({ excludeSelector: ".e-row" });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option("excludeSelector", ".e-row");
                obj.print();
            }
        }
{% endhighlight %}


## Printing content in a new window

It is possible to print the content in a new window by making use of the `printInNewWindow` property, which is depicted in the below code example.

{% highlight javascript %}

        function onPrint(e) {
            var elem = $("#Grid");
            if (!elem.hasClass("e-print")) {
                $("#Grid").ejPrint({ printInNewWindow:true });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option("printInNewWindow",true);
                obj.print();
            }
        }

{% endhighlight %}


## Applying external styles

It is possible to include other external styles on the elements of a printed page, by passing an URL of an external stylesheet to the `externalStyles` property.

{% highlight javascript %}

        function onPrint(e) {
            var elem = $("#Grid");
            if (!elem.hasClass("e-print")) {
                $("#Grid").ejPrint({ externalStyles:"printStyle.css" });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option("externalStyles","printStyle.css");
                obj.print();
            }
        }
    
{% endhighlight %}

The style that is defined within the `printStyle.css` file is depicted below.

{% highlight html %}

<style>

.e-grid .e-headercelldiv{
	font-size:20px !important;
}

</style>

{% endhighlight %}

N> The CSS file can be placed in any of your system location, but its path needs to be provided accurately to the `externalStyles` property.
