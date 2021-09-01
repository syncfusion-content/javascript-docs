---
layout: post
title: Bootstrap Theme for Essential JavaScript components | Syncfusion
description: Learn here all about bootstrap theme support in Syncfusion Essential JavaScript platform, its elements, and more.
platform: js
control: General Topics
documentation: ug
---

# Bootstrap Theme for Essential JavaScript components

**Essential JavaScript** supports all its web components to be used more easily under the bootstrap environment. Usually the bootstrap applies its own CSS styles to the HTML elements globally – so that when the third party vendor components used under that environment will get affected with its appearance – due to the overriding of its CSS styles. With this bootstrap theme support available for all the components, it is very easy to create a more responsive application with no fear of overriding.

A container element is mandatory for the bootstrap to wrap the contents. We can use either fixed-width or fluid-width layout to include the contents of the web page along with EJ components. Use the class named **container** and specify a width to it, for creating fixed width layout. Use the class named **container-fluid** to occupy the entire width of the viewport. EJ components can be nested in any of these layouts and with almost all the bootstrap classes.

The bootstrap theme file is available within the **css** folder which is depicted here. 

## Example: To use the RTE control in bootstrap form layout, 

Create a usual HTML file along with the necessary scripts and stylesheets referred in the page. Bootstrap files can be downloaded from [here](http://getbootstrap.com/getting-started/), if you need to refer it locally. We have used the CDN links for the Scripts and CSS file references in the page within the &lt;head&gt; section as shown below, 

{% highlight html %}


<head>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>


{% endhighlight %}



Here, the **bootstrap.css** file needs to be referred mandatorily in this sample application, as it will be using some of the bootstrap classes such as **container**, **form-group** and so on.

Another important thing to do is to apply our **bootstrap** **theme** for the Syncfusion widgets, so that its CSS styles will not be overridden by the bootstrap layout.

Now, define the containers for two of our Syncfusion widgets namely **RTE** and **button** within the bootstrap layout as shown below,

{% highlight html %}


<div class="container">
        <div class="col-lg-12" id="Comments">
            <div class="form-horizontal" style="padding-top: 25px;">
                <div class="form-group">
                    <label for="name" class="col-sm-2 control-label">Enter Name</label>
                    <div class="col-sm-10">
                        <input type="text" class="form-control" id="name"
                            placeholder="Enter Name">
                    </div>
                </div>
                <div class="form-group">
                    <label for="emailID" class="col-sm-2 control-label">Enter e-Mail ID</label>
                    <div class="col-sm-10">
                        <input type="text" class="form-control" id="emailID"
                            placeholder="Enter e-MailID">
                    </div>
                </div>
                <div class="form-group">
                    <label for="comments" class="col-sm-2 control-label">Enter comments</label>
                    <div class="col-sm-10">
                          <textarea type="text" class="form-control" id="message"></textarea>
                    </div>
                </div>
                <div class="form-group">
                    <div class="col-sm-offset-2 col-sm-10">
                          <button id="Btn" class="btn btn-default">Submit</button>
                    </div>
                </div>
            </div>
        </div>
</div>



{% endhighlight %}



Initialize the RTE and button controls within the &lt;script&gt; section as shown below,

{% highlight javascript %}


        $(function () {

            $("#message").ejRTE({ width: "98%" });

            $("#Btn").ejButton({ width: "100px", height: "40px" });

        });



{% endhighlight %}



Running the above code will display the output similar to the below screenshot,

![bootstraptheme_images1](bootstraptheme_images\bootstraptheme_img1.png)


N> Apart from the default bootstrap theme, All the Essential JavaScript components are provided with built-in **responsive support**, so that it will adjust automatically based on the browser viewport.  
N> Setting width of any of the Syncfusion components to 100% is simply enough to make it responsive. Including **ej.responsive.css** file will make some components like menu, dialog, schedule to change their appearances accordingly in mobile devices.   
N> To render the grid control appropriately in mobile devices, **ejgrid.responsive.css** file needs to be referred separately along with the other CSS and script file references.




