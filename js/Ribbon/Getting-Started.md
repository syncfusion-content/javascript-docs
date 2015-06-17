---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Ribbon
documentation: ug
---

# Getting Started

This section explains briefly how to create a **Ribbon** in your application with **JavaScript**.

## Create your Ribbon in JavaScript

The **Ribbon** can be easily configured to the DOM element such as **&lt;div&gt;**. You can create a **Ribbon** with a highly customizable look and feel. The Ribbon control displays the controls in multiple tabs. This section explains the ribbon tabs, adding controls to the groups, expand/collapse ribbon option, and the control separator.

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img1.png" Caption="Ribbon control with tabs and contextual tab"%}

### Create Ribbon Control

1. Create a HTML file and add the following references to the required libraries.

{% highlight html %}


	<!doctype html>
	<html>
	<head>
	<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
	<!-- style sheet for default theme(flat azure) -->
	
	<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
	
	<!--scripts-->
	
	<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js](http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js)">
	</script>
	
	<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.js)"></script>
	
	<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js](http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js)">
	</script>
	
	<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
	</head>
	<body>
	</body>
	</html>


{% endhighlight %}



2. Add a **&lt;div&gt;** element. It is a container for **ejRibbon**.

{% highlight html %}

	<!-- ... -->
	<body>
	<div id="Ribbon"></div>
	</body>
	<!-- ... -->
	
	
	{% endhighlight %}



3. Create the **ejRibbon** widget as follows. The width property allows you to define the width to the Ribbon. In applicationTab definition, the **itemID** property allows you to specify the ID of the ul list to create the application menu. In tabs definition, the groups property allows you to create one or more groups in the tab. In **contextualTabs** definition, the **backgroundColor** property allows you to define the background color of the contextual tab and **borderColor** property allows you to define the border color of the contextual tab.


	{% highlight html %}
	
	
	<!-- ... -->
	<head>
	</head>
	<!-- ... -->
	<body>
	<div id="Ribbon"></div>
	<ul id="menu">
	<li><a>FILE</a>
	<ul>
	<li><a>New</a></li>
	<li><a>Open</a></li>
	</ul>
	</li>
	</ul>
	<div id="ribbonContent">Ribbon control</div>
	<div id="inserttab">Insert Tab</div>
	<div id="designtab">Design Tab</div>
	
	<script type="text/javascript">
	$(function () {
	$("#Ribbon").ejRibbon({
	width: "500px",
	applicationTab: { Type: "ApplicationMenu", itemID: "menu", menuSettings: { openOnClick: false } },
	tabs: [{
	id: "home", text: "HOME", groups: [{
	text: "New",type: "custom", contentID: "ribbonContent"
	}]
	},
	{
	id: "Calculator", text: "CALCULATOR", groups: [{
	text: "Numbers",type: "custom", contentID: "inserttab"
	}]
	}],
	contextualTabs:
	[{
	backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
	tabs: [
	{
	id: "Design", text: "DESIGN", groups: [{
	text: "Table Style", type: "custom", contentID: "designtab"
	}
	]
	}]
	}]
	});
	
	});
	</script>
	</body>
	<!-- ... -->
	
	
	{% endhighlight %}

4. The following screenshot illustrates the **Ribbon** control.

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img2.png" Caption="Simple ribbon control with tabs and contextual tab"%}

### Add Controls

Add controls to each **Ribbon** tab by using the property content. You can also add custom controls by using the property **contentID**.The property **alignType** is used to align the groups in row or column order. Syncfusion has provided Button, Split button, DropdownList, Toggle button, Gallery, and Custom controls support in your Ribbon control. 

The default **alignType** is rows.

{% highlight html %}

	<!-- ... -->
	<head>
	</head>
	<!-- ... -->
	<body>
	<div id="Ribbon"></div>
	<ul id="menu">
	<li><a>FILE</a>
	<ul>
	<li><a>New</a></li>
	<li><a>Open</a></li>
	</ul>
	</li>
	</ul>
	<div id="Contents"><button id="custom">Custom Control</button></div>
	
	<script type="text/javascript">
	$(function () {
	var fontfamily = [{value:1,text:"Segoe UI"}, {value:2,text:"Arial"}, {value:3,text:"Times New Roman"}, {value:4,text:"Tahoma"}, {value:5,text:"Helvetica"}], fontsize = [{value:1,text:"1pt"},{value:2,text:"2pt"}, {value:3,text:"3pt"}, {value:4,text:"4pt"}, {value:5,text:"5pt"}];
	$("#Ribbon").ejRibbon({
	width: "800px",
	applicationTab: { Type: "ApplicationMenu", itemID: "menu", menuSettings: { openOnClick: false } },
	tabs: [{
	id: "home", text: "HOME", groups: [{
	text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
	groups: [{
	id: "new",
	text: "New",
	toolTip: "New",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	imagePosition: ej.ImagePosition.ImageTop,
	prefixIcon: "e-ribbon e-new",
	click: "executeAction"
	}
	}
	],
	defaults: {
	type: ej.Ribbon.type.button,
	width: 60,
	height: 70
	}
	}]
	},
	{
	text: "Font", alignType: "rows", content: [{
	groups: [{
	id: "fontfamily",
	toolTip: "Font",
	dropdownSettings: {
	dataSource: fontfamily,
	value: 1,
	width: 150
	}
	},
	{
	id: "fontsize",
	toolTip: "FontSize",
	dropdownSettings: {
	dataSource: fontsize,
	value: 1,
	width: 65
	}
	}],
	defaults: {
	type: ej.Ribbon.type.dropDownList,
	height: 28,
	isBig: false,
	}
	},
	{
	groups: [{
	id: "bold",
	text: "bold",
	toolTip: "Bold",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	prefixIcon: "e-ribbon bold"
	}
	},
	{
	id: "italic",
	text: "italic",
	text: "italic",
	toolTip: "Italic",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	prefixIcon: "e-ribbon e-ribbonitalic"
	}
	}],
	defaults: {
	type: ej.Ribbon.type.button,
	isBig: false,
	}
	}]
	},
	{
	text: "CustomControls", type: "custom", contentID: "Contents"
	}]
	}]
	});
	});
	</script>
	<style type="text/css">
	.e-ribbon .e-new:before {
	content: "\e646";
	font-size: 36px;
	position: relative;
	left: -12px;
	top: -4px;
	}
	.e-ribbon .e-ribbonitalic:before {
	content: "\e635";
	}
	
	.e-ribbon .bold:before {
	content: "\e636";
	}
	</style>
	</body>
	<!-- ... -->


{% endhighlight %}



The following screenshot illustrates **Ribbon** with controls.

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img3.png" Caption="Ribbon control with default ribbon controls and custom button control"%}

### Expand/Collapse

The **Ribbon** has **expand/collapse** support. The following screenshot illustrates **Ribbon** in the expanded state,

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img4.png" Caption="Ribbon control in the expanded state"%}





The following screenshot illustrates **Ribbon** in the collapsed state.

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img5.png" Caption="Ribbon control in the collapsed state"%}

### Separator for Controls

The **Ribbon** control has control separator support. Set enableSeparator value to true to enable the separator after a control. **Control separator** supports only row type group.

{% highlight html %}


	<!-- ... -->
	<head>
	</head>
	<!-- ... -->
	<body>
	<div id="Ribbon"></div>
	<ul id="menu">
	<li><a>FILE</a>
	<ul>
	<li><a>New</a></li>
	<li><a>Open</a></li>
	</ul>
	</li>
	</ul>
	<script type="text/javascript">
	$(function () {
	var fontfamily = [{value:1,text:"Segoe UI"}, {value:2,text:"Arial"}, {value:3,text:"Times New Roman"}, {value:4,text:"Tahoma"}, {value:5,text:"Helvetica"}], fontsize = [{value:1,text:"1pt"},{value:2,text:"2pt"}, {value:3,text:"3pt"}, {value:4,text:"4pt"}, {value:5,text:"5pt"}]
	$("#Ribbon").ejRibbon({
	width: "700px",
	applicationTab: { Type: "ApplicationMenu", itemID: "menu", menuSettings: { openOnClick: false } },
	tabs: [{
	id: "home", text: "HOME", groups: [{
	text: "New", alignType: ej.Ribbon.alignType.rows,enableGroupExpander: true, content: [{
	groups: [{
	id: "new",
	text: "New",
	toolTip: "New",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	imagePosition: ej.ImagePosition.ImageTop,
	prefixIcon: "e-ribbon e-new",
	click: "executeAction"
	}
	}
	],
	defaults: {
	type: ej.Ribbon.type.button,
	width: 60,
	height: 70
	}
	}]
	},
	{
	text: "Font", alignType: "rows", content: [{
	groups: [{
	id: "fontfamily",
	toolTip: "Font",
	dropdownSettings: {
	dataSource: fontfamily,
	value:1,
	width: 150
	}
	},
	{
	id: "fontsize",
	toolTip: "FontSize",
	dropdownSettings: {
	dataSource: fontsize,
	value: 1,
	width: 65
	}
	}],
	defaults: {
	type: ej.Ribbon.type.dropDownList,
	height: 28,
	isBig: false,
	}
	},
	{
	groups: [{
	id: "bold",
	text: "bold",
	toolTip: "Bold",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	prefixIcon: "e-ribbon bold"
	}
	},
	{
	id: "italic",
	text: "italic",
	text: "italic",
	toolTip: "Italic",
	enableSeparator: true,
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	prefixIcon: "e-ribbon e-ribbonitalic"
	}
	},
	{
	id: "underline",
	text: "underline",
	text: "underline",
	toolTip: "Underline",
	buttonSettings: {
	contentType: ej.ContentType.ImageOnly,
	prefixIcon: "e-ribbon e-ribbonunderline"
	}
	}],
	defaults: {
	type: ej.Ribbon.type.button,
	isBig: false,
	}
	}]
	}]
	}]
	});
	});
	</script>
	<style type="text/css">
	.e-ribbon .e-new:before {
	content: "\e646";
	font-size: 36px;
	position: relative;
	left: -12px;
	top: -4px;
	}
	.e-ribbon .e-ribbonitalic:before {
	content: "\e635";
	}
	
	.e-ribbon .bold:before {
	content: "\e636";
	}
	.e-ribbon .e-ribbonunderline:before {
	content: "\e634";
	}
	</style>
	</body>
	<!-- ... -->


{% endhighlight %}



The following screenshot illustrates the control separator after the **Italic** Button control.

{% include image.html url="/js/Ribbon/Getting-Started_images/Getting-Started_img6.png" Caption="Ribbon control with control separator"%}

