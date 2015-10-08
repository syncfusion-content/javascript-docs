---
layout: post
title: Custom-Tooltip
description: custom tooltip
platform: js
control: Ribbon
documentation: ug
---

# Custom Tooltip

The **Ribbon** control has Custom Tooltip support that is displayed when you move the mouse over the control elements. You can define the CustomTooltip under the **groups**, **galleryItems**, and **customGalleryItems** etc... CustomTooltip contains **title**, **content**, **prefixIcon** properties that are used to set Title, Content and placing the icon into this.

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
          $(function () {
             $("#defaultRibbon").ejRibbon({
                 width: "100%", 
                 applicationTab: { Type: "ApplicationMenu", itemID: "ribbonmenu" },
                 tabs: [{
                     id: "home", text: "HOME", groups: [
                     {
                         text: "Clipboard", alignType: ej.Ribbon.alignType.columns, content: [{
                             groups: [{
                                 id: "paste",
                                 text: "paste",
                                 customToolTip: {
                                     title: "Paste",
                                     content: "Paste the content.Add content on the Clipboard to your document",
                                     prefixIcon: "e-pastetip"
                                 },
                                 buttonSettings: {
                                     contentType: ej.ContentType.ImageOnly,
                                     prefixIcon: "e-ribbon e-ribbonpaste",
                                     height:75,
                                     width:70
                                 }
                             }
                             ]
                         }]
                     }]
                 }]
             });
          });
       </script>
    </body>
    <!-- ... -->

{% endhighlight %}

The following output is displayed as a result of the above code example.

![]("/js/Ribbon/Custom-Tooltip_images/Custom-Tooltip_img1.png")

