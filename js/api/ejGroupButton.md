---
layout: post
title: Properties, Methods and Events of ejGroupButton Widget
description: API reference for ejGroupButton
documentation: API
platform: js
keywords: GroupButton, ejGroupButton, syncfusion, ejGroupButton api
---

# ejGroupButton

The Essential JavaScript Group Button widget helps to display multiple buttons which are stacked together in a single line and used as a navigation component. Also it manages the checked/unchecked state for a set of buttons, since it supports radio and check button modes. 

#### Syntax

{% highlight javascript %}

$(element).ejGroupButton(options);

{% endhighlight %}


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
options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Settings for GroupButton</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton();
        });
    </script>


{% endhighlight %}


#### Requires


* module:jQuery

* module:ej.core.js

* module:ej.groupbutton.js


## Members




### cssClass `string`
{:#members:cssclass}

Sets the specified class to GroupButton wrapper element, which allows for custom skinning option in ejGroupButton control.


#### Default Value




* ""




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                //set the cssClass during the control initialization
                cssClass:"e-btnColor"
            });
        });
    </script>

{% endhighlight %}


### dataSource `object`
{:#members:datasource}


To set the local JSON data, define a JSON array and initialize the GroupButton with **dataSource** property. Specify the column names in the **fields** property.


#### Default Value 




* null



#### Example


{% highlight html %}

        <div id="groupButton">

        </div>

{% endhighlight %}

{% highlight js %}


        <script>

            $("#groupButton").ejGroupButton({

                groupButtonMode: "radiobutton",

                dataSource: [

                { text: "Day", contentType: "textonly" },

                { text: "Week", contentType: "textonly" },

                { text: "Work Week", contentType: "textonly" },

                { text: "Month", contentType: "textonly", selected: "selected" },

                { text: "Agenda", contentType: "textonly" }],

                showRoundedCorner: true

            });

        </script>

{% endhighlight %}



### enableRTL `boolean`
{:#members:enablertl}


Displays the ejGroupButton in Right to Left direction.


#### Default Value




* false




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                enableRTL: true
            });
        });
    </script>


{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Used to enable or disable the ejGroupButton control.


#### Default Value




* true




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                enabled: false
            });
        });
    </script>
{% endhighlight %}




### fields `object`
{:#members:fields}


Gets or sets a value that indicates to display the values of the data.


### Default value



* null


### fields.contentType `enum|string`


Specifies the content type of the button. Button can have image only, text only, imagetextimage, textandimage, or imageboth as content type.


### fields.htmlAttribute `object`


Specifies the HTML attributes to the element.
 
 
### fields.imagePosition `enum|string`

Specifies the image position in the button. This property is applicable for the content type 'textandimage' only.


### fields.linkAttribute `object`
 
Specifies the link attributes to the element.
 
 
### fields.prefixIcon `string`

Specifies the primary icon for button. This icon will be displayed from the left margin of the button.
 

### fields.selected `boolean`
 
Specifies the button is in selected state.
 

### fields.suffixIcon `string`
 
Specifies the secondary icon for button. This icon will be displayed from the right margin of the button.
 
 
### fields.text `string`
 
Specifies the text in the button.
 
 
### fields.url `string`
 
Specifies the URL of the button for navigation. 

### Example

{% highlight html %}
<script>
$("#groupButton").ejGroupButton({
    groupButtonMode: "radiobutton",
    dataSource: [
    { value: "Day", type: "textonly" },
    { value: "Week", type: "textonly" },
    { value: "Work Week", type: "textonly" },
    { value: "Month", type: "textonly", selected: "selected" },
    { value: "Agenda", type: "textonly" }],
    fields : { contentType :"type", text:"value", selected: "selected" }
  });
 </script>     
{% endhighlight %}

### groupButtonMode `enum | string`
{:#members:groupbuttonmode}

<ts name="ej.GroupButtonMode"/>

Sets the GroupButton behavior to works as Checkbox mode/ radio button mode based on the specified option.

<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>

<td class="name">
CheckBox</td>
<td class="description">Sets the GroupButton to work as checkbox mode </td>
</tr>
<tr>
<td class="name">
RadioButton</td>
<td class="description">Sets the RadioButton to work as radio button mode  </td>
</tr>

</tbody>
</table>


#### Default Value




* ej.GroupButtonMode.RadioButton




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                groupButtonMode: ej.GroupButtonMode.RadioButton
            });
        });
    </script>
                                


{% endhighlight %}




### height `string | number`
{:#members:height}




Used to sets the height of the ejGroupButton control.


#### Default Value




* 28




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                height:40
            });
        });
    </script>

 
{% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}




Defines the characteristics of the ejGroupButton control and extend the capability of an HTML element by adding specified attributes to element tag and by performing the related actions


#### Default Value




* {}




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                htmlAttributes: { title: "Group Button" }
            });
        });
    </script>

{% endhighlight %}




### orientation `enum`
{:#members:orientation}

<ts ref="ej.Orientation"/>

Specify the orientation of the GroupButton. See below to get available orientations 


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Enum for Horizontal Orientation</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Enum for Vertical Orientation</td>
</tr>
</tbody>
</table>

#### Default Value




* ej.Orientation.Horizontal 




#### Example



{% highlight html %}
 

    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                orientation: ej.Orientation.Vertical
            });
        });
    </script>


{% endhighlight %}




### query `Object`
{:#members:query}

Query the dataSource from the table for Groupbutton

#### Default Value:
{:.param}

* null


{% highlight js %}

        <script>

            var dataManger = ej.DataManager({

                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"

            });

            // Query creation

            var query = ej.Query().from("Orders").take(6);

            $(function () {

                //  declaration 

                $("#groupButton").ejGroupButton({

                    dataSource: dataManger,

                    fields: { text: "CustomerID" },

                    query: query,

                });

            });

        </script>

{% endhighlight %}



### selectedItemIndex `number[] | string[]`
{:#members:selecteditemindex}




Sets the list of button elements to be selected. To enable this option groupButtonMode should be in “checkbox” mode.


#### Default Value




* []




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                groupButtonMode: "checkbox",
                selectedItemIndex :["1","2"]
            });
        });
    </script>


{% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Sets the rounder corner to the GroupButton, if sets as true.


#### Default Value




* false




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                showRoundedCorner: true
            });
        });
    </script>
             


{% endhighlight %}



### size `enum | string`
{:#members:size}

<ts ref="ej.ButtonSize" />


Specifies the size of the button. See available [size](http://help.syncfusion.com/js/api/ejbutton#members:size)


#### Default Value




* ej.ButtonSize.Normal




#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                size: ej.ButtonSize.Large
            });
        });
    </script>
{% endhighlight %}


### width `string | number`
{:#members:width}


Defines the width of the ejGroupButton control.


#### Default Value



* ""



#### Example



{% highlight html %}
 

    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>

    <script type="text/javascript">
        $(function () {           
            //  declaration 
            $("#groupButton").ejGroupButton({
                width: "100%"
            });
        });
    </script>

{% endhighlight %}



## Methods


### deselectItem(element)
{:#methods:deselectitem}




Remove the selection state of the specified the button element from the GroupButton

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}
 
    <div id="groupButton">
        <ul>
            <li>Day</li>
            <li>Week</li>
            <li>Month</li>
        </ul>
    </div>
    <script type="text/javascript">
        var grpBtnObj;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            grpBtnObj.deselectItem(getSelectedItem());
        });
    </script>
{% endhighlight %}


### destroy()
{:#methods:destroy}




Destroy the GroupButton widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        <script>
        // Create Button
                    $("#groupButton").ejGroupButton();
                    grpBtnObj = $("#groupButton").ejGroupButton('instance');
                    grpBtnObj.destroy(); // destroy the GroupButton
        </script>

{% endhighlight %}


{% highlight html %}

 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
    
        <script>
            // destroy the button
            $("#groupButton").ejGroupButton();
            $("#groupButton").ejGroupButton("destroy");      
        </script>

{% endhighlight %}




### disable()
{:#methods:disable}




Disables the GroupButton control



#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
 
        <script type="text/javascript">
            var grpBtnObj;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                grpBtnObj.disable();
            });
        </script>

{% endhighlight %}


{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
    
        <script>
        // disable the button
            $("#groupButton").ejGroupButton();
            $("#groupButton").ejGroupButton("disable");      
        </script>

{% endhighlight %}


### disableItem(element)
{:#methods:disableitem}


Disable the specified button element from the ejGroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}

            <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
            </div>
        
            <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                element = $("#groupButton").find('li')[0];
                grpBtnObj.disableItem(element);
            });
            </script>

{% endhighlight %}

### enable()
{:#methods:enable}




Enables the disabled ejGroupButton control.



#### Example



{% highlight html %}
 
        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
        </div>
        
        <script type="text/javascript">
            var grpBtnObj;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance'); 
                grpBtnObj.enable();
            });
        </script>

{% endhighlight %}


{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        
        <script>
            // enable the button
            $("#groupButton").ejGroupButton();
            $("#groupButton").ejGroupButton("enable");       
        </script>

{% endhighlight %}

### enableItem(element)
{:#methods:enableitem}


Enable the specified disabled button element from the ejGroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}

        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
    
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            element = $("#groupButton").find('li')[0];
            grpBtnObj.enableItem(element);
        });
        </script>

{% endhighlight %}


### getIndex(element)
{:#methods:getindex}


Returns the index value for specified button element in the GroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>

####Returns:
number

#### Example



{% highlight html %}
 
        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
         </div>
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            element = $("#groupButton").find('li')[0];
            grpBtnObj.getIndex(element);
        });
        </script>

{% endhighlight %}


### getSelectedItem(element)
{:#methods:getselecteditem}


This method returns the list of active state button elements from the GroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>

####Returns:
number

#### Example



{% highlight html %}

    <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
     </div>
    
    <script type="text/javascript">
    var grpBtnObj;
    $(function () {           
        //create the instance to the ejGroupButton
        $("#groupButton").ejGroupButton();
        grpBtnObj = $("#groupButton").ejGroupButton('instance');
        grpBtnObj.getSelectedItem();
    });
    </script>


{% endhighlight %}

### hide()
{:#methods:hide}




Hides the GroupButton control



#### Example



{% highlight html %}
 
        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
         </div>
         
         
        <script type="text/javascript">
            var grpBtnObj;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                grpBtnObj.hide();
            });
        </script>


{% endhighlight %}


{% highlight html %}
 
        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
        </div>
        
        <script>
            // hide the button
            $("#groupButton").ejGroupButton();
            $("#groupButton").ejGroupButton("hide");      
        </script>

{% endhighlight %}

### hideItem(element)
{:#methods:hideitem}


Hide the specified button element from the ejGroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            element = $("#groupButton").find('li')[0];
            grpBtnObj.hideItem(element);
        });
        </script>

{% endhighlight %}


### isDisabled()
{:#methods:isdisabled}




Returns the disabled state of the specified element button element in GroupButton as Boolean.

####Returns

Boolean

#### Example



{% highlight html %}

        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
        </div>
        
        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                element = $("#groupButton").find('li')[0];
                grpBtnObj.isDisabled(element);
            });
        </script>

{% endhighlight %}



### isSelected()
{:#methods:isselected}




Returns the state of the specified button element as Boolean.

####Returns 

Boolean

#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>

        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                element = $("#groupButton").find('li')[0];
                grpBtnObj.isSelected(element);
            });
        </script>


{% endhighlight %}


### selectItem(element)
{:#methods:selectitem}


Public method used to select the specified button element from the ejGroupButton control.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            element = $("#groupButton").find('li')[0];
            grpBtnObj.selectItem(element);
        });
        </script>


{% endhighlight %}


### show()
{:#methods:show}




Shows the GroupButton control, if its hide.



#### Example



{% highlight html %}

        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
            </div>
        
        <script type="text/javascript">
            var grpBtnObj;
            $(function () {           
                //create the instance to the ejGroupButton
                $("#groupButton").ejGroupButton();
                grpBtnObj = $("#groupButton").ejGroupButton('instance');
                grpBtnObj.show();
            });
        </script>


{% endhighlight %}


{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
 
        <script>
            // shows  the button
            $("#groupButton").ejGroupButton();
            $("#groupButton").ejGroupButton("show");      
        </script>

{% endhighlight %}

### showItem(element)
{:#methods:showitem}


Show the specified hidden button element from the ejGroupButton control. 

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
element</td><td>
jQuery</td><td>
Specific button element</td></tr>
</table>



#### Example



{% highlight html %}

        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
    
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the instance to the ejGroupButton
            $("#groupButton").ejGroupButton();
            grpBtnObj = $("#groupButton").ejGroupButton('instance');
            element = $("#groupButton").find('li')[0];
            grpBtnObj.showItem(element);
        });
        </script>

{% endhighlight %}

## Events




### beforeSelect
{:#events:beforeselect}




Triggered before any button element in the GroupButton get selected.

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
                    argument
                </td>
                <td class="type"><span class="param-type">Object</span></td>
                <td class="description">
                    Event parameters from button
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
                                    disabled
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the button element is disabled or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    element
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Returns the selection button element.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    event
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Event object</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    id
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">Return the button element ID.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    index
                                </td>
                                <td class="type"><span class="param-type">number</span></td>
                                <td class="description">Button item index.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    model
                                </td>
                                <td class="type"><ts ref="ej.GroupButton.Model"/><span class="param-type">object</span> </td>
                                <td class="description">returns the button model</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    selected
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the button element is selected or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    type
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">returns the name of the event</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    status
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">return the button state</td>
                            </tr>
                        </tbody>
                    </table>
                </td>
            </tr>
        </tbody>
        </table>


#### Example



{% highlight html %}

        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
    
        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the the ejGroupButton
                $("#groupButton").ejGroupButton({
                    beforeSelect: function (args) { }
                });        
            });
        </script>
    
{% endhighlight %}




### create
{:#events:create}




Fires after GroupButton control is created.If the user want to perform any operation after the button control creation then the user can make use of this create event.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="type"><ts ref="ej.GroupButton.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the GroupButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the the ejGroupButton
                $("#groupButton").ejGroupButton({
                    create: function (args) { }
                });        
            });
        </script>

{% endhighlight %}




### destroy
{:#events:destroy}




Fires when the GroupButton is destroyed successfully.If the user want to perform any operation after the destroy button control then the user can make use of this destroy event.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from GroupButton
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
<td class="type"><ts ref="ej.GroupButton.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the GroupButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}

        <div id="groupButton">
                <ul>
                    <li>Day</li>
                    <li>Week</li>
                    <li>Month</li>
                </ul>
            </div>
        
        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the the ejGroupButton
                $("#groupButton").ejGroupButton({
                    destroy: function (args) { }
                });        
            });
        </script>
        
{% endhighlight %}


### keyPress
{:#events:keypress}




Triggered once the key is pressed, when the control is in focused state.


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
                    argument
                </td>
                <td class="type"><span class="param-type">Object</span></td>
                <td class="description">
                    Event parameters from button
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
                                    disabled
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the button element is disabled or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    element
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Returns the selection button element.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    event
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Event object</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    id
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">Return the button element ID.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    index
                                </td>
                                <td class="type"><span class="param-type">number</span></td>
                                <td class="description">Button item index.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    model
                                </td>
                                <td class="type"><ts ref="ej.GroupButton.Model"/><span class="param-type">object</span></td>
                                <td class="description">returns the button model</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    selected
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the button element is selected or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    type
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">returns the name of the event</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    status
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">return the button state</td>
                            </tr>
        </tbody>
                    </table>
                </td>
            </tr>
        </tbody>
        </table>



#### Example



{% highlight html %}

        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        <script type="text/javascript">
            var grpBtnObj, element;
            $(function () {           
                //create the the ejGroupButton
                $("#groupButton").ejGroupButton({
                    keyPress: function (args) { }
                });        
            });
        </script>

{% endhighlight %}



### select
{:#events:select}




Triggered when the button element get selected.


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
                    argument
                </td>
                <td class="type"><span class="param-type">Object</span></td>
                <td class="description">
                    Event parameters from button
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
                                    disabled
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the selected button element is disabled or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    element
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Returns the selection button element.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    event
                                </td>
                                <td class="type"><span class="param-type">object</span></td>
                                <td class="description">Event object</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    id
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">Return the selected button element ID.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    index
                                </td>
                                <td class="type"><span class="param-type">number</span></td>
                                <td class="description">Selected button item index.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    model
                                </td>
                                <td class="type"><ts ref="ej.GroupButton.Model"/><span class="param-type">object</span></td>
                                <td class="description">returns the button model</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    selected
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">Boolean value based on whether the button element is selected or not.</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    type
                                </td>
                                <td class="type"><span class="param-type">string</span></td>
                                <td class="description">returns the name of the event</td>
                            </tr>
                            <tr>
                                <td class="name">
                                    status
                                </td>
                                <td class="type"><span class="param-type">boolean</span></td>
                                <td class="description">return the button state</td>
                            </tr>
                         </tbody>
                    </table>
                </td>
            </tr>
        </tbody>
        </table>



#### Example



{% highlight html %}
 
        <div id="groupButton">
            <ul>
                <li>Day</li>
                <li>Week</li>
                <li>Month</li>
            </ul>
        </div>
        
        
        <script type="text/javascript">
        var grpBtnObj, element;
        $(function () {           
            //create the the ejGroupButton
            $("#groupButton").ejGroupButton({
                select: function (args) { }
            });        
        });
        </script>


{% endhighlight %}