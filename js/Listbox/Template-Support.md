---
layout: post
title: Template-Support
description: template support
platform: js
control: ListBox
documentation: ug
---

# Template Support

**ListBox** widget provides the template support, when binding the data for the **ListBox**. For this behaviour, set the common syntax /element in template property. You can add any **HTML** mark-up element inside the **ListBox** using this property.

The following steps explains you the behaviour of template support with **ListBox**.

In an **HTML** page, add a **&lt;li&gt; element** to configure **ListBox** widget.



> **Note**: Images for this sample are available in ‘installed location/images/Employee’


{% highlight html %}

<div id="controlitem">
   <h3>Template Support</h3>
   <div id="selectexperts"></div>
</div>

{% endhighlight %}

{% highlight js %}

    var empList = [{
       text: "Erik Linden",
       eimg: "3",
       desig: "Representative",
       tooltip: "Representative",
       country: "England"
    }, {
       text: "John Linden",
       eimg: "6",
       tooltip: "Manager",
       desig: "Representative",
       country: "Norway"
    }, {
       text: "Louis",
       eimg: "7",
       tooltip: "CEO",
       desig: "Representative",
       country: "Australia"
    }, {
       text: "Lawrence",
       eimg: "8",
       tooltip: "President",
       desig: "Representative",
       country: "India"
    }];
    $(function() {
       $('#selectexperts').ejListBox({
          dataSource: empList,          
          width: "350",
          enableTooltip: true,
          template: '<div title="${tooltip}"><img class="eimg" src="images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/>' +
             '<div class="ename"> ${text} </div> <div class="desig"> ${desig} </div><div class="cont"> ${country} </div></div>'
       });
    });

{% endhighlight %}


Customize the template in **CSS**. 

{% highlight css %}

<style>
   .eimg {
       margin: 0;
       padding: 3px 10px 3px 3px;
       border: 0 none;
       width: 60px;
       height: 60px;
       float: left;
   }
   .ename {
       font-weight: bold;
       padding: 6px 3px 1px 3px;
   }
   .desig, .cont {
       font-size: smaller;
       padding: 3px 3px -1px 0px;
   }
   #selectexperts li {
       width: 200px;
       height: 70px;
       padding: 5px;
   }
</style>

{% endhighlight %}

Output of the above steps.

{% include image.html url="/js/ListBox/Template-Support_images/Template-Support_img1.png"%}

