---
layout: post
title: keyboard-navigation
description: keyboard navigation
platform: js
control: Tab Control
documentation: ug
---

# Keyboard Navigation

**Tab** control provides supports **keyboard** interaction. Using this functionality you can interact with control using keyboard. This is achieved by enabling ‘**allowKeyboardNavigation**’****to **‘true**’**.** By default this property value is set to ‘**true**’.

Following table illustrates the accessible key and their usage

<table>
<tr>
<td>
<b>Keys</b></td><td>
<b>Behavior</b></td></tr>
<tr>
<td>
Up</td><td>
Selected previous item.</td></tr>
<tr>
<td>
Right</td><td>
Selected previous item.</td></tr>
<tr>
<td>
Down</td><td>
Selected next item.</td></tr>
<tr>
<td>
Left</td><td>
Selected next item.</td></tr>
<tr>
<td>
Home</td><td>
Selected first item.</td></tr>
<tr>
<td>
End</td><td>
Selected last item.</td></tr>
</table>
The following code example is used to render the **Tab** element in **RTL** format. 

* Add the following **HTML** to render **Tab** with **keyboard** navigation.

<table>
<tr>
<td>
[HTML]&lt;div id="dishtype" style="width: 650px"&gt;    &lt;ul&gt;        &lt;li&gt;<a href="#pizza">Pizza Menu</a>&lt;/li&gt;        &lt;li&gt;<a href="#sandwich">Sandwich Menu</a>&lt;/li&gt;    &lt;/ul&gt;    &lt;div id="pizza" style="background-color: #F5F5F5"&gt;        &lt;!--Food item description--&gt;        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;    &lt;div id="sandwich" style="background-color: #F5F5F5"&gt;        &lt;!--dish description--&gt;        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
 [JS]// Add the following script to render Tab with keyboard navigation.&lt;script type="text/javascript"&gt;        $(function () {             $("#dishtype").ejTab({ allowKeyboardNavigation: true });                //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) {                // j- key code.                $("#dishtype ul a").focus();            }        });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
[CSHTML]// Add the following code example to the corresponding CSHTML page to render Tab with keyboard navigation.&lt;div style="width:550px"&gt;    @{Html.EJ().Tab("dishtab").Items(data =>           {               data.Add().ID("pizzatype").Text("Pizza Type")                   .ContentTemplate(@&lt;div&gt;                       Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.                   &lt;/div&gt;);               data.Add().ID("sandwichtype").Text("Sandwich Type")                   .ContentTemplate(@<div>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.               &lt;/div&gt;);           }).AllowKeyboardNavigation(true).Render();}&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script to render Tab with keyboard navigation.&lt;script type="text/javascript"&gt;        $(function () {        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) {                // j- key code.                $("#dishtab ul a").focus();            }        });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
[ASPX]// Add the following code example to the corresponding ASPX page to render Tab with keyboard navigation.    &lt;ej:Tab ID="dishtype" runat="server" Width="600px" AllowKeyboardNavigation="true"&gt;        &lt;Items&gt;            &lt;ej:TabItem Id="pizzatype" Text="Pizza Menu"&gt;                &lt;ContentSection&gt;                    <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;                &lt;/ContentSection&gt;            &lt;/ej:TabItem&gt;            &lt;ej:TabItem Id="sandwichtype" Text="Sandwich Menu"&gt;                &lt;ContentSection&gt;                    <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;                &lt;/ContentSection&gt;            &lt;/ej:TabItem&gt;        &lt;/Items&gt;    &lt;/ej:Tab&gt;</td></tr>
<tr>
<td>
[JS]// Add the following script to render Tab with keyboard navigation.&lt;script type="text/javascript"&gt;        $(function () {        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) {                // j- key code.                $("#dishtype ul a").focus();            }        });        });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot illustrates the **Tab** with **keyboard** navigation.

{% include image.html url="\js\Tab\concepts-and-features\keyboard-navigation_images\keyboard-navigation_img1.png" Caption="Figure 40: Tab with keyboard navigation"%}{% include image.html url="\js\Tab\concepts-and-features\keyboard-navigation_images\keyboard-navigation_img2.png" Caption="Figure 40: Tab with keyboard navigation"%}

