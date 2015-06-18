---
layout: post
title: Resize
description: resize 
platform: js
control: Ribbon
documentation: ug
---

# Resize 

**Ribbon** control supports resizing functionality .To enable resizing in the ribbon, you need to set the **allowResizing** property to **true**. When you resize the ribbon window, the Ribbon control automatically resizes to fit into the layout panel. 

{% highlight html %}

     <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
     <div id="defaultRibbon"></div>    
     <ul id="ribbonmenu">
               <li><a>FILE</a>
              <ul><li><a>New</a></li></ul>
               </li>
               </ul>                        
       <script type="text/javascript">
       $(function () {
            $("#defaultRibbon").ejRibbon({
                width: "70%",
               **allowResizing: true**, 
                applicationTab: {
                    Type: "ApplicationMenu", itemID: "ribbonmenu"
                },
                
                tabs: [{
                    id: "home", text: "HOME", groups: [{
                        text: "Clipboard", alignType: ej.Ribbon.alignType.rows, content: [
                        {
                            groups: [{
                                id: "cut",
                                text: "Cut"
                            },
                            {
                                id: "copy",
                                text: "Copy"
                            }
                            ]
                        }]
                    },
                    
                    {
                        text: "Font", alignType: "rows", content: [
                        {
                            groups: [{
                                id: "bold",
                                text: "Bold",
                            },
                               {
                                   id: "italic",
                                   text: "Italic"

                               },
                               {
                                   id: "underline",
                                   text: "Underline"

                               },
                               {
                                   id: "strikethrough",
                                   text: "Strikethrough"
                               }
                            ],
                            defaults: {
                                height: 70
                            }
                        }]
                    },
                    
                    {
                    text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                    id: "new",
                    text: "New",
                    }
                    ],
                    }]
                    },
                    {
                    text: "Actions", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                    id: "undo",
                    text: "Undo"
                    },
                    {
                    id: "redo",
                    text: "Redo"
                    }
                    ],
                    }]
                    }]
                }]
            });
        });
    </script>
    </body>
    <!-- ... -->


{% endhighlight %}


The following screenshot displays **Ribbon** control without resizing the window.

{% include image.html url="/js/Ribbon/Concepts-and-Features/Resize_images/Resize_img1.png" Caption="Ribbon control befor resizing"%}

When you resize the window, the ribbon groups are converted  into group button based on the window width. When you click the group button, the corresponding group items are displayed .The following screenshot displays the **Ribbon** control when clicking the group button **Actions**.

{% include image.html url="/js/Ribbon/Concepts-and-Features/Resize_images/Resize_img2.png" Caption="Ribbon control after clicking the group button Actions"%}

