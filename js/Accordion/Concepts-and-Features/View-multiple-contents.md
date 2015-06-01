---
layout: post
title: View-multiple-contents
description: view multiple contents
platform: js
control: Accordion 
documentation: ug
---

# View multiple contents

By default **Accordion** allows only one panel to be in expanded state. You can enable multiple panels in expand state by setting **enableMultipleOpen** to **true.**

**Enabling multiple panel open**

The following steps explains you to enable multiple panel for **Accordion**.

1. In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Enable multiple open for <b>Accordion</b>            $("#accordion").ejAccordion({<b>                enableMultipleOpen: true</b>            });</td></tr>
</table>


2. Following screenshot is the output for Accordion control on enableMultipleOpen set to true.


{% include image.html url="/js/Accordion/Concepts-and-Features/View-multiple-contents_images/View-multiple-contents_img1.png" Caption="Accordion with Multiple expanded panel"%}

