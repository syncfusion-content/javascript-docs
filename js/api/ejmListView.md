---
layout: post
title: ejmListView
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html ListView control.










$(element).ejmListView<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
//Set listbox in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set listbox in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt; 
// Create ListView
$("#lb").ejmListView(); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.mobile.application


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core


* module:ej.data


* module:ej.touch


* module:ej.mobile.checkbox


* module:ej.mobile.button


* module:ej.mobile.header


* module:ej.mobile.scrollbar


* module:ej.mobile.scrollpanel


* module:ej.mobile.textbox


* module:ej.listviewbase




## Members








### adjustFixedPosition<span class="type-signature type boolean">boolean</span>








Specifies whether need to adjust the scrolling content height for fixed position elements with the height of the control, when scrolling is allowed.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the adjustFixedPosition property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-adjustFixedPosition="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the adjustFixedPosition property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;            
// Set adjustFixedPosition on initialization. 
//To set adjustFixedPosition API value 
&lt;script&gt;
$("#lb").ejmListView ({ adjustFixedPosition: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set adjustFixedPosition, after initialization:
// Get the adjustFixedPosition API value.               
 $("#lb").ejmListView ("option", "adjustFixedPosition");                        
// Set the adjustFixedPosition API
$("#lb").ejmListView ("option", "adjustFixedPosition", true);     
&lt;/script&gt;       </code>
</pre>






### ajaxSettings<span class="type-signature type jsonobject">JSONObject</span>








Specifies the settings option for ajax request.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Set ajaxSettings in unobtrusive way
&lt;div id="lb" data-role="ejmlistview" data-ej-ajaxsettings-type="GET" data-ej-ajaxsettings-cache=false data-ej-ajaxsettings-async=true
data-ej-ajaxsettings-datatype="html" data-ej-ajaxsettings-contenttype="html" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;          </code>
</pre>
<pre class="prettyprint">
<code> 
//Set ajaxSettings in obtrusive way
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
// Set Tab ajaxSettings on initialization. 
//To set ajaxSettings API value 
&lt;script&gt;
$("#lb").ejmListView({ ajaxSettings: { type: 'GET',
  cache: false,
  async: true,
  dataType: "html",
  contentType: "html"
  } });         
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView ajaxSettings, after initialization:
// Get the ajaxSettings API value.
$("#lb").ejmListView ("option", "ajaxSettings");                        
// Set the ajaxSettings API
$("#lb").ejmListView ("option", "ajaxSettings", { type: 'GET',cache: false,async: true,dataType: "html",contentType: "html",url: "",data: {}});        
&lt;/script&gt;    </code>
</pre>






### allowScrolling<span class="type-signature type boolean">boolean</span>








Specifies whether to allow scrolling behavior for the contents.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the allowScrolling property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-allowScrolling="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;            </code>
</pre>
<pre class="prettyprint">
<code> 
//Set the allowScrolling property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;            
// Set allowScrolling on initialization. 
//To set allowScrolling API value 
&lt;script&gt;
$("#lb").ejmListView ({ allowScrolling: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  allowScrolling, after initialization:
// Get the allowScrolling API value.            
$("#lb").ejmListView ("option", "allowScrolling");                      
// Set the allowScrolling API
$("#lb").ejmListView ("option", "allowScrolling", true);  
&lt;/script&gt;          </code>
</pre>






### autoAdjustHeight<span class="type-signature type boolean">boolean</span>








Specifies whether to set the height of the content automatically.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the autoAdjustScrollHeight property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-autoAdjustHeight="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the autoAdjustHeight property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set autoAdjustHeight on initialization. 
//To set autoAdjustHeight API value 
$("#lb").ejmListView ({ autoAdjustHeight: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  autoAdjustHeight, after initialization:
// Get the autoAdjustHeight API value.          
 $("#lb").ejmListView ("option", "autoAdjustHeight");                   
// Set the autoAdjustHeight API
$("#lb").ejmListView ("option", "autoAdjustHeight", true);
&lt;/script&gt;</code>
</pre>






### autoAdjustScrollHeight<span class="type-signature type boolean">boolean</span>








Specifies whether to set the height as scroll height of the content automatically.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the autoAdjustScrollHeight property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-autoAdjustScrollHeight="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the autoAdjustScrollHeight property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set autoAdjustScrollHeight on initialization. 
//To set autoAdjustScrollHeight API value 
$("#lb").ejmListView ({ autoAdjustScrollHeight: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  autoAdjustScrollHeight, after initialization:
// Get the autoAdjustScrollHeight API value.            
 $("#lb").ejmListView ("option", "autoAdjustScrollHeight");                     
// Set the autoAdjustScrollHeight API
$("#lb").ejmListView ("option", "autoAdjustScrollHeight", true);
&lt;/script&gt;</code>
</pre>






### checkDOMChanges<span class="type-signature type boolean">boolean</span>








Specifies whether need to refresh scrollpanel rendered in the control when elements are added dynamically.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the checkDOMChanges property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-checkdomchanges=true&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the checkDOMChanges property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//Set the checkDOMChanges property on initialization. 
//To set checkDOMChanges API value
$("#lb").ejmListView ({ checkDOMChanges: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  checkDOMChanges, after initialization:
// Get the checkDOMChanges API value.           
$("#lb").ejmListView ("option", "checkDOMChanges");                     
// Set the checkDOMChanges API
$("#lb").ejmListView ("option", "checkDOMChanges", true);
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>








Sets the root class for ListView theme. This cssClass API helps to use custom skinning option for ListView control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the cssClass property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-cssclass="customclass"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the cssClass property in obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set cssClass on initialization. 
//To set cssClass API value 
$("#lb").ejmListView ({ cssClass: "customclass" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  cssClass, after initialization:
// Get the cssClass API value.          
 $("#lb").ejmListView ("option", "cssClass");                   
// Set the cssClass API
$("#lb").ejmListView ("option", "cssClass", "customclass");
&lt;/script&gt;</code>
</pre>






### dataSource<span class="type-signature type jsonarray">JSONArray</span>








Specifies the datasource is enabled.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the dataSource property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-datasource="window.dbitem"&gt;
&lt;/div&gt;           
&lt;script&gt;
window.dbitem =
[   { "text": "Hot Singles"},
    { "text": "Rising Artists"},
    { "text": "Live Music" },
    { "text": "Best of 2013 So Far"},
    { "text": "100 Albums - $5 Each"},
    { "text": "Hip-Hop and R&amp;B Sale"},
    { "text": "CD Deals"}];
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code> 
//Set the dataSource property in obtrusive way.
&lt;div id="lb" &gt;
&lt;/div&gt;           
&lt;script&gt;
$(function(){
$("#lb").ejmListView({dataSource:window.dbitem});
});
window.dbitem =
[   { "text": "Hot Singles"},
    { "text": "Rising Artists"},
    { "text": "Live Music" },
    { "text": "Best of 2013 So Far"},
    { "text": "100 Albums - $5 Each"},
    { "text": "Hip-Hop and R&amp;B Sale"},
    { "text": "CD Deals"}];
&lt;/script&gt;  </code>
</pre>
<pre class="prettyprint">
<code>       
&lt;script&gt;
//Get or set  dataSource, after initialization:
// Get the dataSource API value.                
$("#lb").ejmListView ("option", "dataSource");                  
// Set the dataSource API
$("#lb").ejmListView ("option", "dataSource", true);   
&lt;/script&gt;                     </code>
</pre>






### enableAjax<span class="type-signature type boolean">boolean</span>








Specifies whether to load ajax content while selecting item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableAjax property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code>  
//Set the enableAjax property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableAjax on initialization. 
//To set enableAjax API value
$("#lb").ejmListView ({ enableAjax: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableAjax, after initialization:
// Get the enableAjax API value.                
$("#lb").ejmListView ("option", "enableAjax");                  
// Set the enableAjax API
$("#lb").ejmListView ("option", "enableAjax", true);
&lt;/script&gt;</code>
</pre>






### enableCache<span class="type-signature type boolean">boolean</span>








Specifies whether to enable caching the content.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableCache property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enableCache="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true" data-ej-enableCache="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true" data-ej-enableCache="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true" data-ej-enableCache="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableCache property in obtrusive way.
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableCache on initialization. 
//To set enableCache API value 
$("#lb").ejmListView ({ enableCache: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableCache, after initialization:
// Get the enableCache API value.               
$("#lb").ejmListView ("option", "enableCache");                 
// Set the enableCache API
$("#lb").ejmListView ("option", "enableCache", true);
&lt;/script&gt;</code>
</pre>






### enableCheckMark<span class="type-signature type boolean">boolean</span>








Specifies whether to enable check mark for the item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableCheckMark property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableCheckMark property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableCheckMark on initialization. 
//To set enableCheckMark API value 
$("#lb").ejmListView ({ enableCheckMark: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView enableCheckMark, after initialization:
// Get the enableCheckMark API value.           
$("#lb").ejmListView ("option", "enableCheckMark");                     
// Set the enableCheckMark API
$("#lb").ejmListView ("option", "enableCheckMark", true);    
&lt;/script&gt;        </code>
</pre>






### enableFiltering<span class="type-signature type boolean">boolean</span>








Specifies whether to enable the filtering feature to filter the item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableFiltering property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enableFiltering="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableFiltering property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableFiltering on initialization. 
//To set enableFiltering API value 
$("#lb").ejmListView ({ enableFiltering: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView enableFiltering, after initialization:
// Get the enableFiltering API value.           
$("#lb").ejmListView ("option", "enableFiltering");                     
// Set the enableFiltering API
$("#lb").ejmListView ("option", "enableFiltering", true);    
&lt;/script&gt;        </code>
</pre>






### enableGroupList<span class="type-signature type boolean">boolean</span>








Specifies whether to group the list item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableGroupList property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enableGroupList="true"&gt;
        &lt;ul data-ej-grouplisttitle="Network"&gt;
                &lt;li data-ej-text="Airplane Mode"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wi-Fi"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Notifications"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Location Services"&gt;&lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul data-ej-grouplisttitle="Apps"&gt;
                &lt;li data-ej-text="Sound"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Brightness"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wallpaper"&gt;&lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul data-ej-grouplisttitle="Settings"&gt;
                &lt;li data-ej-text="General"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Brightness"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wallpaper"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableGroupList property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul data-ej-grouplisttitle="Network"&gt;
                &lt;li data-ej-text="Airplane Mode"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wi-Fi"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Notifications"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Location Services"&gt;&lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul data-ej-grouplisttitle="Apps"&gt;
                &lt;li data-ej-text="Sound"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Brightness"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wallpaper"&gt;&lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul data-ej-grouplisttitle="Settings"&gt;
                &lt;li data-ej-text="General"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Brightness"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Wallpaper"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableGroupList on initialization. 
//To set enableGroupList API value 
$("#lb").ejmListView ({ enableGroupList: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableGroupList, after initialization:
// Get the enableGroupList API value.           
 $("#lb").ejmListView ("option", "enableGroupList");                    
// Set the enableGroupList API
$("#lb").ejmListView ("option", "enableGroupList", true);
&lt;/script&gt;</code>
</pre>






### enableNativeScrolling<span class="type-signature type boolean">boolean</span>








Specifies whether to enable device's native scroll behavior when scrolling is allowed.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableNativeScrolling property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enableNativeScrolling="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableNativeScrolling property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableNativeScrolling on initialization. 
//To set enableNativeScrolling API value 
$("#lb").ejmListView ({ enableNativeScrolling: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableNativeScrolling, after initialization:
// Get the enableNativeScrolling API value.             
 $("#lb").ejmListView ("option", "enableNativeScrolling");                      
// Set the enableNativeScrolling API
$("#lb").ejmListView ("option", "enableNativeScrolling", true); 
&lt;/script&gt;           </code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-enablepersistence=true &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enablePersistence property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enablePersistence on initialization. 
//To set enablePersistence API value 
$("#lb").ejmListView ({ enablePersistence: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#lb").ejmListView ("option", "enablePersistence");                  
// Set the enablePersistence API
$("#lb").ejmListView ("option", "enablePersistence", true);
&lt;/script&gt;</code>
</pre>






### fieldSettings<span class="type-signature type jsonarray">JSONArray</span>








Specifies the field settings to map the datasource.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the fieldSettings property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-fieldSettings="window.musicFields" data-ej-datasource="window.dbitem" &gt;
&lt;/div&gt;           
&lt;script&gt;
window.dbitem =
[{ "Texts": "Discover Music", "PrimaryKeys": "1" },
    { "Texts": "Hot Singles", "ParentPrimaryKeyss": "1" },
    { "Texts": "Rising Artists", "PrimaryKeyss": null, "ParentPrimaryKeyss": "1" },
    { "Texts": "Live Music", "ParentPrimaryKeyss": "1" },
    { "Texts": "Best of 2013 So Far", "ParentPrimaryKeyss": "1" },
{ "Texts": "Sales and Events", "PrimaryKeys": "2" },
    { "Texts": "100 Albums - $5 Each", "ParentPrimaryKeyss": "2" },
    { "Texts": "Hip-Hop and R&amp;B Sale", "ParentPrimaryKeyss": "2" },
    { "Texts": "CD Deals", "ParentPrimaryKeyss": "2" }];
window.musicFields = {
"href": "Hrefs",
"text": "Texts",
"primaryKey": "PrimaryKeys",
"parentPrimaryKey": "ParentPrimaryKeyss"
};
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the fieldSettings property in obtrusive way.
&lt;div id="lb" &gt;
&lt;/div&gt;           
&lt;script&gt;
window.dbitem =
[{ "Texts": "Discover Music", "PrimaryKeys": "1" },
    { "Texts": "Hot Singles", "ParentPrimaryKeyss": "1" },
    { "Texts": "Rising Artists", "PrimaryKeyss": null, "ParentPrimaryKeyss": "1" },
    { "Texts": "Live Music", "ParentPrimaryKeyss": "1" },
    { "Texts": "Best of 2013 So Far", "ParentPrimaryKeyss": "1" },
{ "Texts": "Sales and Events", "PrimaryKeys": "2" },
    { "Texts": "100 Albums - $5 Each", "ParentPrimaryKeyss": "2" },
    { "Texts": "Hip-Hop and R&amp;B Sale", "ParentPrimaryKeyss": "2" },
    { "Texts": "CD Deals", "ParentPrimaryKeyss": "2" }];
window.musicFields = {
"href": "Hrefs",
"text": "Texts",
"primaryKey": "PrimaryKeys",
"parentPrimaryKey": "ParentPrimaryKeyss"
};
$(function(){
$("#lb").ejmListView({fieldSettings:"window.musicFields",dataSource:"window.dbitem"});
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>         
&lt;script&gt;
//Get or set  fieldSettings, after initialization:
// Get the fieldSettings API value.             
$("#lb").ejmListView ("option", "fieldSettings");                       
// Set the fieldSettings API
$("#lb").ejmListView ("option", "fieldSettings", true); 
&lt;/script&gt; </code>
</pre>






### headerBackButtonText<span class="type-signature type string">string</span>








Specifies the text of the back button in the header.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the headerBackButtonText property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-showHeaderBackButton="true" data-ej-headerBackButtonText="Back"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the headerBackButtonText property in obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set headerBackButtonText on initialization. 
//To set headerBackButtonText API value 
$("#lb").ejmListView ({ showHeader: true,showHeaderBackButton:true,headerBackButtonText: "Back" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  headerBackButtonText, after initialization:
// Get the headerBackButtonText API value.              
 $("#lb").ejmListView ("option", "headerBackButtonText");                       
// Set the headerBackButtonText API
$("#lb").ejmListView ("option", "headerBackButtonText", "Back");
&lt;/script&gt;</code>
</pre>






### headerTitle<span class="type-signature type string">string</span>








Specifies the title of the header.




Default Value:
{:.param}






* Title








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the headerTitle property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-headerTitle="Title"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the headerTitle property in obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set headerTitle on initialization. 
//To set headerTitle API value 
$("#lb").ejmListView ({ headerTitle: "Title" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  headerTitle, after initialization:
// Get the headerTitle API value.               
 $("#lb").ejmListView ("option", "headerTitle");                        
// Set the headerTitle API
$("#lb").ejmListView ("option", "headerTitle", "Title");
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type number">number</span>








Specifies the height of the ListView.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the height property in Unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-height="300"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the height property in Obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
// Set ListView height on initialization. 
//To set height API value 
$("#lb").ejmListView ({ height: 300 });
//Get or set the ListView height, after initialization:
// Gets the height API value.           
 $("#lb").ejmListView ("option", "height");                     
// Sets the height API
$("#lb").ejmListView ("option", "height", 300);</code>
</pre>






### hideHeaderForUnsupportedDevice<span class="type-signature type boolean">boolean</span>








Specifies whether to hide the header for unsupported device.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the hideHeaderForUnsupportedDevice property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-hideHeaderForUnsupportedDevice="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the hideHeaderForUnsupportedDevice property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set hideHeaderForUnsupportedDevice on initialization. 
//To set hideHeaderForUnsupportedDevice API value 
$("#lb").ejmListView ({ hideHeaderForUnsupportedDevice: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  hideHeaderForUnsupportedDevice, after initialization:
// Get the hideHeaderForUnsupportedDevice API value.            
 $("#lb").ejmListView ("option", "hideHeaderForUnsupportedDevice");                     
// Set the hideHeaderForUnsupportedDevice API
$("#lb").ejmListView ("option", "hideHeaderForUnsupportedDevice", true);
&lt;/script&gt;</code>
</pre>






### ios7.inline<span class="type-signature type boolean">boolean</span>








Specifies whether to show the control with inline style in ios7 mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the inline property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-rendermode="ios7" data-ej-ios7-inline="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the inline property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Setinline on initialization. 
//To set inline API value 
$("#lb").ejmListView ({ renderMode:"ios7", ios7:{inline: true} });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  inline, after initialization:
// Get the inline API value.            
$("#lb").ejmListView ("option", "ios7.inline");                 
// Set the inline API
$("#lb").ejmListView ("option", "ios7.inline", true);
&lt;/script&gt;</code>
</pre>






### items<span class="type-signature type jsonarray">JSONarray</span>








Specifies the model values of list as an array of object.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the items property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-items="window.dbitem"e&gt;
&lt;/div&gt;
&lt;script&gt;
window.dbitem =
[{ "text": "Discover Music", "primaryKey": "1" },
    { "text": "Hot Singles", "parentPrimaryKey": "1" },
    { "text": "Rising Artists", "parentPrimaryKey": "1" },
    { "text": "Live Music", "parentPrimaryKey": "1" },
    { "text": "Best of 2013 So Far", "parentPrimaryKey": "1" },
{ "text": "Sales and Events", "primaryKey": "2" },
    { "text": "100 Albums - $5 Each", "parentPrimaryKey": "2" },
    { "text": "Hip-Hop and R&amp;B Sale", "parentPrimaryKey": "2" },
    { "text": "CD Deals", "parentPrimaryKey": "2" }];
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the items property in obtrusive way.
&lt;div id="lb"&gt;
&lt;/div&gt;
&lt;script&gt;
window.dbitem = [{ "text": "Discover Music", "primaryKey": "1" },
    { "text": "Hot Singles", "parentPrimaryKey": "1" },
    { "text": "Rising Artists", "parentPrimaryKey": "1" },
    { "text": "Live Music", "parentPrimaryKey": "1" },
    { "text": "Best of 2013 So Far", "parentPrimaryKey": "1" },
{ "text": "Sales and Events", "primaryKey": "2" },
    { "text": "100 Albums - $5 Each", "parentPrimaryKey": "2" },
    { "text": "Hip-Hop and R&amp;B Sale", "parentPrimaryKey": "2" },
    { "text": "CD Deals", "parentPrimaryKey": "2" }];
//Set the items property on initialization. 
//To set items API value
$("#lb").ejmListView ({ items: "window.dbitem" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set items, after initialization:
// Get the items API value.             
$("#lb").ejmListView ("option", "items");                       
// Set the items API
$("#lb").ejmListView ("option", "items", "window.dbitem");
&lt;/script&gt;</code>
</pre>






### persistSelection<span class="type-signature type boolean">boolean</span>








Specifies whether to retain the selection of the item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the persistSelection property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-persistSelection="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the persistSelection property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set persistSelection on initialization. 
//To set persistSelection API value 
$("#lb").ejmListView ({ persistSelection: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView persistSelection, after initialization:
// Get the persistSelection API value.          
$("#lb").ejmListView ("option", "persistSelection");                    
// Set the persistSelection API
$("#lb").ejmListView ("option", "persistSelection", true);
&lt;/script&gt;</code>
</pre>






### preventSelection<span class="type-signature type boolean">boolean</span>








Specifies whether to prevent the selection of the item.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the preventSelection property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-preventSelection="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the preventSelection property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set preventSelection on initialization. 
//To set preventSelection API value 
$("#lb").ejmListView ({ preventSelection: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView preventSelection, after initialization:
// Get the preventSelection API value.          
$("#lb").ejmListView ("option", "preventSelection");                    
// Set the preventSelection API
$("#lb").ejmListView ("option", "preventSelection", true);
&lt;/script&gt;</code>
</pre>






### query<span class="type-signature type ej.query">ej.Query</span>








Specifies the query to execute with the datasource.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the query property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-fieldSettings="window.dbitem" data-ej-datasource="window.datasource" 
data-ej-query="ej.Query().from('Orders').select('ShipCity').take(5)"&gt;
&lt;/div&gt;            
&lt;script&gt;            
                // DataManager creation
                window.datasource = ej.DataManager({
        url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });
                window.dbitem = { "text": "ShipCity" };            
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the query property in obtrusive way.
&lt;div id="lb" &gt;
&lt;/div&gt;            
&lt;script&gt;            
                // DataManager creation
                window.datasource = ej.DataManager({
        url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });
                window.dbitem = { "text": "ShipCity" };   
$(function(){
$("#lb").ejmListView({fieldSettings:"window.dbitem",dataSource:"window.datasource",query:"ej.Query().from('Orders').select('ShipCity').take(5)"});
});         
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>        
&lt;script&gt;  
//Get or set  query, after initialization:
// Get the query API value.             
$("#lb").ejmListView ("option", "query");                       
// Set the query API
$("#lb").ejmListView ("option", "query", true);  
&lt;/script&gt;</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Specifies the rendering mode of the control. See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderMode property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-renderMode="auto"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the renderMode property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set renderMode on initialization. 
//To set renderMode API value 
$("#lb").ejmListView ({ renderMode: "auto" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  renderMode, after initialization:
// Get the renderMode API value.                
$("#lb").ejmListView ("option", "renderMode");                  
// Set the renderMode API
$("#lb").ejmListView ("option", "renderMode", "auto");
&lt;/script&gt;</code>
</pre>






### renderTemplate<span class="type-signature type boolean">boolean</span>








Specifies whether need to render the control with the template contents.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderTemplate property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target1"&gt;&lt;/li&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target2"&gt;&lt;/li&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target3"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;div id="target1"&gt;
        &lt;div&gt; Template1 &lt;/div&gt;
&lt;/div&gt;
&lt;div id="target2"&gt;
        &lt;div&gt; Template2 &lt;/div&gt;
&lt;/div&gt;
&lt;div id="target3"&gt;
        &lt;div&gt; Template3 &lt;/div&gt;
&lt;/div&gt;            </code>
</pre>






### selectedItemIndex<span class="type-signature type number">number</span>








Specifies the selectedItemIndex of the ListView.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the selectedItemIndex property in Unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-selectedItemIndex="2"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the selectedItemIndex property in Obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
// Set ListView selectedItemIndex on initialization. 
//To set selectedItemIndex API value 
$("#lb").ejmListView ({ selectedItemIndex: 2 });
//Get or set the ListView selectedItemIndex, after initialization:
// Gets the selectedItemIndex API value.                
 $("#lb").ejmListView ("option", "selectedItemIndex");                  
// Sets the selectedItemIndex API
$("#lb").ejmListView ("option", "selectedItemIndex", 2);</code>
</pre>






### showHeader<span class="type-signature type boolean">boolean</span>








Specifies whether to show the header.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showHeader property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-showHeader="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the showHeader property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set showHeader on initialization. 
//To set showHeader API value 
$("#lb").ejmListView ({ showHeader: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  showHeader, after initialization:
// Get the showHeader API value.                
 $("#lb").ejmListView ("option", "showHeader");                 
// Set the showHeader API
$("#lb").ejmListView ("option", "showHeader", true);  
&lt;/script&gt;          </code>
</pre>






### showHeaderBackButton<span class="type-signature type boolean">boolean</span>








Specifies whether to show the back button in the header.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showHeaderBackButton property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-showHeaderBackButton="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the showHeaderBackButton property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set showHeaderBackButton on initialization. 
//To set showHeaderBackButton API value 
$("#lb").ejmListView ({ showHeaderBackButton: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  showHeaderBackButton, after initialization:
// Get the showHeaderBackButton API value.              
 $("#lb").ejmListView ("option", "showHeaderBackButton");                       
// Set the showHeaderBackButton API
$("#lb").ejmListView ("option", "showHeaderBackButton", true);   
&lt;/script&gt;         </code>
</pre>






### showScrollbars<span class="type-signature type boolean">boolean</span>








Specifies whether need to show the scroll bars when scrolling is allowed.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showScrollbars property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-showScrollbars="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the showScrollbars property in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set showScrollbars on initialization. 
//To set showScrollbars API value 
$("#lb").ejmListView ({ showScrollbars: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  showScrollbars, after initialization:
// Get the showScrollbars API value.            
 $("#lb").ejmListView ("option", "showScrollbars");                     
// Set the showScrollbars API
$("#lb").ejmListView ("option", "showScrollbars", true); 
&lt;/script&gt;           </code>
</pre>






### templateId<span class="type-signature type boolean">boolean</span>








Specifies ID of the element contains template contents.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the templateId property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target1"&gt;&lt;/li&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target2"&gt;&lt;/li&gt;
                &lt;li data-ej-rendertemplate=true data-ej-templateid="target3"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;div id="target1"&gt;
        &lt;div&gt; Template1 &lt;/div&gt;
&lt;/div&gt;
&lt;div id="target2"&gt;
        &lt;div&gt; Template2 &lt;/div&gt;
&lt;/div&gt;
&lt;div id="target3"&gt;
        &lt;div&gt; Template3 &lt;/div&gt;
&lt;/div&gt;</code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Specifies the theme. See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-theme="auto"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the theme property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set theme on initialization. 
//To set theme API value 
$("#lb").ejmListView ({ theme: "auto" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  theme, after initialization:
// Get the theme API value.             
$("#lb").ejmListView ("option", "theme");                       
// Set the theme API
$("#lb").ejmListView ("option", "theme", "auto");
&lt;/script&gt;</code>
</pre>






### transition<span class="type-signature type string">string</span>








Specifies the transition effect while navigation happens.




Default Value:
{:.param}






* none








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the transition property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-transition="slide"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the transition property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set transition on initialization. 
//To set transition API value 
$("#lb").ejmListView ({ transition: "slide" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView transition, after initialization:
// Get the transition API value.                
$("#lb").ejmListView ("option", "transition");                  
// Set the transition API
$("#lb").ejmListView ("option", "transition", "slide");
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type number">number</span>








Specifies the width of the ListView.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the width property in Unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-width="200"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the width property in Obtrusive way.
&lt;div id="lb" &gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
// Set ListView width on initialization. 
//To set width API value 
$("#lb").ejmListView ({ width: 200 });
//Get or set the ListView width, after initialization:
// Gets the width API value.            
 $("#lb").ejmListView ("option", "width");                      
// Sets the width API
$("#lb").ejmListView ("option", "width", 200);</code>
</pre>






### windows








Section for windows mode specific functionalities.











### windows.enableCustomText<span class="type-signature type boolean">boolean</span>








By default windows title's text will be in small case. To override this behavior, set this property to true.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the windows mode enableCustomText property for header in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-windows-enableheadercustomtext="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the windows mode enableCustomText property for header in obtrusive way.
&lt;div id="lb"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableCustomText on initialization. 
//To set enableHeaderCustomText API value 
$("#lb").ejmListView ({ windows:{ enableHeaderCustomText: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableHeaderCustomText, after initialization:
// Get the enableHeaderCustomText API value.            
 $("#lb").ejmListView ("option", "windows.enableHeaderCustomText");                     
// Set the enableHeaderCustomText API
$("#lb").ejmListView ("option", "windows.enableHeaderCustomText", true);  
&lt;/script&gt;          </code>
</pre>






### windows.preventSkew<span class="type-signature type boolean">boolean</span>








Specifies whether to prevent skewing behavior in windows mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the preventSkew property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-rendermode="windows" data-ej-windows-preventSkew="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the preventSkew property in obtrusive way.
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set preventSkew on initialization. 
//To set preventSkew API value
$("#lb").ejmListView ({ windows:{preventSkew: true} });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  preventSkew, after initialization:
// Get the preventSkew API value.               
$("#lb").ejmListView ("option", "windows.preventSkew");                 
// Set the preventSkew API
$("#lb").ejmListView ("option", "windows.preventSkew", true);
&lt;/script&gt;</code>
</pre>






### windows.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to render control based on the windowsphone's current accent color and device theme.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderDefault property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-rendermode="windows" data-ej-windows-renderDefault="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the renderDefault property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set renderDefault on initialization. 
//To set renderDefault API value 
$("#lb").ejmListView ({ renderMode:"windows", windows:{renderDefault: true} });                
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  renderDefault, after initialization:
// Get the renderDefault API value.             
$("#lb").ejmListView ("option", "windows.renderDefault");                       
// Set the renderDefault API
$("#lb").ejmListView ("option", "windows.renderDefault", true);
&lt;/script&gt;</code>
</pre>




## Methods








### addItem<span class="signature">()</span>








To add item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call addItem method.
$(document).ready(function(){
$("#lb").ejmListView("addItem",$("&amp;ltli data-ej-text='Comic / Cartoon'&gt;&lt;/li&gt;"),2);
});
&lt;/script&gt;</code>
</pre>






### checkAllItem<span class="signature">()</span>








To check all the items.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call checkAllItem method.
$(document).ready(function(){
$("#lb").ejmListView("checkAllItem");
});
&lt;/script&gt;</code>
</pre>






### checkItem<span class="signature">()</span>








To check item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call checkItem method.
$(document).ready(function(){
$("#lb").ejmListView("checkItem",2);
});
&lt;/script&gt;</code>
</pre>






### clear<span class="signature">()</span>








To clear all the list item in the control before updating with new datasource.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-datasource="window.dbitem1" &gt;
&lt;/div&gt;  
&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="Clear" data-ej-touchend="touchend" /&gt;
         
&lt;script&gt;
window.dbitem1 =
[   { "text": "Hot Singles"},
    { "text": "Rising Artists"},
    { "text": "Live Music" },
    { "text": "Best of 2013 So Far"},
    { "text": "100 Albums - $5 Each"},
    { "text": "Hip-Hop and R&amp;B Sale"},
    { "text": "CD Deals"}];
window.dbitem2 =
[   { "text": "Music"},
    { "text": "Videos"},
    { "text": "Games" },
    { "text": "Chat"},
    { "text": "Others"}];
function touchend(){
    $('#lb').ejmListView("clear");
    $("#lb").ejmListView({dataSource:"window.dbitem2"});
}
&lt;/script&gt;  </code>
</pre>






### deActive<span class="signature">()</span>








To make the item in the given index to be default state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call deActive method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejmListView("deActive",2);
});
&lt;/script&gt;</code>
</pre>






### disableItem<span class="signature">()</span>








To disable item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call disableItem method.
$(document).ready(function(){
$("#lb").ejmListView("disableItem",2);
});
&lt;/script&gt;</code>
</pre>






### enableItem<span class="signature">()</span>








To enable item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call enableItem method.
$(document).ready(function(){
$("#lb").ejmListView("enableItem",2);
});
&lt;/script&gt;</code>
</pre>






### getActiveItem<span class="signature">()</span>








To get the active item.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getActiveItem method.
$(document).ready(function(){
$("#lb").ejmListView("getActiveItem");
});
&lt;/script&gt;</code>
</pre>






### getActiveItemText<span class="signature">()</span>








To get the text of the active item.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getActiveItemText method.
$(document).ready(function(){
$("#lb").ejmListView("getActiveItemText");
});
&lt;/script&gt;</code>
</pre>






### getCheckedItems<span class="signature">()</span>








To get all the checked items.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getCheckedItems method.
$(document).ready(function(){
$("#lb").ejmListView("getCheckedItems");
});
&lt;/script&gt;</code>
</pre>






### getCheckedItemsText<span class="signature">()</span>








To get the text of all the checked items.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getCheckedItemsText method.
$(document).ready(function(){
$("#lb").ejmListView("getCheckedItemsText");
});
&lt;/script&gt;</code>
</pre>






### getItemsCount<span class="signature">()</span>








To get the total item count.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getItemsCount method.
$(document).ready(function(){
$("#lb").ejmListView("getItemsCount");
});
&lt;/script&gt;</code>
</pre>






### getItemText<span class="signature">()</span>








To get the text of the item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call getItemText method.
$(document).ready(function(){
$("#lb").ejmListView("getItemText",2);
});
&lt;/script&gt;</code>
</pre>






### hasChild<span class="signature">()</span>








To check whether the item in the given index has child item.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call hasChild method.
$(document).ready(function(){
$("#lb").ejmListView("hasChild",2);
});
&lt;/script&gt;</code>
</pre>






### hide<span class="signature">()</span>








To hide the list.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call hide method.
$(document).ready(function(){
$("#lb").ejmListView("hide");
});
&lt;/script&gt;</code>
</pre>






### hideItem<span class="signature">()</span>








To hide item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call hideItem method.
$(document).ready(function(){
$("#lb").ejmListView("hideItem",2);
});
&lt;/script&gt;</code>
</pre>






### isChecked<span class="signature">()</span>








To check whether item in the given index is checked.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call isChecked method.
$(document).ready(function(){
$("#lb").ejmListView("isChecked",2);
});
&lt;/script&gt;</code>
</pre>






### loadAjaxContent<span class="signature">()</span>








To load the ajax content while selecting the item.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableAjax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableAjax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableAjax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call enableAjax method.
$(document).ready(function(){
$("#lb").ejmListView("loadAjaxContent","load1.html");
});
&lt;/script&gt;</code>
</pre>






### removeCheckMark<span class="signature">()</span>








To remove the check mark either for specific item in the given index or for all items.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call removeCheckMark method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejmListView("removeCheckMark",2);
});
&lt;/script&gt;</code>
</pre>






### removeItem<span class="signature">()</span>








To remove item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call removeItem method.
$(document).ready(function(){
$("#lb").ejmListView("removeItem",3);
});
&lt;/script&gt;</code>
</pre>






### selectItem<span class="signature">()</span>








To select item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call selectItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejmListView("selectItem",2);
});
&lt;/script&gt;</code>
</pre>






### setActive<span class="signature">()</span>








To make the item in the given index to be active state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call setActive method.
$(document).ready(function(){
$("#lb").ejmListView({persistSelection:true});
$("#lb").ejmListView("setActive",2);
});
&lt;/script&gt;</code>
</pre>






### show<span class="signature">()</span>








To show the list.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call show method.
$(document).ready(function(){
$("#lb").ejmListView("show");
});
&lt;/script&gt;</code>
</pre>






### showItem<span class="signature">()</span>








To show item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call showItem method.
$(document).ready(function(){
$("#lb").ejmListView("showItem",2);
});
&lt;/script&gt;</code>
</pre>






### unCheckAllItem<span class="signature">()</span>








To uncheck all the items.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview" data-ej-enablecheckmark="true"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call unCheckAllItem method.
$(document).ready(function(){
$("#lb").ejmListView("unCheckAllItem");
});
&lt;/script&gt;</code>
</pre>






### unCheckItem<span class="signature">()</span>








To uncheck item in the given index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call unCheckItem method.
$(document).ready(function(){
$("#lb").ejmListView("unCheckItem",2);
});
&lt;/script&gt;</code>
</pre>




## Events








### ajaxBeforeLoad








Event triggers before the ajax request happens.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>ajaxData</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the ajax settings.</td>
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
//Set the ajaxBeforeLoad property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-ajaxBeforeLoad="ajaxBeforeLoad"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//ajaxBeforeLoad event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        ajaxBeforeLoad: function (args) { //handle the event 
}
        });           
});
&lt;/script&gt;</code>
</pre>






### ajaxComplete








Event triggers after the ajax content loaded completely.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
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
//Set the ajaxComplete property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-ajaxComplete="ajaxComplete"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//ajaxComplete event for ListView
&lt;div id="lb" data-role="ejmlistview" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        ajaxComplete: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>






### ajaxError








Event triggers when the ajax request failed.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>errorThrown</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the error thrown in the ajax post.</td>
</tr>
<tr>
<td class="name"><code>textStatus</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the status.</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the curent list item.</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current item text.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current item index.</td>
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
//Set the ajaxError property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-ajaxError="ajaxError"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//ajaxError event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        ajaxError: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>






### ajaxSuccess








Event triggers after the ajax content loaded successfully.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>content</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ajax current content.</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the curent list item.</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current item text.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current item index.</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current url of the ajax post.</td>
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
//Set the ajaxSuccess property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-ajaxSuccess="ajaxSuccess"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//ajaxSuccess event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" data-ej-enableajax="true"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        ajaxSuccess: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>






### headerBackButtonTap








Event triggers when touch end happens on the back button in the header.

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
<td class="description last">Event parameters from listbox.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the text of the button.</td>
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
// Set the headerBackButtonTap property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-showHeaderBackButton="true" data-ej-headerBackButtonTap="headerBackButtonTap"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//headerBackButtonTap event for ListView
&lt;div id="lb" data-role="ejmlistview" data-ej-showHeaderBackButton="true"&gt;
         &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#lb").ejmListView({
        headerBackButtonTap: function (args) { //handle the event 
}
        });         
&lt;/script&gt;</code>
</pre>






### load








Event triggers before the items loaded.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
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
//Set the load property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-load="load"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//load event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        load: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>






### loadComplete








Event triggers after the items loaded.

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
<td class="description last">Event parameters from listview.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
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
//Set the loadComplete property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-loadComplete="loadComplete"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//loadComplete event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        loadComplete: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>






### touchEnd








Event triggers when touch end happens on the item.

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
<td class="description last">Event parameters from listbox.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>hasChild</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If the child element exist return true; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current list item.</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current text of item.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current Index of the item.</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If checked return true; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>checkedItems</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the list of checked items.</td>
</tr>
<tr>
<td class="name"><code>checkedItemsText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current checked item text.</td>
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
//Set the touchEnd property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-touchEnd="touchEnd"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//touchEnd event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        touchEnd: function (args) { //handle the event 
}
        });    
});
&lt;/script&gt;</code>
</pre>






### touchStart








Event triggers when touch start happens on the item.

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
<td class="description last">Event parameters from listbox.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>hasChild</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If the child element exist return true; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current list item.</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current text of item.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current Index of the item.</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If checked return true; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>checkedItems</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the list of checked items.</td>
</tr>
<tr>
<td class="name"><code>checkedItemsText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current checked item text.</td>
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
//Set the touchStart property in unobtrusive way.
&lt;div id="lb" data-role="ejmlistview" data-ej-touchStart="touchStart"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//touchStart event for ListView
&lt;div id="lb" data-role="ejmlistview"&gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Canvas Art"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Black white"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Children"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Preschool Crafts"&gt;&lt;/li&gt;
                &lt;li data-ej-text="School-age Crafts"&gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){
$("#lb").ejmListView({
        touchStart: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



