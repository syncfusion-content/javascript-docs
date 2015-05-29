---
layout: post
title: getting-started-
description: getting started 
platform: js
control: Menu
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Menu** control in your application with **JavaScript**, **ASP.NET MVC** and **ASP.NET**.

## Create Syncfusion Menu in JavaScript

The **Essential JavaScript****Menu** supports displaying a **Menu** of list-out items. This **Menu** is based on ul-li hierarchy, where the sub-list items are rendered as the sub-menu items. The **Menu** control can also be rendered with local and remote data source.  From the following guidelines, you can learn how to customize the **Menu** control for a website. In this case, **Syncfusion’s** website **Menu** is discussed. The following screenshot displays the appearance of **Menu**.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img1.png" Caption="Figure 1: Syncfusion Menu"%}

**Create a Menu**

**Essential JavaScript****Menu** widgets are basically provided with built-in features like keyboard navigation, show and hide **Menu** items with animations, and flexible API’s. From the following guidelines, you can learn how to render **Menu** control with Remote data source value.

* Create an **HTML** file and add the following template into it for **Menu** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
          <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
<!-- add menu element here -->
</body>
</html>


{% endhighlight %}





* Adding **Ul** element for **Menu** rendering.



{% highlight html %}


<ul id="syncfusionProducts"></ul>



{% endhighlight %}



* Initialize the **Menu** control in &lt;script&gt; tag. 

{% highlight js %}


<script type="text/javascript">
        $(function () {// document ready
// simple Menu control creation
            $("#syncfusionProducts").ejMenu();
        });
</script>


{% endhighlight %}



* Output of the above steps.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img2.png" Caption="Figure 2: Essential JavaScript Menu without  Menu item"%}

**Configure parent Menu items**

Every **Menu** has a list of **Menu** items with list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the root level elements of **Menu** control with Remote data source value.  Initialize the **Menu** with data source value as illustrated in the following code example. 

{% highlight js %}


<script type="text/javascript">
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
              text: "InfoText", // Mapping text field with the data source items.

               } 

})
       });
</script>


{% endhighlight %}



The following screenshot displays output.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img3.png" Caption="Figure 3: Essential JavaScript Menu without  sub menu item"%}

**Initialize sub-level Menu items**

Every **Menu** items have a list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the sub level items of **Menu** control. The **parentIdD** field is used to map root level **Menu** item to its sub level **Menu** item.								

The following code example describes how to initialize first level sub menu items of product **Menu** item.

{% highlight js %}


<script type="text/javascript">
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
</script>


{% endhighlight %}



Execute the above code example to render the following output.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img4.png" Caption="Figure 4: Essential JavaScript Menu with sub menu item"%}

**Define multiple level Menu items**

You can define the sub-menu items to multiple levels in **Menu** control. You need to specify the parent Id value to render sub level **Menu** item for the **Menu** items.

To initialize multiple levels sub menu items, use the following code example.


{% highlight js %}


<script type="text/javascript">

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
</script>


{% endhighlight %}



The following screenshot is the output.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img5.png" Caption="Figure 5: Essential JavaScript Menu with multiple level  sub menu item"%}

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items through online data source. You can simply customize the **Menu** widget in an efficient manner.

In summary of this getting started, you have now simulated the **Syncfusion’s** website **Menu** with Essential **JavaScript****Menu**. You have utilized and learnt the appearance customization etc.  

## Create Syncfusion Menu in MVC

The **Essential ASP.NET MVC Menu** control supports displaying a **Menu** out of list items. The **Menu** is based on ul and li hierarchy, where the sub list items are rendered as the sub-menu items .The **Menu** control can also render with local and remote data source. The following section explains you on how to customize the **Menu** control for a website. 

The following screenshot illustrates the appearance of **Syncfusion**’s website **Menu**.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img6.png" Caption="Figure 6: Syncfusion Menu"%}

The **Menu** items in the above screenshot allow you to navigate through multiple menus in a page and select an item. It has a hierarchical structure with sub menus. 

**Create a Menu**

**Essential ASP.NET MVC Menu** widget basically renders with built-in features like keyboard navigation, show and hides **Menu** items with animations and flexible API’s. Refer the following guidelines to render **Menu** control with Local data source value.

1. You can create a **MVC** Project and add the necessary Dll’s and scripts using the[MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)Documentation.



2. Add the following code example to the corresponding view page for **Menu** rendering.



**[C#]**



@Html.EJ().Menu("SyncfusionProducts")



3. Execute the above code to render Empty **Menu** bar.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img7.png" Caption="Figure 7: Essential ASP.NET MVC Menu without menu item"%}

**Configure Parent Menu items**

Each **Menu** consists of a list of **Menu** items with list of sub level **Menu** item. Refer the following guidelines to initialize the root level elements of **Menu** control with Remote data source value. **RootLevelItems** data service is created to define the root level **Menu** items, sub items and InnerItems data services to initialize the sub level and inner sub levels and both can be referred from the following service location. In **Menu** Widgets mention the **RootLevelItem** Data Source in the **Datasource** property.

[http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/](http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/)

To navigate the clicked **Menu** item to a specific URL, define the navigation URL to each **Menu** item and also map to each **Menu** item with specified link through **LinkAttribute** field property.

Initialize the **Menu** with data source value as follows. 



**[View]**

@Html.EJ().Menu("SyncfusionProducts").**MenuFields**(f=> f.**Datasource**(d=> d.**URL**("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).**Query**("ej.Query().from('RootLevelItems')").**Id**("InfoID").**Text**("InfoText").**LinkAttribute**("InfoUrl"))



Execute the above code to display the Root level **Menu** items.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img8.png" Caption="Figure 8: Essential ASP.NET MVC Menu without sub menu item"%}

**Initialize sub-level Menu items**

Each **Menu** items consist of list of sub level **Menu** items. Refer the following guidelines to initialize the sub level items of **Menu** control. The **ParentId****field** property maps root level **Menu** item to its sub level **Menu** item. In **Menu** Widgets mention the **RootLevelItems** and **SubLevelItems** Data Source in the **Datasource** property. The **Child field** property is used to define sub level **Menu** items of parent **Menu** item.							

The following code example explains the initialization of first level sub menu items of **Menu** control.


**[View]**

@Html.EJ().Menu("SyncfusionProducts").MenuFields(f=> f.Datasource(d=> d.URL("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).Query("ej.Query().from('RootLevelItems')").Id("InfoID").Text("InfoText").LinkAttribute("InfoUrl").**Child**(c=>c.**Datasource**(cd=> cd.**URL**("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).**TableName**("SubItems").**Id**("SubItemID").**ParentId**("InfoID").**LinkAttribute**("SubItemUrl").**Text**("SubItemText")))





Execute the above code to render the following output.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img9.png" Caption="Figure 9: Essential ASP.NET MVC Menu with sub menu item"%}

**Define multiple level Menu items**

You can render sub **menu item** to multiple level in **Menu** control. In **Menu** Widgets, mention the **InnerItems** Data Source in the **Datasource** property. The **child field** property is used to define the sub level **Menu** item of parent **Menu**. Specify the **ParentId** value to render sub level **Menu** item for the **Menu** item. Each Level **Menu** item have Child field to define the child level **Menu** item. 

The following code example explains the initialization of multiple level sub menu items.


**[View]**



@Html.EJ().Menu("SyncfusionProducts").MenuFields(f=> f.Datasource(d=> d.URL("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).Query("ej.Query().from('RootLevelItems')").Id("InfoID").Text("InfoText").LinkAttribute("InfoUrl").Child(c=>c.Datasource(cd=> cd.URL("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).TableName("SubItems").Id("SubItemID").ParentId("InfoID").LinkAttribute("SubItemUrl").Text("SubItemText").**Child**(cc=>cc.**Datasource**(ccd=> ccd.**URL**("http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/")).**TableName**("InnerItems").**Id**("InnerSubItemID").**ParentId**("SubItemID").**Text**("InnerSubItemText").**LinkAttribute**("InnerSubItemUrl"))))



Execute the above code to render the multiple sub menus in a hierarchy

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img10.png" Caption="Figure 10: Essential ASP.NET MVC Menu with multiple level  sub menu item"%}

## Create Syncfusion Menu in ASP.NET

The **ASP.NET****Menu** supports you to display a **Menu** of list-out items. This **Menu** is based on **UL-LI** hierarchy, where the sub-list items can be rendered as the sub-menu items. You can also render the **Menu** control with local and remote data source.  From the following guideline, you can learn how to customize the **Menu** control for a website. In this case, **Syncfusion’s** website **Menu** is used to explain this topic. The following screenshot displays the appearance of **Menu**.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img11.png" Caption="Figure 11: Syncfusion Menu"%}

**Create a Menu**

**ASP.NET****Menu** basically provided with built-in features like keyboard navigation, show and hide **Menu** items with animations, and flexible **API’s**. From the following guideline, you can learn how to render **Menu** control.

You can create an **ASP Project** and add necessary **Dll** and script with the help of the given [ASP-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

Add the following code to the corresponding **ASPX** page for **Menu** rendering.



**[ASPX]**

    &lt;div class="frame"&gt;

        &lt;ej:Menu ID="SyncfusionProducts" runat="server" Width="615px"&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt;



Initialize the **Menu** control with the following **CSS.**



**[CSS]**

&lt;style type="text/css"&gt;

        .frame

        {

            border: 1px solid #BBBCBB;

            border-radius: 10px 10px 10px 10px;

            padding: 50px;

            margin-top: 40px;

            width: 700px;

            height: 50px;

            margin-left: 100px;

        }

    &lt;/style&gt;



Output of above steps

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img12.png" Caption="Figure 12: Essential JavaScript Menu without  Menu item"%}

**Configure parent Menu items**

Every **Menu** has a list of **Menu** items with list of sub level **Menu** items. From the following guide line, you can learn how to initialize the root level elements of **Menu** control with **MenuItem** binding.  Initialize the **Menu** with **MenuItem** as illustrated in the following code example. 



**[ASPX]**

&lt;div class="frame"&gt;

        &lt;ej:Menu ID="SyncfusionProducts" Width="615" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Id="Products" Text="Products"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Support" Text="Support"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Purchase" Text="Purchase"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Downloads" Text="Downloads"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Resources" Text="Resources"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Company" Text="Company"&gt;

                &lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt;



The following screenshot displays the resultant output.

{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img13.png" Caption="Figure 13: Essential JavaScript Menu without  sub menu item"%}



**Initialize sub-level Menu items**

Every **Menu** items can have a list of sub level **Menu** items. From the following guideline, you can learn how to initialize the sub level items of **Menu** control. Add **MenuItem** inside Items to create a sub child.					

The following code example describes how to initialize first level sub menu items of product **Menu** item.



**[ASPX]**

    &lt;div class="frame"&gt;

        &lt;ej:Menu ID="SyncfusionProducts" Width="515" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Id="Products" Text="Products"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="ASP.NET"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="ASP.NET MVC"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Mobile MVC"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Silverlight"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Windows Forms"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Windows Phone"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="WinRT (XMAL)"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="WPF"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Orubase Studio"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Support" Text="Support"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Direct-Trac Support"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Community Forums"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Knowledge Base"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Online Documentation"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Services"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Community Forums"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Purchase" Text="Purchase"&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Downloads" Text="Downloads"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Evaluation"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Free E-Books"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Metro Studio"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Latest Version"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Version History"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Resources" Text="Resources"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Technology Resource Portal"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Case Studies"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Bouchers & Datasheets"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="FAQ"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

                &lt;ej:MenuItem Id="Company" Text="Company"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="About Us"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Company Blog"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Technical Blog"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Newsletter"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Partners"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Locations"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Contact Us"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt;



Execute the above code to render the following output.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img14.png" Caption="Figure 14: Essential JavaScript Menu with sub menu item"%}

**Define multiple level Menu items**

You can define the sub-menu items to multiple levels in **Menu** control. You need to add **MenuItem** inside Items to render sub level **Menu** item for the **Menu** item.

To initialize multiple level sub menu items use the following code example.



**[ASPX]**    

&lt;%--Use the below codes with above HTML --%&gt;

            &lt;ej:MenuItem Id="Support" Text="Support"&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Direct-Trac Support"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Community Forums"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Knowledge Base"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Online Documentation"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Services"&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Consulting"&gt;

                                &lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                            &lt;Items&gt;

                                &lt;ej:MenuItem Text="Taining"&gt;

                                &lt;/ej:MenuItem&gt;

                            &lt;/Items&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:MenuItem Text="Community Forums"&gt;

                        &lt;/ej:MenuItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:MenuItem&gt;   





The following screenshot is the resultant output.



{% include image.html url="\js\Menu\getting-started-_images\getting-started-_img15.png" Caption="Figure 15: Essential JavaScript Menu with multiple level  sub menu item"%}

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items. You can simply customize the **Menu** in an efficient manner.

