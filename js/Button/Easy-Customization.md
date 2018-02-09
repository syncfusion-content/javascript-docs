---
layout: post
title: Easy-Customization
description: easy customization
platform: js
control: Button
documentation: ug
api : /api/js/ejbutton
---

# Easy Customization

Button is used in all applications. Button size, content and content location is varied according to each application. Here you can see some customizable option for button that can perform easily. 

## Button Size	

You can render the button in different sizes. Here, you have some predefined size options for rendering a button with different sizes in easiest way. Each size option has different height and width. Mainly it avoids the complexity in rendering button with complex **CSS** class. 

List of predefined button size

<table>
    <tr>
        <th>
            Button Types</th>
        <th>
            Description</th>
    </tr>
    <tr>
        <td>
           Normal
        </td>
        <td>
            Creates button with content size.
        </td>
    </tr>
    <tr>
        <td>
            Mini
        </td>
        <td>
            Creates button with Built-in mini size height, width specified.
        </td>
    </tr>
    <tr>
        <td>
            Small
        </td>
        <td>
            Creates button with Built-in small size height, width specified.
        </td>
    </tr>
    <tr>
        <td>
            Medium
        </td>
        <td>
            Creates button with Built-in medium size height, width specified.
        </td>
    </tr>
    <tr>
        <td>
            Large
        </td>
        <td>
            Creates button with Built-in large size height, width specified.
        </td>
    </tr>
</table>


Apart from the above mentioned predefined size option, you can set your own width and height for button using **height** and **width** property.

The following steps explains you the details about rendering the button with different size options.

In the **HTML** page, add the following button elements to configure button widget.

{% highlight html %}

<button id="button_normal">login</button>
<button id="button_mini">login</button>
<button id="button_small">login</button>
<button id="button_medium">login</button>
<button id="button_large">login</button>
<button id="button_custom">login</button>
    
{% endhighlight %}

{% highlight javascript %}

    //Here size property is used to render the button in different sizes
    $(function () {
        $("#button_normal").ejButton({
            //normal size type is used
            size: "normal",
            showRoundedCorner: true,
            contentType: "imageonly",
            prefixIcon: "e-icon e-handup"
        });
        $("#button_mini").ejButton({
            showRoundedCorner: true,
            //mini size type is used
            size: "mini"
        });
        $("#button_small").ejButton({
            showRoundedCorner: true,
            //small size type is used
            size: "small"
        });
        $("#button_medium").ejButton({
            showRoundedCorner: true,
            //medium size type is used
            size: "medium"
        });
        $("#button_large").ejButton({
            //large size type is used
            size: "large",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
        $("#button_custom").ejButton({
            //button with user given height and width
            height: 50,
            width: 130,
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
    });

{% endhighlight %}

Execute the above code to render the following output.

![](/js/Button/Easy-Customization_images/Easy-Customization_img1.png)


## Content Type

The content of the **Button** is mainly text and images. Instead of using complex **CSS** classes to render **Button** with different content types, you can use some predefined content type options provided for button control. Using this content types you can easily add different types of content for button. **Button** supports the following content types.

List of content types for button

<table>
    <tr>
        <th>
            Content Types</th>
        <th>
            Description</th>
    </tr>
    <tr>
        <td>
            TextOnly
        </td>
        <td>
            Supports only for text content only.
        </td>
    </tr>
    <tr>
        <td>
            ImageOnly
        </td>
        <td>
            Supports only for image content only
        </td>
    </tr>
    <tr>
        <td>
            ImageBoth
        </td>
        <td>
            Supports image for both ends of the button.
        </td>
    </tr>
    <tr>
        <td>
            TextAndImage
        </td>
        <td>
            Supports image with the text content.
        </td>
    </tr>
    <tr>
        <td>
            ImageTextImage
        </td>
        <td>
            Supports image with both ends and middle in text.
        </td>
    </tr>
</table>

## Prefix and Suffix icons

Icons inside the **Button** is added easily using **prefixIcon and suffixIcon** property. Location of the icon in button is a necessary thing and you can easily customize it using the following mentioned options.

**Button** control also supports the Built-in icon libraries. The **ej.widgets.core.min.css** contains definitions for important icons that can be used in buttons. Simply you can use these Built-in icons by mentioning the icon class name as value in **prefixIcon** and **suffixIcon** property. You can use any font icons that are defined in **ej.widgets.core.min.css**. It avoids the complexity in specifying icon using sprite image and **CSS**.

For example the following mentioned Built-in **CSS** class are used to show the font icons that is used by media player.

* e-mediaback
* e-mediaforward
* e-medianext
* e-mediaprev
* e-mediaeject
* e-mediaclose
* e-mediapause
* e-mediaplay

### Prefix Icon

It inserts the icon at the starting position of button. After this prefix icon, you can use text or suffix icon.

### Suffix Icon

It inserts the icon at the ending position of button. Before this suffix icon, you can use text or prefix icon.

The following steps explains you the details about rendering the **Button** with above mentioned **content type**, **prefix** and **suffix icon** options

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

  
<button id="button_imageonly">login</button>
<button id="button_textonly">login</button>
<button id="button_imageboth">login</button>
<button id="button_textandimage">login</button>
<button id="button_imagetextimage">login</button>
<br />
<br />
<button id="button_imageonly_small">login</button>
<button id="button_textonly_small">login</button>
<button id="button_imageboth_small">login</button>
<button id="button_textandimage_small">login</button>
<button id="button_imagetextimage_small">login</button>


{% endhighlight %}

{% highlight javascript %}


    // Here use contentType property to render the button with different contents
    $(function () {
        $("#button_imageonly").ejButton({
            //only image is used as content
            contentType: "imageonly",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup"
        });
        $("#button_textonly").ejButton({
            //only text is used as content
            contentType: "textonly",
            showRoundedCorner: true,
        });
        $("#button_imageboth").ejButton({
            //only images in both end is used as content
            contentType: "imageboth",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
            suffixIcon: "e-icon e-palette"
        });
        $("#button_textandimage").ejButton({
            //text and image is used as content
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup"
        });
        $("#button_imagetextimage").ejButton({
            //images in both end and text in center is used as content
            contentType: "imagetextimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
            suffixIcon: "e-icon e-palette"
        });

        $("#button_imageonly_small").ejButton({
            size: "small",
            //only image is used as content
            contentType: "imageonly",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup"
        });
        $("#button_textonly_small").ejButton({
            size: "small",
            //only text is used as content
            contentType: "textonly",
            showRoundedCorner: true,
        });
        $("#button_imageboth_small").ejButton({
            size: "small",
            //only images in both end is used as content
            contentType: "imageboth",
            showRoundedCorner: true,
            //It specifies the image in prefix location
            prefixIcon: "e-icon e-handup",
            //It specifies the image in suffix location
            suffixIcon: "e-icon e-palette"
        });
        $("#button_textandimage_small").ejButton({
            size: "small",
            //text and image is used as content
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup"
        });
        $("#button_imagetextimage_small").ejButton({
            size: "small",
            //images in both end and text in center is used as content
            contentType: "imagetextimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
            suffixIcon: "e-icon e-palette"
        });
    });


{% endhighlight %}

Execute the above code to render the following output.

![](/js/Button/Easy-Customization_images/Easy-Customization_img2.png) 


## Image Position

To provide the best look and feel for **Button**, position of button images is an important customizable option. With **imagePosition** property you can easily customize the position of images inside button without using any complex **CSS**. **imagePosition** property is applicable only with the **textandimage** of **contentType** property. This property supports the following values.

List of values supported by ImagePosition property

<table>
    <tr>
        <th>
            ImagePosition</th>
        <th>
            Description</th>
    </tr>
    <tr>
        <td>
            ImageLeft
        </td>
        <td>
            Support for aligning text in right and image in left.
        </td>
    </tr>
    <tr>
        <td>
            ImageRight
        </td>
        <td>
            Support for aligning text in left and image in right.
        </td>
    </tr>
    <tr>
        <td>
            ImageTop
        </td>
        <td>
            Support for aligning text in bottom and image in top.
        </td>
    </tr>
    <tr>
        <td>
            ImageBottom
        </td>
        <td>
            Support for aligning text in top and image in bottom.
        </td>
    </tr>
</table>


The following steps explains you the details about rendering the **Button** with the above mentioned image Position options.

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}


<button id="button_imageleft_normal">login</button>
<button id="button_imageleft_mini">login</button>
<button id="button_imageleft_small">login</button>
<button id="button_imageleft_medium">login</button>
<button id="button_imageleft_large">login</button>
<br />
<br />
<button id="button_imageright_normal">login</button>
<button id="button_imageright_mini">login</button>
<button id="button_imageright_small">login</button>
<button id="button_imageright_medium">login</button>
<button id="button_imageright_large">login</button>
<br />
<br />
<button id="button_imagetop">login</button>
<button id="button_imagebottom">login</button>


{% endhighlight %}

{% highlight javascript %}

    //Using imagePosition property you can render the button images with different position
    $(function () {
        $("#button_imageleft_normal").ejButton({
            size: "normal",
            imagePosition: "imageleft",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageleft_mini").ejButton({
            size: "mini",
            imagePosition: "imageleft",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageleft_small").ejButton({
            size: "small",
            imagePosition: "imageleft",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageleft_medium").ejButton({
            size: "medium",
            imagePosition: "imageleft",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageleft_large").ejButton({
            size: "large",
            imagePosition: "imageleft",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageright_normal").ejButton({
            size: "normal",
            imagePosition: "imageright",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageright_mini").ejButton({
            size: "mini",
            imagePosition: "imageright",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageright_small").ejButton({
            size: "small",
            imagePosition: "imageright",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageright_medium").ejButton({
            size: "medium",
            imagePosition: "imageright",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imageright_large").ejButton({
            size: "large",
            imagePosition: "imageright",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
        });
        $("#button_imagetop").ejButton({
            imagePosition: "imagetop",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
            width: 60
        });
        $("#button_imagebottom").ejButton({
            imagePosition: "imagebottom",
            contentType: "textandimage",
            showRoundedCorner: true,
            prefixIcon: "e-icon e-handup",
            width: 60
        });
    });
    
{% endhighlight %}

Execute the above code to render the following output.

![](/js/Button/Easy-Customization_images/Easy-Customization_img3.png)


## Theme support

You can control the style and appearance of **Button** control based on **CSS** classes. In order to apply styles to the **Button** control, you can refer two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer the **ej.widgets.all.min.css** file, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Button** control.

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

## Custom CSS

You can customize the appearance of **Button** control using **CSS** class. Define a **CSS** class as per requirement and assign the class name to **cssClass** property.

The following steps explains you the details about rendering the **Button** with custom **CSS.**

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

<button id="button_customCss1">login</button>
<button id="button_customCss2">login</button>
<button id="button_customCss3">login</button>
<button id="button_customCss4">login</button>
<button id="button_customCss5">login</button>

{% endhighlight %}

{% highlight javascript %}

    //implement custom CSS for each button
    $(function () {
        $("#button_customCss1").ejButton({
            cssClass: "customCss1",
            size: "small",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup",
        });
        $("#button_customCss2").ejButton({
            cssClass: "customCss2",
            size: "small",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
        $("#button_customCss3").ejButton({
            cssClass: "customCss3",
            size: "small",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
        $("#button_customCss4").ejButton({
            cssClass: "customCss4",
            size: "small",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
        $("#button_customCss5").ejButton({
            cssClass: "customCss5",
            size: "small",
            showRoundedCorner: true,
            contentType: "textandimage",
            prefixIcon: "e-icon e-handup"
        });
    });


{% endhighlight %}

Configure the **CSS** styles to apply on buttons.

{% highlight css %}

<style type="text/css" class="cssStyles">
    /* Customize the button background */
    .e-button.customCss1 {
        background-color: #121111;
    }
    .e-button.customCss2 {
        background-color: #94bbd5;
    }
    .e-button.customCss3 {
        background-color: #f3533c;
    }
    .e-button.customCss4 {
        background-color: #d1eeed;
    }
    .e-button.customCss5 {
        background-color: #deb66e;
    }
    /* Customize the button image & text color */
    .e-button.customCss1.e-btn.e-select .e-icon, .e-button.customCss1.e-btn.e-select .e-btntxt {
        color: #94bbd5;
    }
    .e-button.customCss2.e-btn.e-select .e-icon, .e-button.customCss2.e-btn.e-select .e-btntxt {
        color: #121111;
    }
    .e-button.customCss3.e-btn.e-select .e-icon, .e-button.customCss3.e-btn.e-select .e-btntxt {
        color: #cef6f7;
    }
    .e-button.customCss5.e-btn.e-select .e-icon, .e-button.customCss5.e-btn.e-select .e-btntxt {
        color: #534f4f;
    }
</style>


{% endhighlight %}


Execute the above code to render the following output.

![](/js/Button/Easy-Customization_images/Easy-Customization_img4.png)

## Enable/Disable Button widget

**Button** widget provides you an option to enable /disable the widget. You can disable the TimePicker by setting the “**enabled**” property value as **false**.

The following steps explain you to enable/disable property in **Button** widget.

In the **HTML** page, add a **&lt;input&gt;** element to configure **Button** widget.

{% highlight html %}
  
    <button id="button1">Button</button> 

{% endhighlight %}

{% highlight javascript %}

    // To enable/disable Button controls use the following code example.
    //disable Button:
    $(function () {
       $("#button1").ejButton();
        var btnObj = $("#button1").data("ejButton");
        btnObj.disable(); // disable the button
    });

    //enable Button:
    $(function () {
       $("#button1").ejButton();
        var btnObj = $("#button1").data("ejButton");
        btnObj.enable(); // enable the button;
    });

{% endhighlight %}


