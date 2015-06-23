---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TreeView
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **TreeView** in your application with **JavaScript**.

## Create your first TreeView  in JavaScript

The **Essential JavaScript TreeView** property represents hierarchical data in a tree-like structure. **TreeView** allows you to edit, drag items to other **TreeView**, add check boxes, etc. You can refer the following section, to customize **TreeView** in a real time Mail Box Scenario that helps you to show items in a Mailbox with necessary features of **TreeView** property. The following screenshot demonstrates the functions of **TreeView** property with Drag and Drop option.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img1.png"%}

In the above screenshot, you can select the mailbox items. You can write the functions of the corresponding selected item.You can also Drag and Drop the item from one group to another with the help of **Drag and Drop** feature. You can use **splitter** control to split the mail options and its corresponding functions.

**Create the Splitter** 

The **Essential JavaScript Splitter** property is a **layout** control that allows you to divide a web page into distinct areas by using resizable panes. Many **Splitter** panes are created and placed inside the **Splitter** control where the split bars are inserted automatically in between the adjacent panes. For more information about the **Splitter** refer the following link: 

[http://help.syncfusion.com/ug/js/default.htm#!Documents/gettingstarted30.htm](http://help.syncfusion.com/ug/js/default.htm)

Create an HTML file and add the following template in your application.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
      <!-- style sheet for default theme(flat azure) -->
      <link href=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css"rel="stylesheet"/>
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


 Add &lt;div&gt; element to render Splitter.

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



 Initialize Splitter element in &lt;script&gt; tag.

{% highlight js %}

    $(function() {
        // document ready    
        // simple Splitter creation
        $("#innerSpliter").ejSplitter({
            height: 250,
            width: 601,
            // simple Pane Size creation       
            properties: [{}, {
                paneSize: 300
            }]
        });
    });


{% endhighlight %}


 Execute the code example to render the following output.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img2.png"%}

**Configure TreeView inside the Splitter widget** 

**Essential JavaScript TreeView** widget renders built-in features like keyboard navigation, month navigation, animations and flexible API’s. **Essential JavaScript TreeView** can be generated from UL LI elements, JSON data source or using OData service.

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

        $(function() {
            $("#innerSpliter").ejSplitter({
                height: 250,
                width: 601,
                properties: [{}, {
                    paneSize: 300
                }]
            });
            $("#mailboxTree").ejTreeView();
        });

{% endhighlight %}



Execute the code example to render the following output.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img3.png"%}

**Configure Data Source**

Create a **JSON** Data Source for **TreeView** and initialize as follows.

{% highlight js %}

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
    $(function() {
        $("#innerSpliter").ejSplitter({
            height: 250,
            width: 601,
            properties: [{}, {
                paneSize: 300
            }]
        });
        $("#mailboxTree").ejTreeView({
            // mapping JSON Data Source with the fields property of TreeView 
            fields: {
                id: "id",
                parentId: "pid",
                text: "name",
                hasChild: "hasChild",
                dataSource: outlookicons,
                expanded: "expanded"
            }
        });
    });

{% endhighlight %}



Execute this code example to render **TreeView** with **JSON** Data Source.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img4.png"%}

**Configure TreeView with Sprite Icons**

You can design **TreeView to** look like the Mail options application. Create the Sprite **CSS** styles for using mail Icons from the following image source. The source image is taken from the following installed location. 

**[Installed Drive]:**\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\XX.X.X.XX\JavaScript\samples\web\images\mail\ mailicons.png

> **Note**: XX.X.X.XX represents the Essential Studio version number that you are using currently.

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
    $(function() {
        $("#innerSpliter").ejSplitter({
            height: 250,
            width: 601,
            properties: [{}, {
                paneSize: 300
            }]
        });
        $("#mailboxTree").ejTreeView({
            // mapping JSON Data Source with the fields property of TreeView 
            fields: {
                id: "id",
                parentId: "pid",
                text: "name",
                hasChild: "hasChild",
                dataSource: outlookicons,
                expanded: "expanded"
            }
        });
    });


{% endhighlight %}



Execute the code example to render **TreeView** with Mail Icons.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img5.png"%}

**Set the Node Editing Option**

To rename the mail folders, set **allowEdit** property to **“True”**. You can also use F2 key or double-click the node to rename the node.

{% highlight js %}

    $(function() {
        $("#innerSpliter").ejSplitter({
            height: 250,
            width: 601,
            properties: [{}, {
                paneSize: 300
            }]
        });

        $("#mailboxTree").ejTreeView({
            // mapping JSON Data Source with the fields property of TreeView 
            fields: {
                id: "id",
                parentId: "pid",
                text: "name",
                hasChild: "hasChild",
                dataSource: outlookicons,
                expanded: "expanded"
            },
            // Setting TreeNode Editing option to true                    
            allowEditing: true
        });
    });

{% endhighlight %}



> **Note**: Refer to the previous example for datasource

Execute this code example to render node editing.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img6.png"%}

**Set the Drag and Drop Option** 

You can **Drag and Drop** the folders anywhere inside the mailbox by setting the **allowDragAndDrop** to **true**. 

Execute this code example to **Drag and Drop** the nodes anywhere within the **TreeView**.

{% highlight js %}

    $(function() {
        // declaration
        $("#mailboxTree").ejTreeView({
            fields: {
                id: "id",
                parentId: "pid",
                text: "name",
                hasChild: "hasChild",
                dataSource: outlookicons,
                expanded: "expanded"
            },
            allowEditing: true,
            allowDragAndDrop: true
        });
    });


{% endhighlight %}

> **Note**: Refer to the previous example for datasource

### Configure Events for the TreeView

When you click on the Mailbox folder item, the corresponding navigation action is performed in the **select** event that is achieved by declaring the **select** event with the corresponding call back function.  You can rename the folder names and it is not renamed as empty. This validation process is done manually in the **inlineEditValidation** event.

{% highlight js %}

    $(function() {
        // declaration
        $("#mailboxTree").ejTreeView({
            // mapping JSON Data Source with the fields property of TreeView 
            fields: {
                id: "id",
                parentId: "pid",
                text: "name",
                hasChild: "hasChild",
                dataSource: outlookicons,
                expanded: "expanded"
            },
            // Setting TreeNode Editing option to true
            allowEditing: true,
            // Setting TreeView Drag and Drop option to true
            allowDragAndDrop: true,
            // Setting TreeView with the select event for node selection
            nodeSelect: "setAction",
            // Setting TreeView inline edit validation event for node editing
            inlineEditValidation: "validateFolder"
        });
    });

    function validateFolder(args) {
        //write your code here for other folder creation process.
        if (args.newText === "")

        {
            args.cancel = true;
            alert("Folder name cannot be renamed to empty. Please provide some name.");
        }
    }

    function setAction(args) {
        //write your code here for other process.
        $(".mailHead").html(args.value);
        $(".mailCont").html("The Contents of <b>" + args.value + "</b> will be displayed here");
    }

{% endhighlight %}


> **Note**: Refer to the previous example for datasource 

Execute the code example to render **TreeView**. When you select the mail folder in the **TreeView,** the corresponding action takes place by raising the **select** event. 

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img7.png"%}

> **Note**: The inline edit validation is done on the rising of “inlineEditValidation” event as in the screenshot as follows. The “inlineEditValidation” event rises only when the “allowEdit” property is set to True.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img8.png"%}

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

        var nodeIndex = 1,
            treeviewObj, selectedNode;
        $(function() {
            // declaration
            // Please refer the previous sections for the Splitter and TreeView rendering

            // declaration for Context menu
            $("#treeviewMenu").ejMenu({
                menuType: ej.MenuType.ContextMenu,
                openOnClick: false,
                contextMenuTarget: "#mailboxTree",

                click: "menuclick",
                beforeOpen: "beforeOpen"
            });
            treeviewObj = $("#mailboxTree").data("ejTreeView");
        });

        function validateFolder(args) {
            //write your code here for other folder creation process.
            if (args.newText === "") {
                args.cancel = true;
                alert("Folder name cannot be renamed to empty. Please provide some name.");
            }
        }

        function setAction(args) {
            //write your code here for other process.
            $(".mailHead").html(args.value);
            $(".mailCont").html("The contents of <b>" + args.value + "</b> will be displayed here");
        }
        //creating the treeview object before the context menu opens with the selected node
        function beforeOpen(args) {
            if (!$(args.target).hasClass("e-text"))
                args.cancel = true;
            else {
                selectedNode = args.target;
                //selectNode method for treeview.
                treeviewObj.selectNode(selectedNode);
            }
        }

        function menuclick(args) {
            if (args.events.text == "New Folder") {
                //creating the new node in the treeview using addNode method
                treeviewObj.addNode("New Folder" + nodeIndex, selectedNode);
                nodeIndex++;
            } else if (args.events.text == "Delete Folder") {
                //Deleting the existing node in the treeview
                treeviewObj.removeNode(selectedNode);
            }
        }
        
{% endhighlight %}



> **Note**: Refer to the previous example for datasource. 

The following screenshot displays adding a new folder in the **TreeView** using the **Context Menu**. You can right-click on the **TreeView** Node and select the new folder option in the **Context Menu** for the selected folder. A new folder is added as the child of the **Drafts** folder.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img9.png" Caption="TreeView with context menu"%}

The following screenshot illustrates adding a new folder under the **Drafts** folder. 

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img10.png" Caption="TreeView with new folder"%}

The following screenshot illustrates the deleting of new folder that is created as a child of the Forums folder. You can right-click on the **New Folder1** and select the **Delete Folder** option in the **Context Menu**.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img11.png" Caption="TreeView before deleting a folder"%}

The following screenshot displays the **TreeView** after deleting the folder that is created.

{% include image.html url="/js/TreeView/Getting-Started_images/Getting-Started_img12.png" Caption="TreeView after deleting the New Folder1"%}

