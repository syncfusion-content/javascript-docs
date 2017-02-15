---
layout: post
title: Customization of _addToPersist Array in JS widgets
description: Customization of _addToPersist Array in Syncfusion Essential JS widgets.
platform: js
control: common
documentation: ug
---

## State Maintenance

We have provided the State Maintenance support for Essential JS components.You can sustain the user intractable widget model in browser’s local storage even after form post or browser refresh by defining **enablePersistence** property as true.   

{% highlight javascript %}

//Example

$("#fileExplorer").ejFileExplorer({ 
    path: "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/", 
    ajaxAction:”http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations”, 
    enablePersistence:true  
});

{% endhighlight %}

## Customize the Persistence Properties:

You can customize the **_addToPersist** array to achieve the persistence for needed properties of corresponding component.

Please refer the below code block:

{% highlight javascript %}

//Example

<script type="text/javascript" src="//cdn.syncfusion.com/14.4.0.15/js/web/ej.web.all.min.js "></script> 
 <script> 
 //you can customize it as per your requirement 
 ej.FileExplorer.prototype._addToPersist= ["layout", "selectedFolder", "height", "width"]; 
</script> 

{% endhighlight %}

We have prepared a sample based on that and you can get it from following location. 

[Sample Location](http://jsplayground.syncfusion.com/v2steydg) 
