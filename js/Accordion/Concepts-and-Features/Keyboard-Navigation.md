---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: js
control: Accordion 
documentation: ug
---

# Keyboard Navigation

You can use **Keyboard** shortcut keys as an alternative to the mouse on using Accordion widget using **allowKeyboardNavigation** property. However you will have to focus the control to enable the keyboard navigation. Accordion Widget allows you to perform all kind of actions using keyboard shortcuts.

_List of Keyboard shortcut keys_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a> + j	</td><td>
Focuses into the accordion control</td></tr>
<tr>
<td>
Up</td><td>
Moves to previous panel</td></tr>
<tr>
<td>
Down</td><td>
Moves to next panel</td></tr>
<tr>
<td>
Left</td><td>
Moves to previous panel</td></tr>
<tr>
<td>
Right</td><td>
Moves to next panel</td></tr>
<tr>
<td>
Home</td><td>
Moves to the first accordion panel</td></tr>
<tr>
<td>
End</td><td>
Moves to the last accordion panel</td></tr>
</table>
**Configure keyboard interaction**

The following steps explains you on how to enable keyboard interaction for an **Accordion** widget.

1. In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script&gt;    $(function () {        <b>//</b> Configure Keyboard navigation for <b>Accordion</b> by setting <b>allowKeyboardNavigation</b> property to <b>true</b>. Now define the script to focus the <b>Accordion</b> widget on AccessKey + J        $("#accordion").ejAccordion({          <b>allowKeyboardNavigation: true</b>       });      <b>// Define script to focus into the Accordion control on Alt + J shortcut keys.</b>        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#accordion").focus();            }        });    });&lt;/script&gt;</td></tr>
</table>


2. Output for Accordion widget focused and navigated to last item using Keyboard navigation is as follows.



{% include image.html url="/js/Accordion/Concepts-and-Features/Keyboard-Navigation_images/Keyboard-Navigation_img1.png" Caption=""%}

_Accordion with enabled keyboard navigation_

