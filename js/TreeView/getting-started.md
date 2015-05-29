---
layout: post
title: getting-started
description: getting started
platform: js
control: TreeView
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **TreeView** in your application with **JavaScript** and **ASP.NET MVC**.

## Create your first TreeView  in JavaScript

The **Essential JavaScript TreeView** property represents hierarchical data in a tree-like structure. **TreeView** allows you to edit, drag items to other **TreeView**, add check boxes, etc. You can refer the following section, to customize **TreeView** in a real time Mail Box Scenario that helps you to show items in a Mailbox with necessary features of **TreeView** property. The following screenshot demonstrates the functions of **TreeView** property with Drag and Drop option.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img1.png" Caption="Figure 1:TreeView "%}

In the above screenshot, you can select the mailbox items. You can write the functions of the corresponding selected item.You can also Drag and Drop the item from one group to another with the help of **Drag and Drop** feature. You can use **splitter** control to split the mail options and its corresponding functions.

### Create the Splitter 

The **Essential JavaScript****Splitter** property is a **layout** control that allows you to divide a web page into distinct areas by using resizable panes. Many **Splitter** panes are created and placed inside the **Splitter** control where the split bars are inserted automatically in between the adjacent panes. For more information about the **Splitter** refer the following link: [http://help.syncfusion.com/ug/js/default.htm#!Documents/gettingstarted30.htm](http://help.syncfusion.com/ug/js/default.htm)

* Create an **HTML** file and add the following template in your application.



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- style sheet for default theme(flat azure) -->
<linkhref=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css"rel="stylesheet"/>
    <!--scripts-->
    <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"></script>
</head>
<body>
<!-- add the splitter and TreeView element here-->

</body>
</html>



{% endhighlight %}



* Add &lt;div&gt; element to render **Splitter**.



{% highlight html %}


        <div id="innerSpliter">
                    <div>
                        <div style="width: 250px">
                        </div>
                    </div>
                    <div>
                        <div class="cont"> </div>
                    </div>
                </div>


{% endhighlight %}



* Initialize **Splitter** element in **&lt;script&gt;** tag.



{% highlight js %}


<script type="text/javascript">

$(function () {
// document ready

// simple Splitter creation
         $("#innerSpliter").ejSplitter({
// setting height for the Splitter widget
                height: 250,
// setting width for the Splitter widget
                width: 601,
 // simple Pane Size creation
                properties: [{}, { paneSize: 300 }]

                });
});

</script>



{% endhighlight %}



* Execute the code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img2.png" Caption="Figure 2: Splitter"%}

### Configure TreeView inside the Splitter widget 

**Essential JavaScript****TreeView** widget renders built-in features like keyboard navigation, month navigation, animations and flexible API’s. **Essential JavaScript****TreeView** can be generated from UL LI elements, JSON data source or using OData service.

You can style the right pane and render **TreeView** by adding **&lt;div&gt;** element in the splitter **&lt;div&gt;** elements for the Mailbox application.



{% highlight html %}


         <div id="innerSpliter">
                    <div>
                        <div style="width: 180px">
                              <!-- Div elements for Treeview-->
                            <div id="mailboxTree">
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="cont">
                            <!-- Div elements for displaying the messages-->
                            <div class="mailHead">My Mail Box</div>
                            <div class="mailCont"> </div>
                        </div>
                    </div>
          </div> 



{% endhighlight %}



You can style the **Splitter** content using styles given in the following code example.



{% highlight css %}


<style type="text/css" class="cssStyles">

         /*Style Icons*/
        .cont
        {
            padding: 40px 0 0 10px;
            text-align: center;
        }

        .mailHead
        {
            font-weight: bolder;
        }
</style>



{% endhighlight %}



Add the **TreeView** initialization script inside the script section.



{% highlight js %}


<script type="text/javascript">

$(function () {
// document ready

// simple Splitter creation
         $("#innerSpliter").ejSplitter({
// setting height for the Splitter widget
                height: 250,
// setting width for the Splitter widget
                width: 601,
// simple Pane Size creation
                properties: [{}, { paneSize: 300 }]
                });
// simple TreeView creation
**$("#mailboxTree").ejTreeView();**
});

</script>



{% endhighlight %}



Execute the code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img3.png" Caption="Figure 3: Splitter with TreeView"%}

### Configure Data Source

Create a **JSON** Data Source for **TreeView** and initialize as follows.



{% highlight js %}


<script type="text/javascript">

var outlookicons = [
                   { id: 1, name: "MailBox", hasChild: true, expanded: true},
                   { id: 2, pid: 1, name: "Calendar" },
                   { id: 3, pid: 1, name: "Contacts" },
                   { id: 4, pid: 1, name: "DeletedItems" },
                   { id: 5, pid: 1, name: "Drafts" },
                   { id: 6, pid: 1, name: "Inbox", hasChild: true },
                   { id: 7, pid: 6, name: "Incidents" },
                   { id: 8, pid: 6, name: "Forums" },
                   { id: 9, pid: 6, name: "Issue Reports" },
                   { id: 10, pid: 1, name: "Junk E-mail" },
                   { id: 11, pid: 1, name: "Send Items" }
        ];
// document ready
$(function () {


// simple Splitter creation
         $("#innerSpliter").ejSplitter({
// setting height for the Splitter widget
                height: 250,
// setting width for the Splitter widget
                width: 601,
// simple Pane Size creation
                properties: [{}, { paneSize: 300 }]
                });
// simple TreeView creation
$("#mailboxTree").ejTreeView(
                {
// mapping JSON Data Source with the fields property of TreeView 
                    fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: outlookicons, expanded: "expanded" }
         });
});

</script>



{% endhighlight %}



Execute this code example to render **TreeView** with **JSON** Data Source.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img4.png" Caption="Figure 4: TreeView"%}

### Configure TreeView with Sprite Icons

You can design **TreeView to** look like the Mail options application. Create the Sprite **CSS** styles for using mail Icons from the following image source. The source image is taken from the following installed location. 

_**[Installed Drive]:\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\XX.X.X.XX\JavaScript\samples\web\images\mail\ mailicons.png**_

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img5.jpeg)_**Note: XX.X.X.XX represents the Essential Studio version number that you are using currently.**_



Copy the “**mailicons.png**” from the above location and paste it in the folder location of the **HTML** sample page. 





You can show the sprite image icons in **TreeView** loaded inside the **&lt;styles&gt;** tag, using the styles shown in the following code example.



{% highlight css %}

        .mailicon
        {
            background-image: url("mailicons.png");
            display: inline-block;
            overflow: hidden;
            background-repeat: no-repeat;
            text-align: center;
            vertical-align: middle;
            width: 20px;
            height: 18px;
        }
        .sprite-calendar
        {
            background-position: -25px -255px;
        }
        .sprite-contacts
        {
            background-position: -26px -429px;
        }
        .sprite-deleted
        {
            background-position: -24px -152px;
        }
        .sprite-drafts
        {
            background-position:-24px -83px;
        }
        .sprite-folder
        {
            background-position: -24px -464px;
        }
        .sprite-folders
        {
            background-position: -24px -222px;
        }

        .sprite-inbox
        {
            background-position: -25px -13px;
        }
        .sprite-junk
        {
            background-position: -23px -187px;
        }
        .sprite-notes
        {
            background-position: -26px -394px;
        }
        .sprite-outbox
        {
            background-position: 0 -414px;
            width: 16px;
            height: 16px;
        }
        .sprite-root
        {
            background-position: -25px -49px;
        }
        .sprite-sentitems
        {
            background-position: -26px -118px;
        }



{% endhighlight %}



Create a **JSON** Data Source for **TreeView** and initialize as follows.



{% highlight js %}


<script type="text/javascript">
var outlookicons = [
                 { id: 1, name: "MailBox", hasChild: true, expanded: true, spriteCssClass: "mailicon sprite-folder" },
                   { id: 2, pid: 1, name: "Calendar",spriteCssClass:"mailicon sprite-calendar" },
                   { id: 3, pid: 1, name: "Contacts",spriteCssClass:"mailicon sprite-contacts" },
                   { id: 4, pid: 1, name: "DeletedItems", spriteCssClass: "mailicon sprite-deleted" },
                   { id: 5, pid: 1, name: "Drafts", spriteCssClass: "mailicon sprite-drafts" },
                   { id: 6, pid: 1, name: "Inbox", hasChild: true, spriteCssClass: "mailicon sprite-inbox" },
                   { id: 7, pid: 6, name: "Incidents", spriteCssClass: "mailicon sprite-folder" },
                   { id: 8, pid: 6, name: "Forums", spriteCssClass: "mailicon sprite-folder" },
                   { id: 9, pid: 6, name: "Issue Reports", spriteCssClass: "mailicon sprite-folder" },
                   { id: 10, pid: 1, name: "Junk E-mail", spriteCssClass: "mailicon sprite-junk" },
                   { id: 11, pid: 1, name: "Send Items", spriteCssClass: "mailicon sprite-sentitems" }
   ];
$(function () {
// document ready
// simple Splitter creation
         $("#innerSpliter").ejSplitter({
// setting height for the Splitter widget
                height: 250,
// setting width for the Splitter widget
                width: 601,
// simple Pane Size creation
                properties: [{}, { paneSize: 300 }]
                });
// simple TreeView creation
$("#mailboxTree").ejTreeView(
                {
// mapping JSON Data Source with the fields property of TreeView 
                    fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: outlookicons, expanded: "expanded" }
         });
});
</script>



{% endhighlight %}



Execute the code example to render **TreeView** with Mail Icons.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img6.png" Caption="Figure 6: TreeView with mail icons"%}

### Set the Node Editing Option 	

To rename the mail folders, set **allowEdit** property to **“True”**. You can also use F2 key or double-click the node to rename the node.



{% highlight js %}


<script type="text/javascript">


$(function () {            
            // declaration

// simple Splitter creation
         $("#innerSpliter").ejSplitter({

// setting height for the Splitter widget
                height: 250,

// setting width for the Splitter widget
                width: 601,

// simple Pane Size creation
                properties: [{}, { paneSize: 300 }]

                });

  $("#mailboxTree").ejTreeView(
                {

// mapping JSON Data Source with the fields property of TreeView 
                    fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: outlookicons, expanded: "expanded" },

                    // Setting TreeNode Editing option to true
**allowEditing**: true

                });

      });

    </script>



{% endhighlight %}



> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img7.jpeg)_**Note : Refer to the previous example for datasource.**_



Execute this code example to render node editing.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img8.png" Caption="Figure 7: TreeView with Node Editing"%}

### Set the Drag and Drop Option 

You can **Drag and Drop** the folders anywhere inside the mailbox by setting the **allowDragAndDrop** to **tTrue**. 

Execute this code example to **Drag and Drop** the nodes anywhere within the **TreeView**.





{% highlight js %}


<script type="text/javascript">
$(function () {            
            // declaration
  $("#mailboxTree").ejTreeView(
                {
// mapping JSON Data Source with the fields property of TreeView 
                    fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: outlookicons, expanded: "expanded" },

                    // Setting TreeNode Editing option to true
                    allowEditing: true,

                    // Setting TreeView Drag and Drop option to true
**allowDragAndDrop**: true

                });      });
    </script>



{% endhighlight %}

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img9.jpeg)_**Note : Refer to the previous example for datasource.**_

### Configure Events for the TreeView

When you click on the Mailbox folder item, the corresponding navigation action is performed in the **select** event that is achieved by declaring the **select** event with the corresponding call back function.  You can rename the folder names and it is not renamed as empty. This validation process is done manually in the **inlineEditValidation** event.



{% highlight js %}


<script type="text/javascript">
$(function () {            
            // declaration
  $("#mailboxTree").ejTreeView(
                {
// mapping JSON Data Source with the fields property of TreeView 
                    fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: outlookicons, expanded: "expanded" },
                    // Setting TreeNode Editing option to true
                    allowEditing: true,         
                    // Setting TreeView Drag and Drop option to true
                   allowDragAndDrop: true,
                   // Setting TreeView with the select event for node selection
                   nodesSelect: "setAction",
                   // Setting TreeView inline edit validation event for node editing
**inlineEditValidation**: "validateFolder",
                });      });
        function validateFolder(args) {
            //write your code here for other folder creation process.
            if (args.newText === "") //Validate the modified text of mailfolder.

           {
               args.cancel = true;
               alert("Folder name cannot be renamed to empty. Please provide some name.");
           }
        } 
       function setAction(args) {
            //write your code here for other process.
            $(".mailHead").html(args.value);
            $(".mailCont").html("The Contents of <b>"+args.value+"</b> will be displayed here");
        } 
    </script>



{% endhighlight %}



> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img10.jpeg)_**Note: Refer to the previous example for datasource.**_ 



Execute the code example to render **TreeView**. When you select the mail folder in the **TreeView,** the corresponding action takes place by raising the **select** event. 



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img11.png" Caption="Figure 8: TreeView with Select Event"%}

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img12.jpeg)_**Note: The inline edit validation is done on the rising of “inlineEditValidation” event as in the screenshot as follows. The “inlineEditValidation” event rises only when the “allowEdit” property is set to True.**_

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img13.png" Caption="Figure 9: TreeView with Inline Validation Event"%}

### Add or Delete the Folders using Context Menu 

You can add or remove the nodes dynamically during runtime. It is achieved by adding the **Context Menu** option to the **TreeView**. In the **Context Menu**, you can configure add or remove the node functions to the **TreeView**. The following code example illustrates how to configure the **Context Menu** elements for the **TreeView.**



{% highlight html %}


       <!--Elements for the context menu -->

          <ul id="treeviewMenu">
              <li><a href="#">New Folder</a></li>
              <li><a href="#">Delete Folder</a></li>
          </ul>



{% endhighlight %}



Initialize the **Context Menu** in the script section. 



{% highlight js %}


<script type="text/javascript">
var nodeIndex = 1, treeviewObj, selectedNode;
$(function () {            
            // declaration
             // Please refer the previous sections for the Splitter and TreeView rendering

              // declaration for Context menu
                $("#treeviewMenu").ejMenu({
                menuType: ej.MenuType.ContextMenu, // Setting menu type
                openOnClick: false, // Setting the open on click to false
                contextMenuTarget: "#mailboxTree",// Setting the target Id for the menu

                click: "menuclick",// Setting the event on menu click
                beforeOpen: "beforeOpen" //Settings to perform action  before open
            }); 
          treeviewObj = $("#mailboxTree").data("ejTreeView");// Creating the treeview object
   });
        function validateFolder(args) {
            //write your code here for other folder creation process.
            if (args.newText === "") //Validate the modified text of mailfolder.
            {
                args.cancel = true;
                alert("Folder name cannot be renamed to empty. Please provide some name.");
            }
        }
       function setAction(args) {
            //write your code here for other process.
            $(".mailHead").html(args.value);
            $(".mailCont").html("The contents of <b>"+args.value+"</b> will be displayed here");
        } 
           //creating the treeview object before the context menu opens with the selected node
        function beforeOpen(args) {
            if (!$(args.target).hasClass("e-text"))
                args.cancel = true; //write your code here for other process.
            else {
                selectedNode = args.target;
                treeviewObj.selectNode(selectedNode); //selectNode method for treeview.
            }
        }
        function menuclick(args) {
            if (args.events.text == "New Folder") {
                 //creating the new node in the treeview using addNode method
                treeviewObj.addNode("New Folder" + nodeIndex, selectedNode);
                nodeIndex++;
            }
            else if (args.events.text == "Delete Folder") {
                 //Deleting the existing node in the treeview
                treeviewObj.removeNode(selectedNode);
            }
        }
    </script>



{% endhighlight %}



> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img14.jpeg)_**Note: Refer to the previous example for datasource.**_ 

The following screenshot displays adding a new folder in the **TreeView** using the **Context Menu**. You can right-click on the **TreeView** Node and select the new folder option in the **Context Menu** for the selected folder. A new folder is added as the child of the **Drafts** folder.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img15.png" Caption="Figure 10: TreeView with context menu"%}

The following screenshot illustrates adding a new folder under the **Drafts** folder. 

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img16.png" Caption="Figure 11: TreeView with new folder"%}



The following screenshot illustrates the deleting of new folder that is created as a child of the Forums folder. You can right-click on the **New Folder1** and select the **Delete Folder** option in the **Context Menu**.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img17.png" Caption="Figure 12: TreeView before deleting a folder"%}



The following screenshot displays the **TreeView** after deleting the folder that is created.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img18.png" Caption="Figure 13: TreeView after deleting the New Folder1"%}

## Create your first TreeView in MVC

The **Essential ASP.NET MVC TreeView** control represents hierarchical data in a tree-like structure. It allows you to edit, drag items to other **TreeView**, add check boxes, etc. In the following section, you can learn how to customize **TreeView** in a real time Mail Box Scenario that helps you to showcase items in a Mailbox with necessary features of **TreeView**. The following screenshot illustrates the functionality of **TreeView** with **Drag and Drop** option.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img19.png" Caption="Figure 14: Mailbox TreeView"%}

In the above screenshot, you can select the mailbox items and you can write the corresponding functions of the selected item. You can drag and drop the item from one group to another group using the **Drag and Drop** option. You can use the **Splitter** control to split the mail options and its corresponding functions.

**Create the Splitter** 

The **Essential ASP.NET MVC Splitter** is a layout control that allows you to divide a web page into distinct areas by using resizable panes. Many **Splitter** panes are created and placed inside the **Splitter** control and the split bars are inserted automatically between the adjacent panes. For more information about the **Splitter**you can refer the Splitter-Getting Started documentation.

1. Create a MVC Project and add necessary Dll’s and scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code example to the corresponding view page for rendering the **Splitter** window.



**[C#]**



@Html.EJ().Splitter("outer").Height("250").Width("601").Orientation(Orientation.Horizontal).PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;&lt;/div&gt;);

        p.Add().ContentTemplate(

            @&lt;div&gt;&lt;/div&gt;);        

    })





3. Execute the above code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img20.png" Caption="Figure 15: Splitter Window"%}

**Configure TreeView inside the Splitter widget** 

**Essential ASP.NET MVC TreeView** widget basically renders with built-in features like keyboard navigation with animations and flexible API’s. **Essential ASP.NET MVC TreeView** can be generated from UL LI elements, JSON data source or using OData service.

In this application, you can create the **TreeView** with the **JSON** data source. 

You can style the right pane and render **TreeView** by adding **&lt;div&gt;** element in the **Splitter****&lt;div&gt;** elements for the Mailbox application.

Add the following style section to render the **Splitter** layout.



**[CSS]**



&lt;style&gt;

        #outer

        {

            font-size: 14px;

            font-family:sans-serif;

        }

        .cont

        {

            padding: 40px 0 0 10px;

            text-align: center;

        }	

        .splitdiv

        {

            height:100%;

            padding-left:30px;

        }

   &lt;/style&gt;



Add **TreeView** initialization inside the **Splitter** section.



**[C#]**



@Html.EJ().Splitter("outer").Height("250").Width("601").Orientation(Orientation.Horizontal).PaneProperties(

        p =>

        {

            p.Add().ContentTemplate(

                @&lt;div class="splitdiv"&gt;

                  &lt;div&gt;

**@Html.EJ().TreeView("treeView")**

                  &lt;/div&gt; 

               &lt;/div&gt;);



            p.Add().ContentTemplate(

                @&lt;div&gt;

                        &lt;div class="cont"&gt;

                            &lt;!-- Div elements for displaying the messages--&gt;

                            <div class="mailHead">My Mail Box</div>

                            &lt;div class="mailCont"&gt; &lt;/div&gt;

                        &lt;/div&gt;

                    &lt;/div&gt;);        

             })





Execute the above code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img21.png" Caption="Figure 16: Splitter with Empty TreeView"%}

**Configure Data Source**

Create the **JSON** Data Source for **TreeView** and initialize as follows.

Add the following data list to bind in the controller page and define the corresponding data.



**[Model]**



public class Outlookitems

    {

       //Treeview data source should have Id, ParentId and Text as mandatory

        public int Id { get; set; }

       // ParentId takes the value of the parent nodes Id

        public int Pid { get; set; }

       //Text to be displayed in the treeview node

        public string Name { get; set; }

       //Set to true if node has children

        public bool HasChild { get; set; }

      //Set to true if node to be expanded initially

        public bool Expanded { get; set; }

      //Image icon for nodes taken from the sprite css classes

        public string SpriteCss { get; set; }

    }





**[Controller]**

//Refer the Model in the controller

using &lt;Applicationname&gt;.Models;



public ActionResult Index()

        {

            List<Outlookitems> items=new List<Outlookitems>();

            //List items for Mailbox treeview

            items.Add(new Outlookitems { Id = 1, Name = "MailBox", HasChild = true, SpriteCss = "mailicon sprite-root", Expanded = true });

            items.Add(new Outlookitems { Id = 2, Pid = 1, Name = "Calendar", SpriteCss = "mailicon sprite-calendar" });

            items.Add(new Outlookitems { Id = 3, Pid = 1, Name = "Contacts", SpriteCss = "mailicon sprite-contacts" });

            items.Add(new Outlookitems { Id = 4, Pid = 1, Name = "DeletedItems", SpriteCss = "mailicon sprite-deleted" });

            items.Add(new Outlookitems { Id = 5, Pid = 1, Name = "Drafts", SpriteCss = "mailicon sprite-drafts" });

            items.Add(new Outlookitems { Id = 6, Pid = 1, Name = "Inbox", SpriteCss = "mailicon sprite-inbox" });

            items.Add(new Outlookitems { Id = 7, Pid = 6, Name = "Incidents ", SpriteCss = "mailicon sprite-folder" });

            items.Add(new Outlookitems { Id = 8, Pid = 6, Name = "Forums ", SpriteCss = "mailicon sprite-folder" });

            items.Add(new Outlookitems { Id = 9, Pid = 6, Name = "Issue Reports ", SpriteCss = "mailicon sprite-folder" });

            items.Add(new Outlookitems { Id = 10, Pid = 1, Name = "Junk E-mail ", SpriteCss = "mailicon sprite-junk" });

            items.Add(new Outlookitems { Id = 11, Pid = 1, Name = "Sent Items ", SpriteCss = "mailicon sprite-sentitems" });

            ViewData["Items"] = items;

            return View();

        }





Add the following code example in the **Splitter** section to render the **TreeView** in the right side pane.



**[View]**

@* Refer the model in view page*@

@model IEnumerable< _Applicationname_.Models.Outlookitems>



@*TreeView code inside splitter section*@



@&lt;div class="splitdiv"&gt;

    &lt;div&gt;

        @Html.EJ().TreeView("treeView").**TreeViewFields**(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).**Id**("Id").**ParentId**("Pid").Text("Name").**HasChild**("HasChild").**Expanded**("Expanded"))

    &lt;/div&gt; 

&lt;/div&gt;);



Execute the above code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img22.png" Caption="Figure 17: TreeView"%}

**Configure TreeView with Sprite Icons**

To design the **TreeView** to****look like Mail options application, you can create the **Sprite****CSS** styles for using Mail Icons from the following image source. The source image is taken from the following installed location. 

_**[Installed Drive]:\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\XX.X.X.XX\MVC \Samples\web\Images\mail\ mailicons.png**_

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img23.jpeg)_**Note: XX.X.X.XX represents the Essential Studio version number that you are using currently.**_

Copy the “**mailicons.png**” from the above location and paste it in the folder location of the **HTML** sample page.

You can show the **Sprite** image icons in **TreeView** loaded inside the **&lt;styles&gt;** tag, using the styles shown in the following code example.







 &lt;style&gt;

.mailicon

        {

            background-image: url("../Images/mailicons.png");

            display: inline-block;

            overflow: hidden;

            background-repeat: no-repeat;

            text-align: center;

            vertical-align: middle;

            width: 20px;

            height: 18px;

        }

        .sprite-calendar

        {

            background-position: -25px -255px;

        }

        .sprite-contacts

        {

            background-position: -26px -429px;

        }

        .sprite-deleted

        {

            background-position: -24px -152px;

        }

        .sprite-drafts

        {

            background-position:-24px -83px;

        }

        .sprite-folder

        {

            background-position: -24px -464px;

        }

        .sprite-folders

        {

            background-position: -24px -222px;

        }



        .sprite-inbox

        {

            background-position: -25px -13px;

        }

        .sprite-junk

        {

            background-position: -23px -187px;

        }

        .sprite-notes

        {

            background-position: -26px -394px;

        }

        .sprite-outbox

        {

            background-position: 0 -414px;

            width: 16px;

            height: 16px;

        }

        .sprite-root

        {

            background-position: -25px -49px;

        }

        .sprite-sentitems

        {

            background-position: -26px -118px;

        }

&lt;/style&gt; 

@*TreeView code inside splitter section*@



@&lt;div class="splitdiv"&gt;

       &lt;div&gt;

           @Html.EJ().TreeView("treeView").TreeViewFields(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild").Expanded("expanded").**SpriteCssClass**("spriteCss"))

             &lt;/div&gt; 

        &lt;/div&gt;); 





Execute the above code to render the **TreeView** with Mail Icons.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img24.png" Caption="TreeView with Mail Icons"%}

**Set the Node Editing Option** 

To rename the mail folders, set **allowEdit** property to **True**. You can also use F2 key or double-click the node to rename the node.



@*TreeView code inside splitter section*@



    @&lt;div class="splitdiv"&gt;

      &lt;div&gt;

         @Html.EJ().TreeView("treeView").TreeViewFields(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild").Expanded("expanded").SpriteCssClass("spriteCss")).AllowEditing(true)

       &lt;/div&gt; 

    &lt;/div&gt;);





Execute the above code example to render node editing.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img25.png" Caption="Figure 20: TreeView with Node Editing"%}

**Set the Drag and Drop Option** 

In this application you can **Drag and Drop** the folders anywhere inside the mailbox by setting the **DragAndDrop** option to **True**. 

Execute the following code example to **Drag and Drop** the nodes anywhere within the **TreeView**.





@*TreeView code inside splitter section*@



    @&lt;div class="splitdiv"&gt;

       &lt;div&gt;

             @Html.EJ().TreeView("treeView").TreeViewFields(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild").Expanded("expanded").SpriteCssClass("spriteCss")).AllowEditing(true).**AllowDragAndDrop**(true)

       &lt;/div&gt; 

    &lt;/div&gt;);



**Configure Events for the TreeView**

When you click on the Mailbox folder item, the corresponding navigation action is performed in the **select** event and this is achieved by declaring the **select** event with the corresponding call back function.  You can rename the folder names and it is not renamed as empty. This validation process is done manually in the **inlineEditValidation** event.



@*TreeView code inside splitter section*@



@&lt;div class="splitdiv"&gt;

    &lt;div&gt;

@* mapping JSON Data Source with the fields property of TreeView with client side events for node selection and inline edit validation, by enabling the property AllowEdit  *@



      @Html.EJ().TreeView("treeView").TreeViewFields(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild").Expanded("expanded").SpriteCssClass("spriteCss")).AllowEditing(true).AllowDragAndDrop(true).**ClientSideEvents**(s=> s.Node**Select**("treeclicked").**InlineEditValidation**("validateFolder"))

    &lt;/div&gt; 

  &lt;/div&gt;);



&lt;script type="text/javascript"&gt;

    function **validateFolder**(args) {

            //write your code here for other folder creation process.

            if (args.newText === "") //Validate the modified text of mailfolder.

            {

                args.cancel = true;

                alert("Folder name cannot be renamed to empty. Please provide some name.");

            }

        }



    function **treeclicked**(args) {

        //write your code here for other process on selecting tree nodes.

      $(".mailHead").html(args.value);

 $(".mailCont").html("The Contents of &lt;b&gt;" + args.value + "&lt;/b&gt; will be displayed here");

      }

&lt;/script&gt;



Execute the above code example to render **TreeView**. When you select the mail folder in the **TreeView,** the corresponding action takes place by raising the **select** event. 





{% include image.html url="\js\TreeView\getting-started_images\getting-started_img26.png" Caption="Figure 21: TreeView with Select Event"%}



> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img27.jpeg)_**Note: The inline edit validation is done when “InlineEditValidation” event occurs, as in the screenshot as follows. The “InlineEditValidation” event rises only when the “AllowEditing” property is set to True.**_



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img28.png" Caption="Figure 22: TreeView with Inline Validation Event"%}

**Add or Delete the Folders using Context Menu** 

You can add or remove the nodes dynamically during runtime. It is achieved by adding the **Context Menu** option to the **TreeView**. In the **Context Menu**, you can configure add or remove the node functions to the **TreeView**. The following code example illustrates how to configure the **Context Menu** elements for the **TreeView.**

Initialize the **Context****Menu** in the **Splitter** section as follows.



@*TreeView code inside splitter section*@



       @&lt;div class="splitdiv"&gt;

           &lt;div&gt;

                @Html.EJ().TreeView("treeView").TreeViewFields(s => s.**Datasource**((IEnumerable<loadondemand>).ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild").Expanded("expanded").SpriteCssClass("spriteCss")).AllowEditing(true).AllowDragAndDrop(true).ClientSideEvents(s => s.NodeSelect("treeclicked").InlineEditValidation("validateFolder"))

             &lt;/div&gt;

       &lt;!-- Initialize Elements for the context menu --&gt;

            &lt;div&gt;

               @Html.EJ().Menu("treeviewMenu").Items(items =>

          {

              items.Add().Text("New Folder");

              items.Add().Text("Delete Folder");          }).OpenOnClick(false).MenuType(MenuType.**ContextMenu**).ContextMenuTarget("#treeView").**ClientSideEvents**(s => s.**Click**("menuclick").**BeforeOpen**("beforeOpen"))

                 &lt;/div&gt;           

&lt;/div&gt;);



Initialize the **Context Menu** in the script section to create new folder and delete folder.





&lt;script type="text/javascript"&gt;

var nodeIndex = 1, treeviewObj, selectedNode;



      //Refer code for Tree click event and node editing validation 

        function **beforeOpen**(args) {

//creating the treeview object before the context menu opens with the selected node



            treeviewObj = $("#treeView").data("ejTreeView");// Creating the treeview object

            if (!$(args.target).hasClass("e-text"))

                args.cancel = true; //write your code here for other process.

            else {

                selectedNode = args.target;

                treeviewObj.selectNode(selectedNode); //selectNode method for treeview.

            }

        }



        function **menuclick**(args) {

            treeviewObj = $("#treeView").data("ejTreeView");// Creating the treeview object

            if (args.events.text == "New Folder") {

                //creating the new node in the treeview using addNode method

                treeviewObj.addNode("New Folder" + nodeIndex, selectedNode);

                nodeIndex++;

            }

            else if (args.events.text == "Delete Folder") {

                //Deleting the existing node in the treeview

                treeviewObj.removeNode(selectedNode);

            }

        }

    &lt;/script&gt;



The following screenshot illustrates adding of new folder in the **TreeView** using the **Context Menu**. You can right-click on the **TreeView** Node and select the new folder option in the **Context Menu** for the selected folder. 



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img29.png" Caption="Figure 23: TreeView with context menu"%}



In the following screenshot the new folder is added as the child of the “Drafts” folder.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img30.png" Caption="Figure 24: TreeView with new folder"%}



The following screenshot illustrates the deleting of new folder that is created as a child of the “Drafts” folder. You can right-click **New Folder1** and select the **Delete Folder** option in the **Context Menu**.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img31.png" Caption="Figure 25: TreeView before deleting a folder"%}



The following screenshot displays the **TreeView** after deleting the folder that is created.

{% include image.html url="\js\TreeView\getting-started_images\getting-started_img32.png" Caption="Figure 26: TreeView after deleting the “New Folder 1”"%}

## Create your first TreeView  in ASP.NET 

The **Essential ASP.NET WebForms TreeView** property represents hierarchical data in a tree-like structure. **TreeView** allows you to edit, drag items to other **TreeView**, add check boxes, etc. Refer the following section, to customize **TreeView** in a real time Mail Box Scenario that helps you to show items in a Mailbox with necessary features of **TreeView** property. The following screenshot demonstrates the functions of **TreeView** property with Drag and Drop option.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img33.png" Caption="Figure 27: Mailbox TreeView"%}



In the above screenshot, you can select the mailbox items and you can write the corresponding functions of the selected item. You can drag and drop the item from one group to another group using the **Drag and Drop** option. You can use the **Splitter** control to split the mail options and its corresponding functions.

**Create the Splitter**  

The **Essential** **ASP.NET WebForms** **Splitter** is a layout control that allows you to divide a web page into distinct areas by using resizable panes. Many **Splitter** panes are created and placed inside the **Splitter** control and the split bars are inserted automatically between the adjacent panes. For more information about the splitter please refer the Splitter-Getting Started documentation.

1. Create a **WebForms** Project and add necessary Dll’s and scripts with the help of the given [WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code to the corresponding design page for rendering the **Splitter** window.



**[ASPX]**



&lt;div&gt;

**&lt;ej:Splitter Height="251" Width="601" ID="outersplitter" runat="server"&gt;**

            **&lt;ej:SplitPane&gt;**

                &lt;div class="splitdiv"&gt; &lt;/div&gt;

            **&lt;/ej:SplitPane&gt;**

            **&lt;ej:SplitPane&gt;**

                &lt;div&gt; &lt;/div&gt;

            **&lt;/ej:SplitPane&gt;**

        **&lt;/ej:Splitter&gt;**

&lt;/div&gt;



3. Execute the above code example to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img34.png" Caption="Figure 28: Splitter Window"%}

**Configure TreeView inside the Splitter widget** 

**Essential ASP.NET WebForms TreeView** widget basically renders with built-in features like keyboard navigation with animations and flexible API’s. **Essential ASP.NET WebForms** can be generated from UL LI elements, JSON data source or using OData service.

In this application, you can create the **TreeView** with the **JSON** data source. 

You can style the right pane and render **TreeView** by adding **&lt;div&gt;** element in the splitter **&lt;div&gt;** elements for the Mailbox application.

Add the following style section to render the **Splitter** layout.



**[CSS]**

    &lt;style type="text/css"&gt;

        #outersplitter

        {

            margin: 50px 0 0 50px;

        }

        .splitdiv

        {

            font-size: 14px;

            font-family: sans-serif;

        }

        .mailHead

        {

            font-weight: bold;

            text-align: center;

        }

        .cont {

            padding: 40px 0 0 10px;

            text-align: center;

        }

    &lt;/style&gt;



 Add **TreeView** initialization inside the **Splitter** section.



**[ASPX]**

&lt;ej:Splitter Height="250" Width="601" ID="outersplitter" runat="server"&gt;

            &lt;ej:SplitPane&gt;

                &lt;div class="splitdiv"&gt;

                    &lt;div&gt;

**&lt;ej:TreeView ID="Mailbox" runat="server"&gt;**

                        **&lt;/ej:TreeView&gt;**

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/ej:SplitPane&gt;

            &lt;ej:SplitPane&gt;

                &lt;div&gt;

                    &lt;div class="cont"&gt;

                        &lt;!-- Div elements for displaying the messages--&gt;

                        &lt;div class="mailHead"&gt;

                            My Mail Box</div>

                        &lt;div class="mailCont"&gt;

                        &lt;/div&gt;

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/ej:SplitPane&gt;

        &lt;/ej:Splitter&gt;



Execute the above code to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img35.png" Caption="Figure 29: Splitter with Empty TreeView"%}

**Configure Data Source**

Create the **JSON** Data Source for **TreeView** and initialize as follows.

 Add the following data list in the code behind and bind it to the treeview object using **DataSource** property. Map the corresponding fields to TreeView element using datafields.



**[Class]**

//Define a class in code behind page

public class TreeIconsDataSource

{

    public TreeIconsDataSource()    { }

    public TreeIconsDataSource(int _id, int _parentid, string _text, string _hasChild, string _expanded, string _spriteCssClass)

    {

        this.ID = _id;

        this.ParentID = _parentid;

        this.Text = _text;

        this.HasChild = _hasChild;

        this.Expanded = _expanded;

        this.SpriteCssClass = _spriteCssClass;

    }

  //Treeview data source should have Id, ParentId and Text as mandatory

    public int ID { get; set; }

    // ParentId takes the value of the parent nodes I

    public int ParentID { get; set; }

    //Text to be displayed in the treeview node

    public string Text { get; set; }

   //Set to true if node has children

    public string HasChild { get; set; }

   //Set to true if node to be expanded initially

    public string Expanded { get; set; }

   //Image icon for nodes taken from the sprite css classes

    public string SpriteCssClass { get; set; }



    public List<TreeIconsDataSource> GetTreeIconItems()

    {

        List<TreeIconsDataSource> data = new List<TreeIconsDataSource>();

        data.Add(new TreeIconsDataSource(1, 0, "MailBox", "true", "true", "mailicon sprite-root"));

        data.Add(new TreeIconsDataSource(2, 1, "Calendar", "", "", "mailicon sprite-calendar"));

        data.Add(new TreeIconsDataSource(3, 1, "Contacts", "", "", "mailicon sprite-contacts"));

        data.Add(new TreeIconsDataSource(4, 1, "Deleted Items", "", "", "mailicon sprite-deleted"));

        data.Add(new TreeIconsDataSource(5, 1, "Drafts", "", "", "mailicon sprite-drafts"));

        data.Add(new TreeIconsDataSource(6, 1, "Inbox", "true", "", "mailicon sprite-inbox"));

        data.Add(new TreeIconsDataSource(7, 6, "Incidents", "", "", "mailicon sprite-folder"));

        data.Add(new TreeIconsDataSource(8, 6, "Forums", "", "", "mailicon sprite-folder"));

        data.Add(new TreeIconsDataSource(9, 6, "Issues", "", "", "mailicon sprite-folder"));

        data.Add(new TreeIconsDataSource(10, 1, "Junk E-mail", "", "", "mailicon sprite-junk"));

         data.Add(new TreeIconsDataSource(12, 10, "Forums", "", "", "mailicon sprite-folder"));

        data.Add(new TreeIconsDataSource(11, 1, "Sent items", "", "", "mailicon sprite-sentitems"));

        return data;

    }

}

//Map the created list data to DataSource property of TreeView

protected void Page_Load(object sender, EventArgs e)

 {

   this.Mailbox**.DataSource** = new TreeIconsDataSource().GetTreeIconItems().ToList();

 }







Add the following code in the **Splitter** section to render the **TreeView** in the right side pane.



**[ASPX]**

                   &lt;%-- TreeView code inside splitter--%&gt;

  &lt;div class="splitdiv"&gt;

      &lt;div&gt;  

    &lt;%-- Map the corresponding TreeView Fields to DataSource items--%&gt;           



<ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded">

    &lt;/ej:TreeView&gt;

       &lt;/div&gt;

  &lt;/div&gt;





Execute the above code to render the following output.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img36.png" Caption="Figure 30: TreeView"%}

**Configure TreeView with Sprite Icons**

To design the **TreeView** look like Mail options application, you can create the **Sprite** CSS styles for using Mail Icons from the following image source. The source image is taken from the following installed location. 

_**[Installed Drive]:\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\XX.X.X.XX\Web \Samples\web\Content\images\mail\ mailicons.png**_

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img37.jpeg)_**Note: XX.X.X.XX represents the Essential Studio version number that you are using currently.**_

Copy the “**mailicons.png**” from the above location and paste it in the folder location of the **HTML** sample page.

You can show the **Sprite** image icons in **TreeView** loaded inside the **&lt;styles&gt;** tag, using the styles shown in the following code sample.



**[CSS]**

&lt;style type="text/css"&gt;

        .mailicon

        {

            background-image: url("/Images/mailicons.png");

            display: inline-block;

            overflow: hidden;

            background-repeat: no-repeat;

            text-align: center;

            vertical-align: middle;

            width: 20px;

            height: 18px;

        }

        .sprite-calendar

        {

            background-position: -25px -255px;

        }

        .sprite-contacts

        {

            background-position: -26px -429px;

        }

        .sprite-deleted

        {

            background-position: -24px -152px;

        }

        .sprite-drafts

        {

            background-position:-24px -83px;

        }

        .sprite-folder

        {

            background-position: -24px -464px;

        }

        .sprite-folders

        {

            background-position: -24px -222px;

        }



        .sprite-inbox

        {

            background-position: -25px -13px;

        }

        .sprite-junk

        {

            background-position: -23px -187px;

        }

        .sprite-notes

        {

            background-position: -26px -394px;

        }

        .sprite-outbox

        {

            background-position: 0 -414px;

            width: 16px;

            height: 16px;

        }

        .sprite-root

        {

            background-position: -25px -49px;

        }

        .sprite-sentitems

        {

            background-position: -26px -118px;

        }



    &lt;/style&gt;



[ASPX]

                &lt;%-- TreeView code inside splitter--%&gt;

  &lt;div class="splitdiv"&gt;

     &lt;div&gt;                       



       <ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded" DataSpriteCssField="SpriteCssClass">

    &lt;/ej:TreeView&gt;

      &lt;/div&gt;

  &lt;/div&gt;



Execute the above code to render the **TreeView** with Mail Icons.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img38.png" Caption="Figure 32: TreeView with Mail Icons"%}

**Set the Node Editing Option** 

To rename the mail folders, set **AllowEditing** property to “**true**”. You can also use F2 key or double-click the node to rename the node.



**[ASPX]**

     &lt;%-- TreeView code inside splitter--%&gt;

&lt;div class="splitdiv"&gt;

    &lt;div&gt;                       



        <ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded" DataSpriteCssField="SpriteCssClass" AllowEditing="true">

    &lt;/ej:TreeView&gt;

    &lt;/div&gt;

&lt;/div&gt;





Execute the above code example to render node editing.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img39.png" Caption="Figure 33: TreeView with Node Editing"%}

**Set the Drag and Drop Option** 

In this application you can **Drag and Drop** the folders anywhere inside the mailbox by setting the **AllowDragAndDrop** option to **True**. 

Execute the following code example to **Drag and Drop** the nodes anywhere within the **TreeView**.



**[ASPX]**

    &lt;%-- TreeView code inside splitter--%&gt;

&lt;div class="splitdiv"&gt;

    &lt;div&gt;                       



        <ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded" DataSpriteCssField="SpriteCssClass" Width="400px" AllowEditing="true" AllowDragAndDrop="true">

    &lt;/ej:TreeView&gt;

        &lt;/ej:TreeView&gt; 

     &lt;/div&gt;	

&lt;/div&gt;



**Configure Events for the TreeView**

When you click on the Mailbox folder item, the corresponding navigation action is performed in the **ClientSideOnNodeSelected** event and this is achieved by declaring the **ClientSideOnNodeSelected** event with the corresponding call back function.  You can rename the folder names and it is not renamed as empty. This validation process is done manually in the **ClientSideOnInlineEditValidation** event.



&lt;!-- TreeView code inside splitter--&gt;

&lt;div class="splitdiv"&gt;

    &lt;div&gt;                       



          <ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded" DataSpriteCssField="SpriteCssClass" Width="400px" AllowEditing="true" AllowDragAndDrop="true" ClientSideOnNodeSelected="treeClicked" ClientSideOnInlineEditValidation="validateFolder">

    &lt;/ej:TreeView&gt;

         &lt;/ej:TreeView&gt; 

     &lt;/div&gt;

&lt;/div&gt;





Initialize the script section to validate editing and select operation.



**[Script]**

&lt;script type="text/javascript"&gt;

        function validateFolder(args) {

            //write your code here for other folder creation process.

            if (args.newText === "") //Validate the modified text of mailfolder.

            {

             args.cancel = true;

             alert("Folder name cannot be renamed to empty. Please provide some name.");

            }

        }



        function treeClicked(args) {

            //write your code here for other process on selecting tree nodes.

            $(".mailHead").html(args.value);

            $(".mailCont").html("The Contents of &lt;b&gt;" + args.value + "&lt;/b&gt; will be displayed here");

        }

&lt;/script&gt;





Execute the above code example to render **TreeView**. When you select the mail folder in the **TreeView,** the corresponding action takes place by raising the **ClientSideOnNodeSelected** event. 



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img40.png" Caption="Figure 34: TreeView with Select Event"%}

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img41.jpeg)_**Note: The inline edit validation is done when “ClientSideOnInlineEditValidation” event occurs, as in the screen shot as follows. The “ClientSideOnInlineEditValidation” event rises only when the “AllowEditing” property is set to True.**_



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img42.png" Caption="Figure 35: TreeView with Inline Validation Event"%}

**Add or Delete the Folders using Context Menu** 

You can add or remove the nodes dynamically during runtime. It is achieved by adding the **Context Menu** option to the **TreeView**. In the **Context Menu**, you can configure add or remove the node functions to the **TreeView**. The following code example illustrates how to configure the **Context Menu** elements for the **TreeView.**

Initialize the **Context****Menu** in the **Splitter** section as follows.



**[ASPX]**

                      &lt;!-- TreeView code inside splitter--&gt;

&lt;div class="splitdiv"&gt;

    &lt;div&gt;                       



        <ej:TreeView ID="Mailbox" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

                            DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded" DataSpriteCssField="SpriteCssClass" Width="400px" AllowEditing="true" AllowDragAndDrop="true" ClientSideOnNodeSelected="treeClicked" ClientSideOnInlineEditValidation="validateFolder">

         &lt;/ej:TreeView&gt;

    &lt;/div&gt;

             &lt;!-- Initialize Elements for the context menu --&gt;

    &lt;div&gt;

**<ej:Menu ID="treeviewMenu" runat="server" MenuType="ContextMenu" ContextMenuTarget="#**LayoutSection_ControlsSection_outersplitter_ctl00_Mailbox**" OpenOnClick="false"** 

        **ShowSubLevelArrows="true" ClientSideOnBeforeContextOpen="beforeOpen" ClientSideOnClick="menuClick">**

            **&lt;Items&gt;&lt;ej:MenuItem Id="New" Text="New Folder"&gt;****&lt;/ej:MenuItem&gt; &lt;/Items&gt;**

            **&lt;Items&gt;&lt;ej:MenuItem Id="Delete" Text="Delete Folder"&gt;****&lt;/ej:MenuItem&gt;&lt;/Items&gt;**

        **&lt;/ej:Menu&gt;**

    &lt;/div&gt;

&lt;/div&gt;



Initialize the **Context Menu** in the script section to create new folder and delete folder.



**[Script]**

&lt;script type="text/javascript"&gt;

        var nodeIndex = 1, treeviewObj, selectedNode; 

        //Refer code for Tree click event and node editing validation 

        function beforeOpen(args) {

   //creating the treeview object before the context menu opens with the selected node

        treeviewObj = $("#LayoutSection_ControlsSection_outersplitter_ctl00_Mailbox").data("ejTreeView"); // Creating the treeview object

            if (!$(args.target).hasClass("e-text"))

                args.cancel = true; //write your code here for other process.

            else {

                selectedNode = args.target;

                treeviewObj.selectNode(selectedNode); //selectNode method for treeview.

            }

        }

        function menuClick(args) {

        treeviewObj = $("#LayoutSection_ControlsSection_outersplitter_ctl00_Mailbox").data("ejTreeView"); // Creating the treeview object

            if (args.events.ID == "New") {

                //creating the new node in the treeview using addNode method

                treeviewObj.addNode("New Folder" + nodeIndex, selectedNode);

                nodeIndex++;

            }

            else if (args.events.ID == "Delete") {

                //Deleting the existing node in the treeview

                treeviewObj.removeNode(selectedNode);

                $(".mailHead").html("My Mail Box");

                $(".mailCont").html("");

            }

        }

&lt;/script&gt;



The following screenshot illustrates adding of new folder in the **TreeView** using the **Context Menu**. You can right-click on the **TreeView** Node and select the new folder option in the **Context Menu** for the selected folder. 



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img43.png" Caption="Figure 36: TreeView with context menu"%}



In the following screenshot displays the new folder is added as the child of the “Drafts” folder.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img44.png" Caption="Figure 37: TreeView with new folder"%}



The following screenshot illustrates the deleting of new folder that is created as a child of the “Drafts” folder. You can right-click on the **New Folder1** and select the **Delete Folder** option in the **Context Menu**.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img45.png" Caption="Figure 38: TreeView before deleting a folder"%}



The following screenshot displays the **TreeView** after deleting the folder that is created.



{% include image.html url="\js\TreeView\getting-started_images\getting-started_img46.png" Caption="Figure 39: TreeView after deleting the “New Folder 1”"%}

