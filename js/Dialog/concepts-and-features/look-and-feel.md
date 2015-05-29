---
layout: post
title: look-and-feel
description: look and feel
platform: js
control: Dialog
documentation: ug
---

# Look and Feel

You can customize the appearance of **Dialog** widget using various themes that are available in **Essential JavaScript**. Applying themes customizes the entire control and its appearances. Refer the following link.
[http://help.syncfusion.com/ug/js/Documents/theming.htm](http://help.syncfusion.com/ug/js/Documents/theming.htm)

## CSS Class

The **CSS** properties can be customized by using **cssCSS** Class in the **Dialog** control. The following steps explains the implementation of css**CSS** Class option in the **Dialog** widget.

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass</b> property to the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            cssClass: "customCss"</b>        });    &lt;/script&gt;</td></tr>
</table>




**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and assign the CssClass value from the custom class name.**





@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@&lt;div&gt;

The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**CssClass("customCss").**Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and assign the CssClass property from custom class.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" Title="Syncfusion Dialog" CssClass="customCss"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt; 





* Customize the **CSS** class by setting **CSS** Properties. 



{% highlight css %}

**[CSS]**

    <style>
        .customCss {            
            border-color: #661e19 !important;
        }

        /*Customize the dialog header*/
        .customCss .e-header {
            background-color: #2c683b;
        }

        /*Customize the dialog content*/
        .customCss .e-dialog, .customCss .e-dialog-scroller {
          color: #b21010;
          background-color: #f6e492;        
         }
    </style>



{% endhighlight %}



* The output for **Dialog** control after customizing the “**cssClass**” is as follows.

![C:\Users\ApoorvahR\Desktop\13.png](look-and-feel_images\look-and-feel_img1.png)

_Figure_ _43__33__: Dialog with “cssClass"_















