---
layout: post
title: rtl-support
description: rtl support
platform: js
control: Tab Control
documentation: ug
---

# RTL Support

**Tab** control provides support for load contents in right to left format. This is achieved by setting ‘**enableRTL**’ property to “**true**”.

The following code example is used to render the **Tab** element in RTL format. 

* Add the following **HTML** to render **Tab** with **RTL** format.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with RTL format.&lt;script type="text/javascript"&gt;        $(function () {            $("#dishtype").ejTab({ enableRTL:true });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Tab in Rtl format.



&lt;div style="width:550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@&lt;div&gt;

                       Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

                   &lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).EnableRTL(true).Render();}

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Tab in Rtl format.

    &lt;ej:Tab ID="dishtype" runat="server" Width="600px" EnableRTL="true"&gt;

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





* The following screenshot illustrates the **Tab** with **RTL** format.

{% include image.html url="\js\Tab\concepts-and-features\rtl-support_images\rtl-support_img1.png" Caption="Figure 39: Tab with RTL format"%}{% include image.html url="\js\Tab\concepts-and-features\rtl-support_images\rtl-support_img2.png" Caption="Figure 39: Tab with RTL format"%}

