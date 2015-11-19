---
layout: post
title: ejListView
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejListView



The ListView widget builds interactive ListView interface. This control allows you to select an item from a list-like interface and display a set of data items in different layouts or views. Lists are used for displaying data, data navigation, result lists, and data entry.





$(element).ejListView<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
//Set listview in obtrusive way.
<div id="lb">
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script> 
// Create ListView
$("#lb").ejListView(); 
</script>{% endhighlight %}




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


{% highlight html %}
 
//Set the cssClass property in obtrusive way.
<div id="lb" >
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set cssClass on initialization. 
//To set cssClass API value 
$("#lb").ejListView ({ cssClass: "customclass" });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  cssClass, after initialization:
// Get the cssClass API value.          
 $("#lb").ejListView ("option", "cssClass");                    
// Set the cssClass API
$("#lb").ejListView ("option", "cssClass", "customclass");
</script>{% endhighlight %}




### dataSource<span class="type-signature type jsonarray">JSONArray</span>
{:#members:datasource}




Specifies the datasource is enabled.


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
 
//Set the dataSource property in obtrusive way.
<div id="lb" >
</div>           
<script>
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
</script>  {% endhighlight %}


{% highlight html %}
       
<script>
//Get or set  dataSource, after initialization:
// Get the dataSource API value.                
$("#lb").ejListView ("option", "dataSource");                   
// Set the dataSource API
$("#lb").ejListView ("option", "dataSource", true);   
</script>                     {% endhighlight %}




### enableAjax<span class="type-signature type boolean">boolean</span>
{:#members:enableajax}




Specifies whether to load ajax content while selecting item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
  
//Set the enableAjax property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
// Set enableAjax on initialization. 
//To set enableAjax API value
$("#lb").ejListView ({ enableAjax: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  enableAjax, after initialization:
// Get the enableAjax API value.                
$("#lb").ejListView ("option", "enableAjax");                   
// Set the enableAjax API
$("#lb").ejListView ("option", "enableAjax", true);
</script>{% endhighlight %}




### enableCache<span class="type-signature type boolean">boolean</span>
{:#members:enablecache}




Specifies whether to enable caching the content.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the enableCache property in obtrusive way.
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
// Set enableCache on initialization. 
//To set enableCache API value             
$("#lb").ejListView ({ enableAjax: true,enableCache: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  enableCache, after initialization:
// Get the enableCache API value.               
$("#lb").ejListView ("option", "enableCache");                  
// Set the enableCache API
$("#lb").ejListView ("option", "enableCache", true);
</script>{% endhighlight %}




### enableCheckMark<span class="type-signature type boolean">boolean</span>
{:#members:enablecheckmark}




Specifies whether to enable check mark for the item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the enableCheckMark property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set enableCheckMark on initialization. 
//To set enableCheckMark API value 
$("#lb").ejListView ({ enableCheckMark: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the ListView enableCheckMark, after initialization:
// Get the enableCheckMark API value.           
$("#lb").ejListView ("option", "enableCheckMark");                      
// Set the enableCheckMark API
$("#lb").ejListView ("option", "enableCheckMark", true);    
</script>        {% endhighlight %}




### enableFiltering<span class="type-signature type boolean">boolean</span>
{:#members:enablefiltering}




Specifies whether to enable the filtering feature to filter the item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the enableFiltering property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set enableFiltering on initialization. 
//To set enableFiltering API value 
$("#lb").ejListView ({ enableFiltering: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the ListView enableFiltering, after initialization:
// Get the enableFiltering API value.           
$("#lb").ejListView ("option", "enableFiltering");                      
// Set the enableFiltering API
$("#lb").ejListView ("option", "enableFiltering", true);    
</script>        {% endhighlight %}




### enableGroupList<span class="type-signature type boolean">boolean</span>
{:#members:enablegrouplist}




Specifies whether to group the list item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the enableGroupList property in obtrusive way.
<div id="lb">
        <ul data-ej-grouplisttitle="Network">
                <li data-ej-text="Airplane Mode"></li>
                <li data-ej-text="Wi-Fi"></li>
                <li data-ej-text="Notifications"></li>
                <li data-ej-text="Location Services"></li>
        </ul>
        <ul data-ej-grouplisttitle="Apps">
                <li data-ej-text="Sound"></li>
                <li data-ej-text="Brightness"></li>
                <li data-ej-text="Wallpaper"></li>
        </ul>
        <ul data-ej-grouplisttitle="Settings">
                <li data-ej-text="General"></li>
                <li data-ej-text="Brightness"></li>
                <li data-ej-text="Wallpaper"></li>
        </ul>
</div>
<script>
// Set enableGroupList on initialization. 
//To set enableGroupList API value 
$("#lb").ejListView ({ enableGroupList: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  enableGroupList, after initialization:
// Get the enableGroupList API value.           
 $("#lb").ejListView ("option", "enableGroupList");                     
// Set the enableGroupList API
$("#lb").ejListView ("option", "enableGroupList", true);
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the enablePersistence property in obtrusive way.
<div id="lb">
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set enablePersistence on initialization. 
//To set enablePersistence API value 
$("#lb").ejListView ({ enablePersistence: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#lb").ejListView ("option", "enablePersistence");                   
// Set the enablePersistence API
$("#lb").ejListView ("option", "enablePersistence", true);
</script>{% endhighlight %}




### fieldSettings<span class="type-signature type object">object</span>
{:#members:fieldsettings}




Specifies the field settings to map the datasource.



Example
{:.example}


{% highlight html %}
 
//Set the fieldSettings property in obtrusive way.
<div id="lb" >
</div>           
<script>
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
</script>{% endhighlight %}


{% highlight html %}
         
<script>
//Get or set  fieldSettings, after initialization:
// Get the fieldSettings API value.             
$("#lb").ejListView ("option", "fieldSettings");                        
// Set the fieldSettings API
$("#lb").ejListView ("option", "fieldSettings", true); 
</script> {% endhighlight %}




### headerBackButtonText<span class="type-signature type string">string</span>
{:#members:headerbackbuttontext}




Specifies the text of the back button in the header.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//Set the headerBackButtonText property in obtrusive way.
<div id="lb" >
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set headerBackButtonText on initialization. 
//To set headerBackButtonText API value 
$("#lb").ejListView ({showHeader: true,showHeaderBackButton:true, headerBackButtonText: "Back" });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  headerBackButtonText, after initialization:
// Get the headerBackButtonText API value.              
 $("#lb").ejListView ("option", "headerBackButtonText");                        
// Set the headerBackButtonText API
$("#lb").ejListView ("option", "headerBackButtonText", "Back");
</script>{% endhighlight %}




### headerTitle<span class="type-signature type string">string</span>
{:#members:headertitle}




Specifies the title of the header.


Default Value:
{:.param}



* Title




Example
{:.example}


{% highlight html %}
 
//Set the headerTitle property in obtrusive way.
<div id="lb" >
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set headerTitle on initialization. 
//To set headerTitle API value 
$("#lb").ejListView ({ headerTitle: "Title" });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  headerTitle, after initialization:
// Get the headerTitle API value.               
 $("#lb").ejListView ("option", "headerTitle");                 
// Set the headerTitle API
$("#lb").ejListView ("option", "headerTitle", "Title");
</script>{% endhighlight %}




### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//Set the height property in obtrusive way.
<div id="lb" data-ej-allowScrolling=true >
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set height on initialization. 
//To set height API value 
$("#lb").ejListView ({ height: 300 });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  height, after initialization:
// Get the height API value.            
 $("#lb").ejListView ("option", "height");                      
// Set the height API
$("#lb").ejListView ("option", "height", 300);
</script>{% endhighlight %}




### persistSelection<span class="type-signature type boolean">boolean</span>
{:#members:persistselection}




Specifies whether to retain the selection of the item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the persistSelection property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set persistSelection on initialization. 
//To set persistSelection API value 
$("#lb").ejListView ({ persistSelection: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the ListView persistSelection, after initialization:
// Get the persistSelection API value.          
$("#lb").ejListView ("option", "persistSelection");                     
// Set the persistSelection API
$("#lb").ejListView ("option", "persistSelection", true);
</script>{% endhighlight %}




### preventSelection<span class="type-signature type boolean">boolean</span>
{:#members:preventselection}




Specifies whether to prevent the selection of the item.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the preventSelection property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set preventSelection on initialization. 
//To set preventSelection API value 
$("#lb").ejListView ({ preventSelection: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the ListView preventSelection, after initialization:
// Get the preventSelection API value.          
$("#lb").ejListView ("option", "preventSelection");                     
// Set the preventSelection API
$("#lb").ejListView ("option", "preventSelection", true);
</script>{% endhighlight %}




### query<span class="type-signature type ej.query">ej.Query</span>
{:#members:query}




Specifies the query to execute with the datasource.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//Set the query property in obtrusive way.
<div id="lb" >
</div>            
<script>            
                // DataManager creation
                window.datasource = ej.DataManager({
        url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });
                window.dbitem = { "text": "ShipCity" };   
$(function(){
$("#lb").ejListView({fieldSettings:"window.dbitem",dataSource:"window.datasource",query:"ej.Query().from('Orders').select('ShipCity').take(5)"});
});         
</script>{% endhighlight %}


{% highlight html %}
        
<script>  
//Get or set  query, after initialization:
// Get the query API value.             
$("#lb").ejListView ("option", "query");                        
// Set the query API
$("#lb").ejListView ("option", "query", true);  
</script>{% endhighlight %}




### renderTemplate<span class="type-signature type boolean">boolean</span>
{:#members:rendertemplate}




Specifies whether need to render the control with the template contents.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the renderTemplate property in obtrusive way.
<div id="lb">
        <ul>
                <li data-ej-templateid="target1"></li>
                <li data-ej-templateid="target2"></li>
                <li data-ej-templateid="target3"></li>
        </ul>
</div>
<div id="target1">
        <div> Template1 </div>
</div>
<div id="target2">
        <div> Template2 </div>
</div>
<div id="target3">
        <div> Template3 </div>
</div>
<script>
// Set renderTemplate on initialization. 
//To set renderTemplate API value 
$("#lb").ejListView ({ renderTemplate: true });
</script>{% endhighlight %}




### selectedItemIndex<span class="type-signature type number">number</span>
{:#members:selecteditemindex}




Specifies the index of item which need to be in selected state initially while loading.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//Set the selectedItemIndex property in obtrusive way.
<div id="lb">
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set selectedItemIndex on initialization. 
//To set selectedItemIndex API value 
$("#lb").ejListView ({ selectedItemIndex: 2 });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  selectedItemIndex, after initialization:
// Get the selectedItemIndex API value.         
 $("#lb").ejListView ("option", "selectedItemIndex");                   
// Set the selectedItemIndex API
$("#lb").ejListView ("option", "selectedItemIndex", 2);
</script>{% endhighlight %}




### showHeader<span class="type-signature type boolean">boolean</span>
{:#members:showheader}




Specifies whether to show the header.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
//Set the showHeader property in obtrusive way.
<div id="lb">
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set showHeader on initialization. 
//To set showHeader API value 
$("#lb").ejListView ({ showHeader: true });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  showHeader, after initialization:
// Get the showHeader API value.                
 $("#lb").ejListView ("option", "showHeader");                  
// Set the showHeader API
$("#lb").ejListView ("option", "showHeader", true);  
</script>          {% endhighlight %}




### templateId<span class="type-signature type boolean">boolean</span>
{:#members:templateid}




Specifies ID of the element contains template contents.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//Set the templateId property in unobtrusive way.
<div id="lb" data-role="ejlistview">
        <ul>
                <li data-ej-rendertemplate=true data-ej-templateid="target1"></li>
                <li data-ej-rendertemplate=true data-ej-templateid="target2"></li>
                <li data-ej-rendertemplate=true data-ej-templateid="target3"></li>
        </ul>
</div>
<div id="target1">
        <div> Template1 </div>
</div>
<div id="target2">
        <div> Template2 </div>
</div>
<div id="target3">
        <div> Template3 </div>
</div>{% endhighlight %}




### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//Set the width property in obtrusive way.
<div id="lb">
         <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Set width on initialization. 
//To set width API value 
$("#lb").ejListView ({ width: 200 });
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set  width, after initialization:
// Get the width API value.             
 $("#lb").ejListView ("option", "width");                       
// Set the width API
$("#lb").ejListView ("option", "width", 200);
</script>{% endhighlight %}



## Methods




### addItem<span class="signature">()</span>
{:#methods:additem}




To add item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call addItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("addItem",$("&amp;ltli data-ej-text='Comic / Cartoon'></li>"),2);
});
</script>{% endhighlight %}




### checkAllItem<span class="signature">()</span>
{:#methods:checkallitem}




To check all the items.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call checkAllItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("checkAllItem");
});
</script>{% endhighlight %}




### checkItem<span class="signature">()</span>
{:#methods:checkitem}




To check item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call checkItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("checkItem",2);
});
</script>{% endhighlight %}




### clear<span class="signature">()</span>
{:#methods:clear}




To clear all the list item in the control before updating with new datasource.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
</div>  
<input id="button" />
         
<script>
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
</script>  {% endhighlight %}




### deActive<span class="signature">()</span>
{:#methods:deactive}




To make the item in the given index to be default state.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call deActive method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("deActive",2);
});
</script>{% endhighlight %}




### disableItem<span class="signature">()</span>
{:#methods:disableitem}




To disable item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call disableItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("disableItem",2);
});
</script>{% endhighlight %}




### enableItem<span class="signature">()</span>
{:#methods:enableitem}




To enable item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call enableItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("enableItem",2);
});
</script>{% endhighlight %}




### getActiveItem<span class="signature">()</span>
{:#methods:getactiveitem}




To get the active item.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getActiveItem method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("getActiveItem");
});
</script>{% endhighlight %}




### getActiveItemText<span class="signature">()</span>
{:#methods:getactiveitemtext}




To get the text of the active item.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getActiveItemText method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("getActiveItemText");
});
</script>{% endhighlight %}




### getCheckedItems<span class="signature">()</span>
{:#methods:getcheckeditems}




To get all the checked items.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getCheckedItems method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true})
$("#lb").ejListView("getCheckedItems");
});
</script>{% endhighlight %}




### getCheckedItemsText<span class="signature">()</span>
{:#methods:getcheckeditemstext}




To get the text of all the checked items.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getCheckedItemsText method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true})
$("#lb").ejListView("getCheckedItemsText");
});
</script>{% endhighlight %}




### getItemsCount<span class="signature">()</span>
{:#methods:getitemscount}




To get the total item count.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getItemsCount method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("getItemsCount");
});
</script>{% endhighlight %}




### getItemText<span class="signature">()</span>
{:#methods:getitemtext}




To get the text of the item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call getItemText method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("getItemText",2);
});
</script>{% endhighlight %}




### hasChild<span class="signature">()</span>
{:#methods:haschild}




To check whether the item in the given index has child item.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call hasChild method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hasChild",2);
});
</script>{% endhighlight %}




### hide<span class="signature">()</span>
{:#methods:hide}




To hide the list.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call hide method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hide");
});
</script>{% endhighlight %}




### hideItem<span class="signature">()</span>
{:#methods:hideitem}




To hide item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call hideItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("hideItem",2);
});
</script>{% endhighlight %}




### isChecked<span class="signature">()</span>
{:#methods:ischecked}




To check whether item in the given index is checked.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call isChecked method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("isChecked",2);
});
</script>{% endhighlight %}




### loadAjaxContent<span class="signature">()</span>
{:#methods:loadajaxcontent}




To load the ajax content while selecting the item.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
// Call enableAjax method.
$(document).ready(function(){
$("#lb").ejListView ({ enableAjax: true });
$("#lb").ejListView("loadAjaxContent","load1.html");
});
</script>{% endhighlight %}




### removeCheckMark<span class="signature">()</span>
{:#methods:removecheckmark}




To remove the check mark either for specific item in the given index or for all items.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call removeCheckMark method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("removeCheckMark",2);
});
</script>{% endhighlight %}




### removeItem<span class="signature">()</span>
{:#methods:removeitem}




To remove item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call removeItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("removeItem",3);
});
</script>{% endhighlight %}




### selectItem<span class="signature">()</span>
{:#methods:selectitem}




To select item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call selectItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("selectItem",2);
});
</script>{% endhighlight %}




### setActive<span class="signature">()</span>
{:#methods:setactive}




To make the item in the given index to be active state.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call setActive method.
$(document).ready(function(){
$("#lb").ejListView({persistSelection:true});
$("#lb").ejListView("setActive",2);
});
</script>{% endhighlight %}




### show<span class="signature">()</span>
{:#methods:show}




To show the list.



Example
{:.example}


{% highlight html %}
 
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call show method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("show");
});
</script>{% endhighlight %}




### showItem<span class="signature">()</span>
{:#methods:showitem}




To show item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call showItem method.
$(document).ready(function(){
$("#lb").ejListView();
$("#lb").ejListView("showItem",2);
});
</script>{% endhighlight %}




### unCheckAllItem<span class="signature">()</span>
{:#methods:uncheckallitem}




To uncheck all the items.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call unCheckAllItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("unCheckAllItem");
});
</script>{% endhighlight %}




### unCheckItem<span class="signature">()</span>
{:#methods:uncheckitem}




To uncheck item in the given index.



Example
{:.example}


{% highlight html %}
 
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
// Call unCheckItem method.
$(document).ready(function(){
$("#lb").ejListView({enableCheckMark:true});
$("#lb").ejListView("unCheckItem",2);
});
</script>{% endhighlight %}



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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ajaxData{% endhighlight %}</td>
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


{% highlight html %}
 
//ajaxBeforeLoad event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxBeforeLoad: function (args) { //handle the event 
}
        });           
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
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


{% highlight html %}
 
//ajaxComplete event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxComplete: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
errorThrown{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the error thrown in the ajax post.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
textStatus{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the status.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the curent list item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
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


{% highlight html %}
 
//ajaxError event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxError: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
content{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ajax current content.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the curent list item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current item index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
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


{% highlight html %}
 
//ajaxSuccess event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Man of Steel" data-ej-href="load1.html" ></li>
                <li data-ej-text="World War Z" data-ej-href="load2.html" ></li>
                <li data-ej-text="Monsters University" data-ej-href="load3.html" ></li>
        </ul>
</div>
<script>
$(document).ready(function(){            
$("#lb").ejListView({enableAjax: true,
        ajaxSuccess: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
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


{% highlight html %}
 
//load event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
$(document).ready(function(){
$("#lb").ejListView({
        load: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
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


{% highlight html %}
 
//loadComplete event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
$(document).ready(function(){
$("#lb").ejListView({
        loadComplete: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
hasChild{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If the child element exist return true; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current list item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current text of item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current Index of the item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If checked return true; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
checkedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the list of checked items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
checkedItemsText{% endhighlight %}</td>
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


{% highlight html %}
 
//mouseDown event for ListView
<div id="lb">
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
$(document).ready(function(){
$("#lb").ejListView({
        mouseDown: function (args) { //handle the event 
}
        });         
});
</script>{% endhighlight %}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
hasChild{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If the child element exist return true; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current list item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current text of item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current Index of the item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">If checked return true; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
checkedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the list of checked items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
checkedItemsText{% endhighlight %}</td>
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


{% highlight html %}
 
//mouseUP event for ListView
<div id="lb" >
        <ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
                <li data-ej-text="Canvas Art"></li>
                <li data-ej-text="Black white"></li>
                <li data-ej-text="Children"></li>
                <li data-ej-text="Preschool Crafts"></li>
                <li data-ej-text="School-age Crafts"></li>
        </ul>
</div>
<script>
$(document).ready(function(){
$("#lb").ejListView({
        mouseUP: function (args) { //handle the event 
}
        });    
});
</script>{% endhighlight %}



