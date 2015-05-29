---
layout: post
title: getting-started
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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\firstfinal.PNG](getting-started_images\getting-started_img1.png)

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
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"></script>
</head>
<body>
    <!—add the ListBox element here -->
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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\emptylist.PNG](getting-started_images\getting-started_img2.png)

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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\initial.PNG](getting-started_images\getting-started_img3.png)

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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\dragndrop.png](getting-started_images\getting-started_img4.png)

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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\multiselect.PNG](getting-started_images\getting-started_img5.png)

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



![C:\Users\Rajaveni\Desktop\docs\skype simulator\firstfinal.PNG](getting-started_images\getting-started_img6.png)

_Figure_ _6__: ListBox Selection moved to Second ListBox_

## Create your first ListBox in MVC

Here you can learn how to customize **ListBox** in Contact Selection tool. This allows you display the list of contacts, to select and move them to the next **ListBox** that has the selected items. The following example illustrates simulator of Group Creation tool like Skype messenger.

The following screenshot demonstrates the functionality of **ListBox** with **Multi-Selection** and **Drag and Drop** features.



![F:\UG\screen shot\1.PNG](getting-started_images\getting-started_img7.png)

_Figure_ _7__: Skype Group creation tool Simulator using ListBox_

In the above screenshot, you can select a list item from the first **ListBox** widget. After you select the item, you can move the selected item to the second **ListBox** widget. 

**Create a ListBox Widget**

**Essential****JavaScript****ListBox** control renders with built-in features.

The following steps are used to create **ListBox** control.  

1. You can create an **MVC Project** and add necessary **Dll** and script with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code in your **view** page to render **ListBox** controls.



**[view]**    

&lt;div id="sample"&gt;

    &lt;h5&gt;

        <b>Add people</b>&lt;/h5&gt;

    &lt;p&gt;

        Choose a contact and click move button to add in group

    &lt;/p&gt;

    &lt;br /&gt;

    &lt;div id="control"&gt;

        &lt;div id="container1"&gt;

            &lt;p&gt;

                Contacts List</p>

            @Html.EJ().ListBox("list1")

        &lt;/div&gt;

        &lt;div id="container2"&gt;

            &lt;p&gt;

                People in this group</p>

            @Html.EJ().ListBox("list2")

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;





3. Add the following style section for the **ListBox** controls alignment. 



**[Css]**

&lt;style type="text/css" class="cssStyles"&gt;

    #control {

        height: 350px;

        width: 500px;

        padding: 25px;

        background-color: #f7f7f7;

        display: flex;

    }

    #sample {

        height: 472px;

        width: 600px;

    }

    #list2_container {

        float: right;

    }

    #list1_container {

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

    #form1 {

        padding: 25px;

    }



&lt;/style&gt;



4. Run this code to render an empty **ListBox** control.



![F:\UG\screen shot\2.PNG](getting-started_images\getting-started_img8.png)

_Figure_ _8__: Render ListBox with &lt;ul&gt;&lt;/ul&gt; element_

**Configure ListBox with Items**

To populate items inside **ListBox**, you have to add list items inside **&lt;ul&gt;** as **&lt;li&gt;&lt;/li&gt;** elements. The **TargetID** property is used to get the list items from the target. The Id of the **ul** that has the list items is given as the TargetID. Include the following **&lt;ul&gt;**, **&lt;li&gt;** elements in your sample.



**[view]**    

&lt;div id="sample"&gt;

    &lt;h5&gt;

        <b>Add people</b>&lt;/h5&gt;

    &lt;p&gt;

        Choose a contact and click move button to add in group

    &lt;/p&gt;

    &lt;br /&gt;

    &lt;div id="control"&gt;

        &lt;div id="container1"&gt;

            &lt;p&gt;

                Contacts List</p>

            @Html.EJ().ListBox("list1").TargetID("select")

            &lt;ul id="select"&gt;

                &lt;li&gt;

                    &lt;img src="~/images/listbox/busy.png" alt="Categorize" /&gt;

                    Nancy</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/busy.png" alt="Done" /&gt;

                    Andrew</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Flag" /&gt;

                    Janet</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/away.png" alt="Forward" /&gt;

                    Margaret</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/away.png" alt="Move" /&gt;

                    Michael</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="E-mail" /&gt;

                    Robert</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Meeting" /&gt;

                    Laura</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Reply" /&gt;

                    Anne</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/away.png" alt="Move" /&gt;

                    Suyama</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="E-mail" /&gt;

                    Callahan</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Meeting" /&gt;

                    Peacock</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Reply" /&gt;

                    Fuller</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Reply" /&gt;

                    Davolio</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Reply" /&gt;

                    Dodsworth</li>

                &lt;li&gt;

                    &lt;img src="~/images/listbox/avail.png" alt="Reply" /&gt;

                    Louis</li>

            &lt;/ul&gt;

        &lt;/div&gt;

        &lt;div class="middlebuttons"&gt;

            @Html.EJ().Button("Add").Text(">>").ShowRoundedCorner(true).ClientSideEvents(e => e.Click("add"))

            &lt;br /&gt;

            &lt;br /&gt;

            @Html.EJ().Button("Remove").Text("&lt;&lt;").ShowRoundedCorner(true).ClientSideEvents(e =&gt; e.Click("remove"))

        &lt;/div&gt;

        &lt;div id="container2"&gt;

            &lt;p&gt;

                People in this group</p>

            @Html.EJ().ListBox("list2")

            &lt;ul id="selecteditems"&gt;

            &lt;/ul&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;





Run the above code to render **ListBox** with list items rendered inside **ListBox. ListBox** with Contact list items is shown as follows.



![F:\UG\screen shot\3.PNG](getting-started_images\getting-started_img9.png)

_Figure_ _9__: ListBox with Contact list items_

**Enable Drag and Drop** 

You can drag an item from a **ListBox** and drop it in droppable element.To drag and drop a list item across controls or within a control, you have to set the **AllowDragAndDrop** property as “**True**”. 



**[view]**    

@Html.EJ().ListBox("list1").TargetID("select").**AllowDragAndDrop**(true)

@Html.EJ().ListBox("list2").**AllowDragAndDrop**(true)



Run the above code example to render the following **ListBox** with **Drag and drop** feature. **ListBox** with Drag and Drop list items across control is as follows:



![F:\UG\screen shot\4.png](getting-started_images\getting-started_img10.png)

_Figure_ _10__: ListBox with Drag and Drop list items_

**Enable Multiple Selection** 

You can select multiple list items simultaneously in **ListBox** control, and move the multiple, selected items to the selection **ListBox**. To select multiple items in a **ListBox**, set the **AllowMultiSelection** property for the **ListBox** as **“True”**.



**[view]**    

@Html.EJ().ListBox("list1").TargetID("select").**AllowMultiSelection**(true)

.AllowDragAndDrop(true)



Run the above code example to render the following **ListBox** with Multiple selection feature. **ListBox** control with Multiple Selection of list items is as follows.



![F:\UG\screen shot\5.PNG](getting-started_images\getting-started_img11.png)

_Figure_ _11__: ListBox  with Multiple Selection of list items_

**Add items to a Second ListBox**

You have to move the selected list items to the second **ListBox** using **addItem(value)** method and remove existing item in the first **ListBox** using **removeItem()** method.

The following code sample explains how to add an item to a second **ListBox.**



**[JS]**

&lt;script type="text/javascript"&gt;

function add(e) {

        var firstListBox = $('#list1').data("ejListBox");

        var selecteditems = firstListBox.getSelectedItems();

        var len = selecteditems.length;

        for (i = 0; i < len; i++) {

            var value = $(selecteditems[i]).html();

            selecteditems[i].remove();

            var target = $('#list2').data("ejListBox");

            target.addItem(value);

        }

    }

    function remove(e) {

        var firstListBox = $('#list2').data("ejListBox");

        var selecteditem = firstListBox.getSelectedItems();

        var len = selecteditem.length;

        for (i = 0; i < len; i++) {

            var value = $(selecteditem[i]).html();

            selecteditem[i].remove();

            var target = $('#list1').data("ejListBox");

            target.addItem(value);

        }

    }

&lt;/script&gt;



Run this code and you can see the output. Selected items from the first **ListBox** have been moved to second **ListBox** using **addItem()** and **removeItem()** method and it is displayed in the following figure.



![F:\UG\screen shot\1.PNG](getting-started_images\getting-started_img12.png)

_Figure_ _12__: ListBox Selection moved to Second ListBox_

## Create your first ListBox in ASP.NET

Here you can learn how to customize **ListBox** in Contact Selection tool. This allows you display the list of contacts, to select and move them to the next **ListBox** that has the selected items. The following example illustrates simulator of Group Creation tool like Skype messenger.

The following screenshot demonstrates the functionality of **ListBox** with **Multi-Selection** and **Drag and Drop** features.



![](getting-started_images\getting-started_img13.png)

_Figure_ _13__: Skype Group creation tool Simulator using ListBox_

In the above screenshot, you can select a list item from the first **ListBox** widget. After you select the item, you can move the selected item to the second **ListBox** widget. 

**Create ListBox Widget**

**Essential****ASP.NET****ListBox** widget renders with built-in features.

The following steps are used to create **ListBox** control.  

1. You can create a **WEB Project** and add necessary **Dll** and script with the help of the given [ASP-Getting Started Documentation.](http://help.syncfusion.com/ug/js/documents/creatingyourfirstapp.htm)

2. Add the following code to the corresponding **ASPX** page to render the **ListBox**.



**[ASPX]**

&lt;div id="sample"&gt;

    &lt;h5&gt;<b>Add people</b>&lt;/h5&gt;

    <h5>Choose a contact and click move button to add in group &lt;/h5&gt;

    &lt;div id="control"&gt;

        &lt;div id="container1"&gt;

            Contacts List

            &lt;ej:listbox id="select" runat="server"&gt;&lt;/ej:listbox&gt;

        &lt;/div&gt;

        &lt;div class="middlebuttons"&gt;



            &lt;ej:button id="Add" runat="server" type="Button" text="&gt;>" size="Normal" ShowRoundedCorner="true">&lt;/ej:button&gt;

            &lt;br /&gt;

            &lt;br /&gt;

            &lt;ej:button id="Remove" runat="server" type="Button" text="&lt;&lt;" size="Normal" ShowRoundedCorner="true"&gt;&lt;/ej:button&gt;

        &lt;/div&gt;

        &lt;div id="container2"&gt;

            People in this group

              &lt;ej:listbox id="selecteditems" runat="server"&gt; &lt;/ej:listbox&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



3. Add the following style section to the corresponding **ASPX** page for **ListBox** widgets alignment.



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

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

&lt;/style&gt;



4. Run the above code to render the resultant output.



![](getting-started_images\getting-started_img14.png)

_Figure_ _14__: Render ListBox with &lt;ul&gt;&lt;/ul&gt; element_

**Configure ListBox with Items**

To populate items inside **ListBox**, you have to add the list items inside **&lt;ul&gt;** as **&lt;li&gt;&lt;/li&gt;** elements. Include the following **&lt;li&gt;** elements in your sample.



**[ASPX]**

&lt;div id="sample"&gt;

    &lt;h5&gt;<b>Add people</b>&lt;/h5&gt;

    <h5>Choose a contact and click move button to add in group &lt;/h5&gt;

    &lt;div id="control"&gt;

        &lt;div id="container1"&gt;

            Contacts List

            &lt;ej:listbox id="select" runat="server" targetid="icon"&gt;  &lt;/ej:listbox&gt;

            &lt;ul id="icon"&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/busy.png" alt="busy" />Nancy

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/busy.png" alt="busy" />Andrew

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="busy" />Janet



                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Margaret

                &lt;/li&gt;



                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Michael

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Robert

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Laura

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Anne

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Suyama

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Callahan

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Peacock

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Fuller

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Davolio

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Dodsworth

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Louis

                &lt;/li&gt;



            &lt;/ul&gt;

        &lt;/div&gt;

        &lt;div class="middlebuttons"&gt;



            &lt;ej:button id="Add" runat="server" type="Button" text="&gt;>" size="Normal" ShowRoundedCorner="true">&lt;/ej:button&gt;

            &lt;br /&gt;

            &lt;br /&gt;

            &lt;ej:button id="Remove" runat="server" type="Button" text="&lt;&lt;" size="Normal" ShowRoundedCorner="true"&gt;&lt;/ej:button&gt;

        &lt;/div&gt;

        &lt;div id="container2"&gt;

            People in this group



                      &lt;ej:listbox id="selecteditems" runat="server"&gt; &lt;/ej:listbox&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt; 



Run the above code to render **ListBox. ListBox** with Contact list items is shown as follows.



![](getting-started_images\getting-started_img15.png)

_Figure_ _15__: ListBox with Contact list items_

**Enable Drag and Drop**

You can drag an item from a **ListBox** and drop it in droppable element.To drag and drop a list item across controls or within a control, you have to set the **AllowDragAndDrop** property as “**True**”. 



**[ASPX]**

&lt;ej:listbox id="select" runat="server" targetid="icon" AllowDragandDrop="true"&gt;  &lt;/ej:listbox&gt;



&lt;ej:listbox id="selecteditems" AllowDragAndDrop="true" runat="server"&gt; &lt;/ej:listbox&gt;





Run the above code example to render the following **ListBox** with **Drag and drop** feature. **ListBox** with Drag and Drop list items across controls is as follows.



![](getting-started_images\getting-started_img16.png)

_Figure_ _16__: ListBox with Drag and Drop list items_

**Enable Multiple Selection** 

You can select multiple list items simultaneously in **ListBox** control, and move the multiple, selected items to the selection **ListBox**. To select multiple items in a **ListBox**, set the **AllowMultiSelection** property for the **ListBox** as **“True”**.



**[ASPX]**

&lt;ej:listbox id="select" runat="server" targetid="icon" AllowDragAndDrop="true" AllowMultiSelection="true"&gt;  &lt;/ej:listbox&gt;



&lt;ej:listbox id="selecteditems" AllowDragAndDrop="true" AllowMultiSelection="true" runat="server"&gt; &lt;/ej:listbox&gt;





Run the above code example to render the following **ListBox** with **Multiple selection** feature. **ListBox** control with Multiple Selection of list items is displayed as follows.



![](getting-started_images\getting-started_img17.png)

_Figure_ _17__: ListBox  with Multiple Selection of list items_

**Add items to a Second ListBox**

You have to move the selected list items to the second **ListBox** using **addItem(value)** method and remove existing item in the first **ListBox** using **removeItem()** method.

The following code sample explains how to add an item to a second **ListBox.**

1. Add the following code to the corresponding **ASPX** page to render **ListBox**.



**[ASPX]**

&lt;div id="sample"&gt;

    &lt;h5&gt;<b>Add people</b>&lt;/h5&gt;

    <h5>Choose a contact and click move button to add in group &lt;/h5&gt;

    &lt;div id="control"&gt;

        &lt;div id="container1"&gt;

            Contacts List

            &lt;ej:listbox id="select" runat="server" targetid="icon" AllowDragAndDrop="true" AllowMultiSelection="true"&gt;  &lt;/ej:listbox&gt;

            &lt;ul id="icon"&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/busy.png" alt="busy" />Nancy

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/busy.png" alt="busy" />Andrew

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="busy" />Janet



                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Margaret

                &lt;/li&gt;



                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Michael

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Robert

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Laura

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Anne

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/away.png" alt="away" />Suyama

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Callahan

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Peacock

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Fuller

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Davolio

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Dodsworth

                &lt;/li&gt;

                &lt;li&gt;

                    <img src="../images/Listbox/avail.png" alt="avail" />Louis

                &lt;/li&gt;



            &lt;/ul&gt;

        &lt;/div&gt;

        &lt;div class="middlebuttons"&gt;



            &lt;ej:button id="Add" runat="server" type="Button" text="&gt;>" size="Normal" ShowRoundedCorner="true" **ClientSideOnClick="add**">&lt;/ej:button&gt;

            &lt;br /&gt;

            &lt;br /&gt;

            &lt;ej:button id="Remove" runat="server" type="Button" text="&lt;&lt;" size="Normal" ShowRoundedCorner="true" ClientSideOnClick="remove"&gt;**&lt;/ej:button&gt;**

        &lt;/div&gt;

        &lt;div id="container2"&gt;

            People in this group

                              &lt;ej:listbox id="selecteditems" AllowDragAndDrop="true" AllowMultiSelection="true" runat="server"&gt; &lt;/ej:listbox&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;





2. Add the mentioned code to the corresponding **ASPX** page to add an item to a second **ListBox.**



**[JavaScript]**



&lt;script type="text/javascript"&gt;

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

&lt;/script&gt;





3. Add the following style section to the corresponding **ASPX** page for **ListBox** widgets alignment.



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

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

&lt;/style&gt;



Run this code and you can see the output. Selected items from the first **ListBox** has been moved to Second **ListBox** using **addItem()** and **removeItem()** method and it is shown in the following figure.



****![](getting-started_images\getting-started_img18.png)

_Figure_ _18__: ListBox Selection moved to Second ListBox_

