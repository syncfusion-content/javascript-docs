---
layout: post
title: How to section in Splitter for Essential JS? 
description: How to achieve specific requirements in Splitter for Essential JS
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---
# How To?

### Change Expand/Collapse icons

By default, you are provided with collapse/expand icons in **Split bar** to collapse or expand the splitter panes. We have provided template support to replace existing expand/collapse icons. The template support will only replace the icons where you need to define the action handler for the template.

* (expanderTemplate)[https://help.syncfusion.com/api/js/ejsplitter#members:expandertemplate] Specifies HTML element string to replace template with existing expand/collapse icons. 

* (clickOnExpander)[https://help.syncfusion.com/api/js/ejsplitter#events:clickonexpander] event is triggered when we click on the template icon. This will allow you to define action to be performed on clicking the template icon.

{% highlight html %}

<div id="outterSplitter">
    <div id="innerSplitter">
        <div>
            <div class="cont">Pane 1 </div>
        </div>
        <div>
            <div class="cont">Pane 2 </div>
        </div>
    </div>                   
</div>

{% endhighlight %}

{% highlight js %}

        $("#innerSplitter").ejSplitter({
             height: 250,width:"80%",
             expanderTemplate: '<img class="eimg" src="basketball.png" alt="employee"/>',
			 clickOnExpander: function(args)
			{
			      if(flag) {this.collapse(0); flag=false;}
			      else {this.expand(0); flag=true;}
			}
		};)

{% endhighlight %}

{% highlight css %}

        .cont {
            padding: 10px 0 0 10px;
            text-align: center;
        }   
        .eimg {
            height:40px;
            width:35px;
			margin-left: -13px;
        }  
       .e-splitter .e-splitbar .e-splitter-h-template {
            top: 15%;
       }

{% endhighlight %}

The output for Splitter with **Template support**.

![](/js/Splitter/How-To_images/Template_Support_img.png) 