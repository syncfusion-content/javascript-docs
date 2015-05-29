---
layout: post
title: scroll-support
description: scroll support
platform: js
control: Tab Control
documentation: ug
---

# Scroll Support

**Tab** control provides you scrolling support on Tab items to display a larger number of tabs with scroll buttons to get rid of the extending page size. The enabled Scroll buttons can be used to traverse through the elements.

By default, **Tab** header is rendered without scroll button. You can add the scroll button by setting the "**enableTabScroll**" property to "**true**". When you move the cursor over the **Tab** header the scroll button is displayed.   



You can use the following code example to render the **Tab** widget with scroll button.

* Add the following **HTML** code to create a simple Tab with scroll button.



<table>
<tr>
<td>
[HTML]&lt;div style="width: 500px; padding: 50px;"&gt;    &lt;div id="dishtype"&gt;        &lt;ul&gt;            &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;            &lt;li&gt;<a href="#pasta">Pasta Menu</a>&lt;/li&gt;            &lt;li&gt;<a href="#burger">Burger Menu</a>&lt;/li&gt;            &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;            &lt;li&gt;<a href="#spaghetti">Spaghetti Menu</a>&lt;/li&gt;            &lt;li&gt;<a href="#ramen">Ramen Menu</a>&lt;/li&gt;        &lt;/ul&gt;        &lt;div id="pizza" style="background-color: #F5F5F5"&gt;            &lt;!--Food item description--&gt;            &lt;p&gt;                Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;        &lt;div id="pasta" style="background-color: #F5F5F5"&gt;            &lt;!--dish description--&gt;            &lt;p&gt;                Pasta cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;        &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;            &lt;!--dish description--&gt;            &lt;p&gt;                Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;        &lt;div id="burger" style="background-color: #F5F5F5"&gt;            &lt;!--dish description--&gt;            &lt;p&gt;                Burger cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;        &lt;div id="spaghetti" style="background-color: #F5F5F5"&gt;            &lt;!--dish description--&gt;            &lt;p&gt;                Spaghetti cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;        &lt;div id="ramen" style="background-color: #F5F5F5"&gt;            &lt;!--dish description--&gt;            &lt;p&gt;                Ramen cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script to render Tab control    &lt;script type="text/javascript"&gt;        $(function () {            $("#dishtype").ejTab({                enableTabScroll: true            });        });		    &lt;/script&gt;</td></tr>
</table>


[CHTML]

@*Add the following code example to the corresponding CSHTML page to render Tab with scroll button.*@

&lt;div style="width: 550px"&gt;

            @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("pastatype").Text("Pasta Type")

                   .ContentTemplate(@<div>Pasta cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("burgertype").Text("Burger Type")

                   .ContentTemplate(@<div>Burger cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("spaghettitype").Text("Spaghetti Type")

                   .ContentTemplate(@<div>Spaghetti cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

               data.Add().ID("ramentype").Text("Ramen Type")

                   .ContentTemplate(@<div>Ramen cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/div&gt;);

           }).EnableTabScroll(true).Render();}

        &lt;/div&gt;



[ASPX]

@*Add the following code example to the corresponding CSHTML page to render Tab with scroll button.*@

&lt;ej:Tab ID="dishtype" runat="server" EnableTabScroll="true" Width="600px"&gt;

    &lt;Items&gt;

        &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

            &lt;ContentSection&gt;

                <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="pastatype" Text="Pasta Menu"&gt;

            &lt;ContentSection&gt;

                &lt;p&gt; Pasta cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="burgertype" Text="Burger Menu"&gt;

            &lt;ContentSection&gt;

                &lt;p&gt; Burger cooked to perfection tossed with vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

        &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

            &lt;ContentSection&gt;

                <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;            

        &lt;ej:TabItem Id="spaghetti" Text="Spaghetti Menu"&gt;

            &lt;ContentSection&gt;

                &lt;p&gt; Spaghetti cooked to perfection tossed with vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

        &lt;ej:TabItem Id="ramen" Text="Ramen Menu"&gt;

            &lt;ContentSection&gt;

                &lt;p&gt; Ramen cooked to perfection tossed with vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

    &lt;/Items&gt;

&lt;/ej:Tab&gt;





The following screenshot illustrates you the **Tab** control with scroll button. 

![](scroll-support_images\scroll-support_img1.png)![](scroll-support_images\scroll-support_img2.png)

_Figure_ _41__: Tab control with scroll support_



