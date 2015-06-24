---
layout: post
title: ejWaitingPopup
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Button control.










## $(element).ejWaitingPopup<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
// Simple waiting popup creation.
$("#target").ejWaitingPopup({ showOnInit: true });
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






## Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.waitingpopup.js




## Members








### cssClass<span class="type-signature type string">String</span>








Sets the root class for the WaitingPopup control theme




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To Initialize the WaitingPopup with the cssClass  value specified. 
        $("#target").ejWaitingPopup({showOnInit: true, cssClass : 'gradient-lime '});
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### showImage<span class="type-signature type boolean">Boolean</span>








Enables or disables the default loading icon.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To set showImage API value during initialization  
        $("#target").ejWaitingPopup({ showOnInit: true, showImage: false});
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### showOnInit<span class="type-signature type boolean">Boolean</span>








Enables the visibility of the WaitingPopup control




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To set showOnInit API value during initialization  
        $("#target").ejWaitingPopup({ showOnInit: true});
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### template<span class="type-signature type object">object</span>








Loads HTML content inside the popup panel instead of the default icon




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="content"&gt;
  &lt;div class="block"&gt;
  &lt;div class="logo"&gt;
&lt;/div&gt;
   &lt;div class="text"&gt;
    &lt;p&gt; Content is loading ... &lt;/p&gt;
     &lt;/div&gt;
            &lt;/div&gt;
&lt;div class="loader"&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
//To Initialize the WaitingPopup control with the template value specified.
        $("#target").ejWaitingPopup({ showOnInit: true,template: $('#content') });
&lt;/script&gt;
&lt;style&gt;
         
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
&lt;/style&gt;</code>
</pre>






### text<span class="type-signature type string">String</span>








Sets the custom text in the pop-up panel to notify the waiting process




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To Initialize the WaitingPopup with the text value specified
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;' });
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>




## Methods








### hide<span class="signature">()</span>








To hide the waiting popup





Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
// Calls the hide method of WaitingPopup not to display.
popupObj.hide();
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// hide WaitingPopup using the hide method.
$("#target").ejWaitingPopup('hide');
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### refresh<span class="signature">()</span>








Refreshes the WaitingPopup control by resetting the pop-up panel position and content position





Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
popupObj.refresh();
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// Refresh the WaitingPopup using refresh method.
$("#target").ejWaitingPopup('refresh');
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### show<span class="signature">()</span>








To show the waiting popup





Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// Initialize the WaitingPopup object.
  var popupObj = $("#target").data("ejWaitingPopup");
// Calls the show method of WaitingPopup to display.
popupObj.show();
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
$("#target").ejWaitingPopup({showOnInit: true});
// Display WaitingPopup using the show method.
$("#target").ejWaitingPopup("show");
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>




## Events








### create








Fires after Create waitingpopup successfully

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the waitingpopup model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To Initialize the WaitingPopup with the text value specified with create event
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;',create: function (args) {} });
&lt;/script&gt;
&lt;style&gt;
              #target {
            height: 200px;
            width: 600px;
            margin: 0 auto;
        }

       #target_WaitingPopup .e-image {
            display: block;
            height: 70px;
        }
&lt;/style&gt;</code>
</pre>






### destroy








Fires after Destroy waitingpopup successfully

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the waitingpopup model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
 &lt;div id="target"&gt;&lt;/div&gt;
&lt;script&gt;
//To Initialize the WaitingPopup with the text value specified with destroy event
        $("#target").ejWaitingPopup({showOnInit: true, text: 'waiting&hellip;',destroy: function (args) {} });
&lt;/script&gt;
&lt;style&gt;
            #target {
          height: 200px;
          width: 600px;
          margin: 0 auto;
      }

     #target_WaitingPopup .e-image {
          display: block;
          height: 70px;
      }
&lt;/style&gt;</code>
</pre>



