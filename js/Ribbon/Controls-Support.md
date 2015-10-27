---
layout: post
title: Controls-Support
description: controls support
platform: js
control: Ribbon
documentation: ug
---

# Controls Support

In **Ribbon** control, Button,SplitButton,DropDownList Toggle button,Custom controls provide support to the groups.

* **type** property is used to define the controls.
* **ej.Ribbon.type.splitButton**-to add Split button control.
* **ej.Ribbon.type.button**-to add Button control.
* **ej.Ribbon.type.dropDownList**-to add Dropdown List control.
* **ej.Ribbon.type.toggleButton**-to add Toggle button control.
* **ej.Ribbon.type.custom**-to add custom controls.

The default type is **button**.

{% highlight html %}

	<!-- ... -->
	<head>
	</head>
	<!-- ... -->
	<body>
	   <div id="Ribbon"></div>
	   <ul id="menu">
	      <li>
	         <a>FILE</a>
	         <ul>
	            <li><a>New</a></li>
	         </ul>
	      </li>
	   </ul>
	   <ul id="split">
	      <li><span>Paste</span></li>
	   </ul>
	   <input id="fontcolor"/>
	   <script type="text/javascript">
			var fontfamily = [{
			    value: 1,
			    text: "Segoe UI"
			}, {
			    value: 2,
			    text: "Arial"
			}, {
			    value: 3,
			    text: "Times New Roman"
			}, {
			    value: 4,
			    text: "Tahoma"
			}, {
			    value: 5,
			    text: "Helvetica"
			}];
			$(function() {
			    $("#Ribbon").ejRibbon({
			        width: 800,
			        applicationTab: {
			            type: "ApplicationMenu",
			            menuItemID: "menu",
			            menuSettings: {
			                openOnClick: false
			            }
			        },
			        tabs: [{
			            id: "home",
			            text: "HOME",
			            groups: [{
			                text: "SplitButton",
			                alignType: ej.Ribbon.alignType.columns,
			                content: [{
			                    groups: [{
			                        id: "paste",
			                        text: "paste",
			                        toolTip: "Paste",
			                        type: ej.Ribbon.type.splitButton,
			                        splitButtonSettings: {
			                            contentType: ej.ContentType.ImageOnly,
			                            targetID: "split",
			                            prefixIcon: "e-ribbon e-ribbonpaste",
			                            buttonMode: "dropdown",
			                            arrowPosition: "bottom"
			                        }
			                    }],
			                    defaults: {
			                        type: ej.Ribbon.type.splitButton,
			                        width: 50,
			                        height: 70
			                    }
			                }]
			            }, {
			                text: "Dropdown List",
			                alignType: ej.Ribbon.alignType.rows,
			                content: [{
			                    groups: [{
			                        id: "fontfamily",
			                        toolTip: "Font",
			                        type: ej.Ribbon.type.dropDownList,
			                        dropdownSettings: {
			                            dataSource: fontfamily,
			                            value: "1",
			                            width: 150
			                        }
			                    }]
			                }]
			            }, {
			                text: "Custom",
			                alignType: ej.Ribbon.alignType.rows,
			                content: [{
			                    groups: [{
			                        id: "fontcolor",
			                        text: "Font Color",
			                        toolTip: "Font Color",
			                        type: ej.Ribbon.type.custom,
			                        contentID: "fontcolor"
			                    }]
			                }]
			            }, {
			                text: "Button",
			                alignType: ej.Ribbon.alignType.rows,
			                content: [{
			                    groups: [{
			                        id: "undo",
			                        text: "Undo",
			                        toolTip: "Undo",
			                        buttonSettings: {
			                            contentType: ej.ContentType.TextAndImage,
			                            imagePosition: ej.ImagePosition.ImageTop,
			                            prefixIcon: "e-ribbon e-undo",
			                            click: "executeAction"
			                        }
			                    }],
			                    defaults: {
			                        type: ej.Ribbon.type.button,
			                        width: 40,
			                        height: 70
			                    }
			                }]
			            }, {
			                text: "Toggle",
			                alignType: ej.Ribbon.alignType.columns,
			                content: [{
			                    groups: [{
			                        id: "bold",
			                        toolTip: "Bold",
			                        type: ej.Ribbon.type.toggleButton,
			                        toggleButtonSettings: {
			                            contentType: ej.ContentType.ImageOnly,
			                            defaultText: "Bold",
			                            activeText: "Bold",
			                            defaultPrefixIcon: "e-ribbon bold",
			                            activePrefixIcon: "e-ribbon bold",
			                            click: "executeAction"
			                        }
			                    }],
			                    defaults: {
			                        width: 40,
			                        height: 70
			                    }
			                }]
			            }]
			        }],
			        create: "createControl",
			    });
			});
			
			function createControl(args) {
			    $("#fontcolor").ejColorPicker({
			        value: "#FFFF00",
			        modelType: "palette",
			        cssClass: "e-ribbon",
			        toolIcon: "e-icon e-fontcoloricon"
			    });
			}
	   </script>
	   <style>
	      .e-ribbon .e-ribbonpaste:before {
	      content: "\e645";
	      font-size: 36px;
	      position: relative;
	      left: -9px;
	      top: -4px;
	      font-family:"ej-webfont";
	      }
	      .e-ribbon .e-undo:before {
	      content: "\e736";
	      font-size: 28px;
	      position: relative;
	      left: -2px;
	      top: 2px;
	      font-family:"ej-webfont";
	      }
	      .e-ribbon .bold:before {
	      content: "\e636";
	      font-family:"ej-webfont";
	      }
	      .e-ribbon .e-fontcoloricon:before {
	      content: "\e632";
	      font-size: 15px;
	      position: relative;    
	      right: -1px;
	      top: -9px;
	      font-family:"ej-webfont";
	      }
	   </style>
	</body>
	<!-- ... -->
	
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](/js/Ribbon/Controls-Support_images/Controls-Support_img1.png)

