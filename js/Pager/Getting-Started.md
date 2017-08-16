---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Pager
documentation: ug
api : /api/js/ejpager
---

# Getting Started

This section briefly explains about how to create a **Pager** control in your application with Javascript. The following sample explains how to render a **Pager** control in your application.



## Creating your first Pager in Javascript

The **Essential Javascript Pager** control render’s based on total records count, page size, page count values.

Create an HTML file and add the following code template to the HTML file.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!--- Add pager element Here  --->
   </body>
</html>


{% endhighlight %}


Add &lt;Div&gt; element to create a Pager control.

{% highlight html %}

<div id="pager"> </div>

{% endhighlight %}


Initialize **Pager** control in the **script** section with properties.

N> The totalRecordsCount, pageSize and pageCount API values play a key role in rendering a pager control. Since pageSize and pageCount API’s are dependent on each other and pager will be updated each time the value changes as explained below.

**Total records Count:** totalRecordsCount defines the total number of records which is bounded as a single data.

{% highlight javascript %}

        $(function () {

            $("#pager").ejPager({

                totalRecordsCount: 20,

            });

        });


{% endhighlight %}

Run the above sample to get the below output.

![](/js/Pager/Getting-Started_images/Getting-Started_img1.png)


 **Page Size:**  pageSize value defines the number records to be displayed per page. The default value for the pageSize API is 12. 
 
 N> The page count value changes with change in the pageSize value.

  {% highlight javascript %}

        $(function () {

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

            });

        });


{% endhighlight %}

Run the above sample to get the below output.

![](/js/Pager/Getting-Started_images/Getting-Started_img2.png)

**Page Count:**  pageCount value defines the number of pages to be displayed in the pager control for navigation. The default value for pageCount is 10 and value will be updated based on totalaRecordsCount and pageSize values.

{% highlight javascript %}

        $(function () {

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount: 3,


            });

        });


{% endhighlight %}

Run the above sample to get the below output.

![](/js/Pager/Getting-Started_images/Getting-Started_img3.png)

