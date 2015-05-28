---
layout: post
title: ajax-settings
description: ajax settings
platform: js
control: Accordion 
documentation: ug
---

# Ajax settings

**Accordion** widgets allow you to load content for the **Accordion****panel** using **Ajax**. This renders content from the specified **URL** location that is set to the anchor tag. You can set the destination file URL string by using **aAjaxUrl** property **Ajax** contents enables you to load the content of the **Accordion** panel when it is expanded. This enhances the **Accordion** control efficiency when a large content is to be loaded into the panel.

**Populate accordion with AJAX content**

* Create **HTML** files with required content to be loaded for **Accordion** panel and save it in your drive location.

* In the **HTML** page, define a **&lt;div&gt;** element that is a container for **Accordion** widget and add the contents **URL** location in the **&lt;a&gt;** tag accordingly.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="accordion" style="width: 650px"&gt;    &lt;h3&gt;        <a href="#">WCF</a>&lt;/h3&gt;    &lt;div&gt;        &lt;p&gt;            WCF is a tool often used to implement and deploy a service-oriented architecture (SOA).             It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers. Clients can consume multiple services; services can be consumed by multiple clients. Services are loosely coupled to each other. Services typically have a WSDL interface (Web Services Description Language) that any WCF client can use to consume the service, regardless of which platform the service is hosted on.             WCF implements many advanced Web services (WS) standards such as WS-Addressing, WS-ReliableMessaging and WS-Security. With the release of .NET Framework 4.0, WCF also provides RSS Syndication Services, WS-Discovery, routing and better support for REST services.        &lt;/p&gt;    &lt;/div&gt;    &lt;h3&gt;<b>        <a href="mvccontent.html">Model–view–controller (MVC)&lt;/a&gt;</b>&lt;/h3&gt;    &lt;div&gt;    &lt;/div&gt;    &lt;h3&gt;        <b><a href="wpfcontent.html">WPF</a></b>&lt;/h3&gt;    &lt;div&gt;    &lt;/div&gt;                      &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Configure the <b>Accordion</b> control          $("#accordion").ejAccordion();</td></tr>
</table>


**[CSHTML]**

**// In the View page, render Accordion with corresponding data and set AjaxUrl property for the corresponding headers.**







&lt;div style="width: 800px; float:left;"&gt;

@{Html.EJ().Accordion("accordion").Items(data =>

        {

            data.Add().Text("MVC").**AjaxUrl("../../Content/mvccontent.html");**

            data.Add().Text("WPF").**AjaxUrl("../../Content/wpfcontent.html");**

            data.Add().Text("WCF").ContentTemplate(@&lt;div&gt;

               WCF is a tool often used to implement and deploy a service-oriented architecture (SOA).It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers. Clients can consume multiple services; services can be consumed by multiple clients. Services are loosely coupled to each other. Services typically have a WSDL interface (Web Services Description Language) that any WCF client can use to consume the service, regardless of which platform the service is hosted on. WCF implements many advanced Web services (WS) standards such as WS-Addressing, WS-ReliableMessaging and WS-Security. With the release of .NET Framework 4.0, WCF also provides RSS Syndication Services, WS-Discovery, routing and better support for REST services.&lt;/div&gt;);

       }).Render();}

&lt;/div&gt;



**[ASPX]**

**// In Design page render Accordion with corresponding AccordionItems and set AjaxUrl property for the corresponding headers with the URLs.**



&lt;div style="width: 700px;"&gt;

    &lt;ej:Accordion ID="BasicAccordion" runat="server"&gt;

        &lt;Items&gt;

            &lt;ej:AccordionItem Text="MVC" AjaxUrl="mvccontent.html"&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="WPF" AjaxUrl="wpfcontent.html"&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="WCF"&gt;

                &lt;ContentSection&gt;

                        WCF is a tool often used to implement and deploy a service-oriented architecture (SOA).It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers. Clients can consume multiple services; services can be consumed by multiple clients. Services are loosely coupled to each other. Services typically have a WSDL interface (Web Services Description Language) that any WCF client can use to consume the service, regardless of which platform the service is hosted on. WCF implements many advanced Web services (WS) standards such as WS-Addressing, WS-ReliableMessaging and WS-Security. With the release of .NET Framework 4.0, WCF also provides RSS Syndication Services, WS-Discovery, routing and better support for REST services.

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



* Output for **Accordion** control with loaded **Ajax** content is as follows.



![C:\Users\ApoorvahR\Desktop\6.png](ajax-settings_images\ajax-settings_img1.png)

_Figure_ _20__10__: Accordion with loaded AJAX content_

