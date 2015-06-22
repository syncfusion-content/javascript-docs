---
layout: post
title: Templates
description: templates
platform: js
control: AutoComplete
documentation: ug
---

# Templates

You can provide a **Template** for customizing the appearance of the AutoComplete textbox suggestions. This is achieved by assigning a string template to the template property.

## Configuring Templates

The following steps explain you how to define a **Template** to display a text and image for an AutoComplete textbox.

1. In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

         <input type="text" id="selectCountry" />


{% endhighlight %}


 Define the **CSS** classes for the sprite images. You can find the images in the following location:

[Installed Drive]:\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\X.X.X.X\JS \Samples\ web \images\autocomplete\flags.png

{% highlight css %}

<style type="text/css" class="cssStyles">
        /* Sprite css for country flags */
        .flag
        {
            background: url("../images/autocomplete/flags.png") no-repeat;
            float: left;
            height: 15px;
            margin-right: 10px;
            margin-top: 3px;
            width: 25px;
        }

        .flag.flag-am {background-position: -25px 0}
        .flag.flag-ar {background-position: -50px 0}
        .flag.flag-bd {background-position: -75px 0}
        .flag.flag-br {background-position: -100px 0}
        .flag.flag-ca {background-position: -125px 0}
        .flag.flag-cn {background-position: 0 -15px}
        .flag.flag-cu {background-position: -25px -15px}
        .flag.flag-dk {background-position: -50px -15px}
        .flag.flag-dz {background-position: -75px -15px}
        .flag.flag-ee {background-position: -100px -15px}
        .flag.flag-eg {background-position: -125px -15px}
        .flag.flag-es {background-position: 0 -30px}
        .flag.flag-fi {background-position: -25px -30px}
        .flag.flag-fr {background-position: -50px -30px}
        .flag.flag-gl {background-position: -75px -30px}
        .flag.flag-id {background-position: -100px -30px}
        .flag.flag-in {background-position: -125px -30px}
        .flag.flag-mx {background-position: 0 -45px}
        .flag.flag-my {background-position: -25px -45px}
        .flag.flag-nl {background-position: -50px -45px}
        .flag.flag-no {background-position: -75px -45px}
        .flag.flag-nz {background-position: -100px -45px}
        .flag.flag-pl {background-position: -125px -45px}
        .flag.flag-pt {background-position: 0 -60px}
        .flag.flag-qa {background-position: -25px -60px}
        .flag.flag-ro {background-position: -50px -60px}
        .flag.flag-sa {background-position: -75px -60px}
        .flag.flag-sg {background-position: -100px -60px}
        .flag.flag-th {background-position: -125px -60px}
        .flag.flag-tr {background-position: 0 -75px}
        .flag.flag-ua {background-position: -25px -75px}
        .flag.flag-us {background-position: -50px -75px}
        .flag.flag-uy {background-position: -75px -75px}
        .flag.flag-vn {background-position: -100px -75px}
        .flag.flag-ye {background-position: -125px -75px}
        .txt {
            display: table-cell;
            height: 20px;
            vertical-align: middle;
        }  

   </style>



{% endhighlight %}



 Define **dataSource** elements with required **template** fields using the **Sprite CSS** class names,

{% highlight js %}


      var countries = [
             { text: "Algeria", sprite: "flag-dz" }, { text: "Argentina", sprite: "flag-ar" },
             { text: "Armenia", sprite: "flag-am" }, { text: "Brazil", sprite: "flag-br" },
             { text: "Bangladesh", sprite: "flag-bd" }, { text: "Canada", sprite: "flag-ca" },
             { text: "Cuba", sprite: "flag-cu" }, { text: "China", sprite: "flag-cn" },
             { text: "Denmark", sprite: "flag-dk" }, { text: "Estonia", sprite: "flag-ee" },
             { text: "Egypt", sprite: "flag-eg" }, { text: "France", sprite: "flag-fr" },
             { text: "Finland", sprite: "flag-fi" }, { text: "Greenland", sprite: "flag-gl" },
             { text: "India", sprite: "flag-in" }, { text: "Indonesia", sprite: "flag-id" },
             { text: "Malaysia", sprite: "flag-my" },{ text: "Mexico", sprite: "flag-mx" },
             { text: "New Zealand",sprite: "flag-nz" },{text:"Netherlands",sprite:"flag-nl" },
             { text: "Norway", sprite: "flag-no" }, { text: "Portugal", sprite: "flag-pt" },
             { text: "Poland", sprite: "flag-pl" },{ text: "Qatar", sprite: "flag-qa" },
             { text: "Romania", sprite: "flag-ro" }, { text: "Spain", sprite: "flag-es" },
             { text:"Singapore", sprite: "flag-sg" },{text:"Saudi Arabia",sprite: "flag-sa" },
             { text: "Thailand", sprite: "flag-th" },{ text: "Turkey", sprite: "flag-tr" },
             { text: "Ukraine", sprite:"flag-ua" }, {text:"United States",sprite: "flag-us" },
             { text: "Uruguay", sprite: "flag-uy" }, { text: "Viet Nam", sprite: "flag-vn" },
             { text: "Yemen", sprite: "flag-ye" }	
          ];


{% endhighlight %}


 Configure the **template** structure for **AutoComplete** control by including a **&lt;div&gt;** element with an image and text in every row of the popup panel. Assign the corresponding variable name within **${**&lt;field name&gt;**}** to map them into the list.


{% highlight js %}


        $('#selectCountry').ejAutocomplete({
                dataSource: countries,
                width: 205,
                template: '&lt;div class="flag ${sprite}"&gt; &lt;/div&gt;' +
                        '&lt;div class="txt"&gt; ${text} &lt;/div&gt;'
            });


{% endhighlight %}


The following image is the output for **AutoComplete** widget with **Template** support.

{% include image.html url="/js/Autocomplete/Templates_images/Templates_img1.png" Caption="AutoComplete with Custom template"%}

