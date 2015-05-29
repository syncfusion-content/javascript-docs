---
layout: post
title: appearance-and-styling-
description: appearance and styling 
platform: js
control: WaitingPopup
documentation: ug
---

# Appearance and Styling 

## Custom Text

**WaitingPopup** control provides support for Custom Text to mention any message inside the pop-up panel.  You can specify a custom text through the option **text** that displays when the **Waiting PopupWaitingPopup** is loading.

The following steps explains you the configuration of the custom text for **WaitingPopup** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;                   &lt;div id="waitingPopUp"&gt;&lt;/div&gt;            &lt;/div&gt;  </td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add Custom Text for WaitingPopup control as follows.</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#waitingPopUp").ejWaitingPopup({            showOnInit: true,            <b>text</b>: "Loading... Please wait..."        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



&lt;div id="target"&gt;

        @Html.EJ().WaitingPopup("target").ShowOnInit(true).**Text("Loading... Please wait...")**

&lt;/div&gt;



**[ASPX]**

 &lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True" Text="Loading... Please wait..."&gt;&lt;/ej:WaitingPopup&gt;



* Add the following styles to render **WaitingPopup** widget.

{% highlight css %}

**[css]**

<style type="text/css" class="cssStyles">
    #waitingPopUpcontrol {
        height: 320px;
        width: 600px;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.



![](appearance-and-styling-_images\appearance-and-styling-_img1.png)

_Figure_ _16__8__: Custom Text in WaitingPopup_

## Template

**WaitingPopup** widget provides support for template to customize the appearance of it by including **HTML** content instead of the default image.

The following steps explains you on how to define template to display a text and image for **WaitingPopup** control.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **WaitingPopup** widget.



{% highlight html %}

**[HTML]**
<div class="control">               
    <div id="waitingPopUp"></div>            
</div>  


{% endhighlight %}



* Add customized template for **WaitingPopup** control using the following code example.



{% highlight html %}

<div id="content">
    <div class="block">
        <div class="logo"></div>
        <div class="txt">
            <p>Create cutting edge </p>
            <p><b>HTML5</b> web application </p>
            <p>with ease </p>
        </div>
    </div>
    <div class="loader"></div>
</div>


{% endhighlight %}



* Initialize the **WaitingPopup** with custom template using the following code example.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#waitingPopUp").ejWaitingPopup({
            showOnInit: true, 
            template: $("#content")
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**



&lt;div id="target"&gt;

    @Html.EJ().WaitingPopup("target").ShowOnInit(true).**Template("#content")**

    &lt;div id="content"&gt;

        &lt;div class="block"&gt;

            &lt;div class="logo"&gt;&lt;/div&gt;

            &lt;div class="txt"&gt;

                <p>Create cutting edge &lt;/p&gt;

                &lt;p&gt;<b>HTML5</b> web application &lt;/p&gt;

                <p>with ease &lt;/p&gt;

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;div class="loader"&gt;&lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



**[ASPX]**



&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True" Template="#content"&gt;**&lt;/ej:WaitingPopup&gt;**

    &lt;div id="content"&gt;

        &lt;div class="block"&gt;

            &lt;div class="logo"&gt;&lt;/div&gt;

            &lt;div class="txt"&gt;

                <p>Create cutting edge &lt;/p&gt;

                &lt;p&gt;<b>HTML5</b> web application &lt;/p&gt;

                <p>with ease &lt;/p&gt;

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;div class="loader"&gt;&lt;/div&gt;

    &lt;/div&gt;



* In **CSS**, you can configure the custom styles for **WaitingPopup**.


![C:\Users\ApoorvahR\Desktop\Note.png](appearance-and-styling-_images\appearance-and-styling-_img2.png)_**Note: Images for this sample are available ‘installed sample location /Content/images/waitingpopup’ and we need to define images in mentioned CSS. Henceforth the images will display.**_





{% highlight css %}

**[Stylesheet]**
<style type="text/css" class="cssStyles">
    #waitingPopUp {
        height: 320px;
        width: 600px;
        margin: 0 auto;
    }
    .block {
        height: 76px;
    }
    .logo {
        background-image: url("../images/waitingpopup/js_logo.png");
        float: left;
        height: 100%;
        width: 77px;
        margin-right: 15px;
    }
    .txt {
        float: left;
        font-size: 17px;
        height: 100%;
        text-align: left;
    }
    .txt p {
        margin: 0;
    }
    .loader {
        background: url("../images/waitingpopup/load_light.gif") no-repeat scroll -5px 18px transparent;
        height: 40px;
        width: 100%;
    }
    #content {
        cursor: default;
        height: 112px;
        width: 275px;
    }
</style><style type="text/css" class="cssStyles">
    #waitingPopUp {
        height: 320px;
        width: 600px;
        margin: 0 auto;
    }

        .block {
        height: 76px;
    }

    .logo {
        background-image: url("../Image/js_logo.png");
        float: left;
        height: 100%;
        width: 77px;
        margin-right: 15px;
    }

    .txt {
        float: left;
        font-size: 17px;
        height: 100%;
        text-align: left;
    }

    .txt p {
        margin: 0;
    }

    .loader {
        background: url("../Image/load_light.gif") no-repeat scroll -5px 18px transparent;
        height: 40px;
        width: 100%;
    }

    #content {
        cursor: default;
        height: 112px;
        width: 275px;
    }
</style>


{% endhighlight %}





Execute the above code to render the following output.


![](appearance-and-styling-_images\appearance-and-styling-_img3.png)![](appearance-and-styling-_images\appearance-and-styling-_img4.png)

_Figure_ _9__17__: WaitingPopup with Custom template_

## CSS Class

You can use the **CSS** class to customize the **WaitingPopup** control appearance. Define a **CSS** class as per requirement and assign the class name to **cssClass** property.

The following steps allows you to configure **CSS** class for an auto-complete textbox.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **WaitingPopup** widget.



{% highlight html %}

**[HTML]**
<div class="control">               
    <div id="waitingPopUp"></div>            
</div>  
**[JavaScript]**
**// Add the cssClass property to WaitingPopup widget as follows.**


<script type="text/javascript">
    $(function () {
        // declaration
        $("#waitingPopUp").ejWaitingPopup({
            showOnInit: true,
**cssClass: "customStyle",**
            text: "Loading.. Please wait..."
        });
    });
</script>


{% endhighlight %}





**[CSHTML]**



&lt;div id="target"&gt;

 @Html.EJ().WaitingPopup("target").ShowOnInit(true).**CssClass("custom").**Text("Loading... Please wait...")&lt;/div&gt;



**[ASPX]**



&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True" CssClass="custom" Text="Loading... Please wait..."&gt;&lt;/ej:WaitingPopup&gt;



* Define CSS class for customizing the WaitingPopup widget.



{% highlight css %}


**[CSS]**
<style type="text/css" class="cssStyles">
    /*Customize the panel property*/
    #waitingPopUp {
        height: 320px;
        width: 600px;
        margin: 0 auto;
    }
    /* Customize the WaitingPopup */
    .**customStyle**{
        background-color:darkred;
        font-style:italic;
        font-weight:bolder;
        opacity:0.5;
    }
</style>


{% endhighlight %}





The following screenshot displays the output for the above code.



![](appearance-and-styling-_images\appearance-and-styling-_img5.png)

_Figure_ _1__8__0__: WaitingPopup with customized CSS_





