---
layout: post
title: icons-and-navigation
description: icons and navigation
platform: js
control: Menu
documentation: ug
---

# Icons and navigation

Icons are the images that is displayed in the **Menu** control. To specify the menu with icons you can use **sprite** property to display the icons. 

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="menujson"&gt;&lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b><b>// Initialize the Menu control in JavaScript.</b>&lt;script type="text/javascript"&gt;    var data = [        { id: 1, text: "Inbox", parentId: null, sprite: "mail-ca" },        { id: 2, text: "Sent Items", parentId: null, sprite: "mail-cn" },        { id: 3, text: "All Mail", parentId: null, sprite: "mail-ee" },        { id: 4, text: "Outbox", parentId: null, sprite: "mail-es" },        //first level child        { id: 11, parentId: 1, text: "Mark as unread", sprite: "mail-dz" },        { id: 12, parentId: 1, text: "Forward", sprite: "mail-am" },        { id: 13, parentId: 1, text: "Mark as favourite", sprite: "mail-bd" },        { id: 14, parentId: 1, text: "Mark as important", sprite: "mail-cu" },        { id: 15, parentId: 2, text: "Move to trash", sprite: "mail-dk" },        { id: 16, parentId: 2, text: "Delete", sprite: "mail-eg" },        { id: 17, parentId: 3, text: "New Mail", sprite: "mail-fi" },        { id: 18, parentId: 3, text: "Read Mail", sprite: "mail-in" },        { id: 19, parentId: 3, text: "Unread Mail", sprite: "mail-my" },        { id: 20, parentId: 4, text: "Discard draft", sprite: "mail-nz" },        { id: 21, parentId: 4, text: "Send again", sprite: "mail-no" },        { id: 22, parentId: 4, text: "Delete", sprite: "mail-pl" },    ];    jQuery(function ($) {        $("#menujson").ejMenu({            width: 425,            fields: { dataSource: data, id: "id", parentId: "parentId", text: "text", spriteCssClass: "sprite" }        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code in your CSHTML page</b>       @Html.EJ().Menu("menujson").MenuFields(f => f.Datasource((IEnumerable<Check.Controllers.CheckController.icons>)ViewBag.datasource).Id("pid").Text("mtext").ParentId("parent").SpriteCssClass("sprite"))</td></tr>
<tr>
<td>
<b>[CS]</b><b>// </b>In the controller page add the codeusing System;using System.Collections.Generic;using System.Linq;using System.Web;using System.Web.Mvc;using Check.Models;namespace Check.Controllers{    public class CheckController : Controller    {        public class icons        {            public string mtext { get; set; }            public string sprite { get; set; }            public int pid { get; set; }            public string parent { get; set; }        }                List<icons> menu = new List<icons>();        public ActionResult DataBindingJson()        {            menu.Add(new icons { pid = 1, mtext = "Inbox", parent = null, sprite="mail-ca" });            menu.Add(new icons { pid = 2, mtext = "Sent items", parent = null, sprite="mail-cn" });            menu.Add(new icons { pid = 3, mtext = "All mail", parent = null, sprite="mail-ee" });            menu.Add(new icons { pid = 4, mtext = "Outbox", parent = null, sprite="mail-es" });            menu.Add(new icons { pid = 11, parent = "1", mtext = "Mark as unread", sprite = "mail-dz" });            menu.Add(new icons { pid = 12, parent = "1", mtext = "Forward", sprite = "mail-am" });            menu.Add(new icons { pid = 13, parent = "1", mtext = "Mark as favourite", sprite = "mail-bd" });            menu.Add(new icons { pid = 14, parent = "1", mtext = "Mark as important", sprite = "mail-cu" });            menu.Add(new icons { pid = 15, parent = "2", mtext = "Move to trash", sprite = "mail-dk" });            menu.Add(new icons { pid = 16, parent = "2", mtext = "Delete", sprite = "mail-eg" });            menu.Add(new icons { pid = 17, parent = "3", mtext = "New mail", sprite = "mail-fi" });            menu.Add(new icons { pid = 18, parent = "3", mtext = "Read mail", sprite = "mail-in" });            menu.Add(new icons { pid = 19, parent = "3", mtext = "Unread mail", sprite = "mail-my" });            menu.Add(new icons { pid = 20, parent = "4", mtext = "Discard draft", sprite = "mail-nz" });            menu.Add(new icons { pid = 21, parent = "4", mtext = "Send again", sprite = "mail-no" });            menu.Add(new icons { pid = 22, parent = "4", mtext = "Delete", sprite = "mail-pl" });            ViewBag.datasource = menu;            return View();        }    }} </td></tr>
</table>


<table>
<tr>
<td>
[ASPX]// Add the code in ASPX page        &lt;ej:Menu ID="menujson" DataIdField="id" DataParentIdField="parentId" DataTextField="text" DataSpriteCssField="sprite" runat="server"&gt;&lt;/ej:Menu&gt;</td></tr>
<tr>
<td>
[CS]// In code behind add this code    public class Check : System.Web.UI.Page    {        public class icons        {            public string mtext { get; set; }            public string sprite { get; set; }            public int pid { get; set; }            public string parent { get; set; }        }                List<icons> menu = new List<icons>();        public ActionResult DataBindingJson()        {            menu.Add(new icons { pid = 1, mtext = "Inbox", parent = null, sprite="mail-ca" });            menu.Add(new icons { pid = 2, mtext = "Sent items", parent = null, sprite="mail-cn" });            menu.Add(new icons { pid = 3, mtext = "All mail", parent = null, sprite="mail-ee" });            menu.Add(new icons { pid = 4, mtext = "Outbox", parent = null, sprite="mail-es" });            menu.Add(new icons { pid = 11, parent = "1", mtext = "Mark as unread", sprite = "mail-dz" });            menu.Add(new icons { pid = 12, parent = "1", mtext = "Forward", sprite = "mail-am" });            menu.Add(new icons { pid = 13, parent = "1", mtext = "Mark as favourite", sprite = "mail-bd" });            menu.Add(new icons { pid = 14, parent = "1", mtext = "Mark as important", sprite = "mail-cu" });            menu.Add(new icons { pid = 15, parent = "2", mtext = "Move to trash", sprite = "mail-dk" });            menu.Add(new icons { pid = 16, parent = "2", mtext = "Delete", sprite = "mail-eg" });            menu.Add(new icons { pid = 17, parent = "3", mtext = "New mail", sprite = "mail-fi" });            menu.Add(new icons { pid = 18, parent = "3", mtext = "Read mail", sprite = "mail-in" });            menu.Add(new icons { pid = 19, parent = "3", mtext = "Unread mail", sprite = "mail-my" });            menu.Add(new icons { pid = 20, parent = "4", mtext = "Discard draft", sprite = "mail-nz" });            menu.Add(new icons { pid = 21, parent = "4", mtext = "Send again", sprite = "mail-no" });            menu.Add(new icons { pid = 22, parent = "4", mtext = "Delete", sprite = "mail-pl" });            ViewBag.datasource = menu;            return View();        }    }</td></tr>
</table>


* Add the following code in your style section.



{% highlight css %}

**[CSS]**

<style type="text/css">
        #menujson {
            margin-left: 50px;
        }
        .e-menu li > ul > li > a {
            padding: 3px 24px 3px 35px;
        }
        [class^="mail-"],
        [class*="mail-"] {
            background-image: url("../images/spriteimage.png");
            height: 18px;
            left: 2px;
            top: 4px;
            width: 24px;
        }
        .mail-dz { background-position: -68px -15px;     }
        .mail-am { background-position: 91px -45px;      }
        .mail-bd { background-position: -98px 0;         }
        .mail-cu { background-position: -607px -221px;   }
        .mail-dk { background-position: -67px -15px;     }
        .mail-eg { background-position: 600px -15px;     }
        .mail-fi { background-position: 12441px 12458px; }
        .mail-in { background-position: -307px -103px;   }
        .mail-my { background-position: 240px -102px;    }
        .mail-nz { background-position: -100px -45px;    }
        .mail-no { background-position: -69px -45px;     }
        .mail-pl { background-position: -129px -45px;    }
        .mail-ca { background-position: -1345px -387px;  }
        .mail-cn { background-position: -427px -42px;    }
        .mail-ee { background-position: -706px -15px;    }
        .mail-es { background-position: -1157px -43px    }
    </style>


{% endhighlight %}



The following screenshot displays the output for the above code.                                                                                                       

![](icons-and-navigation_images\icons-and-navigation_img1.png)

_Figure_ _24__10__: Menu with Icons_

**Navigation**

Navigation in Menu control is the default usage to navigate into the other web page. You can navigate to another page in menu item by providing link to the menu items. Navigation in **Menu** control can be achieved by placing “**href**” path to the anchor tag. Use the following code sample for navigating in **Menu** control.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div&gt;    &lt;ul id="weblink"&gt;        &lt;li id="searchengine"&gt;            <a href="#">Search engine</a>            &lt;ul&gt;                &lt;li&gt;<a href="http://www.bing.com/">Bing</a>&lt;/li&gt;                &lt;li&gt;<a href="https://www.google.co.in/">Google</a>&lt;/li&gt;                &lt;li&gt;<a href="https://in.yahoo.com/">Yahoo</a>&lt;/li&gt;                &lt;li&gt;<a href="http://www.rediff.com/">Rediff</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="atd"&gt;<a href="http://allthingsd.com/">All things digital</a>&lt;/li&gt;        &lt;li id="electronics"&gt;            <a>Electronics</a>            &lt;ul&gt;                &lt;li&gt;                    <a href="http://www.engadget.com/">Engadget</a>                &lt;/li&gt;                &lt;li&gt;<a href="http://www.electronista.com/">Electronista</a>&lt;/li&gt;                &lt;li&gt;<a href="http://www.gearlog.com/">Gearlog</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="cnet"&gt;<a href="http://www.centernetworks.com/">Center networks</a>&lt;/li&gt;        &lt;li id="webpronews"&gt;            <a href="http://www.webpronews.com/">Webpronews</a>        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript] </b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#weblink").ejMenu({ width: 612 });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code in your CSHTML page.**

    &lt;div class="imgframe"&gt;

    @Html.EJ().Menu("weblink").Items(items =>

        {

            items.Add().Url("#").Id("searchengine").Text("Search engine").Children(child =>

                {

                    child.Add().Url("http://www.bing.com/").Text("Bing");

                    child.Add().Url("https://www.google.co.in/").Text("Google");

                    child.Add().Url("https://in.yahoo.com/").Text("Yahoo");

                    child.Add().Url("http://www.rediff.com/").Text("Rediff");

                });

            items.Add().Url("http://allthingsd.com/").Text("All things digital");



            items.Add().Url("").Text("Electronics").Children(child =>

                {

                    child.Add().Url("http://www.engadget.com/").Text("Engadget");

                    child.Add().Url("http://www.electronista.com/").Text("Electronista");

                    child.Add().Url("http://www.gearlog.com/").Text("Gearlog");

                });

            items.Add().Url("http://www.centernetworks.com/").Text("Center networks");

            items.Add().Url("http://www.webpronews.com/").Text("Web pronews");



        }).Width("500")

&lt;/div&gt;





[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="weblink" Width="600" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Id="searchengine" Text="Search engine"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Bing" Url="http://www.bing.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Google" Url="https://www.google.co.in/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Yahoo" Url="http://in.yahoo.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Rediff" Url="https://www.rediff.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Text="All things digital" Url="http://allthingsd.com/"&gt;&lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Text="Electronics"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Engagdget" Url="http://www.engadget.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Electronista" Url="http://www.electronista.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Gearlog" Url="http://www.gearlog.com/"&gt;&lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Text="Center networks" Url="http://centernetworks.com/"&gt;&lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Text="Web pronews" Url="http://webpronews.com/"&gt;&lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt; 



The following screenshot displays the output for the above code example.            

![](icons-and-navigation_images\icons-and-navigation_img2.png)

_Figure_ _25__11__: Navigation of Menu_

When you click on “**Google**” that is present under “Search engine”, it navigates to the link that you specified in the sample code. Then the output is as follows.

![C:\Users\kaliswaran\Desktop\menu2.PNG](icons-and-navigation_images\icons-and-navigation_img3.png)

_Figure_ _26__12__: After navigating to a menu item_

