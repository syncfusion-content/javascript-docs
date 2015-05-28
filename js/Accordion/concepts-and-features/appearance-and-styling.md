---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: Accordion 
documentation: ug
---

# Appearance and Styling

**Adjusting Accordion size**

You can customize the **Accordion** panel height using **heightAdjustMode** property. It can be set to **enum** values like content, fill or auto. By default **heightAdjustMode** is set to **content** so the panel height is adjusted to the content size.

**Configure Height of Accordion panel**

The following steps explains you on how to configure **Accordion** panel height.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Configure <b>heightAdjustMode</b> for accordion            $("#accordion").ejAccordion({                <b>heightAdjustMode: "auto"</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with corresponding data and define HeightAdjustMode.**



&lt;div style="width:850px"&gt;

&lt;div style="width: 400px; float:left;"&gt;

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

        }).**HeightAdjustMode(HeightAdjustMode.Auto)**.Render();}

&lt;/div&gt;

&lt;div style="width: 400px; float:right;"&gt;

@{Html.EJ().Accordion("accordionfill").Items(data =>

        {

            data.Add().Text("Essential Chart").ContentTemplate(@&lt;div&gt;

                Essential Chart for ASP.NET MVC is a visually stunning, high-performance charting component that is easy to use. It includes 35 chart types ranging from simple column charts to specialized financial charts. The charts are highly customizable and have a powerful data model that makes data binding simple.

            &lt;/div&gt;);

            data.Add().Text("Essential Schedule").ContentTemplate(@&lt;div&gt;

                Essential Schedule for ASP.NET MVC is an Outlook Calendar-like scheduler control that lets you add rich scheduling capabilities to your web applications. It includes an advanced set of features including data binding, multiple resource views, rich interactivity, support for AJAX, client-side events, and much more.

            &lt;/div&gt;);

            data.Add().Text("Essential Grid").ContentTemplate(@&lt;div&gt;

                Essential Grid for ASP.NET MVC is a feature-rich control that provides extensive appearance customization options with support for grouped records. With Essential Grid for ASP.NET MVC, you can create a grid with a highly customizable look and feel. This grid is very useful for generating complex grid-based reports with rich formatting. It supports paging, sorting, grouping, filtering, and editing features. It also supports a JSON mode in which you can handle all the operations like paging and sorting. The performance of these operations in the JSON mode will be much faster than if the grid were to handle them. Essential Grid generates clean HTML in compliance with XHTML 1.0. It supports any kind of IEnumerable data source. It uses LINQ data retrieval techniques for handling data sources, and offers high performance.&lt;/div&gt;);

        }).**HeightAdjustMode(HeightAdjustMode.Fill)**.Render();}

&lt;/div&gt;

&lt;/div&gt;



**[ASPX]**

**// In design page configure Accordion with corresponding AccordionItems and define the HeightAdjustMode**



&lt;div style="width: 850px"&gt;

    &lt;div style="width: 400px; float: left;"&gt;

    &lt;h3&gt;<span>Auto Mode</span>&lt;/h3&gt;

    &lt;ej:Accordion ID="AccordionAuto" runat="server" HeightAdjustMode="Auto"&gt;

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



    &lt;div style="width: 400px; float: right;"&gt;

    &lt;h3&gt;<span>Fill Mode</span>&lt;/h3&gt;

    &lt;ej:Accordion ID="AccordionFill" runat="server" HeightAdjustMode="Fill"&gt;

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

&lt;/div&gt;





* Output for **Accordion** control when panel height is set to **auto** so that the maximum content height and **Fill** for minimum content height in all the panels is as follows.



![](appearance-and-styling_images\appearance-and-styling_img1.png)

_Figure_ _25__15__: Accordion height set to auto adjust mode_

**Rounded corner**

You can customize the shape of the **Accordion** widget from regular rectangular shape to rounded rectangle shape enabling **roundedCorner property** that is set to false by default.

**Enabling Rounded corner property**

The following steps explains you in enabling the **showRoundedCorner** property for an **Accordion** control.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable <b>showRoundedCorner</b> for <b>Accordion</b>    $("#accordion").ejAccordion({                <b>showRoundedCorner</b>: <b>true</b>            }); </td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with corresponding data and enable the ShowRoundedCorner property for it.**



&lt;div style="width: 400px; float:left;"&gt;

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

        }).**ShowRoundedCorner(true).**Render();}

&lt;/div&gt;



**[ASPX]**

**// In Design page configure Accordion with corresponding AccordionItems and enable the ShowRoundedCorner property for it.**



&lt;div style="width: 400px;"&gt;

    &lt;ej:Accordion ID="BasicAccordion" runat="server" ShowRoundedCorner="true"&gt;

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





* Output for accordion widget when “**showRoundedCorner**” is set to “**true**” is as follows.


![C:\Users\ApoorvahR\Desktop\8.png](appearance-and-styling_images\appearance-and-styling_img2.png)

_Figure_ _26__16__: Accordion with Rounded rectangular appearance_

**Customize Accordion icon**

**Accordion** widget allows you to customize the icons using **customIcon** option that has two properties **header** and **selectedHeader**. By default, the classes of header and selectedHeader are e-collapse and e-expand respectively. By setting the desired CSS class names for these properties as required overrides the default icons with customized icons.

**Configuring custom icon for Accordion**

The following steps explains you the configuration of icon for an **Accordion** control.

* In an **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Set the “e-arrowheaddown” and “e-arrowheadup” classes to header and selectedHeader properties.  “e-arrowheaddown” and “e-arrowheadup” are available in ej.widgets.core.min.css file.$("#accordion").ejAccordion({      customIcon: {/*  To set icon for the collapsed accordion headers  */                    <b>header: "e-arrowheaddown"</b>,                     /*  To set icon for the selected accordion headers  */                    <b>selectedHeader: "e-arrowheadup" </b>                }        }); </td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with corresponding data and set the “e-arrowheaddown” and “e-arrowheadup” classes to Header and SelectedHeader properties.  “E-arrowheaddown” and “e-arrowheadup” are available in ej.widgets.core.min.css file.**



&lt;div style="width: 400px; float:left;"&gt;

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

        }).**CustomIcon(icon =>icon.SelectedHeader("e-arrowheadup").Header("e-arrowheaddown"))**.Render();}

&lt;/div&gt;



**[ASPX]**

**// In Design page configure Accordion with corresponding AccordionItems. To customize the header icons, set the “e-arrowheaddown” and “e-arrowheadup” classes to Header and SelectedHeader properties.  “e-arrowheaddown” and “e-arrowheadup” are available in ej.widgets.core.min.css file.**



&lt;div style="width: 400px;"&gt;

    &lt;ej:Accordion ID="BasicAccordion" runat="server" EnableMultipleOpen="true"&gt;

**&lt;CustomIcon Header="e-arrowheaddown" SelectedHeader="e-arrowheadup" /&gt;**

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



* Output for **Accordion** widget with customized icons is as follows.



![](appearance-and-styling_images\appearance-and-styling_img3.png)

_Figure_ _27__17__: Accordion with customized icons_

**Animations**

**Set animation**

By default the **Animation** for expanding and collapsing is enabled. To remove the Animation you can set the **enableAnimation** property to **false**. This restricts customizing animations as well. By default **enableAnimation** is set to **true**.

Following code disables **Animation** for **Accordion**.


{% highlight js %}

**[JavaScript]**
$("#accordion").ejAccordion({
**enableAnimation: false**
       }); 


{% endhighlight %}

**Expand and collapse speed**

This feature allows you to set the speed for expanding and collapsing the **Accordion** panels. By default it is set to 300 in milliseconds. By configuring the animation speed you can optimize the delay in loading the panel content.

The following code sample sets value for **expandSpeed** and **collapseSpeed** properties,

{% highlight js %}

**[JavaScript]**
$("#accordion").ejAccordion({
                **expandSpeed:600,**
                **collapseSpeed:1000,**
                collapsible:true
            }); 


{% endhighlight %}



**[CSHTML]**

**// The following code example sets values for ExpandSpeed and CollapseSpeed properties.**



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

        }).**CollapseSpeed("1000").ExpandSpeed("600")**.Render();}

&lt;/div&gt;



**[ASPX]**

    &lt;div style="width: 400px;"&gt;

    &lt;ej:Accordion ID="BasicAccordion" runat="server" CollapseSpeed="1000" ExpandSpeed="600"&gt;

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





**Theme**

You can control the style and appearance of **Accordion** control based on **CSS** classes. In order to apply styles to the **Accordion** widget, you can refer two files, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Accordion** control namely

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

**CSS class**

**CSS** class can be used to customize the **Accordion** control appearance. Define a **CSS** class asyou’re your requirement and assign the class name to **cssClass** property.

**Configure AutoComplete textbox using CSS class**

The following steps allows you to configure **CSS** class for an **Accordion** widget.

* In the **HTML** page, define a **&lt;div&gt;** element that is a container for  **Accordion** widget and add the contents correspondingly



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 400px"&gt;     &lt;h3&gt;          <a href="#">Orubase</a>&lt;/h3&gt;      &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;          Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.    &lt;/div&gt;      &lt;h3&gt;           <a href="#">WinRTXAML</a>&lt;/h3&gt;       &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.           &lt;/div&gt;            &lt;h3&gt;             <a href="#">Metro Studio</a>&lt;/h3&gt;     &lt;div&gt;  &lt;!-- add accordion contents here to load contents under this header --&gt;           Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                          &lt;/div&gt;                         &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Set the <b>cssClass</b> property for <b>Accordion</b>         $("#accordion").ejAccordion({                <b>cssClass: "customCss"</b>            });</td></tr>
</table>


**[CSHTML]**

**// In the View page, configure Accordion with corresponding data and set the CssClass property with corresponding CSS class name.**



&lt;div style="width: 400px; float:left;"&gt;

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

        }).**CssClass("customCss")**.Render();}

&lt;/div&gt;



**[ASPX]**

**// In design page configure Accordion with corresponding AccordionItems and set the CssClass property with corresponding CSS class name**



&lt;div style="width: 400px;"&gt;

    &lt;ej:Accordion ID="BasicAccordion" runat="server" CssClass="customCss"&gt;

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





* Define **CSS** class for customizing the **Accordion.**



{% highlight css %}

**[Style]**
<style class="cssStyles">
         .customCss
         {
            font-style: italic;
            text-align:justify;
         }
         .customCss span.e-icon {
            display: none !important;
         }
         .customCss h3
         {
             text-decoration:underline;
             text-align:center;
         }
    </style>



{% endhighlight %}



* Define **Css** class for customizing the **Accordion.**

**[CSS]**

&lt;style type="text/css"&gt;

        .customCss

        {

            font-style: italic;

            text-align: justify;

        }

        /* Customize to hide icon */

        .customCss span.e-icon

        {

            display: none !important;

        }

        /* customize header text */

        .customCss h3

        {

            text-decoration: underline;

            text-align: center;

        }

    &lt;/style&gt;



* Output for **Accordion** with customized **CSS** property to hide the **Accordion** icon and format its content is as follows.

![](appearance-and-styling_images\appearance-and-styling_img4.png)

_Figure_ _28__18__: Accordion with Custom CSS property_

