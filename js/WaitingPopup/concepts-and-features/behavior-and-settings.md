---
layout: post
title: behavior-and-settings
description: behavior and settings
platform: js
control: WaitingPopup
documentation: ug
---

# Behavior and Settings

## Automatic Initializing WaitingPopup widget

**WaitingPopup** widget contains **showOnInit** property that allows the popup to display over a target on page load automatically. By default, **showOnInit** property is set as false.

The following steps explains you on how to display the **WaitingPopup** on page load.

* In an **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;                   &lt;div id="waitingPopUp"&gt;&lt;/div&gt;            &lt;/div&gt;  </td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Configure the WaitingPopup to display automatically on page load as follows.</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#waitingPopUp").ejWaitingPopup({            <b>showOnInit</b>: true,        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



&lt;div id="target"&gt;

    @Html.EJ().WaitingPopup("target").**ShowOnInit(true)**

&lt;/div&gt;



**[ASPX]**

&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True"&gt;**&lt;/ej:WaitingPopup&gt;**



* Add the following styles to render **WaitingPopup** widget.



{% highlight css %}

**[css]**

<style type="text/css" class="cssStyles">
    #waitingPopUp control {
        height: 320px;
        width: 600px;
    }
</style>


{% endhighlight %}



The following screenshot illustrates the **WaitingPopup** when **showOnInit** is set to “**true**”.

![](behavior-and-settings_images\behavior-and-settings_img1.png)

_Figure_ _4__12__: WaitingPopup with enabled showOnInit property_

## Enable / Disable Popup Indicator

You can show or hide the popup indicator of **WaitingPopup** widget using **showImage** property. By default, **showImage** property is set as **true**.

The following steps explains you to enable / disable popup indicator in **WaitingPopup** widget.

* In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;                   &lt;div id="waitingPopUp"&gt;&lt;/div&gt;            &lt;/div&gt;  </td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// To configure Enable / Disable popup indicator in WaitingPopup, use the following code.</b><b>Enable popup indicator:</b>$(function () {    // declaration    $("#waitingPopUp").ejWaitingPopup({        showOnInit: true,        <b>showImage: true,</b>         text: "Loading... Please wait..."    });});<b>Disable popup indicator:</b>$(function () {    // declaration    $("#waitingPopUp").ejWaitingPopup({        showOnInit: true,        <b>showImage: false,</b><b>        </b>text: "Loading... Please wait..."    });});</td></tr>
</table>


**[CSHTML]**



**Enable popup indicator:**

&lt;div id="target"&gt;

    @Html.EJ().WaitingPopup("target").ShowOnInit(true).**ShowImage(true).**Text("Loading... Please wait...")



&lt;/div&gt;



**Disable popup indicator:**

&lt;div id="target"&gt;

   @Html.EJ().WaitingPopup("target").ShowOnInit(true).**ShowImage(false).**Text("Loading... Please wait...")

&lt;/div&gt;



**[ASPX]**

**Enable popup indicator:**

&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True" ShowImage="true" Text="Loading... Please wait..."&gt;&lt;/ej:WaitingPopup&gt;



**Disable popup indicator:**

&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True" ShowImage="false" Text="Loading... Please wait..."&gt;&lt;/ej:WaitingPopup&gt;



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

![](behavior-and-settings_images\behavior-and-settings_img2.png)

_Figure_ _5__13__: Enabled popup indicator WaitingPopup widget_

![](behavior-and-settings_images\behavior-and-settings_img3.png)

_Figure_ _6__14__: Disabled popup indicator WaitingPopup widget_

## Show / Hide WaitingPopup

Using **show()** and **hide()** methods, you can display or hide the **WaitingPopup** widget over the target area.

The following steps explains you to show / hide the **WaitingPopup** widget.

* In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;                   &lt;div id="waitingPopUp"&gt;&lt;/div&gt;            &lt;/div&gt;  </td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use the following code to Show / Hide WaitingPopup.</b><b>Show WaitingPopup:</b>$(function () {    $("#waitingPopUp").ejWaitingPopup();    var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");    popUpObj.show();});<b>Hide WaitingPopup:</b>$(function () {    $("#waitingPopUp").ejWaitingPopup();    var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");    popUpObj.hide();});</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>&lt;div id="target"&gt;    @Html.EJ().WaitingPopup("target").<b>ShowOnInit(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>Show WaitingPopup:</b>&lt;script type="text/javascript"&gt;    var popUpObj;    $(function () {        $("#target").ejWaitingPopup();        popUpObj = $("#target").data("ejWaitingPopup");        popUpObj.show();    });&lt;/script&gt;<b>Hide WaitingPopup:</b>&lt;script type="text/javascript"&gt;    var popUpObj    $(function () {        $("#target").ejWaitingPopup();         popUpObj = $("#target").data("ejWaitingPopup");        popUpObj.hide();    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>&lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="True"&gt;&lt;/ej:WaitingPopup&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>Show WaitingPopup:</b>&lt;script type="text/javascript"&gt;    var popUpObj;    $(function () {        $("#target").ejWaitingPopup();        popUpObj = $("#target").data("ejWaitingPopup");<b>        popUpObj.show();</b>    });&lt;/script&gt;<b>Hide WaitingPopup:</b>&lt;script type="text/javascript"&gt;    var popUpObj    $(function () {        $("#target").ejWaitingPopup();         popUpObj = $("#target").data("ejWaitingPopup");        <b>popUpObj.hide();</b>    });&lt;/script&gt;</td></tr>
</table>




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



The following screenshot illustrates a **WaitingPopup** when **show()** method is invoked.

![](behavior-and-settings_images\behavior-and-settings_img4.png)

_Figure_ _15__7__: WaitingPopup with show() method_

