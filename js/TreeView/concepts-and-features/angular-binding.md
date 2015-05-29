---
layout: post
title: angular-binding
description: angular binding
platform: js
control: TreeView
documentation: ug
---

# Angular Binding

**AngularJS** is a **JavaScript** framework. It is added to an **HTML** page with a **&lt;script&gt;** tag. It extends **HTML** attributes with directives, and binds data to **HTML** with expressions. **AngularJS** directives allow you to specify custom and reusable **HTML** tags that moderate the behavior of certain elements.

**Angular****binding** uses directives to plug its action into the page. Directives, all prefaced with ng-, are placed in **HTML** attributes. To know more about **Angular binding** refer the following link,

[http://help.syncfusion.com/ug/js/#!documents/angularjs.htm](http://help.syncfusion.com/ug/js/)

Apply the plugin and property assigning the **TreeView** element through the directive that starts with the letter **“e-“.** The following example depicts how to bind data to the **TreeView** control through **Angular****support**.



{% highlight html %}

<!DOCTYPE html>
<html lang="en" **ng-app**="treeApp">
<head>
    <!--@*To add the following script in html page for angular support-->*@
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script><script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.1/angular.min.js"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js)"> </script>
<script src=" http://cdn.syncfusion.com/js/web/ej.unobtrusive-latest.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/ej.widget.angular-latest.min.js"></script>
</head>
<body **ng-controller**="TreeCtrl">

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



**[View]**

@*To add the following scripts in your view page for angular support*@   

    &lt;script src="@Url.Content("~/Scripts/angular.min.js")"&gt;&lt;/script&gt;

    &lt;script src="@Url.Content("~/Scripts/ej/ej.unobtrusive.min.js")"&gt;&lt;/script&gt;

    &lt;script src="@Url.Content("~/Scripts/ej/ej.widget.angular.min.js")"&gt;&lt;/script&gt;



&lt;div ng-app="treeviewApp"&gt;

     &lt;div ng-controller="treeviewCtrl"&gt;            

         &lt;div id="treeView" ej-treeview e-fields-datasource="dataList" e-fields-id="id" e-fields-parentid="pid" e-fields-text="name" e-fields-haschild="hasChild"/&gt;&lt;/div&gt;                            



    &lt;script&gt;

        var localData = [

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

        angular.module('treeviewApp', ['ejangular']).controller('treeviewCtrl', function ($scope) {

            $scope.dataList = localData;

        });

    &lt;/script&gt;

&lt;/div&gt;

&lt;/div&gt;





**[ASPX]**

\\Add the following scripts in your aspx page for angular support.  

        &lt;script src="Scripts/angular.min.js"&gt;&lt;/script&gt;

        &lt;script src="Scripts/ej.unobtrusive.min.js"&gt;&lt;/script&gt;

        &lt;script src="Scripts/ej.widget.angular.min.js"&gt;&lt;/script&gt;

&lt;div ng-app="treeApp"&gt;

        &lt;div ng-controller="TreeCtrl"&gt;

            &lt;div id="treeView" ej-treeview e-fields-datasource="dataList" e-fields-id="id" e-fields-parentid="pid" e-fields-text="name" e-fields-haschild="hasChild" e-fields-expanded="expanded" /&gt;

        &lt;/div&gt;

    &lt;/div&gt;            

    &lt;script&gt;

        var localData = [

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

        angular.module(' treeApp', ['ejangular']).controller('TreeCtrl', function ($scope) {

            $scope.dataList = localData;

        });

    &lt;/script&gt;

&lt;/div&gt;

&lt;/div&gt;





In the above code example, “ng-app” is a directive that is used to declare an element as a root element of the application, allowing behavior to be modified through custom **HTML** tags and by using the “ng-controller” directive you can get the scope value of **TreeView** control.

The following screenshot displays the output of the above code.

![](angular-binding_images\angular-binding_img1.png)





























![](angular-binding_images\angular-binding_img2.png)



_Figure_ _23__56__: TreeView with Angular Binding_

