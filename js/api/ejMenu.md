---
layout: post
title: Properties, Methods and Events of ejMenu Widget
description: API reference for ejMenu
documentation: API
platform: js
keywords: Menu, ejMenu, syncfusion, Menu api  
---

# ejMenu

The Menu control supports displaying a Menu created from list items. The Menu is based on a hierarchy of UL and LI elements where the list items are rendered as sub-menu items.

#### Syntax

{% highlight javascript %}

$(element).ejMenu()

{% endhighlight %}

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
{% endhighlight %}

{% highlight javascript %}

    $("#menu").ejMenu();

{% endhighlight %}


#### Requires


* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.menu.js


* module:ej.checkbox.js


## Members

### animationType `enum`
{:#members:animationtype}

<ts name="ej.AnimationType" />

To enable or disable the Animation while hover or click an menu items.See <a href="global.html#AnimationType">AnimationType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">Used to set AnimationType as Default</td>
</tr>
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set AnimationType as None</td>
</tr>
</tbody>
</table>


#### Default Value

* ej.AnimationType.Default

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
  
      //To set animationType API value during initialization   
      $("#menu").ejMenu({ animationType: ej.AnimationType.Default }); 

{% endhighlight %}

### contextMenuTarget `string`
{:#members:contextmenutarget}

Specifies the target id of context menu. On right clicking the specified contextTarget element, context menu gets shown.

#### Default Value

* null

#### Example

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
 
{% endhighlight %}

{% highlight javascript %}   

        //To set contextMenuTarget API value during initialization  

        $("#contextMenu").ejMenu({ menuType: ej.MenuType.ContextMenu, contextMenuTarget: "#target" });

{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Specify the CSS class to achieve custom theme.

#### Default Value

* ""

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 
 
     //To Set the CSS class during initialization.    

     $("#menu").ejMenu({  cssClass: 'gradient-lime ' });

{% endhighlight %}


### enableAnimation `boolean`
{:#members:enableanimation}

To enable or disable the Animation effect while hover or click an menu items.

#### Default Value

* true

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul> 

{% endhighlight %}

{% highlight javascript %}
 
      //To set enableAnimation API value during initialization 
      
      $("#menu").ejMenu({ enableAnimation: true });

{% endhighlight %}


### enableCenterAlign `boolean`
{:#members:enablecenteralign}

Specifies the root menu items to be aligned center in horizontal menu.


#### Default Value

* false

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
    
{% endhighlight %}

{% highlight javascript %}
 
      //To set enableCenterAlign API value during initialization  

      $("#menu").ejMenu({ enableCenterAlign: true });

{% endhighlight %}


### enabled `boolean`
{:#members:enabled}


Enable / Disable the Menu control.

#### Default Value

* true

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}

     //To set enabled API value during initialization  
 
     $("#menu").ejMenu({ enabled: true });

{% endhighlight %}


### enableRTL `boolean`
{:#members:enablertl}

Specifies the menu items to be displayed in right to left direction.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

 
{% endhighlight %}

{% highlight javascript %}

     //To set rtl API value during initialization  

     $("#menu").ejMenu({ enableRTL: true });

{% endhighlight %}


### enableSeparator `boolean`
{:#members:enableseparator}

 When this property sets to false, the menu items is displayed without any separators.

#### Default Value

* true

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
 
        //To set enableSeparator API value during initialization  

        $("#menu").ejMenu({ enableSeparator: true });

{% endhighlight %}


### excludeTarget `string`
{:#members:excludetarget}

Specifies the target which needs to be excluded. i.e., The context menu will not be displayed in those specified targets.

#### Default Value

* null

#### Example

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
         
{% endhighlight %}

{% highlight javascript %}                  
 
    //To set excludeTarget API value during initialization  

    $("#contextMenu").ejMenu({ menuType:ej.MenuType.ContextMenu,contextMenuTarget:"#target",excludeTarget: ".inner" });

{% endhighlight %}


### fields `object`
{:#members:fields}

Fields used to bind the data source and it includes following field members to make data bind easier.

#### Default Value

* null

#### Example

{% highlight html %}

    <ul id="menu"/>
        
{% endhighlight %}

{% highlight javascript %}        
 
        //To set fields API value during initialization  

              $("#menu").ejMenu({ 
               fields: { dataSource: window.menu, id: "id", parentId: "parentId", text: "text", spriteCssClass: "sprite" }
          });


{% endhighlight %}

### fields.child `object`
{:#members:fields-child}

It receives the child data for the inner level.


### fields.dataSource `object`
{:#members:fields-datasource}

It receives datasource as Essential DataManager object and JSON object.

### fields.htmlAttribute `string`
{:#members:fields-htmlattribute}


Specifies the HTML attributes to &ldquo;LI&rdquo; item list.


### fields.id `string`
{:#members:fields-id}

Specifies the id to menu items list

### fields.imageAttribute `string`
{:#members:fields-imageattribute}

Specifies the image attribute to &ldquo;img&rdquo; tag inside items list.


### fields.imageUrl `string`
{:#members:fields-imageurl}


Specifies the image URL to &ldquo;img&rdquo; tag inside item list.


### fields.linkAttribute `string`
{:#members:fields-linkattribute}


Adds custom attributes like "target" to the anchor tag of the menu items.



### fields.parentId `string`
{:#members:fields-parentid}


Specifies the parent id of the table.


### fields.query `object`
{:#members:fields-query}


It receives query to retrieve data from the table (query is same as SQL).


### fields.spriteCssClass `string`
{:#members:fields-spritecssclass}

Specifies the sprite CSS class to &ldquo;LI&rdquo; item list.


### fields.tableName `string`
{:#members:fields-tablename}


It receives table name to execute query on the corresponding table.


### fields.text `string`
{:#members:fields-text}

Specifies the text of menu items list.


### fields.url `string`
{:#members:fields-url}

Specifies the URL to the anchor tag in menu item list.

### height `string|number`
{:#members:height}


Specifies the height of the root menu.

#### Default Value

* "auto"

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
    
{% endhighlight %}

{% highlight javascript %}
 
        //To set height API value during initialization  
        $("#menu").ejMenu({ height: 22 }); 

{% endhighlight %}


### htmlAttributes `object`

{:#members:htmlattributes}

Specifies the list of HTML attributes to be added to menu control.

#### Default Value

* {}

#### Example

{% highlight html %}
 
        <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
  
        //To set htmlAttributes API value during initialization  

        $("#menu").ejMenu({ htmlAttributes:{"aria-label":"menu"} });

{% endhighlight %}

### menuType `string|enum`
{:#members:menutype}

<ts name="ej.MenuType" />

Specifies the type of the menu. Essential JavaScript Menu consists of two type of menu, they are Normal Menu and Context Menu mode.See <a href="global.html#MenuType">MenuType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
ContextMenu</td>
<td class="type">string</td>
<td class="default">contextmenu</td>
<td class="description">Used to set MenuType as ContextMenu</td>
</tr>
<tr>
<td class="name">
NormalMenu</td>
<td class="type">string</td>
<td class="default">normal menu</td>
<td class="description">Used to set MenuType as NormalMenu</td>
</tr>
</tbody>
</table>


#### Default Value

* ej.MenuType.NormalMenu

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
  
        //To set menuType API value during initialization  

        $("#menu").ejMenu({ menuType: "normalmenu" });

{% endhighlight %}


### openOnClick `boolean`
{:#members:openonclick}



Specifies the sub menu items to be show or open only on click.


#### Default Value



* false



#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
 
       //To set openOnClick API value during initialization  
 
        $("#menu").ejMenu({ openOnClick: true });


{% endhighlight %}


### orientation `string|enum`
{:#members:orientation}

<ts ref="ej.Orientation" />


Specifies the orientation of normal menu. Normal menu can rendered in horizontal or vertical direction by using this API. See <a href="global.html#Orientation">Orientation</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Used to set Orientation as Horizontal</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Used to set Orientation as Vertical</td>
</tr>
</tbody>
</table>


#### Default Value

* ej.Orientation.Horizontal

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
  
        //To set orientation API value during initialization  
 
         $("#menu").ejMenu({ orientation: ej.Orientation.Horizontal });

{% endhighlight %}


### showRootLevelArrows `boolean`
{:#members:showRootLevelArrows}


Specifies the main menu items arrows only to be shown if it contains child items.


#### Default Value


* true


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}

        //To set showRootLevelArrows API value during initialization  
        
        $("#menu").ejMenu({ showRootLevelArrows: true });

{% endhighlight %}



### showSubLevelArrows `boolean`
{:#members:showsublevelarrows}


Specifies the sub menu items arrows only to be shown if it contains child items.


#### Default Value

* true

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}
 
        //To set showSubLevelArrows API value during initialization  
 
        $("#menu").ejMenu({ showSubLevelArrows: true });

{% endhighlight %}


### subMenuDirection `string|enum`
{:#members:submenudirection}

<ts name="ej.Direction" />


Specifies position of pull down submenu that will appear on mouse over.See <a href="global.html#Direction">Direction</a>

<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to set Direction as Left</td>
</tr>
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set Direction as None</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to set Direction as Right</td>
</tr>
</tbody>
</table>


#### Default Value


* ej.Direction.Right



#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
    
{% endhighlight %}

{% highlight javascript %}
 

        //To set subMenuDirection API value during initialization  

        $("#menu").ejMenu({ subMenuDirection: ej.Direction.Right });
        
{% endhighlight %}



### titleText `string`
{:#members:titletext}


Specifies the title to responsive menu.



#### Default Value


* "Menu"



#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}

        //To set titleText API value during initialization  

        $("#menu").ejMenu({ titleText: "Menu" });
        
{% endhighlight %}


### width `string|number`
{:#members:width}


Specifies the width of the main menu.

#### Default Value

* auto

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 
  
        //To set width API value during initialization  
 
        $("#menu").ejMenu({ width: "800px",height:"30px" });
          
{% endhighlight %}


## Methods


### disable()
{:#methods:disable}


Disables the Menu control.


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

 
{% endhighlight %}

{% highlight javascript %}

    $("#menu").ejMenu();
    
    //initialize the menu object
    var menuObj = $("#menu").data("ejMenu");
    
    //To disable Menu control
    menuObj.disable();
    
{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 

    $("#menu").ejMenu();
    
    //To disable Menu control
    $("#menu").ejMenu("disable");

{% endhighlight %}


### disableItem(itemtext)
{:#methods:disableitem}


Specifies the Menu Item to be disabled by using the Menu Item Text.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
itemtext</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Specifies the Menu Item Text to be disabled.</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To disable Menu item using item text
        menuObj.disableItem("Home");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To disable Menu item using item text
        $("#menu").ejMenu("disableItem", "Home");

{% endhighlight %}


### disableItemByID(itemid)
{:#methods:disableitembyid}



Specifies the Menu Item to be disabled by using the Menu Item Id.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
itemid</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Specifies the Menu Item id to be disabled</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To disable Menu item using item id
        menuObj.disableItemByID("More");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
{% endhighlight %}

{% highlight javascript %} 
 
        $("#menu").ejMenu();

        //To disable Menu item using item id
        $("#menu").ejMenu("disableItemByID", "More");

{% endhighlight %}



### enable()
{:#methods:enable}


Enables the Menu control.


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To enable Menu control
        menuObj.enable();

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //To enable Menu control
        $("#menu").ejMenu("enable");

{% endhighlight %}



### enableItem(itemtext)
{:#methods:enableitem}



Specifies the Menu Item to be enabled by using the Menu Item Text.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
itemtext</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Specifies the Menu Item Text to be enabled.</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To enable Menu item using item text
        menuObj.enableItem("Search Jobs");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
{% endhighlight %}

{% highlight javascript %}     

        $("#menu").ejMenu();

        //To enable Menu item using item text
        $("#menu").ejMenu("enableItem", "Search Jobs");

{% endhighlight %}


### enableItemByID(itemid)
{:#methods:enableitembyid}



Specifies the Menu Item to be enabled by using the Menu Item Id.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
itemid</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Specifies the Menu Item id to be enabled.</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To enable Menu item using item id
        menuObj.enableItemByID("More");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To enable Menu item using item id
        $("#menu").ejMenu("enableItemByID", "More");

{% endhighlight %}



### hide()
{:#methods:hide}

Hides the Context Menu control.

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To hide context menu
        menuObj.hide();

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //To hide context menu
        $("#menu").ejMenu("hide");

{% endhighlight %}


### hideItems([itemID])
{:#methods:hideItems}

Hides the specific items in Menu control.

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
            <ul>
                <li id="search"><a>Advanced Search</a></li>
                <li id="company"><a>Jobs by Company</a></li>
                <li><a>Jobs by Category</a></li>
                <li><a>Jobs by Location</a></li>
                <li><a>Jobs by Skills</a></li>
                <li><a>Jobs by Designation</a></li>
            </ul>
        </li>
        <li id="Post Resume"><a>Post Resume</a></li>
        <li id="Job Seeker"><a>JobSeeker Login</a></li>
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To hide the menu items
        menuObj.hideItems(["#search","#company"]);

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
            <ul>
                <li id="search"><a>Advanced Search</a></li>
                <li id="company"><a>Jobs by Company</a></li>
                <li><a>Jobs by Category</a></li>
                <li><a>Jobs by Location</a></li>
                <li><a>Jobs by Skills</a></li>
                <li><a>Jobs by Designation</a></li>
            </ul>
        </li>
        <li id="Post Resume"><a>Post Resume</a></li>
        <li id="Job Seeker"><a>JobSeeker Login</a></li>
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //To hide the menu items
        $("#menu").ejMenu("hideItems","#search");

{% endhighlight %}

### insert(item, target)
{:#methods:insert}



Insert the menu item as child of target node.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
item</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Information about Menu item.</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">string|Object</span></td>
<td class="description">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

    $("#menu").ejMenu();
    
    //initialize the menu object
    var menuObj = $("#menu").data("ejMenu");
    
    //To insert menu item
    menuObj.insert([{
        id: "More",
        text: "More"
    }], "#Home");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To insert menu item 
        $("#menu").ejMenu("insert", [{
            id: "More",
            text: "More"
        }], "#Home");

{% endhighlight %}


### insertAfter(item, target)
{:#methods:insertafter}



Insert the menu item after the target node.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
item</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Information about Menu item.</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">string|Object</span></td>
<td class="description">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();
        
        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        
        //To insert menu item 
        menuObj.insertAfter([{
            id: "More",
            text: "More"
        }], "#Home");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To insert menu item 
        $("#menu").ejMenu("insertAfter", [{
            id: "More",
            text: "More"
        }], "#Home");

{% endhighlight %}


### insertBefore(item, target)
{:#methods:insertbefore}


Insert the menu item before the target node.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
item</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Information about Menu item.</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">string|Object</span></td>
<td class="description">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To insert menu item 
        menuObj.insertBefore([{
            id: "More",
            text: "More"
        }], "#Home");

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To insert menu item 
        $("#menu").ejMenu("insertBefore", [{
            id: "More",
            text: "More"
        }], "#Home");

{% endhighlight %}


### remove(target)
{:#methods:remove}


Remove Menu item.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object|array</span></td>
<td class="description">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To remove menu item 
        menuObj.remove(["#Home"]);

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To remove menu item 
        $("#menu").ejMenu("remove", ["#Home"]);

{% endhighlight %}


### show(locationX, locationY, targetElement, event)
{:#methods:show}


To show the Menu control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
locationX</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">x co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name">
locationY</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">y co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name">
targetElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">target element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To show menu
        menuObj.show();

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        $("#menu").ejMenu();

        //To show menu
        $("#menu").ejMenu("show");

{% endhighlight %}

### showItems([itemID])
{:#methods:showItems}

Show the specific items in Menu control.

#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
            <ul>
                <li id="search"><a>Advanced Search</a></li>
                <li id="company"><a>Jobs by Company</a></li>
                <li><a>Jobs by Category</a></li>
                <li><a>Jobs by Location</a></li>
                <li><a>Jobs by Skills</a></li>
                <li><a>Jobs by Designation</a></li>
            </ul>
        </li>
        <li id="Post Resume"><a>Post Resume</a></li>
        <li id="Job Seeker"><a>JobSeeker Login</a></li>
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //initialize the menu object
        var menuObj = $("#menu").data("ejMenu");

        //To show the menu items
        menuObj.showItems(["#search","#company"]);

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
            <ul>
                <li id="search"><a>Advanced Search</a></li>
                <li id="company"><a>Jobs by Company</a></li>
                <li><a>Jobs by Category</a></li>
                <li><a>Jobs by Location</a></li>
                <li><a>Jobs by Skills</a></li>
                <li><a>Jobs by Designation</a></li>
            </ul>
        </li>
        <li id="Post Resume"><a>Post Resume</a></li>
        <li id="Job Seeker"><a>JobSeeker Login</a></li>
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>
 
{% endhighlight %}

{% highlight javascript %} 

        $("#menu").ejMenu();

        //To show the menu items.
        $("#menu").ejMenu("showItems",#search");

{% endhighlight %}

## Events


### beforeOpen
{:#events:beforeopen}


Fires before context menu gets open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from context menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  

        //before context menu open event for menu
        $("#menu").ejMenu({
            beforeOpen: function (args) { }
        }); 
  
{% endhighlight %}

### click
{:#events:click}


Fires when mouse click on menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event</td>
</tr>
<tr>
<td class="name">
selectedItem</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the selected item</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //click event for menu
        $("#menu").ejMenu({
            click: function (args) { }
        });
  
{% endhighlight %}


### close
{:#events:close}


Fire when context menu on close.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //context menu close event for menu
        $("#menu").ejMenu({
            close: function (args) { }
        });
  
{% endhighlight %}


### open
{:#events:open}



Fires when context menu on open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //context menu open event for menu
        $("#menu").ejMenu({
            open: function (args) { }
        });
  
{% endhighlight %}


### create
{:#events:create}


Fires to create menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %} 
 
        //Create event for menu
        $("#menu").ejMenu({
            create: function (args) { }
        });
   
{% endhighlight %}

### destroy
{:#events:destroy}

Fires to destroy menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //Destroy event for menu
        $("#menu").ejMenu({
            destroy: function (args) { }
        });

{% endhighlight %}


### keydown
{:#events:keydown}


Fires when key down on menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
menuText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //keydown event for menu
        $("#menu").ejMenu({
            keydown: function (args) { }
        });
 
 {% endhighlight %}


### mouseout
{:#events:mouseout}


Fires when mouse out from menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}

    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
  
        //mouse out event for menu
        $("#menu").ejMenu({
            mouseout: function (args) { }
        });
 
{% endhighlight %}


### mouseover
{:#events:mouseover}


Fires when mouse over the Menu items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from menu
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Menu.Model"/><span class="param-type">object</span></td>
<td class="description">returns the menu model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns clicked menu item text</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
    <ul id="menu">
        <li id="Home"><a>Home</a></li>
        <li>
            <a>Search Jobs</a>
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
        <li id="Fast Forward">
            <a>Fast Forward</a>
            <ul>
                <li><a>Resume writing</a></li>
                <li><a>Certification</a></li>
                <li><a>Resume Spotlight</a></li>
                <li><a>Jobs4u</a></li>
            </ul>
        </li>
        <li id="More">
            <a>More</a>
            <ul>
                <li><a>Mobile</a></li>
                <li><a>Pay check</a></li>
                <li><a>Blog</a></li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight javascript %}  
 
        //mouse over event for menu
        $("#menu").ejMenu({
            mouseover: function (args) { }
        }); 

{% endhighlight %}




