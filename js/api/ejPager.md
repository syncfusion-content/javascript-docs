---
layout: post
title: Properties, Methods and Events of ejPager Widget
description: Methods,members and events avaliable in ejPager
documentation: API
platform: js
keywords: ejPager, API, Essential JS Pager
metaname: 
metacontent: 
---

# Pager

Custom Design for HTML Pager control.


#### Syntax

{% highlight javascript %}

$(element).ejPager()

{% endhighlight %}



#### Example

{% highlight html %}
 
<div id="pager"></div> 
 
<script>
// Create ejPager
pagerModel = {pageSize:5,pageCount:5,currentPage:1}
$("#pager").ejPager(pagerModel);     
</script>

{% endhighlight %}


#### Requires

* module:jQuery-1.10.2.min.js
* module:ej.core.js
* module:ej.touch.js
* module:ej.pager.js


## Members


### pageSize `Number`

{:#members:pagesize}

Gets or sets a value that indicates whether to define the number of records displayed per page.

#### Default Value:
{:.param}
* 12

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({pageSize: 2 })
});
</script>
{% endhighlight %}


### pageCount `Number`
{:#members:pagecount}

Gets or sets a value that indicates whether to define the number of pages displayed in the pager for navigation.

#### Default Value:
{:.param}
* 10

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({pageCount: 5 })
});
</script>
{% endhighlight %}


### currentPage `Number`
{:#members:currentpage}

Gets or sets a value that indicates whether to define which page to display currently in pager.

#### Default Value:
{:.param}
* 1

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({currentPage: 1 })
});
</script>
{% endhighlight %}

### totalPages `Number`
{:#members:totalpages}

Get or sets a value of total number of pages in the pager. The totalPages value is calculated based on page size and total records.

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({totalPages: 1 })
});
</script>
{% endhighlight %}

### totalRecordsCount `Number`
{:#members:totalrecordscount}

Get the value of total number of records which is bound to a data item. 

#### Default Value:
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({totalRecordsCount: 10 })
});
</script>
{% endhighlight %}

### enableQueryString `Boolean`
{:#members:enablequerystring}

Gets or sets a value that indicates whether to pass the current page information as a query string along with the URL while navigating to other page.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({enableQueryString: true })
});
</script>

{% endhighlight %}

## enableExternalMessage `Boolean`
{:#members:enableExternalMessage}

Gets or sets a value that indicates whether to display the external Message in Pager.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({enableExternalMessage: true })
});
</script>

{% endhighlight %}


## externalMessage `String`
{:#members:externalMessage}

Gets or sets a value that indicates whether to display the external Message in Pager.

#### Default Value:
{:.param}
* empty string

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({enableExternalMessage: true, externalMessage:"external message in Pager" })
});
</script>

{% endhighlight %}

N> `enableExternalMessage` default value as false. so We must enable `enableExternalMessage` set as true when enable externalMessage.



## customText `String`
{:#members:customText}

Gets or sets a value that indicates whether to display the custom text message in Pager.

#### Default Value:
{:.param}
* empty string

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({customText ="custom pager text"})
});
</script>

{% endhighlight %}


### locale `String`
{:#members:locale}

Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data i.e. in a language and culture specific to a particular country or region.

#### Default Value:
{:.param}
* "en-US"

#### Example
{:.example}
{% highlight html %} 
<div id="pager"></div> 
<script>
ej.Pager.locale["es-ES"] = {
   pagerInfo: "{0} de {1} p&aacute;ginas ({2} art&iacute;culos)"
};
$("#pager").ejPager({locale: "es-ES"})
});
</script>
{% endhighlight %}



### enableRTL `Boolean`
{:#members:enablertl}

Align content in the pager control from right to left by setting the property as true.

#### Default Value:
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({enableRTL:true})
});
</script>
{% endhighlight %}

### showPageInfo `Boolean`
{:#members:showpageinfo}

Shows or hides the current page information in pager footer.

#### Default Value:
{:.param}
* true

#### Example
{:.example}

{% highlight html %}

<div id="pager"></div> 
<script>
$("#pager").ejPager({showPageInfo:false})
});
</script>

{% endhighlight %}

## Methods

### gotoPage(pageIndex)
{:#methods:gotopage}

Send a paging request to specified page through the pager control.

####Example

{:.example}


{% highlight html %}
 
			<div class="frame">
                        <ul id="sliderContent">
						     <li><img class="image" src="{{ site.releaseversion }}/themes/web/images/rotator/nature.jpg"  title="Nature"/></li>
                            <li><img class="image" src="{{ site.releaseversion }}/themes/web/images/rotator/bird.jpg"   title="Beautiful Bird"/></li>
                            <li><img class="image" src="{{ site.releaseversion }}/themes/web/images/rotator/sculpture.jpg"  title="Amazing Sculptures"/></li>
                           
                        </ul>
                    </div>                


    <script type="text/javascript">
        $(function () {
            // declaration
          
            $("#sliderContent").ejRotator({
                slideWidth: "600px",
                frameSpace: "0px",
                showPager: true,
            });
		
			var obj = $("#sliderContent").ejRotator("instance")
				$('.e-pager-wrap').css('display','none')
			$("<div id='pager' style='width:600px'></div>").appendTo($("body"));
			$('#pager').ejPager({totalPages:3,pageCount:2,click:"page"})
        });
		function page(args){
		$("#pager").children().find('.e-currentitem').removeClass('e-currentitem');
		$(args.event.target).addClass('e-currentitem');
		var obj = $("#sliderContent").ejRotator("instance").gotoIndex(args.currentPage);
		if(args.currentPage >1){
		    $('.e-first.e-icon').removeClass('e-firstpagedisabled e-disable')
			$('.e-prev.e-icon').removeClass('e-prevpagedisabled e-disable')
		}
		else
			{
			$('.e-first.e-icon').addClass('e-firstpagedisabled e-disable')
			$('.e-prev.e-icon').addClass('e-prevpagedisabled e-disable')
		}
		if(args.currentPage >=3){
		$('.e-lastpage.e-icon').addClass('e-lastpagedisabled e-disable')
		$('.e-nextpage.e-icon').addClass('e-nextpagedisabled e-disable')
		}
		else{
		$('.e-lastpage.e-icon').removeClass('e-lastpagedisabled e-disable')
		$('.e-nextpage.e-icon').removeClass('e-nextpagedisabled e-disable')
		}
	}
		
		
    </script>
    <style type="text/css" class="cssStyles">
        .frame {
            width: 600px;
        }
        #sliderContent > li .image {
            width:600px;
            height:350px;
        }
    </style>
	
	{% endhighlight %}


### refreshPager()
{:#methods:refreshpager}

`refreshPager()` helps to refresh the model value of pager control.

#### Example

{% highlight html %}
 
<div id="pager"></div> 
 
<script>
$('#pager').ejpager();
var pgObj = $("#pager").data("ejpager");
pgObj.refreshPager(); 
</script>

{% endhighlight %}



## Events

### click
{:#events:click}

Triggered when pager numeric item is clicked in pager control.

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when pager click event is triggered.
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentPage{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the current page index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the pager model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current action event type and its target.</td>
</tr>

</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}
<div id="pager"></div> 
<script>
$("#pager").ejPager({
   click: function (args) {}
});
</script>{% endhighlight %}
