---
layout: post
title: Behavior-settings
description: behavior settings
platform: js
control: Toolbar
documentation: ug
api: /api/js/ejtoolbar
---

# Behavior settings

The following are some miscellaneous properties that enables you to change the behavior of **Toolbar** control.

## Enabling Toolbar

The **Toolbar** property [enabled](https://help.syncfusion.com/api/js/ejtoolbar#members:enabled) is used to enable or disable the **Toolbar**. Set the value to this property as **Boolean** type.

{% highlight html %}

<div class="cols-sample-area">
   <div id="toolbar">
      <ul>
         <li id="Left" title="Left">
            <div class="ToolbarItems LeftAlign_tool"></div>
         </li>
         <li id="Center" title="Center">
            <div class="ToolbarItems CenterAlign_tool"></div>
         </li>
         <li id="Right" title="Right">
            <div class="ToolbarItems RightAlign_tool"></div>
         </li>
         <li id="Justify" title="Justify">
            <div class="ToolbarItems Justify_tool"></div>
         </li>
      </ul>
      <ul>
         <li id="Bold" title="Bold">
            <div class="ToolbarItems Bold_tool"></div>
         </li>
         <li id="Italic" title="Italic">
            <div class="ToolbarItems Italic_tool"></div>
         </li>
         <li id="StrikeThrough" title="Strike Through">
            <div class="ToolbarItems StrikeThrough_tool"></div>
         </li>
         <li id="UndeLine" title="UnderLine">
            <div class="ToolbarItems Underline_tool"></div>
         </li>
      </ul>
   </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        // declaration
        $("#toolbar").ejToolbar({ enabled: true });
    });

{% endhighlight %}

{% highlight css %}

<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}

## Hiding Toolbar 

The **Toolbar** property [hide](https://help.syncfusion.com/api/js/ejtoolbar#members:hide) is used to show or hide the **Toolbar**. Set the value to this property as **Boolean** type.


{% highlight javascript %}

    $(function () {
        // declaration
        $("#toolbar").ejToolbar({ hide: true });
    });

{% endhighlight %}

## Disable Or Enable Separate Toolbar Item

We can enable or disable a separate toolbar item by using the following methods.

### Disable Item

The **Toolbar** method [disableItem](https://help.syncfusion.com/api/js/ejtoolbar#methods:disableitem) and [disableItemByID](https://help.syncfusion.com/api/js/ejtoolbar#methods:disableitembyid) can be used to disable separate toolbar item. In the below code we have disabled the third toolbar item by using these two methods

{% highlight html %}

    <div class="cols-sample-area">
       <div id="editingToolbar">
            <ul>
                <li id="cut" class="e-icon e-cut_01" title="Cut"></li>
                <li id="copy" class="e-icon e-copy_02" title="Copy"></li>
                <li id="paste" class="e-icon e-paste_01" title="Paste"></li>
            </ul>
            <ul>
                <li id="Bold" class="e-icon e-bold_01" title="Bold"> </li>
                <li id="UndeLine" class="e-icon e-underline_01" title="UnderLine"></li>
                <li id="StrikeThrough" class="e-icon e-strikethrough_01" title="Strike Through"></li>
           </ul>
           <ul>
               <li id="Left" class="e-icon e-align-left_01" title="Left"></li>
               <li id="Center" class="e-icon e-align-center_01" title="Center"></li>
               <li id="Right" class="e-icon e-align-right_01" title="Right"></li>
               <li id="Justify" class="e-icon e-align-justify_01" title="Justify"></li>
            </ul>
       </div>
    </div>

{% endhighlight %}

{% highlight javascript %}
        $(function () {
                    // declaration
                    $("#editingToolbar").ejToolbar();
                   $("#editingToolbar").ejToolbar("disableItem",$("li")[2]);
                    
                });

{% endhighlight %}

OR
{% highlight javascript %}
        $(function () {
                    // declaration
                    $("#editingToolbar").ejToolbar();
                    $("#editingToolbar").ejToolbar("disableItemByID","paste");
                    
                });

{% endhighlight %}


![](Behaviour-settings_images/Behaviour-settings1.jpg)

### Enable Item

The **Toolbar** method [enableItem](https://help.syncfusion.com/api/js/ejtoolbar#methods:enableitem) and [enableItemByID](https://help.syncfusion.com/api/js/ejtoolbar#methods:enableitembyid) can be used to enable separate toolbar item. In the below code we have disabled the first five items initially and enabled the third toolbar item by using these two methods

{% highlight html %}

    <div class="cols-sample-area">
       <div id="editingToolbar">
            <ul>
                <li id="cut" class="e-icon e-cut_01" title="Cut"></li>
                <li id="copy" class="e-icon e-copy_02" title="Copy"></li>
                <li id="paste" class="e-icon e-paste_01" title="Paste"></li>
            </ul>
            <ul>
                <li id="Bold" class="e-icon e-bold_01" title="Bold"> </li>
                <li id="UndeLine" class="e-icon e-underline_01" title="UnderLine"></li>
                <li id="StrikeThrough" class="e-icon e-strikethrough_01" title="Strike Through"></li>
           </ul>
           <ul>
               <li id="Left" class="e-icon e-align-left_01" title="Left"></li>
               <li id="Center" class="e-icon e-align-center_01" title="Center"></li>
               <li id="Right" class="e-icon e-align-right_01" title="Right"></li>
               <li id="Justify" class="e-icon e-align-justify_01" title="Justify"></li>
            </ul>
       </div>
    </div>

{% endhighlight %}

{% highlight javascript %}
        $(function () {
                    // declaration
                   $("#editingToolbar").ejToolbar({disabledItemIndices: [0,1,2,3,4]});
                   $("#editingToolbar").ejToolbar("enableItem",$("li")[2]);
                    
                });

{% endhighlight %}

OR
{% highlight javascript %}
        $(function () {
                    // declaration
                   $("#editingToolbar").ejToolbar({disabledItemIndices: [0,1,2,3,4]});
                    $("#editingToolbar").ejToolbar("enableItemByID","paste");
                    
                });

{% endhighlight %}

![](Behaviour-settings_images/Behaviour-settings2.jpg)