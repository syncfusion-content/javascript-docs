---
layout: post
title: ejListView
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html ListView control.





$(element).ejListView<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
//Set listview in obtrusive way.
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
$("#lb").ejListView(); 
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.core

* module:ej.unobtrusive

* module:ej.data

* module:ej.touch

* module:ej.checkbox

* module:ej.listviewbase


## Members




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for ListView theme. This cssClass API helps to use custom skinning option for ListView control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}

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
$("#lb").ejListView ({ cssClass: "customclass" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  cssClass, after initialization:
// Get the cssClass API value.          
 $("#lb").ejListView ("option", "cssClass");                    
// Set the cssClass API
$("#lb").ejListView ("option", "cssClass", "customclass");
&lt;/script&gt;</code>
</pre>



### dataSource<span class="type-signature type jsonarray">JSONArray</span>
{:#members:datasource}




Specifies the datasource is enabled.


Default Value:
{:.param}



* []




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the dataSource property in obtrusive way.
&lt;div id="lb" &gt;
&lt;/div&gt;           
&lt;script&gt;
$(function(){
$("#lb").ejListView({dataSource:window.dbitem});
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
$("#lb").ejListView ("option", "dataSource");                   
// Set the dataSource API
$("#lb").ejListView ("option", "dataSource", true);   
&lt;/script&gt;                     </code>
</pre>



### enableAjax<span class="type-signature type boolean">boolean</span>
{:#members:enableajax}




Specifies whether to load ajax content while selecting item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ enableAjax: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableAjax, after initialization:
// Get the enableAjax API value.                
$("#lb").ejListView ("option", "enableAjax");                   
// Set the enableAjax API
$("#lb").ejListView ("option", "enableAjax", true);
&lt;/script&gt;</code>
</pre>



### enableCache<span class="type-signature type boolean">boolean</span>
{:#members:enablecache}




Specifies whether to enable caching the content.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableCache property in obtrusive way.
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Set enableCache on initialization. 
//To set enableCache API value             
$("#lb").ejListView ({ enableAjax: true,enableCache: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableCache, after initialization:
// Get the enableCache API value.               
$("#lb").ejListView ("option", "enableCache");                  
// Set the enableCache API
$("#lb").ejListView ("option", "enableCache", true);
&lt;/script&gt;</code>
</pre>



### enableCheckMark<span class="type-signature type boolean">boolean</span>
{:#members:enablecheckmark}




Specifies whether to enable check mark for the item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ enableCheckMark: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView enableCheckMark, after initialization:
// Get the enableCheckMark API value.           
$("#lb").ejListView ("option", "enableCheckMark");                      
// Set the enableCheckMark API
$("#lb").ejListView ("option", "enableCheckMark", true);    
&lt;/script&gt;        </code>
</pre>



### enableFiltering<span class="type-signature type boolean">boolean</span>
{:#members:enablefiltering}




Specifies whether to enable the filtering feature to filter the item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ enableFiltering: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView enableFiltering, after initialization:
// Get the enableFiltering API value.           
$("#lb").ejListView ("option", "enableFiltering");                      
// Set the enableFiltering API
$("#lb").ejListView ("option", "enableFiltering", true);    
&lt;/script&gt;        </code>
</pre>



### enableGroupList<span class="type-signature type boolean">boolean</span>
{:#members:enablegrouplist}




Specifies whether to group the list item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ enableGroupList: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enableGroupList, after initialization:
// Get the enableGroupList API value.           
 $("#lb").ejListView ("option", "enableGroupList");                     
// Set the enableGroupList API
$("#lb").ejListView ("option", "enableGroupList", true);
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ enablePersistence: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#lb").ejListView ("option", "enablePersistence");                   
// Set the enablePersistence API
$("#lb").ejListView ("option", "enablePersistence", true);
&lt;/script&gt;</code>
</pre>



### fieldSettings<span class="type-signature type object">object</span>
{:#members:fieldsettings}




Specifies the field settings to map the datasource.



Example
{:.example}

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
$("#lb").ejListView({fieldSettings:"window.musicFields",dataSource:"window.dbitem"});
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>         
&lt;script&gt;
//Get or set  fieldSettings, after initialization:
// Get the fieldSettings API value.             
$("#lb").ejListView ("option", "fieldSettings");                        
// Set the fieldSettings API
$("#lb").ejListView ("option", "fieldSettings", true); 
&lt;/script&gt; </code>
</pre>



### headerBackButtonText<span class="type-signature type string">string</span>
{:#members:headerbackbuttontext}




Specifies the text of the back button in the header.


Default Value:
{:.param}



* null




Example
{:.example}

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
$("#lb").ejListView ({showHeader: true,showHeaderBackButton:true, headerBackButtonText: "Back" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  headerBackButtonText, after initialization:
// Get the headerBackButtonText API value.              
 $("#lb").ejListView ("option", "headerBackButtonText");                        
// Set the headerBackButtonText API
$("#lb").ejListView ("option", "headerBackButtonText", "Back");
&lt;/script&gt;</code>
</pre>



### headerTitle<span class="type-signature type string">string</span>
{:#members:headertitle}




Specifies the title of the header.


Default Value:
{:.param}



* Title




Example
{:.example}

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
$("#lb").ejListView ({ headerTitle: "Title" });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  headerTitle, after initialization:
// Get the headerTitle API value.               
 $("#lb").ejListView ("option", "headerTitle");                 
// Set the headerTitle API
$("#lb").ejListView ("option", "headerTitle", "Title");
&lt;/script&gt;</code>
</pre>



### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the height property in obtrusive way.
&lt;div id="lb" data-ej-allowScrolling=true &gt;
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
// Set height on initialization. 
//To set height API value 
$("#lb").ejListView ({ height: 300 });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  height, after initialization:
// Get the height API value.            
 $("#lb").ejListView ("option", "height");                      
// Set the height API
$("#lb").ejListView ("option", "height", 300);
&lt;/script&gt;</code>
</pre>



### persistSelection<span class="type-signature type boolean">boolean</span>
{:#members:persistselection}




Specifies whether to retain the selection of the item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ persistSelection: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView persistSelection, after initialization:
// Get the persistSelection API value.          
$("#lb").ejListView ("option", "persistSelection");                     
// Set the persistSelection API
$("#lb").ejListView ("option", "persistSelection", true);
&lt;/script&gt;</code>
</pre>



### preventSelection<span class="type-signature type boolean">boolean</span>
{:#members:preventselection}




Specifies whether to prevent the selection of the item.


Default Value:
{:.param}



* false




Example
{:.example}

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
$("#lb").ejListView ({ preventSelection: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the ListView preventSelection, after initialization:
// Get the preventSelection API value.          
$("#lb").ejListView ("option", "preventSelection");                     
// Set the preventSelection API
$("#lb").ejListView ("option", "preventSelection", true);
&lt;/script&gt;</code>
</pre>



### query<span class="type-signature type ej.query">ej.Query</span>
{:#members:query}




Specifies the query to execute with the datasource.


Default Value:
{:.param}



* null




Example
{:.example}

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
$("#lb").ejListView({fieldSettings:"window.dbitem",dataSource:"window.datasource",query:"ej.Query().from('Orders').select('ShipCity').take(5)"});
});         
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>        
&lt;script&gt;  
//Get or set  query, after initialization:
// Get the query API value.             
$("#lb").ejListView ("option", "query");                        
// Set the query API
$("#lb").ejListView ("option", "query", true);  
&lt;/script&gt;</code>
</pre>



### renderTemplate<span class="type-signature type boolean">boolean</span>
{:#members:rendertemplate}




Specifies whether need to render the control with the template contents.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderTemplate property in obtrusive way.
&lt;div id="lb"&gt;
        &lt;ul&gt;
                &lt;li data-ej-templateid="target1"&gt;&lt;/li&gt;
                &lt;li data-ej-templateid="target2"&gt;&lt;/li&gt;
                &lt;li data-ej-templateid="target3"&gt;&lt;/li&gt;
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
&lt;/div&gt;
&lt;script&gt;
// Set renderTemplate on initialization. 
//To set renderTemplate API value 
$("#lb").ejListView ({ renderTemplate: true });
&lt;/script&gt;</code>
</pre>



### selectedItemIndex<span class="type-signature type number">number</span>
{:#members:selecteditemindex}




Specifies the index of item which need to be in selected state initially while loading.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the selectedItemIndex property in obtrusive way.
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
// Set selectedItemIndex on initialization. 
//To set selectedItemIndex API value 
$("#lb").ejListView ({ selectedItemIndex: 2 });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  selectedItemIndex, after initialization:
// Get the selectedItemIndex API value.         
 $("#lb").ejListView ("option", "selectedItemIndex");                   
// Set the selectedItemIndex API
$("#lb").ejListView ("option", "selectedItemIndex", 2);
&lt;/script&gt;</code>
</pre>



### showHeader<span class="type-signature type boolean">boolean</span>
{:#members:showheader}




Specifies whether to show the header.


Default Value:
{:.param}



* true




Example
{:.example}

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
$("#lb").ejListView ({ showHeader: true });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  showHeader, after initialization:
// Get the showHeader API value.                
 $("#lb").ejListView ("option", "showHeader");                  
// Set the showHeader API
$("#lb").ejListView ("option", "showHeader", true);  
&lt;/script&gt;          </code>
</pre>



### templateId<span class="type-signature type boolean">boolean</span>
{:#members:templateid}




Specifies ID of the element contains template contents.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the templateId property in unobtrusive way.
&lt;div id="lb" data-role="ejlistview"&gt;
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



### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the width property in obtrusive way.
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
// Set width on initialization. 
//To set width API value 
$("#lb").ejListView ({ width: 200 });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set  width, after initialization:
// Get the width API value.             
 $("#lb").ejListView ("option", "width");                       
// Set the width API
$("#lb").ejListView ("option", "width", 200);
&lt;/script&gt;</code>
</pre>


## Methods




### addItem<span class="signature">()</span>
{:#methods:additem}




To add item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call addItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("addItem",$("&amp;ltli data-ej-text='Comic / Cartoon'&gt;&lt;/li&gt;"),2);
});
&lt;/script&gt;</code>
</pre>



### checkAllItem<span class="signature">()</span>
{:#methods:checkallitem}




To check all the items.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call checkAllItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("checkAllItem");
});
&lt;/script&gt;</code>
</pre>



### checkItem<span class="signature">()</span>
{:#methods:checkitem}




To check item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call checkItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("checkItem",2);
});
&lt;/script&gt;</code>
</pre>



### clear<span class="signature">()</span>
{:#methods:clear}




To clear all the list item in the control before updating with new datasource.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" &gt;
&lt;/div&gt;  
&lt;input id="button" /&gt;
         
&lt;script&gt;
$(document).ready(function(){
$("#button").ejButton();
$("#button").ejButton({ text: "Clear" });
$("#lb").ejListView();
$("#lb").ejListView({dataSource:"window.dbitem1"});
$("#button").ejButton({ 
click: function (args) { 
$('#lb').ejListView("clear");
$("#lb").ejListView({dataSource:"window.dbitem2"});
}
});
});
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
&lt;/script&gt;  </code>
</pre>



### deActive<span class="signature">()</span>
{:#methods:deactive}




To make the item in the given index to be default state.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call deActive method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("deActive",2);
});
&lt;/script&gt;</code>
</pre>



### disableItem<span class="signature">()</span>
{:#methods:disableitem}




To disable item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call disableItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("disableItem",2);
});
&lt;/script&gt;</code>
</pre>



### enableItem<span class="signature">()</span>
{:#methods:enableitem}




To enable item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call enableItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("enableItem",2);
});
&lt;/script&gt;</code>
</pre>



### getActiveItem<span class="signature">()</span>
{:#methods:getactiveitem}




To get the active item.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getActiveItem method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("getActiveItem");
});
&lt;/script&gt;</code>
</pre>



### getActiveItemText<span class="signature">()</span>
{:#methods:getactiveitemtext}




To get the text of the active item.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getActiveItemText method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("getActiveItemText");
});
&lt;/script&gt;</code>
</pre>



### getCheckedItems<span class="signature">()</span>
{:#methods:getcheckeditems}




To get all the checked items.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getCheckedItems method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true})
$("#lb").ejListView("getCheckedItems");
});
&lt;/script&gt;</code>
</pre>



### getCheckedItemsText<span class="signature">()</span>
{:#methods:getcheckeditemstext}




To get the text of all the checked items.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getCheckedItemsText method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true})
$("#lb").ejListView("getCheckedItemsText");
});
&lt;/script&gt;</code>
</pre>



### getItemsCount<span class="signature">()</span>
{:#methods:getitemscount}




To get the total item count.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getItemsCount method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("getItemsCount");
});
&lt;/script&gt;</code>
</pre>



### getItemText<span class="signature">()</span>
{:#methods:getitemtext}




To get the text of the item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call getItemText method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("getItemText",2);
});
&lt;/script&gt;</code>
</pre>



### hasChild<span class="signature">()</span>
{:#methods:haschild}




To check whether the item in the given index has child item.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call hasChild method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hasChild",2);
});
&lt;/script&gt;</code>
</pre>



### hide<span class="signature">()</span>
{:#methods:hide}




To hide the list.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call hide method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hide");
});
&lt;/script&gt;</code>
</pre>



### hideItem<span class="signature">()</span>
{:#methods:hideitem}




To hide item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call hideItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hideItem",2);
});
&lt;/script&gt;</code>
</pre>



### isChecked<span class="signature">()</span>
{:#methods:ischecked}




To check whether item in the given index is checked.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call isChecked method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("isChecked",2);
});
&lt;/script&gt;</code>
</pre>



### loadAjaxContent<span class="signature">()</span>
{:#methods:loadajaxcontent}




To load the ajax content while selecting the item.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Call enableAjax method.
$(document).ready(function(){
$("#lb").ejListView ({ enableAjax: true });
$("#lb").ejListView("loadAjaxContent","load1.html");
});
&lt;/script&gt;</code>
</pre>



### removeCheckMark<span class="signature">()</span>
{:#methods:removecheckmark}




To remove the check mark either for specific item in the given index or for all items.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call removeCheckMark method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("removeCheckMark",2);
});
&lt;/script&gt;</code>
</pre>



### removeItem<span class="signature">()</span>
{:#methods:removeitem}




To remove item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call removeItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("removeItem",3);
});
&lt;/script&gt;</code>
</pre>



### selectItem<span class="signature">()</span>
{:#methods:selectitem}




To select item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call selectItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("selectItem",2);
});
&lt;/script&gt;</code>
</pre>



### setActive<span class="signature">()</span>
{:#methods:setactive}




To make the item in the given index to be active state.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call setActive method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("setActive",2);
});
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#methods:show}




To show the list.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call show method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("show");
});
&lt;/script&gt;</code>
</pre>



### showItem<span class="signature">()</span>
{:#methods:showitem}




To show item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call showItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("showItem",2);
});
&lt;/script&gt;</code>
</pre>



### unCheckAllItem<span class="signature">()</span>
{:#methods:uncheckallitem}




To uncheck all the items.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call unCheckAllItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("unCheckAllItem");
});
&lt;/script&gt;</code>
</pre>



### unCheckItem<span class="signature">()</span>
{:#methods:uncheckitem}




To uncheck item in the given index.



Example
{:.example}

<pre class="prettyprint">
<code> 
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
// Call unCheckItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("unCheckItem",2);
});
&lt;/script&gt;</code>
</pre>


## Events




### ajaxBeforeLoad
{:#events:ajaxbeforeload}




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
//ajaxBeforeLoad event for ListView
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxBeforeLoad: function (args) { //handle the event 
}
        });           
});
&lt;/script&gt;</code>
</pre>



### ajaxComplete
{:#events:ajaxcomplete}




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
//ajaxComplete event for ListView
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxComplete: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### ajaxError
{:#events:ajaxerror}




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
//ajaxError event for ListView
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxError: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### ajaxSuccess
{:#events:ajaxsuccess}




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
//ajaxSuccess event for ListView
&lt;div id="lb" &gt;
        &lt;ul&gt;
                &lt;li data-ej-text="Man of Steel" data-ej-href="load1.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="World War Z" data-ej-href="load2.html" &gt;&lt;/li&gt;
                &lt;li data-ej-text="Monsters University" data-ej-href="load3.html" &gt;&lt;/li&gt;
        &lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxSuccess: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### load
{:#events:load}




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
//load event for ListView
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
$(document).ready(function(){
$("#lb").ejListView({
        load: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### loadComplete
{:#events:loadcomplete}




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
//loadComplete event for ListView
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
$(document).ready(function(){
$("#lb").ejListView({
        loadComplete: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### mouseDown
{:#events:mousedown}




Event triggers when mouse down happens on the item.

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
//mouseDown event for ListView
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
$(document).ready(function(){
$("#lb").ejListView({
        mouseDown: function (args) { //handle the event 
}
        });         
});
&lt;/script&gt;</code>
</pre>



### mouseUP
{:#events:mouseup}




Event triggers when mouse up happens on the item.

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
//mouseUP event for ListView
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
$(document).ready(function(){
$("#lb").ejListView({
        mouseUP: function (args) { //handle the event 
}
        });    
});
&lt;/script&gt;</code>
</pre>


