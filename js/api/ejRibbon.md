---
layout: post
title: Properties, Methods and Events of ejRibbon Widget
description: Members,Methods,Events available in ejRibbon
documentation: API
platform: js
keywords: ribbon, ejRibbon, syncfusion, ribbon api
---

# ejRibbon

The ribbon can be easily configured to the DOM element, such as div. You can create a ribbon with a highly customizable look and feel.

#### Syntax

{% highlight javascript %}

    $(element).ejRibbon();

{% endhighlight %}

#### Example

{% highlight html %}
    
    <div id="Ribbon"></div> 
    
    <script>
    // Create Ribbon
    $('#Ribbon').ejRibbon();         
    </script>

{% endhighlight %}

#### Requires


* module:jQuery
* module:jquery.easing.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.globalize.min.js
* module:ej.dropdownlist.js
* module:ej.button.js
* module:ej.tab.js
* module:ej.splitbutton.js
* module:ej.ribbon.js
* module:ej.menu.js
* module:ej.scroller.js
* module:ej.checkbox.js
* module:ej.togglebutton.js


## Members

### allowResizing `boolean`
{:#members:allowresizing}

Enables the ribbon resize feature.allowResizing is a deprecated property of [`isResponsive`](http://help.syncfusion.com/js/api/ejribbon#members:isresponsive). 

#### Default Value

* false

#### Example

{% highlight html %}
 
    <ul id="ribbonmenu">
        <li>
            <a>FILE </a>
            <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
            </ul>
        </li>
     </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">   
       $(function() {
            $("#Ribbon").ejRibbon({
                width: "100%",
                allowResizing: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "cut",
                                text: "Cut"
                            }, {
                                id: "copy",
                                text: "Copy"
                            }, {
                                id: "paste",
                                text: "Paste"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }, {
                        text: "Font",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold"
                            }, {
                                id: "italic",
                                text: "Italic"
                            }, {
                                id: "underline",
                                text: "Underline"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }, {
                        text: "Alignment",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "left",
                                text: " Left"
                            }, {
                                id: "center",
                                text: "Center"
                            }, {
                                id: "right",
                                text: "Right"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }]
                }]
            });
        });      
    </script>  

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

When set to true, adapts the Ribbon layout to fit the screen size of devices on which it renders.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <ul id="ribbonmenu">
        <li>
            <a>FILE </a>
            <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
            </ul>
        </li>
     </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">   
       $(function() {
            $("#Ribbon").ejRibbon({
                width: "100%",
                isResponsive: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "cut",
                                text: "Cut"
                            }, {
                                id: "copy",
                                text: "Copy"
                            }, {
                                id: "paste",
                                text: "Paste"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }, {
                        text: "Font",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold"
                            }, {
                                id: "italic",
                                text: "Italic"
                            }, {
                                id: "underline",
                                text: "Underline"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }, {
                        text: "Alignment",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "left",
                                text: " Left"
                            }, {
                                id: "center",
                                text: "Center"
                            }, {
                                id: "right",
                                text: "Right"
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 70,
                                width: 75
                            }
                        }]
                    }]
                }]
            });
        });      
    </script>  

{% endhighlight %}

### isMobileOnly `boolean`
{:#members:ismobileonly}

When isMobileOnly is true,its shows in mobile toolbar.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <div id="defaultRibbon"></div>
    <script type="text/javascript">
        $(function () {
            $("#defaultRibbon").ejRibbon({
                width: "100%",
                allowResizing: true,
                groupClick: function (args) {
                    if ($(args.target).hasClass("e-ribGroupContent") && args.targetElement == "resizedGroup")
                        this.goToMainContent();
                },
                tabs: [{
                    id: "home", text: "HOME", groups: [ {
                        text: "Font", alignType: "rows", content: [{
                            groups: [{
                                id: "bold",
                                type: ej.Ribbon.Type.ToggleButton,
                                isMobileOnly: true,
                                toggleButtonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    defaultText: "Bold",
                                    activeText: "Bold",
                                    defaultPrefixIcon: "e-icon e-ribbon e-resbold",
                                    activePrefixIcon: "e-icon e-ribbon e-resbold",
                                    click: "executeAction"
                                }
                            },
                               {
                                   id: "italic",
                                   type: ej.Ribbon.Type.ToggleButton,
                                   isMobileOnly: true,
                                   toggleButtonSettings: {
                                       contentType: ej.ContentType.ImageOnly,
                                       defaultText: "Italic",
                                       activeText: "Italic",
                                       defaultPrefixIcon: "e-icon e-ribbon e-resitalic",
                                       activePrefixIcon: "e-icon e-ribbon e-resitalic",
                                       click: "executeAction"
                                   }
                               },
                               {
                                   id: "underline",
                                   text: "Underline",
                                   type: ej.Ribbon.Type.ToggleButton,
                                   isMobileOnly: true,
                                   toggleButtonSettings: {
                                       contentType: ej.ContentType.ImageOnly,
                                       defaultText: "Underline",
                                       activeText: "Underline",
                                       defaultPrefixIcon: "e-icon e-ribbon e-resunderline",
                                       activePrefixIcon: "e-icon e-ribbon e-resunderline",
                                       click: "executeAction"
                                   }
                               },
                               {
                                   id: "strikethrough",
                                   text: "strikethrough",
                                   isMobileOnly: true,
                                   type: ej.Ribbon.Type.ToggleButton,
                                   toggleButtonSettings: {
                                       contentType: ej.ContentType.ImageOnly,
                                       defaultText: "Strikethrough",
                                       activeText: "Strikethrough",
                                       defaultPrefixIcon: "e-icon e-ribbon strikethrough",
                                       activePrefixIcon: "e-icon e-ribbon strikethrough",
                                       click: "executeAction"
                                   }
                               },
                               {
                                   id: "superscript",
                                   text: "superscript",
                                   isMobileOnly: true,
                                   buttonSettings: {
                                       contentType: ej.ContentType.ImageOnly,
                                       prefixIcon: "e-icon e-ribbon e-superscripticon",
                                       click: "executeAction"
                                   }
                               }
                            ],
                            defaults: {
                                isBig: false
                            }
                        }, ]
                    },
				]
                },
			],
                create: "createControl",
            });
        });
    </script>
    <style>
        .e-ribbon .e-Font:before {
            font-family: 'ej-ribbonfont';
            content: "\e90e";
            top: 7px !important;
            text-indent: -2px;
        }
    </style>

{% endhighlight %}

### buttonDefaults `object`
{:#members:buttondefaults}

Specifies the height, width, enableRTL, showRoundedCorner,enabled,cssClass property to the controls in the ribbon commonly and 
it will work only when those properties are not defined in buttonSettings and content defaults.

#### Default Value:

* object

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script>
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "100%",
            buttonDefaults: {
                width: 50,
                height: 40,
                showRoundedCorner: true
            },
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                                width: 70,
                                height: 50
                            }
                        }]
                    }]
                }]
            }]
        });
    });
    </script>

{% endhighlight %}

### showQAT `boolean`  
{:#members:showqat}

Property to enable the ribbon quick access toolbar.

#### Default Value:

* false

#### Example

{% highlight html %}

    <ul id="ribbonmenu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">   
        $(function () {
            $("#Ribbon").ejRibbon({
                width: "100%",
                showQAT: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Font",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon bold"
                                }
                            }, {
                                id: "italic",
                                text: "Italic",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonitalic"
                                }
                            }, {
                                id: "underline",
                                text: "Underline",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonunderline"
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 30
                            }
                        }]
                    }]
                }]
            });
        });
</script>

{% endhighlight %}

### collapsePinSettings `object`
{:#members:collapsepinsettings}

Sets custom setting to the collapsible pin in the ribbon.

#### Default Value:

* Object

#### Example

{% highlight html %}

      <div id="defaultRibbon"></div>
      <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
         </ul>
        <script>
            $(function() {
            $("#defaultRibbon").ejRibbon({
                width: "100%",
                collapsePinSettings: {
                    toolTip: "Pin the Ribbon"
                },
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "New",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
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
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                width: 60,
                                height: 70
                            }
                        }]
                    }]
                }],
            });
        });
      </script>
  
{% endhighlight %}

### collapsePinSettings.toolTip `string` 
{:#members:collapsepinsettings-tooltip}

Sets tooltip for the collapse pin .

#### Default Value:

* null

#### Example

{% highlight html %}
      
     <div id="defaultRibbon"></div>
     <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
     </ul>
     <script>
        $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            collapsePinSettings: {
                toolTip: "Pin the Ribbon"
            },
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
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
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }],
    
        });
    });
    </script>

{% endhighlight %}

### collapsePinSettings.customToolTip  `object` 
{:#members:collapsepinsettings-customtooltip }

Specifies the custom tooltip for collapse pin.Refer to ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.

#### Default Value:

* Object

#### Example

{% highlight html %}
   
      <div id="defaultRibbon"></div>
      <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
       </ul>
    <script>
    $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            collapsePinSettings:{
                        customToolTip:{
                        title: "Pin the Ribbon",
                        content: "<h6>Keep it open while you work</h6>"
                        }
                    },	
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
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
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }],
    
        });
    });
    </script>

{% endhighlight %}

### enableRTL `object`
{:#members:enablertl}

Align content in the ribbon control from right to left by setting the property as true.

#### Default Value:

* false

#### Example

{% highlight html %}
   
    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
    <li><a>ملف</a>
        <ul>
            <li><a>جديد</a></li>
            <li><a>فتح</a></li>
            <li><a>حفظ</a></li>
        </ul>
    </li>
    </ul>
    <script type="text/javascript">
    $(function () {

        $("#defaultRibbon").ejRibbon({
            width: "100%",
            enableRTL: true,
            applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "ribbonmenu", menuSettings: { openOnClick: false } },
            tabs: [{
                id: "home", text: "منزل", groups: [{
                    text: "جديد", alignType: ej.Ribbon.AlignType.Rows, content: [{
                        groups: [{
                            id: "new",
                            text: "جديد",
                            toolTip: "جديد",
                            buttonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                imagePosition: ej.ImagePosition.ImageTop,
                                prefixIcon: "e-ribbon e-new",
                                click: "executeAction"
                            }
                        }
                        ],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 80
                        }
                    }]
                },
                ]
            },
            ]
        });
    });
    </script>

{% endhighlight %}

### expandPinSettings `object`
{:#members:expandpinsettings}

Sets custom setting to the expandable pin in the ribbon.

#### Default Value:

* Object

#### Example

{% highlight html %}
   
       <div id="defaultRibbon"></div>
       <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
        </ul>
        <script>
        $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            expandPinSettings:{				   
                        toolTip: "Collapse the Ribbon"                  
                    },
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
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
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }],
                }],
            }]
        });
    });
    </script>

{% endhighlight %}

### expandPinSettings.toolTip `string` 
{:#members:expandpinsettings-tooltip}

Sets tooltip for the expand pin.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
       <li><a>FILE</a>
            <ul>
             <li><a>New</a></li>
             </ul>
        </li>
     </ul>
     <script>
            $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            expandPinSettings:{				   
                        toolTip: "Collapse the Ribbon"                  
                    },
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
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
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }],
                }],
            }]
        });
    });
    </script>

{% endhighlight %}

### expandPinSettings.customToolTip `object` 
{:#members:expandpinsettings-customtooltip }

Specifies the custom tooltip for expand pin.Refer to ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.

#### Default Value:

* Object

#### Example

{% highlight html %}

    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
    </ul>
    <script>
    $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            expandPinSettings:{
                        customToolTip:{
                        title: "Collapse the Ribbon",
                        content: "<h6>Click the icon to collapse the Ribbon.</h6>"
                        }
                    },
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
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
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }],
                }],
            }]
        });
    });
    </script>

{% endhighlight %}

### applicationTab `object`
{:#members:applicationtab}

Specifies the application tab to contain application menu or backstage page in the ribbon control.

#### Default Value:

* Object

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
      $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
        });
     });
    </script>

  {% endhighlight %}


### applicationTab.backstageSettings `object`
{:#members:applicationtab-backstagesettings}

Specifies the ribbon backstage page items.

#### Default Value:

* object

#### Example

    {% highlight html %}
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>   
    {% endhighlight %}

### applicationTab.backstageSettings.text `string`
{:#members:applicationtab-backstagesettings-text}

Specifies the display text of application tab.

#### Default Value:

* null

#### Example

   {% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>
   {% endhighlight %}

### applicationTab.backstageSettings.height `string|number`
{:#members:applicationtab-backstagesettings-height}

Specifies the height of ribbon backstage page.

#### Default Value:

* null

#### Example

{% highlight html %}
    
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}

### applicationTab.backstageSettings.width `string|number`
{:#members:applicationtab-backstagesettings-width}

Specifies the width of ribbon backstage page.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}

### applicationTab.backstageSettings.pages `array`
{:#members:applicationtab-backstagesettings-pages}

Specifies the ribbon backstage page with its tab and button elements.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.pages.id `string`
{:#members:applicationtab-backstagesettings-pages-id}

Specifies the id for ribbon backstage page's tab and button elements.

#### Default Value:

* null

#### Example

{% highlight html %}
    
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.pages.text `string`
{:#members:applicationtab-backstagesettings-pages-text}

Specifies the text for ribbon backstage page's tab header and button elements.

#### Default Value:

* null

#### Example

{% highlight html %}
    
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.pages.itemType `enum`
{:#members:applicationtab-backstagesettings-pages-itemtype}

<ts name="ej.Ribbon.ItemType"/>

Specifies the type for ribbon backstage page's contents. Set "ej.Ribbon.BackStageItemType.Tab" to render the tab or "ej.Ribbon.BackStageItemType.Button" to render the button.

#### Default Value:

* ej.Ribbon.ItemType.Tab

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Button</td>
<td class="description">To render the button for ribbon backstage page’s contents</td>
</tr>
<tr>
<td class="name">Tab</td>
<td class="description">To render the tab for ribbon backstage page’s contents</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.pages.contentID `string`
{:#members:applicationtab-backstagesettings-pages-contentid}

Specifies the id of HTML elements like `div`,`ul`, etc., as ribbon backstage page's tab content.

#### Default Value:

* null

#### Example

{% highlight html %}
    
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.pages.enableSeparator `boolean`
{:#members:applicationtab-backstagesettings-pages-enableseparator}

Specifies the separator between backstage page's tab and button elements.

#### Default Value:

* false

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.backstageSettings.headerWidth `string|number`
{:#members:applicationtab-backstagesettings-headerwidth}

Specifies the width of backstage page header that contains tabs and buttons.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    </script>

{% endhighlight %}


### applicationTab.menuItemID `string`
{:#members:applicationtab-menuitemid}

Specifies the ID of `ul` list to create application menu in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
    
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button </button>
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,type:"custom",contentID:"btn"
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### applicationTab.menuSettings `object`
{:#members:applicationtab-menusettings}

Specifies the menu members, events by using the menu settings for the menu in the application tab.

#### Default Value:

* object
<ts ref = “ej.Menu.Model” />

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,type:"custom",contentID:"btn"
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### applicationTab.type `enum`
{:#members:applicationtab-type}

<ts name="ej.Ribbon.ApplicationTabType"/>

Specifies the application menu or backstage page. Specify the type of application tab as "ej.Ribbon.ApplicationTabType.Menu" to render the application menu or "ej.Ribbon.ApplicationTabType.Backstage" to render backstage page in the ribbon control.

#### Default Value:

* ej.Ribbon.ApplicationTabType.Menu

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Menu</td>
<td class="description">applicationTab display as menu</td>
</tr>
<tr>
<td class="name">Backstage</td>
<td class="description">applicationTab display as backstage</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
    
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,type:"custom",contentID:"btn"
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### contextualTabs `array`
{:#members:contextualtabs}

Specifies the contextual tabs and tab set to the ribbon control with the background color and border color. Refer to the tabs section for adding tabs into the contextual tab and contextual tab set.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <button id="design">Design button</button>
    <button id="div1">First button</button>
    <button id="div2">Second button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        contextualTabs: [{
            backgroundColor: "#FCFBEB",
            borderColor: "#F2CC1C",
            tabs: [{
                id: "Design",
                text: "DESIGN",
                groups: [{
                    text: "Table Style Options",
                    type: "custom",
                    contentID: "design"
                }]
            }]
        }, {
            borderColor: "lightblue",
            backgroundColor: "blue",
            tabs: [{
                id: "tabset1",
                text: "Tabset1",
                groups: [{
                    text: "Tabset1 Styles",
                    type: "custom",
                    contentID: "div1"
                }]
            }, {
                id: "tabset2",
                text: "Tabset2",
                groups: [{
                    text: "Tabset2 Styles",
                    type: "custom",
                    contentID: "div2"
                }]
            }]
        }]
    });
    });
    </script>  

{% endhighlight %}


### contextualTabs.backgroundColor `string`
{:#members:contextualtabs-backgroundcolor}

Specifies the backgroundColor of the contextual tabs and tab set in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <button id="design">Design button</button>
    <button id="div1">First button</button>
    <button id="div2">Second button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         contextualTabs: [{
             backgroundColor: "#FCFBEB",
             borderColor: "#F2CC1C",
             tabs: [{
                 id: "Design",
                 text: "DESIGN",
                 groups: [{
                     text: "Table Style Options",
                     type: "custom",
                     contentID: "design"
                 }]
             }]
         }, {
             borderColor: "lightblue",
             backgroundColor: "blue",
             tabs: [{
                 id: "tabset1",
                 text: "Tabset1",
                 groups: [{
                     text: "Tabset1 Styles",
                     type: "custom",
                     contentID: "div1"
                 }]
             }, {
                 id: "tabset2",
                 text: "Tabset2",
                 groups: [{
                     text: "Tabset2 Styles",
                     type: "custom",
                     contentID: "div2"
                 }]
             }]
         }]
     });
    });
    </script>  

{% endhighlight %}


### contextualTabs.borderColor `string`
{:#members:contextualtabs-bordercolor}

Specifies the borderColor of the contextual tabs and tab set in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <button id="design">Design button</button>
    <button id="div1">First button</button>
    <button id="div2">Second button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        contextualTabs: [{
            backgroundColor: "#FCFBEB",
            borderColor: "#F2CC1C",
            tabs: [{
                id: "Design",
                text: "DESIGN",
                groups: [{
                    text: "Table Style Options",
                    type: "custom",
                    contentID: "design"
                }]
            }]
        }, {
            borderColor: "lightblue",
            backgroundColor: "blue",
            tabs: [{
                id: "tabset1",
                text: "Tabset1",
                groups: [{
                    text: "Tabset1 Styles",
                    type: "custom",
                    contentID: "div1"
                }]
            }, {
                id: "tabset2",
                text: "Tabset2",
                groups: [{
                    text: "Tabset2 Styles",
                    type: "custom",
                    contentID: "div2"
                }]
            }]
        }]
    });
    });    
    </script> 

 {% endhighlight %}

### contextualTabs.tabs `array`
{:#members:contextualtabs-tabs}

Specifies the tabs to present in the contextual tabs and tab set. Refer to the tabs section for adding tabs into the contextual tabs and tab set.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <button id="design">Design button</button>
    <button id="div1">First button</button>
    <button id="div2">Second button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         contextualTabs: [{
             backgroundColor: "#FCFBEB",
             borderColor: "#F2CC1C",
             tabs: [{
                 id: "Design",
                 text: "DESIGN",
                 groups: [{
                     text: "Table Style Options",
                     type: "custom",
                     contentID: "design"
                 }]
             }]
         }, {
             borderColor: "lightblue",
             backgroundColor: "blue",
             tabs: [{
                 id: "tabset1",
                 text: "Tabset1",
                 groups: [{
                     text: "Tabset1 Styles",
                     type: "custom",
                     contentID: "div1"
                 }]
             }, {
                 id: "tabset2",
                 text: "Tabset2",
                 groups: [{
                     text: "Tabset2 Styles",
                     type: "custom",
                     contentID: "div2"
                 }]
             }]
         }]
     });
    });
    </script>  

{% endhighlight %}


### disabledItemIndex `array`
{:#members:disableditemindex}

Specifies the index or indexes to disable the given index tab or indexes tabs in the ribbon control.

#### Default Value:

* 0

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button<button>
    <button id="insert">Insert button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         width: "100%",
         // Set the disabledItemIndex during initialization. 
         disabledItemIndex: [1, 2],
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }, {
             id: "insert",
             text: "INSERT",
             groups: [{
                 text: "Insert group",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "insert"
             }]
         }]
     });
    });          
    </script>  

{% endhighlight %}


### enabledItemIndex `array`
{:#members:enableditemindex}

Specifies the index or indexes to enable the given index tab or indexes tabs in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button<button>
    <button id="insert">Insert button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }, {
            id: "insert",
            text: "INSERT",
            groups: [{
                text: "Insert group",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "insert"
            }]
        }]
    });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    ribbonObj.option({
    disabledItemIndex: [1, 2]
    });
    // Enable the required ribbon tab from the ribbon control.
    ribbonObj.option({
    enabledItemIndex: [1]
    });
    </script>  

{% endhighlight %}


### selectedItemIndex `number`
{:#members:selecteditemindex}

Specifies the index of the ribbon tab to select the given index tab item in the ribbon control.

#### Default Value:

* 1

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button<button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        width: "100%",
        // Set the selectedItemIndex during initialization. 
        selectedItemIndex: 2,
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }, {
            id: "insert",
            text: "INSERT",
            groups: [{
                text: "Insert group",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "insert"
            }]
        }]
    });
    });      
    </script>  

{% endhighlight %}


### tabs `array`
{:#members:tabs}

Specifies the tabs and its groups. Also specifies the control details that has to be placed in the tab area in the ribbon control.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <button id="insert">Insert button</button>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }, {
             id: "insert",
             text: "INSERT",
             groups: [{
                 text: "Insert group",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "insert"
             }]
         }]
     });
     }); 
    </script>  

{% endhighlight %}


### tabs.groups `array`
{:#members:tabs-groups}

Specifies single group or multiple groups and its contents to each tab in the ribbon control.

#### Default Value:

* array

#### Example

{% highlight html %}
    
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });   
    </script> 

 {% endhighlight %}


### tabs.groups.alignType `enum`
{:#members:tabs-groups-aligntype}

<ts name="ej.Ribbon.AlignType"/>

Specifies the alignment of controls in the groups in 'row' type or 'column' type. Value for row type is "ej.Ribbon.AlignType.Rows" and for column type is "ej.Ribbon.alignType.columns".

#### Default Value:

* ej.Ribbon.AlignType.Rows

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Rows</td>
<td class="description">To align the group content's in row</td>
</tr>
<tr>
<td class="name">Columns</td>
<td class="description">To align group content's in columns</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });        
    </script>  

{% endhighlight %}


### tabs.groups.content `array`
{:#members:tabs-groups-content}

Specifies the Syncfusion button, split button, dropdown list, toggle button, gallery, custom controls to the groups in the ribbon control.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.content.defaults `object`
{:#members:tabs-groups-content-defaults}

Specifies the height, width, type, isBig property to the controls in the group commonly.

#### Default Value:

* object

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                            width: 100,
                            }
                        },
                           {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        height: 70
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.defaults.height `string|number`
{:#members:tabs-groups-content-defaults-height}

Specifies the controls height such as Syncfusion button,split button,dropdown list,toggle button in the subgroup of  the ribbon tab.

#### Default Value:

* null

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                            width: 100,
                            }
                        },
                           {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        height: 70
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.defaults.width `string|number`
{:#members:tabs-groups-content-defaults-width}

Specifies the controls width such as Syncfusion button,split button,dropdown list,toggle button in the subgroup of  the ribbon tab.

#### Default Value:

* null

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                            width: 100,
                            }
                        },
                           {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 70
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.defaults.type `string`
{:#members:tabs-groups-content-defaults-type}

Specifies the controls type such as Syncfusion button,split button,dropdown list,toggle button in the subgroup of  the ribbon tab.

#### Default Value:

* ej.Ribbon.Type.Button

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                            width: 100,
                            }
                        },
                           {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 70
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.defaults.isBig `boolean`
{:#members:tabs-groups-content-defaults-isbig}

Specifies the controls size such as Syncfusion button,split button,dropdown list,toggle button in the subgroup of  the ribbon tab.

#### Default Value:

* false

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                            width: 100,
                            }
                        },
                           {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 70,
                        isBig: true
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.groups `array`
{:#members:tabs-groups-content-groups}

Specifies the controls such as Syncfusion button, split button, dropdown list, toggle button, gallery, custom controls in the subgroup of the ribbon tab .

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.buttonSettings `object`
{:#members:tabs-groups-content-groups-buttonsettings}

Specifies the Syncfusion button members, events by using this buttonSettings.

#### Default Value:

* object
<ts ref = “ej.Button.Model” />

#### Example

   {% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
        <script type="text/javascript">   
        $(function() {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "100%",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            isBig: true,
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                                width: 100,
                            }
                        }]
                    }]
                }]
            }]
        });
        });        
    </script>  

   {% endhighlight %}


### tabs.groups.content.groups.columns `number`
{:#members:tabs-groups-content-groups-columns}

It is used to set the count of gallery contents in a row.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li>
        <a>FILE </a>
        <ul>
        <li><a>New</a></li>
        <li><a>Open</a></li>
        <li><a>Save</a></li>
        <li><a>Save as</a></li>
        <li><a>Print</a></li>
        </ul>
    </li>
    </ul>
    <div id="Ribbon"></div>
    <ul id="custommenu">
    <li>
        <a>New Quick Step</a>
        <ul>
        <li><a>Move to new folder</a></li>
        <li><a>Categorize &amp; Move</a></li>
        <li><a>Flag &amp; Move</a></li>
        </ul>
    </li>
    </ul>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Gallery",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "Gallery",
                        columns: 3,
                        itemHeight: 65,
                        itemWidth: 68,
                        expandedColumns: 4,
                        type: ej.Ribbon.type.gallery,
                        galleryItems: [{
                            text: "Content1",
                            toolTip: "GalleryContent1"
                        }, {
                            text: "Content2",
                            toolTip: "GalleryContent2"
                        }, {
                            text: "Content3",
                            toolTip: "GalleryContent3"
                        }, {
                            text: "Content4",
                            toolTip: "GalleryContent4"
                        }, {
                            text: "Content5",
                            toolTip: "GalleryContent5"
                        }, {
                            text: "Content6",
                            toolTip: "GalleryContent6"
                        }],
                        customGalleryItems: [{
                            customItemType: ej.Ribbon.customItemType.menu,
                            menuId: "custommenu",
                            menuSettings: {
                                openOnClick: false
                            }
                        }, {
                            text: "Save Selection as new quick style",
                            toolTip: "Save Selection as new quick style",
                            customItemType: ej.Ribbon.customItemType.button,
                            buttonSettings: {
                                cssClass: "e-extrabtnstyle"
                            }
                        }]
                    }]
                }]
            }]
        }]
    });
    }); 
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.contentID `string`
{:#members:tabs-groups-content-groups-contentid}

Specifies the custom items such as div, table, controls as custom controls with the type "ej.Ribbon.Type.Custom" in the groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <input id="fontcolor"/> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.Type.Button,
                        buttonSettings: {
                            width: 160,
                            height: 50
                        }
                    }, {
                        id: "fontcolor",
                        text: "Font Color",
                        toolTip: "Font Color",
                        type: ej.Ribbon.Type.Custom,
                        contentID: "fontcolor"
                    }]
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

 {% endhighlight %}


### tabs.groups.content.groups.cssClass `string`
{:#members:tabs-groups-content-groups-cssclass}

Specifies the CSS class property to apply styles to the button, split, dropdown controls in the groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <style>
    .e-cssclass {
        margin-left: 20px;
    }
    </style>
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            cssClass:"e-cssclass",
                            isBig:true,
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 100,
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script> 

 {% endhighlight %}

### tabs.groups.content.groups.customGalleryItems `array`
{:#members:tabs-groups-content-groups-customgalleryitems}

Specifies the Syncfusion button and menu as gallery extra items.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                 </ul>
                </li>
        </ul>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    }); 
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.customGalleryItems.buttonSettings `object`
{:#members:tabs-groups-content-groups-customgalleryitems-buttonsettings}

Specifies the Syncfusion button members, events by using buttonSettings.

#### Default Value:

* object
<ts ref = “ej.Button.Model” />

#### Example


{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             customToolTip: {
                                 title: "<u>Save</u>",
                                 content: "<i>Save Selection as new quick style</i>",
                                 prefixIcon: "e-expander",
                             },
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
     });       
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.customGalleryItems.customItemType `enum`
{:#members:tabs-groups-content-groups-customgalleryitems-customitemtype}

<ts name="ej.Ribbon.CustomItemType"/>

Specifies the type as ej.Ribbon.CustomItemType.Menu or ej.Ribbon.CustomItemType.Button to render Syncfusion button and menu.

#### Default Value:

* ej.Ribbon.CustomItemType.Button

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Button</td>
<td class="description">Specifies the button type in customGalleryItems</td>
</tr>
<tr>
<td class="name">Menu</td>
<td class="description">Specifies the menu type in customGalleryItems</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             customToolTip: {
                                 title: "<u>Save</u>",
                                 content: "<i>Save Selection as new quick style</i>",
                                 prefixIcon: "e-expander",
                             },
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
     }); 
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.customGalleryItems.customToolTip `object`
{:#members:tabs-groups-content-groups-customgalleryitems-customtooltip}

Specifies the custom tooltip for gallery extra item's button. Refer to ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.

#### Default Value:

* object

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                    </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             customToolTip: {
                                 title: "<u>Save</u>",
                                 content: "<i>Save Selection as new quick style</i>",
                                 prefixIcon: "e-expander",
                             },
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    });       
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.customGalleryItems.menuId `string`
{:#members:tabs-groups-content-groups-customgalleryitems-menuid}

Specifies the UL list id to render menu as gallery extra item.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                 <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             customToolTip: {
                                 title: "<u>Save</u>",
                                 content: "<i>Save Selection as new quick style</i>",
                                 prefixIcon: "e-expander",
                             },
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    }); 
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.customGalleryItems.menuSettings `object`
{:#members:tabs-groups-content-groups-customgalleryitems-menusettings}

Specifies the Syncfusion menu members, events by using menuSettings.

#### Default Value:

* object
<ts ref = “ej.Menu.Model” />

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             customToolTip: {
                                 title: "<u>Save</u>",
                                 content: "<i>Save Selection as new quick style</i>",
                                 prefixIcon: "e-expander",
                             },
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
     }); 
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.customGalleryItems.text `string`
{:#members:tabs-groups-content-groups-customgalleryitems-text}

Specifies the text for gallery extra item's button.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function () {
       $("#Ribbon").ejRibbon({
     // Set the width during initialization.         
      width: "700px",
      applicationTab: {
      type: ej.Ribbon.ApplicationTabType.Menu,
      menuItemID: "menu",
      menuSettings: {
          openOnClick: false
      }
    },
     tabs: [{
      id: "home",
      text: "HOME",
      groups: [{
          text: "Gallery",
          alignType: ej.Ribbon.AlignType.Rows,
          content: [{
              groups: [{
                  id: "Gallery",
                  columns: 3,
                  itemHeight: 65,
                  itemWidth: 68,
                  expandedColumns: 4,
                  type: ej.Ribbon.type.gallery,
                  galleryItems: [{
                      text: "Content1",
                      toolTip: "GalleryContent1"
                  }, {
                      text: "Content2",
                      toolTip: "GalleryContent2"
                  }, {
                      text: "Content3",
                      toolTip: "GalleryContent3"
                  }, {
                      text: "Content4",
                      toolTip: "GalleryContent4"
                  }, {
                      text: "Content5",
                      toolTip: "GalleryContent5"
                  }, {
                      text: "Content6",
                      toolTip: "GalleryContent6"
                  }],
                  customGalleryItems: [{
                      customItemType: ej.Ribbon.customItemType.menu,
                      menuId: "custommenu",
                      menuSettings: {
                          openOnClick: false
                      }
                  }, {
                      text: "Save Selection as new quick style",
                      toolTip: "Save Selection as new quick style",
                      customItemType: ej.Ribbon.customItemType.button,
                      buttonSettings: {
                          cssClass: "e-extrabtnstyle"
                      }
                  }]
              }]
          }]
      }]
     }]
    });
    });   
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.customGalleryItems.toolTip `string`
{:#members:tabs-groups-content-groups-customgalleryitems-tooltip}

Specifies the tooltip for gallery extra item's button.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
     $(function() {
      $("#Ribbon").ejRibbon({
          // Set the width during initialization.         
          width: "700px",
          applicationTab: {
              type: ej.Ribbon.ApplicationTabType.Menu,
              menuItemID: "menu",
              menuSettings: {
                  openOnClick: false
              }
          },
          tabs: [{
              id: "home",
              text: "HOME",
              groups: [{
                  text: "Gallery",
                  alignType: ej.Ribbon.AlignType.Rows,
                  content: [{
                      groups: [{
                          id: "Gallery",
                          columns: 3,
                          itemHeight: 65,
                          itemWidth: 68,
                          expandedColumns: 4,
                          type: ej.Ribbon.type.gallery,
                          galleryItems: [{
                              text: "Content1",
                              toolTip: "GalleryContent1"
                          }, {
                              text: "Content2",
                              toolTip: "GalleryContent2"
                          }, {
                              text: "Content3",
                              toolTip: "GalleryContent3"
                          }, {
                              text: "Content4",
                              toolTip: "GalleryContent4"
                          }, {
                              text: "Content5",
                              toolTip: "GalleryContent5"
                          }, {
                              text: "Content6",
                              toolTip: "GalleryContent6"
                          }],
                          customGalleryItems: [{
                              customItemType: ej.Ribbon.customItemType.menu,
                              menuId: "custommenu",
                              menuSettings: {
                                  openOnClick: false
                              }
                          }, {
                              text: "Save Selection as new quick style",
                              toolTip: "Save Selection as new quick style",
                              customItemType: ej.Ribbon.customItemType.button,
                              buttonSettings: {
                                  cssClass: "e-extrabtnstyle"
                              }
                          }]
                      }]
                  }]
              }]
          }]
      });
    });           
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.customToolTip `object`
{:#members:tabs-groups-content-groups-customtooltip}

Provides custom tooltip for button, split button, dropdown list, toggle button, custom controls in the sub groups. Text and HTML support are also provided for title and content.

#### Default Value:

* Object

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Expand",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "expand",
                         text: "Expand Button",
                         customToolTip: {
                             title: "<i&amp;gtExpand</i>",
                             content: "<h5&amp;gtExpand content</h5>",
                             prefixIcon: "e-expander",
                         }
                     }, {
                         id: "new",
                         text: "New Button",
                         customToolTip: {
                             title: "New",
                             content: "New content"
                         }
                     }]
                 }]
             }]
         }]
     });
    }); 
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.customToolTip.content `string`
{:#members:tabs-groups-content-groups-customtooltip-content}

Sets content to the custom tooltip. Text and HTML support are provided for content.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
      $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Expand",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "expand",
                         text: "Expand Button",
                         customToolTip: {
                             title: "<i&amp;gtExpand</i>",
                             content: "<h5&amp;gtExpand content</h5>",
                             prefixIcon: "e-expander",
                         }
                     }, {
                         id: "new",
                         text: "New Button",
                         customToolTip: {
                             title: "New",
                             content: "New content"
                         }
                     }]
                 }]
             }]
         }]
     });
    });    
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.customToolTip.prefixIcon `string`
{:#members:tabs-groups-content-groups-customtooltip-prefixicon}

Sets icon to the custom tooltip content.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Expand",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                        customToolTip: {
                            title: "<i>Expand</i>",
                            content: "<h5>Expand content</h5>",
                            prefixIcon: "e-expander",
                        }
                    }, {
                        id: "new",
                        text: "New Button",
                        customToolTip: {
                            title: "New",
                            content: "New content"
                        }
                    }]
                }]
            }]
        }]
    });
    });  
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.customToolTip.title `string`
{:#members:tabs-groups-content-groups-customtooltip-title}

Sets title to the custom tooltip. Text and HTML support are provided for title and the title is in bold for text format.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Expand",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                        customToolTip: {
                            title: "<i>Expand</i>",
                            content: "<h5>Expand content</h5>",
                            prefixIcon: "e-expander",
                        }
                    }, {
                        id: "new",
                        text: "New Button",
                        customToolTip: {
                            title: "New",
                            content: "New content"
                        }
                    }]
                }]
            }]
        }]
    });
    });         
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.dropdownSettings `object`
{:#members:tabs-groups-content-groups-dropdownsettings}

Specifies the Syncfusion dropdown list members, events by using this dropdownSettings.

#### Default Value:

* object
<ts ref = “ej.DropDownList.Model” />

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <style>
    .e-cssclass {
        margin-left: 20px;
    }
    </style>
    <script type="text/javascript">  
    var fontfamily = ["Segoe UI", "Arial", "Times New Roman", "Tahoma", "Helvetica"];
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "fontfamily",
                        toolTip: "Font",
                        type: ej.Ribbon.Type.DropDownList,
                        dropdownSettings: {
                            dataSource: fontfamily,
                            value: "Segoe UI",
                            width: 150
                        }
                    }]
                }]
            }]
        }]
    });
    });         
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.enableSeparator `boolean`
{:#members:tabs-groups-content-groups-enableseparator}

Specifies the separator to the control that is in row type group. The separator separates the control from the next control in the group. Set "true" to enable the separator.

#### Default Value:

* false

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            enableSeparator: true,
                            buttonSettings: {
                            width: 100,
                            }
                        },
                          {
                            id: "font",
                            text: "Font",
                            toolTip: "Font",
                            buttonSettings: {
                            width: 150,
                            }
                        }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                        height: 70
                    }
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.expandedColumns `number`
{:#members:tabs-groups-content-groups-expandedcolumns}

Sets the count of gallery contents in a row, when the gallery is in expanded state.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    });     
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.galleryItems `array`
{:#members:tabs-groups-content-groups-galleryitems}

Defines each gallery content.

#### Default Value:

* array

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    });  
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.galleryItems.buttonSettings `object`
{:#members:tabs-groups-content-groups-galleryitems-buttonsettings}

Specifies the Syncfusion button members, events by using buttonSettings.

#### Default Value:

* object
<ts ref = “ej.Button.Model” />

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    .e-gallerycontent1{
    font-style: italic;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1",
                             buttonSettings: {
                                 cssClass: "e-gallerycontent1"
                             }
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    });
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.galleryItems.customToolTip `object`
{:#members:tabs-groups-content-groups-galleryitems-customtooltip}

Specifies the custom tooltip for gallery content. Refer to ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.

#### Default Value:

* object

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Gallery",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "Gallery",
                        columns: 3,
                        itemHeight: 65,
                        itemWidth: 68,
                        expandedColumns: 4,
                        type: ej.Ribbon.type.gallery,
                        galleryItems: [{
                            text: "Content1",
                            customToolTip: {
                                title: "<u>GalleryContent</u>",
                                content: "<b>GalleryContent 1</b>",
                                prefixIcon: "e-expander",
                            }
                        }, {
                            text: "Content2",
                            toolTip: "GalleryContent2"
                        }, {
                            text: "Content3",
                            toolTip: "GalleryContent3"
                        }, {
                            text: "Content4",
                            toolTip: "GalleryContent4"
                        }, {
                            text: "Content5",
                            toolTip: "GalleryContent5"
                        }, {
                            text: "Content6",
                            toolTip: "GalleryContent6"
                        }],
                        customGalleryItems: [{
                            customItemType: ej.Ribbon.customItemType.menu,
                            menuId: "custommenu",
                            menuSettings: {
                                openOnClick: false
                            }
                        }, {
                            text: "Save Selection as new quick style",
                            toolTip: "Save Selection as new quick style",
                            customItemType: ej.Ribbon.customItemType.button,
                            buttonSettings: {
                                cssClass: "e-extrabtnstyle"
                            }
                        }]
                    }]
                }]
            }]
        }]
    });
    });        
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.galleryItems.text `string`
{:#members:tabs-groups-content-groups-galleryitems-text}

Sets text for the gallery content.

#### Default Value:

* null

#### Example


{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
     });  
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.galleryItems.toolTip `string`
{:#members:tabs-groups-content-groups-galleryitems-tooltip}

Sets tooltip for the gallery content.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Gallery",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "Gallery",
                        columns: 3,
                        itemHeight: 65,
                        itemWidth: 68,
                        expandedColumns: 4,
                        type: ej.Ribbon.type.gallery,
                        galleryItems: [{
                            text: "Content1",
                            toolTip: "GalleryContent1"
                        }, {
                            text: "Content2",
                            toolTip: "GalleryContent2"
                        }, {
                            text: "Content3",
                            toolTip: "GalleryContent3"
                        }, {
                            text: "Content4",
                            toolTip: "GalleryContent4"
                        }, {
                            text: "Content5",
                            toolTip: "GalleryContent5"
                        }, {
                            text: "Content6",
                            toolTip: "GalleryContent6"
                        }],
                        customGalleryItems: [{
                            customItemType: ej.Ribbon.customItemType.menu,
                            menuId: "custommenu",
                            menuSettings: {
                                openOnClick: false
                            }
                        }, {
                            text: "Save Selection as new quick style",
                            toolTip: "Save Selection as new quick style",
                            customItemType: ej.Ribbon.customItemType.button,
                            buttonSettings: {
                                cssClass: "e-extrabtnstyle"
                            }
                        }]
                    }]
                }]
            }]
        }]
    });
    });   
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.id `string`
{:#members:tabs-groups-content-groups-id}

Specifies the Id for button, split button, dropdown list, toggle button, gallery, custom controls in the sub groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script> 

 {% endhighlight %}


### tabs.groups.content.groups.isBig `boolean`
{:#members:tabs-groups-content-groups-isbig}

Specifies the size for button, split button controls. Set "true" for big size and "false" for small size.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            isBig:true,
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 100
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script> 

{% endhighlight %}


### tabs.groups.content.groups.itemHeight `string|number`
{:#members:tabs-groups-content-groups-itemheight}

Sets the height of each gallery content.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",
                             toolTip: "Save Selection as new quick style",
                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }]
     });
    });    
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.itemWidth `string|number`
{:#members:tabs-groups-content-groups-itemwidth}

Sets the width of each gallery content.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <style>
    .e-extracontent .e-extrabtnstyle{
    padding-left: 28px;
    text-align: left;
    }
    </style>
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="custommenu">
                <li><a>New Quick Step</a>
                <ul>
                <li><a>Move to new folder</a></li>
                <li><a>Categorize &amp; Move</a></li>
                <li><a>Flag &amp; Move</a></li>
                </ul>
                </li>
        </ul>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "Gallery",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "Gallery",
                        columns: 3,
                        itemHeight: 65,
                        itemWidth: 68,
                        expandedColumns: 4,
                        type: ej.Ribbon.type.gallery,
                        galleryItems: [{
                            text: "Content1",
                            toolTip: "GalleryContent1"
                        }, {
                            text: "Content2",
                            toolTip: "GalleryContent2"
                        }, {
                            text: "Content3",
                            toolTip: "GalleryContent3"
                        }, {
                            text: "Content4",
                            toolTip: "GalleryContent4"
                        }, {
                            text: "Content5",
                            toolTip: "GalleryContent5"
                        }, {
                            text: "Content6",
                            toolTip: "GalleryContent6"
                        }],
                        customGalleryItems: [{
                            customItemType: ej.Ribbon.customItemType.menu,
                            menuId: "custommenu",
                            menuSettings: {
                                openOnClick: false
                            }
                        }, {
                            text: "Save Selection as new quick style",
                            toolTip: "Save Selection as new quick style",
                            customItemType: ej.Ribbon.customItemType.button,
                            buttonSettings: {
                                cssClass: "e-extrabtnstyle"
                            }
                        }]
                    }]
                }]
            }]
        }]
    });
    });     
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.splitButtonSettings `object`
{:#members:tabs-groups-content-groups-splitbuttonsettings}

Specifies the Syncfusion split button members, events by using this splitButtonSettings.

#### Default Value:

* object
<ts ref = “ej.SplitButton.Model” />

#### Example

{% highlight html %}
    
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <ul id="split">
    <li><span>Paste</span></li>
    </ul>
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            isBig:true,
                            type: ej.Ribbon.Type.SplitButton,
                            splitButtonSettings: {
                            targetID: "split",
                            buttonMode: "dropdown",
                            arrowPosition:"bottom"
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.text `string`
{:#members:tabs-groups-content-groups-text}

Specifies the text for button, split button, toggle button controls in the sub groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.toggleButtonSettings `object`
{:#members:tabs-groups-content-groups-togglebuttonsettings}

Specifies the Syncfusion toggle button members, events by using toggleButtonSettings.

#### Default Value:

* object
<ts ref = “ej.ToggleButton.Model” />

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "bold",
                            toolTip: "Bold",
                            isBig:true,
                            type: ej.Ribbon.Type.ToggleButton,
                            toggleButtonSettings: {
                            defaultText: "Bold",
                            activeText: "BoldTog"
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.content.groups.toolTip `string`
{:#members:tabs-groups-content-groups-tooltip}

Specifies the tooltip for button, split button, dropdown list, toggle button, custom controls in the sub groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}

### tabs.groups.content.groups.quickAccessMode `enum`
{:#members:tabs-groups-content-groups-quickaccessmode}

<ts name="ej.Ribbon.QuickAccessMode"/>

To add,show and hide controls in Quick Access toolbar.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">None</td>
<td class="description">Controls are hidden in Quick Access toolbar </td>
</tr>
<tr>
<td class="name">ToolBar</td>
<td class="description">Add controls in toolBar</td>
</tr>
<tr>
<td class="name">Menu</td>
<td class="description">Add controls in menu</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.Ribbon.QuickAccessMode.None

#### Example

{% highlight html %}

    <ul id="ribbonmenu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">   
        $(function () {
            $("#Ribbon").ejRibbon({
                width: "100%",
                showQAT: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Font",
                        alignType: ej.Ribbon.AlignType.Rows,
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon bold"
                                }
                            }, {
                                id: "italic",
                                text: "Italic",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonitalic"
                                }
                            }, {
                                id: "underline",
                                text: "Underline",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonunderline"
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                height: 30
                            }
                        }]
                    }]
                }]
            });
        });
    </script> 

{% endhighlight %}

### tabs.groups.content.groups.type `enum`
{:#members:tabs-groups-content-groups-type}

<ts name="ej.Ribbon.Type"/>

Specifies the type as "ej.Ribbon.Type.Button" or "ej.Ribbon.Type.SplitButton" or "ej.Ribbon.Type.DropDownList" or "ej.Ribbon.Type.ToggleButton" or "ej.Ribbon.Type.Custom" or "ej.Ribbon.Type.Gallery" to render button, split, dropdown, toggle button, gallery, custom controls.

#### Default Value:

* ej.Ribbon.Type.Button

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Button</td>
<td class="description">Specifies the button control</td>
</tr>
<tr>
<td class="name">SplitButton</td>
<td class="description">Specifies the split button</td>
</tr>
<tr>
<td class="name">DropDownList</td>
<td class="description">Specifies the dropDown</td>
</tr>
<tr>
<td class="name">Custom</td>
<td class="description">To append external element's</td>
</tr>
<tr>
<td class="name">ToggleButton</td>
<td class="description">Specifies the toggle button</td>
</tr>
<tr>
<td class="name">Gallery</td>
<td class="description">Specifies the ribbon gallery</td>
</tr>
</tbody>
</table>
 
#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {
        $("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "100%",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows,content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            type: ej.Ribbon.Type.Button,
                            buttonSettings: {
                            width: 160,
                            height: 50
                            }
                        }]
                    }]
            }]
            }]
    });
    });             
    </script>  

{% endhighlight %}


### tabs.groups.contentID `string`
{:#members:tabs-groups-contentid}

Specifies the ID of custom items to be placed in the groups.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });      
    </script>  

{% endhighlight %}


### tabs.groups.customContent `string`
{:#members:tabs-groups-customcontent}

Specifies the HTML contents to place into the groups.

#### Default Value:

* null

#### Example


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 type: "custom",
                 customContent: "<button id='customContent'>Custom Content</button>"
             }]
         }]
     });
    });        
    </script>  

{% endhighlight %}


### tabs.groups.enableGroupExpander `boolean`
{:#members:tabs-groups-enablegroupexpander}

Specifies the group expander for groups in the ribbon control. Set "true" to enable the group expander.

#### Default Value:

* false

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                enableGroupExpander: true,
                contentID: "btn"
            }]
        }]
    });
    });      
    </script>  

{% endhighlight %}

### tabs.groups.groupExpanderSettings `object`
{:#members:tabs-groups-groupexpandersettings}

Sets custom setting to the groups in the ribbon control.

#### Default Value:

* Object

#### Example 

{% highlight html %}

    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
    </ul>
    <script>
        $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    enableGroupExpander: true,
                    groupExpanderSettings:{   
                                toolTip: "Clipboard"                       
                            }
                }]
            }]
        });
    });
        </script>

{% endhighlight %}

### tabs.groups.groupExpanderSettings.toolTip `string` 
{:#members:tabs-groups-groupexpandersettings-tooltip}

Sets tooltip for the group expander of the group.

#### Default Value:

* null

#### Example

{% highlight html %}
  
    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
    </ul>
    <script>
        $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    enableGroupExpander: true,
                    groupExpanderSettings:{   
                                toolTip: "Clipboard"                       
                            }
                }]
            }]
        });
    });
        </script>

{% endhighlight %}

### tabs.groups.groupExpanderSettings.customToolTip `object` 
{:#members:tabs-groups-groupexpandersettings-customtooltip }

Specifies the custom tooltip for group expander.Refer to ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.

#### Default Value:

* Object

#### Example

{% highlight html %}

    div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
				<li><a>FILE</a>
                    <ul>
                    <li><a>New</a></li>
                    <li><a>Open</a></li>
			    	</ul>
				</li>
    </ul>
    <script>
        $(function() {
        $("#defaultRibbon").ejRibbon({
            width: "100%",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    enableGroupExpander: true,
                    groupExpanderSettings:{   
                                customToolTip:{
                                title: "Clipboard",
                                content: "<h6>Show a popup for the Clipboard group.</h6>"
                                }                     
                            }
                }]
            }]
        });
    });
    </script>

{% endhighlight %}

### tabs.groups.text `string`
{:#members:tabs-groups-text}

Specifies the text to the groups in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });         
    </script>  

{% endhighlight %}


### tabs.groups.type `string`
{:#members:tabs-groups-type}

Specifies the custom items such as div, table, controls by using the "custom" type.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });      
    </script>  

{% endhighlight %}


### tabs.id `string`
{:#members:tabs-id}

Specifies the ID for each tab's content panel.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });     
    </script>  

{% endhighlight %}


### tabs.text `string`
{:#members:tabs-text}

Specifies the text of the tab in the ribbon control.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });       
    </script> 

 {% endhighlight %}

### locale `string`
{:#members:locale}

Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data i.e. in a language and culture specific to a particular country or region and  it will need to use the user's preference. 

#### Default Value:

* "en-US"

#### Example

{% highlight html %}

    <div id="defaultRibbon"></div>
    <ul id="ribbonmenu">
       <li><a>FILE</a>
            <ul>
             <li><a>New</a></li>
             </ul>
        </li>
     </ul>
     <script>
            ej.Ribbon.Locale["es-ES"] = {
            CustomizeQuickAccess: "Agordu Rapida Aliro",
            MoreCommands: "pli Komando"
        };
        
        $(function() {
            $("#defaultRibbon").ejRibbon({
                width: "100%",
                locale: "es-ES",
                showQAT: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Menu,
                    menuItemID: "ribbonmenu",
                    menuSettings: {
                        openOnClick: false
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        alignType: ej.Ribbon.alignType.columns,
                        content: [{
                            groups: [{
                                id: "paste",
                                text: "paste",
                                toolTip: "Paste",
                                quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                                splitButtonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-ribbon e-ribbonpaste",
                                    targetID: "pasteSplit",
                                    buttonMode: "dropdown",
                                    arrowPosition: ej.ArrowPosition.Bottom,
                                    click: "executeAction"
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.Type.SplitButton,
                                width: 50,
                                height: 70
                            }
                        }]
                    }]
                }]
            });
        
        });
     </script>
     
{% endhighlight %}

### width `string|number`
{:#members:width}

Specifies the width to the ribbon control. You can set width in string or number format.

#### Default Value:

* null

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });        
    </script>  


{% endhighlight %}


## Methods


### addContextualTabs(contextualTabSet, \[index\])
{:#methods:addcontextualtabs}

Adds contextual tab or contextual tab set dynamically in the ribbon control with contextual tabs object and index position. When index is null, ribbon contextual tab or contextual tab set is added at the last index.

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
<td class="name">contextualTabSet</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">contextual tab or contextual tab set object.</td>
</tr>
<tr>
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the contextual tab or contextual tab set, this is optional.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <div id="design">ContextualTab</div>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
     var cTab = {
         backgroundColor: "#FCFBEB",
         borderColor: "#F2CC1C",
         tabs: [{
             id: "Design",
             text: "DESIGN",
             groups: [{
                 text: "Table Style",
                 type: "custom",
                 contentID: "design"
             }]
         }]
     }
     //initialize the Ribbon object
     var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Add new contextual tab or contextual tab set with given list
     ribbonObj.addContextualTabs(cTab, 2);
    </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <div id="design">ContextualTab</div>
    <script type="text/javascript">   
     $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    var cTab = {
     backgroundColor: "#FCFBEB",
     borderColor: "#F2CC1C",
     tabs: [{
         id: "Design",
         text: "DESIGN",
         groups: [{
             text: "Table Style",
             type: "custom",
             contentID: "design"
         }]
     }]
    }
     $("#Ribbon").ejRibbon("addContextualTabs", cTab, 2);
    </script> 

 {% endhighlight %}

### addBackStageItem(item,\[index\])
{:#methods:addbackstageitem}

Add new option to Backstage page.

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
<td class="name">item</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">select the object to add the backstage item</td>
</tr>
<tr>
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index to the backstage item this is optional.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var addBackStage =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
    //initialize the Ribbon object
     var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Add backstage items to the ribbon
     ribbonObj.addBackStageItem(addBackStage, 1);
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var addBackStage =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
     $("#Ribbon").ejRibbon("addBackStageItem",addBackStage, 1); 
    </script>
    
{% endhighlight %}

### addTab(tabText, ribbonGroups, \[index\])
{:#methods:addtab}

Adds tab dynamically in the ribbon control with given name, tab group array and index position. When index is null, ribbon tab is added at the last index.

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
<td class="name">tabText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">ribbon tab display text.</td>
</tr>
<tr>
<td class="name">ribbonGroups</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">groups to be displayed in ribbon tab .</td>
</tr>
<tr>
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the ribbon tab,this is optional.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
        <ul id="menu">
        <li><a>FILE </a>
        <ul>
        <li><a>New</a></li>
        <li><a>Open</a></li>
        <li><a>Save</a></li>
        <li><a>Save as</a></li>
        <li><a>Print</a></li>
        </ul></li></ul>
        <div id="Ribbon"></div> 
        <button id="btn">Home button</button>
        <script type="text/javascript">   
        $(function() {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "700px",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
        });
        var tabGroup = [{
        text: "New",
        alignType: ej.Ribbon.AlignType.Rows,
        content: [{
            groups: [{
                id: "new",
                text: "New",
                toolTip: "New"
            }],
            defaults: {
                type: ej.Ribbon.Type.Button,
                width: 60,
                height: 70
            }
        }]
        }];
        //initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // Add new ribbon tab with given list
        ribbonObj.addTab("Tab2", tabGroup, 2);
        </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});
    var tabGroup = [{
    text: "New",
    alignType: ej.Ribbon.AlignType.Rows,
    content: [{
        groups: [{
            id: "new",
            text: "New",
            toolTip: "New"
        }],
        defaults: {
            type: ej.Ribbon.Type.Button,
            width: 60,
            height: 70
        }
    }]
    }];
    $("#Ribbon").ejRibbon("addTab", "Tab2", tabGroup, 2); 
    </script>  

{% endhighlight %}

### addTabGroup(tabIndex, tabGroup, \[groupIndex\])
{:#methods:addtabgroup}

Adds tab group dynamically in the ribbon control with given tab index, tab group object and group index position. When group index is null, ribbon group is added at the last index.

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
<td class="name">tabIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">tabGroup</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">group to be displayed in ribbon tab .</td>
</tr>
<tr>
<td class="name">groupIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the ribbon group,this is optional.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "One",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "one",
                        text: "one"
                    }, {
                        id: "two",
                        text: "two"
                    }],
                    defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 60,
                        height: 70
                    }
                }]
            }]
        }]
    });
    });
    var ribbonGrp = {
    text: "New",
    alignType: ej.Ribbon.AlignType.Rows,
    content: [{
        groups: [{
            id: "new",
            text: "New"
        }],
        defaults: {
            type: ej.Ribbon.Type.Button,
            width: 60,
            height: 70
        }
    }]
    };
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Add new ribbon group with given list
    ribbonObj.addTabGroup(1, ribbonGrp, 0);
    </script>  

{% endhighlight %}


{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "One",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "one",
                        text: "one"
                    }, {
                        id: "two",
                        text: "two"
                    }],
                    defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 60,
                        height: 70
                    }
                }]
            }]
        }]
    });
    });
    var ribbonGrp = {
        text: "New",
        alignType: ej.Ribbon.AlignType.Rows,
        content: [{
            groups: [{
                id: "new",
                text: "New"
            }],
            defaults: {
                type: ej.Ribbon.Type.Button,
                width: 60,
                height: 70
            }
        }]
    };
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    $("#Ribbon").ejRibbon("addTabGroup", 1, ribbonGrp, 0);
    $("#Ribbon").ejRibbon("addTab", "Tab2", tabGroup, 2);
    </script>  

{% endhighlight %}


### addTabGroupContent(tabIndex, groupIndex, subGroupIndex, content, \[contentIndex\])
{:#methods:addtabgroupcontent}

Adds group content dynamically in the ribbon control with given tab index, group index, sub group index, content and content index position. When content index is null, content is added at the last index.

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
<td class="name">tabIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">groupIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon group index.</td>
</tr>
<tr>
<td class="name">subGroupIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">sub group index in the ribbon group,</td>
</tr>
<tr>
<td class="name">content</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">content to be displayed in the ribbon group.</td>
</tr>
<tr>
<td class="name">contentIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon content index .this is optional.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "One",
                alignType: ej.Ribbon.AlignType.Rows,
                content: [{
                    groups: [{
                        id: "one",
                        text: "one"
                    }, {
                        id: "two",
                        text: "two"
                    }],
                    defaults: {
                        type: ej.Ribbon.Type.Button,
                        width: 60,
                        height: 70
                    }
                }]
            }]
        }]
    });
    });
    var content = {
        id: "new",
        text: "new",
    };
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Add new ribbon content with given list
    ribbonObj.addTabGroupContent(1, 0, 0, content, 2);
        </script> 

 {% endhighlight %}


{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <script type="text/javascript">   
    $(function () {$("#Ribbon").ejRibbon({
    // Set the width during initialization.         
        width: "700px",
        applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [{
                text: "One", alignType: ej.Ribbon.AlignType.Rows, content: [{
                    groups: [{
                        id: "one",
                        text: "one"
                    },{
                        id: "two",
                        text: "two"
                    }],
                        defaults: {
                        type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                }]
            }]
        }]
    });        
    });         
     var content= {
                    id: "new",
                    text: "new",
                };
            //initialize the Ribbon object
            $("#Ribbon").ejRibbon("addTabGroupContent",1,0,0,content,2); 
    
    </script> 

 {% endhighlight %}


### hideBackstage()
{:#methods:hidebackstage}

Hides the ribbon backstage page.

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // hide the ribbon backstage page.
    ribbonObj.hideBackstage();
    </script>

{% endhighlight %}

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    $("#Ribbon").ejRibbon("hideBackstage");
    </script>

{% endhighlight %}


### collapse()
{:#methods:collapse}

Collapses the ribbon tab content.

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // collapse the ribbon control.
    ribbonObj.collapse();
        </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "700px",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    $("#Ribbon").ejRibbon("collapse");
    </script>  

{% endhighlight %}


### destroy()
{:#methods:destroy}

Destroys the ribbon widget. All the events bound using this._on are unbound automatically and the ribbon control is moved to pre-init state.

#### Example

{% highlight javascript %}
 
    <script>
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    ribbonObj.destroy(); // destroy the ribbon
    </script>

{% endhighlight %}


{% highlight javascript %}
 
    <script>
    // destroy the ribbon
    $("#Ribbon").ejRibbon("destroy");        
    </script>

{% endhighlight %}


### expand()
{:#methods:expand}

Expands the ribbon tab content.

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // expand the ribbon control.
    ribbonObj.collapse();
    ribbonObj.expand();
    </script> 

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "700px",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    $("#Ribbon").ejRibbon("collapse");
    $("#Ribbon").ejRibbon("expand");
    </script>  

{% endhighlight %}

### getTabText(index)
{:#methods:gettabtext}

Gets text of the given index tab in the ribbon control.

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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the tab item.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

String


#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // To get text of the given index tab in the ribbon control.
    ribbonObj.getTabText(1);
        </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    $("#Ribbon").ejRibbon("getTabText", 1);
    </script> 

{% endhighlight %}


### hideTab(text)
{:#methods:hidetab}

Hides the given text tab in the ribbon control.

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
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
      $(function() {
      $("#Ribbon").ejRibbon({
          // Set the width during initialization.         
          width: "100%",
          applicationTab: {
              type: ej.Ribbon.ApplicationTabType.Menu,
              menuItemID: "menu",
              menuSettings: {
                  openOnClick: false
              }
          },
          tabs: [{
              id: "home",
              text: "HOME",
              groups: [{
                  text: "New",
                  alignType: ej.Ribbon.AlignType.Rows,
                  type: "custom",
                  contentID: "btn"
              }]
          }]
      });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // hide the given text tab item in the ribbon control.
    ribbonObj.hideTab("HOME");
        </script> 

 {% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    $("#Ribbon").ejRibbon("hideTab", "HOME");
    </script>  

{% endhighlight %}


### isEnable(text)
{:#methods:isenable}

Checks whether the given text tab in the ribbon control is enabled or not.

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
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    //  To check given text tab in the ribbon control is enabled or not.
    ribbonObj.isEnable("HOME");
    </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
      $("#Ribbon").ejRibbon({
          // Set the width during initialization.         
          width: "100%",
          applicationTab: {
              type: ej.Ribbon.ApplicationTabType.Menu,
              menuItemID: "menu",
              menuSettings: {
                  openOnClick: false
              }
          },
          tabs: [{
              id: "home",
              text: "HOME",
              groups: [{
                  text: "New",
                  alignType: ej.Ribbon.AlignType.Rows,
                  type: "custom",
                  contentID: "btn"
              }]
          }]
      });
    });
    $("#Ribbon").ejRibbon("isEnable", "HOME");
    </script>  

{% endhighlight %}


### isVisible(text)
{:#methods:isvisible}

Checks whether the given text tab in the ribbon control is visible or not.

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
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Boolean

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    //  To check given text tab in the ribbon control is visible or not.
    ribbonObj.isVisible("HOME");
    </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">  
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    $("#Ribbon").ejRibbon("isVisible", "HOME");
    </script>  

{% endhighlight %}


### removeTab(index)
{:#methods:removetab}

Removes the given index tab item from the ribbon control.

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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of tab item.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Remove the given index tab item from the ribbon control.
    ribbonObj.removeTab(1);
    </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    $("#Ribbon").ejRibbon("removeTab", 1); 
    </script>  

{% endhighlight %}


### setTabText(tabText, newText)
{:#methods:settabtext}

Sets new text to the given text tab in the ribbon control.

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
<td class="name">tabText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">current text of the tab item.</td>
</tr>
<tr>
<td class="name">newText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">new text of the tab item.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // Set new text to the given text tab in the ribbon control.
    ribbonObj.setTabText("HOME", "NEW");
    </script> 

 {% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    $("#Ribbon").ejRibbon("setTabText", "HOME", "NEW");
    </script>  

{% endhighlight %}


### showBackstage()
{:#methods:showbackstage}

Displays the ribbon backstage page.

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
     //initialize the Ribbon object
      var ribbonObj = $("#Ribbon").data("ejRibbon");
     // show the ribbon backstage page.
      ribbonObj.showBackstage();
    </script>

{% endhighlight %}

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }]
        });
    });    
    $("#Ribbon").ejRibbon("showBackstage");
    </script>

{% endhighlight %}


### showTab(text)
{:#methods:showtab}

Displays the given text tab in the ribbon control.

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
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
    });
    //initialize the ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // hide the given text tab item in the ribbon control.
    ribbonObj.showTab("HOME");
    </script>  

{% endhighlight %}


{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }]
     });
    });
    $("#Ribbon").ejRibbon("showTab", "HOME");
    </script>  

{% endhighlight %}

### updateGroup(tabIndex, groupId, \[contentGroup\])
{:#methods:updategroup}

To customize Group alone in the inside content.

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
<td class="name">tabIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">groupId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">group id to be displayed in ribbon tab .</td>
</tr>
<tr>
<td class="name">contentGroup</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">contentGroup is used in the object</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
        <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
        </ul>
    </li>
    </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "700px",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "One",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "one",
                            text: "one"
                        }, {
                            id: "two",
                            text: "two"

                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }]
        });
    });
    var ribbonGrp =
         {
           text: "new one "
          };
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    ribbonObj.updateGroup(1, one, ribbonGrp);
    </script>

{% endhighlight %}

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
        <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
        </ul>
    </li>
    </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "700px",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "One",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "one",
                            text: "one"
                        }, {
                            id: "two",
                            text: "two"

                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }]
        });
    });
    var ribbonGrp =
         {
           text: "new one "
          };
    $("#Ribbon").ejRibbon("updateGroup",1, "one", ribbonGrp);
    </script>

{% endhighlight %}

### updateBackStageItem(index,\[item\])
{:#methods:updatebackstageitem}

Update option in existing Backstage.

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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index to the backstage item</td>
</tr>
<tr>
<td class="name">item</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">select the object to add the backstage item</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var updateBackStage =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
    $("#Ribbon").ejRibbon("updateBackStageItem",1,updateBackStage);
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var updateBackSatge =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    ribbonObj.updateBackSatgeItem(1,updateBackSatge);
    </script>
    
{% endhighlight %}

### removeTabGroupContent(tabIndex, groupIndex, \[subGroupIndex\])
{:#methods:removetabgroupcontent}

To customize whole content from Tab Group.

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
<td class="name">tabIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">groupIndex</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">ribbon group index.</td>
</tr>
<tr>
<td class="name">subGroupIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">sub group index in the ribbon group,</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
        <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
        </ul>
    </li>
    </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "700px",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "One",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "one",
                            text: "one"
                        }, {
                            id: "two",
                            text: "two"
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }]
        });
    });
    var content = {
        id: "new",
        text: "new",
    };
    $("#Ribbon").ejRibbon("removeTabGroupContent",1, "One", 0);
    </script>

 {% endhighlight %}

{% highlight html %}
        
    <ul id="menu">
    <li><a>FILE </a>
        <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
            <li><a>Save as</a></li>
            <li><a>Print</a></li>
        </ul>
    </li>
    </ul>
    <div id="Ribbon"></div>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            // Set the width during initialization.         
            width: "700px",
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "menu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "One",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "one",
                            text: "one"
                        }, {
                            id: "two",
                            text: "two"
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                }]
            }]
        });
    });
    var content = {
        id: "new",
        text: "new",
    };
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // remove tab group content in the ribbon 
    ribbonObj.removeTabGroupContent(1, "One", 0);
    </script>

 {% endhighlight %}
 
### removeBackStageItem(index)
{:#methods:removebackstageitem}

Remove option from Backstage.

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
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index to the backstage item</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
   <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var removeBackStage =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
    //initialize the Ribbon object
    var ribbonObj = $("#Ribbon").data("ejRibbon");
    // remove backstage item in the ribbon 
    ribbonObj.removeBackStageItem(1);
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style: none">
        <div style="margin-left: 30px; font-size: 20px">Open</div>
        <li>Recent Workbooks</li>
        <li>Computer</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">
    $(function () {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "open",
                        text: "Open",
                        contentID: "content1"
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],

        });
    });
    var removeBackStage =
                    {
                        id: "File",
                        text: "File",
                        itemType: ej.Ribbon.ItemType.Tab
                    }
    $("#Ribbon").ejRibbon("removeBackStageItem",1);
    </script>
    
{% endhighlight %}

## Events

### beforeTabRemove
{:#events:beforetabremove}

Triggered before the ribbon tab item is removed.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current tab item index in the ribbon control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        beforeTabRemove: function(args) {}
    });
    });
    </script>  

{% endhighlight %}

### create
{:#events:create}

Triggered before the ribbon control is created.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Ribbon.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         create: function(args) {}
     });
    });  
    </script>  

{% endhighlight %}

### destroy
{:#events:destroy}

Triggered before the ribbon control is destroyed.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">deleteIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current ribbon tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         destroy: function(args) {}
     });
    });           
    </script>  

{% endhighlight %}

### groupClick
{:#events:groupclick}

Triggered when the control in the group is clicked successfully.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the control clicked in the group.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         groupClick: function(args) {}
     });
    });  
    </script>  

{% endhighlight %}

### groupExpand
{:#events:groupexpand}

Triggered when the group expander in the group is clicked successfully.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the clicked group expander.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        groupExpand: function(args) {}
    });
    });      
    </script>  

{% endhighlight %}

### galleryItemClick
{:#events:galleryitemclick}

Triggered when an item in the Gallery control is clicked successfully.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">galleryModel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gallery model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the item clicked in the gallery.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{

                 text: "Gallery",
                 alignType: ej.Ribbon.AlignType.Rows,
                 content: [{
                     groups: [{
                         id: "Gallery",
                         columns: 3,
                         itemHeight: 65,
                         itemWidth: 68,
                         expandedColumns: 4,
                         type: ej.Ribbon.type.gallery,
                         galleryItems: [{
                             text: "Content1",
                             toolTip: "GalleryContent1"
                         }, {
                             text: "Content2",
                             toolTip: "GalleryContent2"
                         }, {
                             text: "Content3",
                             toolTip: "GalleryContent3"
                         }, {
                             text: "Content4",
                             toolTip: "GalleryContent4"
                         }, {
                             text: "Content5",
                             toolTip: "GalleryContent5"
                         }, {
                             text: "Content6",
                             toolTip: "GalleryContent6"
                         }],
                         customGalleryItems: [{
                             customItemType: ej.Ribbon.customItemType.menu,
                             menuId: "custommenu",
                             menuSettings: {
                                 openOnClick: false
                             }
                         }, {
                             text: "Save Selection as new quick style",

                             customItemType: ej.Ribbon.customItemType.button,
                             buttonSettings: {
                                 cssClass: "e-extrabtnstyle"
                             }
                         }]
                     }]
                 }]
             }]
         }],
         galleryItemClick: function(args) {}
     });
    });   
    </script>  

{% endhighlight %}

### backstageItemClick
{:#events:backstageitemclick}

Triggered when a tab or button in the backstage page is clicked successfully.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the item clicked in the gallery.</td>
</tr>
<tr>
<td class="name">id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the id of the target item.</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the text of the target item.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <div id="content1">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
    <li>Protect Workbook</li>
    <li>Inspect Workbook</li>
    <li>Versions</li>
    <li>Browser View Options</li>
    </ul>
    </div>
    <div id="content2">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
    <li>Recent Workbooks</li>
    <li>Computer</li>
    </ul>
    </div>
    <div id="content3">
    <ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
    <li>Create PDF/XPS Document</li>
    <li>Change File Type</li>
    </ul>
    </div>
    <div id="Ribbon"></div>
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "500px",
            applicationTab: {
                 type: ej.Ribbon.ApplicationTabType.Backstage,
                backstageSettings: {
                    text: "FILE",
                    height: 250,
                    width: 600,
                    headerWidth: 125,
                    pages: [{
                        id: "info",
                        text: "Info",
                        itemType: ej.Ribbon.itemType.tab,
                        contentID: "content1"
                    }, {
                        id: "open",
                        text: "Open",
                        contentID: "content2"
                    }, {
                        id: "export",
                        text: "Export",
                        contentID: "content3",
                        enableSeparator: true
                    }, {
                        id: "exit",
                        text: "Exit",
                        itemType: ej.Ribbon.itemType.button
                    }]
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "New",
                    alignType: ej.Ribbon.AlignType.Rows,
                    type: "custom",
                    contentID: "btn"
                }]
            }],
        backstageItemClick : function (args) {}
        });
    });   
    </script>

{% endhighlight %}

### collapse
{:#events:collapse}

Triggered when the ribbon control is collapsed.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         collapse: function(args) {}
     });
    });  
    </script>  

{% endhighlight %}


### expand
{:#events:expand}

Triggered when the ribbon control is expanded.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         expand: function(args) {}
     });
    });       
    </script>  

{% endhighlight %}

### load
{:#events:load}

Triggered before the ribbon control is load.

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         load: function(args) {}
     });
    });       
    </script>  

{% endhighlight %}

### tabAdd
{:#events:tabadd}

Triggered after adding the new ribbon tab item.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">tabHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns new added tab header.</td>
</tr>
<tr>
<td class="name">tabContent</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns new added tab content panel.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         tabAdd: function(args) {}
     });
    });
    </script>  

{% endhighlight %}

### tabClick
{:#events:tabclick}

Triggered when tab is clicked successfully in the ribbon control.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">prevActiveHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">prevActiveIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns previous active index.</td>
</tr>
<tr>
<td class="name">activeHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active tab header .</td>
</tr>
<tr>
<td class="name">activeIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         tabClick: function(args) {}
     });
    });
    </script>  

{% endhighlight %}

### tabCreate
{:#events:tabcreate}

Triggered before the ribbon tab is created.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">deleteIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current ribbon tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        tabCreate: function(args) {}
    });
    });   
    </script>  

{% endhighlight %}


### tabRemove
{:#events:tabremove}

Triggered after the tab item is removed from the ribbon control.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">removedIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the removed index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
     $("#Ribbon").ejRibbon({
         // Set the width during initialization.         
         width: "100%",
         applicationTab: {
             type: ej.Ribbon.ApplicationTabType.Menu,
             menuItemID: "menu",
             menuSettings: {
                 openOnClick: false
             }
         },
         tabs: [{
             id: "home",
             text: "HOME",
             groups: [{
                 text: "New",
                 alignType: ej.Ribbon.AlignType.Rows,
                 type: "custom",
                 contentID: "btn"
             }]
         }],
         tabRemove: function(args) {}
     });
    });       
    </script>  

{% endhighlight %}

### tabSelect
{:#events:tabselect}

Triggered after the ribbon tab item is selected in the ribbon control.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">prevActiveHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">prevActiveIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns previous active index.</td>
</tr>
<tr>
<td class="name">activeHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active tab header .</td>
</tr>
<tr>
<td class="name">activeIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
    $("#Ribbon").ejRibbon({
        // Set the width during initialization.         
        width: "100%",
        applicationTab: {
            type: ej.Ribbon.ApplicationTabType.Menu,
            menuItemID: "menu",
            menuSettings: {
                openOnClick: false
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.AlignType.Rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
        tabSelect: function(args) {}
    });
    });      
    </script>  

{% endhighlight %}

### toggleButtonClick
{:#events:togglebuttonclick}

Triggered when the expand/collapse button is clicked successfully .

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the expand/collapse button.</td>
</tr>
</tbody>
</table>




#### Example

{% highlight html %}
 
    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
      $("#Ribbon").ejRibbon({
          // Set the width during initialization.         
          width: "100%",
          applicationTab: {
              type: ej.Ribbon.ApplicationTabType.Menu,
              menuItemID: "menu",
              menuSettings: {
                  openOnClick: false
              }
          },
          tabs: [{
              id: "home",
              text: "HOME",
              groups: [{
                  text: "New",
                  alignType: ej.Ribbon.AlignType.Rows,
                  type: "custom",
                  contentID: "btn"
              }]
          }],
          toggleButtonClick: function(args) {}
      });
    });
    </script>  

{% endhighlight %}

### qatMenuItemClick        
{:#events:qatmenuitemclick}

Triggered when the QAT menu item is clicked successfully .

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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the clicked menu item text.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <ul id="menu">
    <li><a>FILE </a>
    <ul>
    <li><a>New</a></li>
    <li><a>Open</a></li>
    <li><a>Save</a></li>
    <li><a>Save as</a></li>
    <li><a>Print</a></li>
    </ul></li></ul>
    <div id="Ribbon"></div> 
    <button id="btn">Home button</button>
    <script type="text/javascript">   
    $(function() {
        $("#Ribbon").ejRibbon({
            width: "100%",
            showQAT: true,
            applicationTab: {
                type: ej.Ribbon.ApplicationTabType.Menu,
                menuItemID: "ribbonmenu",
                menuSettings: {
                    openOnClick: false
                }
            },
            tabs: [{
                id: "home",
                text: "HOME",
                groups: [{
                    text: "Font",
                    alignType: ej.Ribbon.AlignType.Rows,
                    content: [{
                        groups: [{
                            id: "bold",
                            text: "Bold",
                            quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                            buttonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                prefixIcon: "e-ribbon bold"
                            }
                        }, {
                            id: "italic",
                            text: "Italic",
                            quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                            buttonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                prefixIcon: "e-ribbon e-ribbonitalic"
                            }
                        }, {
                            id: "underline",
                            text: "Underline",
                            quickAccessMode: ej.Ribbon.QuickAccessMode.ToolBar,
                            buttonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                prefixIcon: "e-ribbon e-ribbonunderline"
                            }
                        }],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            height: 30
                        }
                    }]
                }]
            }],
            qatMenuItemClick: function(args) {}
        });
    });
    </script>
 
{% endhighlight %}



