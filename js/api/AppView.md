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


{% highlight html %}
 
<div data-role="appview"></div>
       {% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core




## Members








### addMetaTags<span class="type-signature type boolean">boolean</span>
{:#members:addmetatags}








Specifies the Appview addMetaTags property to disable the meta description in the page




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set addMetaTags API value
<script>
      App.addMetaTags=false;
</script>         {% endhighlight %}







### pageTransition<span class="type-signature type enum">enum</span>
{:#members:pagetransition}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* slide








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<div data-role="appview">
<a href="page2.html" data-ej-apptransition="pop"> Move To Page2 </a>
</div>{% endhighlight %}







### renderEJMControlsByDef<span class="type-signature type boolean">boolean</span>
{:#members:renderejmcontrolsbydef}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<script>
      App.renderEJMControlsByDef=false;
</script>         {% endhighlight %}





## Methods








### activeHistory<span class="signature">()</span>
{:#methods:activehistory}








To return the Current Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Current Page
<script>            
      App.pageHistory.activeHistory();            
</script>           {% endhighlight %}







### add<span class="signature">()</span>
{:#methods:add}








To Add the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.add("http://js.syncfusion.com/demos/mobile/",{title:"Mobile Demo"});            
</script>           {% endhighlight %}







### clearForward<span class="signature">()</span>
{:#methods:clearforward}








To Clear the Forward History





Example
{:.example}


{% highlight html %}
 
//Clear Forward History
<script>            
      App.pageHistory.clearForward();            
</script>           {% endhighlight %}







### convertToRelativeUrl<span class="signature">()</span>
{:#methods:converttorelativeurl}








To convert absolute url to relative url





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.convertToRelativeUrl("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### createPage<span class="signature">()</span>
{:#methods:createpage}








To create a Appview Page





Example
{:.example}


{% highlight html %}
 
//Create AppView
<script>            
      App.createPage($("#AppPage"));            
</script>           {% endhighlight %}







### find<span class="signature">()</span>
{:#methods:find}








To find url in History





Example
{:.example}


{% highlight html %}
 
//find the url in history
<script>            
      App.pageHistory.find("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### getLocation<span class="signature">()</span>
{:#methods:getlocation}








To get the URL location of current page





Example
{:.example}


{% highlight html %}
             
<script>
      App.getLocation();//return current url location
</script>         {% endhighlight %}







### hasProtocol<span class="signature">()</span>
{:#methods:hasprotocol}








To check url has protocol





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.hasProtocol("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### initPage<span class="signature">()</span>
{:#methods:initpage}








To Initalize the dynamically created appview





Example
{:.example}


{% highlight html %}
 
//Initalize AppView
<script>            
      App.initPage();            
</script>           {% endhighlight %}







### lastHistory<span class="signature">()</span>
{:#methods:lasthistory}








To return the Last Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Last Page
<script>            
      App.pageHistory.lastHistory();            
</script>           {% endhighlight %}







### loadView<span class="signature">()</span>
{:#methods:loadview}








To load a specific view page





Example
{:.example}


{% highlight html %}
 
//Load Page
<script>            
      App.loadView("page2.html");            
</script>           {% endhighlight %}







### makeUrlAbsolute<span class="signature">()</span>
{:#methods:makeurlabsolute}








To Get Compelete Url





Example
{:.example}


{% highlight html %}
 
//get absolute url
<script>            
      App.route.makeUrlAbsolute("#default");            
</script>           {% endhighlight %}







### nextHistory<span class="signature">()</span>
{:#methods:nexthistory}








To return the Current Next History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.nextHistory();            
</script>           {% endhighlight %}







### prevHistory<span class="signature">()</span>
{:#methods:prevhistory}








To return the Current Previous History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.prevHistory();            
</script>           {% endhighlight %}







### replace<span class="signature">()</span>
{:#methods:replace}








To Replace the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.replace("#sample");            
</script>           {% endhighlight %}







### setPageRenderMode<span class="signature">()</span>
{:#methods:setpagerendermode}








To set page rendermode





Example
{:.example}


{% highlight html %}
 
//set page render mode
<script>            
      App.route.setPageRenderMode($("#page2"));            
</script>           {% endhighlight %}







### splitUrl<span class="signature">()</span>
{:#methods:spliturl}








To Split URL





Example
{:.example}


{% highlight html %}
 
//Get Url Sections
<script>            
      App.route.splitUrl("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### transferPage<span class="signature">()</span>
{:#methods:transferpage}








To transfer one page to another page





Example
{:.example}


{% highlight html %}
 
//Transfer Page
<script>
 function loadpage(){
      App.transferPage(App.activePage,"page2.html");
 }
</script>  {% endhighlight %}


{% highlight html %}
<body>
<a href="#" onClick="loadpage()" > Move to Page2  </a>
</body>{% endhighlight %}







### userAgent<span class="signature">()</span>
{:#methods:useragent}








To get the userAgent Name





Example
{:.example}


{% highlight html %}
             
<script>
      ej.userAgent();//return user agent name
</script>         {% endhighlight %}




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


{% highlight html %}
 
<div data-role="appview"></div>
       {% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core




## Members








### addMetaTags<span class="type-signature type boolean">boolean</span>
{:#members:addmetatags}








Specifies the Appview addMetaTags property to disable the meta description in the page




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set addMetaTags API value
<script>
      App.addMetaTags=false;
</script>         {% endhighlight %}







### pageTransition<span class="type-signature type enum">enum</span>
{:#members:pagetransition}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* slide








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<div data-role="appview">
<a href="page2.html" data-ej-apptransition="pop"> Move To Page2 </a>
</div>{% endhighlight %}







### renderEJMControlsByDef<span class="type-signature type boolean">boolean</span>
{:#members:renderejmcontrolsbydef}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<script>
      App.renderEJMControlsByDef=false;
</script>         {% endhighlight %}





## Methods








### activeHistory<span class="signature">()</span>
{:#methods:activehistory}








To return the Current Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Current Page
<script>            
      App.pageHistory.activeHistory();            
</script>           {% endhighlight %}







### add<span class="signature">()</span>
{:#methods:add}








To Add the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.add("http://js.syncfusion.com/demos/mobile/",{title:"Mobile Demo"});            
</script>           {% endhighlight %}







### clearForward<span class="signature">()</span>
{:#methods:clearforward}








To Clear the Forward History





Example
{:.example}


{% highlight html %}
 
//Clear Forward History
<script>            
      App.pageHistory.clearForward();            
</script>           {% endhighlight %}







### convertToRelativeUrl<span class="signature">()</span>
{:#methods:converttorelativeurl}








To convert absolute url to relative url





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.convertToRelativeUrl("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### createPage<span class="signature">()</span>
{:#methods:createpage}








To create a Appview Page





Example
{:.example}


{% highlight html %}
 
//Create AppView
<script>            
      App.createPage($("#AppPage"));            
</script>           {% endhighlight %}







### find<span class="signature">()</span>
{:#methods:find}








To find url in History





Example
{:.example}


{% highlight html %}
 
//find the url in history
<script>            
      App.pageHistory.find("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### getLocation<span class="signature">()</span>
{:#methods:getlocation}








To get the URL location of current page





Example
{:.example}


{% highlight html %}
             
<script>
      App.getLocation();//return current url location
</script>         {% endhighlight %}







### hasProtocol<span class="signature">()</span>
{:#methods:hasprotocol}








To check url has protocol





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.hasProtocol("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### initPage<span class="signature">()</span>
{:#methods:initpage}








To Initalize the dynamically created appview





Example
{:.example}


{% highlight html %}
 
//Initalize AppView
<script>            
      App.initPage();            
</script>           {% endhighlight %}







### lastHistory<span class="signature">()</span>
{:#methods:lasthistory}








To return the Last Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Last Page
<script>            
      App.pageHistory.lastHistory();            
</script>           {% endhighlight %}







### loadView<span class="signature">()</span>
{:#methods:loadview}








To load a specific view page





Example
{:.example}


{% highlight html %}
 
//Load Page
<script>            
      App.loadView("page2.html");            
</script>           {% endhighlight %}







### makeUrlAbsolute<span class="signature">()</span>
{:#methods:makeurlabsolute}








To Get Compelete Url





Example
{:.example}


{% highlight html %}
 
//get absolute url
<script>            
      App.route.makeUrlAbsolute("#default");            
</script>           {% endhighlight %}







### nextHistory<span class="signature">()</span>
{:#methods:nexthistory}








To return the Current Next History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.nextHistory();            
</script>           {% endhighlight %}







### prevHistory<span class="signature">()</span>
{:#methods:prevhistory}








To return the Current Previous History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.prevHistory();            
</script>           {% endhighlight %}







### replace<span class="signature">()</span>
{:#methods:replace}








To Replace the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.replace("#sample");            
</script>           {% endhighlight %}







### setPageRenderMode<span class="signature">()</span>
{:#methods:setpagerendermode}








To set page rendermode





Example
{:.example}


{% highlight html %}
 
//set page render mode
<script>            
      App.route.setPageRenderMode($("#page2"));            
</script>           {% endhighlight %}







### splitUrl<span class="signature">()</span>
{:#methods:spliturl}








To Split URL





Example
{:.example}


{% highlight html %}
 
//Get Url Sections
<script>            
      App.route.splitUrl("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### transferPage<span class="signature">()</span>
{:#methods:transferpage}








To transfer one page to another page





Example
{:.example}


{% highlight html %}
 
//Transfer Page
<script>
 function loadpage(){
      App.transferPage(App.activePage,"page2.html");
 }
</script>  {% endhighlight %}


{% highlight html %}
<body>
<a href="#" onClick="loadpage()" > Move to Page2  </a>
</body>{% endhighlight %}







### userAgent<span class="signature">()</span>
{:#methods:useragent}








To get the userAgent Name





Example
{:.example}


{% highlight html %}
             
<script>
      ej.userAgent();//return user agent name
</script>         {% endhighlight %}




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


{% highlight html %}
 
<div data-role="appview"></div>
       {% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core




## Members








### addMetaTags<span class="type-signature type boolean">boolean</span>
{:#members:addmetatags}








Specifies the Appview addMetaTags property to disable the meta description in the page




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set addMetaTags API value
<script>
      App.addMetaTags=false;
</script>         {% endhighlight %}







### pageTransition<span class="type-signature type enum">enum</span>
{:#members:pagetransition}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* slide








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<div data-role="appview">
<a href="page2.html" data-ej-apptransition="pop"> Move To Page2 </a>
</div>{% endhighlight %}







### renderEJMControlsByDef<span class="type-signature type boolean">boolean</span>
{:#members:renderejmcontrolsbydef}








Specifies the Appview renderEJMControlsByDef property to disable modifying nomar style controls




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set renderEJMControlsByDef API value
<script>
      App.renderEJMControlsByDef=false;
</script>         {% endhighlight %}





## Methods








### activeHistory<span class="signature">()</span>
{:#methods:activehistory}








To return the Current Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Current Page
<script>            
      App.pageHistory.activeHistory();            
</script>           {% endhighlight %}







### add<span class="signature">()</span>
{:#methods:add}








To Add the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.add("http://js.syncfusion.com/demos/mobile/",{title:"Mobile Demo"});            
</script>           {% endhighlight %}







### clearForward<span class="signature">()</span>
{:#methods:clearforward}








To Clear the Forward History





Example
{:.example}


{% highlight html %}
 
//Clear Forward History
<script>            
      App.pageHistory.clearForward();            
</script>           {% endhighlight %}







### convertToRelativeUrl<span class="signature">()</span>
{:#methods:converttorelativeurl}








To convert absolute url to relative url





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.convertToRelativeUrl("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### createPage<span class="signature">()</span>
{:#methods:createpage}








To create a Appview Page





Example
{:.example}


{% highlight html %}
 
//Create AppView
<script>            
      App.createPage($("#AppPage"));            
</script>           {% endhighlight %}







### find<span class="signature">()</span>
{:#methods:find}








To find url in History





Example
{:.example}


{% highlight html %}
 
//find the url in history
<script>            
      App.pageHistory.find("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### getLocation<span class="signature">()</span>
{:#methods:getlocation}








To get the URL location of current page





Example
{:.example}


{% highlight html %}
             
<script>
      App.getLocation();//return current url location
</script>         {% endhighlight %}







### hasProtocol<span class="signature">()</span>
{:#methods:hasprotocol}








To check url has protocol





Example
{:.example}


{% highlight html %}
 
//check for hash
<script>            
      App.route.hasProtocol("http://js.syncfusion.com/demos/mobile/default.html");            
</script>           {% endhighlight %}







### initPage<span class="signature">()</span>
{:#methods:initpage}








To Initalize the dynamically created appview





Example
{:.example}


{% highlight html %}
 
//Initalize AppView
<script>            
      App.initPage();            
</script>           {% endhighlight %}







### lastHistory<span class="signature">()</span>
{:#methods:lasthistory}








To return the Last Page History





Example
{:.example}


{% highlight html %}
 
//Get History about Last Page
<script>            
      App.pageHistory.lastHistory();            
</script>           {% endhighlight %}







### loadView<span class="signature">()</span>
{:#methods:loadview}








To load a specific view page





Example
{:.example}


{% highlight html %}
 
//Load Page
<script>            
      App.loadView("page2.html");            
</script>           {% endhighlight %}







### makeUrlAbsolute<span class="signature">()</span>
{:#methods:makeurlabsolute}








To Get Compelete Url





Example
{:.example}


{% highlight html %}
 
//get absolute url
<script>            
      App.route.makeUrlAbsolute("#default");            
</script>           {% endhighlight %}







### nextHistory<span class="signature">()</span>
{:#methods:nexthistory}








To return the Current Next History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.nextHistory();            
</script>           {% endhighlight %}







### prevHistory<span class="signature">()</span>
{:#methods:prevhistory}








To return the Current Previous History





Example
{:.example}


{% highlight html %}
 
//Get History about Next Page
<script>            
      App.pageHistory.prevHistory();            
</script>           {% endhighlight %}







### replace<span class="signature">()</span>
{:#methods:replace}








To Replace the Page History





Example
{:.example}


{% highlight html %}
 
//Set History about Page
<script>            
      App.pageHistory.replace("#sample");            
</script>           {% endhighlight %}







### setPageRenderMode<span class="signature">()</span>
{:#methods:setpagerendermode}








To set page rendermode





Example
{:.example}


{% highlight html %}
 
//set page render mode
<script>            
      App.route.setPageRenderMode($("#page2"));            
</script>           {% endhighlight %}







### splitUrl<span class="signature">()</span>
{:#methods:spliturl}








To Split URL





Example
{:.example}


{% highlight html %}
 
//Get Url Sections
<script>            
      App.route.splitUrl("http://js.syncfusion.com/demos/mobile/");            
</script>           {% endhighlight %}







### transferPage<span class="signature">()</span>
{:#methods:transferpage}








To transfer one page to another page





Example
{:.example}


{% highlight html %}
 
//Transfer Page
<script>
 function loadpage(){
      App.transferPage(App.activePage,"page2.html");
 }
</script>  {% endhighlight %}


{% highlight html %}
<body>
<a href="#" onClick="loadpage()" > Move to Page2  </a>
</body>{% endhighlight %}







### userAgent<span class="signature">()</span>
{:#methods:useragent}








To get the userAgent Name





Example
{:.example}


{% highlight html %}
             
<script>
      ej.userAgent();//return user agent name
</script>         {% endhighlight %}




