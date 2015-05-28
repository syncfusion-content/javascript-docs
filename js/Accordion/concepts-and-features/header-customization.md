---
layout: post
title: header-customization
description: header customization
platform: js
control: Accordion 
documentation: ug
---

# Header customization

**Collapsible**

**Accordion** widget allows you to set Collapsible state for an **Accordion** header. Thus you can expand and collapse accordion contents. By default **collapsible** is set to **false**.

**Enable Collapsible settings**

The following steps explains to enable Collapsible state for **Accordion**.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]	</b>// Configure collapsible header for <b>Accordion</b>            $("#accordion").ejAccordion({                <b>collapsible:true</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and enable Collapsible property.**



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

               }).**Collapsible(true)**.Render();}

&lt;/div&gt;





**[ASPX]**

**// In Design page render Accordion with corresponding AccordionItems and enable the Collapsible property**



&lt;div style="width:400px"&gt;     

    &lt;ej:Accordion ID="BasicAccordion" runat="server" Collapsible="true"&gt;

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





* Output for **Accordion** control with collapsible headers.


![](header-customization_images\header-customization_img1.png)

_Figure_ _16__6__: Accordion with collapsible headers_

**Enable Header expand**

**Accordion** widget provides you support to set the event, where the headers should expand and collapse. The **events** properties takes default events like mouseout, mouseover, and click.

**Configure header expand event**

The following steps explains you to configure header expand event for **Accordion**.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Configure header expand event for <b>Accordion</b><br>            $("#accordion").ejAccordion({                <b>events: "mouseout"</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and configure the Events property.**



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

               }).**Events("mouseout")**.Render();}

&lt;/div&gt;



**[ASPX]**

**//  In Design page render Accordion with corresponding AccordionItems and configure the Events property**

&lt;div style="width:400px"&gt;     

    &lt;ej:Accordion ID="BasicAccordion" runat="server" Events="mouseout"&gt;

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





* Output for **Accordion** control that expands header on **mouseout** event is as follows.


![](header-customization_images\header-customization_img2.png)

_Figure_ _17__7__: Accordion header expand/collapse on “mouseout” event_

**Set selected header**

**Single selection**

Using **selectedItemIndex** property you can modify the expanded panel when the control is rendered. By default **selectedItemIndex** is ‘0’ that always activate the first **Accordion** panel.

**Specify the selected item in Accordion panel**

The following steps explains you to configure selected item for **Accordion**.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Configure selected item for <b>Accordion</b> based on the index            $("#accordion").ejAccordion({<b>                selectedItemIndex: 1</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and configure selected item for Accordion based on the index.**





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

               }).**SelectedItemIndex(2)**.Render();}

&lt;/div&gt;



**[ASPX]**

**//  In Design page render Accordion with corresponding AccordionItems and configure selected item for accordion based on the index**



&lt;div style="width:400px"&gt;     

    &lt;ej:Accordion ID="BasicAccordion" runat="server" SelectedItemIndex="2"&gt;

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



* Output for **Accordion** control with the selected item by index is as follows.

![](header-customization_images\header-customization_img3.png)

_Figure_ _18__8__: Accordion control configured with “selectedItemIndex”_

**Multiple selection**

In **Accordion** widget you can select multiple panel items using **selectedItems** property. It takes array of indices that needs to be selected on rendering the control. As you need to select multiple items, you can set **enableMultipleOpen** to **true**.

**Configure multiple selection in Accordion panel**

The following steps explains to configure selected items for **Accordion**.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Configure multiple item selection for <b>Accordion</b>            $("#accordion").ejAccordion({<b>                selectedItems:[0,2],</b><b>                enableMultipleOpen : true</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and configure multiple items selection for Accordion.**





&lt;div style="width: 400px"&gt;

    @{      //List of integer array with index values.

        List<int> selecteditem = new List<int>() { 0, 1, 2 };

    }

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

               })**.SelectedItems(selecteditem).EnableMultipleOpen(true).**Render();}

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b><b>// In ASPX page render Accordion with corresponding AccordionItems and set EnableMultipleOpen as true.</b>&lt;div style="width:400px"&gt;         &lt;ej:Accordion ID="BasicAccordion" runat="server" EnableMultipleOpen="true"&gt;    &lt;Items&gt;        &lt;ej:AccordionItem Text="Orubase"&gt;            &lt;contentsection&gt;                Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.             &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;        &lt;ej:AccordionItem Text="WinRT XAML"&gt;            &lt;contentsection&gt;                Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.            &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;        &lt;ej:AccordionItem Text="Metro Studio"&gt;            &lt;contentsection&gt;                Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.             &lt;/contentsection&gt;        &lt;/ej:AccordionItem&gt;    &lt;/Items&gt;    &lt;/ej:Accordion&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CodeBehind – C#]</b>protected void Page_Load(object sender, EventArgs e)        {            List<int> SelectedItems = new List<int>() { 0, 2 };            <b>this.BasicAccordion.SelectedItems = SelectedItems;</b>        }</td></tr>
</table>


* Output for **Accordion** control with the multiple selected items is as follows.


![](header-customization_images\header-customization_img4.png)

_Figure_ _19__9__: Accordion with multiple selected items_

