---
layout: post
title: ejMenu
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Menu control.










#### $(element).ejMenu<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
// Create Menu
$("#menu").ejMenu({height: 22});        
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.menu.js


* module:ej.checkbox.js




### Members








#### animationType<span class="type-signature type enum">enum</span>








To enable or disable the Animation while hover or click an menu items..See <a href="global.html#AnimationType">AnimationType</a>




Default Value:
{:.param}






* ej.animation.Default








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;  
//To set animationType API value during initialization  
  //To set animationType API value 
  $("#menu").ejMenu({ height:22,animationType: ej.AnimationType.Default }); 
&lt;/script&gt;</code>
</pre>






#### contextMenuTarget<span class="type-signature type string">string</span>








Specifies the target id of context menu. On right clicking the specified contextTarget element, context menu gets shown.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code>     &lt;div id="target" class="textarea"&gt;
                           HTML is written in the form of HTML elements consisting of tags enclosed in angle
                           brackets (like
                           &lt;html&gt;
                           ),within the web page content. HTML tags most commonly come in pairs like and ,although
                           some tags, known as empty elements, are unpaired, for example
                           &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into
                           visible or audible web pages. The browser does not display the HTML tags, but uses
                           the tags to interpret the content of the page.
                       &lt;/div&gt;
                       &lt;ul id="contextMenu"&gt;
                           &lt;li&gt;&lt;a&gt;Cut&lt;/a&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Copy&lt;/a&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Paste&lt;/a&gt;&lt;/li&gt; 
                      &lt;li class="separator"&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Comments&lt;/a&gt;&lt;/li&gt;
                           &lt;li&gt;&lt;a&gt;Links&lt;/a&gt;&lt;/li&gt;
                           &lt;li&gt;&lt;a&gt;Clear Formatting&lt;/a&gt;&lt;/li&gt;  
                       &lt;/ul&gt;           
&lt;script&gt;
//To set contextMenuTarget API value during initialization  
        //To set contextMenuTarget API value 
        $("#contextMenu").ejMenu({menuType:ej.MenuType.ContextMenu, height:22,contextMenuTarget:"#target"});  
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Specify the CSS class to Menu to achieve custom theme.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
//To Set the CSS class during initialization.                   
        $("#menu").ejMenu({ height:22, cssClass:'gradient-lime ' });            
&lt;/script&gt;</code>
</pre>






#### enableAnimation<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable or disable the animation effect.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set enableAnimation API value during initialization  
  //To set enableAnimation API value 
  $("#menu").ejMenu({ height:22,enableAnimation: true });
&lt;/script&gt;</code>
</pre>






#### enableCenterAlign<span class="type-signature type boolean">boolean</span>








Specifies the root menu items to be aligned center in horizontal menu.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set enableCenterAlign API value during initialization  
        //To set enableCenterAlign API value 
        $("#menu").ejMenu({ height:22,enableCenterAlign: true });
&lt;/script&gt;</code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








Enable / Disable the Menu control.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set enabled API value during initialization  
        //To set enabled API value 
        $("#menu").ejMenu({ height:22,enabled: true });
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Specifies the menu items to be displayed in right to left direction.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set rtl API value during initialization  
        //To set rtl API value 
        $("#menu").ejMenu({ height:22,enableRTL: true });
&lt;/script&gt;</code>
</pre>






#### enableSeparator<span class="type-signature type boolean">boolean</span>








/** When this property sets to false, the menu list is displayed without any separators.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set enableSeparator API value during initialization  
        //To set enableSeparator API value 
        $("#menu").ejMenu({ height:22,enableSeparator: true });
&lt;/script&gt;</code>
</pre>






#### excludeTarget<span class="type-signature type string">string</span>








Specifies the target which needs to be excluded. i.e., The context menu will not be displayed in those specified targets.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code>     &lt;div id="target" class="textarea"&gt;
                           HTML is written in the form of HTML elements consisting of tags enclosed in angle
                           brackets (like
                           &lt;html&gt;
                           ),within the web page content. HTML tags most commonly come in pairs like and ,although
                           some tags, known as empty elements, are unpaired, for example
                           &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into
                           visible or audible web pages. The browser does not display the HTML tags, but uses
                           the tags to interpret the content of the page.
        &lt;div class="inner"&gt; 
                       Context Menu will not be displayed here !!
                       &lt;/div&gt;                     
                       &lt;/div&gt;
                       &lt;ul id="contextMenu"&gt;
                           &lt;li&gt;&lt;a&gt;Cut&lt;/a&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Copy&lt;/a&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Paste&lt;/a&gt;&lt;/li&gt; 
                      &lt;li class="separator"&gt;&lt;/li&gt; 
                           &lt;li&gt;&lt;a&gt;Comments&lt;/a&gt;&lt;/li&gt;
                           &lt;li&gt;&lt;a&gt;Links&lt;/a&gt;&lt;/li&gt;
                           &lt;li&gt;&lt;a&gt;Clear Formatting&lt;/a&gt;&lt;/li&gt;  
                       &lt;/ul&gt;           
&lt;script&gt; 
//To set excludeTarget API value during initialization  
//To set excludeTarget API value 
$("#contextMenu").ejMenu({ menuType:ej.MenuType.ContextMenu,height:22,contextMenuTarget:"#target",excludeTarget: ".inner" });
&lt;/script&gt;</code>
</pre>






#### fields<span class="type-signature type object">Object</span>








Fields used to bind the data source and it includes following field members to make databind easier.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code>&lt;ul id="menu"&gt;
&lt;script&gt; 
//To set fields API value during initialization  
        //To set fields API value 
              $("#menu").ejMenu({ height:22,
               fields: { dataSource: window.menu, id: "id", parentId: "parentId", text: "text", spriteCssClass: "sprite" }
          });
&lt;/script&gt; </code>
</pre>






#### fields.child<span class="type-signature type object">Object</span>








It receives the child data for the inner level.











#### fields.dataSource<span class="type-signature type object">Object</span>








datasource receives Essential DataManager object and JSON object.











#### fields.htmlAttribute<span class="type-signature type string">string</span>








Specifies the html attributes to &ldquo;li&rdquo; item list.











#### fields.id<span class="type-signature type string">string</span>








Specifies the id to menu items list











#### fields.imageAttribute<span class="type-signature type string">string</span>








Specifies the image attribute to &ldquo;img&rdquo; tag inside items list.











#### fields.imageUrl<span class="type-signature type string">string</span>








Specifies the image URL to &ldquo;img&rdquo; tag inside item list.











#### fields.linkAttribute<span class="type-signature type string">string</span>








Adds custom attributes like "target" to the anchor tag of the menu items.











#### fields.parentId<span class="type-signature type string">string</span>








Specifies the parent id of the table.











#### fields.query<span class="type-signature type object">Object</span>








It receives query to retrieve data from the table (query is same as SQL).











#### fields.spriteCssClass<span class="type-signature type string">string</span>








Specifies the sprite CSS class to &ldquo;li&rdquo; item list











#### fields.tableName<span class="type-signature type string">string</span>








It receives table name to execute query on the corresponding table











#### fields.text<span class="type-signature type string">string</span>








Specifies the text of menu items list.











#### fields.url<span class="type-signature type string">string</span>








Specifies the url to the anchor tag in menu item list.











#### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>








Specifies the height of the root menu.




Default Value:
{:.param}






* "auto"








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
//To set height API value during initialization  
  $("#menu").ejMenu({ height: 22 }); 
&lt;/script&gt; </code>
</pre>






#### menuType<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>








Specifies the type of the menu. Essential JavaScript Menu consists of two type of menu, they are Normal Menu and Context Menu both Normal and Context Menu mode.See <a href="global.html#MenuType">MenuType</a>




Default Value:
{:.param}






* ej.menuType.NormalMenu








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;  
//To set menuType API value during initialization  
  //To set menuType API value 
  $("#menu").ejMenu({ height:22,menuType: "normalmenu" });
&lt;/script&gt; </code>
</pre>






#### openOnClick<span class="type-signature type boolean">boolean</span>








Specifies the sub menu items to be show or open only on click.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set openOnClick API value during initialization  
        //To set openOnClick API value 
        $("#menu").ejMenu({ height:22,openOnClick: true });
&lt;/script&gt;</code>
</pre>






#### orientation<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>








Specifies the orientation of normal menu. Normal menu can rendered in horizontal or vertical direction by using this API. See <a href="global.html#Direction">Direction</a>




Default Value:
{:.param}






* ej.orientation.Horizontal








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;  
//To set orientation API value during initialization  
  //To set orientation API value 
  $("#menu").ejMenu({ height:22,orientation: ej.Orientation.Horizontal });
&lt;/script&gt;</code>
</pre>






#### showRooltLevelArrows<span class="type-signature type boolean">boolean</span>








Specifies the main menu items arrows only to be shown if it contains child items.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set showRooltLevelArrows API value during initialization  
        //To set showRooltLevelArrows API value 
        $("#menu").ejMenu({ height:22,showRooltLevelArrows: true });
&lt;/script&gt;</code>
</pre>






#### showSubLevelArrows<span class="type-signature type boolean">boolean</span>








Specifies the sub menu items arrows only to be shown if it contains child items.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set showSubLevelArrows API value during initialization  
        //To set showSubLevelArrows API value 
        $("#menu").ejMenu({ height:22,showSubLevelArrows: true });
&lt;/script&gt;</code>
</pre>






#### subMenuDirection<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>








Specifies the sub menu popup direction.See <a href="global.html#Direction">Direction</a>




Default Value:
{:.param}






* ej.direction.Right








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set subMenuDirection API value during initialization  
        //To set subMenuDirection API value 
        $("#menu").ejMenu({ height:22,subMenuDirection: ej.Direction.Right });
&lt;/script&gt;</code>
</pre>






#### titleText<span class="type-signature type string">string</span>








Specifies the title to responsive menu.




Default Value:
{:.param}






* "Menu"








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
//To set titleText API value during initialization  
        //To set titleText API value 
        $("#menu").ejMenu({ height:22,titleText: "Menu" });
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>








Specifies the width of the main menu.




Default Value:
{:.param}






* auto








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;  
//To set width API value during initialization  
  //To set width API value 
  $("#menu").ejMenu({ width: "800px",height:"30px" });  
&lt;/script&gt;</code>
</pre>




### Methods








#### disable<span class="signature">()</span>








Disables the Menu control.





##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu control
        menuObj.disable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To disable Menu control
$("#menu").ejMenu("disable");
&lt;/script&gt;</code>
</pre>






#### disableItem<span class="signature">(itemtext)</span>








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
<td class="name"><code>itemtext</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specifies the Menu Item Text to be disabled.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu item using item text
        menuObj.disableItem("Home");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To disable Menu item using item text
$("#menu").ejMenu("disableItem","Home");
&lt;/script&gt;</code>
</pre>






#### disableItembyID<span class="signature">(itemid)</span>








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
<td class="name"><code>itemid</code></td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">number</span></td>
<td class="description last">Specifies the Menu Item id to be disabled</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To disable Menu item using item id
        menuObj.disableItemByID("More");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To disable Menu item using item id
$("#menu").ejMenu("disableItemByID","More");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








Enables the Menu control.





##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu control
        menuObj.enable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22}); 
//To enable Menu control
$("#menu").ejMenu("enable");
&lt;/script&gt;</code>
</pre>






#### enableItem<span class="signature">(itemtext)</span>








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
<td class="name"><code>itemtext</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Specifies the Menu Item Text to be enabled.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu item using item text
menuObj.disableItem("Home");
menuObj.disableItem("Search Jobs");
        menuObj.enableItem("Search Jobs");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22}); 
//To enable Menu item using item text
$("#menu").ejMenu("disableItem","Home");
$("#menu").ejMenu("disableItem","Search Jobs");
$("#menu").ejMenu("enableItem","Search Jobs");
&lt;/script&gt;</code>
</pre>






#### enableItembyID<span class="signature">(itemid)</span>








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
<td class="name"><code>itemid</code></td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">number</span></td>
<td class="description last">Specifies the Menu Item id to be enabled.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To enable Menu item using item id
menuObj.disable();
        menuObj.enableItemByID("More");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To enable Menu item using item id
 $("#menu").ejMenu("disable");
$("#menu").ejMenu("enableItemByID","More");
&lt;/script&gt;</code>
</pre>






#### hideContextMenu<span class="signature">()</span>








Hides the Context Menu control.





##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To hide context menu
        menuObj.hideContextMenu();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To hide context menu
$("#menu").ejMenu("hideContextMenu");
&lt;/script&gt;</code>
</pre>






#### insert<span class="signature">(item, target)</span>








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
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insert([{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insert",[{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>






#### insertAfter<span class="signature">(item, target)</span>








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
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insertAfter([{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insertAfter",[{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>






#### insertBefore<span class="signature">(item, target)</span>








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
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">ArrayObject</span></td>
<td class="description last">Information about Menu item.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">string</span> | <span class="param-type">Object</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To insert menu item 
        menuObj.insertBefore([{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To insert menu item 
$("#menu").ejMenu("insertBefore",[{
         id:"More",
       text:"More"
                }],"#Home");
&lt;/script&gt;</code>
</pre>






#### remove<span class="signature">(target)</span>








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
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">ArrayObject</span> | <span class="param-type">ArrayString</span></td>
<td class="description last">Selector of target node or Object of target node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
var menuObj = $("#menu").data("ejMenu");
//To remove menu item 
menuObj.remove(["#Home"]);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To remove menu item 
$("#menu").ejMenu("remove",["#Home"]);
&lt;/script&gt;</code>
</pre>






#### showContextMenu<span class="signature">(locationX, locationY, targetElement, event)</span>








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
<td class="name"><code>locationX</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">x co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name"><code>locationY</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">y co-ordinate position of context menu.</td>
</tr>
<tr>
<td class="name"><code>targetElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">target element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">name of the event</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//initialize the menu object
        var menuObj = $("#menu").data("ejMenu");
        //To show context menu
        menuObj.ShowContextMenu();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;
$("#menu").ejMenu({height:22,}); 
//To show context menu
$("#menu").ejMenu("ShowContextMenu");
&lt;/script&gt;</code>
</pre>




### Events








#### beforeContextOpen








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //before context menu open event for menu
 $("#menu").ejMenu({height:22,
 beforeOpen: function (args) {}
 });   
&lt;/script&gt;</code>
</pre>






#### click








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
</tr>
<tr>
<td class="name"><code>selectedItem</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the selected item</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //click event for menu
 $("#menu").ejMenu({height:22,
 click: function (args){}
 });   
&lt;/script&gt;</code>
</pre>






#### contextClose








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //context menu close event for menu
 $("#menu").ejMenu({height:22,
 close: function (args) {}
 });   
&lt;/script&gt;</code>
</pre>






#### contextOpen








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //context menu open event for menu
 $("#menu").ejMenu({height:22,
 open: function (args) {}
 });   
&lt;/script&gt;</code>
</pre>






#### create








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //Create event for menu
 $("#menu").ejMenu({height:22,
 create: function (args){}
 });   
&lt;/script&gt;</code>
</pre>






#### destroy








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //Destroy event for menu
 $("#menu").ejMenu({height:22,
 destroy: function (args){}
 }); 
&lt;/script&gt;  </code>
</pre>






#### keydown








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>menuText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
 //keydown event for menu
 $("#menu").ejMenu({height:22,
 keydown: function (args){}
 });  
&lt;/script&gt; </code>
</pre>






#### mouseout








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt;  
 //mouse out event for menu
 $("#menu").ejMenu({height:22,
 mouseout: function (args) {}
 });   
&lt;/script&gt;</code>
</pre>






#### mouseover








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the menu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns clicked menu item text</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="menu"&gt;
&lt;li id="Home"&gt;&lt;a&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Search Jobs&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Advanced Search&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Company&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Category&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Location&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Skills&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs by Designation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="Post Resume"&gt;&lt;a&gt;Post Resume&lt;/a&gt;&lt;/li&gt;
&lt;li id="Job Seeker"&gt;&lt;a&gt;JobSeeker Login&lt;/a&gt;&lt;/li&gt;
&lt;li id="Fast Forward"&gt;&lt;a&gt;Fast Forward&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Resume writing&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Certification&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Resume Spotlight&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Jobs4u&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li id="More"&gt;&lt;a&gt;More&lt;/a&gt;
&lt;ul&gt;
&lt;li&gt;&lt;a&gt;Mobile&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Pay check&lt;/a&gt;&lt;/li&gt;
&lt;li&gt;&lt;a&gt;Blog&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;

 
&lt;script&gt; 
  //mouse over event for menu
 $("#menu").ejMenu({height:22,
 mouseover: function (args) {}
 });   
&lt;/script&gt;</code>
</pre>



