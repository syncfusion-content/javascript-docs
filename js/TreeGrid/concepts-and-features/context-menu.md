---
layout: post
title: context-menu
description: context menu
platform: js
control: TreeGrid
documentation: ug
---

# Context Menu

**Context menu** in **TreeGrid** control is used to manipulate (add, edit and delete) the tree grid rows. In **ejTreeGrid**, context menu can be enabled with **contextMenuSettings** API. The **contextMenuSettings** property contains two inner properties **showContextMenu** and **contextMenuItems**.

The **showContextMenu** property is used to **enable or disable** the context menu, default value for this property is **false.**

The **contextMenuItems** property is used to add the menu items to context menu, this property renders ‘Add’ and ‘Delete’ by default when the menu items are not provided.



{% highlight js %}


$("#treegrid1").ejTreeGrid(
        {   
           // ...     
            editSettings:{allowEditing: true , editMode:”rowEditing”},
            contextMenuSettings:{showContextMenu: true 
                                contextMenuItems:[ ”add”,”edit”,”delete”]},
            // ...             
        });


{% endhighlight %}







The following screenshot displays the Context menu in **TreeGrid** control.

{% include image.html url="\js\TreeGrid\concepts-and-features\context-menu_images\context-menu_img1.png" Caption="Figure 29: Context menu in TreeGrid"%}

## ContextMenu Customization

Context menu can be customized by adding a new custom menu item to it. In **ejTreeGrid**, context menu can be customized using **contextMenuOpen** client side event. This event is triggered when the context menu is rendered with mouse right click action. The following properties are available in the event,

* **headerText:** Display text for menu item.

* **iconPath:** Image location for menu item.

* **eventHandler:** Client side event for menu item click.



{% highlight js %}


$("#treegrid1").ejTreeGrid(
        {   
           // ...     
            contextMenuSettings:{showContextMenu: true},
            contextMenuOpen: customMenu,
            // ...             
        });


<script type=”text/javascript”>
  function customMenu( args )
{
   args.contextMenuItems.push(
   {
      headerText: "customMenu",
   iconPath: “url(…/images/custommenu.png)”,
   eventHandler: customMenuClick,
   }
   );
}
  function customMenuClick( args )
  {
                // ...     

             // ...     
  }
</script>



{% endhighlight %}







The following screenshot displays the customization of Context menu in **TreeGrid** control.

{% include image.html url="\js\TreeGrid\concepts-and-features\context-menu_images\context-menu_img2.png" Caption="Figure 30: Customization of Context menu"%}





