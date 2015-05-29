---
layout: post
title: miscellaneous
description: miscellaneous
platform: js
control: Menu
documentation: ug
---

# Miscellaneous

**Height**

Specifies the height of the root menu. You can customize the height of the **Menu** control by using height property. 

* You can specify the height of the **Menu** control in the script as follows.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
**height: 50**
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**// You can specify the height of the Menu control in the CSHTML page as follows.**

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



        }).**Height("50")**

&lt;/div&gt;







[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Height="50" runat="server"&gt;

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

**Width**

Specifies the width of the main menu. You can customize the width of the **Menu** control by using width property.

* You can specify the width of the **Menu** control in the script as follows.

{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 700
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**// You can specify the width of the Menu control in the CSHTML page as follows.**

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



        }).**Width("700")**

&lt;/div&gt;



[ASPX]

// Add the code in ASPX page

&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="700" runat="server"&gt;

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

**Open on click**

Specifies the sub menu items to be show or open only on click. It accepts the Boolean value. Its default value is false. If we set “**openOnClick**” property to true then the submenu items will open only on click. By default the submenu will open when we hover on menu items.

* Add the following **&lt;script&gt;** in the above code sample. 



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 612,
**openOnClick: true**
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**// Add the following code in the CSHTML page.** 

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



        }).Width("612").**OpenOnClick(true)**

&lt;/div&gt;



[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="500" OpenOnClick="true" runat="server"&gt;

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



Output screenshot for the above code example is as follows.

![](miscellaneous_images\miscellaneous_img1.png)

_Figure_ _41__: Sub menu items to open on click_

**Animation**

Animation type is used to enable or disable the Animation when hover or click on menu items. Its value type is string. It accepts two values such as “none” and “default”. Support to disable the Animation Type when hover or click on menu items is none. Support to enable the Animation Type when hover or click on menu items is default. 

* Add the following **&lt;script&gt;** in the above sample code. 



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 612,
**animationType: ej.AnimationType.Default**
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**// Add the following code in the CSHTML page.** 

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



        }).Width("612").**AnimationType(AnimationType.Default)**

&lt;/div&gt;





[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="500" AnimationType="Default" runat="server"&gt;

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


Output screenshot for the above code sample is as follows.

![](miscellaneous_images\miscellaneous_img2.png)

_Figure_ _42__27__: Animation_

**Title text**

Specifies the title to the responsive menu. You can provide title to the **Menu** control by using titleText property. 

* You can specify the title of the **Menu** control in the script as follows.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            titleText: "Title of the Menu"
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**// You can specify the title of the Menu control in the CSHTML page as follows.**

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



        }).Width("500").**TitleText("Title of the Menu")**

    &lt;/div&gt;





[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="500" TitleText="Title of the Menu" runat="server"&gt;

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





The following screenshot displays the output of the above code.

![](miscellaneous_images\miscellaneous_img3.png)

_Figure_ _43__28__: Title text for Responsive Layout_

**Show root level arrows**

Specifies the main menu item arrows to display only when it contains child menu items. You can use “**showRooltLevelArrows**” property to display the arrows of main menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

* Add the following **&lt;script&gt;** in the above code sample.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
        jQuery(function ($) {
            $("#menucontrol").ejMenu({
                width: 500,
                showRooltLevelArrows: false
            });
        });
    </script>


{% endhighlight %}



**[CSHTML]**

**// Add the following code in the CSHTML page.**

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



        }).Width("500").**ShowRooltLevelArrows(false)**

    &lt;/div&gt;





[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="500" ShowRooltLevelArrows="false" runat="server"&gt;

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



The following screenshot displays the output of the above code.

![](miscellaneous_images\miscellaneous_img4.png)

_Figure_ _44__29__: Show root level arrows_

**Show sub level arrows**

Specifies the sub menu items arrows to display only when it contains child menu items. You can use “**showSubLevelArrows**” property to show the arrows of sub menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

* Add the following **&lt;script&gt;** in the sample code.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
        jQuery(function ($) {
            $("#menucontrol").ejMenu({
                width: 500,
                showSubLevelArrows: false
            });
        });
    </script>


{% endhighlight %}



**[CSHTML]**

**// Add the following code in the CSHTML page.**

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



        }).Width("500").**ShowSubLevelArrows(false)**

    &lt;/div&gt;





[ASPX]

// Add the code in ASPX page



&lt;div class="imgframe"&gt;

        &lt;ej:Menu ID="keyboard" Width="500" ShowSubLevelArrows="false" runat="server"&gt;

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





The following screenshot displays the output of the above code.

![](miscellaneous_images\miscellaneous_img5.png)

_Figure_ _45__30__: Show sub level arrows_

