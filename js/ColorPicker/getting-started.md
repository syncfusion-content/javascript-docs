---
layout: post
title: getting-started
description: getting started
platform: js
control: ColorPicker
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **ColorPicker** in your application with **JavaScript**, **ASP.NET MVC** and **ASP.NET**.

## Create your first ColorPicker in JavaScript

The **Essential JavaScript****ColorPicker** control provides you support for selecting the colors in different sources such as palettes, picker or custom palettes. You can also render the color value from control in three formats such as RGB, HSV and HEXCODE. 

* In this example, you can learn how to customize **ColorPicker** control in a category Application. 

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img1.png" Caption="Figure 1: ColorPicker Control"%}

In the following sections you can learn, How to:

* Create ColorPicker control

* Initialize the other widgets

* Add Value to ListBox Control

### Create ColorPicker Control

Use the following steps to create the **ColorPicker** control.

* Create an **HTML** file and add the following template to it for **ColorPicker** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
     <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

    <title>Getting Started Essential JS</title>
    <!-- Style sheet for default theme (flat azure) -->
    <link 
href="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"
rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
       <!—add the ColorPicker element here -->
</body>
</html>


{% endhighlight %}





* Add the input element to render **&lt;ColorPicker&gt;** control.



{% highlight html %}


<input type="text" id="CategoryColor" />



{% endhighlight %}



* Initialize **ColorPicker** element in **&lt;script&gt;** tag.



{% highlight js %}

<script>
    jQuery(function ($) {
        $("#CategoryColor").ejColorPicker({ value: "#278787" });       
    });        
</script>


{% endhighlight %}



Run the above code to render the following output.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img2.png" Caption="Figure 2: Default Colorpicker Control"%}

### Initialize the other widgets

To add the priority value to the **ListBox**, the text value is received from the input element and color for each priority is received by the **ColorPicker** control. To add each new priority value to the **ListBox** control click the **Add** button.

You can refer the following link for more information on creation of **ListBox**.
[http://help.syncfusion.com](http://help.syncfusion.com)

* The following code example is used to create the Priority form using **ListBox** control and **ColorPicker** control.



{% highlight html %}


<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <div class="frame">
                <div id="control">
                    <ul id="selectcheck">
                        <li><span class="color high"></span>High</li>
                        <li><span class="color normal"></span>Normal</li>
                        <li><span class="color low"></span>Low</li>
                    </ul>
                </div>
            </div>
        </div>
        <div id="Properties">
            <table class="prop-grid">
                <tr class="row">
                    <td class="column">Name
                    </td>
                    <td class="column">
                        <input type="text" id="categoryName" />
                    </td>
                </tr>
                <tr class="row">
                    <td class="column">Color
                    </td>
                    <td class="column">
                        <!--Colorpicker element-->
                        <input type="text" id="CategoryColor" /> 
                    </td>
                    <td class="column">
                        <!--Add button for add the new category-->
                        <input type="button" class="e-btn e-select" id="AddCategory" />
                    </td>
                </tr>
                <tr class="row">
                </tr>
            </table>
        </div>
    </div>
</div>


{% endhighlight %}



* Initialize the element in **&lt;script&gt;** tag.



{% highlight js %}

<script>
    var listBoxObj, colorObj;
    jQuery(function ($) {
        //initliaze the listbox with object creation
        listBoxObj = $("#selectcheck").ejListBox().data('ejListBox');
        //initliaze the colorpicker with object creation
        colorObj = $("#CategoryColor").ejColorPicker({ value: "#278787" }).data('ejColorPicker');
        //initliaze the button 
        $("#AddCategory").ejButton({ text: "Add", width: "82px", height: "21px" });
    });
</script>


{% endhighlight %}



* Add the following style section to align form fields. 



{% highlight css %}

<style>
    .content-container-fluid > .row {
        width: 410px;
        border: 1px solid #bbbcbb;
        padding: 16px;
        height: 272px;
    }

    .color.high {
        background-color: red;
    }

    .color.normal {
        background-color: green;
    }

    .color.low {
        background-color: blue;
    }

    .cols-sample-area {
        width: 205px;
    }

    .cols-sample-area, #Properties {
        display: inline-block;
        float: left;
    }

    #Properties #categoryName {
        width: 140px;
        height: 20px;
    }

    #Properties .column {
        display: inline-block;
        width: 45px;
        margin: 10px 0 0;
    }

    #Properties .row {
        padding: 10px 0px 5px 0px;
    }

    .color {
        width: 13px;
        height: 13px;
        border: 1px solid;
        display: inline-block;
        margin-right: 6px;
        margin-bottom: -3px;
    }
</style>


{% endhighlight %}



Run the above code to render the following output.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img3.png" Caption="Figure 3: Color Picker control"%}

### Add value with Selected Color 

You can add the value to **ListBox** with selected color by performing the button click event. The following script section defines the click event for the button element.

* Initialize the click event for the button element in **&lt;script&gt;** tag.



{% highlight js %}

<script>
        jQuery(function ($) {
        //reuse the previous section script block    
        //initliaze the button with click event
        $("#AddCategory").ejButton({ text: "Add", click: "addCategoryValue", width: "82px", height: "21px" });
        });
         //The following function used to add the new value to the listbox control
        function addCategoryValue() {
            if ($("#categoryName").val() !== "") {
                //To get the selected color from the colorpicker by using getValue()
                listBoxObj.addItem("<span class='color' style='background-color: " + colorObj.getValue() + "' ></span>" + $("#categoryName").val());
                $("#categoryName").val("");
            }
        }
</script>


{% endhighlight %}



The following screenshot illustrates the resultant output after you click **Add** button.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img4.png" Caption="Figure 4: Value from Color Picker control"%}

## Create your first ColorPicker in ASP.NET MVC

The **Essential ASP.NET MVC****ColorPicker** control provides support for selecting the colors in different sources such as palettes, picker or custom palettes. You can also render the color value from control in three formats such as RGB, HSV and HEXCODE. 

In this example, you can learn how to customize **ColorPicker** control in a category Application. 

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img5.png" Caption="Figure 5: ColorPicker Control"%}

In the following sections you can learn, How to:

* Create ColorPicker control

* Initialize the other widgets

* Add Value to ListBox Control

**Create ColorPicker Control**

Use the following steps to create the **ColorPicker** control.

* You can create a **MVC** Project and add necessary **Dll’s** and **Scripts** with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* Add the following code example to the corresponding view page for rendering the **ColorPicker** window.



**[CSHTML]**



@Html.EJ().ColorPicker("CategoryColor").Value("#278787")



Run this code to render the resultant output of the above steps.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img6.png" Caption="Figure 6: Default Colorpicker Control"%}

**Initialize the other widgets**

To add the priority value to the **ListBox**, the text value is obtained from the input element and color for each priority is received by **ColorPicker** control. To add each new priority value to **ListBox** control, click the **Add** button.

You can refer to the following link for more information on creation on **ListBox**

[http://help.syncfusion.com](http://help.syncfusion.com)



* The following code example is used to create the Priority form using **ListBox** control and **ColorPicker** control.



**[CSHTML]**

&lt;div class="content-container-fluid"&gt;

        &lt;div class="row"&gt;

            &lt;div class="sample-area"&gt;

                &lt;div class="frame"&gt;

                    &lt;div id="control"&gt;

                        &lt;ul id="ColorValues"&gt;

                            &lt;li&gt;&lt;span class="color high"&gt;</span>High</li>

                            &lt;li&gt;&lt;span class="color normal"&gt;</span>Normal</li>

                            &lt;li&gt;&lt;span class="color low"&gt;</span>Low</li>

                        &lt;/ul&gt;

                        @Html.EJ().ListBox("selectPriority").TargetID("ColorValues")

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;div id="Properties"&gt;

                &lt;table class="prop-grid"&gt;

                    &lt;tr class="row"&gt;

                        <td class="column">Name

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;input type="text" id="categoryName" /&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr class="row"&gt;

                        <td class="column">Color

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;!--Colorpicker element--&gt;

                            @Html.EJ().ColorPicker("CategoryColor").Value("#278787")

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;!--Add button for add the new category--&gt;                                @Html.EJ().Button("AddCategory").Text("Add").Width("82px").Height("28px").Type(ButtonType.Button).ClientSideEvents(events => events.Click("addCategoryValue"))

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr class="row"&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



Add the following style section to align form fields. 



**[CSS]**



&lt;style&gt;

    .content-container-fluid > .row {

        width: 410px;

        border: 1px solid #bbbcbb;

        padding: 16px;

        height: 272px;

    }



    .color.high {

        background-color: red;

    }



    .color.normal {

        background-color: green;

    }



    .color.low {

        background-color: blue;

    }



    .sample-area {

        width: 205px;

    }



    .sample-area, #Properties {

        display: inline-block;

        float: left;

    }



    #Properties #categoryName {

        width: 140px;

        height: 20px;

    }



    #Properties .column {

        display: inline-block;

        width: 45px;

        margin: 10px 0 0;

    }



    #Properties .row {

        padding: 10px 0px 5px 0px;

    }



    .color {

        width: 13px;

        height: 13px;

        border: 1px solid;

        display: inline-block;

        margin-right: 6px;

        margin-bottom: -3px;

    }

&lt;/style&gt;



Initialize the element in **&lt;script&gt;** tag.



**[JavaScript]**

&lt;script&gt;

    var listBoxObj, colorObj;

    jQuery(function ($) {

        //initliaze the listbox with object creation

        listBoxObj = $("#selectPriority").data('ejListBox');

        //initliaze the colorpicker with object creation

        colorObj = $("#CategoryColor").data('ejColorPicker');        

    });

&lt;/script&gt;



Run the above code to render the following output.



{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img7.png" Caption="Figure 7: Color Picker control"%}

**Add value to ListBox Control** 

You can add the value to **ListBox** with selected color by performing the button click event. The following script section define the click event for the button element.

* Initialize the click event to button element in **&lt;script&gt;** tag.



**[JavaScript]**

&lt;script&gt;

        jQuery(function ($) {

        //reuse the previous section script block            

         //The following function used to add the new value to the listbox control

        function addCategoryValue() {

            if ($("#categoryName").val() !== "") {

                //To get the selected color from the colorpicker by using getValue()

                listBoxObj.addItem("&lt;span class='color' style='background-color: " + colorObj.getValue() + "' &gt;&lt;/span&gt;" + $("#categoryName").val());

                $("#categoryName").val("");

            }

        }

&lt;/script&gt;



The following screenshot illustrates the resultant output after you click **Add** button.



{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img8.png" Caption="Figure 8: Value from Color Picker control"%}

## Create your first ColorPicker in ASP.NET

The **Essential ASP.NET WebForms****ColorPicker** control provides you support for selecting the colors in different sources such as palettes, picker or custom palettes. You can also rend the color value from control in three formats such as RGB, HSV and HEXCODE. 

In this example, you can learn how to customize **ColorPicker** control in a category Application. 

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img9.png" Caption="Figure 9: ColorPicker Control"%}

In the following sections you can learn, How to:

* Create ColorPicker control

* Initialize the other widgets

* Add Value to ListBox Control

**Create ColorPicker Control**

Use the following steps to create the **ColorPicker** control.

* Create a **WebForms** Project and add necessary **Dll’s** and **scripts** with the help of the given [WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* Create the **ASPX** page and add the following code to it for **ColorPicker** creation.



**[ASPX]**

&lt;ej:ColorPicker runat="server" ID="CategoryColor" Value="#278787"&gt; &lt;/ej:ColorPicker&gt;



Run this code to render the resultant output of the above steps.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img10.png" Caption="Figure 10: Default Colorpicker control"%}

**Initialize the other widgets**

To add the priority value to the **ListBox**, the text value is obtained from the input element and color for each priority is received by **ColorPicker** control. To add each new priority value to **ListBox** control, click the **Add** button.

You can refer the following link for more information on creation on **ListBox**

[http://help.syncfusion.com](http://help.syncfusion.com)

* The following code example is used to create the Priority form using **ListBox** control and **ColorPicker** control.




**[ASPX]**

&lt;div class="content-container-fluid"&gt;

        &lt;div class="row"&gt;

            &lt;div class="sample-area"&gt;

                &lt;div class="frame"&gt;

                    &lt;div id="control"&gt;

                        &lt;ul id="ColorValues"&gt;

                            &lt;li&gt;&lt;span class="color high"&gt;</span>High</li>

                            &lt;li&gt;&lt;span class="color normal"&gt;</span>Normal</li>

                            &lt;li&gt;&lt;span class="color low"&gt;</span>Low</li>

                        &lt;/ul&gt;

                        &lt;ej:ListBox ID="selectPriority" runat="server" TargetID="ColorValues"&gt;&lt;/ej:ListBox&gt;

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;div id="Properties"&gt;

                &lt;table class="prop-grid"&gt;

                    &lt;tr class="row"&gt;

                        <td class="column">Name

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;input type="text" id="categoryName" /&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr class="row"&gt;

                        <td class="column">Color

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;!--Colorpicker element--&gt;

                            &lt;ej:ColorPicker ID="CategoryColor" runat="server" Value="#278787"&gt;&lt;/ej:ColorPicker&gt;                            

                        &lt;/td&gt;

                        &lt;td class="column"&gt;

                            &lt;!--Add button for add the new category--&gt;

                            &lt;ej:Button ID="AddCategory" runat="server" Text="Add" Width="82px" Type="Button" Height="21px" ClientSideOnClick="addCategoryValue"&gt; &lt;/ej:Button&gt;                            

                        &lt;/td&gt;

                    &lt;/tr&gt;                    

                &lt;/table&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



Add the following style section to align form fields. 



**[CSS]**

&lt;style&gt;

    .content-container-fluid > .row {

        width: 410px;

        border: 1px solid #bbbcbb;

        padding: 16px;

        height: 272px;

    }



    .color.high {

        background-color: red;

    }



    .color.normal {

        background-color: green;

    }



    .color.low {

        background-color: blue;

    }



    .sample-area {

        width: 205px;

    }



    .sample-area, #Properties {

        display: inline-block;

        float: left;

    }



    #Properties #categoryName {

        width: 140px;

        height: 20px;

    }



    #Properties .column {

        display: inline-block;

        width: 45px;

        margin: 10px 0 0;

    }



    #Properties .row {

        padding: 10px 0px 5px 0px;

    }



    .color {

        width: 13px;

        height: 13px;

        border: 1px solid;

        display: inline-block;

        margin-right: 6px;

        margin-bottom: -3px;

    }

&lt;/style&gt;



Initialize the element in **&lt;script&gt;** tag.



**[JavaScript]**

&lt;script&gt;

    var listBoxObj, colorObj;

    jQuery(function ($) {

        //initliaze the listbox with object creation

        listBoxObj = $("#selectPriority").data('ejListBox');

        //initliaze the colorpicker with object creation

        colorObj = $("#CategoryColor").data('ejColorPicker');        

    });

&lt;/script&gt;





Run the above code to render the following output.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img11.png" Caption="Figure 11: Color Picker control"%}

**Add value to ListBox Control** 

You can add the value to **ListBox** with selected color by performing the button click event. The following script section define the click event for the button element.

* Initialize the click event to button element in **&lt;script&gt;** tag.



**[JavaScript]**

&lt;script&gt;

        jQuery(function ($) {

        //reuse the previous section script block            

         //The following function used to add the new value to the listbox control

        function addCategoryValue() {

            if ($("#categoryName").val() !== "") {

                //To get the selected color from the colorpicker by using getValue()

                listBoxObj.addItem("&lt;span class='color' style='background-color: " + colorObj.getValue() + "' &gt;&lt;/span&gt;" + $("#categoryName").val());

                $("#categoryName").val("");

            }

        }

&lt;/script&gt;





The following screenshot illustrates the resultant output after you click **Add** button.

{% include image.html url="\js\ColorPicker\getting-started_images\getting-started_img12.png" Caption="Figure 12: Value from Color Picker control"%}

