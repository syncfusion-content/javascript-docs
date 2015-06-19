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



> _**Note: Images for this sample are available in ‘installed location/images/Employee’**_

> 

<table>
<tr>
<td>
<b>[HTML]   </b>&lt;div id="controlitem"&gt;    <h3>Template Support</h3>    &lt;div id="selectexperts"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in JavaScript &lt;script type="text/javascript"&gt;    var target;    var empList = [       { text: "Erik Linden", eimg: "3", desig: "Representative", tooltip: "Representative", country: "England" }, { text: "John Linden", eimg: "6", tooltip: "Manager", desig: "Representative", country: "Norway" },          { text: "Louis", eimg: "7", tooltip: "CEO", desig: "Representative", country: "Australia" }, { text: "Lawrence", eimg: "8", tooltip: "President", desig: "Representative", country: "India" }];    $(function () {        $('#selectexperts').ejListBox({            dataSource: empList, height: "245", enableTooltip: true,            template: '&lt;div title="${tooltip}"&gt;&lt;img class="eimg" src="images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +                        '&lt;div class="ename"&gt; ${text} &lt;/div&gt; &lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;&lt;/div&gt;'        });    });&lt;/script&gt;</td></tr>
</table>
Customize the template in **CSS**. 

{% highlight css %}

**[CSS]**  
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

{% include image.html url="/js/ListBox/Concepts-and-Features/Template-Support_images/Template-Support_img1.png" Caption="ListBox with template support"%}

