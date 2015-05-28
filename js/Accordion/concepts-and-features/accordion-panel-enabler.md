---
layout: post
title: accordion-panel-enabler
description: accordion panel enabler
platform: js
control: Accordion 
documentation: ug
---

# Accordion Panel enabler

**Enable/Disable widget**

**You can enable or disable the Accordion** widget on initial rendering using the **enabled** property. By default **enabled** property is set to true and the **Accordion** panels are active always. 

 The following steps explain you on how to disable the **Accordion** widget

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>To disable the control set <b>enabled</b> property value as <b>false</b>            $("#accordion").ejAccordion({<b>                enabled:false</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and disable the control actions.**



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

            }).**Enabled(false)**.Render();}

&lt;/div&gt;



**[ASPX]**

**// In design page render Accordion with corresponding AccordionItems and disable the control using Enabled property.**



&lt;div style="width: 400px"&gt;

&lt;ej:Accordion ID="BasicAccordion" runat="server" Enabled="false"&gt;

        &lt;Items&gt;

            &lt;ej:AccordionItem Text="Orubase"&gt;

                &lt;ContentSection&gt;

                     Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe. 

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="WinRT XAML"&gt;

                &lt;ContentSection&gt;

                    Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Metro Studio"&gt;

                &lt;ContentSection&gt;

                    Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons. 

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



* Output for disabled **Accordion** control is as follows.



![](accordion-panel-enabler_images\accordion-panel-enabler_img1.png)

_Figure_ _22__12__: Disabled accordion widget_

**Enable panel items**

You can enable the **Accordion** widget items on initial loading using **enabledItems** property. This property takes array of indices whose panel needs to be enabled in **Accordion** widget. 

The **disabledItems** property disables the **Accordion** items based on the index. This takes array of indices whose panel is to be disabled. 

**Enabling accordion panel items**

The following steps explains you on how to enable the panel items in **Accordion** widget

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// To enable and disable accordion panel items set the values for enabledItems and disabledItems            $("#accordion").ejAccordion({<b>                enabledItems: [1, 2],</b><b>                disabledItems:[0],</b><b>                </b>selectedItemIndex:1,                enableMultipleOpen : true            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with the corresponding data, and to enable and disable Accordion panel items set the values for EnabledItems and DisabledItems.**



@{      //List of integer array with index values.

    List<int> enableditem = new List<int>() { 1, 2 };

    List<int> disableditem = new List<int>() { 0 };

}

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

            }).SelectedItemIndex(1).**EnabledItems(enableditem).DisableItems(disableditem)**.EnableMultipleOpen(true).Render();}

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b><b>// In Design page configure Accordion with corresponding AccordionItems and configure multiple open using EnableMultipleOpen property.</b>&lt;div style="width:400px"&gt;         &lt;ej:Accordion ID="BasicAccordion" runat="server" SelectedItemIndex="1" EnableMultipleOpen="true"&gt;    &lt;Items&gt;        &lt;ej:AccordionItem Text="Orubase"&gt;            &lt;contentsection&gt;                Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.             &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;        &lt;ej:AccordionItem Text="WinRT XAML"&gt;            &lt;contentsection&gt;                Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.            &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;        &lt;ej:AccordionItem Text="Metro Studio"&gt;            &lt;contentsection&gt;                Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.             &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;    &lt;/Items&gt;    &lt;/ej:Accordion&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CodeBehind – C#]</b>protected void Page_Load(object sender, EventArgs e)        {            List<int> enableditem = new List<int>() { 1, 2 };            List<int> disableditem = new List<int>() { 0 };            <b>this.BasicAccordion.EnabledItems = enableditem;</b><b>            this.BasicAccordion.DisableItems = disableditem;</b>        }</td></tr>
</table>


* Output for **Accordion** control with some enabled and disabled items, where first panel is disabled and it can’t be expanded or collapsed is as follows.



![](accordion-panel-enabler_images\accordion-panel-enabler_img2.png)

_Figure_ _23__13__: Accordion with disabled and enabled items_

