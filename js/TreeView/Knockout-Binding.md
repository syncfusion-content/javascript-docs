---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: TreeView
documentation: ug
---

# Knockout Binding

**KnockoutJS** is a **JavaScript** library that allows you to bind **HTML** elements against any data model.

It uses a **Model-View-ViewModel** (MVVM) design pattern, where the **Model** is your stored data, **View** is the visual representation of that data (**UI**) and **ViewModel** acts as the intermediary between the **Model** and the **View**. For more information about the **Knockout** **binding**, refer the online documentation in the following link,

<http://help.syncfusion.com/js/knockoutjs>

When using **KO**, the view page is simply an **HTML** document with declarative bindings and you can link it to the **ViewModel**. **ViewModel** is nothing but an object, holding a list of items for creating the **TreeView** control using **Knockout binding**.

In **Knockout binding** by using **ko.observableArray**, you can hold the data of **TreeView** and bind it to an array of values by using **ko.applyBindings**. When you call **ko.applyBindings** with a specific element, it binds everything under that element.

The following example depicts the way to bind data to the **TreeView** control through **Knockout Support**.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Knockout support in Treeview Essential JS</title>
    <!--To add the following script in html page for knockout support-->
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body data-autoinit="false">
    <div style="width: 250px">
        <div id="treeview" data-bind="ejTreeView: { fields: { dataSource: dataSource, id: 'id', text: 'name', hasChild: 'hasChild', expanded: 'expanded', parentId: 'pid' } } "></div>
    </div>
    <script type="text/javascript">
        $(function () {
            var tview = [
                   { id: 1, name: "Favorites", hasChild: true },
                   { id: 2, pid: 1, name: "Desktop" },
                   { id: 3, pid: 1, name: "Downloads" },
                   { id: 4, pid: 1, name: "Recent places" },
                   { id: 5, name: "libraries", hasChild: true },
                   { id: 6, pid: 5, name: "Documents", hasChild: true },
                   { id: 7, pid: 6, name: "My Documents" },
                   { id: 8, pid: 6, name: "Public Documents" },
                   { id: 9, pid: 5, name: "Pictures", hasChild: true },
                   { id: 10, pid: 9, name: "My Pictures" },
                   { id: 11, pid: 9, name: "Public Pictures" },
                   { id: 12, pid: 5, name: "Music", hasChild: true },
                   { id: 13, pid: 9, name: "My Music" },
                   { id: 14, pid: 9, name: "Public Music" },
                   { id: 15, pid: 5, name: "Subversion" },
                   { id: 16, name: "Computer", hasChild: true },
                   { id: 17, pid: 16, name: "Folder(C)" },
                   { id: 18, pid: 16, name: "Folder(D)" },
                   { id: 19, pid: 16, name: "Folder(F)" },

            ];
            window.employeeView = {
                dataSource: ko.observableArray(tview),
            };
            ko.applyBindings(employeeView);
        });

    </script>
</body>
</html>


{% endhighlight %}



The following screenshot displays the output of the above code.

![](/js/TreeView/Knockout-Binding_images/Knockout-Binding_img1.png)

