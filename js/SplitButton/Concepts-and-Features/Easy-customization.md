---
layout: post
title: Easy-customization
description: easy customization
platform: js
control: Split Button
documentation: ug
---

# Easy customization

**Split Button** is used in many applications. **Split Button** Size, Content and content location is varied according to each application. The following sections describes you some customizable options for Sp**lit Button** that can perform easily. 

## Content for Split button

The **targetID** is a mandatory one, without this field it acts as normal button on two sides. This **targetID** property is used to specify the list of content for **Split Button**. The list of content is rendered as a vertical menu list. This vertical menu list is open, when you click on the down arrow of the **Split Button**.

The following steps explains you the details about rendering the **Split Button** with content.

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>  &lt;div class="spltspan"&gt;        <button id="spltbutton">login</button>        &lt;ul id="Ul11"&gt;            &lt;li&gt;<span>User</span>&lt;/li&gt;            &lt;li&gt;<span>Guest</span>&lt;/li&gt;            &lt;li&gt;<span>Admin</span>&lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#spltbutton").ejSplitButton({                size: "small",                contentType: "textandimage",                showRoundedCorner: true,                //targetID used to specify vertical menu content<b>                targetID: "Ul11",</b>                prefixIcon: "e-uiLight e-login"            });        });    &lt;/script&gt;</td></tr>
<tr>
<td>
{% highlight html %}<br><br><b>[HTML]</b>  <div class="spltspan">        <button id="spltbutton">login</button>        <ul id="Ul11">            <li><span>User</span></li>            <li><span>Guest</span></li>            <li><span>Admin</span></li>        </ul>    </div><br><br>{% endhighlight %}<br><br></td></tr>
</table>
****


Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Easy-customization_images/Easy-customization_img1.png" Caption="Figure 3: Split button with content"%}

## Button Size

You can render the **Split Button** in different sizes. The following table contains some predefined size option for rendering a **Split Button** in easiest way. Each size option has different height and width. Mainly it avoids the complexity in rendering **Split Button** with complex **CSS** class. 

_Table_ _1__: List of Button size_

<table>
<tr>
<td>
<b>normal</b></td><td>
Creates split button with content size.</td></tr>
<tr>
<td>
<b>mini</b></td><td>
Creates split button with inbuilt mini size height, width specified.</td></tr>
<tr>
<td>
<b>small</b></td><td>
Creates split button with inbuilt small size height, width specified.</td></tr>
<tr>
<td>
<b>medium</b></td><td>
Creates split button with inbuilt medium size height, width specified.</td></tr>
<tr>
<td>
<b>Large</b></td><td>
Creates split button with inbuilt large size height, width specified.</td></tr>
</table>


Apart from the above mentioned predefined size option, you can set your own width and height for S**plit Button** using **height** and **width** property.

The following steps explains you the details about rendering the **Split Button** with above mentioned size options.

* In the **HTML** page, add the following button elements to configure **Split Button** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;table&gt;            &lt;tr&gt;                                &lt;td class="btnsht"&gt;                    &lt;div class="spltspan"&gt;                        <button id="spltbutton_normal">login</button>                        &lt;ul id="Ul11"&gt;                            &lt;li&gt;<span>User</span>&lt;/li&gt;                            &lt;li&gt;<span>Guest</span>&lt;/li&gt;                            &lt;li&gt;<span>Admin</span>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/div&gt;                &lt;/td&gt;                             &lt;td&gt;                    <button id="spltbutton_mini">login</button>                    &lt;ul id="Ul21"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                                   &lt;td class="btnsht"&gt;                    <button id="spltbutton_small">login</button>                    &lt;ul id="Ul31"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                                 &lt;td class="btnsht"&gt;                    <button id="spltbutton_medium">login</button>                    &lt;ul id="Ul41"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                       &lt;td class="btnsht"&gt;                    <button id="spltbutton_large">login</button>                    &lt;ul id="Ul51"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                 &lt;td class="btnsht"&gt;                    <button id="spltbutton_customsize">login</button>                    &lt;ul id="Ul61"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //Here we used size property to render the split button in different sizes            $("#spltbutton_normal").ejSplitButton({                //normal size type is used<b>                size: "normal",</b>                showRoundedCorner: true,                contentType: "imageonly",                targetID: "Ul11",                prefixIcon: "e-uiLight e-login"            });            $("#spltbutton_mini").ejSplitButton({                //mini size type is used<b>                size: "mini",</b>                showRoundedCorner: true,                targetID: "Ul21",            });            $("#spltbutton_small").ejSplitButton({                //small size type is used<b>                size: "small",</b>                showRoundedCorner: true,                targetID: "Ul31",            });            $("#spltbutton_medium").ejSplitButton({                //medium size type is used<b>                size: "medium",</b>                showRoundedCorner: true,                targetID: "Ul41",            });            $("#spltbutton_large").ejSplitButton({                //large size type is used<b>                size: "large",</b>                showRoundedCorner: true,                targetID: "Ul51",                contentType: "textandimage",                prefixIcon: "e-login e-uiLight",            });            $("#spltbutton_customsize").ejSplitButton({                //user given height and width<b>                height: 50,</b><b>                width: 150,</b>                showRoundedCorner: true,                targetID: "Ul61",                contentType: "textandimage",                prefixIcon: "e-login e-uiLight",            });        });    &lt;/script&gt;</td></tr>
</table>


Configure the styles



{% highlight css %}

[CSS]    <style>
        .control {
            width: 500px;
        }
    </style>


{% endhighlight %}


Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Easy-customization_images/Easy-customization_img2.png" Caption="Figure 4: Split button with different sizes"%}

## Content Type

The content of the **Split Button** is mainly rendered as text and images. Instead of using complex **CSS** classes to render **Split Button** with different content types, you can use some predefined content type options listed in the following table. Using this content types you can easily add different types of content for **Split Button**. Split Button supports the following content types.

_Table_ _2__: List of content types_

<table>
<tr>
<td>
<b>textonly</b></td><td>
Supports only for text content only.</td></tr>
<tr>
<td>
<b>imageonly</b></td><td>
Supports only for image content only</td></tr>
<tr>
<td>
<b>imageboth</b></td><td>
Supports image for both ends of the button.</td></tr>
<tr>
<td>
<b>textandimage</b></td><td>
Supports image with the text content.</td></tr>
<tr>
<td>
<b>imagetextimage</b></td><td>
Supports image with both ends and middle in text.</td></tr>
</table>
### Prefix and Suffix icons

Icons inside the **Split Button** is added easily using **prefixIcon and suffixIcon** property. Location of the icon in **Split Button** is a necessary thing. You can customize the location of Icon easily using the following mentioned options.

**Split Button** control also supports the build-in icon libraries. The **ej.widgets.core.min** CSS contains definitions for important icons that are used in **Split Buttons**. You can use these build-in icons by mentioning the icon class name as value in **prefixIcon** and **suffixIcon** property. You can use any font icons that is defined in **ej.widgets.core.min** CSS. It avoids the complexity in specifying icon using sprite image and CSS.

For example the following build-in CSS class are used to display the font icons that is used by media player.

* e-mediaback

* e-mediaforward

* e-medianext

* e-mediaprev

* e-mediaeject

* e-mediaclose

* e-mediapause

* e-mediaplay

#### Prefix Icon

It inserts the icon at the starting position of **Split Button**. After this prefix icon, you can use text or suffix icon.

#### Suffix Icon

It inserts the icon at the ending position of **Split Button**. Before this suffix icon, you can use text or prefix icon.

The following steps explains you the details on rendering the **Split Button** with above mentioned **content type**, **prefix** and **suffix icon** options

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageonly">login</button>                &lt;ul id="Ul11"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td&gt;                <button id="spltbutton_textonly">login</button>                &lt;ul id="Ul21"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageboth">login</button>                &lt;ul id="Ul31"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_textandimage">login</button>                &lt;ul id="Ul41"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imagetextimage">login</button>                &lt;ul id="Ul51"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>//</b> Initialize the control in <b>JavaScript</b><b>    </b>&lt;script type="text/javascript"&gt;     // Here we used contentType property to render the split button with different contents     $(function () {         $("#spltbutton_imageonly").ejSplitButton({             size: "medium",             //only image is used as content<b>             contentType: "imageonly",</b>             showRoundedCorner: true,             prefixIcon: "e-uiLight e-handup",             targetID: "Ul11",         });         $("#spltbutton_textonly").ejSplitButton({             size: "medium",             //only text is used as content<b>             contentType: "textonly",</b>             showRoundedCorner: true,             targetID: "Ul21",         });         $("#spltbutton_imageboth").ejSplitButton({             size: "medium",             //only images in both end is used as content<b>             contentType: "imageboth",</b>             showRoundedCorner: true,             //e-handup is a build in class, which specify font icon             prefixIcon: "e-uiLight e-handup",             //e-palette is a build in class, which specify font icon             suffixIcon: "e-uiLight e-palette",             targetID: "Ul31",         });         $("#spltbutton_textandimage").ejSplitButton({             size: "medium",             //text and image is used as content<b>             contentType: "textandimage",</b>             showRoundedCorner: true,             prefixIcon: "e-uiLight e-handup",             targetID: "Ul41",         });         $("#spltbutton_imagetextimage").ejSplitButton({             size: "medium",             //images in both end and text in center is used as content<b>             contentType: "imagetextimage",</b>             showRoundedCorner: true,             //It specifies the image in prefix location             prefixIcon: "e-uiLight e-handup",             //It specifies the image in suffix location             suffixIcon: "e-uiLight e-palette",             targetID: "Ul51",         });     });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

**[CSS]**    <style>
        .control {
            width: 500px;
        }
    </style>


{% endhighlight %}


Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Easy-customization_images/Easy-customization_img3.png" Caption="Figure 5: Split button with different content types"%}

## Image Position

To provide the best look and feel for **Split Button**, position of images in **Split Button** is important. Using **imagePosition** property, you can easily customize the position of images inside **Split Button** without using any complex CSS. **imagePosition** property is applicable only with the **textandimage** content type property. This property represent the position of images with respect to text.


<table>
<tr>
<td>
<b>imageleft</b></td><td>
Support for aligning text in right and image in left.</td></tr>
<tr>
<td>
<b>imageright</b></td><td>
Support for aligning text in left and image in right.</td></tr>
<tr>
<td>
<b>imagetop</b></td><td>
Support for aligning text in bottom and image in top.</td></tr>
<tr>
<td>
<b>imagebottom</b></td><td>
Support for aligning text in top and image in bottom.</td></tr>
</table>

The following steps explains you the details on rendering the **Split Button** with above mentioned image position options.

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageleft_normal">login</button>                &lt;ul id="Ul11"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td&gt;                <button id="spltbutton_imageleft_small">login</button>                &lt;ul id="Ul21"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageleft_medium">login</button>                &lt;ul id="Ul31"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageleft_large">login</button>                &lt;ul id="Ul41"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;                   &lt;/tr&gt;      &lt;tr&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageright_normal">login</button>                &lt;ul id="Ul1"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td&gt;                <button id="spltbutton_imageright_small">login</button>                &lt;ul id="Ul2"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageright_medium">login</button>                &lt;ul id="Ul3"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imageright_large">login</button>                &lt;ul id="Ul4"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;                   &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                <button id="spltbutton_imagetop">login</button>                &lt;ul id="Ul5"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td&gt;                <button id="spltbutton_imagebottom">login</button>                &lt;ul id="Ul6"&gt;                    &lt;li&gt;<span>User</span>&lt;/li&gt;                    &lt;li&gt;<span>Guest</span>&lt;/li&gt;                    &lt;li&gt;<span>Admin</span>&lt;/li&gt;                &lt;/ul&gt;            &lt;/td&gt;                            &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    //Using imagePosition property we can render the split button images with different position    $(function () {        $("#spltbutton_imageleft_normal").ejSplitButton({<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul11",        });        $("#spltbutton_imageleft_small").ejSplitButton({            size: "small",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul21",        });        $("#spltbutton_imageleft_medium").ejSplitButton({            size: "medium",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul31",        });        $("#spltbutton_imageleft_large").ejSplitButton({            size: "large",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul1",        });        $("#spltbutton_imageright_normal").ejSplitButton({            <b>imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul2",        });        $("#spltbutton_imageright_small").ejSplitButton({            size: "small",<b>            imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul3",        });        $("#spltbutton_imageright_medium").ejSplitButton({            size: "medium",<b>            imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul4",        });        $("#spltbutton_imageright_large").ejSplitButton({            size: "large",<b>            imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul41",        });        $("#spltbutton_imagetop").ejSplitButton({<b>            imagePosition: "imagetop",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul5",            height: 60        });        $("#spltbutton_imagebottom").ejSplitButton({            <b>imagePosition: "imagebottom",</b>            contentType: "textandimage",            showRoundedCorner: true,            prefixIcon: "e-uiLight e-handup",            targetID: "Ul6",            height: 60        });    });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .control {
            width: 420px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Easy-customization_images/Easy-customization_img4.png" Caption="Figure 6: Split button with different image positions"%}

## Theme support

You can control the style and appearance of **Split Button** based on **CSS** classes. In order to apply styles to the **Split Button** control, you can refer two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer the **ej.widgets.all.min.css** file, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Split Button** control namely

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

You can use the **CSS** class to customize the **Split Button** control appearance. Define a **CSS** class as per requirement and assign the class name to **cssClass** property.

The following steps explains you the details about rendering the **Split Button** with custom CSS.

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td class="btnsht"&gt;                    &lt;div class="spltspan"&gt;                        <button id="spltbutton_customCss1">login</button>                        &lt;ul id="Ul11"&gt;                            &lt;li&gt;<span>User</span>&lt;/li&gt;                            &lt;li&gt;<span>Guest</span>&lt;/li&gt;                            &lt;li&gt;<span>Admin</span>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/div&gt;                &lt;/td&gt;                &lt;td&gt;                    <button id="spltbutton_customCss2">login</button>                    &lt;ul id="Ul21"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                &lt;td class="btnsht"&gt;                    <button id="spltbutton_customCss3">login</button>                    &lt;ul id="Ul31"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                &lt;td class="btnsht"&gt;                    <button id="spltbutton_customCss4">login</button>                    &lt;ul id="Ul41"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;                &lt;td class="btnsht"&gt;                    <button id="spltbutton_customCss5">login</button>                    &lt;ul id="Ul51"&gt;                        &lt;li&gt;<span>User</span>&lt;/li&gt;                        &lt;li&gt;<span>Guest</span>&lt;/li&gt;                        &lt;li&gt;<span>Admin</span>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //implement custom CSS for each split button            $("#spltbutton_customCss1").ejSplitButton({<b>                cssClass: "customCss1",</b>                size: "small",                showRoundedCorner: true,                contentType: "textandimage",                prefixIcon: "e-uiLight e-handup",                targetID: "Ul11"            });            $("#spltbutton_customCss2").ejSplitButton({<b>                cssClass: "customCss2",</b>                size: "small",                showRoundedCorner: true,                contentType: "textandimage",                prefixIcon: "e-uiLight e-handup",                targetID: "Ul21"            });            $("#spltbutton_customCss3").ejSplitButton({<b>                cssClass: "customCss3",</b>                size: "small",                showRoundedCorner: true,                contentType: "textandimage",                prefixIcon: "e-uiLight e-handup",                targetID: "Ul31"            });            $("#spltbutton_customCss4").ejSplitButton({                <b>cssClass: "customCss4",</b>                size: "small",                showRoundedCorner: true,                contentType: "textandimage",                prefixIcon: "e-uiLight e-handup",                targetID: "Ul41"            });            $("#spltbutton_customCss5").ejSplitButton({                <b>cssClass: "customCss5",</b>                size: "small",                showRoundedCorner: true,                contentType: "textandimage",                prefixIcon: "e-uiLight e-handup",                targetID: "Ul51"            });        });    &lt;/script&gt;</td></tr>
</table>


Configure the CSS styles to apply on buttons



{% highlight css %}

**[CSS]**
<style type="text/css">
        /* Customize the button background */
       .e-split .customCss1 {
            background-color: #121111;
        }
        .e-split .customCss2 {
            background-color: #94bbd5;
        }
        .e-split .customCss3 {
            background-color: #f3533c;
        }
        .e-split .customCss4 {
            background-color: #d1eeed;
        }
        .e-split .customCss5 {
            background-color: #deb66e;
        }
         /* Customize the button image & text color */
        .e-split .customCss1.e-btn.e-select .e-icon, .e-split .customCss1.e-btn.e-select .e-btntxt {
            color: #94bbd5;
        }
        .e-split .customCss2.e-btn.e-select .e-icon, .e-split .customCss2.e-btn.e-select .e-btntxt {
            color: #121111;
        }
        .e-split .customCss3.e-btn.e-select .e-icon, .e-split .customCss3.e-btn.e-select .e-btntxt {
            color: #cef6f7;
        }
        .e-split .customCss5.e-btn.e-select .e-icon, .e-split .customCss5.e-btn.e-select .e-btntxt {
            color: #534f4f;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Easy-customization_images/Easy-customization_img5.png" Caption="Figure 7: Split button with Custom CSS"%}

