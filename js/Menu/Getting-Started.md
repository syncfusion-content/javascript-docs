---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: Menu
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Menu** control in your application with **JavaScript**.

## Create Syncfusion Menu in JavaScript

The **Essential JavaScript** **Menu** supports displaying a **Menu** of list-out items. This **Menu** is based on ul-li hierarchy, where the sub-list items are rendered as the sub-menu items. The **Menu** control can also be rendered with local and remote data source.  From the following guidelines, you can learn how to customize the **Menu** control for a website. In this case, **Syncfusion’s** website **Menu** is discussed. The following screenshot displays the appearance of **Menu**.



{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img1.png" Caption="Syncfusion Menu"%}

**Create a Menu**

**Essential JavaScript** **Menu** widgets are basically provided with built-in features like keyboard navigation, show and hide **Menu** items with animations, and flexible API’s. From the following guidelines, you can learn how to render **Menu** control with Remote data source value.

Create an **HTML** file and add the following template into it for **Menu** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add menu element here -->
</body>
</html>



{% endhighlight %}





Adding **Ul** element for **Menu** rendering.



{% highlight html %}


<ul id="syncfusionProducts"></ul>



{% endhighlight %}



Initialize the **Menu** control in &lt;script&gt; tag. 

{% highlight js %}

        $(function () {
            // document ready
            // simple Menu control creation
            $("#syncfusionProducts").ejMenu();
        });
        

{% endhighlight %}



Output of the above steps.

{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img2.png" Caption="Essential JavaScript Menu without  Menu item"%}

**Configure parent Menu items**

Every **Menu** has a list of **Menu** items with list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the root level elements of **Menu** control with Remote data source value.  Initialize the **Menu** with data source value as illustrated in the following code example. 

{% highlight js %}


        $(function () {// document ready
            // DataManager creation

            var dataManger = ej.DataManager({

                // Assign the Remote data service path to url

                url: "http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/"
            });

            // used to retrieve the items from online data.

            var query = ej.Query().from("RootLevelItems");
            // simple Menu control creation
            $("#syncfusionProducts").ejMenu({

                // fields property used to bind the data source and also it includes list of field members such as id, text, parentId to render menu control. 

                fields: {
                    dataSource: dataManger, //Assign data source value to dataSource property
                    query: query,
                    id: "InfoID", // Mapping id fields with the data source items.
                    text: "InfoText" // Mapping text field with the data source items.

                }

            })
        });


{% endhighlight %}



The following screenshot displays output.

{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img3.png" Caption="Essential JavaScript Menu without  sub menu item"%}

**Initialize sub-level Menu items**

Every **Menu** items have a list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the sub level items of **Menu** control. The **parentId** field is used to map root level **Menu** item to its sub level **Menu** item.								

The following code example describes how to initialize first level sub menu items of product **Menu** item.

{% highlight js %}


        $(function () {// document ready
            // Define the DataManager and Query as per Above Code Snippet.
            // simple Menu control creation

            $("#syncfusionProducts").ejMenu({
                fields: {
                    dataSource: dataManger, query: query, id: "InfoID", text: "InfoText",
                    //Define the Child level Menu Items through below child field
                    child: {
                        //Define the Sub level Menu Itmes Source
                        dataSource: dataManger,
                        tableName: "SubItems", // Sub Level Items
                        // parentID field used to map root level menu item to its sub level menu item.
                        id: "SubItemID", parentId: "InfoID", text: "SubItemText"
                    }
                }
            });
        });


{% endhighlight %}



Execute the above code example to render the following output.



{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img4.png" Caption="Essential JavaScript Menu with sub menu item"%}

**Define multiple level Menu items**

You can define the sub-menu items to multiple levels in **Menu** control. You need to specify the parent Id value to render sub level **Menu** item for the **Menu** items.

To initialize multiple levels sub menu items, use the following code example.


{% highlight js %}


        $(function () {// document ready
            // Define the DataManager and Query as per Above Code Snippet.
            $("#syncfusionProducts").ejMenu({
                fields: {
                    dataSource: dataManger,
                    query: query,
                    id: "InfoID", text: "InfoText",
                    child: {
                        //Define the Sub level Menu Items
                        dataSource: dataManger,
                        tableName: "SubItems", // Sub Level Items table name
                        id: "SubItemID", parentId: "InfoID", text: "SubItemText",

                        child: {
                            //Define the Inner Sub level Menu Items
                            dataSource: dataManger,
                            tableName: "InnerItems",// Inner Sub Level Items table name
                            // parentID field used to map root level menu item to its sub level menu item.
                            id: "InnerSubItemID", parentId: "SubItemID", text: "InnerSubItemText"
                        }
                    }
                }
            });
        });


{% endhighlight %}



The following screenshot is the output.



{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img5.png" Caption="Essential JavaScript Menu with multiple level  sub menu item"%}

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items through online data source. You can simply customize the **Menu** widget in an efficient manner.

In summary of this getting started, you have now simulated the **Syncfusion’s** website **Menu** with **Essential JavaScript Menu**. You have utilized and learnt the appearance customization etc.  

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items. You can simply customize the **Menu** in an efficient manner.

