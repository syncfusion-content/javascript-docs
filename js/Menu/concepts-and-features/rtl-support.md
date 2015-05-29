---
layout: post
title: rtl-support
description: rtl support
platform: js
control: Menu
documentation: ug
---

# RTL Support

The **enableRTL** option allows the **Menu** control to display it in the right to left direction. By default, this option is set to “false” in the **Menu** control.

* The following code depicts you on how to enable the **rtl** property of the **Menu** control.

<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({ <b>enableRTL: true</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// The following code example depicts how to enable the rtl property of the Menu control.

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



        }).Width("500").**EnableRTL(true)**

    &lt;/div&gt;





[ASPX]

// Add the code in ASPX page

&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="menucontrol" Width="500" EnableRTL="true" runat="server"&gt;

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



Following screenshot displays the output for the above code.

![](rtl-support_images\rtl-support_img1.png)

_Figure_ _35__21__: RTL Support_

