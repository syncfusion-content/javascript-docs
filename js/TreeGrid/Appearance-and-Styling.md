---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Appearance and Styling

The look and feel of the TreeGrid control can be customized by applying themes.

The following are the available themes in TreeGrid control.

1. Flat Azure                
2. Flat Azure Dark             
3. Flat Lime                             
4. Flat Lime Dark                  
5. Flat Saffron                       
6. Flat Saffron Dark
7. Gradient Azure
8. Gradient Azure Dark
9. Gradient Lime
10. Gradient Lime Dark
11. Gradient Saffron
12. Gradient Saffron Dark
13. Bootstrap

You can apply the theme (Gradient lime) to the TreeGrid control by using the style sheet from the online link as follows.

{% highlight html %}

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">

	<head>

	<title>Getting Started with TreeGrid Control for JavaScript</title>

	<!-- style sheet for default theme(gradient lime) -->
	<link href=" http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet">

	//...	
	</head>
	
</html>

{% endhighlight %}

The following screenshot shows the TreeGrid control with Gradient-lime theme.

![](/js/TreeGrid/Appearance-and-Styling_images/Appearance-and-Styling_img1.png)

## Configuring CSS class

In TreeGrid [`cssClass`](/api/js/ejtreegrid#members:cssclass) property is used to apply different customized styles to multiple TreeGrid controls available in sample page.

The following code example shows how to apply different background color for each TreeGrid control's toolbar element.

{% highlight html %}
    <style>
        .c-class1.e-treegrid .e-toolbar {
            background-color: rgba(169, 45, 45, 0.31);
        }
        .c-class2.e-treegrid .e-toolbar {
            background-color: rgba(0, 128, 0, 0.2);
        }
    </style>
    <div>
        <div id="TreeGridContainer"></div>
    </div>

    <div>
        <div id="TreeGridContainer1"></div>
    </div>
    <script>
    $("#TreeGridContainer").ejTreeGrid({
        //...
        cssClass: "c-class1",
    });

     $("#TreeGridContainer1").ejTreeGrid({
        //...
        cssClass: "c-class2",
    });
    </script>

{% endhighlight %}

The below screenshot shows the output of above code example.

![](/js/TreeGrid/Appearance-and-Styling_images/Appearance-and-Styling_img2.png)

![](/js/TreeGrid/Appearance-and-Styling_images/Appearance-and-Styling_img3.png)
