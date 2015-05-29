---
layout: post
title: look-and-feel
description: look and feel
platform: js
control: Menu
documentation: ug
---

# Look and feel

**Essential JavaScript** controls feature 12 built-in themes, six flat and gradient effects, and also supports custom skin options for user-defined themes.

12 themes support available for **Menu** control namely,

default-theme

flat-azure-dark

flat-lime

flat-lime-dark

flat-saffron

flat-saffron-dark

gradient-azure

gradient-azure-dark

gradient-lime

gradient-lime-dark

gradient-saffron

gradient-saffron-dark

**Cssclass**

**Menu** control also customizes its appearance using user-defined **CSS** and custom skin options (colors and backgrounds). To apply custom themes you can use the “cssClass” property. “cssClass” property sets the root class for **Menu** control theme.

Using this **cssClass** you can override the existing styles under the theme style sheet. The theme stylesheet applies theme-specific styles like colors and backgrounds. In the following sample the value of “cssClass” property is set as “Purple-dark”. Purple-dark is added as root class to **Menu** control at the runtime. From this root class you can customize the **Menu** control theme.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div&gt;    &lt;div&gt;        &lt;ul id="menucontrol"&gt;            &lt;li id="home"&gt;                <a href="#">Home</a>                &lt;ul&gt;                    &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                    &lt;li&gt;<a>Launch</a>&lt;/li&gt;                    &lt;li&gt;                        <a>About</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Location</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Services"&gt;                <a>Services</a>                &lt;ul&gt;                    &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;            &lt;li id="Contact"&gt;                <a>Contact us</a>                &lt;ul&gt;                    &lt;li&gt;<a>E-mail</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Careers"&gt;                <a>Careers</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Position</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Apply online</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({            width: 500,            cssClass: "Purple-dark"        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code in your CSHTML page.**

&lt;div class="imgframe"&gt;

    @Html.EJ().Menu("menucontrol").Items(items =>

        {

            items.Add().Url("#").Id("Home").Text("Home").Children(child =>

                {

                    child.Add().Url("").Text("Foundation");

                    child.Add().Url("").Text("Launch");

                    child.Add().Url("").Text("About").Children(child1 =>

                    {

                        child1.Add().Url("").Text("Company");

                        child1.Add().Url("").Text("Location");

                    });

                });

            items.Add().Url("").Text("Services").Children(child =>

                {

                    child.Add().Url("").Text("Consulting");

                    child.Add().Url("").Text("Outsourcing");

                });

            items.Add().Url("").Text("About");

            items.Add().Id("Contact").Url("").Text("Contact Us").Children(child =>

                {

                    child.Add().Url("").Text("Contact number");

                    child.Add().Url("").Text("E-mail");

                });

            items.Add().Url("").Id("Careers").Text("Careers").Children(child =>

                 {



                     child.Add().Url("").Text("Position").Children(child1 =>

                             {

                                 child1.Add().Url("").Text("Developer");

                                 child1.Add().Url("").Text("Manager");

                             });

                     child.Add().Url("").Text("Apply online");

                 });



        }).Width("500").**CssClass("Purple-dark")**

&lt;/div&gt;



[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="menucontrol" Width="500" CssClass="Purple-dark" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Id="Home" Text="Home"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Foundation"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Launch"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="About"&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Company"&gt;&lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Location"&gt;&lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;



                &lt;/ej:MenuItem&gt;





                &lt;ej:MenuItem Id="Services" Text="Services"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Consulting"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Outsourcing"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="About" Text="About"&gt;&lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Contact" Text="Contact us"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Contact Number"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Email"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Careers" Text="Careers"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Position"&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Developer"&gt;&lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Manager"&gt;&lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Apply online"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt;



* Add the following code in your style section.

{% highlight css %}

**[CSS]**

<style type="text/css" class="cssStyles">
    .Purple-dark {
        background: pink;
    }

    .Purple-dark.e-horizontal .e-list > a {
            color: #4800ff;
     }
</style>


{% endhighlight %}



Following screenshot displays the output of the above code.

![C:\Users\kaliswaran\Desktop\M-CSS.png](look-and-feel_images\look-and-feel_img1.png)

_Figure_ _31__17__: Look and feel of a Menu_

