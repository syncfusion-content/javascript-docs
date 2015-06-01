---
layout: post
title: Easy-Customization
description: easy customization
platform: js
control: Toggle Button
documentation: ug
---

# Easy Customization

**Toggle Button** is used in all applications. Toggle Button Size, Content and content location is varied according to each application. The following section contains some customizable option for T**oggle Button** that can perform easily. 

## Toggle State

**Toggle Button** has two states like off / on state in a switch. By default you can set any state at initial and then you can move from one state to another state by clicking on the **Toggle Button**. These two states are **Default** and **Active.****toggleState** property is used to****set the state of **Toggle Button** as default state or active state.

The following steps explains you the details about rendering the **Toggle Button** with different toggle state.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="checkbox" id="toggle_default" /&gt;        &lt;br /&gt;    &lt;input type="checkbox" id="toggle_active" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            $("#toggle_default").ejToggleButton({                size: "small",                contentType: "textandimage",                defaultText: "Play",                activeText: "Pause",                defaultPrefixIcon: "e-mediaplay e-uiLight",                activePrefixIcon: "e-mediapause e-uiLight",                //set the button in default state<b>                toggleState: false</b>            });            $("#toggle_active").ejToggleButton({                size: "small",                contentType: "textandimage",                defaultText: "Play",                activeText: "Pause",                defaultPrefixIcon: "e-mediaplay e-uiLight",                activePrefixIcon: "e-mediapause e-uiLight",                //set the button in active state<b>                toggleState: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img1.png" Caption=""%}

_Figure 4: Toggle button with two different toggle states_



## Toggle state with icons

### Prefix and Suffix Icons

You can add icons in prefix and suffix position of **Toggle Button**. Location of Icon is customized easily using the following mentioned option. This is applicable for the content type’s **imageOnly**, **textandimage**, **imagetextimage** and **imageboth**.

**Toggle Button** control also supports the build-in icon libraries. The **ej.widgets.core.min** CSS contains the definition for important icons that are used in toggle buttons. You can use these build-in icons by mentioning the icon class name as value in **defaultPrefixIcon**, **defaultSuffixIcon**, **activePrefixIcon**,****and **activeSuffixIcon** property. You can use any font icons that is defined in **ej.widgets.core.min** CSS. It avoids the complexity in specifying icon using sprite image and CSS.

For example the following mentioned build-in CSS class are used to show the font icons that are used by media player.

* e-mediaback

* e-mediaforward

* e-medianext

* e-mediaprev

* e-mediaeject

* e-mediaclose

* e-mediapause

* e-mediaplay

### Prefix Icon

It inserts the icon at the starting position of **Toggle Button**. After this prefix icon, you can use text or suffix icon.

### Suffix Icon

It inserts the icon at the ending position of **Toggle Button**. Before this suffix icon, you can use text or prefix icon.

You can also set icon in different location (prefix, suffix) and in different state (default, active) by using the option provided. The following properties are defined for merging the option to add text, icon with different position and in toggle states.

_Table_ _1__: Property Table_

<table>
<tr>
<td>
<b>activeText</b></td><td>
Specifies the text of toggle button in active state</td></tr>
<tr>
<td>
<b>activePrefixIcon</b></td><td>
Specifies the prefix icon of toggle button in active state</td></tr>
<tr>
<td>
<b>activeSuffixIcon</b></td><td>
Specifies the suffix icon of toggle button in active state</td></tr>
<tr>
<td>
<b>defaultText</b></td><td>
Specifies the text of toggle button in default state.</td></tr>
<tr>
<td>
<b>defaultPrefixIcon</b></td><td>
Specifies the prefix icon of toggle button in default state</td></tr>
<tr>
<td>
<b>defaultSuffixIcon</b></td><td>
Specifies the suffix icon of toggle button in default state</td></tr>
</table>


The following steps explains you the details about rendering the **Toggle Button** with above mentioned customization properties.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget



<table>
<tr>
<td>
<b> [HTML]</b>    &lt;input type="checkbox" id="toggle_content" /&gt;    <label for="toggle_content">Toggle</label></td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;            $(function () {                $("#toggle_content").ejToggleButton({                    showRoundedCorner: true,                    contentType: "imagetextimage",                    //e-mediaforward class contain font icon<b>                    defaultPrefixIcon: "e-mediaforward e-uiLight",</b><b>                    //e-mediaback class contain font icon</b><b>                    activePrefixIcon: "e-mediaback e-uiLight",</b><b>                    defaultText: "forward",</b><b>                    activeText: "backward",</b><b>                    //e-undo class contain font icon</b><b>                    defaultSuffixIcon: "e-undo e-uiLight",</b><b>                    //e- redo class contain font icon</b><b>                    activeSuffixIcon: "e-redo e-uiLight"</b>                });            });    &lt;/script&gt;</td></tr>
</table>


Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img2.png" Caption=""%}

_Figure 5: Before clicking the toggle button_

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img3.png" Caption=""%}

_Figure 6: After clicking the toggle button_

## Toggle button size

You can render the **Toggle Button** in different sizes. You can use some predefined size option for rendering a **Toggle Button** in easiest way. Each size option has different height and width. It mainly avoids the complexity in rendering **Toggle Button** with complex CSS class. You can mention the **size** of the **Toggle Button** using the following five predefined size options. 

_Table_ _2__: Predefined Toggle Button size_

<table>
<tr>
<td>
<b>normal</b></td><td>
Creates toggle button with content size.</td></tr>
<tr>
<td>
<b>mini</b></td><td>
Creates toggle button with inbuilt mini size height, width specified.</td></tr>
<tr>
<td>
<b>small</b></td><td>
Creates toggle button with inbuilt small size height, width specified.</td></tr>
<tr>
<td>
<b>medium</b></td><td>
Creates toggle button with inbuilt medium size height, width specified.</td></tr>
<tr>
<td>
<b>large</b></td><td>
Creates toggle button with inbuilt large size height, width specified.</td></tr>
</table>


You can also set your own width and height for toggle button using height and width property.

The following steps explains you the details about rendering the **Toggle Button** with above mentioned size options.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_normal" /&gt;                <label for="toggle_normal">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_mini" /&gt;                <label for="toggle_mini">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_small" /&gt;                <label for="toggle_small">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_medium" /&gt;                <label for="toggle_medium">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_large" /&gt;                <label for="toggle_large">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;      &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customSize" /&gt;                <label for="toggle_customSize">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    //Here use size property to render the toggle button in different sizes    $(function () {        $("#toggle_normal").ejToggleButton({            //normal size of toggle button            <b>size: "normal",</b>            showRoundedCorner: true,            contentType: "imageonly",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight",        });        $("#toggle_mini").ejToggleButton({            defaultText: "Play",            showRoundedCorner: true,            activeText: "Next",            //mini size of toggle button<b>            size: "mini",</b>        });        $("#toggle_small").ejToggleButton({            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            //small size of toggle button<b>            size: "small",</b>        });        $("#toggle_medium").ejToggleButton({            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            //medium size of toggle button            <b>size: "medium",</b>        });        $("#toggle_large").ejToggleButton({            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            //large size of toggle button<b>            size: "large",</b>            contentType: "textandimage",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight",        });        $("#toggle_customSize").ejToggleButton({            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            //set own height and width<b>            height: 50,</b><b>            width: 150,</b>            contentType: "textandimage",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight",        });    });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .control {
            width: 600px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img4.png" Caption=""%}

_Figure 7: Toggle button in different sizes_

## Content type

The content of the **Toggle Button** is mainly text and images. Instead of using complex CSS classes to render **Toggle Button** with different content types, you can use some predefined content type options as listed in the following table. Using this content type you can easily add different types of content for **Toggle Button**. The **Toggle Button** supports the following content types.

_Table_ _3__: List of Content types_

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
Supports image for both ends of the toggle button.</td></tr>
<tr>
<td>
<b>textandimage</b></td><td>
Supports image with the text content.</td></tr>
<tr>
<td>
<b>imagetextimage</b></td><td>
Supports image with both ends and middle in text.</td></tr>
</table>


The following steps explains you the details about rendering the **Toggle Button** with above mentioned **content type** options.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageonly" /&gt;                <label for="toggle_imageonly">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_textonly" /&gt;                <label for="toggle_textonly">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageboth" /&gt;                <label for="toggle_imageboth">Toggle</label>            &lt;/td&gt;                   &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_textandimage" /&gt;                <label for="toggle_textandimage">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imagetextimage" /&gt;                <label for="toggle_imagetextimage">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;         &lt;/table&gt;    &lt;br /&gt;    &lt;br /&gt;     &lt;table&gt;          &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageonly_small" /&gt;                <label for="toggle_imageonly_small">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_textonly_small" /&gt;                <label for="toggle_textonly_small">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageboth_small" /&gt;                <label for="toggle_imageboth_small">Toggle</label>            &lt;/td&gt;                   &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_textandimage_small" /&gt;                <label for="toggle_textandimage_small">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imagetextimage_small" /&gt;                <label for="toggle_imagetextimage_small">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>   &lt;script type="text/javascript"&gt;      // Here use contentType property to render the toggle button with different contents      $(function () {          $("#toggle_imageonly").ejToggleButton({              showRoundedCorner: true,              //only image is used as content<b>              contentType: "imageonly",</b>              defaultPrefixIcon: "e-mediaplay e-uiLight",              activePrefixIcon: "e-mediapause e-uiLight"          });          $("#toggle_textonly").ejToggleButton({              //only text is used as content<b>              contentType: "textonly",</b>              defaultText: "Play",              showRoundedCorner: true,              activeText: "Next"          });          $("#toggle_imageboth").ejToggleButton({              //only images in both end is used as content<b>              contentType: "imageboth",</b>              showRoundedCorner: true,              defaultPrefixIcon: "e-mediaforward e-uiLight",              activePrefixIcon: "e-mediaback e-uiLight",              defaultSuffixIcon: "e-undo e-uiLight",              activeSuffixIcon: "e-redo e-uiLight"          });          $("#toggle_textandimage").ejToggleButton({              //text and image is used as content<b>              contentType: "textandimage",</b>              showRoundedCorner: true,              defaultText: "Play",              activeText: "Next",              defaultPrefixIcon: "e-mediaplay e-uiLight",              activePrefixIcon: "e-mediapause e-uiLight"          });          $("#toggle_imagetextimage").ejToggleButton({              //image text image is used as content<b>              contentType: "imagetextimage",</b>              showRoundedCorner: true,              defaultPrefixIcon: "e-mediaforward e-uiLight",              activePrefixIcon: "e-mediaback e-uiLight",              defaultText: "forward",              activeText: "backward",              defaultSuffixIcon: "e-undo e-uiLight",              activeSuffixIcon: "e-redo e-uiLight"          });          $("#toggle_imageonly_small").ejToggleButton({              size: "small",              showRoundedCorner: true,<b>              contentType: "imageonly",</b>              defaultPrefixIcon: "e-mediaplay e-uiLight",              activePrefixIcon: "e-mediapause e-uiLight"          });          $("#toggle_textonly_small").ejToggleButton({              size: "small",<b>              contentType: "textonly",</b>              defaultText: "Play",              showRoundedCorner: true,              activeText: "Next"          });          $("#toggle_imageboth_small").ejToggleButton({              size: "small",            <b>  contentType: "imageboth",</b>              showRoundedCorner: true,              defaultPrefixIcon: "e-mediaforward e-uiLight",              activePrefixIcon: "e-mediaback e-uiLight",              defaultSuffixIcon: "e-undo e-uiLight",              activeSuffixIcon: "e-redo e-uiLight"          });          $("#toggle_textandimage_small").ejToggleButton({              size: "small",<b>              contentType: "textandimage",</b>              showRoundedCorner: true,              defaultText: "Play",              activeText: "Next",              defaultPrefixIcon: "e-mediaplay e-uiLight",              activePrefixIcon: "e-mediapause e-uiLight"          });          $("#toggle_imagetextimage_small").ejToggleButton({              size: "small",<b>              contentType: "imagetextimage",</b>              showRoundedCorner: true,              defaultPrefixIcon: "e-mediaforward e-uiLight",              activePrefixIcon: "e-mediaback e-uiLight",              defaultText: "forward",              activeText: "backward",              defaultSuffixIcon: "e-undo e-uiLight",              activeSuffixIcon: "e-redo e-uiLight"          });      });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .normal {
            width: 300px;
        }

        .small {
            width: 450px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img5.png" Caption=""%}

_Figure 8: Toggle button with different content types_

## Image position

To provide the best look and feel for **Toggle Button**, position of images in toggle button is important. You can easily customize the position of images inside toggle button using **imagePosition** property without using any complex CSS. **imagePosition** property is applicable only with the **textandimage** content type property. This property represent the position of images with respect to text.

_Table_ _4__: Property Table_

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


The following steps explains you the details about rendering the **Toggle Button** with above mentioned image Position options.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageleft_normal" /&gt;                <label for="toggle_imageleft_normal">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageleft_mini" /&gt;                <label for="toggle_imageleft_mini">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageleft_small" /&gt;                <label for="toggle_imageleft_small">Toggle</label>            &lt;/td&gt;                   &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageleft_medium" /&gt;                <label for="toggle_imageleft_medium">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageleft_large" /&gt;                <label for="toggle_imageleft_large">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;         &lt;/table&gt;    &lt;br /&gt;    &lt;br /&gt;     &lt;table&gt;          &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageright_normal" /&gt;                <label for="toggle_imageright_normal">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageright_mini" /&gt;                <label for="toggle_imageright_mini">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageright_small" /&gt;                <label for="toggle_imageright_small">Toggle</label>            &lt;/td&gt;                   &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageright_medium" /&gt;                <label for="toggle_imageright_medium">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imageright_large" /&gt;                <label for="toggle_imageright_large">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;     &lt;br /&gt;    &lt;br /&gt;     &lt;table&gt;          &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imagetop" /&gt;                <label for="toggle_imagetop">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_imagebottom" /&gt;                <label for="toggle_imagebottom">Toggle</label>            &lt;/td&gt;                       &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    //It explains how to render the toggle button images with different position    $(function () {        $("#toggle_imageleft_normal").ejToggleButton({            size: "normal",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageleft_mini").ejToggleButton({            size: "mini",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageleft_small").ejToggleButton({            size: "small",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageleft_medium").ejToggleButton({            size: "medium",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageleft_large").ejToggleButton({            size: "large",<b>            imagePosition: "imageleft",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageright_normal").ejToggleButton({            size: "normal",<b>            imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageright_mini").ejToggleButton({            size: "mini",            <b>imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageright_small").ejToggleButton({            size: "small",            <b>imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageright_medium").ejToggleButton({            size: "medium",           <b> imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imageright_large").ejToggleButton({            size: "large",<b>            imagePosition: "imageright",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_imagetop").ejToggleButton({<b>            imagePosition: "imagetop",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight",            width: 60        });        $("#toggle_imagebottom").ejToggleButton({<b>            imagePosition: "imagebottom",</b>            contentType: "textandimage",            showRoundedCorner: true,            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight",            width: 60        });    });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .one {
            width: 450px;
        }

        .two{
            width: 115px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img6.png" Caption=""%}

_Figure 9: Toggle button with different type of image position_

## Theme support

You can control the style and appearance of **Toggle Button** based on CSS classes. To apply styles to the **Toggle Button** control, you can refer two files, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Toggle Button** control namely,

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

You can use the CSS to customize the **Toggle Button** control appearance. Define a CSS class as per requirement and assign the class name to **cssClass** property.

The following steps explains you the details about rendering the **Toggle Button** with custom CSS.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customCss1" /&gt;                <label for="toggle_customCss1">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customCss2" /&gt;                <label for="toggle_customCss2">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customCss3" /&gt;                <label for="toggle_customCss3">Toggle</label>            &lt;/td&gt;                   &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customCss4" /&gt;                <label for="toggle_customCss4">Toggle</label>            &lt;/td&gt;                 &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="toggle_customCss5" /&gt;                <label for="toggle_customCss5">Toggle</label>            &lt;/td&gt;        &lt;/tr&gt;         &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    //implement custom CSS for each toggle button    $(function () {        $("#toggle_customCss1").ejToggleButton({<b>            cssClass: "customCss1",</b>            size: "small",            showRoundedCorner: true,            contentType: "textandimage",            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_customCss2").ejToggleButton({<b>            cssClass: "customCss2",</b>            size: "small",            showRoundedCorner: true,            contentType: "textandimage",            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_customCss3").ejToggleButton({<b>            cssClass: "customCss3",</b>            size: "small",            showRoundedCorner: true,            contentType: "textandimage",            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_customCss4").ejToggleButton({<b>            cssClass: "customCss4",</b>            size: "small",            showRoundedCorner: true,            contentType: "textandimage",            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });        $("#toggle_customCss5").ejToggleButton({<b>            cssClass: "customCss5",</b>            size: "small",            showRoundedCorner: true,            contentType: "textandimage",            defaultText: "Play",            activeText: "Next",            defaultPrefixIcon: "e-mediaplay e-uiLight",            activePrefixIcon: "e-mediapause e-uiLight"        });    });    &lt;/script&gt;</td></tr>
</table>


Configure the CSS styles to apply on buttons.



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
        /* Customize the button background */
        .e-togglebutton.customCss1 {
            background-color: #121111;
        }
        .e-togglebutton.customCss2 {
            background-color: #94bbd5;
        }
        .e-togglebutton.customCss3 {
            background-color: #f3533c;
        }
        .e-togglebutton.customCss4 {
            background-color: #d1eeed;
        }
        .e-togglebutton.customCss5 {
            background-color: #deb66e;
        }
         /* Customize the button image & text color */
        .e-togglebutton.customCss1.e-btn.e-select .e-icon, .e-togglebutton.customCss1.e-btn.e-select .e-btntxt {
            color: #94bbd5;
        }
        .e-togglebutton.customCss2.e-btn.e-select .e-icon, .e-togglebutton.customCss2.e-btn.e-select .e-btntxt {
            color: #121111;
        }
        .e-togglebutton.customCss3.e-btn.e-select .e-icon, .e-togglebutton.customCss3.e-btn.e-select .e-btntxt {
            color: #cef6f7;
        }
        .e-togglebutton.customCss5.e-btn.e-select .e-icon, .e-togglebutton.customCss5.e-btn.e-select .e-btntxt {
            color: #534f4f;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img7.png" Caption=""%}

_Figure 10: Toggle button with Custom CSS_

