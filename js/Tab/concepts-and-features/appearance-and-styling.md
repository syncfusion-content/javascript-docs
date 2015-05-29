---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: Tab Control
documentation: ug
---

# Appearance and Styling

**Header Image Customization**

To set the **Tab** header image for each **Tab** item you can specify image in &lt;span&gt; tag element during the **Tab** header declaration time.

In **MVC**, to set the **Tab** header image for each **Tab** item you need to specify image in “**ImageCssClass”** property during the **TabItem** declaration.

The following code example is used to add the header image for the root **Tab** header element. 

* Add the following **HTML** to render **Tab** with header image.



<table>
<tr>
<td>
[HTML] &lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;&lt;span class="dish pizzaImg"&gt;&lt;/span&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;&lt;span class="dish sandwichImg"&gt;&lt;/span&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script for Tab render with customizes header image.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab();            });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with header image.

 &lt;div id="dishtab" style="width:550px"&gt;

    &lt;ul&gt;

        &lt;li&gt;&lt;span class="dish pizzaImg"&gt;&lt;/span&gt;<a href="#pizzatype">Pizza Type</a>&lt;/li&gt;

        &lt;li&gt;&lt;span class="dish sandwichImg"&gt;&lt;/span&gt;<a href="#sandwichtype">Sandwich Type</a>&lt;/li&gt;

    &lt;/ul&gt;

    &lt;div id="pizzatype" style="background-color: #F5F5F5"&gt;

        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

    &lt;/div&gt;

    &lt;div id="sandwichtype" style="background-color: #F5F5F5"&gt;        

        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

    &lt;/div&gt;

    @Html.EJ().Tab("dishtab")

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with header image.

     &lt;ej:Tab ID="dishtype" runat="server" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" ImageCssClass="dish pizzaImg" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" ImageCssClass="dish sandwichImg" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;







* Add following **CSS** for header image customization.

{% highlight css %}

[CSS]
<style type="text/css" class="cssStyles">
        .dish {
            display: inline-block;
            vertical-align: middle;
            margin: 0px -9px 0px 9px;           
        }
        .pizzaImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_chicken-delite.png") no-repeat;
            height: 25px;
            width: 25px;
        }
        .sandwichImg, .pastaImg {
            height: 25px;
            width: 25px;
        }
        .sandwichImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-fresh.png") no-repeat;
        }
</style> 


{% endhighlight %}

* The following screenshot illustrates the **Tab** with the customized header image. 

![](appearance-and-styling_images\appearance-and-styling_img1.png)![](appearance-and-styling_images\appearance-and-styling_img2.png)

_Figure_ _28__:_ _Header Image Customization_

**Rounded corner**

By enabling ‘**showRoundedCorner’** property, you can customize the shape of the **Tab** widget from regular rectangular shape to rounded rectangle shape that is set to ‘**false**’ by default. 

The following code example is used to render the **Tab** widget with **Rounded C****corner**.

* Add the following **HTML** to render **Tab** with rounder corner.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script to render Tab with rounded corner.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ showRoundedCorner: true });        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with rounded corner.



&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).ShowRoundedCorner(true).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with rounded corner.

    &lt;ej:Tab ID="dishtype" runat="server" ShowRoundedCorner="true" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





* The following screenshot illustrates the **Tab** with Rounded corner.

![](appearance-and-styling_images\appearance-and-styling_img3.png)![](appearance-and-styling_images\appearance-and-styling_img4.png)

_Figure_ _29__:_ _Tab with rounded corner_

**Enable/Disable**

You can enable or disable the **Tab** widget by ‘**enabled’** property. By default, the property set to ‘**true**’**.**

The following code example is used to render the **Tab** widget with enable/disable.

* Add the following **HTML** to render **Tab** with enable/disable.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with disabled format.&lt;script type="text/javascript"&gt;    $(function () {        $("#dishtype").ejTab({ enabled: false });    });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with Enable/Disable format.



&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).Enabled(false).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with Enable/Disable format.



    &lt;ej:Tab ID="dishtype" runat="server" Enabled="false" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





* The following screenshot illustrates the **Tab** with disabled format.

![](appearance-and-styling_images\appearance-and-styling_img5.png)![](appearance-and-styling_images\appearance-and-styling_img6.png)

_Figure_ _30__:_ _Tab with_ _disabled format_

**Enabling Reload Icon**

Without refresh/reload the whole page, you can reload a particular **Tab** using **Reload** icon. The **Reload** icon is appeared at right corner of the **Tab** by enabling the property ‘**showReloadIcon**’ to ‘**true**’. When you move cursor over the **Tab** headers, the **Reload** icon is displayed. By default the property value is set to ‘**false**’.   

The following code example is used to render the **Tab** widget with **Reload** icon.

* Add the following **HTML** to render **Tab** with **Reload** icon.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with Reload icon.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ showReloadIcon: true });        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with reload icon.



&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).ShowReloadIcon(true).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with reload icon.

    &lt;ej:Tab ID="dishtype" runat="server" ShowReloadIcon="true" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





* The following screenshot illustrates the **Tab** with **Reload** icon.

![](appearance-and-styling_images\appearance-and-styling_img7.png)![](appearance-and-styling_images\appearance-and-styling_img8.png)

_Figure_ _31__:_ _Tab with reload icon_



**Collapsible Tabs**

You can collapse the **Tab** content by enabling the ‘**collapsible’** property to ‘**true**’. When the property is set to ‘**true**’ then click the active **Tab** header, the **Tab** contents are hided. By default, the property value is set to ‘**false**’.

The following code example is used to render the **Tab** widget with customized collapsible mode.

* Add the following **HTML** to render **Tab** with customized collapsible mode.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with customized collapsible mode.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ collapsible: true });        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with collapsible mode.

&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).Collapsible(true).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with collapsible mode.

    &lt;ej:Tab ID="dishtype" runat="server" Collapsible="true" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;



* The following screenshot illustrates the **Tab** with customized collapsible mode.

![](appearance-and-styling_images\appearance-and-styling_img9.png)![](appearance-and-styling_images\appearance-and-styling_img10.png)

_Figure_ _32__:_ _Tab with_ _customized collapsible mode_

**Adjusting Tab Size**

**Height Adjust Mode and Height**

The height of the **Tab** widget is customized by ‘**height**’ property. The **Tab** widget height depends on ‘**heightAdjustMode**’ property. Using the **heightAdjustMode** property, you can adjust height by “**content**”, “**auto**”, “**fill**”. By default the **heightAdjustMode** is set as **content**.

The following code example is used to render the **Tab** widget with customized height and height adjust mode.

* Add the following **HTML** to render **Tab** with customized height and height adjust mode.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with customized height and height adjust mode.&lt;script type="text/javascript"&gt;       $(function () {                    $("#dishtype").ejTab({ heightAdjustMode:"fill", height:"300px"});        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with customized height and height adjust mode.



&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

              data.Add().ID("sandwichtype").Text("Sandwich Type")

                  .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).HeightAdjustMode(HeightAdjustMode.Fill).Height("300px").Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with customized height and height adjust mode.



    &lt;ej:Tab ID="dishtype" runat="server" HeightAdjustMode="Fill" Height="300px" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;



* The following screenshot illustrates the **Tab** with customized height and height adjust mode.

![](appearance-and-styling_images\appearance-and-styling_img11.png)![](appearance-and-styling_images\appearance-and-styling_img12.png)

_Figure_ _33__:_ _Tab with_ _customized height and height adjust mode_



**Width**

The **width** of the **Tab** widget is customized by using ‘**width**’ property that accepts only the pixel values.

The following code example is used to render the **Tab** widget with customized width.

* Add the following **HTML** to render **Tab** with customized width.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with customized width.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ width:"450px" });        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with customized width.



&lt;div&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).Width("450").Render();}

&lt;/div&gt;



[ASPX]

//Add the following code example to the corresponding ASPX page to render Tab with customized width.



    &lt;ej:Tab ID="dishtype" runat="server" Width="450px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





* The following screenshot illustrates the **Tab** with customized width.

![](appearance-and-styling_images\appearance-and-styling_img13.png)![](appearance-and-styling_images\appearance-and-styling_img14.png)

_Figure_ _34__:_ _Tab with_ _customized width_

**Theme**

**Tab** control’s style and appearance are controlled based on **CSS** classes. In order to apply styles to the **Tab** control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 13 themes support available for **Tab** control namely

* default-theme

* bootstrap-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

**Custom styles**

The style of the **Tab** widget is customized by ‘**cssClass**’ property. 

The following code example is used to render the **Tab** widget with customized style.

* Add the following **HTML** to render **Tab** with customized style.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with customized style.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ cssClass: "custom" });        });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with customized style.



&lt;div&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).CssClass("custom").Render();}

&lt;/div&gt;





[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with customized style.

    &lt;ej:Tab ID="dishtype" runat="server" CssClass="custom"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





* Add the following styles

{% highlight css %}

**[CSS]**
<style type="text/css">
        .custom {
            width:650px;
        }
    </style>


{% endhighlight %}

* The following screenshot illustrates the **Tab** with customized style.

![](appearance-and-styling_images\appearance-and-styling_img15.png)![](appearance-and-styling_images\appearance-and-styling_img16.png)

_Figure_ _35__:_ _Tab with_ _customized style_

