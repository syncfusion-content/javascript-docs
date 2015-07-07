---
layout: post
title: AppView
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Appview.










$(element).AppView<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div data-role="appview"&gt;&lt;/div&gt;
       </code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core




## Members








### addMetaTags<span class="type-signature type boolean">boolean</span>
{:#addmetatags}
{:#addMetaTags}








Specifies the Appview addMetaTags property to disable the meta description in the page




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set addMetaTags API value
&lt;script&gt;
      App.addMetaTags=false;
&lt;/script&gt;         </code>
</pre>






### pageTransition<span class="type-signature type enum">enum</span>
{:#pagetransition}
{:#pageTransition}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* slide








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set renderEJMControlsByDef API value
&lt;div data-role="appview"&gt;
&lt;a href="page2.html" data-ej-apptransition="pop"&gt; Move To Page2 &lt;/a&gt;
&lt;/div&gt;</code>
</pre>






### renderEJMControlsByDef<span class="type-signature type boolean">boolean</span>
{:#renderejmcontrolsbydef}
{:#renderEJMControlsByDef}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set renderEJMControlsByDef API value
&lt;script&gt;
      App.renderEJMControlsByDef=false;
&lt;/script&gt;         </code>
</pre>




## Methods








### activeHistory<span class="signature">()</span>
{:#activehistory}
{:#activeHistory}








To return the Current Page History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get History about Current Page
&lt;script&gt;            
      App.pageHistory.activeHistory();            
&lt;/script&gt;           </code>
</pre>






### add<span class="signature">()</span>
{:#add}
{:#add}








To Add the Page History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Set History about Page
&lt;script&gt;            
      App.pageHistory.add("http://js.syncfusion.com/demos/mobile/",{title:"Mobile Demo"});            
&lt;/script&gt;           </code>
</pre>






### clearForward<span class="signature">()</span>
{:#clearforward}
{:#clearForward}








To Clear the Forward History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Clear Forward History
&lt;script&gt;            
      App.pageHistory.clearForward();            
&lt;/script&gt;           </code>
</pre>






### convertToRelativeUrl<span class="signature">()</span>
{:#converttorelativeurl}
{:#convertToRelativeUrl}








To convert absolute url to relative url





Example
{:.example}

<pre class="prettyprint">
<code> 
//check for hash
&lt;script&gt;            
      App.route.convertToRelativeUrl("http://js.syncfusion.com/demos/mobile/default.html");            
&lt;/script&gt;           </code>
</pre>






### createPage<span class="signature">()</span>
{:#createpage}
{:#createPage}








To create a Appview Page





Example
{:.example}

<pre class="prettyprint">
<code> 
//Create AppView
&lt;script&gt;            
      App.createPage($("#AppPage"));            
&lt;/script&gt;           </code>
</pre>






### find<span class="signature">()</span>
{:#find}
{:#find}








To find url in History





Example
{:.example}

<pre class="prettyprint">
<code> 
//find the url in history
&lt;script&gt;            
      App.pageHistory.find("http://js.syncfusion.com/demos/mobile/");            
&lt;/script&gt;           </code>
</pre>






### getLocation<span class="signature">()</span>
{:#getlocation}
{:#getLocation}








To get the URL location of current page





Example
{:.example}

<pre class="prettyprint">
<code>             
&lt;script&gt;
      App.getLocation();//return current url location
&lt;/script&gt;         </code>
</pre>






### hasProtocol<span class="signature">()</span>
{:#hasprotocol}
{:#hasProtocol}








To check url has protocol





Example
{:.example}

<pre class="prettyprint">
<code> 
//check for hash
&lt;script&gt;            
      App.route.hasProtocol("http://js.syncfusion.com/demos/mobile/default.html");            
&lt;/script&gt;           </code>
</pre>






### initPage<span class="signature">()</span>
{:#initpage}
{:#initPage}








To Initalize the dynamically created appview





Example
{:.example}

<pre class="prettyprint">
<code> 
//Initalize AppView
&lt;script&gt;            
      App.initPage();            
&lt;/script&gt;           </code>
</pre>






### lastHistory<span class="signature">()</span>
{:#lasthistory}
{:#lastHistory}








To return the Last Page History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get History about Last Page
&lt;script&gt;            
      App.pageHistory.lastHistory();            
&lt;/script&gt;           </code>
</pre>






### loadView<span class="signature">()</span>
{:#loadview}
{:#loadView}








To load a specific view page





Example
{:.example}

<pre class="prettyprint">
<code> 
//Load Page
&lt;script&gt;            
      App.loadView("page2.html");            
&lt;/script&gt;           </code>
</pre>






### makeUrlAbsolute<span class="signature">()</span>
{:#makeurlabsolute}
{:#makeUrlAbsolute}








To Get Compelete Url





Example
{:.example}

<pre class="prettyprint">
<code> 
//get absolute url
&lt;script&gt;            
      App.route.makeUrlAbsolute("#default");            
&lt;/script&gt;           </code>
</pre>






### nextHistory<span class="signature">()</span>
{:#nexthistory}
{:#nextHistory}








To return the Current Next History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get History about Next Page
&lt;script&gt;            
      App.pageHistory.nextHistory();            
&lt;/script&gt;           </code>
</pre>






### prevHistory<span class="signature">()</span>
{:#prevhistory}
{:#prevHistory}








To return the Current Previous History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get History about Next Page
&lt;script&gt;            
      App.pageHistory.prevHistory();            
&lt;/script&gt;           </code>
</pre>






### replace<span class="signature">()</span>
{:#replace}
{:#replace}








To Replace the Page History





Example
{:.example}

<pre class="prettyprint">
<code> 
//Set History about Page
&lt;script&gt;            
      App.pageHistory.replace("#sample");            
&lt;/script&gt;           </code>
</pre>






### setPageRenderMode<span class="signature">()</span>
{:#setpagerendermode}
{:#setPageRenderMode}








To set page rendermode





Example
{:.example}

<pre class="prettyprint">
<code> 
//set page render mode
&lt;script&gt;            
      App.route.setPageRenderMode($("#page2"));            
&lt;/script&gt;           </code>
</pre>






### splitUrl<span class="signature">()</span>
{:#spliturl}
{:#splitUrl}








To Split URL





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get Url Sections
&lt;script&gt;            
      App.route.splitUrl("http://js.syncfusion.com/demos/mobile/");            
&lt;/script&gt;           </code>
</pre>






### transferPage<span class="signature">()</span>
{:#transferpage}
{:#transferPage}








To transfer one page to another page





Example
{:.example}

<pre class="prettyprint">
<code> 
//Transfer Page
&lt;script&gt;
 function loadpage(){
      App.transferPage(App.activePage,"page2.html");
 }
&lt;/script&gt;  </code>
</pre>
<pre class="prettyprint">
<code>&lt;body&gt;
&lt;a href="#" onClick="loadpage()" &gt; Move to Page2  &lt;/a&gt;
&lt;/body&gt;</code>
</pre>






### userAgent<span class="signature">()</span>
{:#useragent}
{:#userAgent}








To get the userAgent Name





Example
{:.example}

<pre class="prettyprint">
<code>             
&lt;script&gt;
      ej.userAgent();//return user agent name
&lt;/script&gt;         </code>
</pre>



