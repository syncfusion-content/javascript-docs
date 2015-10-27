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
          <li>
             <a>FILE</a>
             <ul>
                <li><a>New</a></li>
             </ul>
          </li>
       </ul>
       <script type="text/javascript">
            $(function() {
              $("#defaultRibbon").ejRibbon({
                  width: "70%",
                  allowResizing: true,
                  applicationTab: {
                      type: "ApplicationMenu",
                      menuItemID: "ribbonmenu"
                  },

                  tabs: [{
                      id: "home",
                      text: "HOME",
                      groups: [{
                              text: "Clipboard",
                              alignType: ej.Ribbon.alignType.rows,
                              content: [{
                                  groups: [{
                                      id: "cut",
                                      text: "Cut"
                                  }, {
                                      id: "copy",
                                      text: "Copy"
                                  }]
                              }]
                          },

                          {
                              text: "Font",
                              alignType: "rows",
                              content: [{
                                  groups: [{
                                      id: "bold",
                                      text: "Bold",
                                  }, {
                                      id: "italic",
                                      text: "Italic"

                                  }, {
                                      id: "underline",
                                      text: "Underline"

                                  }, {
                                      id: "strikethrough",
                                      text: "Strikethrough"
                                  }],
                                  defaults: {
                                      height: 70
                                  }
                              }]
                          },

                          {
                              text: "New",
                              alignType: ej.Ribbon.alignType.rows,
                              content: [{
                                  groups: [{
                                      id: "new",
                                      text: "New",
                                  }],
                              }]
                          }, {
                              text: "Actions",
                              alignType: ej.Ribbon.alignType.rows,
                              content: [{
                                  groups: [{
                                      id: "undo",
                                      text: "Undo",
                                      buttonSettings: {
                                          contentType: ej.ContentType.TextAndImage,
                                          imagePosition: ej.ImagePosition.ImageTop,
                                          prefixIcon: "e-ribbon e-undo"
                                      }
                                  }, {
                                      id: "redo",
                                      text: "Redo",
                                      buttonSettings: {
                                          contentType: ej.ContentType.TextAndImage,
                                          imagePosition: ej.ImagePosition.ImageTop,
                                          prefixIcon: "e-ribbon e-redo"
                                      }
                                  }],
                                  defaults: {
                                      type: "button",
                                      width: 40,
                                      height: 70
                                  }
                              }]
                          }
                      ]
                  }]
              });
          });
       </script>
       <style>
          .e-ribbon .e-Clipboard:before {
          content: "\e645";
          font-size: 27px;
          position: relative;
          left: -9px;
          font-family:"ej-webfont"; 
          line-height: 1;
          }
          .e-ribbon .e-Actions:before {
          content: "\e736";
          font-size: 27px;
          position: relative;
          left: -2px;
          line-height: 1;
          font-family:"ej-webfont";
          }
          .e-ribbon .e-Font:before {
          content: "\e636";
          font-family:"ej-webfont";
          line-height: 1;
          font-size: 27px;
          }
          .e-ribbon .e-New:before {
          content: "\e632";
          font-size: 27px;
          position: relative;    
          right: -1px;
          font-family:"ej-webfont";
          line-height: 1;
          }
       </style>
    </body>
    <!-- ... -->

{% endhighlight %}

The following screenshot displays **Ribbon** control without resizing the window.

![](/js/Ribbon/Resize_images/Resize_img1.png)

When you resize the window, the ribbon groups are converted  into group button based on the window width. When you click the group button, the corresponding group items are displayed .The following screenshot displays the Ribbon control when clicking the group button **Actions**.

![](/js/Ribbon/Resize_images/Resize_img2.png)

