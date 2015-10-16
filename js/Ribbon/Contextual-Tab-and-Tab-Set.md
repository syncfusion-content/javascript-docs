---
layout: post
title: Contextual-Tab-and-Tab-Set
description: contextual tab and tab set
platform: js
control: Ribbon
documentation: ug
---

# Contextual Tab and Tab Set

You can add **Contextual Tabs** and **Tab Set** in the Ribbon control. In contextualTabs definition, use tabs property to add contextual tabs and contextual tab set. In tabs definition, use **backgroundColor** property to apply background color to the **Contextual Tabs** and **Tab Set**. Use **borderColor** property to apply border color to the **Contextual Tabs** and **Tab Set**.

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
                <li><a>Open</a></li>
             </ul>
          </li>
       </ul>
       <div id="Contents">Custom Control</div>
       <div id="contextualTab"><button id="contextualBtn">Contextual Tab</button></div>
       <div id="contextualTabset1"><button id="contextualTabsetBtn1">Contextual Tabset1</button></div>
       <div id="contextualTabset2"><button id="contextualTabsetBtn2">Contextual Tabset2</button></div>
       <script type="text/javascript">
        $(function() {
            $("#Ribbon").ejRibbon({
                width: "800px",
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
                        text: "CustomControls",
                        type: "custom",
                        contentID: "Contents"
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
                            contentID: "contextualTab"
                        }]
                    }]
                }, {
                    backgroundColor: "blue",
                    borderColor: "lightblue",
                    tabs: [{
                        id: "tabset1",
                        text: "Tabset1",
                        groups: [{
                            text: "Tabset1 Style",
                            type: "custom",
                            contentID: "contextualTabset1"
                        }]
                    }, {
                        id: "tabset2",
                        text: "Tabset2",
                        groups: [{
                            text: "Tabset2 Style",
                            type: "custom",
                            contentID: "contextualTabset2"
                        }]
                    }]
                }]        
            });
        });
       </script>
    </body>
    <!-- ... -->

{% endhighlight %}

The following screenshot illustrates Ribbon with **Contextual Tabs** and **Tab Set**.

![](/js/Ribbon/Contextual-Tab-and-Tab-Set_images/Contextual-Tab-and-Tab-Set_img1.png)

