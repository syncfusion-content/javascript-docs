---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: DropDownList
documentation: ug
---

# Behavior Settings

The following are some miscellaneous properties that helps you to change the behavior of **DropdownList** control 

**Target ID**

You can append a list with dropdown textbox by using **targetID** property. You need to define a &lt;ul&gt;, &lt; li&gt; tag that you want to show on **Dropdown List** and then set the id of parent &lt;ul&gt; tag to **targetID** property. Its data type is string. 

The following steps explains you the configuration of **targetID** property in Dropdownlist

In an HTML page, add a &lt;input&gt; element to configure Dropdownlist widget

{% highlight html %}

         <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>
       </div>

{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list"
            });
        });

{% endhighlight %}

**Number of items in the list**

**Dropdown** widget provides you support to customize the items visible on popup visible. The **itemsCount** property defines the number of items that is displayed on **DropdownList** . Its data type is number.

The following steps explains you the configuration of **itemsCount** property in **DropdownList**

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

    <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                itemsCount: 3                
            });
        });

{% endhighlight %}

Output of the above steps

{% include image.html url="/js/DropDownList/Behaviour-Settings_images/Behaviour-Settings_img1.png" Caption="Dropdown with itemsCount property"%}

**Select the value by index** 

Dropdown widget provides you support to select an item by mentioning the index of the item. The **selectedItemIndex** property helps you to select the particular item from the list. Its date type is number. 

The following steps explains you the configuration of **selectedItemIndex** property in **DropdownList**

 In an HTML page, add a &lt;input&gt; element to configure DropdownList  widget

{% highlight html %}

         <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>

        </div>


{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",                
                selectedItemIndex: 1                
            });
        });

{% endhighlight %}

Output of the above steps


{% include image.html url="/js/DropDownList/Behaviour-Settings_images/Behaviour-Settings_img2.png" Caption="Dropdown with selecteditemindex property"%}

**Show Popup on load**

You can display the popup panel when page load itself using **showPopupOnLoad** property. Its data type is Boolean. 

The following steps explains you the configuration of **showPopupOnLoad** property in **DropdownList**

 In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

         <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>
        </div>


{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                showPopupOnLoad: true
            });
        });
{% endhighlight %}

**Multiple selection through index** 

You can select the list of items from the **DropdownList** using **selectedItems** property. Its data type is array. To achieve this, you need to set true to **checkbox** property in **DropdownList** . 

The following steps explains you the configuration of **selectedItems** property in **DropdownList**

 In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

      <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>

        </div>

{% endhighlight %}

{% highlight js %}
 
           // Initialize the control in JavaScript     
           $('#dropdownlist').ejDropDownList({
                targetID: "list",
                selectedItems: [0, 1],
                showCheckbox:true

            });

{% endhighlight %}

Output of the above steps

{% include image.html url="/js/DropDownList/Behaviour-Settings_images/Behaviour-Settings_img3.png" Caption="Dropdown with selecteditems property"%}

**Read-only**

This feature supports to make the dropdown as readable. That is, you can make the dropdown as editable or non-editable by setting Boolean type value to **readOnly** property.

The following steps explains you the configuration of **readOnly** property in **DropdownList**.

 In an HTML page, add a &lt;input&gt; element to configure DropdownList widget


{% highlight html %}


     <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>

       </div>

{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                readOnly: true
            });
        });

{% endhighlight %}

**Enable or Disable the Dropdown Widget**

This features enables you to set the enable or disable options for dropdown by setting Boolean type value to **enabled** property. 

The following steps explains you the configuration of **enabled** property in **DropdownList** .

 In an HTML page, add a &lt;input&gt; element to configure DropdownList widget.


{% highlight html %}

     <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>

       </div>

{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript      
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                enabled: false
            });
        });

{% endhighlight %}

Output of the above steps 


{% include image.html url="/js/DropDownList/Behaviour-Settings_images/Behaviour-Settings_img4.png" Caption="Dropdown with enable property"%}

**Persistence support** 

This features enables you to save current model value to browser cookies for state maintains. When you refresh the **DropDownList** control page, it retains the model value apply from browser cookies. The date type of **enablePersistence** is Boolean type. 

The following steps explains you the configuration of **enablePersistence** property in DropdownList

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget


{% highlight html %}

     <input type="text" id="dropdownlist" />

        <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
                <li>Science</li>
            </ul>
        </div>

{% endhighlight %}

{% highlight js %}
  
        // Initialize the control in JavaScript    
        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                enablePersistence: true
            });
        });	


{% endhighlight %}
