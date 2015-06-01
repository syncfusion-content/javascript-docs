---
layout: post
title: Getting-Started
description: getting started
platform: js
control: ListBox
documentation: ug
---

# Getting Started

This section explains briefly on how to create a **ListBox** control in your application.

## Create your first ListBox in JavaScript

Here you can learn how to customize **ListBox** in Contact Selection tool. This allows you display the list of contacts, to select and move them to the next **ListBox** that has the selected items. The following example illustrates simulator of Group Creation tool like Skype messenger.

The following screenshot demonstrates the functionality of **ListBox** with **Multi-Selection** and **Drag and Drop** features.



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img1.png" Caption=""%}

_Figure_ _1__: Group creation tool Simulator using ListBox_

In the above screenshot, you can select a list item from the first **ListBox** widget. After you select the item, you can move the selected item to the second **ListBox** widget. 

**Create a ListBox Widget**

**Essential****JavaScript****ListBox** widget renders with built-in features.

* You can create an **HTML** file and add the following code example to it. 



{% highlight html %}


<!doctype html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src=" http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js "></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>
</head>
<body>
    <!--add the ListBox element here -->
</body>
</html>



{% endhighlight %}



* Add the **&lt;ul&gt;** element to render **ListBox** widgets.



{% highlight html %}


<div id="sample">
    <h5><b>Add people</b></h5>
    <h5>Choose a contact and click move button to add in group </h5>
    <div id="control">

        <div id="container1">
            Contacts List
            <ul id="select">
            </ul>
        </div>

        <div class="middlebuttons">
            <button id="Add">>></button>
            <br />
            <br />
            <button id="Remove"><<</button>
        </div>

        <div id="container2">
            People in this group
            <ul id="selecteditems">
            </ul>
        </div>
    </div>
</div>


{% endhighlight %}



* Add the following style section for the **ListBox** widgets alignment. 



{% highlight css %}


<style type="text/css" class="cssStyles">
    #control {
        height: 300px;
        width: 500px;
        padding: 25px;
        background-color: #f7f7f7;
        display: flex;
    }

    #sample {
        height: 472px;
        width: 600px;
    }

    #selecteditems_container {
        float: right;
    }

    #select_container {
        float: left;
    }

    .middlebuttons {
        padding: 91px 25px 25px 25px;
    }

    #container1, #container2 {
        width: 200px;
    }

    img {
        padding-right: 10px;
        padding-top: 3px;
        width: 18px;
        height: 15px;
    }
</style>



{% endhighlight %}



* Initialize the **ListBox** and other widgets using the following code sample.



{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        // document ready
        // simple ListBox creation 

        $("#select").ejListBox();
        $("#selecteditems").ejListBox();
        // simple Button creation 
        // to add list item to selection ListBox
        $("#Add").ejButton({
            size: "normal",
            showRoundedCorner: true,
        });
        // to remove an list item from selection ListBox
        $("#Remove").ejButton({
            size: "normal",
            showRoundedCorner: true,
        });
    });
</script>



{% endhighlight %}



* Run this code to render the resultant output of the above steps.



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img2.png" Caption=""%}

_Figure_ _2__: Render ListBox with &lt;ul&gt;&lt;/ul&gt; element_

**Configure ListBox with Items**

To populate items inside **ListBox**, you have to add list items inside **&lt;ul&gt;** as **&lt;li&gt;&lt;/li&gt;** elements. Include the following **&lt;li&gt;** elements in your sample.



{% highlight html %}


<div id="sample">
    <h5><b>Add people</b></h5>
    <h5>Choose a contact and click move button to add in group </h5>
    <div id="control">

        <div id="container1">
            Contacts List
            <ul id="select">
                <li>
                    <img src="images/listbox/busy.png" alt=" busy" />
                    Nancy</li>
                <li>
                    <img src="images/listbox/busy.png" alt="busy" />
                    Andrew</li>
                <li>
                    <img src="images/listbox/avail.png" alt="Flag" />
                    Janet</li>
                <li>
                    <img src="images/listbox/away.png" alt="away" />
                    Margaret</li>
                <li>
                    <img src="images/listbox/away.png" alt="away" />
                    Michael</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Robert</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Laura</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Anne</li>
                <li>
                    <img src="images/listbox/away.png" alt="away" />
                    Suyama</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Callahan</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Peacock</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Fuller</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Davolio</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Dodsworth</li>
                <li>
                    <img src="images/listbox/avail.png" alt="avail" />
                    Louis</li>
            </ul>
        </div>

        <div class="middlebuttons">
            <button id="Add">>></button>
            <br />
            <br />
            <button id="Remove"><<</button>
        </div>

        <div id="container2">
            People in this group

            <ul id="selecteditems">
            </ul>
        </div>
    </div>
</div>



{% endhighlight %}



Run the above code to render **ListBox** with list items rendered inside **ListBox. ListBox** with Contact list items is shown as follows.



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img3.png" Caption=""%}

_Figure_ _3__: ListBox with Contact list items_

**Enable Drag and Drop** 

You can drag an item from a **ListBox** and drop it in a droppable element.To drag and drop a list item across control or within the control, you have to set **allowDragAndDrop** property as **“True”.**



{% highlight js %}

<script type="text/javascript">
    jQuery(function ($) {
        $("#select").ejListBox({
            allowDragAndDrop: true
        });
        $("#selecteditems").ejListBox({ **allowDragAndDrop: true** });
        // simple Button creation 
        // to add list item to selection ListBox
        $("#Add").ejButton({
            size: "normal", click: "add",
            showRoundedCorner: true,
        });
        // to remove an list item from selection ListBox
        $("#Remove").ejButton({
            size: "normal", click: "remove",
            showRoundedCorner: true,
        });
    });
</script>


{% endhighlight %}



Run the above code example to render the following **ListBox** with **Drag and Drop** feature. **ListBox** with Drag and Drop list items across control is displayed in the following image. 



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img4.png" Caption=""%}

_Figure_ _4__: ListBox with Drag and Drop list items_

**Enable Multiple Selection** 

You can select multiple list items simultaneously in **ListBox** control, and move the multiple selected items to selection listbox. To select multiple items in a **ListBox**, set **allowMultiSelection** property for the **ListBox** as **“True”**.



{% highlight js %}

<script type="text/javascript">
    jQuery(function ($) {

        $("#select").ejListBox({
**allowDragAndDrop: true, allowMultiSelection: true**
        });
        $("#selecteditems").ejListBox({ allowDragAndDrop: true, });
        // simple Button creation 
        // to add list item to selection ListBox
        $("#Add").ejButton({
            size: "normal", click: "add",
            showRoundedCorner: true,
        });
        // to remove an list item from selection ListBox
        $("#Remove").ejButton({
            size: "normal", click: "remove",
            showRoundedCorner: true,
        });
    });
</script>


{% endhighlight %}



Run the above code example to render the following **ListBox** with **Multi-Selection** feature. **ListBox** control with **Multi-Selection** of list items is displayed as follows.



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img5.png" Caption=""%}

_Figure_ _5__: ListBox  with Multiple Selection of list items_

**Adding items to a Second ListBox**

You have to move the selected list item to the second **ListBox** using **addItem(value)** method. And remove existing item in the first **ListBox** using **removeItem()** method.

The following code sample explains how to add to an item to second **ListBox.**



{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#select").ejListBox();
        $("#selecteditems").ejListBox();
        // simple Button creation 
        // to add list item to selection ListBox
        $("#Add").ejButton({
            size: "normal", click: "add",
            showRoundedCorner: true,
        });
        // to remove an list item from selection ListBox
        $("#Remove").ejButton({
            size: "normal", click: "remove",
            showRoundedCorner: true,
        });
    });
    function add(e) {
        var firstListBox = $('#select').data("ejListBox");
        var selecteditems = firstListBox.getSelectedItems();
        var len = selecteditems.length;
        for (i = 0; i < len; i++) {
            var value = $(selecteditems[i]).html();
            selecteditems[i].remove();
            var target = $('#selecteditems').data("ejListBox");
            target.addItem(value);
        }
    }

    function remove(e) {
        var firstListBox = $('#selecteditems').data("ejListBox");
        var selecteditem = firstListBox.getSelectedItems();
        var len = selecteditem.length;
        for (i = 0; i < len; i++) {
            var value = $(selecteditems[i]).html();
            selecteditem[i].remove();
            var target = $('#select').data("ejListBox");
            target.addItem(value);
        }
    }
</script>


{% endhighlight %}



Run this code and you can see the output. Selected items from the first **ListBox** has been moved to Second **ListBox** using **addItem()** and **removeItem()** method and it is shown in the following figure.



{% include image.html url="/js/Listbox/Getting-Started_images/Getting-Started_img6.png" Caption=""%}

_Figure_ _6__: ListBox Selection moved to Second ListBox_

