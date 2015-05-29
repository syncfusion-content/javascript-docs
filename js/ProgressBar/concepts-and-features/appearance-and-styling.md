---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: Progress Bar
documentation: ug
---

# Appearance and Styling

## Adjusting ProgressBar size

**ProgressBar** widget provides the ability to change or adjust the **ProgressBar** size. The ‘**height’** and ‘**width’** properties in the **ProgressBar** widget allows you to set the maximum height and maximum width for the **ProgressBar**. The value set to this property is **string or Number** type.

The following steps explain you on how to adjust the **ProgressBar** size.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code example to adjust the ProgressBar size (Number).&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({            value: 50,<b>            width: 400,</b><b>            height: 40</b>        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;(OR)Add the code to adjust the <b>ProgressBar </b>size (String).<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({            value: 50,<b>            width: "400px"“400px”,</b><b>            height: "40px"“40px”</b>        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b> [CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized size.</b>@Html.EJ().ProgressBar("progressbar").Value(40).<b>Height("40").Width("400")</b>        </td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});                         });        &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized size.</b> &lt;ej:ProgressBar ID="progressbar" runat="server" Value="40"  Height="40" Width="400" &gt;&lt;/ej:ProgressBar&gt;    </td></tr>
<tr>
<td>
<b>[JavaScript]</b>  &lt;script&gt;          var progress;          $(document).ready(function () {              progress = $("#progressbar").data("ejProgressBar");              progress.setModel({ text: progress.getValue() + " %"});          });    &lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output.



{% include image.html url="\js\ProgressBar\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img1.png" Caption=" Figure 19: Adjusting ProgressBar size"%}

## Custom text

**Custom text** is displayed when the **ProgressBar** shows different levels of progress in the **ProgressBar**. Support for **Custom text** to mention the percentage or any other message inside the **ProgressBar** is possible by using “**text**” property.

The following steps explain the configuration of the **Custom text** for the **ProgressBar** widget.

*   In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add Custom Text for the ProgressBar widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({            <b>text: "loading",</b>            value: 35,            height: 20,            width: 500        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized text.**



@Html.EJ().ProgressBar("progressbar").**Text("loading").**Value(40).Height("20").Width("500")



**[ASPX]**

**// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized text.**



 &lt;ej:ProgressBar ID="progressbar" runat="server"  Text="loading" Value="40"  Height="20" Width="500" &gt;&lt;/ej:ProgressBar&gt;







* The following screenshot displays the output.       {% include image.html url="\js\ProgressBar\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img2.png" Caption="    Figure 120: Custom Text in ProgressBar"%}

## Theme

The **ProgressBar** widget style and appearance are controlled based on **CSS** classes. In order to apply **Theme** to the **ProgressBar** widget, you can refer two files, namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project, as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes’ support available for the **ProgressBar** widget namely,

* Default-theme

* Flat-azure-dark

* Fat-lime

* Flat-lime-dark

* Flat-saffron

* Flat-saffron-dark

* Gradient-azure

* Gradient-azure-dark

* Gradient-lime

* Gradient-lime-dark

* Gradient-saffron

* Gradient-saffron-dark

## CSS class

To apply custom styles to the **ProgressBar** widget, you can specify the **cCssClass** property. The specified **CSS** name is added in the root of the **ProgressBar** widget.

The following code example is used to render the **ProgressBar** widget with customized style.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;        </td></tr>
<tr>
<td>
 <b>[JavaScript]</b>// Add the class for the ProgressBar Widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({<b>            cssClass: 'custom',</b>            value: 750,            height: 20,            width: 500        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + "%" });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized style.</b>@Html.EJ().ProgressBar("progressbar").Value(70).Height("20").Width("500").<b>CssClass("custom")</b>          </td></tr>
<tr>
<td>
<b>[JavaScript]</b>   &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});                         });        &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized style.</b>&lt;ej:ProgressBar ID="progressbar" runat="server" Value="70"  Height="20" Width="500" CssClass="custom" &gt;&lt;/ej:ProgressBar&gt;    </td></tr>
<tr>
<td>
<b> [JavaScript]</b>   &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});                         });        &lt;/script&gt;</td></tr>
</table>


* Add the following styles to render the **ProgressBar** with customized style.

{% highlight css %}

**[CSS]**

<style type="text/css">
    .custom .e-progress {
      background-color:gray;
    }

</style>


{% endhighlight %}



* The following screenshot displays the output.

{% include image.html url="\js\ProgressBar\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img3.png" Caption="      Figure 121: Appearance and styling in Progress BarProgressBar"%}

