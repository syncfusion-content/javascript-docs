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

### Section for template icon suppport

By default, you are provided with collpase/expand icons in **Split bar** to collapse or expand the corresponding pane element in **Splitter**. But now, we have provided template support to replace existing expand/collapse icons. **expanderTemplate** Specifies HTML element string to replace template with existing expand/collapse icons. **clickOnExpander** event is triggered when we click on the template icon.

{% highlight html %}

<div id="outterSpliter">
    <div id="innerSpliter">
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

        $("#innerSpliter").ejSplitter({
             height: 250,width:"80%",
             expanderTemplate: '<img class="eimg" src="basketball.png" alt="employee"/>',
			 clickOnExpander: function(args)
			{
			      if(flag) {this.collapse(0); flag=false;}
			      else {this.expand(0); flag=true;}
			}
		};)

{% endhighlight %}

The output for Splitter with **Tempalet support**.

![](/js/Splitter/How-To_images/Template_Support_img.png) 