---
layout: post
title: Customize-Header
description: customize header
platform: js
control: ListView
documentation: ug
api: /api/js/ejlistview
---

# Customize Header

In **ListView**, you can enable the built-in **Header** support. To show or hide the **Header** in **ListView**, use the [showHeader](https://help.syncfusion.com/api/js/ejlistview#members:showheader) property. By default, **ListView** is rendered with the **Header**. You can set the title for the **Header** by using the [headerTitle](https://help.syncfusion.com/api/js/ejlistview#members:headertitle) property.

In some cases, for the purpose of navigation, you may want to show the **Back** button in **ListView Header**. To achieve this, [showheaderbackbutton](https://help.syncfusion.com/api/js/ejlistview#members:showheaderbackbutton) property is used. By default, **ListView** is not rendered with the header back button in parent page. To customize the text shown in **ListView Header Back** button, the property [headerbackbuttontext](https://help.syncfusion.com/api/js/ejlistview#members:headerbackbuttontext) is used. 

Refer the following code example.



{% highlight html %}


        <div id="defaultListView">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}
 
        $(function () {
            $("#defaultListView").ejListView({showHeader:true, **showHeaderBackButton:true, headerBackButtonText :"Menu"**, width:400});
        });

{% endhighlight %}



Run the code to get the following output

![](/js/ListView/Customize-Header_images/Customize-Header_img1.png) 

