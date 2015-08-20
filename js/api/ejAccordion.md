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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
       $(function () {
           // Initialize Accordion control creation.
           $("#accordion").ejAccordion();
       });
   </script> {% endhighlight %}




Requires
{:.require}



* module:jQuery

* module:jquery.easing.1.3.min.js

* module:ej.core.js

* module:ej.accordion.js


## Members




### ajaxSettings<span class="type-signature type object">object</span>
{:#members:ajaxsettings}




Specifies the ajaxSettings option to load the content to the accordion control.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// Set the ajaxSettings options during initialization.                  
        $("#accordion").ejAccordion({  ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true } });
</script> 
{% endhighlight %}




### ajaxSettings.async<span class="type-signature type boolean">Boolean</span>
{:#members:ajaxsettings-async}




It specifies, whether to enable or disable asynchronous request.






### ajaxSettings.cache<span class="type-signature type boolean">Boolean</span>
{:#members:ajaxsettings-cache}




It specifies the page will be cached in the web browser.






### ajaxSettings.contentType<span class="type-signature type string">String</span>
{:#members:ajaxsettings-contenttype}




It specifies the type of data is send in the query string.






### ajaxSettings.data<span class="type-signature type object">Object</span>
{:#members:ajaxsettings-data}




It specifies the data as an object, will be passed in the query string.






### ajaxSettings.dataType<span class="type-signature type string">String</span>
{:#members:ajaxsettings-datatype}




It specifies the type of data that you're expecting back from the response.






### ajaxSettings.type<span class="type-signature type string">String</span>
{:#members:ajaxsettings-type}




It specifies the HTTP request type.






### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}




Accordion headers can be expanded and collapsed on keyboard action.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable allowKeyboardNavigation on initialization.
        $("#accordion").ejAccordion({ allowKeyboardNavigation: true});
</script>{% endhighlight %}




### collapseSpeed<span class="type-signature type integer/string">integer/string</span>
{:#members:collapsespeed}




To set the Accordion headers Collapse Speed.


Default Value:
{:.param}



* 300




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Set collapseSpeed on initialization.
        $("#accordion").ejAccordion({ collapseSpeed: 500});
</script>{% endhighlight %}




### collapsible<span class="type-signature type boolean">boolean</span>
{:#members:collapsible}




Specifies the collapsible state of accordion control.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="accordion">
<h3>
<a href="#">Orubase</a></h3>
<div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
</div>
 <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
// Allow to collapsible on initialization. 
        //To set collapsible API value 
         $("#accordion").ejAccordion({ collapsible: true});
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}




Sets the root class for the Accordion theme. This cssClass API enables the use of custom skinning options for the Accordion control. By defining the root class using this
API, we need to include this root class in the CSS.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
 //cssClass on initialization.
        $("#accordion").ejAccordion({cssClass: "gradient-lime" });
</script>{% endhighlight %}




### customIcon<span class="type-signature type jsonobject">JSONObject</span>
{:#members:customicon}




The header icon can be customized using this API. It has two properties: header as the collapsing header CSS class name, and selectedHeader as the active header CSS class
name. It accepts CSS class names with string as the type. * &bull;header: This class name set to collapsing header. This accepts the string type value. &bull;selectedHeader: This class name set to
expanded header. This accepts the string type value.


Default Value:
{:.param}



* "{ header: "e-acrdn-collapsicon", selectedHeader: "e-acrdn-expandicon" }"




Example
{:.example}


{% highlight html %}
        
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">           
//customIcon on initialization. 
  $("#accordion").ejAccordion({
                customIcon: {
                        header: "header-close",
                        selectedHeader: "header-expand"
                }
        });
</script>{% endhighlight %}




### disabledItems<span class="type-signature type integerarray">Integerarray</span>
{:#members:disableditems}




To deactivate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // disabledItems on initialization.
        $("#accordion").ejAccordion({ disabledItems: [0,1] });
</script>{% endhighlight %}




### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members:enableanimation}




Specifies the animation behavior in accordion.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// Set the enableAnimation value during initialization.                         
        $("#accordion").ejAccordion({  enableAnimation : false });
</script> 
{% endhighlight %}




### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}




With the Enabled property, you can enable or disable the Accordion.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable accordion on initialization.
        $("#accordion").ejAccordion({ enabled: true});
</script>{% endhighlight %}




### enabledItems<span class="type-signature type integerarray">Integerarray</span>
{:#members:enableditems}




To activate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // enabledItems on initialization.
        $("#accordion").ejAccordion({ enabledItems: [0,1] });
</script>{% endhighlight %}




### enableMultipleOpen<span class="type-signature type boolean">boolean</span>
{:#members:enablemultipleopen}




Multiple content panels to activate at a time.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enableMultipleOpen on initialization.
        $("#accordion").ejAccordion({ enableMultipleOpen: true});
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for maintaining states. When refreshing the accordion control page, the model value is applied from browser cookies or HTML 5
local storage.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enablePersistence on initialization.
        $("#accordion").ejAccordion({ enablePersistence: true});
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Display headers and panel text from right-to-left.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enableRTL on initialization.
        $("#accordion").ejAccordion({ enableRTL: true});
</script>{% endhighlight %}




### events<span class="type-signature type string">String</span>
{:#members:events}




The events API binds the action for activating the accordion header. Users can activate the header by using mouse actions such as mouse-over, mouse-up, mouse-down, and so
on.


Default Value:
{:.param}



* "click"




Example
{:.example}


{% highlight html %}
                       
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
// Bind events API on initialization. 
$("#accordion").ejAccordion({ events: "mouseover" });
</script>{% endhighlight %}




### expandSpeed<span class="type-signature type integer/string">integer/string</span>
{:#members:expandspeed}




To set the Accordion headers Expand Speed.


Default Value:
{:.param}



* 300




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Set expandSpeed on initialization.
        $("#accordion").ejAccordion({ expandSpeed: 500});
</script>{% endhighlight %}




### header<span class="type-signature type string">String</span>
{:#members:header}




Set class name to collapsing header.



Example
{:.example}


{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">           
//header on initialization. 
  $("#accordion").ejAccordion({
                        header: "collapsicon"
        });
</script>{% endhighlight %}




### heightAdjustMode<span class="type-signature type enum/string">Enum/String</span>
{:#members:heightadjustmode}




Adjusts the content panel height based on the given option (content, auto, or fill). By default, the panel heights are adjusted based on the content. See <a href=
"global.html#HeightAdjustMode">HeightAdjustMode</a>


Default Value:
{:.param}



* "content"




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//heightAdjustMode  for content div on initialization. 
$("#accordion").ejAccordion({ heightAdjustMode : ej.Accordion.HeightAdjustMode.Auto }); //enum 
</script>{% endhighlight %}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//Pass value on string type. 
$("#accordion").ejAccordion({ heightAdjustMode : "auto" }); 
</script>{% endhighlight %}




### selectedHeader<span class="type-signature type string">String</span>
{:#members:selectedheader}




Set class name to expanded header.



Example
{:.example}


{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">           
//Selected header on initialization. 
  $("#accordion").ejAccordion({
                
                        selectedHeader: "activeicon"
                
        });
</script>{% endhighlight %}




### selectedItemIndex<span class="type-signature type integer">Integer</span>
{:#members:selecteditemindex}




The given index header will activate (open). If collapsible is set to true, and a negative value is given, then all headers are collapsed. Otherwise, the first panel is
activated.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
 //Activate given header on initialization.
        $("#accordion").ejAccordion({ selectedItemIndex : 1 });
</script>{% endhighlight %}




### selectedItems<span class="type-signature type integerarray">Integerarray</span>
{:#members:selecteditems}




To activate multiple headers for the accordion, give the index value for array type for this API. The enableMultipleOpen property should be set as true.


Default Value:
{:.param}



* [0]




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // selectedItems on initialization.
        $("#accordion").ejAccordion({ selectedItems: [0,1] });
</script>{% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Displays rounded corner borders on the Accordion control's panels and headers.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
  // Enable showRoundedCorner on initialization.
        $("#accordion").ejAccordion({ showRoundedCorner: true});
</script>{% endhighlight %}



## Methods




### collapseAll<span class="signature">()</span>
{:#methods:collapseall}




collapseAll the accordion widget collapse All the header and content panel Before we call this method, we must set "collapsible" is true. Then only collapseAll method will
working.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// Call collapseAll method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("collapseAll");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// collapse All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.collapseAll(); //Calls the collapseAll method of Accordion.      
</script>{% endhighlight %}




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the Accordion widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.destroy(); //Calls the destroy method of Accordion.
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// destroy the Accordion
$("#Accordion").ejAccordion("destroy"); 
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




disables the accordion widget disables All the header and content panel.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// Call disable method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("disable");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// disable the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disable(); //Calls the disable method of Accordion.      
</script>{% endhighlight %}




### disableItems<span class="signature">()</span>
{:#methods:disableitems}




enable the accordion widget Enables given index header and content panel.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call disableItems method.
$("#accordion").ejAccordion("disableItems", 1);
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// disableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems(1); //Calls the disableItems method of Accordion.   
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




enable the accordion widget Enables all the headers and content panels.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call enable method.
$("#accordion").ejAccordion("enable");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// destroy the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.enable(); //Calls the enable method of Accordion.        
</script>{% endhighlight %}




### enableItems<span class="signature">()</span>
{:#methods:enableitems}




enable the accordion widget Enables given index header and content panel.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call enableItems method.
$("#accordion").ejAccordion("disableItems", 0); 
$("#accordion").ejAccordion("disableItems", 1); 
$("#accordion").ejAccordion("enableItems", 1);
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// enableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems(0);
accObj.disableItems(1);
accObj.enableItems(1); //Calls the enable method of Accordion.  
</script>{% endhighlight %}




### expandAll<span class="signature">()</span>
{:#methods:expandall}




expand All the accordion widget expand All the header and content panel Before we call this method, we must set "enableMultipleOpen" is true. Then only expandAll method will
working.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// Call expandAll method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("expandAll");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// expand All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.expandAll(); //Calls the expandAll method of Accordion.  
</script>{% endhighlight %}




### getItemsCount<span class="signature">()</span>
{:#methods:getitemscount}




Returns the total number of panels in the control.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call getItemsCount method.
$("#accordion").ejAccordion("getItemsCount");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// getItemsCount the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.getItemsCount(); //Calls the getItemsCount method of Accordion.  
</script>{% endhighlight %}




### hide<span class="signature">()</span>
{:#methods:hide}




Hides the visible Accordion control.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call hide method.
$("#accordion").ejAccordion("hide");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// hide the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.hide(); //Calls the hide method of Accordion.    
</script>{% endhighlight %}




### show<span class="signature">()</span>
{:#methods:show}




Shows the hidden Accordion control.



Example
{:.example}


{% highlight html %}
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call show method.
$("#accordion").ejAccordion("show");
</script>{% endhighlight %}


{% highlight html %}
 
   <div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
<script>
// show the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.show(); //Calls the show method of Accordion.    
</script>{% endhighlight %}



## Events




### activate
{:#events:activate}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active header</td>
</tr>
<tr>
<td class="name">{% highlight html %}
inActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
inActiveHeader{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ activate: function (args) {}
});
</script>{% endhighlight %}




### ajaxBeforeLoad
{:#events:ajaxbeforeload}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxBeforeLoad event
        $("#accordion").ejAccordion({ ajaxBeforeLoad: function (args) {}
});
</script>{% endhighlight %}




### ajaxError
{:#events:ajaxerror}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns current ajax content location</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxError event
        $("#accordion").ejAccordion({ ajaxError: function (args) {}
});
</script>{% endhighlight %}




### ajaxLoad
{:#events:ajaxload}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxLoad event
        $("#accordion").ejAccordion({ ajaxLoad: function (args) {}
});
</script>{% endhighlight %}




### ajaxSuccess
{:#events:ajaxsuccess}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns current ajax content location</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the succesfull data sent.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
content{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxSuccess event
        $("#accordion").ejAccordion({ ajaxSuccess: function (args) {}
});
</script>{% endhighlight %}




### beforeActivate
{:#events:beforeactivate}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial beforeActivate event
        $("#accordion").ejAccordion({ beforeActivate: function (args) {}
});
</script>{% endhighlight %}




### beforeInactivate
{:#events:beforeinactivate}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
inActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns active index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
inActiveHeader{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ beforeInactivate: function (args) {}
});
</script>{% endhighlight %}




### create
{:#events:create}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial create event
        $("#accordion").ejAccordion({ create: function (args) {}
});
</script>{% endhighlight %}




### destroy
{:#events:destroy}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial destroy event
        $("#accordion").ejAccordion({ destroy: function (args) {}
});
</script>{% endhighlight %}




### inActivate
{:#events:inactivate}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the accordion model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
inActiveIndex{% endhighlight %}</td>
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


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">Orubase</a></h3>
       <div>
Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
       </div>
       <h3>
           <a href="#">WinRT XAML</a></h3>
       <div>
Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, PDF viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
       </div>
       <h3>
           <a href="#">Metro Studio</a></h3>
       <div>
Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ inActivate: function (args) {}
});
</script>{% endhighlight %}



