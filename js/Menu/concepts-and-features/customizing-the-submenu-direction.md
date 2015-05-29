---
layout: post
title: customizing-the-submenu-direction
description: customizing the submenu direction
platform: js
control: Menu
documentation: ug
---

# Customizing the Submenu direction

You can customize the direction to open the sub menu items using **subMenuDirection** property. **subMenuDirection** accepts the type as string or enum and value as “Left” and “Right”. 

In the following example, the Sub menus opens in the Left side of the menu.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="coProducts"&gt;                &lt;li id="Products"&gt;                    <a href="#">Products</a>                    &lt;ul&gt;                        &lt;li&gt;<a>ASP.NET</a>&lt;/li&gt;                        &lt;li&gt;<a>ASP.NET MVC</a>&lt;/li&gt;                        &lt;ul&gt;                            &lt;li&gt;<a>WinRT (XMAL)&lt;/a&gt;&lt;/li&gt;                            &lt;li&gt;<a>Silverlight</a>&lt;/li&gt;                        &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Support"&gt;                <a>Support</a>                &lt;ul&gt;                    &lt;li&gt;<a>Direct-Trac Support</a>&lt;/li&gt;                    &lt;li&gt;                        <a>Services</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                            &lt;li&gt;<a>Training</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Purchase"&gt;<a>Purchase</a>&lt;/li&gt;            &lt;li id="Downloads"&gt;                <a>Downloads</a>                &lt;ul&gt;                    &lt;li&gt;<a>Evaluation</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Resources"&gt;                <a>Resources</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Technology Resource Portal &lt;/a&gt;                        &lt;ul&gt;                            &lt;li&gt;<a>White Papers</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>FAQ</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Company"&gt;                <a>Company</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>About Us</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Media Kit</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Company Blog</a>&lt;/li&gt;                    &lt;li&gt;<a>Technical Blog</a>&lt;/li&gt;                    &lt;li&gt;<a>Newsletter</a>&lt;/li&gt;                    &lt;li&gt;                        <a>Partners</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Technology Partners</a>&lt;/li&gt;                            &lt;li&gt;<a>Training Partners</a>&lt;/li&gt;                            &lt;li&gt;<a>Consulting Partners</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        <a>Locations</a>                        &lt;ul&gt;                            &lt;li&gt;<a>RDU</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Contact Us</a>&lt;/li&gt;                    &lt;li&gt;<a>Careers</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#coProducts").ejMenu(        {            subMenuDirection: "left"        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**   

**// Add the following code in your CSHTML page.**

 &lt;div class="imgframe"&gt;

    @Html.EJ().Menu("syncfusionProducts").Items(items =>

               {

                   items.Add().Url("#").Id("Products").Text("Products").Children(child =>

                       {

                           child.Add().Url("").Text("ASP.NET");

                           child.Add().Url("").Text("ASP.NET MVC");

                           child.Add().Url("").Text("Mobile MVC");

                           child.Add().Url("").Text("Silverlight");

                           child.Add().Url("").Text("Windows Forms");

                           child.Add().Url("").Text("Windows Phone");

                           child.Add().Url("").Text("WinRT (XMAL)");

                           child.Add().Url("").Text("WPF");

                           child.Add().Url("").Text("Orubase Studio");

                           child.Add().Url("").Text("Metro Studio");

                           child.Add().Url("").Text("What's New").Children(child1 =>

                               {

                                   child1.Add().Url("").Text("ASP.NET");

                                   child1.Add().Url("").Text("WPF");

                                   child1.Add().Url("").Text("Silverlight");

                                   child1.Add().Url("").Text("Windows Forms");

                                   child1.Add().Url("").Text("Windows Phone");

                                   child1.Add().Url("").Text("ASP.NET MVC");

                                   child1.Add().Url("").Text("ASP.NET");

                               });

                       });

                   items.Add().Url("").Text("Support").Children(child =>

                       {

                           child.Add().Url("").Text("Direct-Trac Support");

                           child.Add().Url("").Text("Community Forums");

                           child.Add().Url("").Text("Knowledge Base");

                           child.Add().Url("").Text("Online Documentation");

                           child.Add().Url("").Text("Services").Children(child1 =>

                               {

                                   child1.Add().Url("").Text("Consulting");

                                   child1.Add().Url("").Text("Training");

                               });

                       });

                   items.Add().Url("").Id("Purchase").Text("Purchase");

                   items.Add().Url("").Id("Downloads").Text("Downloads").Children(child =>

                       {

                           child.Add().Url("").Text("Evaluation");

                           child.Add().Url("").Text("Free E-Books");

                           child.Add().Url("").Text("Metro Studio");

                           child.Add().Url("").Text("Latest Version");

                           child.Add().Url("").Text("Version History");

                       });

                   items.Add().Id("Resources").Url("").Text("Resources").Children(child =>

                      {

                          child.Add().Url("").Text("Technology Resource Portal").Children(child1 =>

                                      {

                                          child1.Add().Url("").Text("E-Books");

                                          child1.Add().Url("").Text("White Papers");

                                      });

                          child.Add().Url("").Text("Case Studies");

                          child.Add().Url("").Text("Bouchers & Datasheets");

                          child.Add().Url("").Text("FAQ");

                      });

                   items.Add().Url("").Id("Company").Text("Company").Children(child =>

                   {

                       child.Add().Url("").Text("About Us").Children(child1 =>

                           {

                               child1.Add().Url("").Text("More About Us");

                               child1.Add().Url("").Text("Management");

                               child1.Add().Url("").Text("News & Events");

                               child1.Add().Url("").Text("Customer Quotes");

                               child1.Add().Url("").Text("Customer Lists");

                               child1.Add().Url("").Text("Case Studies");

                               child1.Add().Url("").Text("Awards");

                               child1.Add().Url("").Text("Media Kit");

                           });

                       child.Add().Url("").Text("Company Blog");

                       child.Add().Url("").Text("Technical Blog");

                       child.Add().Url("").Text("Newsletter");

                       child.Add().Url("").Text("Partners").Children(child1 =>

                           {

                               child1.Add().Url("").Text("Technology Partners");

                               child1.Add().Url("").Text("Training Partners");

                               child1.Add().Url("").Text("Consulting Partners");

                           });

                       child.Add().Url("").Text("Locations").Children(child1 =>

                       {

                           child1.Add().Url("").Text("RDU");

                           child1.Add().Url("").Text("Chennai");

                       });

                       child.Add().Url("").Text("Contact Us");

                       child.Add().Url("").Text("Careers");

                   });



               }).Width("500").**SubMenuDirection(Direction.Left)**

&lt;/div&gt;







[ASPX]  

 // Add the code in ASPX page 

&lt;ej:Menu ID="syncfusionProducts" SubMenuDirection="Left" runat="server"&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Id="Products" Text="Products"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="ASP.NET"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="ASP.NET MVC"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Mobile MVC"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Silverlight"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Windows Forms"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Windows Phone"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="WinRT (XMAL)"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="WPF"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Orubase Studio"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Metro Studio"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="What's New"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="WinRT (XMAL)"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="WPF"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Silverlight"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Windows Forms"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="ASP.NET MVC"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="ASP.NET"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;



                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;



            &lt;ej:MenuItem Id="Support" Text="Support"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Direct-Trac Support"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Community Forums"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Knowledge Base"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Online Documentation"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Services"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Consulting"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Taining"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Community Forums"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Id="Purchase" Text="Purchase"&gt;&lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Id="Downloads" Text="Downloads"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Evaluation"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Free E-Books"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Metro Studio"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Latest Version"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Version History"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Id="Resources" Text="Resources"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Technology Resource Portal"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="E-books"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="White Papers"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Case Studies"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Bouchers & Datasheets"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="FAQ"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Id="Company" Text="Company"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="About Us"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="More About Us"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Management"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="News & Events"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Customer Quotes"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Customer Lists"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Case Studies"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Awards"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Media Kit"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Company Blog"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Technical Blog"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Newsletter"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Partners"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Technology Partners"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Training Partners"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Consulting Partners"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;



                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;



                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Locations"&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="RDU"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                        &lt;Items&gt;

                            &lt;ej:MenuItem Text="Chennai"&gt;&lt;/ej:MenuItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Contact Us"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Contact Us"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Menu&gt;



The output for the above code example is as follows.          

![C:\Users\kaliswaran\Desktop\M-openDir.png](customizing-the-submenu-direction_images\customizing-the-submenu-direction_img1.png)

_Figure_ _29__15__: Customizing Submenu Direction_

You can even achieve auto positioning for Context Menu. Use the following code sample for context menu in order to open the submenu items of context menu in left side.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]     </b> &lt;div&gt;    &lt;div id="target" class="textarea"&gt;        HTML is written in the form of HTML elements consisting of tags enclosed in angle        brackets (like        &lt;html&gt;        ),within the web page content. HTML tags most commonly come in pairs like and ,although        some tags, known as empty elements, are unpaired, for example        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into        visible or audible web pages. The browser does not display the HTML tags, but uses        the tags to interpret the content of the page.    &lt;/div&gt;    &lt;ul id="contextMenu"&gt;        &lt;li&gt;            <a>Cut</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Cut Particular</a>                &lt;/li&gt;                &lt;li&gt;<a>Cut Fully</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;<a>Copy</a>&lt;/li&gt;        &lt;li&gt;<a>Paste</a>&lt;/li&gt;        &lt;li class="separator"&gt;&lt;/li&gt;        &lt;li&gt;<a>Comments</a>&lt;/li&gt;        &lt;li&gt;<a>Links</a>&lt;/li&gt;        &lt;li&gt;<a>Clear Formatting</a>&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#contextMenu").ejMenu(             {                 menuType: ej.MenuType.ContextMenu,                 openOnClick: false,                 contextMenuTargetID: "#target",                 <b>subMenuDirection: ej.Direction.Left</b>             });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**     

**// Add the following code in your CSHTML page.**

&lt;div id="target" class="textarea"&gt;

    HTML is written in the form of HTML elements consisting of tags enclosed in angle

    brackets (like &lt;html&gt; ),within the web page content. HTML tags most commonly

    come in pairs like and ,although some tags, known as empty elements, are unpaired,

    for example &lt;img&gt;. The purpose of a web browser is to read HTML documents

    and compose them into visible or audible web pages. The browser does not display

    the HTML tags, but uses the tags to interpret the content of the page.

&lt;/div&gt;

@Html.EJ().Menu("docfile").Items(items =>

                   {

                       items.Add().Url("").Text("Cut").Children(child =>

                       {

                           child.Add().Url("").Text("Cut Particular");

                           child.Add().Url("").Text("Cut Fully");

                       });

                       items.Add().Url("").Text("Copy");

                       items.Add().Url("").Text("Paste");

                       items.Add().Url("").Text("Comments");

                       items.Add().Url("").Text("Links");

                       items.Add().Url("").Text("Clear Formatting");                   }).MenuType(MenuType.ContextMenu).OpenOnClick(true).ContextMenuTarget("#target").**SubMenuDirection(Direction.Left)**



[ASPX]     

// Add the code in ASPX page

&lt;div id="target" class="textarea"&gt;

        HTML is written in the form of HTML elements consisting of tags enclosed in angle

        brackets (like

        &lt;html&gt;

        ),within the web page content. HTML tags most commonly come in pairs like and ,although

        some tags, known as empty elements, are unpaired, for example

        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into

        visible or audible web pages. The browser does not display the HTML tags, but uses

        the tags to interpret the content of the page.

    &lt;/div&gt;

    &lt;ej:Menu ID="Menu1" MenuType="ContextMenu" OpenOnClick="false" SubMenuDirection="Left" runat="server" ContextMenuTarget="#target"&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Cut"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Cut Particularly"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Cut Fully"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Copy"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Paste"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem SpriteCssClass="separator"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Comments"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Links"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Clear Formatting"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Menu&gt;





* Add the following code in your style section.

{% highlight css %}

**[CSS]**

<style type="text/css">
    .textarea {
        border: 1px solid;
        padding: 10px;
        position: relative;
        text-align: justify;
        width: 463px;
        color: gray;
        margin: 0 auto;
    }
</style>


{% endhighlight %}


The output for the above code example is as follows.

![](customizing-the-submenu-direction_images\customizing-the-submenu-direction_img2.png)

_Figure_ _30__16__: Customizing Submenu direction in Context Menu_

