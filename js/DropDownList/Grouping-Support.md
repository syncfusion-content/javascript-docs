---
layout: post
title: Grouping-Support
description: grouping support
platform: js
control: DropDownList
documentation: ug
---

# Grouping Support

**Grouping Support using DataSource**

**Grouping** DropDownList items can be done by using **category** field. Set the category field and define it in the **DataSource**. Then map the fields for the data items of the **DropDownList** and set **allowGrouping** property value to **true**.

The following steps explain you how to group data items in the **DropDownList** control by using **DataSource**.

In an HTML page, add a &lt;input&gt; element to configure **DropDownList** widget.

{% highlight html %}

     <input type="text" id="categoryGrouping" />     

{% endhighlight %}

Configure the **DataSource** and initialize the **DropDownList** widget in the Script section as follows.

{% highlight js %}

         $(function () {
            var countries = [
               { country: "Austria", group: "A" },
               { country: "Australia", group: "A" }, { country: "Antarctica", group: "A" },
               { country: "Bangladesh", group: "B" }, { country: "Belgium", group: "B" },
               { country: "Brazil", group: "B" },
               { country: "Canada", group: "C" }, { country: "China", group: "C" },
               { country: "Cuba", group: "C" },
               { country: "Denmark", group: "D" }, { country: "Dominica", group: "D" },
               { country: "Europe", group: "E" }, { country: "Egypt", group: "E" },
               { country: "England", group: "E" },
               { country: "India", group: "I" }, { country: "Indonesia", group: "I" },
               { country: "Ireland", group: "I" }, { country: "Italy", group: "I" },
               { country: "France", group: "F" }, { country: "Finland", group: "F" },
               { country: "Germany", group: "G" }, { country: "Greece", group: "G" },
               { country: "Greenland", group: "G" }, { country: "Georgia", group: "G" },
               { country: "Haiti", group: "H" }, { country: "Hong Kong", group: "H" }
            ];
            $('#categoryGrouping').ejDropDownList({
                dataSource: countries,
                fields: { text: "country", category: "group" },
                allowGrouping: true,
                width: "150px"
            });
});

{% endhighlight %}



3. The above code example illustrates the following output.

{% include image.html url="/js/DropDownList/Grouping-Support_images/Grouping-Support_img1.png" Caption="Figure 29: Grouping support by using DateaSource"%}

**Grouping Support using UL and LI structure**

Another way to group **DropDownList** is by using **UL** and **LI structure**. Here, you have to specify the group category in the **&lt;span&gt;** tag. The ID of the **&lt;div&gt;** tag should be given as the **targetId** for the **DropDownList** control. The following code example illustrates how to achieve Grouping in DropDownList control by using **UL and LI structure**.

1. Add the input element and the UL and LI structures to group the **DropDownList** control.

{% highlight html %}

    <input type="text" id="vegetable" />
    <div id="vegetablelist">
        <ul>
            <span>Leafy and Salad</span>
            <li>Cabbage</li>
            <li>Pea</li>
            <li>Spinach</li>
            <li>Wheatgrass</li>
            <li>Yarrow </li>
            <span>Beans</span>
            <li>Chickpea</li>
            <li>Green bean</li> 
             <span>Bulb and Stem</span>
            <li>Garlic</li>
            <li>Garlic Chives</li>
             <span>Root and Tuberous</span>
            <li>Beetroot</li>
            <li>Carrot</li>
        </ul>
    </div>
         
{% endhighlight %}

{% highlight js %}

    // You can initialize the DropDownList control in the script section and add the Target ID to the DropDownList as follows.
    $('#vegetable').ejDropDownList({
         targetID: "vegetablelist",
         width:"150px"
     });

{% endhighlight %}

{% include image.html url="/js/DropDownList/Grouping-Support_images/Grouping-Support_img2.png" Caption="Figure 30: Grouping in Dropdownlist by using UL and LI structure "%}

