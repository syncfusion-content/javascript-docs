---
layout: post
title: ajax-content-load-load-on-demand
description: ajax content load (load on demand)
platform: js
control: Tab Control
documentation: ug
---

# Ajax Content Load (Load on Demand)

You can change the contents in sub **Tab** element periodically and you are provided with a support to change the contents without any problems. To achieve the content load, use the **Load on Demand** concept.

In **Load On-Demand**, the external **HTML** file with the necessary details is referred in &lt;href&gt; section during **Tab** header declaration section. Also include “**dataType**”, “**contentType**”, and “**anync**” in the script like the following example when rendering the control. When you click the **Tab** header, the Ajax automatically calls the content from the external files and displays in a **Tab** content section. 

**Sub Tab with Ajax Content**

Each item has a variety of options and these options are also specified in the limited space. So you can choose the **Tab** control that is used within the root **Tab** to specify more details.

The following code example illustrates to create the **Tab** control within the root **Tab** element. This **HTML** code is appended within the previous **HTML** code section. To render the child **Tab** with its header, add this code example within the first **Tab** &lt;div&gt; element. 

* Add the following **HTML** to render sub **Tab** with **ajax** content.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;div id="pizzaType"&gt;            &lt;ul&gt;                &lt;li&gt;                    <a href="content/cornSpinach.html">Corn & Spinach &lt;/a&gt;&lt;/li&gt;                &lt;li&gt;                    <a href="Content/chickenDelite.html">Chicken Delite &lt;/a&gt;&lt;/li&gt;            &lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;        &lt;div id="sandwichType"&gt;            &lt;ul&gt;                &lt;li&gt;                    <a href="Content/gardenVeggie.html">Garden Veggie &lt;/a&gt;&lt;/li&gt;                &lt;li&gt;                    <a href="Content/chickenTikka.html">Chicken Tikka &lt;/a&gt;&lt;/li&gt;                &lt;li&gt;                    <a href="Content/paneerTikka.html">Paneer Tikka &lt;/a&gt;&lt;/li&gt;            &lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render sub Tab with Ajax content.&lt;script type="text/javascript"&gt;   $(function () {        $("#dishtype").ejTab();                        $("#pizzaType").ejTab({ dataType: "html", contentType: "html", async: true });            $("#sandwichType").ejTab({ dataType: "html", contentType: "html", async: true }); });         &lt;/script&gt; </td></tr>
</table>


[CSHTML]

// Add the following code example to the corresponding CSHTML page to render sub Tab with ajax content.



&lt;div id="dishtype" style="width: 550px"&gt;

    &lt;ul&gt;

        &lt;li&gt;<a href="#pizzatype">Pizza Type</a>&lt;/li&gt;

        &lt;li&gt;<a href="#sandwichtype">Sandwich Type</a>&lt;/li&gt;

    &lt;/ul&gt;    

    &lt;div id="pizzatype" style="background-color: #F5F5F5"&gt;

        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

        @firstTab()

        @Html.EJ().Tab("dishtype").AjaxSettings(ajax => ajax.ContentType("html").DataType("html").Async(true))



        @helper firstTab()

        {

            @Html.EJ().Tab("PizzaType").Items(data =>

          {

              data.Add().ID("Corn-Spinach").Text("Corn Spinach").Url("Content/cornSpinach.html");

              data.Add().ID("ChickenDelite").Text("Chicken-Delite").Url("Content/chickenDelite.html");

          })

        }

    &lt;/div&gt;

    &lt;div id="sandwichtype" style="background-color: #F5F5F5"&gt;

        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

        @secondTab()

        @helper secondTab()

        {

            @Html.EJ().Tab("sandwichtype").Items(data =>

          {

              data.Add().ID("gardenveggie").Text("Corn Spinach").Url("Content/gardenVeggie.html");

              data.Add().ID("chickentikka").Text("Chicken-Delite").Url("Content/chickenTikka.html");              data.Add().ID("PaneerTikka").Text("PaneerTikka").Url("Content/paneerTikka.html");

          })

        }

    &lt;/div&gt;

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render sub Tab with ajax content.

    &lt;ej:Tab ID="dishtype" runat="server" Width="600px"&gt;

        &lt;Items&gt;

            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                    &lt;ej:Tab ID="PizzaTab" runat="server"&gt;

                        &lt;Items&gt;

                            &lt;ej:TabItem Id="PizzaMenu" Text="Corn Spinach" Url="Content/cornSpinach.html"&gt;

                            &lt;/ej:TabItem&gt;

                            &lt;ej:TabItem Id="PizzaMenu1" Text="Chicken-Delite" Url="Content/chickenDelite.html"&gt;

                            &lt;/ej:TabItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:Tab&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;

                &lt;ContentSection&gt;

                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                    &lt;ej:Tab ID="Tab1" runat="server"&gt;

                        &lt;Items&gt;

                            &lt;ej:TabItem Id="gardenveggie" Text="Garden Veggie" Url="Content/gardenVeggie.html"&gt;

                            &lt;/ej:TabItem&gt;

                            &lt;ej:TabItem Id="chickentikka" Text="Chicken-Tikka" Url="Content/chickenTikka.html"&gt;

                            &lt;/ej:TabItem&gt;

                            &lt;ej:TabItem Id="paneertikka" Text="Paneer-Tikka" Url="Content/paneerTikka.html"&gt;

                            &lt;/ej:TabItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:Tab&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:TabItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Tab&gt;





*   The file ‘**cornSpinach.html**’ content is as follows. 

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
<imgsrc="[http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png](http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png)"alt="corn-spinach">
        <div class="ingredients">
            Rate    : $70<br/> Ingredients : cheese, sweet corn &amp; green capsicums.
            <br />
            Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.                    </div>
    </div>   
</body>
</html>


{% endhighlight %}



* The file ‘**chickenDelite.html’** content is as follows.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
        <img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite">
        <div class="ingredients">
            Rate    : $100<br /> Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.   <br /> 
             Description: This is a tasty, elegant chicken dish that is easy to prepare.
        </div>
    </div>
</body>
</html>


{% endhighlight %}



At the time of **Ajax** call, the content fetched from external file referenced location is illustrated in the following screenshot. 



![](ajax-content-load-load-on-demand_images\ajax-content-load-load-on-demand_img1.png)![](ajax-content-load-load-on-demand_images\ajax-content-load-load-on-demand_img2.png)

_Figure_ _37__:_ _Ajax Call_



The following screenshot illustrates the First **Tab** with the sub **Tab** control using **Load on Demand**. 

![](ajax-content-load-load-on-demand_images\ajax-content-load-load-on-demand_img3.png)![](ajax-content-load-load-on-demand_images\ajax-content-load-load-on-demand_img4.png)

_Figure_ _38__:_ _Tab section with sub Tab control using Load on Demand._

