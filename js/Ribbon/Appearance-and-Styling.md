---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Ribbon
documentation: ug
---

# Appearance and Styling

## SelectedItemIndex

Specifies the index of the **Ribbon tab** to select the given index tab item in the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">
            var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }, {
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.option({
                    selectedItemIndex: 2
                });
            });
       </script>       
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->
    
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img1.png")

## DisabledItemIndex

Specifies the index or indexes to disable the corresponding tabs in the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">
          var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.option({
                    disabledItemIndex: [1, 2]
                });
            });
       </script>
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->

{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img2.png")

## EnableItemIndex

 Specifies the index or indexes to enable the corresponding tabs in the **Ribbon** control.

{% highlight html %}
        
    <!-- ... -->
    <head></head>
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
       <div id="content">Home control</div>
       <script type="text/javascript">
            var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.option({
                    disabledItemIndex: [1, 2]
                });
                ribbonObj.option({
                    enabledItemIndex: [1]
                });
            });
       </script>
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->
        
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img3.png")

## HideTab

This method is used to hide the given text tab in the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">
            var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.hideTab("HOME");
            });
       </script>
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->

{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img4.png")

## ShowTab

This method is used to show the given text tab in the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">
            var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.hideTab("HOME");
                ribbonObj.showTab("HOME");
            });
       </script>        
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->
  
{% endhighlight %}
  
The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img5.png")

## RemoveTab

This method is used to remove the given index tab item from the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">
            var ribbonObj;
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: "600px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
                ribbonObj = $("#Ribbon").data("ejRibbon");
                ribbonObj.removeTab(2);
            });
       </script>
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->
        
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img6.png")

## Width

Specifies the **width** to the **Ribbon** control.

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
       <div id="content">Home control</div>
       <script type="text/javascript">                                                                                             
            $(function() {
                $("#Ribbon").ejRibbon({
                    width: 800,
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu",
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "insert",
                        text: "INSERT",
                        groups: [{
                            text: "Clipboard",
                            alignType: ej.Ribbon.alignType.columns,
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
                                    type: ej.Ribbon.type.button,
                                    isBig: true,
                                    width: 50,
                                    height: 70
                                }
                            }]
                        }]
                    }, {
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            alignType: ej.Ribbon.alignType.rows,
                            type: "custom",
                            contentID: "content"
                        }]
                    }]
                });
            });
       </script>
       <style type="text/css">
          .e-ribbon .e-ribbonpaste:before {
          content: "\e645";
          font-family:"ej-webfont";
          font-size: 36px;
          position: relative;
          left: -9px;
          top: -4px;
          }
       </style>
    </body>
    <!-- ... -->
        
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img7.png")

## Add Tab Groups

This method is used to add Ribbon Group dynamically in the Ribbon control. This method needs three arguments **addTabGroup(Tab index, Groupcollection, Group index).**

* **Tab index**: Index of tab, where the group is to be added.
* **TabGroup collection**: Collection of the groups that group needs to add.
* **Group Index**: Index of ribbon group, where the group is to be added. It is optional argument, when this argument is not given, group is added at last position by default.

{% highlight html %}
   
    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <script type="text/javascript">
        $(function() {
              $("#Ribbon").ejRibbon({
                  width: "700px",
                  applicationTab: {
                      Type: "ApplicationMenu",
                      itemID: "menu"
                  },
                  tabs: [{
                      id: "home",
                      text: "HOME",
                      groups: [{
                          text: "One",
                          alignType: ej.Ribbon.alignType.rows,
                          content: [{
                              groups: [{
                                  id: "one",
                                  text: "one"
                              }, {
                                  id: "two",
                                  text: "two"
                              }],
                              defaults: {
                                  type: ej.Ribbon.type.button,
                                  width: 60,
                                  height: 70
                              }
                          }]
                      }]
                  }]
              });
              var ribbonGrp = {
                  text: "New",
                  alignType: ej.Ribbon.alignType.rows,
                  content: [{
                      groups: [{
                          id: "new",
                          text: "New"
                      }],
                      defaults: {
                          type: ej.Ribbon.type.button,
                          width: 60,
                          height: 70
                      }
                  }]
              };
              //initialize the Ribbon object
              var ribbonObj = $("#Ribbon").data("ejRibbon");
              // Add new ribbon group with given list
              ribbonObj.addTabGroup(1, ribbonGrp, 0);
          });                            
       </script>
    </body>
    <!-- ... -->
    
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img8.png")

## Add Tab Group Content

This method is used to add group content dynamically in the ribbon. This method contains five arguments **addTabGroupContent(Tab index, Group index, Subgroup index, Content, Content index).**

* **Tab index**: Ribbon Tab index.
* **Group index**: Ribbon group index.
* **Subgroup Index**: Sub group index. Content to be added belongs to this sub group index.
* **Content**: Collection of the group content that is added as Ribbon group content. 
* **Content Index**: Ribbon content index, this is optional argument. When this argument is not given, the Group content is added at last position by default.

{% highlight html %}

    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <script type="text/javascript">
            $(function() {
                $("#Ribbon").ejRibbon({
                    // Set the width during initialization. 	
                    width: "700px",
                    applicationTab: {
                        Type: "ApplicationMenu",
                        itemID: "menu"
                    },
                    tabs: [{
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "One",
                            alignType: ej.Ribbon.alignType.rows,
                            content: [{
                                groups: [{
                                    id: "one",
                                    text: "one"
                                }, {
                                    id: "two",
                                    text: "two"
                                }],
                                defaults: {
                                    type: ej.Ribbon.type.button,
                                    width: 60,
                                    height: 70
                                }
                            }]
                        }]
                    }]
                });
                var content = {
                    id: "new",
                    text: "new",
                };
                //initialize the Ribbon object
                var ribbonObj = $("#Ribbon").data("ejRibbon");
                // Add new ribbon content with given list
                ribbonObj.addTabGroupContent(1, 0, 0, content, 2);
            });             
       </script>
    </body>
    <!-- ... -->
        
{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img9.png")

## Collapse and Expand

### Collapse

**Collapse** method is used to minimize the ribbon control tab contents.You can minimize the Ribbon tab content by using the client side method **collapse()**.

{% highlight html %}

    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <div id="paste" style="height:40px;width:43px;">Paste</div>
       <script type="text/javascript">
        $(function() {
            $("#Ribbon").ejRibbon({
                width: "800px",
                applicationTab: {
                    Type: "ApplicationMenu",
                    itemID: "menu"
                },
                tabs: [{
                    id: "insert",
                    text: "INSERT",
                    groups: [{
                        text: "Clipboard",
                        type: "custom",
                        contentID: "paste"
                    }]
                }]
            });
            ribbonObj = $("#Ribbon").data("ejRibbon");
            ribbonObj.collapse();
        });
       </script>
    </body>
    <!-- ... -->    
        
{% endhighlight %}

The following screenshot displays the output of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img10.png")

### Expand

**Expand** method is used to expand the minimized ribbon control tab contents.You can expand the Ribbon tab content by using the client side method **expand()**.

{% highlight html %}
  
    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <div id="paste" style="height:40px;width:43px;">Paste</div>
       <script type="text/javascript">
        $(function() {
            $("#Ribbon").ejRibbon({
                width: "800px",
                applicationTab: {
                    Type: "ApplicationMenu",
                    itemID: "menu"
                },
                tabs: [{
                    id: "insert",
                    text: "INSERT",
                    groups: [{
                        text: "Clipboard",
                        type: "custom",
                        contentID: "paste"
                    }]
                }]
            });
            ribbonObj = $("#Ribbon").data("ejRibbon");
            ribbonObj.expand();
        });
       </script>
    </body>
    <!-- ... -->
        
{% endhighlight %}

The following screenshot displays the output of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img11.png")

## AddTab

This method is used to add tab dynamically in the Ribbon control. This method requires three arguments **addTab(Tabname,TabGroupcollection,index).**

* **Tabname**: Name of the tab.
* **TabGroupcollection**: Collection of the tab groups that tab needs to add.
* **Index**: Index in which the tab is to be added.It is an optional argument. When this argument is not given, by default the tab is added at the last position.

{% highlight html %}
  
    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <div id="paste" style="height:40px;width:43px;">Paste</div>
       <div id="newtab" style="height:35px;width:43px;">AddTab</div>
       <script type="text/javascript">
         $(function() {
            $("#Ribbon").ejRibbon({
                width: "800px",
                applicationTab: {
                    Type: "ApplicationMenu",
                    itemID: "menu"
                },
                tabs: [{
                    id: "insert",
                    text: "INSERT",
                    groups: [{
                        text: "Clipboard",
                        type: "custom",
                        contentID: "paste"
                    }]
                }]
            });
            var tabGroup = [{
                text: "New",
                type: "custom",
                contentID: "newtab"
            }];
                    
            ribbonObj = $("#Ribbon").data("ejRibbon");
            ribbonObj.addTab("AddTab", tabGroup, 2);
        });
       </script>
    </body>
    <!-- ... -->

{% endhighlight %}

The following screenshot displays the output of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img12.png")

## AddContextualTabs

This method is used to add contextual tabs dynamically.This method has two arguments **addContextualTabs(Contextualtabs,index).**

* **Contextualtabs**: Collection of the contextual tabs that contextual tab needs to add.
* **Index**: Index in which the tab is to be added.It is optional argument. When this argument is not given, by default the tab is added at the last position.

{% highlight html %}
  
    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <ul id="menu">
          <li><a>FILE</a></li>
       </ul>
       <div id="paste" style="height:40px;width:43px;">Paste</div>
       <div id="design">ContextualTab</div>
       <script type="text/javascript">
        $(function() {
         $("#Ribbon").ejRibbon({
             width: "800px",
             applicationTab: {
                 Type: "ApplicationMenu",
                 itemID: "menu"
             },
             tabs: [{
                 id: "insert",
                 text: "INSERT",
                 groups: [{
                     text: "Clipboard",
                     type: "custom",
                     contentID: "paste"
                 }]
             }]
         });
         var contextualTab = {
             backgroundColor: "#FCFBEB",
             borderColor: "#F2CC1C",
             tabs: [{
                 id: "Design",
                 text: "DESIGN",
                 groups: [{
                     text: "Tabgroup",
                     type: "custom",
                     contentID: "design"
                 }]
             }]
         }
         ribbonObj = $("#Ribbon").data("ejRibbon");
         ribbonObj.addContextualTabs(contextualTab, 2);
     });
       </script>
    </body>
    <!-- ... -->

{% endhighlight %}

The following screenshot displays the output of the above code example.

![]("/js/Ribbon/Appearance-and-Styling_images/Appearance-and-Styling_img13.png")

