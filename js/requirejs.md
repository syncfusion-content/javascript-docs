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

`(installed location)**\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external`   
_For example, If you have installed the Essential Studio package within `C:\Program Files (x86)`, then navigate to the location,_ **C:\Program Files (x86)**\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external  

## Using RequireJS to create a Syncfusion treeView widget

### CDN link reference

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
                  jquery: 'http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min',

                  easing: 'http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min',

                  scripts: 'http://cdn.syncfusion.com/{{ site.releaseversion }}/js/assets/scripts'
            }
        });



{% endhighlight %}



* Once the **RequireJS** paths are configured, now you can load the needed widgets within the **require** scope by passing the corresponding **Module** path. You can also mention the external dependencies here as specified below,

{% highlight javascript %}


      require(["jquery", "easing", "scripts/web/ej.treeview.min"], function () {

            $("#tree").ejTreeView({  //initializes the TreeView
                fields: {
                    id: "id", parentId: "pid", text: "name",
                    dataSource: [
                       { id: 1, name: "Parent1", expanded: true },
                       { id: 2, pid: 1, name: "Child1" },
                       { id: 3, pid: 1, name: "Child2" },
                       { id: 4, name: "Parent2", expanded: true },
                       { id: 5, pid: 4, name: "Child3" },
                       { id: 6, pid: 4, name: "Child4" },
                       { id: 7, pid: 4, name: "Child5" }
                    ]
                }
            });

      });



{% endhighlight %}



### Local reference of Scripts and Stylesheets

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
            jquery: 'assets/external/jquery-1.10.2.min',
           easing: 'assets/external/jquery.easing.1.3.min'

            }
        });

   require(["jquery", "easing", "assets/scripts/web/ej.treeview.min"], function () {

            $("#tree").ejTreeView({  // initializes the TreeView
                fields: {
                    id: "id", parentId: "pid", text: "name",
                    dataSource: [
                       { id: 1, name: "Parent1", expanded: true },
                       { id: 2, pid: 1, name: "Child1" },
                       { id: 3, pid: 1, name: "Child2" },
                       { id: 4, name: "Parent2", expanded: true },
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



Running the above code will display the output as shown below - where only the scripts required to render the **treeView** control are loaded,

![](requirejs_images\requirejs_img2.png)

