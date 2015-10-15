---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: TreeView
documentation: ug
---

# Angular Binding

**AngularJS** is a **JavaScript** framework. It is added to an **HTML** page with a **&lt;script&gt;** tag. It extends **HTML** attributes with directives, and binds data to **HTML** with expressions. **AngularJS** directives allow you to specify custom and reusable **HTML** tags that moderate the behavior of certain elements.

**Angular binding** uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in **HTML** attributes. To know more about **Angular binding** refer the following link,

<http://docs.syncfusion.com/js/angularjs>

Apply the plugin and property assigning the **TreeView** element through the directive that starts with the letter **“e-“.** The following example depicts how to bind data to the **TreeView** control through **Angular support**.

{% highlight html %}

<!DOCTYPE html>
<html lang="en" ng-app="treeApp">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"> </script>
</head>
<body ng-controller="TreeCtrl">

    <div id="treeView" ej-treeview e-fields-datasource="dataList" e-fields-id="id" e-fields-parentid="pid" e-fields-text="name" e-fields-haschild="hasChild" e-fields-expanded="expanded" />
    <script>
        var icons = [
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
        angular.module('treeApp', ['ejangular']).controller('TreeCtrl', function ($scope) {
            $scope.dataList = icons;
        });
    </script>
</body>
</html>



{% endhighlight %}



In the above code example, “ng-app” is a directive that is used to declare an element as a root element of the application, allowing behavior to be modified through custom **HTML** tags and by using the “ng-controller” directive you can get the scope value of **TreeView** control.

The following screenshot displays the output of the above code.

{% include image.html url="/js/TreeView/Angular-Binding_images/Angular-Binding_img1.png"%}

