---
layout: post
title: integration-with-other-widgets
description: integration with other widgets
platform: js
control: Tab Control
documentation: ug
---

# Integration with other widgets

You can provide more customization to the **Tab** with **rating** control as content in it for describing the item rating value.

The **Essential JavaScript Rating** and **MVC Rating** control provide you an intuitive rating experience that allows you to select the number of stars that represents the rating. For more information about the rating, you can refer the following link:

[http://help.syncfusion.com/ug/js/default.htm#!Documents/gettingstarted25.htm](http://help.syncfusion.com/ug/js/default.htm)

The following code example explains you the **rating** control creation. The input element is used to create the **rating** control. Render the input element as **rating** control using the input element **id**. The code example is placed within the content description &lt;div&gt; element to declare the **rating** control and description in the **Tab** section and it is appended with the header initialization code section &lt;div&gt; element.

* Add the following **HTML** to render **Tab** with other widget.

<table>
<tr>
<td>
[HTML]   &lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        <p>Rating:&lt;/p&gt;        &lt;div class="dishRating"&gt;            &lt;input id="pizzarating" type="text" class="rating" /&gt;&lt;br /&gt;        &lt;/div&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        <p>Rating:&lt;/p&gt;        &lt;div class="dishRating"&gt;            &lt;input id="sandwichrating" type="text" class="rating" /&gt;        &lt;/div&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script to render Tab with other widget.&lt;script type="text/javascript"&gt;$(function () {            $("#dishtype").ejTab();            $("#pizzarating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.8 });            $("#snadwichrating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.8 });});&lt;/script&gt;</td></tr>
</table>


[CSHTML]  

// Add the following code example to the corresponding CSHTML page to render Tab with other widgets.



&lt;div style="width:550px"&gt;

    @{Html.EJ().Tab("dishtab").Items(data =>

           {

               data.Add().ID("pizzatype").Text("Pizza Type")

                   .ContentTemplate(@<div>Rating:@Html.EJ().Rating("PRating").Value(4)

                       Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

                   &lt;/div&gt;);

               data.Add().ID("sandwichtype").Text("Sandwich Type")

                   .ContentTemplate(@<div>Rating:@Html.EJ().Rating("SRating").Value(4)

                   Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.

               &lt;/div&gt;);

           }).Render();}

&lt;/div&gt;



[ASPX]    

// Add the following code example to the corresponding ASPX page to render Tab with other widgets.



    &lt;ej:Tab ID="dishtype" runat="server" ShowReloadIcon="true" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    &lt;div&gt; Rating :

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="ratingpizza" Value="4" Precision="Exact" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                    &lt;/div&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    &lt;div&gt; Rating :

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="ratingsandwich" Value="4" Precision="Exact" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                    &lt;/div&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





To render the **rating** controls in the first **Tab** element refer the styles mentioned in the following code example. 

* Add the following styles to render **Tab**.

{% highlight css %}

[CSS]
<style type="text/css" class="cssStyles">
        .dishRating {
            position: absolute;
            margin: -31px 0px 0px 80px;
        }       
    </style>


{% endhighlight %}



* The following screenshot illustrates the **Tab** content with rating control. 

![](integration-with-other-widgets_images\integration-with-other-widgets_img1.png)![](integration-with-other-widgets_images\integration-with-other-widgets_img2.png)

_Figure_ _36__:_ _Tab content section with Rating Control_

