---
layout: post
title: ejTooltip
description: API reference for ejTooltip
documentation: API
platform: js
keywords: Tooltip, ejTooltip, syncfusion, Tooltip api
---

# ejTooltip
The Tooltip control will display a popup hint when the user hover/click/focus to the element. 

#### Syntax
$(element).ejTooltip(options);

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
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for Tooltip</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
 
    // Creates the Tooltip
    <script>
        $("#test").ejTooltip(
		{
		     content: "JavaScript is the programming language of HTML and the Web."
		});
    </script>

{% endhighlight %}

#### Requires
{:.require}

* module:jQuery
* module:jQuery.easing.1.3.js
* module:ej.core.js

## Members

### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}

Tooltip control can be accessed through the keyboard shortcut keys.

#### Default Value
{:.param}
* true

#### Example
{:.example}

{% highlight html %}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script>
        $("#test").ejTooltip(
		 {
		     content: "JavaScript is the programming language of HTML and the Web.",
		     allowKeyboardNavigation: true
             
		 });
    </script>
    
{% endhighlight %}

### animation `object`
{:#members:animation}

Specifies the animation behavior in  Tooltip. It contains the following sub properties.

<table>
<tr>
<th>
Name<br/><br/></th><th>
Type<br/><br/></th><th>
Default<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
effect<br/><br/></td><td>
Enum<br/><br/></td><td>
None<br/><br/></td><td>
Determines the type of effect. The possible values are fade, slide and none<br/><br/></td></tr>
<tr>
<td>
speed<br/><br/></td><td>
integer <br/><br/></td><td>
0<br/><br/></td><td>
Sets the animation speed in milliseconds.<br/><br/></td></tr>
</table>

### animation.effect `enum`
{:#members:animation-effect}

<ts name="ej.Tooltip.effect"/>

Determines the type of effect.

#### Default Value
{:.param}
* ej.Tooltip.Effect.None

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">None</td>
<td class="description">No animation takes place when showing/hiding the Tooltip</td>
</tr>
<tr>
<td class="name">Slide</td>
<td class="description">Sliding effect takes place when showing/hiding the Tooltip</td>
</tr> 
<tr>
<td class="name">Fade</td>
<td class="description">Fade the Tooltip in and out of visibility.</td>
</tr>
</table>

### animation.speed `number`
{:#members:animation-speed}

Sets the animation speed in milliseconds.

#### Default Value
{:.param}
* 4000

#### Example
{:.example}
{% highlight html %}

    <div class="control">
        
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            animation :{ effect : "slide", speed : 1000}
        });

    </script>

{% endhighlight %}
      
### associate `enum`
{:#members:associate}

<ts name="ej.Tooltip.Associate"/>
    
Sets the position related to target element, window, mouse or (x,y) co-ordinates.

#### Default Value
{:.param}
* ej.Tooltip.Associate.Target

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Target</td>
<td class="description">Sets the position related to target element.</td>
</tr>
<tr>
<td class="name">MouseFollow</td>
<td class="description">Sets the position related to mouse.</td>
</tr> 
<tr>
<td class="name">MouseEnter</td>
<td class="description">Sets the position related to mouse, first entry to the target element.</td>
</tr> 
<tr>
<td class="name">Axis</td>
<td class="description">Sets the position related to (x,y) co-ordinates.</td>
</tr> 
<tr>
<td class="name">Window</td>
<td class="description">Sets the position related to browser window.</td>
</tr> 
</table>

#### Example
{:.example}

{% highlight html %}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a> the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            associate: "mousefollow"
        });

    </script>
    
{% endhighlight %}

And also, absolute positioning via horizontal(x), vertical(y) e.g. A Tooltip at 10px from left and top of the page:

{% highlight html %}
{:.example}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            associate: "axis",
            position :{
               target:{  horizontal : 10, vertical : 10 }
            }
        });

    </script>
    
{% endhighlight %}

### autoCloseTimeout `number`
{:#members:autoclosetimeout}

Specified the delay to hide Tooltip when closeMode is auto.

#### Default Value
{:.param}
* 4000

#### Example
{:.example}
{% highlight html %}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            closeMode: "auto",
            autoCloseTimeout : 5000
            
        });

    </script>
    
{% endhighlight %}

### closeMode `enum`
{:#members:closemode}

<ts name="ej.Tooltip.CloseMode"/>

Specifies the closing behavior of Tooltip popup.

#### Default Value
{:.param}
* ej.Tooltip.CloseMode.None

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Sticky</td>
<td class="description">Enables close button in Tooltip.</td>
</tr>
<tr>
<td class="name">Auto</td>
<td class="description">Sets the delay for Tooltip close</td>
</tr> 
<tr>
<td class="name">None</td>
<td class="description">The Tooltip will be display normally.</td>
</tr> 
</table>

#### Example

{% highlight html %}
{:.example}

        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                closeMode : "sticky"
            });

        </script>
        
{% endhighlight %}


#### Example
{:.example}
{% highlight html %}
 
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                closeMode : "auto"
            });

        </script>
        
{% endhighlight %}

### collision `enum`
{:#members:collision}

<ts name="ej.Tooltip.Collision"/>
    
Sets the Tooltip in alternate position when collision occurs.

#### Default Value
{:.param}
* ej.Tooltip.Collision.FlipFit

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Flip</td>
<td class="description">Flips the Tooltip to the opposite side of the target, if collision is occurs.</td>
</tr>
<tr>
<td class="name">Fit</td>
<td class="description">Shift the Tooltip popup away from the edge of the window(collision side) that means adjacent position.</td>
</tr> 
<tr>
<td class="name">FlipFit</td>
<td class="description">Ensure as much of the element is visible as possible to showcase.</td>
</tr> 
<tr>
<td class="name">None</td>
<td class="description">No collision detection is take place</td>
</tr> 
</table>

#### Example
{:.example}
{% highlight html %}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            collision : "fit"
   
        });

    </script>
    
{% endhighlight %}

#### Example
{:.example}
{% highlight html %}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            collision : "flip"
  
        });

    </script>
    
{% endhighlight %}
        

### containment `string`
{:#members:containment}

Specified the selector for the container element.

#### Default Value
{:.param}
* body

#### Example
{:.example}
{% highlight html %}

    <div class="frame>
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            containment : ".frame"
   
        });

    </script>
    
{% endhighlight %}

### content `string`
{:#members:content}

Specifies the text for Tooltip.

#### Default Value
{:.param}
* null

#### Example

{% highlight html %}
{:.example}

    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script>
        $("#test").ejTooltip(
		 {
		     content: "JavaScript is the programming language of HTML and the Web."
		  
		 });
    </script>
    
{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Sets the root CSS class for Tooltip for the customization.

#### Default Value
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
 
    <head>
        <style>
    		.myStyle{
    			background-color :#d588c3;
    			color : blue;
    			border-color : #4cf522;
    		}
    		.myStyle:before{
    			
    			border-right-color: #4cf522;
    		}
    		.myStyle:after{
    			
    			border-right-color: #d588c3;
    		}
        </style>
    </head>
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    <div>
    <script type="text/javascript">

        $("#test").ejTooltip(
	    {
               content: "JavaScript is the programming language of HTML and the Web.",
                cssClass : "myStyle"
         });
            
     </script>
	
{% endhighlight %}

### enabled `boolean`
{:#members:enabled}

Enables or disables the Tooltip.

#### Default Value
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
 
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                enabled: false
            });

        </script>
    
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Sets the Tooltip direction from right to left.

#### Default Value
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script>
        // Initializes the Tooltip with the enableRTL value specified.
         $("#test").ejTooltip(
		 {
		     content: "JavaScript is the programming language of HTML and the Web.",
             enableRTL: true 
             
		 });
    </script>
    
{% endhighlight %}

### height `string|number`
{:#members:height}

Defines the height of the Tooltip popup.

#### Default Value
{:.param}
* auto

#### Example
{:.example}
{% highlight html %}
 
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                height :"50px"
            });

        </script>
        
{% endhighlight %}


### isBalloon  `boolean`
{:#members:isballoon}

Enables the arrow in Tooltip.

#### Default Value
{:.param}
* true

#### Example
{:.example}
{% highlight html %}
 
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                isBalloon :false
            });

        </script>
        
{% endhighlight %}

### position `object`
{:#members:position}

defines various attributes of the Tooltip position

### position.target `object`
{:#members:position-target}

Sets the Tooltip position against target.

### position.target.horizontal `string|number`
{:#members:position-target-horizontal}

Sets the Tooltip position against target based on horizontal(x) value.

#### Default Value
{:.param}
* center

### position.target.vertical `string|number`
{:#members:position-target-vertical}

Sets the Tooltip position against target based on vertical(y) value.

#### Default Value
{:.param}
* top

### position.stem `object`
{:#members:position-stem}

Sets the arrow position again popup.

### position.stem.horizontal `string`
{:#members:position-stem-horizontal}

Sets the arrow position again popup based on horizontal(x) value

#### Default Value
{:.param}
* center

### position.stem.vertical `string`
{:#members:position-stem-vertical}

Sets the arrow position again popup based on vertical(y) value

#### Default Value
{:.param}
* bottom

#### Example
{:.example}
{% highlight html %}
 
        <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
        </div>
        <script type="text/javascript">

            $("#test").ejTooltip(
            {
                content: "JavaScript is the programming language of HTML and the Web.",
                 position:{
						target :{
							horizontal : "center",
							vertical : "top"
						},
						stem: {
						    horizontal: "center",
						    vertical: "bottom"
						}
					}
            });

        </script>
        
{% endhighlight %}

### showRoundedCorner `boolean`
{:#members:showroundedcorner}

Enables or disables rounded corner.

#### Default Value
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            showRoundedCorner :true
        });

    </script>
        
{% endhighlight %}

### showShadow `boolean`
{:#members:showshadow}

Enables or disables shadow effect.

#### Default Value
{:.param}
* false

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <script type="text/javascript">

        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web.",
            showShadow :true
        });

    </script>
        
{% endhighlight %}

### target `string`
{:#members:target}

Specified a selector for elements, within the container.

#### Default Value
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
 
        <table id="details">
            <tr>
                <th>EmployeeID</th>
                <th>Name</th>
                <th>Designation</th>
            </tr>
            <tr>
                <td>SF6089</td>
                <td><a href="#" class="e-info" title="Peter">Peter</a></td>
                <td>Software Engineer</td>
            </tr>
            <tr>
                <td>SF6073</td>
                <td> <a href="#" class="e-info" title="Joe">Joe </a> </td>
                <td>Tester</td>
            </tr>
            <tr>
                <td>SF6073</td>
                <td> <a href="#"class="e-info" title="Lois"> Lois </a> </td>
                <td>Content Writer</td>
            </tr>
            <tr>
                <td>SF7896</td>
                <td> <a href="#" class="e-info" title="Cleveland"> Cleveland </a> </td>
                <td>Graphics Designer</td>
            </tr>
        </table>

        <script type="text/javascript">

            $("#detail").ejTooltip(
            {
                target: ".e-info"
       
            });

        </script>
        <style>
             table {
                border-collapse: collapse;
                width: 100%;
            }

            th, td {
                text-align: left;
                padding: 8px;
            }
            tr:nth-child(even) {
                background-color: #f2f2f2;
            }

            th {
                background-color: #4CAF50;
                color: white;
            }
        </style>

{% endhighlight %}

### title `string`
{:#members:title}

The title text to be displayed in the Tooltip header.

#### Default Value
{:.param}
* null

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

        $("#test").ejTooltip(
		{
		    content: "JavaScript is the programming language of HTML and the Web.",
		    title : "Header"
		});

    </script>
    
{% endhighlight %}

### trigger `enum`
{:#members:trigger}

<ts name="ej.Tooltip.Trigger"/>
    
Specified the event action to show case the Tooltip.
  
#### Default Value
{:.param}
* ej.Tooltip.Trigger.Hover

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td class="name">Click</td>
<td class="description">The Tooltip to be shown when the target element is clicked.</td>
</tr>
<tr>
<td class="name">Hover</td>
<td class="description">Enables the Tooltip when hover on the target element.</td>
</tr> 
<tr>
<td class="name">Focus</td>
<td class="description">Enables the Tooltip when focus is set to target element.</td>
</tr> 
</table>

The below example will cause the Tooltip to be shown when the target element is clicked.

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

        $("#test").ejTooltip(
		{
		    content: "JavaScript is the programming language of HTML and the Web.",
		    trigger : "click"
		});

    </script>
    
{% endhighlight %}

The below example will cause the Tooltip to be shown when the target element is focused:

#### Example

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

        $("#test").ejTooltip(
		{
		    content: "JavaScript is the programming language of HTML and the Web.",
		    trigger : "focus"
		});

    </script>
    
{% endhighlight %}

### width `string|number`
{:#members:width}

Defines the width of the Tooltip popup.

#### Default Value
{:.param}
* auto

#### Example
{:.example}
{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

        $("#test").ejTooltip(
		{
		    content: "JavaScript is the programming language of HTML and the Web.",
		    width:"100px"
		});

    </script>
    
{% endhighlight %}
 
## Methods

### destroy()
{:#methods:destroy}

Destroys the Tooltip control.

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
     <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    var tipObj =$("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		}).data("ejTooltip");
	    tipObj.destroy();

    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		});
	    $("#test").ejTooltip('destroy');

    </script>
    
{% endhighlight %}

### disable()
{:#methods:disable}

Disables the Tooltip control.

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    var tipObj =$("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		}).data("ejTooltip");
	    tipObj.disable();

    </script>
     
{% endhighlight %}

{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		});
	    $("#test").ejTooltip('disable');

    </script>

{% endhighlight %}

### enable()
{:#methods:enable}

Enables the Tooltip control.

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
     <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    var tipObj =$("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		}).data("ejTooltip");
	    tipObj.enable();

    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		});
	    $("#test").ejTooltip('enable');

    </script>

{% endhighlight %}

### hide([effect],[func])
{:#methods:hide}

Hide the Tooltip popup.

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
<td class="name">effect</td>
<td class="type"> <span class="param-type">string</span></td>
<td class="description"> <span class="optional">optional</span> Determines the type of effect that takes place when hiding the tooltip.</td>
</tr>
<tr>
<td class="name">func</td>
<td class="type"> <span class="param-type"> function </span> </td>
<td class="description"> <span class="optional">optional</span> custom effect takes place when hiding the tooltip.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
     <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    var tipObj =$("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		}).data("ejTooltip");
	    tipObj.hide();

    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		});
	    $("#test").ejTooltip('hide');

    </script>

{% endhighlight %}

{% highlight html %}

    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <button id="open">Hide</button>
 
    // Creates the Tooltip
    <script>
    
        $("#test").ejTooltip(
		{
		     content: "JavaScript is the programming language of HTML and the Web."
		});
        tip = $("#test").data("ejTooltip");
        tip.show();
        
        $("#open").ejButton({
            size: "large",
            showRoundedCorner: true,
            click: "onClick",

        });
      
        function onClick(args){
        	tip = $("#test").data("ejTooltip");
        	tip.hide("myFunc");
        }
        
         function myFunc(args) {
			tip = $("#test").data("ejTooltip");
			$(tip.tooltip).slideDown(200, "easeOutElastic");
        
        }
        
    </script>
    
{% endhighlight %}

### show([target],[effect],[func])
{:#methods:show}

Shows the Tooltip popup for the given target element with the specified effect.

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
<td class="name">effect</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">optional</span> Determines the type of effect that takes place when showing the tooltip.</td>
</tr>
<tr>
<td class="name">func</td>
<td class="type"><span class="param-type">function</span></td>
<td class="description"><span class="optional">optional</span> custom effect takes place when showing the tooltip.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">jQuery</span></td>
<td class="description"><span class="optional">optional</span> Tooltip will be shown for the given element</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Void

#### Example
{:.example}

{% highlight html %}
 
     <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
     </div>

    <script type="text/javascript">

	    var tipObj =$("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		}).data("ejTooltip");
	    tipObj.show();

    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">

	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web."
		});
	    $("#test").ejTooltip('show');

    </script>

{% endhighlight %}

{% highlight html %}

    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <button id="open">Open</button>
 
    // Creates the Tooltip
    <script>
    
        $("#test").ejTooltip(
		{
		     content: "JavaScript is the programming language of HTML and the Web."
		});
        
        $("#open").ejButton({
            size: "large",
            showRoundedCorner: true,
            click: "onClick",

        });
      
        function onClick(args){
        	tip = $("#test").data("ejTooltip");
        	tip.show("myFunc");
        }
        
         function myFunc(args) {
			tip = $("#test").data("ejTooltip");
			$(tip.tooltip).slideDown(200, "easeOutElastic");
        
        }
        
    </script>
    
{% endhighlight %}

{% highlight html %}

    <div class="control">
            TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
    <div class="new">
            JavaScript is a high-level, dynamic, untyped, and <a id="newPosition" href="#"> interpreted </a>programming language.
    </div>
    <button id="open">Re position</button>
 
    // Creates the Tooltip
    <script>
    
        $("#test").ejTooltip(
		{
		     content: "JavaScript is the programming language of HTML and the Web."
		});
        
        $("#open").ejButton({
            size: "large",
            showRoundedCorner: true,
            click: "onClick",

        });
      
        function onClick(args){
        	tip = $("#test").data("ejTooltip");
        	tip.show("#newPosition");
        }
 
    </script>
    
{% endhighlight %}

## Events

### beforeClose 
{:#events:beforeclose}

This event is triggered before the Tooltip widget get closed.

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">
content</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the Tooltip's content</td>
</tr>
</tbody>
</table>


#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            beforeClose: function (args) {
               // do your changes
            }
        });
    </script>
    
 {% endhighlight %}

### beforeOpen
{:#events:beforeopen}


This event is triggered before the Tooltip widget gets open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
content</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the Tooltip's content</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            beforeOpen: function (args) {
               // do your changes
            }
        });
    </script>
    
 {% endhighlight %}
 
### click
{:#events:click}

Fires on clicking to the target element. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event object</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            trigger: "click",
            click: function (args) {
               // do your changes
            }
        });
    </script>

{% endhighlight %}
 
### close
{:#events:close}

This event is triggered after the Tooltip widget is closed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
content</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the Tooltip's content</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            close: function (args) {
               // do your changes
            }
        });
    </script>
    
 {% endhighlight %}
 
### create
{:#events:create}

This event is triggered after the Tooltip is created successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            create: function (args) {
               // do your changes
            }
        });
    </script>
    
 {% endhighlight %}

### destroy
{:#events:destroy}

This event is triggered after the Tooltip widget is destroyed successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            destroy: function (args) {
               // do your changes
            }
        });
    </script>

{% endhighlight %}

### hover
{:#events:hover}

This event is triggered while hovering the target element, when tooltip positioning relates to target element.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event object</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            hover: function (args) {
               // do your changes
            }
        });
    </script>

{% endhighlight %}

### open
{:#events:open}

This event is triggered after the Tooltip is opened.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
content</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the Tooltip's content</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            open: function (args) {
               // do your changes
            }
        });
    </script>
    
 {% endhighlight %}

### tracking
{:#events:tracking}

This event is triggered while hover the target element, when the tooltip positioning is relates to the mouse.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Tooltip model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event object</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>

    <script type="text/javascript">
	    $("#test").ejTooltip(
		{
            content: "JavaScript is the programming language of HTML and the Web.",
            associate :"mouse",
            tracking: function (args) {
               // do your changes
            }
        });
    </script>

{% endhighlight %}





