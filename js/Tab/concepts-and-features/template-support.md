---
layout: post
title: template-support
description: template support
platform: js
control: Tab Control
documentation: ug
---

# Template Support

**ASP.NET MVC**

The Content template option provided in MVC is used to specify the HTML elements inside the Tab control. We can use this option to load any HTML elements and showcase it in the Tab panels as per our requirement.

The following code block showcases how to use content template option in the Tab control.



**[CSHTML]**



&lt;div style="width:650px"&gt;

    @{Html.EJ().Tab("pizzaMenu").Items(data =>

           {

               data.Add().ID("gardenfresh").Text("GARDEN FRESH (Veg)")

                   .ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $50

                        &lt;br /&gt;

                        Ingredients : cheese, onions, green capsicums & tomatoes.

                    &lt;/div&gt;

                &lt;/div&gt;);

               data.Add().ID("cornandspinach").Text("CORN & SPINACH (Veg)")

                   .ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $70

                        &lt;br /&gt;

                        Ingredients : cheese, sweet corn & green capsicums.

                    &lt;/div&gt;

                &lt;/div&gt;);

               data.Add().ID("chickendelite").Text("CHICKEN DELITE (Non-veg)")

                   .ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $100

                        &lt;br /&gt;

                        Ingredients : cheese, chicken chunks, onions & pineapple chunks.

                    &lt;/div&gt;

                &lt;/div&gt;);

           }).Render();}

&lt;/div&gt;



**JavaScript**

In **JavaScript**, wWe can load the contents or HTML elements directly inside the &lt;div&gt; element which we are going to convert as Tab control.



{% highlight html %}

**[HTML]**
    <div id="dishtype" style="width: 650px">
        <ul>
            <li><a href="#corn">Corn & Spinach </a></li>
            <li><a href="#chicken">Chicken Delite</a></li>
        </ul>
        <div id="corn" style="background-color: #F5F5F5">
            <div class="e-content">
                <img src="http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach">
                <div class="ingredients">
                    Rate    : $70<br /> Ingredients : cheese, sweet corn &amp; green capsicums.
                    <br />
                    Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.
                </div>
            </div>
        </div>
        <div id="chicken" style="background-color: #F5F5F5">
            <!--Content for Chicken Delite-->
        </div>
    </div>


{% endhighlight %}





{% highlight js %}

**[SCRIPT]**
<script type="text/javascript">
        $(function () {
            $("#dishtype").ejTab();
        });
    </script>$("#pizzaMenu").ejTab();



{% endhighlight %}



**ASP.NET**

In **ASP.NET** we can use the **&lt;contentsection&gt;** tag to load the contents for the **Tab** control.

**[ASPX]**

&lt;ej:Tab ID="pizzaMenu" runat="server" Width="650px"&gt;

    &lt;items&gt;

        &lt;ej:tabitem id="gardenfresh" text="GARDEN FRESH (Veg)"&gt;

            &lt;contentsection&gt;

                    &lt;img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $50

                        &lt;br /&gt;

                        Ingredients : cheese, onions, green capsicums & tomatoes.

                    &lt;/div&gt;

            &lt;/contentsection&gt;

        &lt;/ej:tabitem&gt;

        &lt;ej:tabitem id="cornandspinach" text="CORN & SPINACH (Veg)"&gt;

            &lt;contentsection&gt;

                &lt;img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" /&gt;

                &lt;div class="ingredients"&gt;

                    Rate    : $70

                    &lt;br /&gt;

                    Ingredients : cheese, sweet corn & green capsicums.

                &lt;/div&gt;

            &lt;/contentsection&gt;

        &lt;/ej:tabitem&gt;

        &lt;ej:tabitem id="chickendelite" text="CHICKEN DELITE (Non-veg)"&gt;

            &lt;contentsection&gt;

                &lt;img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" /&gt;

                &lt;div class="ingredients"&gt;

                    Rate    : $100

                    &lt;br /&gt;

                    Ingredients : cheese, chicken chunks, onions & pineapple chunks.

                &lt;/div&gt;

            &lt;/contentsection&gt;

        &lt;/ej:tabitem&gt;

    &lt;/items&gt;

&lt;/ej:Tab&gt;



**Output:**

![](template-support_images\template-support_img1.png)![](template-support_images\template-support_img2.png)

