---
layout: post
title: Group-Expander
description: group expander
platform: js
control: Ribbon
documentation: ug
---

# Group Expander

The **Ribbon** control has group expander support. Set **enableGroupExpander** value to true to enable the group expander for each group in the ribbon tab. The event for group expander is **groupExpand**.

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
	var fontfamily = [{value:1,text:"Segoe UI"}, {value:2,text:"Arial"}, {value:3,text:"Times New Roman"}, {value:4,text:"Tahoma"}, {value:5,text:"Helvetica"}], fontsize = [{value:1,text:"1pt"},{value:2,text:"2pt"}, {value:3,text:"3pt"}, {value:4,text:"4pt"}, {value:5,text:"5pt"}];
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
	});</script>
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
	</body><!-- ... -->


{% endhighlight %}

The following screenshot illustrates the group New with the group expander.

{% include image.html url="/js/Ribbon/Concepts-and-Features/Group-Expander_images/Group-Expander_img1.png" Caption="Ribbon control with the Group expander"%}

