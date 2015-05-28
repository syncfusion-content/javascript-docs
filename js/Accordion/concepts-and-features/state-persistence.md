---
layout: post
title: state-persistence
description: state persistence
platform: js
control: Accordion 
documentation: ug
---

# State Persistence

**Accordion** widget can store the model value in the browser cookies and on every time after initial rendering, the control get the model from the cookie only. Using **enablePersistence** property you can store the model value in cookies. Thus when any changes are made dynamically then those values are updated in cookie. On refreshing the page the past state of the **Accordion** control is maintained in cookie and control is rendered from it.

**Configure state persistence of Accordion panel**

The following steps explains to enable state maintenance for **Accordion**.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Configure <b>enablePersistence</b> for <b>Accordion</b>            $("#accordion").ejAccordion({<b>                enablePersistence:true</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with corresponding data and enable the state persistence.**



&lt;div style="width: 400px"&gt;

@{Html.EJ().Accordion("accordion").Items(data =>

            {

                data.Add().Text("Essential Chart").ContentTemplate(@&lt;div&gt;

                    Essential Chart for ASP.NET MVC is a visually stunning, high-performance charting component that is easy to use. It includes 35 chart types ranging from simple column charts to specialized financial charts. The charts are highly customizable and have a powerful data model that makes data binding simple.

                &lt;/div&gt;);

                data.Add().Text("Essential Schedule").ContentTemplate(@&lt;div&gt;

                    Essential Schedule for ASP.NET MVC is an Outlook Calendar-like scheduler control that lets you add rich scheduling capabilities to your web applications. It includes an advanced set of features including data binding, multiple resource views, rich interactivity, support for AJAX, client-side events, and much more.

                &lt;/div&gt;);

                data.Add().Text("Essential Grid").ContentTemplate(@&lt;div&gt;

                    Essential Grid for ASP.NET MVC is a feature-rich control that provides extensive appearance customization options with support for grouped records. With Essential Grid for ASP.NET MVC, you can create a grid with a highly customizable look and feel. This grid is very useful for generating complex grid-based reports with rich formatting. It supports paging, sorting, grouping, filtering, and editing features. It also supports a JSON mode in which you can handle all the operations like paging and sorting. The performance of these operations in the JSON mode will be much faster than if the grid were to handle them. Essential Grid generates clean HTML in compliance with XHTML 1.0. It supports any kind of IEnumerable data source. It uses LINQ data retrieval techniques for handling data sources, and offers high performance.&lt;/div&gt;);

            }).**EnablePersistence(true)**.Render();}

&lt;/div&gt;



**[ASPX]**

**// In Design page configure Accordion with corresponding AccordionItems and enable the state persistence**



&lt;div style="width:400px"&gt;     

    &lt;ej:Accordion ID="BasicAccordion" runat="server" EnablePersistence="true"&gt;

    &lt;Items&gt;

        &lt;ej:AccordionItem Text="Orubase"&gt;

            &lt;contentsection&gt;

                Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe. 

            &lt;/contentsection&gt;

        &lt;/ej:AccordionItem&gt;

        &lt;ej:AccordionItem Text="WinRT XAML"&gt;

            &lt;contentsection&gt;

                Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.

            &lt;/contentsection&gt;

        &lt;/ej:AccordionItem&gt;

        &lt;ej:AccordionItem Text="Metro Studio"&gt;

            &lt;contentsection&gt;

                Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons. 

            &lt;/contentsection&gt;

        &lt;/ej:AccordionItem&gt;

    &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;





* Output after page refresh maintaining the previous state of **Accordion** widget is as follows.



![](state-persistence_images\state-persistence_img1.png)

_Figure_ _24__14__: Accordion with state persistence_

