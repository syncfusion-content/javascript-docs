---
layout: post
title: How to - DropDownList widget for Syncfusion Essential JS
description: How To Section in DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
---

## How To

### How to append custom HTML in DropDownList popup outside the scroller part?

Create a custom html element and insert it after popup wrapper. Detailed sample is given [here](http://jsplayground.syncfusion.com/ey2mpity)

### How to set focus to control initially?

[Access key](https://en.wikipedia.org/wiki/Access_key# "") property can be added in input element to set focus. Here focus is set by using access key + “j”.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight js %}

        <script type="text/javascript">
        $(function () {
            var items = [
              { text: "ListItem 1", value: "item1" },
	          { text: "ListItem 2", value: "item2" },
		      { text: "ListItem 3", value: "item3" },
		      { text: "ListItem 4", value: "item4" },
		      { text: "ListItem 5", value: "item5" }
            ];
            $('#dropdown1').ejDropDownList({
                dataSource: items,
                fields: { text: "text", value: "value" }
            });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#dropdown1_wrapper").focus();
            }
          });
       });
    </script>


{% endhighlight %}

### How to clear the text of DropDownList input?

To clear the text of the DropDownList input, you can use “[clearText](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:cleartext)” method.

### How to add an item dynamically to the DropDownList?

You can use “[addItem](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:additem)” method to add single or multiple items dynamically to the popup list. You can define all the possible values that is supported by field property such as text, value, image and its associated attributes such as alt, width, and height etc., html attributes.

Adding text and value is demonstrated in the below given sample,

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight js %}

    <script type="text/javascript">
        $(function () {
            var items = [
              { text: "ListItem 1", value: "item1" },
	          { text: "ListItem 2", value: "item2" },
		      { text: "ListItem 3", value: "item3" },
		      { text: "ListItem 4", value: "item4" },
		      { text: "ListItem 5", value: "item5" }
            ];
            $('#dropdown1').ejDropDownList({
                dataSource: items,
                fields: { text: "text", value: "value" }
            });

            $('#dropdown1').ejDropDownList("addItem", { text: "New Text", value: "text1" });

        });
    </script>

{% endhighlight %}

### How to Disable/ Enable the DropDownList widget?

You can enable or disable the DropDownList widget using “enabled” property or methods. Detailed information is given [here](#_Enable/Disable_the_widget).
### How to control the popup visibility via methods in script showPopup ()/hidePopup ()?

By default popup list is shown on DropDownList button click but you can display the list initially by enabling the “[showPopupOnLoad](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:showpopuponload)” property. You can also use [showPopup ()](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:showpopup) or [hidePopup ()](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:hidepopup) methods at run time to display or hide the popup list.

### How to retrieve the selected item data from select event via arguments?

Bind the select event and you can retrieve the value from args.value. 

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight js %}

        <script type="text/javascript">
        $(function () {
            var items = [
              { text: "ListItem 1", value: "item1" },
	          { text: "ListItem 2", value: "item2" },
		      { text: "ListItem 3", value: "item3" },
		      { text: "ListItem 4", value: "item4" },
		      { text: "ListItem 5", value: "item5" }
            ];
            $('#dropdown1').ejDropDownList({
                dataSource: items,
                fields: { text: "text", value: "value" },
                select: function (args) {
                    console.log("Value is " + args.value);
                }
            });
        });
    </script>


{% endhighlight %}

The following screenshot will exhibit the select event arguments details,
![](HowTo_images/HowTo_img1.jpeg)

### How to add check all option in popup list?

You can use `headerTemplate` property to add any HTML element. Code snippet to add check all option is given below,

{% highlight html %}

     <input type="text" id="dropdown1" />
	 
	 <style>
        .temp {
            height: 30px;
            display: block;
            padding-left: 13px;
            padding-top: 5px;
            border-bottom: 1px solid #c8c8c8;
        }
        .e-chkbox-wrap .e-text {
            font-size: 14px;
            padding-left: 10px;
        }
    </style>
     
{% endhighlight %}

{% highlight js %}

	<script>
        $(function () {
            var items = [
              { text: "ListItem 1", value: "item1" },
	          { text: "ListItem 2", value: "item2" },
		      { text: "ListItem 3", value: "item3" },
		      { text: "ListItem 4", value: "item4" },
		      { text: "ListItem 5", value: "item5" }
            ];
            $('#dropdown1').ejDropDownList({
                width: 300,
                dataSource: items,
                fields: { text: "text", value: "value" },
                showCheckbox: true,
                headerTemplate: "<div class='temp' ><input id ='check' type='checkbox'  />   </div>"
            });
            $("#check").ejCheckBox({ text: "Check All", change: "onallChange" });
        });
        function onallChange(args) {
            window.flag = true;
            var obj = $("#dropdown1").ejDropDownList("instance");
            if (args.isChecked) obj.checkAll();
            else obj.uncheckAll();
            window.flag = false;
        }
    </script>  


{% endhighlight %}

The following screenshot exhibits the output of the above code,
![](HowTo_images/HowTo_img2.jpeg)

