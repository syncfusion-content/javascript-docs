---
layout: post
title: ejAccordion
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Accordion control.





$(element).ejAccordion<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
       $(function () {
           // Initialize Accordion control creation.
           $("#accordion").ejAccordion();
       });
   &lt;/script&gt; </code>
</pre>



Requires
{:.require}



* module:jQuery

* module:jquery.easing.1.3.min.js

* module:ej.core.js

* module:ej.accordion.js


## Members




### ajaxSettings<span class="type-signature type object">object</span>
{:#ajaxsettings}
{:#ajaxSettings}




Specifies the ajaxSettings option to load the content to the accordion control.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// Set the ajaxSettings options during initialization.                  
        $("#accordion").ejAccordion({  ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true } });
&lt;/script&gt; 
</code>
</pre>



### ajaxSettings.async<span class="type-signature type boolean">Boolean</span>
{:#ajaxsettings-async}
{:#ajaxSettings-async}




It specifies, whether to enable or disable asynchronous request.






### ajaxSettings.cache<span class="type-signature type boolean">Boolean</span>
{:#ajaxsettings-cache}
{:#ajaxSettings-cache}




It specifies the page will be cached in the web browser.






### ajaxSettings.contentType<span class="type-signature type string">String</span>
{:#ajaxsettings-contenttype}
{:#ajaxSettings-contentType}




It specifies the type of data is send in the query string.






### ajaxSettings.data<span class="type-signature type object">Object</span>
{:#ajaxsettings-data}
{:#ajaxSettings-data}




It specifies the data as an object, will be passed in the query string.






### ajaxSettings.dataType<span class="type-signature type string">String</span>
{:#ajaxsettings-datatype}
{:#ajaxSettings-dataType}




It specifies the type of data that you're expecting back from the response.






### ajaxSettings.type<span class="type-signature type string">String</span>
{:#ajaxsettings-type}
{:#ajaxSettings-type}




It specifies the HTTP request type.






### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#allowkeyboardnavigation}
{:#allowKeyboardNavigation}




Accordion headers can be expanded and collapsed on keyboard action.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable allowKeyboardNavigation on initialization.
        $("#accordion").ejAccordion({ allowKeyboardNavigation: true});
&lt;/script&gt;</code>
</pre>



### collapseSpeed<span class="type-signature type integer/string">integer/string</span>
{:#collapsespeed}
{:#collapseSpeed}




To set the Accordion headers Collapse Speed.


Default Value:
{:.param}



* 300




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Set collapseSpeed on initialization.
        $("#accordion").ejAccordion({ collapseSpeed: 500});
&lt;/script&gt;</code>
</pre>



### collapsible<span class="type-signature type boolean">boolean</span>
{:#collapsible}
{:#collapsible}




Specifies the collapsible state of accordion control.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
&lt;h3&gt;
&lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
&lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
&lt;/div&gt;
 &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
// Allow to collapsible on initialization. 
        //To set collapsible API value 
         $("#accordion").ejAccordion({ collapsible: true});
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">String</span>
{:#cssclass}
{:#cssClass}




Sets the root class for the Accordion theme. This cssClass API enables the use of custom skinning options for the Accordion control. By defining the root class using this
API, we need to include this root class in the CSS.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
 //cssClass on initialization.
        $("#accordion").ejAccordion({cssClass: "gradient-lime" });
&lt;/script&gt;</code>
</pre>



### customIcon<span class="type-signature type jsonobject">JSONObject</span>
{:#customicon}
{:#customIcon}




The header icon can be customized using this API. It has two properties: header as the collapsing header CSS class name, and selectedHeader as the active header CSS class
name. It accepts CSS class names with string as the type. * &bull;header: This class name set to collapsing header. This accepts the string type value. &bull;selectedHeader: This class name set to
expanded header. This accepts the string type value.


Default Value:
{:.param}



* "{ header: "e-acrdn-collapsicon", selectedHeader: "e-acrdn-expandicon" }"




Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;           
//customIcon on initialization. 
  $("#accordion").ejAccordion({
                customIcon: {
                        header: "header-close",
                        selectedHeader: "header-expand"
                }
        });
&lt;/script&gt;</code>
</pre>



### disabledItems<span class="type-signature type integerarray">Integerarray</span>
{:#disableditems}
{:#disabledItems}




To deactivate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* []




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // disabledItems on initialization.
        $("#accordion").ejAccordion({ disabledItems: [0,1] });
&lt;/script&gt;</code>
</pre>



### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#enableanimation}
{:#enableAnimation}




Specifies the animation behavior in accordion.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// Set the enableAnimation value during initialization.                         
        $("#accordion").ejAccordion({  enableAnimation : false });
&lt;/script&gt; 
</code>
</pre>



### enabled<span class="type-signature type boolean">Boolean</span>
{:#enabled}
{:#enabled}




With the Enabled property, you can enable or disable the Accordion.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable accordion on initialization.
        $("#accordion").ejAccordion({ enabled: true});
&lt;/script&gt;</code>
</pre>



### enabledItems<span class="type-signature type integerarray">Integerarray</span>
{:#enableditems}
{:#enabledItems}




To activate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* []




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // enabledItems on initialization.
        $("#accordion").ejAccordion({ enabledItems: [0,1] });
&lt;/script&gt;</code>
</pre>



### enableMultipleOpen<span class="type-signature type boolean">boolean</span>
{:#enablemultipleopen}
{:#enableMultipleOpen}




Multiple content panels to activate at a time.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable enableMultipleOpen on initialization.
        $("#accordion").ejAccordion({ enableMultipleOpen: true});
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#enablepersistence}
{:#enablePersistence}




Save current model value to browser cookies for maintaining states. When refreshing the accordion control page, the model value is applied from browser cookies or HTML 5
local storage.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable enablePersistence on initialization.
        $("#accordion").ejAccordion({ enablePersistence: true});
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#enablertl}
{:#enableRTL}




Display headers and panel text from right-to-left.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable enableRTL on initialization.
        $("#accordion").ejAccordion({ enableRTL: true});
&lt;/script&gt;</code>
</pre>



### events<span class="type-signature type string">String</span>
{:#events}
{:#events}




The events API binds the action for activating the accordion header. Users can activate the header by using mouse actions such as mouse-over, mouse-up, mouse-down, and so
on.


Default Value:
{:.param}



* "click"




Example
{:.example}

<pre class="prettyprint">
<code>                       
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
// Bind events API on initialization. 
$("#accordion").ejAccordion({ events: "mouseover" });
&lt;/script&gt;</code>
</pre>



### expandSpeed<span class="type-signature type integer/string">integer/string</span>
{:#expandspeed}
{:#expandSpeed}




To set the Accordion headers Expand Speed.


Default Value:
{:.param}



* 300




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Set expandSpeed on initialization.
        $("#accordion").ejAccordion({ expandSpeed: 500});
&lt;/script&gt;</code>
</pre>



### header<span class="type-signature type string">String</span>
{:#header}
{:#header}




Set class name to collapsing header.



Example
{:.example}

<pre class="prettyprint">
<code>      
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;           
//header on initialization. 
  $("#accordion").ejAccordion({
                        header: "collapsicon"
        });
&lt;/script&gt;</code>
</pre>



### heightAdjustMode<span class="type-signature type enum/string">Enum/String</span>
{:#heightadjustmode}
{:#heightAdjustMode}




Adjusts the content panel height based on the given option (content, auto, or fill). By default, the panel heights are adjusted based on the content. See <a href=
"global.html#HeightAdjustMode">HeightAdjustMode</a>


Default Value:
{:.param}



* "content"




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//heightAdjustMode  for content div on initialization. 
$("#accordion").ejAccordion({ heightAdjustMode : ej.Accordion.HeightAdjustMode.Auto }); //enum 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//Pass value on string type. 
$("#accordion").ejAccordion({ heightAdjustMode : "auto" }); 
&lt;/script&gt;</code>
</pre>



### selectedHeader<span class="type-signature type string">String</span>
{:#selectedheader}
{:#selectedHeader}




Set class name to expanded header.



Example
{:.example}

<pre class="prettyprint">
<code>      
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;           
//Selected header on initialization. 
  $("#accordion").ejAccordion({
                
                        selectedHeader: "activeicon"
                
        });
&lt;/script&gt;</code>
</pre>



### selectedItemIndex<span class="type-signature type integer">Integer</span>
{:#selecteditemindex}
{:#selectedItemIndex}




The given index header will activate (open). If collapsible is set to true, and a negative value is given, then all headers are collapsed. Otherwise, the first panel is
activated.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
 //Activate given header on initialization.
        $("#accordion").ejAccordion({ selectedItemIndex : 1 });
&lt;/script&gt;</code>
</pre>



### selectedItems<span class="type-signature type integerarray">Integerarray</span>
{:#selecteditems}
{:#selectedItems}




To activate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* [0]




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // selectedItems on initialization.
        $("#accordion").ejAccordion({ selectedItems: [0,1] });
&lt;/script&gt;</code>
</pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#showroundedcorner}
{:#showRoundedCorner}




Displays rounded corner borders on the Accordion control's panels and headers.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
  // Enable showRoundedCorner on initialization.
        $("#accordion").ejAccordion({ showRoundedCorner: true});
&lt;/script&gt;</code>
</pre>


## Methods




### collapseAll<span class="signature">()</span>
{:#collapseall}
{:#collapseAll}




collapseAll the accordion widget collapse All the header and content panel Before we call this method, we must set "collapsible" is true. Then only collapseAll method will
working.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// Call collapseAll method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("collapseAll");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// collapse All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.collapseAll(); //Calls the collapseAll method of Accordion.      
&lt;/script&gt;</code>
</pre>



### destroy<span class="signature">()</span>
{:#destroy}
{:#destroy}




destroy the Accordion widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.destroy(); //Calls the destroy method of Accordion.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// destroy the Accordion
$("#Accordion").ejAccordion("destroy"); 
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#disable}
{:#disable}




disables the accordion widget disables All the header and content panel.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// Call disable method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("disable");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// disable the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disable(); //Calls the disable method of Accordion.      
&lt;/script&gt;</code>
</pre>



### disableItems<span class="signature">()</span>
{:#disableitems}
{:#disableItems}




enable the accordion widget Enables given index header and content panel.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call disableItems method.
$("#accordion").ejAccordion("disableItems", 1);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// disableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems(1); //Calls the disableItems method of Accordion.   
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#enable}
{:#enable}




enable the accordion widget Enables all the headers and content panels.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call enable method.
$("#accordion").ejAccordion("enable");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// destroy the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.enable(); //Calls the enable method of Accordion.        
&lt;/script&gt;</code>
</pre>



### enableItems<span class="signature">()</span>
{:#enableitems}
{:#enableItems}




enable the accordion widget Enables given index header and content panel.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call enableItems method.
$("#accordion").ejAccordion("disableItems", 0); 
$("#accordion").ejAccordion("disableItems", 1); 
$("#accordion").ejAccordion("enableItems", 1);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// enableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems(0);
accObj.disableItems(1);
accObj.enableItems(1); //Calls the enable method of Accordion.  
&lt;/script&gt;</code>
</pre>



### expandAll<span class="signature">()</span>
{:#expandall}
{:#expandAll}




expand All the accordion widget expand All the header and content panel Before we call this method, we must set "enableMultipleOpen" is true. Then only expandAll method will
working.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// Call expandAll method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("expandAll");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// expand All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.expandAll(); //Calls the expandAll method of Accordion.  
&lt;/script&gt;</code>
</pre>



### getItemsCount<span class="signature">()</span>
{:#getitemscount}
{:#getItemsCount}




Returns the total number of panels in the control.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call getItemsCount method.
$("#accordion").ejAccordion("getItemsCount");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// getItemsCount the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.getItemsCount(); //Calls the getItemsCount method of Accordion.  
&lt;/script&gt;</code>
</pre>



### hide<span class="signature">()</span>
{:#hide}
{:#hide}




Hides the visible Accordion control.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call hide method.
$("#accordion").ejAccordion("hide");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// hide the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.hide(); //Calls the hide method of Accordion.    
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#show}
{:#show}




Shows the hidden Accordion control.



Example
{:.example}

<pre class="prettyprint">
<code>   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
           $("#accordion").ejAccordion();
// Call show method.
$("#accordion").ejAccordion("show");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
&lt;script&gt;
// show the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.show(); //Calls the show method of Accordion.    
&lt;/script&gt;</code>
</pre>


## Events




### activate
{:#activate}
{:#activate}




Triggered after a Accordion item is active or inactive. Argument values are activeindex, activeHeader, inActiveHeader, inActiveIndex and current model value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>activeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name"><code>activeHeader</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active header</td>
</tr>
<tr>
<td class="name"><code>inActiveIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name"><code>inActiveHeader</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active header</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial activate event
        $("#accordion").ejAccordion({ activate: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### ajaxBeforeLoad
{:#ajaxbeforeload}
{:#ajaxBeforeLoad}




Triggered before the AJAX content is loaded in a content panel. Arguments have location of the content (URL) and current model value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns current ajax content location</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial ajaxBeforeLoad event
        $("#accordion").ejAccordion({ ajaxBeforeLoad: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### ajaxError
{:#ajaxerror}
{:#ajaxError}




Triggered after AJAX load failed action. Arguments have URL, error message, and current model value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns current ajax content location</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the failed data sent.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial ajaxError event
        $("#accordion").ejAccordion({ ajaxError: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### ajaxLoad
{:#ajaxload}
{:#ajaxLoad}




Triggered after the AJAX content loads. Arguments have current model values.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the url</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial ajaxLoad event
        $("#accordion").ejAccordion({ ajaxLoad: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### ajaxSuccess
{:#ajaxsuccess}
{:#ajaxSuccess}




Triggered after AJAX success action. Arguments have URL, content, and current model values.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns current ajax content location</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the succesfull data sent.</td>
</tr>
<tr>
<td class="name"><code>content</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ajax content.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial ajaxSuccess event
        $("#accordion").ejAccordion({ ajaxSuccess: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### beforeActivate
{:#beforeactivate}
{:#beforeActivate}




Triggered before a tab item is active. Arguments have active index and model values.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>activeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial beforeActivate event
        $("#accordion").ejAccordion({ beforeActivate: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### beforeInactivate
{:#beforeinactivate}
{:#beforeInactivate}




Triggered after a Accordion item is active or inactive. Argument values are activeindex, activeHeader, inActiveHeader, inActiveIndex and current model value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>inActiveIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name"><code>inActiveHeader</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active header</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial activate event
        $("#accordion").ejAccordion({ beforeInactivate: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### create
{:#create}
{:#create}




Triggered after Accordion control creation.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial create event
        $("#accordion").ejAccordion({ create: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### destroy
{:#destroy}
{:#destroy}




Triggered after Accordion control destroy.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial destroy event
        $("#accordion").ejAccordion({ destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### inActivate
{:#inactivate}
{:#inActivate}




Triggered after a Accordion item is active or inactive. Argument values are activeindex, activeHeader, inActiveHeader, inActiveIndex and current model value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from accordion
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>inActiveIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="accordion"&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Orubase&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;WinRT XAML&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       &lt;/div&gt;
       &lt;h3&gt;
           &lt;a href="#"&gt;Metro Studio&lt;/a&gt;&lt;/h3&gt;
       &lt;div&gt;
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       &lt;/div&gt;
   &lt;/div&gt;
 &lt;script type="text/javascript"&gt;
//initial activate event
        $("#accordion").ejAccordion({ inActivate: function (args) {}
});
&lt;/script&gt;</code>
</pre>


