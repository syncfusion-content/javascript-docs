---
layout: post
title: getting-started
description: getting started
platform: js
control: Splitter
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Splitter** in your application with **JavaScript**, **ASP.NET MVC** and **ASP.NET**.

## Create your first Splitter in JavaScript

**Essential JavaScript****Splitter** widget consists of movable split bar(s) that divides a container's display area into two or more resizable and collapsible panels. 

From the following guidelines, you can create a **Splitter**, add Tree view in the **Splitter** and set actions to view the image. It is used to split the document or image and Expand or Collapse in the **Splitter**. The following screenshot demonstrates the functionality of **Splitter** widget.



{% include image.html url="\js\Splitter\getting-started_images\getting-started_img1.png" Caption="Figure 1: Splitter                                       "%}{% include image.html url="\js\Splitter\getting-started_images\getting-started_img2.png" Caption="Figure 1: Splitter                                       "%}

### Create Splitter Control

* Create an **HTML** file and add the following template in the **HTML** file.

{% highlight html %}

<!doctype html>

<html>
<head>
    <title>Essential Studio for JavaScript : Rotator Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
     <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>

<body>
    <!-- add Splitter element here --><!-- add Splitter element here --
</body>
</html>


{% endhighlight %}



Add **&lt;input&gt;** element to create **Splitter**. Save the images in the corresponding location.



{% highlight html %}

<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <!----------------Splitter Control---------------->
            <div id="outterSplitter">
                <div>
                    <div class="cont">
                        <h3 class="h3">ASP.NET MVC</h3>
                        <!-- Add the Tree View element here -->
                    </div>
                </div>
                <div>
                    <div class="cont">
                        <div class="_content">
                            Select any product from the tree to show the description.
                        </div>
                        <div class="tools des">
                            <h3>Mobile</h3>
                            <img src="galaxy.jpg" />
                        </div>
                        <div class="chart des">
                            <h3>Harddisk</h3>
                            <img src="harddisk.jpg" />
                        </div>
                        <div class="grid des">
                            <h3>Logo</h3>
                            <img src="right.jpg" />
                        </div>
                    </div>
                </div>
            </div>
            <!------------------------------------------------->
        </div>
    </div>
</div><div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <!----------------Splitter Control---------------->
            <div id="outterSplitter">
                <div>
                    <div class="cont">
                        <h3 class="h3">ASP.NET MVC</h3>
<!-- Add the Tree View element here -- >
                    </div>
                </div>
                <div>
    <div class="cont">
     <div class="_content">
      Select any product from the tree to show the description.
                        </div>
                        <div class="tools des">
                            <h3>Mobile</h3>
                            <img src="galaxy.jpg" />
                        </div>
                        <div class="chart des">
                            <h3>Harddisk</h3>
                            <img src="harddisk.jpg" />
                        </div>
                        <div class="grid des">
                            <h3>Logo</h3>
                        <img src="right.jpg" />
                        </div>
                    </div>
                </div>
            </div>
            <!------------------------------------------------->
        </div>
    </div>
</div>



{% endhighlight %}



Add the following styles to show the **Splitter** control in horizontal order.



{% highlight css %}

<style type="text/css" class="cssStyles">
     #outterSplitter {
            margin: 0 auto;
        }
        .cont {
            padding: 20px;
            min-width: 50px;
        }
            .cont #treeView_Container {
                margin-bottom: 0;
                border: none;
            }
        .h3 {
            font-size: 14px;
            margin: 0;
        }

        .des {
            display: none;
        }</style>


{% endhighlight %}

### Configure Tree View 

Add the following code example in **HTML** file to configure Tree View.



{% highlight html %}

<ul id="treeView" class="visibleHide">
    <li>
        Mobile
        <ul>
            <li id="tools" class="_child">Galaxy</li>
        </ul>
    </li>
    <li>
        Harddisk
        <ul>
            <li id="chart" class="_child">Segate </li>
        </ul>
    </li>
    <li>
        Logo
        <ul>
            <li id="grid" class="_child">Amazon</li>
        </ul>
    </li>
</ul><ul id="treeView" class="visibleHide">
                            <li>
                                Mobile
                                <ul>
                                    <li id="tools" class="_child">Galaxy</li>
                                </ul>
                            </li>
                            <li>
                                Harddisk
                                <ul>
                                    <li id="chart" class="_child">Segate </li>
                                </ul>
                            </li>
                            <li>
                                Logo
                                <ul>
                                    <li id="grid" class="_child">Amazon</li>
                                </ul>
                            </li>
                        </ul>



{% endhighlight %}

### Set Actions

Add the following code example in the view page to set the action to view the image.



{% highlight js %}


<script type="text/javascript">
    $(function () {
        $("#treeView").ejTreeView({ nodeSelect: "treeClicked" });
        $("#outterSplitter").ejSplitter({
            height: 280, width: 501,
            properties: [{ paneSize: 200 }]
        });
    });
    function treeClicked(sender, args) {
        if (sender.currentElement.hasClass('_child')) {
            var content = $('.' + sender.currentElement[0].id).html();
            $('._content').html(content);
        }
    }
</script>


{% endhighlight %}



The following screenshot is the output for the above code.



{% include image.html url="\js\Splitter\getting-started_images\getting-started_img3.png" Caption="Figure 2: Splitter action to view image"%}{% include image.html url="\js\Splitter\getting-started_images\getting-started_img4.png" Caption="Figure 2: Splitter action to view image"%}

## Create your first Splitter in MVC

**ASP.NET MVC****Splitter** control consists of movable split bar(s) that divides the container's display area into two or more resizable and collapsible panels. Refer the following guidelines to create a **Splitter**, add tree view in the **Splitter** and how to set actions to view the image that is used to split the document or image and also Expand or Collapse the **Splitter**. 

The following screenshot illustrates a **Splitter** control.



{% include image.html url="\js\Splitter\getting-started_images\getting-started_img5.png" Caption="Figure 3: Splitter"%}

**Create a Splitter**

**Essential Studio ASP.NET MVC Splitter** control has a built-in feature to split the display into horizontal and vertical order.

1. Create an **MVC** Project and add required assemblies, scripts, and styles to it.  Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code example to the corresponding view page to render the **Splitter**. Move the images under the folder **~/Images/mail**



    @{Html.EJ().Splitter("outterSplitter").PaneProperties(p =>

    {

        p.Add().ContentTemplate(

            @&lt;div class="cont"&gt;

                &lt;h3 class="h3"&gt;

                             ASP.NET MVC

                &lt;/h3&gt;

&lt;!—Add the Tree View Element here--&gt;

 &lt;/div&gt;).PaneSize("200");

        p.Add().ContentTemplate(

            @&lt;div class="cont"&gt;

                &lt;div class="_content"&gt;

                    Select any product from the tree to show the description.

                &lt;/div&gt;

                &lt;div class="tools des"&gt;

                    &lt;h3&gt;

                        Mobile

                    &lt;/h3&gt;

                    &lt;p&gt;

                        &lt;img src="@Url.Content("~/Images/mail/galaxy.jpg")" &gt;

                    &lt;/p&gt;

                &lt;/div&gt;

                &lt;div class="chart des"&gt;

                    &lt;h3&gt;

                        Harddisk

                    &lt;/h3&gt;

                    &lt;p&gt; &lt;img src="@Url.Content("~/Images/mail/harddisk.jpg")"&gt;&lt;/p&gt;

                &lt;/div&gt;

                &lt;div class="grid des"&gt;

                    &lt;h3&gt;

                        Logo

                    &lt;/h3&gt;

                    &lt;p&gt;

                        &lt;img src="@Url.Content("~/Images/mail/right.jpg")"&gt;

                    &lt;/p&gt;

                &lt;/div&gt;

            &lt;/div&gt;).PaneSize("200");})

.Height("400").Width("100%").Render();}



3. Add the following style in the view page to set the height and width of the **Splitter**.



        &lt;style type="text/css" class="cssStyles"&gt;

    #outterSplitter {

        margin: 0 auto;

    }

    .cont #treeView_Container {

        margin-bottom: 0;

        border: none;

    }

    .h3, ._content, p {

        font-size: 14px;

        margin-top: 10px;

        text-indent: 10px;

    }

    .des {

        display: none;

    }

&lt;/style&gt;

**Configure Tree View**

Add the following code example in the corresponding view page.



&lt;ul id="treeView" class="visibleHide"&gt;

                    &lt;li&gt;

                        Mobile

                        &lt;ul&gt;

                            <li id="tools" class="_child">Galaxy</li>

                        &lt;/ul&gt;

                    &lt;/li&gt;

                    &lt;li&gt;

                        Harddisk

                        &lt;ul&gt;

                            <li id="chart" class="_child">Segate &lt;/li&gt;

                        &lt;/ul&gt;

                    &lt;/li&gt;

                    &lt;li&gt;

                        Logo

                        &lt;ul&gt;

                            <li id="grid" class="_child">Amazon</li>

                        &lt;/ul&gt;

                    &lt;/li&gt;

                &lt;/ul&gt;

**Set Actions to Splitter control to view the image**

Add the following code example in the view page to set action in **Splitter** control to view the image.



    &lt;script type="text/javascript"&gt;

        $(function () {

            $("#treeView").ejTreeView({ nodeSelect: "treeClicked" });

        });

        function treeClicked(sender, args) {

            if (sender.currentElement.hasClass('_child')) {

                var content = $('.' + sender.currentElement[0].id).html();

                $('._content').html(content);

            }

        }

    &lt;/script&gt;



Execute the above code example to render the following output.



{% include image.html url="\js\Splitter\getting-started_images\getting-started_img6.png" Caption="Figure 4: Splitter action to view the image     "%}

## Create your first Splitter in ASP.NET

**ASP.NET****Splitter** control consists of movable split bar(s) that divides a container's display area into two or more resizable and collapsible panels. 

From the following guidelines, you can create a **Splitter**, add Tree view in the **Splitter** and set actions to view the image. It is used to split the document or image and Expand or Collapse in the **Splitter**. The following screenshot demonstrates the functionality of **Splitter** widget.



![](getting-started_images\getting-started_img7.png)

_Figure_ _5__: Splitter___

**Create Splitter Control**

* You can create an **ASP.NET Web Forms** Project and add necessary **Dll’s** and scripts with the help of the given [ ASP.NET -Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* Add the following code example to the corresponding **ASPX** page to render **Splitter**. 



&lt;div class="content-container-fluid"&gt;

        &lt;div class="row"&gt;

            &lt;div class="cols-sample-area"&gt;

                &lt;ej:Splitter ID="outterSplitter" runat="server" Height="280" Width="501"&gt;

                    &lt;ej:SplitPane PaneSize="200"&gt;

                        &lt;div&gt;

                            &lt;div class="cont"&gt;

                                &lt;h3 class="h3"&gt;

                                    ASP.NET</h3>

&lt;%--add tree view control here--%&gt;

                            &lt;/div&gt;

                        &lt;/div&gt;

                    &lt;/ej:SplitPane&gt;

                    &lt;ej:SplitPane PaneSize="200"&gt;

                        &lt;div&gt;

                            &lt;div class="cont"&gt;

                                &lt;div class="_content"&gt;

                                    Select any product from the tree to show the description.

                                &lt;/div&gt;

                                &lt;div class="tool des"&gt;

                                    &lt;h3&gt;

                                        Tools</h3>

                                    &lt;img src="galaxy.jpg" /&gt;

                                &lt;/div&gt;

                                &lt;div class="chart des"&gt;

                                    &lt;h3&gt;

                                        Chart</h3>

                                    &lt;img src="hard.jpg" /&gt;

                                &lt;/div&gt;

                                &lt;div class="grid des"&gt;

                                    &lt;h3&gt;

                                        Grid</h3>

                                    &lt;img src="amazon.png" /&gt;

                                &lt;/div&gt;

                            &lt;/div&gt;

                        &lt;/div&gt;

                    &lt;/ej:SplitPane&gt;

                &lt;/ej:Splitter&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



* Add the following styles to show the **Splitter** control in horizontal order.



&lt;style type="text/css" class="cssStyles"&gt;

        . #outterSplitter

        {

            margin: 0 auto;

        }

        .cont

        {

            padding: 20px;

            min-width: 50px;

        }

        .cont #treeView_Container

        {

            margin-bottom: 0;

            border: none;

        }

        .h3

        {

            font-size: 14px;

            margin: 0;

        }



        .des

        {

            display: none;

        }

    &lt;/style&gt;



**Configure Tree View** 

Add the following code example in **ASPX** file to configure Tree View. Refer the following link to know more details on **TreeView** control.

[http://help.syncfusion.com/ug/js/documents/createyourfirsttreev.htm](http://help.syncfusion.com/ug/js/documents/createyourfirsttreev.htm)



&lt;ej:TreeView ID="TreeView" runat="server" ClientSideOnNodeSelected="treeClicked"&gt;

                                &lt;Nodes&gt;

                                    &lt;ej:TreeViewNode Text="Tools"&gt;

                                        &lt;Nodes&gt;

                                            &lt;ej:TreeViewNode Text="Description" Id="tool"&gt;

                                            &lt;/ej:TreeViewNode&gt;

                                        &lt;/Nodes&gt;

                                    &lt;/ej:TreeViewNode&gt;

                                    &lt;ej:TreeViewNode Text="Chart"&gt;

                                        &lt;Nodes&gt;

                                            &lt;ej:TreeViewNode Text="Description" Id="chart"&gt;

                                            &lt;/ej:TreeViewNode&gt;

                                        &lt;/Nodes&gt;

                                    &lt;/ej:TreeViewNode&gt;

                                    &lt;ej:TreeViewNode Text="Grid"&gt;

                                        &lt;Nodes&gt;

                                            &lt;ej:TreeViewNode Text="Description" Id="grid"&gt;

                                            &lt;/ej:TreeViewNode&gt;

                                        &lt;/Nodes&gt;

                                    &lt;/ej:TreeViewNode&gt;

                                &lt;/Nodes&gt;

                            &lt;/ej:TreeView&gt;

**Set Actions**

Add the following code example in the **ASPX** page to set the action to view the image.





&lt;script type="text/javascript"&gt;

    function treeClicked(sender, args) {



var content = $('.' + sender.currentElement[0].id).html();

            $('._content').html(content);

    }

&lt;/script&gt;



The following screenshot is the output for the above code.



![](getting-started_images\getting-started_img8.png)

_Figure_ _6__: Splitter action to view image_

