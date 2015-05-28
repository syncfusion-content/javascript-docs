---
layout: post
title: template-support
description: template support
platform: js
control: Accordion 
documentation: ug
---

# Template Support

**ASP.NET MVC**

The **Content template** option provided in **MVC** is used to specify the **HTML** elements inside the **Accordion** control. You can use this option to load any **HTML** elements and display it in the **Accordion** panels as per your requirement.

The following code example explains how to use content template option in the **Accordion** control.



**[CSHTML]**



&lt;div style="width:500px;"&gt;

    @{Html.EJ().Accordion("pizzaMenu").Items(data =>

               {

                   data.Add().Text("GARDEN FRESH (Veg)").ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" /&gt;

                                        &lt;div class="ingredients"&gt;

                        Rate    : $50

                        &lt;br /&gt;

                        Ingredients : cheese, onions, green capsicums & tomatoes.

                    &lt;/div&gt;

                &lt;/div&gt;);

                   data.Add().Text("CORN & SPINACH (Veg)").ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $70

                        &lt;br /&gt;

                        Ingredients : cheese, sweet corn & green capsicums.

                    &lt;/div&gt;

                &lt;/div&gt;);

                   data.Add().Text("CHICKEN DELITE (Non-veg)").ContentTemplate(@&lt;div&gt;

                    &lt;img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" /&gt;

                    &lt;div class="ingredients"&gt;

                        Rate    : $100

                        &lt;br /&gt;

                        Ingredients : cheese, chicken chunks, onions & pineapple chunks.

                    &lt;/div&gt;

                &lt;/div&gt;);

               }).EnableMultipleOpen(true).Render();}

&lt;/div&gt;





**JavaScript**

In **JavaScript**, you can load the contents or **HTML** elements directly inside the **&lt;div&gt;** element that you are going to convert as **Accordion** control.

{% highlight html %}

[HTML]
<div id="pizzaMenu" style="width: 500px">
    <h3>
        <a href="#">GARDEN FRESH (Veg)</a>
</h3>
    <div>
        <img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $50
            <br />
            Ingredients : cheese, onions, green capsicums & tomatoes.
        </div>
    </div>
    <h3>
        <a href="#">CORN & SPINACH (Veg)</a>
    </h3>
    <div>
        <img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $70
            <br />
            Ingredients : cheese, sweet corn & green capsicums.
        </div>
    </div>
    <h3>
        <a href="#">CHICKEN DELITE (Non-veg)</a>
    </h3>
    <div>
        <img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $100
            <br />
            Ingredients : cheese, chicken chunks, onions & pineapple chunks.
        </div>
    </div>
</div>



{% endhighlight %}



{% highlight js %}

**[SCRIPT]**
$("#pizzaMenu").ejAccordion({ enableMultipleOpen: true });



{% endhighlight %}



**ASP.NET**

In **ASP.NET,** you can use the **&lt;contentsection&gt;** tag to load the contents for the **Accordion** control.

[ASPX]

&lt;div style="width:500px"&gt;

    &lt;ej:Accordion ID="pizzaMenu" runat="server" EnableMultipleOpen="true"&gt;

        &lt;items&gt;

            &lt;ej:accordionitem text="GARDEN FRESH (Veg)"&gt;

                &lt;contentsection&gt;

                    &lt;div&gt;

                        &lt;img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" /&gt;

                        &lt;div class="ingredients"&gt;

                            Rate    : $50

                            &lt;br /&gt;

                            Ingredients : cheese, onions, green capsicums & tomatoes.

                        &lt;/div&gt;

                    &lt;/div&gt;

                &lt;/contentsection&gt;

            &lt;/ej:accordionitem&gt;

            &lt;ej:accordionitem text="CORN & SPINACH (Veg)"&gt;

                &lt;contentsection&gt;

                    &lt;div&gt;

                        &lt;img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" /&gt;

                        &lt;div class="ingredients"&gt;

                            Rate    : $70

                            &lt;br /&gt;

                            Ingredients : cheese, sweet corn & green capsicums.

                        &lt;/div&gt;

                    &lt;/div&gt;

                &lt;/contentsection&gt;

            &lt;/ej:accordionitem&gt;

            &lt;ej:accordionitem text="CHICKEN DELITE (Non-veg)"&gt;

                &lt;contentsection&gt;

                    &lt;div&gt;

                        &lt;img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" /&gt;

                        &lt;div class="ingredients"&gt;

                            Rate    : $100

                            &lt;br /&gt;

                            Ingredients : cheese, chicken chunks, onions & pineapple chunks.

                        &lt;/div&gt;

                    &lt;/div&gt;

                &lt;/contentsection&gt;

            &lt;/ej:accordionitem&gt;

        &lt;/items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



**Output:**



![](template-support_images\template-support_img1.png)



