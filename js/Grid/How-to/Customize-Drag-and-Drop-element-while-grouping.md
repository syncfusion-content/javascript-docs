---
layout: post
title: Customize-Drag-and-Drop-element-while-grouping
description: customize drag and drop element while grouping
platform: js
control: Grid
documentation: ug
---

### Customize Drag and Drop element while grouping

In this section, you can learn how to customize drag and drop element. This drag and drop element is framed by using **CSS** classes with default values. When you want to change or customize drag and drop element, then just override default values of **CSS** class values. **e-cloneproperties** is the name of drag and drop element in **CSS** class.

{% highlight html %}

**[JS]**

<style type="text/css">
**.e-grid .e-cloneproperties {**
            **background-color: black;**
        **}**
    </style>
</head>
    <body>
        <div id="Grid"></div>
        <script type="text/javascript">
            $(function () {// Document is ready.
                $("#Grid").ejGrid({
                    //window.gridData is refered from jsondata.min.js
                    dataSource: window.gridData,
                    allowGrouping: true,
                    allowPaging: true
                });
            });
        </script>
    </body>
</html>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/How-to/Customize-Drag-and-Drop-element-while-grouping_images/Customize-Drag-and-Drop-element-while-grouping_img1.png" Caption="Drag and Drop Element Customization"%}

