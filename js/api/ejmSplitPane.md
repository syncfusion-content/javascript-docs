---
layout: post
title: ejmSplitPane
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html SplitPane control.





$(element).ejmSplitPane<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code>// Create SplitPane in unobtrusive way&lt;div id="splitview" data-role="ejmsplitpane" &gt;  &lt;div data-ej-layout="pane"&gt;   &lt;div&gt;   &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>&lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Create SplitPane in obtrusive way$(function(){$("#splitview").ejmSplitPane(); });&lt;/script&gt;</code></pre>



Requires
{:.require}


* module:jQuery

* module:ej.mobile.applicationf

* module:ej.core

* module:ej.unobtrusive

* module:ej.mobile.core

* module:ej.data

* module:ej.touch

* module:ej.mobile.scrollbar

* module:ej.mobile.scrollpanel

* module:ej.mobile.toolbar

* module:ej.mobile.menu

* module:ej.mobile.header


## Members




### allowLeftPaneScrolling<span class="type-signature type boolean">boolean</span>




Specifies whether to allow scrolling for leftpane content.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the allowLeftPaneScrolling property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-allowleftpanescrolling=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; $(function(){// Set the allowLeftPaneScrolling on initialization. //To set allowLeftPaneScrolling API value $("#splitview").ejmSplitPane({ allowLeftPaneScrolling: false });        });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the allowLeftPaneScrolling, after initialization:
// Get the allowLeftPaneScrolling API value.             $("#splitview").ejmSplitPane("option", "allowLeftPaneScrolling");                      // Set the allowLeftPaneScrolling API value.$("#splitview").ejmSplitPane("option", "allowLeftPaneScrolling", false);                        </code></pre>



### allowRightPaneScrolling<span class="type-signature type boolean">boolean</span>




Specifies whether to allow scrolling for rightpane content.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the allowRightPaneScrolling property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-allowrightpanescrolling=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; $(function(){// Set the allowRightPaneScrolling on initialization. //To set allowRightPaneScrolling API value $("#splitview").ejmSplitPane({ allowRightPaneScrolling: false });       });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the allowRightPaneScrolling, after initialization:
// Get the allowRightPaneScrolling API value.            $("#splitview").ejmSplitPane("option", "allowRightPaneScrolling");                     // Set the allowRightPaneScrolling API value.$("#splitview").ejmSplitPane("option", "allowRightPaneScrolling", false);                       </code></pre>



### android




Section for android rendermode specific functionalities.






### android.showToolbar<span class="type-signature type bool">bool</span>




Specifies whether to show the toolbar when the control is rendered in android mode.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showToolbar property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-rendermode="android" data-ej-android-showtoolbar=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showToolbar on initialization. //To set showToolbar API value $(function(){$("#splitview").ejmSplitPane({ android:{showToolbar: false} ,renderMode:"android"});    });     &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showToolbar, after initialization:
// Get the showToolbar API value.                $("#splitview").ejmSplitPane("option", "android.showToolbar");                 // Set the showToolbar API value.$("#splitview").ejmSplitPane("option", "android.showToolbar", false);                   </code></pre>



### cssClass<span class="type-signature type string">string</span>




Sets the root class for SplitPane theme. This cssClass API helps to use custom skinning option for SplitPane control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the cssClass property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-cssclass= "customclass"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the cssClass on initialization. //To set cssClass API value $("#splitview").ejmSplitPane({ cssClass: "customclass" });      &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the cssClass, after initialization:
// Get the cssClass API value.           $("#splitview").ejmSplitPane("option", "cssClass");                    // Set the cssClass API value.$("#splitview").ejmSplitPane("option", "cssClass","customclass" );                      </code></pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>




Saves current model value to browser cookies for state maintains. While refreshing the page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the enablePersistence property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-enablepersistence=true &gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the enablePersistence on initialization. //To set enablePersistence API value $("#splitview").ejmSplitPane({ enablePersistence: true });      &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.          $("#splitview").ejmSplitPane("option", "enablePersistence");                   // Set the enablePersistence API value.$("#splitview").ejmSplitPane("option", "enablePersistence", true);                      </code></pre>



### enableSwipe<span class="type-signature type boolean">Boolean</span>




Enable or Disable the swiping behavior to the content.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the enableSwipe property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-enableswipe=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the enableSwipe on initialization. //To set enableSwipe API value $("#splitview").ejmSplitPane({ enableSwipe: false });   &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the enableSwipe, after initialization:
// Get the enableSwipe API value.                $("#splitview").ejmSplitPane("option", "enableSwipe");                 // Set the enableSwipe API value.$("#splitview").ejmSplitPane("option", "enableSwipe",false);                    </code></pre>



### flat




Section for flat rendermode specific functionalities.






### flat.showLeftPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the left header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showLeftPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-flat-showleftpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showLeftPaneHeader on initialization. //To set showLeftPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ flat:{ showLeftPaneHeader: false } ,renderMode:"flat"}); });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showLeftPaneHeader, after initialization:
// Get the showLeftPaneHeader API value.                 $("#splitview").ejmSplitPane("option", "flat.showLeftPaneHeader");                     // Set the showLeftPaneHeader API value.$("#splitview").ejmSplitPane("option", "flat.showLeftPaneHeader", false);                       </code></pre>



### flat.showRightPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the right header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showRightPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-flat-showrightpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showRightPaneHeader on initialization. //To set showRightPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ flat:{ showRightPaneHeader: false } ,renderMode:"flat"});        });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showRightPaneHeader, after initialization:
// Get the showRightPaneHeader API value.                $("#splitview").ejmSplitPane("option", "flat.showRightPaneHeader");                    // Set the showRightPaneHeader API value.$("#splitview").ejmSplitPane("option", "flat.showRightPaneHeader", false);                      </code></pre>



### ios7




Section for ios7 rendermode specific functionalities.






### ios7.showLeftPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the left header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showLeftPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-ios7-showleftpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showLeftPaneHeader on initialization. //To set showLeftPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ ios7:{ showLeftPaneHeader: false } ,renderMode:"ios7"}); });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showLeftPaneHeader, after initialization:
// Get the showLeftPaneHeader API value.                 $("#splitview").ejmSplitPane("option", "ios7.showLeftPaneHeader");                     // Set the showLeftPaneHeader API value.$("#splitview").ejmSplitPane("option", "ios7.showLeftPaneHeader", false);                       </code></pre>



### ios7.showRightPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the right header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showRightPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-ios7-showrightpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showRightPaneHeader on initialization. //To set showRightPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ ios7:{ showRightPaneHeader: false } ,renderMode:"ios7"});        });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showRightPaneHeader, after initialization:
// Get the showRightPaneHeader API value.                $("#splitview").ejmSplitPane("option", "ios7.showRightPaneHeader");                    // Set the showRightPaneHeader API value.$("#splitview").ejmSplitPane("option", "ios7.showRightPaneHeader", false);                      </code></pre>



### leftHeaderSettings<span class="type-signature type string">String</span>




Section for set the header functionalities to the left header of the Split Pane control.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the leftHeaderSettings property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-leftheadersettings-title="Title"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the leftHeaderSettings on initialization. //To set leftHeaderSettings API value $("#splitview").ejmSplitPane({ leftHeaderSettings:{title: "Title" }});  &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the leftHeaderSettings, after initialization:
// Get the leftHeaderSettings API value.                 $("#splitview").ejmSplitPane("option", "leftHeaderSettings.title");                    // Set the leftHeaderSettings API value.$("#splitview").ejmSplitPane("option", "leftHeaderSettings.title","Title");                     </code></pre>



### leftPaneScrollSettings<span class="type-signature type number">Number</span>




Section for scroll panel specific functionalities appear to the left pane content


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the leftPaneScrollSettings property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-leftpanescrollsettings-targetwidth=300&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the leftPaneScrollSettings on initialization. //To set leftPaneScrollSettings API value $("#splitview").ejmSplitPane({ leftPaneScrollSettings:{targetWidth: 300 }});    &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the leftPaneScrollSettings, after initialization:
// Get the leftPaneScrollSettings API value.             $("#splitview").ejmSplitPane("option", "leftPaneScrollSettings.targetWidth");                  // Set the leftPaneScrollSettings API value.$("#splitview").ejmSplitPane("option", "leftPaneScrollSettings.targetWidth", 300);                      </code></pre>



### overlayDirection<span class="type-signature type enum">enum</span>




Specifies the direction to slide the overlay leftpane


Default Value:
{:.param}



* left




Example
{:.example}
<pre class="prettyprint"><code> //Set the overlayDirection property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-overlaydirection=right&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the overlayDirection on initialization. //To set overlayDirection API value $("#splitview").ejmSplitPane({ overlayDirection: right });      &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the overlayDirection, after initialization:
// Get the overlayDirection API value.           $("#splitview").ejmSplitPane("option", "overlayDirection");                    // Set the overlayDirection API value.$("#splitview").ejmSplitPane("option", "overlayDirection",right);                       </code></pre>



### overlayLeftPane<span class="type-signature type boolean">Boolean</span>




specifies whether to overlay the leftpane content on lower resolutions.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the overlayLeftPane property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-overlayleftpane=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the overlayLeftPane on initialization. //To set overlayLeftPane API value $("#splitview").ejmSplitPane({ overlayLeftPane: false });       &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the overlayLeftPane, after initialization:
// Get the overlayLeftPane API value.            $("#splitview").ejmSplitPane("option", "overlayLeftPane");                     // Set the overlayLeftPane API value.$("#splitview").ejmSplitPane("option", "overlayLeftPane",false);                        </code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Changes the rendering mode of the SplitPane. See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the renderMode property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-rendermode="auto"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;                    </code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; $(function(){// Set SplitPane rendermode on initialization. //To set renderMode API value $("#splitview").ejmSplitPane({ renderMode: ej.mobile.RenderMode.Android });     });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the renderMode, after initialization:
// Get the renderMode API value.                 $("#splitview").ejmSplitPane("option", "renderMode");                  // Set the renderMode  API value$("#splitview").ejmSplitpane("option", "renderMode", ej.mobile.RenderMode.Android);                     </code></pre>



### rightHeaderSettings<span class="type-signature type string">String</span>




Section for set the header functionalities to the right header of the Split Pane control.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the rightHeaderSettings property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-rightheadersettings-title="Title"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the rightHeaderSettings on initialization. //To set rightHeaderSettings API value $("#splitview").ejmSplitPane({ rightHeaderSettings:{title: "Title" }}); &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the rightHeaderSettings, after initialization:
// Get the rightHeaderSettings API value.                $("#splitview").ejmSplitPane("option", "rightHeaderSettings.title");                   // Set the rightHeaderSettings API value.$("#splitview").ejmSplitPane("option", "rightHeaderSettings.title","Title");                    </code></pre>



### rightPaneScrollSettings<span class="type-signature type number">Number</span>




Section for scroll panel specific functionalities appear to the right pane content.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the rightPaneScrollSettings property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-rightpanescrollsettings-targetwidth=300&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the rightPaneScrollSettings on initialization. //To set rightPaneScrollSettings API value $("#splitview").ejmSplitPane({ rightPaneScrollSettings:{targetWidth: 300} });   &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the rightPaneScrollSettings, after initialization:
// Get the rightPaneScrollSettings API value.            $("#splitview").ejmSplitPane("option", "rightPaneScrollSettings.targetWidth");                 // Set the rightPaneScrollSettings API value.$("#splitview").ejmSplitPane("option", "rightPaneScrollSettings.targetWidth", 300);                     </code></pre>



### theme<span class="type-signature type enum">enum</span>




Changes the theme of the SplitPane. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the theme property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-theme="auto"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; $(function(){// Set the theme on initialization. //To set theme API value $("#splitview").ejmSplitPane({ theme: ej.mobile.Theme.Dark });  });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the theme, after initialization:
// Get the theme API value.              $("#splitpane").ejmSplitPane("option", "theme");                       // Set the theme API value.$("#splitview").ejmSplitPane("option", "theme", ej.mobile.Theme.Dark);                  </code></pre>



### toolbarSettings<span class="type-signature type string">String</span>




Section for specifies toolbar functionalities when the control is rendered.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the toolbarSettings property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-toolbarsettings-title="Title"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the toolbarSettings on initialization. //To set toolbarSettings API value $("#splitview").ejmSplitPane({ toolbarSettings:{title: "Title" }});     &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the toolbarSettings, after initialization:
// Get the toolbarSettings API value.            $("#splitview").ejmSplitPane("option", "toolbarSettings.title");                       // Set the toolbarSettings API value.$("#splitview").ejmSplitPane("option", "toolbarSettings.title","Title");                        </code></pre>



### windows




Section for windows rendermode specific functionalities.






### windows.showLeftPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the left header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showLeftPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-windows-showleftpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showLeftPaneHeader on initialization. //To set showLeftPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ windows:{ showLeftPaneHeader: false } ,renderMode:"windows"});   });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showLeftPaneHeader, after initialization:
// Get the showLeftPaneHeader API value.                 $("#splitview").ejmSplitPane("option", "windows.showLeftPaneHeader");                  // Set the showLeftPaneHeader API value.$("#splitview").ejmSplitPane("option", "windows.showLeftPaneHeader", false);                    </code></pre>



### windows.showRightPaneHeader<span class="type-signature type bool">bool</span>




Specifies whether to show the right header .


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the showRightPaneHeader property in Unobtrusive way.&lt;div id="splitview" data-role="ejmsplitpane" data-ej-windows-showrightpaneheader=false&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt; // Set the showRightPaneHeader on initialization. //To set showRightPaneHeader API value $(function(){$("#splitview").ejmSplitPane({ windows:{ showRightPaneHeader: false } ,renderMode:"windows"});  });&lt;/script&gt; </code></pre><pre class="prettyprint"><code> //Get or set the showRightPaneHeader, after initialization:
// Get the showRightPaneHeader API value.                $("#splitview").ejmSplitPane("option", "windows.showRightPaneHeader");                 // Set the showRightPaneHeader API value.$("#splitview").ejmSplitPane("option", "windows.showRightPaneHeader", false);                   </code></pre>


## Methods




### loadContent<span class="signature">()</span>




To handle right side content loading



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt;// To load right Pane content$("#splitview").ejmSplitPane("loadContent", "sample.html",{reload: true,documenturl: "#Default",type: "get",title: "title",transition: "none",checkDOMChanges: true,isHigherLevel: true,hashMonitoring: true,enableNativeScrolling: true,pageId: "currentpageid",rightHeaderSettings:{showLeftButton: true,showRightButton: true,leftButtonCaption: "Home",rightButtonCaption: "Next",leftButtonStyle: "back",leftButtonTap: "LeftButtonTapped",rightButtonTap: "RightButtonTapped"}});&lt;/script&gt;</code></pre>



### refreshLeftScroller<span class="signature">()</span>




To refresh the left pane scrolling.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;div id="rightpane-sample"&gt;    &lt;/div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt;// To transfer the page$(function () {var split = $("#splitview").data("ejmSplitPane");$("#splitview").ejmSplitPane("afterLoadSuccess","loaded");});function loaded() {$.ajax({url: "sample2.html",contentType: "application/json",type: "GET",dataType: "html",crossOrigin: true,success: function (response) {$("#rightpane-sample").html(response.split(/&lt;\ body[^=""&gt;]*&gt;/gmi)[1]);ej.widget.init($("#rightpane-sample"));var instance = $("#splitview").data("ejmSplitPane");instance.refreshLeftScroller();},error: function (error) {alert("Load Failed");}});}&lt;/script&gt;&lt;/\&gt;</code></pre>



### refreshRightScroller<span class="signature">()</span>




To refresh the active right pane scrolling.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt;// To transfer the page$(function () {var split = $("#splitview").data("ejmSplitPane");$("#splitview").ejmSplitPane("afterLoadSuccess","loaded");split.loadContent("sample1.html", {transition: "none",pageId: "currentpageid"});});function loaded() {$.ajax({url: "sample2.html",contentType: "application/json",type: "GET",dataType: "html",crossOrigin: true,success: function (response) {$("#rightpane-sample").html(response.split(/&lt;\ body[^=""&gt;]*&gt;/gmi)[1]);ej.widget.init($("#rightpane-sample"));//rightpane-sample id element is declared in sample1.html file.var instance = $("#splitview").data("ejmSplitPane");instance.refreshRightScroller();},error: function (error) {alert("Load Failed");}});}&lt;/script&gt;&lt;/\&gt;</code></pre>



### transferPage<span class="signature">()</span>




To handle transferPage



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;&lt;script&gt;// To transfer the page$("#splitview").ejmSplitPane("transferPage", $("#newpage"),{reload: true,documenturl: "#Default",type: "get",title: "title",transition: "none",enableNativeScrolling: true,pageId: "currentpageid",checkDOMChanges: true,isHigherLevel: true,hashMonitoring: true,rightHeaderSettings:{showLeftButton: true,showRightButton: true,leftButtonCaption: "Home",rightButtonCaption: "Next",leftButtonStyle: "back",leftButtonTap: "LeftButtonTapped",rightButtonTap: "RightButtonTapped"}});&lt;/script&gt;</code></pre>


## Events




### afterLoadSuccess




Event triggers after the ajax content is loaded.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.topage</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the sub page.</td></tr><tr><td class="name"><code>argument.rightPaneHeader</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the instance of right header</td></tr><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toolbar<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>leftPaneHeader</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the instance of left header</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview" data-role="ejmsplitpane" data-ej-afterloadsuccess="afterLoadSuccess"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // afterLoadSuccess event for Splitpanes$("#splitview").ejmSplitPane({        afterLoadSuccess: function (args) { //handle the event }        });           </code></pre>



### beforeTransfer




Event triggers before the content is transfer.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.topage</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the sub page.</td></tr><tr><td class="name"><code>argument.rightPaneHeader</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the instance of right header</td></tr><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toolbar<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>leftPaneHeader</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the instance of left header</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="splitview" data-role="ejmsplitpane" data-ej-afterloadsuccess="beforeTransfer"&gt;  &lt;div data-ej-layout="pane"&gt;    &lt;div&gt;    &lt;/div&gt;  &lt;/div&gt;  &lt;div data-ej-layout="pane"&gt;  &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> //  beforeTransfer event for Splitpanes$("#splitview").ejmSplitPane({        beforeTransfer: function (args) { //handle the event }        });           </code></pre>


