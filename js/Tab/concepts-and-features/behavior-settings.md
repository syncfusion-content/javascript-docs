---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: Tab Control
documentation: ug
---

# Behavior Settings

**Close Button**

By default, **Tab** contents are rendered without **Close****Button**. You can add the **Close****Button** by setting the ‘**showCloseButton**’ property to ‘**true**’. When you move cursor over the **Tab** headers, the **Close****Button** is displayed.   

The following code example is used to render the **Tab** widget with **Close****Button**.

* Add the following **HTML** for simple **Tab** creation with **Close****Button**.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]//Add the following script for Tab Render with Close Button.&lt;script type="text/javascript"&gt;        $(function () {            $("#dishtype").ejTab({ showCloseButton: true });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with close button.



&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).ShowCloseButton(true).Render();}

&lt;/div&gt;



[ASPX]

 // Add the following code example to the corresponding ASPX page to render Tab with close button.



    &lt;ej:Tab ID="dishtype" runat="server" ShowCloseButton="true" Width="600px"&gt;

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





* The following screenshot illustrates the **Tab** with **Close****Button**. 

{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img1.png" Caption="Figure 24: Tab control with close button"%}{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img2.png" Caption="Figure 24: Tab control with close button"%}

**Orientation**

By default, **Tab** control renders in horizontal orientation. You can change the **Orientation** to vertical using the ‘**headerPosition**’ property. Using  this property, you can customize the header by ” **top**”,” **bottom**”, “**left**”, and  “**right**”.

The following code example is used to render the sub **Tab** widget in the vertical orientation. 

* Add the following **HTML** for **Tab** orientation.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script for Tab render with customized orientation.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ headerPosition: "left", height: "220px" });                                                  });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with customized orientation.

&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).HeaderPosition(HeaderPosition.Left).Height("220").Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with customized orientation.



    &lt;ej:Tab ID="dishtype" runat="server" HeaderPosition="Left" Width="600px"&gt;

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



* The following screenshot illustrates the sub **Tab** with vertical orientation. 

{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img3.png" Caption="Figure 25: Sub Tab customized orientation"%}{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img4.png" Caption="Figure 25: Sub Tab customized orientation"%}

**State Maintenance**

When the page gets refreshed or reloaded, the **Tab** state is changed (i.e.) the focus is moved to start **Tab**. You can maintain the state of the **Tab** by using ‘**enablePersistence**’ property. When this property is set to **‘true’,** it retains the state. 

The following code example is used to render the **Tab** widget with state maintenance. 

* Add the following **HTML** for **Tab****state****maintenance**.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script for Tab state maintenance.&lt;script type="text/javascript"&gt;        $(function () {                      $("#dishtype").ejTab({ enablePersistence: true });             });&lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab with state maintenance.

&lt;div style="width: 550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                    .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).EnablePersistence(true).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab with state maintenance.

    &lt;ej:Tab ID="dishtype" runat="server" EnablePersistence="true" Width="600px"&gt;

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





* The following screenshot illustrates the **Tab** with **State****maintenance**.

![](behavior-settings_images\behavior-settings_img5.png)![](behavior-settings_images\behavior-settings_img6.png)

_Figure_ _26__:_ _State before page refresh_



{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img7.png" Caption="Figure 27: State after page refresh"%}{% include image.html url="\js\Tab\concepts-and-features\behavior-settings_images\behavior-settings_img8.png" Caption="Figure 27: State after page refresh"%}

