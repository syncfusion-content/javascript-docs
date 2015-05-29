---
layout: post
title: getting-started
description: getting started
platform: js
control: TagCloud
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **TagCloud** in your application with **JavaScript**, **ASP.NET MVC** and **ASP.NET**.

## Create your first TagCloud in JavaScript

The **TagCloud** can be easily configured to the div element in which the tags are placed. The following screenshot illustrates the functionality of a **TagCloud** widget with a list of the topmost search engines. 



{% include image.html url="\js\TagCloud\getting-started_images\getting-started_img1.png" Caption="Figure 1: TagCloud Widget"%}

### Create TagCloud widget

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head> 
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
      <!--Add necessary HTML elements-->
       <!--Apply Scripts-->//Add necessary HTML elements
      //Apply Scripts
</body>
</html>


{% endhighlight %}



Add necessary **HTML** elements.



{% highlight html %}


    <div id="tagcloud">
    </div>


{% endhighlight %}



Add the following code example before **&lt;/body&gt;** tag to add list of items to the **TagCloud** and initialize the **TagCloud** widget.



{% highlight js %}


      <script>
            $("document").ready(function (event) {
              var websiteCollection = [
              { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
         { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
         { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
         { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
         { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
         { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
         { text: "Infospace", url: "http://infospace.com/", frequency: 8 },
         { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
         { text: "Dogpile", url: "http://www.dogpile.com/", frequency: 4 },

         { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
         { text: "Info", url: "http://www.info.com/", frequency: 6 },
         { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
         { text: "Contenko", url: "http://www.contenko.com/", frequency: 3 },
         { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
            ];
            $("#tagcloud").ejTagCloud({
                dataSource: websiteCollection,
                titleText: "Tech Sites"
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays the output of the above code example.



{% include image.html url="\js\TagCloud\getting-started_images\getting-started_img2.png" Caption="Figure 2: TagCloud with Min/Max Fonts"%}

### Set Min and Max Font Size

In the above code example, the **fFrequency** properties are used to set the min and max font size to the **TagCloud** list item.

{% highlight js %}


      <script>
            $("document").ready(function (event) {
              var websiteCollection = [
              { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
         { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
         { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
         { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
         { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
         { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
         { text: "Infospace", url: "http://infospace.com/", frequency: 8 },
         { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
         { text: "Dogpile", url: "http://www.dogpile.com/", frequency: 4 },

         { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
         { text: "Info", url: "http://www.info.com/", frequency: 6 },
         { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
         { text: "Contenko", url: "http://www.contenko.com/", frequency: 3 },
         { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
            ];
            $("#tagcloud").ejTagCloud({         
                dataSource: websiteCollection,
                titleText: "Tech Sites"
            });
        });
    </script>


{% endhighlight %}



In the above code, the min font size is 3 and max font size is 24.

### Set event to perform an operation

Here, you can set the **TagCloud** events such as create, mouseover, mouseout, click.



{% highlight js %}


      <script>
    $("document").ready(function (event) {
              var websiteCollection = [
              { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
         { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
         { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
         { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
         { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
         { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
         { text: "Infospace", url: "http://infospace.com/", frequency: 8 },
         { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
         { text: "Dogpile", url: "http://www.dogpile.com/", frequency: 4 },

         { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
         { text: "Info", url: "http://www.info.com/", frequency: 6 },
         { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
         { text: "Contenko", url: "http://www.contenko.com/", frequency: 3 },
         { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
            ];
        $("#tagcloud").ejTagCloud({
            dataSource: websiteCollection,
            titleText: "Tech Sites",
            create: "oncreate",
            mouseover: "onmouseover",
            mouseout: "onmouseout",
            click: "onclick",
            width: "auto"
        });
    });
    function oncreate(args) {
        alert();
    }
    function onmouseover(args) {
        alert();
    }
    function onmouseout(args) {
        alert();
    }
    function onclick(args) {
        alert();
    }
</script>


{% endhighlight %}



In the above code example, the **alert()** function is used  to show the events that happened.

## Create your first TagCloud in MVC

**ASP.NET MVC TagCloud** provides support to display a weighted list, where the weight of each item is reflected by the size of the item's text. **TagCloud** is rendered as a link and as you click it, you can drill into the selected category. Refer the following guidelines to create **TagCloud** scenario. This allows you to display a weighted list.

{% include image.html url="\js\TagCloud\getting-started_images\getting-started_img3.png" Caption="Figure 3: TagCloud"%}

In the above screenshot, you can see the weighted list and a click on any item drills into the respective category.

**Create a TagCloud** 

**Essential Studio ASP.NET MVC****TagCloud** widget has built-in features such as clicking on one of the sites in the **TagCloud** brings all relevant results only from the selected source. You can easily create the **TagCloud** widget element as follows.

1. You can create a **MVC** Project and add required assemblies, scripts and styles to it.  Refer [MVC-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

2. Add the following code to the corresponding view page to render **TagCloud**.





@Html.EJ().TagCloud("tagEvents").Datasource((IEnumerable<MvcApplication.Models.WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("text").Url("url").Frequency("frequency")).Title("Tech Sites")





3. Add the following style to show the weighted list.



&lt;style type="text/css"&gt;

        #tagEvents {

            margin: 0 auto;

        }

    &lt;/style&gt;

**Set the Min and Max Font Size**

Create the class for WebsiteCollection and define the necessary data members. Add the following code in WebsiteCollection.cs part.





public class WebsiteCollection

    {

        public string text { get; set; }

        public string url { get; set; }

        public int frequency { get; set; }

    }



You can set the **minimum** and **maximum** font size in **Frequency** tag by adding the following code example to the Home Controller.cs part.

****

public ActionResult Index()

  {

List<WebsiteCollection> sites = new List<WebsiteCollection>();



 sites.Add(new WebsiteCollection { text = "Google", url = "http://tech.firstpost.com/tag/google", frequency = 12 });

            sites.Add(new WebsiteCollection { text = "Apple", url = "http://tech.firstpost.com/tag/apple-iwork", frequency = 3 });

            sites.Add(new WebsiteCollection { text = "Drone", url = "http://tech.firstpost.com/tag/drone", frequency = 8 });

            sites.Add(new WebsiteCollection { text = "google Drone", url = "http://tech.firstpost.com/tag/google-drones/", frequency = 2 });

            sites.Add(new WebsiteCollection { text = "apple iwork", url = "http://tech.firstpost.com/tag/apple-iwork", frequency = 12 });

            sites.Add(new WebsiteCollection { text = "tech-buzz", url = "http://tech.firstpost.com/tag/tech-buzz", frequency = 5 });

            sites.Add(new WebsiteCollection { text = "netizens", url = "http://tech.firstpost.com/tag/netizens", frequency = 8 });

            sites.Add(new WebsiteCollection { text = "selfile", url = "http://tech.firstpost.com/tag/selfie", frequency = 20 });

            sites.Add(new WebsiteCollection { text = "globalselfile", url = "http://tech.firstpost.com/tag/nasa-globalselfie", frequency = 1 });

            sites.Add(new WebsiteCollection { text = "extreme", url = "http://www.extremetech.com/", frequency = 3 });

            sites.Add(new WebsiteCollection { text = "at-t move", url = "http://www.extremetech.com/extreme/182815-att-moves-to-acquire-directv-to-defend-against-comcast-everyone-loses", frequency = 5 });

            sites.Add(new WebsiteCollection { text = "Gearlog", url = "http://www.gearlog.com/", frequency = 9 });

            sites.Add(new WebsiteCollection { text = "Information Week", url = "http://www.informationweek.com/", frequency = 0 });

            sites.Add(new WebsiteCollection { text = "PCWorld", url = "http://www.pcworld.com/", frequency = 11 });

            sites.Add(new WebsiteCollection { text = "Tech Republic", url = "http://techrepublic.com/", frequency = 3 });

            sites.Add(new WebsiteCollection { text = "Valleywag", url = "http://valleywag.gawker.com/", frequency = 6 });

            sites.Add(new WebsiteCollection { text = "computing", url = "http://www.extremetech.com/category/computing", frequency = 9 });

            sites.Add(new WebsiteCollection { text = "WebProNews", url = "http://www.webpronews.com/", frequency = 2 });             

            ViewBag.datasource = sites;

            return View();           

}

**Set an event to perform operation**

You can perform the event operations like mouse hover, mouse hover away by adding the following code example inside index.cshtml part.      





@Html.EJ().TagCloud("tagEvents").Datasource((IEnumerable<MvcApplication.Models.WebsiteCollection>)ViewBag.datasource).TagCloudFields(tag => tag.Text("text").Url("url").Frequency("frequency")).Title("Tech sites").ClientSideEvents(evt => evt.Create("oncreate").MouseOver("onmouseover").MouseOut("onmouseout"))



&lt;div id="tagCloudTarget"&gt;

    &lt;ul&gt;

        <li>mouseover</li>

        <li>mouseout</li>

        <li>click</li>

    &lt;/ul&gt;

&lt;/div&gt;

    @Html.EJ().DropDownList("selectControls_input").TargetID("tagCloudTarget").ShowCheckbox(true).CheckAll(true).ClientSideEvents(evt => evt.Change("evtpropscheckedevent"))

    &lt;style type="text/css"&gt;

        #tagEvents {

            margin: 0 auto;

        }

    &lt;/style&gt;

&lt;script&gt;

        function evtpropscheckedevent(args) {

            tagObj = $("#tagEvents").data("ejTagCloud");

            if (args.isChecked) {

                switch (args.selectedText) {

                    case "mouseover": tagObj.option(args.selectedText, "onmouseover"); break;

                    case "mouseout": tagObj.option(args.selectedText, "onmouseout"); break;

                    case "click": tagObj.option(args.selectedText, "onclick"); break;

                }

            }

            else tagObj.option(args.selectedText, null);

        }



        function oncreate(args) {

            jQuery.addEventLog("Tagcloud has been <span class='eventTitle'>created</span>.");

        }

        function onmouseover(args) {

            jQuery.addEventLog("Mouse pointer is <span class='eventTitle'>hovered &lt;/span&gt; on " + args.value + ".&lt;/br&gt;");

        }

        function onmouseout(args) {

            jQuery.addEventLog("Mouse pointer is <span class='eventTitle'>hovered away</span> from " + args.value + ".&lt;/br&gt;");

        }

        function onclick(args) {

            jQuery.addEventLog(args.selectedText + " is <span class='eventTitle'>clicked</span>.&lt;/br&gt;");

        }

        function onClear() {

            $("#EventLog").html("");

        }



    &lt;/script&gt;







You can execute the above code to render the following output.



{% include image.html url="\js\TagCloud\getting-started_images\getting-started_img4.png" Caption="Figure 4: TagCloud"%}

When you move the mouse to latest technology (weighted) list, it is denoted in Event Trace and this is illustrated in the following screenshot.



{% include image.html url="\js\TagCloud\getting-started_images\getting-started_img5.png" Caption="Figure 5: Event Trace"%}

## Create your first TagCloud in ASP.NET

You can easily configure the **TagCloud** to the **&lt;div&gt;** element where the tags are placed. The following screenshot illustrates you the functionality of a **TagCloud** with a list of the topmost search engines. 



![](getting-started_images\getting-started_img6.png)

_Figure_ _6__: TagCloud control_

**Create a TagCloud** 

**Essential Studio ASP.NET TagCloud** has built-in features such as clicking on one of the sites in the **TagCloud** brings all relevant results only from the selected source. You can easily create the **TagCloud** control element as follows.

* You can create a **WEB** Project and add required assemblies, scripts and styles to it.  Refer [ASP-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

Create an **A****SPX** file and add the following code to the file.



**[ASPX]**

<ej:TagCloud ID="TagEvents" Title="Tech Sites" runat="server" DataTextField="text"

        DataUrlField="url" DataFrequencyField="frequency">&lt;/ej:TagCloud&gt;



Add the following code in code behind to bind the data source with **TagCloud** control.



**[CS]**

protected void Page_Load(object sender, EventArgs e)

        {

           this.TagEvents.DataSource = new TagCloudData().GetTagCloudItems().ToList();

}

public class TagCloudData

    {



        public string text { get; set; }

        public string url { get; set; }

        public int frequency { get; set; }



        public List<TagCloudData> GetTagCloudItems()

        {

            List<TagCloudData> sites = new List<TagCloudData>() ;

            sites.Add(new TagCloudData { text = "Yahoo!", url = "http://search.yahoo.com/", frequency = 20 });

            sites.Add(new TagCloudData { text = "DuckDuckGo", url = "https://duckduckgo.com/", frequency = 5 });

            sites.Add(new TagCloudData { text = "Bing", url = "http://www.bing.com/", frequency = 23 });

            sites.Add(new TagCloudData { text = "Blekko", url = "http://blekko.com/", frequency = 4 });

            sites.Add(new TagCloudData { text = "Alhea", url = "http://www.alhea.com/", frequency = 3 });

            sites.Add(new TagCloudData { text = "MyWebSearch", url = "http://home.mywebsearch.com/index.jhtml", frequency = 10 });

            sites.Add(new TagCloudData { text = "Infospace", url = "http://infospace.com/", frequency = 8 });

            sites.Add(new TagCloudData { text = "Google", url = "https://www.google.co.in/", frequency = 24 });

            sites.Add(new TagCloudData { text = "Dogpile", url = "http://www.dogpile.com/", frequency = 4 });



            sites.Add(new TagCloudData { text = "Wow", url = "http://www.wow.com/", frequency = 14 });

            sites.Add(new TagCloudData { text = "Info", url = "http://www.info.com/", frequency = 6 });

            sites.Add(new TagCloudData { text = "WebCrawler", url = "http://www.webcrawler.com/", frequency = 12 });

            sites.Add(new TagCloudData { text = "Contenko", url = "http://www.contenko.com/", frequency = 3 });

            sites.Add(new TagCloudData { text = "Aol Search", url = "http://search.aol.com", frequency = 16 });



            return sites;

        }    

    }



The following screenshot displays the output of the above code example.



![](getting-started_images\getting-started_img7.png)

_Figure_ _7__: TagCloud with Min/Max Fonts_

**Set Min and Max Font Size**

In the above code example, the **Frequency** properties are used to set the min and max font size to the **TagCloud** list item.



**[CS]**

public List<TagCloudData> GetTagCloudItems()

        {

List<TagCloudData> sites = new List<TagCloudData>() ;

            sites.Add(new TagCloudData { text = "Yahoo!", url = "http://search.yahoo.com/", frequency = 20 });

            sites.Add(new TagCloudData { text = "DuckDuckGo", url = "https://duckduckgo.com/", frequency = 5 });

//use the list values given above

}



In the above code, the min font size is 5 and max font size is 20.

**Set event to perform an operation**

Here, you can set the **TagCloud** server side click event.

Add the same code that is given in Step 3 

**[ASPX]**

<ej:TagCloud ID="TagEvents" Title="Tech Sites" runat="server" DataTextField="text"

        DataUrlField="url" DataFrequencyField="frequency" OnClick="Tagevents_Click">

    &lt;/ej:TagCloud&gt;

    &lt;label id="EventLog" runat="server"&gt;

    &lt;/label&gt;



**[CS]**

protected void Tagevents_Click(object sender, Syncfusion.JavaScript.Web.TagCloudEventArgs e)

        {

            this.EventLog.InnerHtml += "\n" + "TagCloud Item " + e.Value + "has been clicked< \r\n";

        }


In the above code example, the **Event log** is used to illustrate the events that occurred.

