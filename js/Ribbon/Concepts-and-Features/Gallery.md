---
layout: post
title: Gallery
description: gallery
platform: js
control: Ribbon
documentation: ug
---

# Gallery

The **Ribbon** control has gallery support. By using the Gallery in Ribbon, items are displayed with good look and feel and it also enables to classify the items as groups for easy navigation.Gallery can be included in the **tabgroups**.

To use the gallery feature, include the following properties under **tabgroups**.

* **id** –defines the id of the gallery.

* **type**- defines the type of the item and it must be of type ej.Ribbon.type.gallery.

* **columns** –defines the number of columns to be displayed in a row at intial without gallery expand operation.

* **expandedColumns**-defines the number of columns to be displayed in a row at gallery expand operation.

* **itemHeight** –defines the height of the  contents.

* **itemWidth** –defines the width of contents.

* **galleryItems** –defines the collection of the items to be included in the gallery.

* **customGalleryItems**- defines the additional items to be  displayed at gallery expand operation. It can be of customItemType  ej.Ribbon. customItemType.button or ej.Ribbon. customItemType.menu. By default value it is ej.Ribbon. customItemType.button.



{% highlight html %}


    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
    <div id="defaultRibbon">
        </div>
        <ul id="ribbonmenu">
            <li><a>FILE</a> </li>
        </ul>
        <ul id="custommenu">
            <li><a>New Quick Step</a>
                <ul>
                    <li><a>Flag and Move</a></li>
                </ul>
            </li>
        </ul>
        <div id="paste" style="height: 40px; width: 43px;">Paste</div>
        <script type="text/javascript">
               $(function () {
                $("#defaultRibbon").ejRibbon({
                    width: "800",
                    applicationTab: { Type: "ApplicationMenu", itemID: "ribbonmenu" },
                    tabs: [{
                        id: "home", text: "HOME", groups: [{
                            text: "Clipboard", type: "custom", contentID: "paste"
                        },
      {
          text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
              groups: [
    {
        id: "Gallery1",
        columns: 2,
        itemHeight: 54,
        itemWidth: 68,
        expandedColumns: 3,
        type: ej.Ribbon.type.gallery,
        galleryItems: [{
            text: "Content1",
            toolTip: "Content1",
        },
       {
           text: "Content2",
           toolTip: "Content2",
       }
       ,
       {
           text: "Content3",
           toolTip: "Content3"
       },
           {
               text: "Content4",
               toolTip: "Content4"
           },
           {
               text: "Content5",
               toolTip: "Content5"
           }
        ],
    
        customGalleryItems: [
       {
           text: "Save Selection as new quick style",
           toolTip: "Save",
           customItemType: ej.Ribbon. customItemType.button,
       },
       {
           customItemType: ej.Ribbon. customItemType.menu,
           menuId: "custommenu"
       }]
    }]
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

{% include image.html url="/js/Ribbon/Concepts-and-Features/Gallery_images/Gallery_img1.png" Caption="Ribbon control default Gallery."%}



{% include image.html url="/js/Ribbon/Concepts-and-Features/Gallery_images/Gallery_img2.png" Caption="Ribbon control after  Gallery expand operation"%}

