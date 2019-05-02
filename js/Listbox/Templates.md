---
layout: post
title: Templates in Syncfusion ListBox
description: templates
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Templates

The ListBox widget’s appearance can be customized based on different needs using templates. The desired templates can be defined using the [template](https://help.syncfusion.com/api/js/ejlistbox#members:template) property.

{% highlight html %}
   <ul id="listbox"></ul>
    <script type="text/javascript">
        var data = [{
            text: "Erik Linden",
            imageName: "3",
            designation: "Representative",
            country: "England"
        },
            { text: "John Linden", imageName: "6", designation: "Representative", country: "Norway" },
            { text: "Louis", imageName: "7", designation: "Representative", country: "Australia" },
            { text: "Lawrence", imageName: "8", designation: "Representative", country: "India" }];
        $(function () {
            $('#listbox').ejListBox({
                dataSource: data,
                height: "240",
                width: "350",
                //defining templates
                template: '<div><img class="image" src="images/Employees/${imageName}.png" alt="employee"/>' + '<div class="text"> ${text} </div><div class="desig">${designation}</div><div class="country"> ${country} </div></div>'
            });
        });
    </script>

{% endhighlight %}



N> In the above code snippet, the image path (images/Employees) is given just for demonstration. Hence the images will not be displayed while using the above code.

{% seealso %} [Data Binding](https://help.syncfusion.com/js/listbox/databinding). {% endseealso %}

Define the styles for the template as below.

{% highlight css %}

        .image
        {
            margin:0;
            padding: 3px 10px 3px 3px;
            border:0 none;
            width:60px;
            height:60px;
            float:left;
        }
        .text
        {
             font-weight:bold;
             padding:6px 3px 1px 3px;
        }
        .designation,.country{
            font-size:smaller;
            padding:3px 3px 0px 0px;
        }




{% endhighlight %}



![ALt text](Templates_images\Templates_img1.png)

## Render template with conditional statements

By default, [template](https://help.syncfusion.com/api/js/ejlistbox#members:template) property in ListBox control accepts only string values.To render ListBox items using jsrender script template, use the [targetID](https://help.syncfusion.com/api/js/ejlistbox#members:targetid) property and map the corresponding element id to this property.     

Refer to the following code.

{% highlight html %}

    <div class="row">
     <div class="cols-sample-area">
        <div class="ctrllabel">Select a List</div>
        <div id="list"></div>
        <div id="template">
        </div>
     </div>
    </div>

{% endhighlight %}

{% highlight javascript %}
     
    <script id="tableTemplate" type="text/x-jsrender">
      {% raw %} {{if ID < 4}}  {% endraw %}
      <li><span class="e-icon e-user" style=" display: inline-block;"></span><span style=" display: inline-block;"><b>{{:text}}</b></span></li>
      {% raw %} {{else}}
      <li>{{:text}}</li>
     {{/if}} {% endraw %}
    </script>
    <script>
      $(function () {
          var list = [{ text: "Erik", ID: "1" }, { text: "John", ID: "2" }, { text: "Nancy", ID: "3" }, { text: "David", ID: "4" }, { text: "Martin", ID: "5" }, {text: "Louis",  ID: "6" }];
        $("#template").append($("#tableTemplate").render(list)); //append jsrender template to div element.
        $("#list").ejListBox({
            targetID: "template"
        });
      })
    </script>

{% endhighlight %}

Refer to the sample [here](https://jsplayground.syncfusion.com/4nfszgmf)

