---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Rating
documentation: ug
---

# Appearance and Styling

## Show ToolTip

**Rating** control provides support for **Tooltip** values. This is achieved by enabling the **showTooltip** property to be **‘True’.** When you move the mouse over the **Rating** control it displays the **Tooltip** value as **rating** **value**. By default this property value is set to **‘True’**.

The following code example is used to render the **Rating** control without **tooltip**.

1. Add the following HTML to render Rating with Tooltip.

{% highlight html %}

[HTML]
<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

[JS]
// Add the following script to render Rating without Tooltip.

<script type="text/javascript">
     $("#rating").ejRating({ showTooltip:false });
   </script>


{% endhighlight %}



The following screenshot illustrates **Rating** without **Tooltip**.

{% include image.html url="/js/Rating/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Rating without Tooltip"%}

## Adjusting Rating Size

### Adjust Shape Width and Shape Height

You can customize the width and height of the **Rating** by **shapeWidth** and **shapeHeight** properties. These properties completely depend on rating image’s size. The **shapeWidth** and **shapeHeight** are adjusted within the **rating** image size.

The following code example is used to render the **Rating** control with customized **shapeWidth** and **shapeHeight**.

1. Add the following HTML to render Rating with customized shapeWidth and shapeHeight.

{% highlight html %}

[HTML]
<div style="margin-top: 0px;">
        <h4>Rating:</h4>
        <input id="rating" type="text" class="rating" />
 </div>

[JS]
// Add the following script to render Rating with customized shapeWidth and shapeHeight.

<script type="text/javascript">
      $("#rating").ejRating({ value: 4, shapeWidth: 29, shapeHeight: 29 });   </script>


{% endhighlight %}



2. Add the following styles.

{% highlight css %}

[CSS]
<style type="text/css">
        .e-rating
{
    margin-top: -7px;
}

.e-rating.e-horizontal .e-shape-list, .e-rating.e-vertical .e-shape-list,
.e-rating.e-horizontal .e-shape, .e-rating.e-vertical .e-shape, .e-rating.e-horizontal .e-ul,.e-rating.e-vertical .e-ul,.e-rating.e-horizontal .e-reset, .e-rating.e-vertical .e-reset 
{
height:28px;width:28px;
background:url(images/crystal-stars.png) no-repeat;
}
   .e-rating.e-horizontal .e-reset, .e-rating.e-vertical .e-reset {
background-position: 0 42px;
margin-left: 2px;
}
   .e-rating.e-horizontal .e-shape-list
{
    background-position: 0 -56px;
}

   .e-rating.e-horizontal .e-reset:hover
{
    background-position: 0 42px;
}
    .e-rating .e-shape.inactive {
        background-position: 0 -56px;
    }

    .e-rating .e-shape.active {
        background-position: 0 -112px;
    }

    .e-rating .e-shape.selected {
        background-position: 0 -84px;
    }
.e-tooltip {background-color:white;border:2px solid #b0c4de;color:black}    </style>


{% endhighlight %}



The following screenshot illustrates **Rating** with customized **shapeWidth** and **shapeHeight**.

{% include image.html url="/js/Rating/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Rating with customized shapeWidth and shapeHeight"%}

## Theme

**Rating** control’s style and appearance are controlled based on **CSS** classes. In order to apply styles to the **Rating** control, refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes support available for **Rating** control namely:

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

## Custom styles

The style of the **Rating** control is customized by **cssClass** property. 

The following code example is used to render the **Rating** control with **customized** **style**.

1. Add the following HTML to render Rating with customized style.

{% highlight html %}

**[HTML]**
<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />

                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight html %}

**[JS]**

// Add the following script to render Rating with customized style.

<script type="text/javascript">
        $("#rating").ejRating({ cssClass: "custom" });
    </script>

{% endhighlight %}

2. Add the following styles.

{% highlight css %}

**[CSS]**
<style type="text/css">
        .custom {
            background-color: greenyellow;
        }
    </style>


{% endhighlight %}



The following screenshot illustrates the **Rating** with customized style.

{% include image.html url="/js/Rating/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" Caption="Rating with customized style"%}

