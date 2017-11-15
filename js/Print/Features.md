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
            var ele = $("#Grid");
            if (!ele.hasClass("e-print")) {
                $("#Grid").ejPrint();
                var obj = $("#Grid").ejPrint("instance");
                obj.print(".control2");
            } else {
                obj = $("#Grid").ejPrint("instance");
                obj.print(".control2");
            }
        }
        
{% endhighlight %}

![](Print-Features-Images\Features1.png)

## Printing entire page

It is possible to print the entire web page by caling the `ejPrint` on the document body, which is depicted in the below code example.

{% highlight javascript %}

        function onPrint(e) {
            var ele = $(document.body);
            if (!ele.hasClass("e-print")) {
                $(document.body).ejPrint();
            } else {
                obj = $(document.body).ejPrint("instance");
                obj.print();
            }
        }
          

{% endhighlight %}

![](Print-Features-Images\Features2.png)


## Excluding specific elements

It is possible to exclude specific selectors from a page or from specific component before printing it. This can be achieved by using the `excludeSelector` property.

{% highlight javascript %}

        function onPrint(e) {
            var ele = $("#Grid");
            if (!ele.hasClass("e-print")) {
                $("#Grid").ejPrint({ excludeSelector: ".e-row" });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option(excludeSelector, ".e-row");
                obj.print();
            }
        }
{% endhighlight %}

![](Print-Features-Images\Features3.png)

## Printing content in a new window

It is possible to print the content in a new window by making use of the `printInNewWindow` property, which is depicted in the below code example.

{% highlight javascript %}

        function onPrint(e) {
            var ele = $("#Grid");
            if (!ele.hasClass("e-print")) {
                $("#Grid").ejPrint({ printInNewWindow:true });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option(printInNewWindow,true);
                obj.print();
            }
        }

{% endhighlight %}

## Applying external styles

It is possible to include other external styles on the printed page, by passing an URL of an external stylesheet to the `externalStyles` property.

{% highlight javascript %}

        function onPrint(e) {
            var ele = $("#Grid");
            if (!ele.hasClass("e-print")) {
                $("#Grid").ejPrint({ externalStyles:"printStyle.css" });
            } else {
                var obj = $("#Grid").ejPrint("instance");
                obj.option(externalStyles,"printStyle.css");
                obj.print();
            }
        }
    
{% endhighlight %}

printStyle.css file

{% highlight html %}

<style>

.e-grid .e-headercelldiv{
	font-size:20px !important;
}

</style>

{% endhighlight %}