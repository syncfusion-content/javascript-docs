---
layout: post
title: Properties, Methods and Events of ejWaitingPopup Widget
description: API reference for ejWaitingPopup
documentation: API
platform: js
keywords: WaitingPopup, ejWaitingPopup, syncfusion, WaitingPopup api 
---

# ejWaitingPopup



The WaitingPopup control for JavaScript is a visual element that provides support for displaying a pop-up indicator over a target area and preventing the end user’s interaction with the target area while loading.




#### Syntax

{% highlight javascript %}

$(element).ejWaitingPopup()

{% endhighlight %}




#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
// Simple waiting popup creation.
$("#target").ejWaitingPopup({ showOnInit: true });
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}







#### Requires





* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.waitingpopup.js




## Members








### cssClass `string`
{:#members:cssclass}








Sets the root class for the WaitingPopup control theme




#### Default Value







* null








#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To Initialize the WaitingPopup with the cssClass  value specified. 
        $("#target").ejWaitingPopup({showOnInit: true, cssClass : 'gradient-lime '});
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}







### showImage `boolean`
{:#members:showimage}








Enables or disables the default loading icon.




#### Default Value







* true








#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To set showImage API value during initialization  
        $("#target").ejWaitingPopup({ showOnInit: true, showImage: false});
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}







### showOnInit `boolean`
{:#members:showoninit}








Enables the visibility of the WaitingPopup control




#### Default Value







* false








#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To set showOnInit API value during initialization  
        $("#target").ejWaitingPopup({ showOnInit: true});
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}







### target `string`
{:#members:target} 

Specified a selector for elements, within the container. 

#### Default Value 

* null
 
#### Example
 
{% highlight html %}
 
 <div id="target"></div>
<script>
//To set target API value during initialization  
        $("#target").ejWaitingPopup({ showOnInit: true,target: "body"});
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}
  
### template `object`
{:#members:template}








Loads HTML content inside the popup panel instead of the default icon




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="content">
  <div class="block">
  <div class="logo">
</div>
   <div class="text">
    <p> Content is loading ... </p>
     </div>
            </div>
<div class="loader">
</div>
</div>
<script>
//To Initialize the WaitingPopup control with the template value specified.
        $("#target").ejWaitingPopup({ showOnInit: true,template: $('#content') });
</script>
<style>
         
          .block {
            height: 76px;
        }

        .logo {
            background-image: url("themes/images/waitingpopup/js_logo.png");
            float: left;
            height: 100%;
            width: 77px;
            margin-right: 15px;
        }

        .txt {
            float: left;
            font-size: 17px;
            height: 100%;
            text-align: left;
        }

            .txt p {
                margin: 0;
            }

        .loader {
            background: url("themes/images/waitingpopup/load_light.gif") no-repeat scroll -5px 18px transparent;
            height: 40px;
            width: 100%;
        }

        .darktheme .loader {
            background-image: url("themes/images/waitingpopup/load_dark.gif");
        }

        #content {
            cursor: default;
            height: 112px;
            width: 275px;
        }
</style>
{% endhighlight %}







### text `string`
{:#members:text}








Sets the custom text in the pop-up panel to notify the waiting process




#### Default Value







* null








#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To Initialize the WaitingPopup with the text value specified
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;' });
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}





## Methods








### hide()
{:#methods:hide}








To hide the waiting popup





#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
// Calls the hide method of WaitingPopup not to display.
popupObj.hide();
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>
{% endhighlight %}


{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// hide WaitingPopup using the hide method.
$("#target").ejWaitingPopup('hide');
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>
{% endhighlight %}







### refresh()
{:#methods:refresh}








Refreshes the WaitingPopup control by resetting the pop-up panel position and content position





#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
popupObj.refresh();
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}


{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// Refresh the WaitingPopup using refresh method.
$("#target").ejWaitingPopup('refresh');
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}







### show()
{:#methods:show}








To show the waiting popup





#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
// Calls the show method of WaitingPopup to display.
popupObj.show();
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>

{% endhighlight %}


{% highlight html %}
 
 <div id="target"></div>
<script>
$("#target").ejWaitingPopup({showOnInit: true});
// Display WaitingPopup using the show method.
$("#target").ejWaitingPopup("show");
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>
{% endhighlight %}





## Events








### create
{:#events:create}








Fires after Create WaitingPopup successfully

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
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.WaitingPopup.Model"/><span class="param-type">object</span></td>
<td class="description">returns the WaitingPopup model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To Initialize the WaitingPopup with the text value specified with create event
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;',create: function (args) {} });
</script>
<style>
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
</style>
{% endhighlight %}







### destroy
{:#events:destroy}








Fires after Destroy WaitingPopup successfully

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
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.WaitingPopup.Model"/><span class="param-type">object</span></td>
<td class="description">returns the WaitingPopup model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
 <div id="target"></div>
<script>
//To Initialize the WaitingPopup with the text value specified with destroy event
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;',destroy: function (args) {} });
</script>
<style>
            #target {
          height: 200px;
          width: 600px;
          margin: 0 auto;
      }

     #target_WaitingPopup .e-image {
          display: block;
          height: 70px;
      }
</style>

{% endhighlight %}




