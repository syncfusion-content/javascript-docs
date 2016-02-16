---
layout: post
title:  Resize
description:resize
documentation: ug
platform: js
keywords: resize,ribbon resize
---

# Resize 

Ribbon control dynamically resizes to display possible number of controls in the optimal layout as the application window size changes.

As the window is narrowed, controls in the Ribbon will be combined as group button with dropdown arrow, in which controls can be expanded with dropdown arrow.

## Enable Resizing 

Set [`allowResizing`](http://help.syncfusion.com/js/api/ejribbon#members:allowresizing) as true to enable resizing in Ribbon.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbonmenu">
        <li><a>FILE </a>
            <ul>
                <li><a>New</a></li>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
    <script type="text/javascript">
        $(function () {
            $("#Ribbon").ejRibbon({
                width: "20%",

                // resizing enabled
                allowResizing: true,
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonmenu",
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        content: [{
                            groups: [{
                                id: "cut",
                                text: "Cut"
                            }, {
                                id: "copy",
                                text: "Copy"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }, {
                        text: "Font",
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold"
                            }, {
                                id: "italic",
                                text: "Italic"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }, {
                        text: "Align",
                        content: [{
                            groups: [{
                                id: "left",
                                text: " Left"
                            }, {
                                id: "right",
                                text: "Right"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }]
                }]
            });
        });
    </script>

{% endhighlight %}

![](/js/Ribbon/Resize_images/Resize_img1.png)

## Group Button Customization

Based on window size, detailed group is shrined into single button and you can expand group items with group button click.

For each group shirked for resizing, Custom Class will be added based on group text.ie, `e-action` whereas `action` is group text. Using this custom class, group button can be customized such as to set icons etc.

{% highlight html %}

    <div id="Ribbon"></div>    
    <ul id="ribbonmenu">
        <li>
            <a>FILE</a>
            <ul>
                <li><a>New</a></li>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
    <script type="text/javascript">
        $(function () {
            var fontfamily = ["Segoe UI", "Arial"],
                fontsize = ["1pt", "2pt"];
            $("#Ribbon").ejRibbon({
                width: "36%",

                // resizing enabled
                allowResizing: true,
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonmenu"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        alignType: ej.Ribbon.alignType.columns,
                        enableGroupExpander: true,
                        content: [{
                            groups: [{
                                id: "paste",
                                text: "paste",
                                toolTip: "Paste",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonpaste"
                                }
                            }],
                            defaults: {
                                isBig: true,
                                width: 50,
                                height: 70
                            }
                        }, {
                            groups: [{
                                id: "cut",
                                text: "Cut",
                                toolTip: "Cut",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    prefixIcon: "e-ribbon e-ribboncut"
                                }
                            }, {
                                id: "copy",
                                text: "Copy",
                                toolTip: "Copy",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    prefixIcon: "e-ribbon e-ribboncopy"
                                }
                            }],
                            defaults: {
                                width: 60,
                                height: 40,
                                isBig: false
                            }
                        }]
                    }, {
                        text: "Font",
                        alignType: "rows",
                        content: [{
                            groups: [{
                                id: "fontfamily",
                                toolTip: "Font",
                                dropdownSettings: {
                                    dataSource: fontfamily,
                                    text: "Segoe UI",
                                    width: 150
                                }
                            }, {
                                id: "fontsize",
                                toolTip: "FontSize",
                                dropdownSettings: {
                                    dataSource: fontsize,
                                    text: "1pt",
                                    width: 65
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.type.dropDownList,
                                height: 28,
                                isBig: false,
                            }
                        }]

                    }, {
                        text: "New",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "new",
                                text: "New",
                                toolTip: "New",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-ribbon e-new"
                                }
                            }],
                            defaults: {
                                width: 60,
                                height: 40
                            }
                        }]
                    }, {
                        text: "Actions",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "undo",
                                text: "Undo",
                                toolTip: "Undo",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-ribbon e-undo"
                                }
                            }, {
                                id: "redo",
                                text: "Redo",
                                toolTip: "Redo",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-ribbon e-redo"
                                }
                            }],
                            defaults: {
                                width: 40,
                                height: 70
                            }
                        }]
                    }]
                }, {
                    id: "layout",
                    text: "LAYOUT",
                    groups: [{
                        text: "Print Layout",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "printlayout",
                                text: "Print Layout",
                                toolTip: "Print Layout",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-ribbon e-printlayout"
                                }
                            }],
                            defaults: {
                                width: 80,
                                height: 70
                            }
                        }]
                    }]
                }]
            });
        });
    </script>
    <style type="text/css">
        /*styles set to resize group based on group text custom class*/
        .e-ribbon .e-New:before, .e-ribbon .e-Actions:before {
            font-family: "ej-ribbonfont";
            font-size: 28px;
            line-height: 35px;
        }
        .e-ribbon .e-New:before {
            /*e-New to group “New” */
            content: "\e167";            
            text-indent: -1.5px;
        }
        .e-ribbon .e-Actions:before {
            /*e-Actions to group “Actions”*/
            content: "\e177";
            text-indent: 7px;
        }
    </style>

{% endhighlight %}

![](/js/Ribbon/Resize_images/Resize_img2.png)
