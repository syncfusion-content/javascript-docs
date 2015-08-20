---
layout: post
title: ejMenu
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Menu control.










$(element).ejMenu<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
// Create Menu
$("#menu").ejMenu({height: 22});        
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.menu.js


* module:ej.checkbox.js




## Members








### animationType<span class="type-signature type enum">enum</span>
{:#members:animationtype}








To enable or disable the Animation while hover or click an menu items..See <a href="global.html#AnimationType">AnimationType</a>




Default Value:
{:.param}






* ej.animation.Default








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>  
//To set animationType API value during initialization  
  //To set animationType API value 
  $("#menu").ejMenu({ height:22,animationType: ej.AnimationType.Default }); 
</script>{% endhighlight %}







### contextMenuTarget<span class="type-signature type string">string</span>
{:#members:contextmenutarget}








Specifies the target id of context menu. On right clicking the specified contextTarget element, context menu gets shown.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
     <div id="target" class="textarea">
                           HTML is written in the form of HTML elements consisting of tags enclosed in angle
                           brackets (like
                           <html>
                           ),within the web page content. HTML tags most commonly come in pairs like and ,although
                           some tags, known as empty elements, are unpaired, for example
                           <img>. The purpose of a web browser is to read HTML documents and compose them into
                           visible or audible web pages. The browser does not display the HTML tags, but uses
                           the tags to interpret the content of the page.
                       </div>
                       <ul id="contextMenu">
                           <li><a>Cut</a></li> 
                           <li><a>Copy</a></li> 
                           <li><a>Paste</a></li> 
                      <li class="separator"></li> 
                           <li><a>Comments</a></li>
                           <li><a>Links</a></li>
                           <li><a>Clear Formatting</a></li>  
                       </ul>           
<script>
//To set contextMenuTarget API value during initialization  
        //To set contextMenuTarget API value 
        $("#contextMenu").ejMenu({menuType:ej.MenuType.ContextMenu, height:22,contextMenuTarget:"#target"});  
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class to Menu to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
//To Set the CSS class during initialization.                   
        $("#menu").ejMenu({ height:22, cssClass:'gradient-lime ' });            
</script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Gets or sets a value that indicates whether to enable or disable the animation effect.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set enableAnimation API value during initialization  
  //To set enableAnimation API value 
  $("#menu").ejMenu({ height:22,enableAnimation: true });
</script>{% endhighlight %}







### enableCenterAlign<span class="type-signature type boolean">boolean</span>
{:#members:enablecenteralign}








Specifies the root menu items to be aligned center in horizontal menu.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set enableCenterAlign API value during initialization  
        //To set enableCenterAlign API value 
        $("#menu").ejMenu({ height:22,enableCenterAlign: true });
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








Enable / Disable the Menu control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set enabled API value during initialization  
        //To set enabled API value 
        $("#menu").ejMenu({ height:22,enabled: true });
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Specifies the menu items to be displayed in right to left direction.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set rtl API value during initialization  
        //To set rtl API value 
        $("#menu").ejMenu({ height:22,enableRTL: true });
</script>{% endhighlight %}







### enableSeparator<span class="type-signature type boolean">boolean</span>
{:#members:enableseparator}








/** When this property sets to false, the menu list is displayed without any separators.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set enableSeparator API value during initialization  
        //To set enableSeparator API value 
        $("#menu").ejMenu({ height:22,enableSeparator: true });
</script>{% endhighlight %}







### excludeTarget<span class="type-signature type string">string</span>
{:#members:excludetarget}








Specifies the target which needs to be excluded. i.e., The context menu will not be displayed in those specified targets.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
     <div id="target" class="textarea">
                           HTML is written in the form of HTML elements consisting of tags enclosed in angle
                           brackets (like
                           <html>
                           ),within the web page content. HTML tags most commonly come in pairs like and ,although
                           some tags, known as empty elements, are unpaired, for example
                           <img>. The purpose of a web browser is to read HTML documents and compose them into
                           visible or audible web pages. The browser does not display the HTML tags, but uses
                           the tags to interpret the content of the page.
        <div class="inner"> 
                       Context Menu will not be displayed here !!
                       </div>                     
                       </div>
                       <ul id="contextMenu">
                           <li><a>Cut</a></li> 
                           <li><a>Copy</a></li> 
                           <li><a>Paste</a></li> 
                      <li class="separator"></li> 
                           <li><a>Comments</a></li>
                           <li><a>Links</a></li>
                           <li><a>Clear Formatting</a></li>  
                       </ul>           
<script> 
//To set excludeTarget API value during initialization  
//To set excludeTarget API value 
$("#contextMenu").ejMenu({ menuType:ej.MenuType.ContextMenu,height:22,contextMenuTarget:"#target",excludeTarget: ".inner" });
</script>{% endhighlight %}







### fields<span class="type-signature type object">Object</span>
{:#members:fields}








Fields used to bind the data source and it includes following field members to make databind easier.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<ul id="menu">
<script> 
//To set fields API value during initialization  
        //To set fields API value 
              $("#menu").ejMenu({ height:22,
               fields: { dataSource: window.menu, id: "id", parentId: "parentId", text: "text", spriteCssClass: "sprite" }
          });
</script> {% endhighlight %}







### fields.child<span class="type-signature type object">Object</span>
{:#members:fields-child}








It receives the child data for the inner level.











### fields.dataSource<span class="type-signature type object">Object</span>
{:#members:fields-datasource}








datasource receives Essential DataManager object and JSON object.











### fields.htmlAttribute<span class="type-signature type string">string</span>
{:#members:fields-htmlattribute}








Specifies the html attributes to &ldquo;li&rdquo; item list.











### fields.id<span class="type-signature type string">string</span>
{:#members:fields-id}








Specifies the id to menu items list











### fields.imageAttribute<span class="type-signature type string">string</span>
{:#members:fields-imageattribute}








Specifies the image attribute to &ldquo;img&rdquo; tag inside items list.











### fields.imageUrl<span class="type-signature type string">string</span>
{:#members:fields-imageurl}








Specifies the image URL to &ldquo;img&rdquo; tag inside item list.











### fields.linkAttribute<span class="type-signature type string">string</span>
{:#members:fields-linkattribute}








Adds custom attributes like "target" to the anchor tag of the menu items.











### fields.parentId<span class="type-signature type string">string</span>
{:#members:fields-parentid}








Specifies the parent id of the table.











### fields.query<span class="type-signature type object">Object</span>
{:#members:fields-query}








It receives query to retrieve data from the table (query is same as SQL).











### fields.spriteCssClass<span class="type-signature type string">string</span>
{:#members:fields-spritecssclass}








Specifies the sprite CSS class to &ldquo;li&rdquo; item list











### fields.tableName<span class="type-signature type string">string</span>
{:#members:fields-tablename}








It receives table name to execute query on the corresponding table











### fields.text<span class="type-signature type string">string</span>
{:#members:fields-text}








Specifies the text of menu items list.











### fields.url<span class="type-signature type string">string</span>
{:#members:fields-url}








Specifies the url to the anchor tag in menu item list.











### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}








Specifies the height of the root menu.




Default Value:
{:.param}






* "auto"








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
//To set height API value during initialization  
  $("#menu").ejMenu({ height: 22 }); 
</script> {% endhighlight %}







### menuType<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>
{:#members:menutype}








Specifies the type of the menu. Essential JavaScript Menu consists of two type of menu, they are Normal Menu and Context Menu both Normal and Context Menu mode.See <a href="global.html#MenuType">MenuType</a>




Default Value:
{:.param}






* ej.menuType.NormalMenu








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>  
//To set menuType API value during initialization  
  //To set menuType API value 
  $("#menu").ejMenu({ height:22,menuType: "normalmenu" });
</script> {% endhighlight %}







### openOnClick<span class="type-signature type boolean">boolean</span>
{:#members:openonclick}








Specifies the sub menu items to be show or open only on click.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set openOnClick API value during initialization  
        //To set openOnClick API value 
        $("#menu").ejMenu({ height:22,openOnClick: true });
</script>{% endhighlight %}







### orientation<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>
{:#members:orientation}








Specifies the orientation of normal menu. Normal menu can rendered in horizontal or vertical direction by using this API. See <a href="global.html#Direction">Direction</a>




Default Value:
{:.param}






* ej.orientation.Horizontal








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>  
//To set orientation API value during initialization  
  //To set orientation API value 
  $("#menu").ejMenu({ height:22,orientation: ej.Orientation.Horizontal });
</script>{% endhighlight %}







### showRooltLevelArrows<span class="type-signature type boolean">boolean</span>
{:#members:showrooltlevelarrows}








Specifies the main menu items arrows only to be shown if it contains child items.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set showRooltLevelArrows API value during initialization  
        //To set showRooltLevelArrows API value 
        $("#menu").ejMenu({ height:22,showRooltLevelArrows: true });
</script>{% endhighlight %}







### showSubLevelArrows<span class="type-signature type boolean">boolean</span>
{:#members:showsublevelarrows}








Specifies the sub menu items arrows only to be shown if it contains child items.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set showSubLevelArrows API value during initialization  
        //To set showSubLevelArrows API value 
        $("#menu").ejMenu({ height:22,showSubLevelArrows: true });
</script>{% endhighlight %}







### subMenuDirection<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>
{:#members:submenudirection}








Specifies the sub menu popup direction.See <a href="global.html#Direction">Direction</a>




Default Value:
{:.param}






* ej.direction.Right








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set subMenuDirection API value during initialization  
        //To set subMenuDirection API value 
        $("#menu").ejMenu({ height:22,subMenuDirection: ej.Direction.Right });
</script>{% endhighlight %}







### titleText<span class="type-signature type string">string</span>
{:#members:titletext}








Specifies the title to responsive menu.




Default Value:
{:.param}






* "Menu"








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
//To set titleText API value during initialization  
        //To set titleText API value 
        $("#menu").ejMenu({ height:22,titleText: "Menu" });
</script>{% endhighlight %}







### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}








Specifies the width of the main menu.




Default Value:
{:.param}






* auto








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>  
//To set width API value during initialization  
  //To set width API value 
  $("#menu").ejMenu({ width: "800px",height:"30px" });  
</script>{% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








Disables the Menu control.





Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu control
        menuObj.disable();
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To disable Menu control
$("#menu").ejMenu("disable");
</script>{% endhighlight %}







### disableItem<span class="signature">(itemtext)</span>
{:#methods:disableitem}








Specifies the Menu Item to be disabled by using the Menu Item Text.

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
itemtext{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specifies the Menu Item Text to be disabled.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu item using item text
        menuObj.disableItem("Home");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To disable Menu item using item text
$("#menu").ejMenu("disableItem","Home");
</script>{% endhighlight %}







### disableItembyID<span class="signature">(itemid)</span>
{:#methods:disableitembyid}








Specifies the Menu Item to be disabled by using the Menu Item Id.

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
itemid{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">number</span></td>
<td class="description last">Specifies the Menu Item id to be disabled</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu item using item id
        menuObj.disableItemByID("More");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To disable Menu item using item id
$("#menu").ejMenu("disableItemByID","More");
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








Enables the Menu control.





Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu control
        menuObj.enable();
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22}); 
//To enable Menu control
$("#menu").ejMenu("enable");
</script>{% endhighlight %}







### enableItem<span class="signature">(itemtext)</span>
{:#methods:enableitem}








Specifies the Menu Item to be enabled by using the Menu Item Text.

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
itemtext{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specifies the Menu Item Text to be enabled.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu item using item text
menuObj.disableItem("Home");
menuObj.disableItem("Search Jobs");
        menuObj.enableItem("Search Jobs");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22}); 
//To enable Menu item using item text
$("#menu").ejMenu("disableItem","Home");
$("#menu").ejMenu("disableItem","Search Jobs");
$("#menu").ejMenu("enableItem","Search Jobs");
</script>{% endhighlight %}







### enableItembyID<span class="signature">(itemid)</span>
{:#methods:enableitembyid}








Specifies the Menu Item to be enabled by using the Menu Item Id.

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
itemid{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">number</span></td>
<td class="description last">Specifies the Menu Item id to be enabled.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu item using item id
menuObj.disable();
        menuObj.enableItemByID("More");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To enable Menu item using item id
 $("#menu").ejMenu("disable");
$("#menu").ejMenu("enableItemByID","More");
</script>{% endhighlight %}







### hideContextMenu<span class="signature">()</span>
{:#methods:hidecontextmenu}








Hides the Context Menu control.





Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To hide context menu
        menuObj.hideContextMenu();
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To hide context menu
$("#menu").ejMenu("hideContextMenu");
</script>{% endhighlight %}







### insert<span class="signature">(item, target)</span>
{:#methods:insert}








Insert the menu item as child of target node.

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
item{% endhighlight %}</td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insert([{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insert",[{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}







### insertAfter<span class="signature">(item, target)</span>
{:#methods:insertafter}








Insert the menu item after the target node.

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
item{% endhighlight %}</td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insertAfter([{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insertAfter",[{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}







### insertBefore<span class="signature">(item, target)</span>
{:#methods:insertbefore}








Insert the menu item before the target node.

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
item{% endhighlight %}</td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insertBefore([{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insertBefore",[{
         id:"More",
       text:"More"
                }],"#Home");
</script>{% endhighlight %}







### remove<span class="signature">(target)</span>
{:#methods:remove}








Remove Menu item.

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
target{% endhighlight %}</td>
<td class="type"><span class="param-type">ArrayObject</span> | <span class="param-type">ArrayString</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
var menuObj = $("#menu").data("ejMenu");
//To remove menu item 
menuObj.remove(["#Home"]);
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To remove menu item 
$("#menu").ejMenu("remove",["#Home"]);
</script>{% endhighlight %}







### showContextMenu<span class="signature">(locationX, locationY, targetElement, event)</span>
{:#methods:showcontextmenu}








Shows the Context Menu .

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
locationX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">x co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
locationY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">y co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">target element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To show context menu
        menuObj.ShowContextMenu();
</script>{% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>
$("#menu").ejMenu({height:22,}); 
//To show context menu
$("#menu").ejMenu("ShowContextMenu");
</script>{% endhighlight %}





## Events








### beforeContextOpen
{:#events:beforecontextopen}








Fires before context menu gets open.

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
<td class="description last">Event parameters from context menu
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
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //before context menu open event for menu
 $("#menu").ejMenu({height:22,
 beforeOpen: function (args) {}
 });   
</script>{% endhighlight %}







### click
{:#events:click}








Fires when mouse click on menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItem{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the selected item</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //click event for menu
 $("#menu").ejMenu({height:22,
 click: function (args){}
 });   
</script>{% endhighlight %}







### contextClose
{:#events:contextclose}








Fire when context menu on close.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //context menu close event for menu
 $("#menu").ejMenu({height:22,
 close: function (args) {}
 });   
</script>{% endhighlight %}







### contextOpen
{:#events:contextopen}








Fires when context menu on open.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //context menu open event for menu
 $("#menu").ejMenu({height:22,
 open: function (args) {}
 });   
</script>{% endhighlight %}







### create
{:#events:create}








Fires to create menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //Create event for menu
 $("#menu").ejMenu({height:22,
 create: function (args){}
 });   
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires to destroy menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //Destroy event for menu
 $("#menu").ejMenu({height:22,
 destroy: function (args){}
 }); 
</script>  {% endhighlight %}







### keydown
{:#events:keydown}








Fires when key down on menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
menuText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
 //keydown event for menu
 $("#menu").ejMenu({height:22,
 keydown: function (args){}
 });  
</script> {% endhighlight %}







### mouseout
{:#events:mouseout}








Fires when mouse out from menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
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
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script>  
 //mouse out event for menu
 $("#menu").ejMenu({height:22,
 mouseout: function (args) {}
 });   
</script>{% endhighlight %}







### mouseover
{:#events:mouseover}








Fires when mouse over the Menu items.

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
<td class="description last">Event parameters from menu
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
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
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
 
<ul id="menu">
<li id="Home"><a>Home</a></li>
<li><a>Search Jobs</a>
<ul>
<li><a>Advanced Search</a></li>
<li><a>Jobs by Company</a></li>
<li><a>Jobs by Category</a></li>
<li><a>Jobs by Location</a></li>
<li><a>Jobs by Skills</a></li>
<li><a>Jobs by Designation</a></li>
</ul>
</li>
<li id="Post Resume"><a>Post Resume</a></li>
<li id="Job Seeker"><a>JobSeeker Login</a></li>
<li id="Fast Forward"><a>Fast Forward</a>
<ul>
<li><a>Resume writing</a></li>
<li><a>Certification</a></li>
<li><a>Resume Spotlight</a></li>
<li><a>Jobs4u</a></li>
</ul>
</li>
<li id="More"><a>More</a>
<ul>
<li><a>Mobile</a></li>
<li><a>Pay check</a></li>
<li><a>Blog</a></li>
</ul>
</li>
</ul>

 
<script> 
  //mouse over event for menu
 $("#menu").ejMenu({height:22,
 mouseover: function (args) {}
 });   
</script>{% endhighlight %}




