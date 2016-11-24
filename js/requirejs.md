---
layout: post
title: RequireJS support for all of Essential JavaScript components
description: requirejs
platform: js
control: General Topics
documentation: ug
---

# RequireJS

**Essential JavaScript** includes [RequireJS](http://www.requirejs.org/) support for all of its components, which implements the **AMD** (Asynchronous Module Definition) specification. Its main goal is to load the user-specified multiple custom scripts/modules in a particular order – as one relies on the other. Also, it improves the speed and quality of the code.

In General, a single widget file **ej.web.all.min.js** file is used to load any of the Syncfusion widgets – but with the introduction of new **AMD** **modules**, it is not necessary to refer the entire script files in the project – just adding the script reference for **RequireJS** is enough – as it loads only the required widgets scripts at the required time. 

The local module structure is as follows – where all the widget modules are placed under the **assets** folder. For detailed information on **assets** folder structure, refer here.

![](requirejs_images\requirejs_img1.png)

You can find the **require.min.js** from the following installed location of your machine,

`(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external`   
_For example, If you have installed the Essential Studio package within `C:\Program Files (x86)`, then navigate to the location,_ **C:\Program Files (x86)**\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external  

N> For version lower than 13.3.0.18, refer this [Knowledge Base](http://www.syncfusion.com/support/kb/7146).

N> From version 14.3.0.49, we have removed the **jquery.easing** dependency from our components. For version lower than 14.3.0.49, you need to refer the jquery.easing as additional dependency. 


## Using RequireJS to create a Syncfusion TreeView widget

### Load the Syncfusion files from CDN link  

* Create a HTML file and add the CSS file and **require.min.js** file reference within the head section as shown below,

{% highlight html %}


<head>

    <title>TreeView with RequireJS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--script for RequireJS-->
    <script src="http://cdn.syncfusion.com/js/assets/external/require.min.js"></script>

</head>



{% endhighlight %}



* While using the **RequireJS**, some custom scripts are needed for running the application. In this case, you need to configure the **RequireJS** with the other dependencies within the script section as follows,

{% highlight javascript %}


        require.config({

            paths: {

                "jquery": 'http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min',

                "jsrender": 'http://cdn.syncfusion.com/js/assets/external/jsrender.min',

                "ejscripts": 'http://cdn.syncfusion.com/{{ site.releaseversion }}/js'
            }

        });



{% endhighlight %}



* Once the **RequireJS** paths are configured, now you can load the needed widgets within the **require** scope by passing the corresponding **Module** path. You can also mention the external dependencies here as specified below,

{% highlight javascript %}


      require(["ejscripts/web/ej.treeview.min"], function () {

            $("#tree").ejTreeView({  //initializes the TreeView
                fields: {
                    id: "id", parentId: "pid", text: "name",
                    dataSource: [
                       { id: 1, name: "Parent1", expanded: true ,hasChild: true},
                       { id: 2, pid: 1, name: "Child1" },
                       { id: 3, pid: 1, name: "Child2" },
                       { id: 4, name: "Parent2", expanded: true ,hasChild: true},
                       { id: 5, pid: 4, name: "Child3" },
                       { id: 6, pid: 4, name: "Child4" },
                       { id: 7, pid: 4, name: "Child5" }
                    ]
                }
            });

      });



{% endhighlight %}



### Load the Syncfusion files from a local directory

The above specified CDN links can also be replaced with the local scripts and Stylesheets. To do so, simply copy the assets folder from the installed location on your machine into the sample application directory and then refer it in your sample code as shown below. For referring the stylesheets locally, refer here.

{% highlight html %}


 <!DOCTYPE html>
<html>
<head>
    <title>TreeView with RequireJS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

    <!-- style sheet for default theme(flat azure) follow the steps from here -->
    <link href="**Content/ej/web/default-theme/ej.web.all.min.css**" rel="stylesheet" />

    <!--script for RequireJS-->
    <script src="**assets/external/require.min.js**"></script>
</head>

<body>

    <div id="tree"></div>

    <script>
        require.config({
            paths: {

                "jquery": 'assets/external/jquery-3.0.0.min',

                "jsrender": 'assets/external/jsrender.min',
              
            }
        });

        require(["assets/scripts/web/ej.treeview.min"], function () {

            $("#tree").ejTreeView({  // initializes the TreeView
                fields: {
                    id: "id", parentId: "pid", text: "name",
                    dataSource: [
                       { id: 1, name: "Parent1", expanded: true,hasChild: true },
                       { id: 2, pid: 1, name: "Child1" },
                       { id: 3, pid: 1, name: "Child2" },
                       { id: 4, name: "Parent2", expanded: true,hasChild: true },
                       { id: 5, pid: 4, name: "Child3" },
                       { id: 6, pid: 4, name: "Child4" },
                       { id: 7, pid: 4, name: "Child5" }
                    ]
                }
            });

        });
    </script>
</body>
</html>



{% endhighlight %}



Running the above code will display the output as shown below - where only the scripts required to render the **TreeView** control are loaded,

![](requirejs_images\requirejs_img2.png)

## Using RequireJS to create a Syncfusion TreeView widget with AngularJS

Essential JavaScript provides a complete support of AngularJS for all the Syncfusion widgets, which can be achieved by integrating and referring the Syncfusion JS library ej.widget.angular.min.js file in the application. The below example demonstrates how to initialize TreeView Widget with AngularJS using RequireJS.

{% highlight html %}

<!doctype html>
<html lang="en">
<head>
    <title>TreeView - Angular with RequireJS</title>
    <link rel="stylesheet" id="linkTag" href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/require.min.js"></script>
</head>
<body ng-controller="TreeViewCtrl">

    <div id="treeView" ej-treeview e-fields-datasource="dataList" e-fields-id="id" e-fields-parentid="pid" e-fields-text="name" e-fields-haschild="hasChild" e-fields-expanded="expanded" />

    <script>

        requirejs.config({

            paths: {

                "jquery": 'http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min',

                "jsrender": 'http://cdn.syncfusion.com/js/assets/external/jsrender.min',
                
                "angular": 'http://cdn.syncfusion.com/js/assets/external/angular.min',

                "ejscripts": 'http://cdn.syncfusion.com/{{ site.releaseversion }}/js'

            }

        });

        var localData = [
            { id: 1, name: "Parent1", expanded: true, hasChild: true },
            { id: 2, pid: 1, name: "Child1" },
            { id: 3, pid: 1, name: "Child2" },
            { id: 4, name: "Parent2", expanded: true, hasChild: true },
            { id: 5, pid: 4, name: "Child3" },
            { id: 6, pid: 4, name: "Child4" },
            { id: 7, pid: 4, name: "Child5" }
        ];

        require(["ejscripts/common/ej.widget.angular.min", "ejscripts/web/ej.treeview.min"], function () {

            angular.module('syncApp', ['ejangular'])
                .controller('TreeViewCtrl', function ($scope) {
                    $scope.dataList = localData;
                });

            angular.bootstrap(document, ['syncApp']);

        });

    </script>
</body>
</html>



{% endhighlight %}

## Using RequireJS to create a Syncfusion TreeView widget with KnockoutJS

Essential JavaScript provides a complete support of KnockoutJS (MVVM pattern) for all the Syncfusion widgets, which can be achieved by integrating and referring the Syncfusion JS library ej.widget.ko.min.js file in the application. The below example demonstrates how to load KnockoutJS and initialize TreeView Widget with RequireJS.

{% highlight html %}

<!doctype html>
<html>
<head>
    <title>TreeView - Knockout with RequireJS</title>
    <link rel="stylesheet" href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/require.min.js"></script>
</head>
<body>

    <div class="control">
        <div id="treeview" data-bind="ejTreeView: {fields :{ dataSource: dataSource,id:'id',text:'name',hasChild:'hasChild',expanded:'expanded',parentId:'pid'}} "></div>
    </div>

    <script>

        requirejs.config({

            paths: {

                "jquery": 'http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min',

                "jsrender": 'http://cdn.syncfusion.com/js/assets/external/jsrender.min',
                
                "knockout": 'http://cdn.syncfusion.com/js/assets/external/knockout.min',

                "ejscripts": 'http://cdn.syncfusion.com/{{ site.releaseversion }}/js'

            }

        });

        require(["ejscripts/common/ej.widget.ko.min", "ejscripts/web/ej.treeview.min"], function (ko) {

            var localData = [
            { id: 1, name: "Parent1", expanded: true, hasChild: true },
            { id: 2, pid: 1, name: "Child1" },
            { id: 3, pid: 1, name: "Child2" },
            { id: 4, name: "Parent2", expanded: true, hasChild: true },
            { id: 5, pid: 4, name: "Child3" },
            { id: 6, pid: 4, name: "Child4" },
            { id: 7, pid: 4, name: "Child5" }
            ];

            window.viewModel = {
                dataSource: localData
            };

            ko.applyBindings(viewModel);

        });

    </script>
</body>
</html>

{% endhighlight %}

