---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: DropDownList
documentation: ug
---

# Appearance and Styling

**Popup Customization**  

**Popup Height**

**DropdownList** widget provides you support to customize the dimensions of the dropdown popup. By using **popupHeight** property, you can set the height of the popup list. Its data type is string. 

**Popup Width**

Dropdown list widget provides you support to customize the dimensions of the dropdown popup. By using **popupWidth** property, you can set the width of the popup list. Its data type is string. 

**Defining the popup customizing properties**

The following steps explains you the configuration of **popupHeight** & **popupWidth** properties in **DropdownList**

* In an **HTML** page, add a &lt;input&gt; element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;      &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;         $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>popupWidth</b>: "250px",                <b>popupHeight</b>: "100px"                          });        });    &lt;/script&gt;</td></tr>
</table>


* Output of the above steps



{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption=""%}

_Figure 21: Dropdown with popup customization property_  

**Adjusting Dropdown size**

**Width**

**DropdownList** widget provides you support to customize the dimensions of the dropdown textbox. By using **width** property you can set the width of the dropdown textbox. Its data type is string.

**Height**

**DropdownList** widget provides you support to customize the dimensions of the dropdown textbox. By using **height** property, you can set the height of the dropdown textbox. Its data type is string.

**Defining the dropdown size properties**

The following steps explains you the configuration of **height** & **width** properties in **DropdownList**

* In an **HTML** page, add a &lt;input&gt; element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b>// Initialize the control in <b>JavaScript</b><b> </b>&lt;script type="text/javascript"&gt;        $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>width</b>: "250px",                <b>height</b>: "50px"                          });        });&lt;/script&gt;</td></tr>
</table>


Output of the above steps


{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption=""%}

_Figure 22: Dropdown with dropdown textbox customization property_  

**Water Mark** 

**DropdownList** widget provides the support to water mark of the dropdown textbox. The **watermarkText** defines the text that display on page load. Its data type is string.

**Defining the Water Mark property**

The following steps explains the configuration of **watermarkText** properties in **DropdownList****.**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;      &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b><b>  </b>&lt;script type="text/javascript"&gt;   $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>watermarkText</b>: "Select"            });        }); &lt;/script&gt;</td></tr>
</table>


Output of the above steps


{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" Caption=""%}

_Figure 23: Dropdown with WaterMark property_  

**Enabling Rounded corner**

**DropdownList** widget provides you support to change the appearance of dropdown textbox. By using **showRoundedCorner** you can create a rounded corner on the dropdown textbox. Its data type is Boolean.

The following steps explains you  the configuration of Rounded corner of the **DropdownList**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;                &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;      &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",<b>                showRoundedCorner:true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* Output of the above steps


{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img4.png" Caption=""%}

_Figure 24: Dropdown with Rounded corner property_  

**Icons Support** 

You can add the icons or images with list items in dropdown popup by using sprite **CSS** class. The following steps explains you the configuration about the icons support with **DropdownList**


> {% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img5.png" Caption=""%}_**Note: Images for this sample are available in ‘installed location /themes/images’ and you need to define images in mentioned CSS. Henceforth the images display.**_ 


* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]   </b>  &lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="mailtoolslist"&gt;            &lt;ul&gt;                &lt;li&gt;                    &lt;div class="mailtools categorize"&gt;&lt;/div&gt;                    Categorize and Move</li>                &lt;li&gt;                    &lt;div class="mailtools done"&gt;&lt;/div&gt;                    Done</li>                &lt;li&gt;                    &lt;div class="mailtools flag"&gt;&lt;/div&gt;                    Flag & Move</li>                &lt;li&gt;                    &lt;div class="mailtools forward"&gt;&lt;/div&gt;                    Forward</li>                &lt;li&gt;                    &lt;div class="mailtools movetofolder"&gt;&lt;/div&gt;                    Move to Folder</li>                &lt;li&gt;                    &lt;div class="mailtools newmail"&gt;&lt;/div&gt;                    New E-mail</li>                &lt;li&gt;                    &lt;div class="mailtools meeting"&gt;&lt;/div&gt;                    New Meeting</li>                &lt;li&gt;                    &lt;div class="mailtools reply"&gt;&lt;/div&gt;                    Reply & Delete</li>            &lt;/ul&gt;     &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        var target;        $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "mailtoolslist"                });        });    &lt;/script&gt;</td></tr>
</table>


* Configure sprite **CSS** styles to **DropdownList**



{% highlight css %}

[CSS]

<style type="text/css" class="cssStyles">
        /*controls*/
        .mailtools {
            display: block;
            background-image: url('../images/iconsapps.png');
            height: 25px;
            width: 25px;
            background-position: center center;
            background-repeat: no-repeat;
        }

            .mailtools.done {
                background-position: 0 0;
            }

            .mailtools.movetofolder {
                background-position: 0 -22px;
            }

            .mailtools.categorize {
                background-position: 0 -46px;
            }

            .mailtools.flag {
                background-position: 0 -70px;
            }

            .mailtools.forward {
                background-position: 0 -94px;
            }

            .mailtools.newmail {
                background-position: 0 -116px;
            }

            .mailtools.reply {
                background-position: 0 -140px;
            }

            .mailtools.meeting {
                background-position: 0 -164px;
            }

        .control {
            margin-left: 20px;
        }

        .ctrllabel {
            padding-bottom: 3px;
        }
   </style>


{% endhighlight %}



Output of the above steps



{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img6.png" Caption=""%}

_Figure 25: Dropdown with Icons property_  

**Animation with Dropdown list** 

This feature adds some animation effect to dropdown widget when show /hide the popup list. This is achieved by setting Boolean value to **enableAnimation** property**.**

**Defining the Animation property**

The following steps explains you the configuration of **enableAnimation** properties in **DropdownList**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;   $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>enableAnimation :</b> true            });        }); &lt;/script&gt;</td></tr>
</table>
**Theme**

**DropdownList** control’s style and appearance can be controlled based on **CSS** classes. In order to apply styles to the **DropdownList** control, you need to refer two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **DropdownList** control namely

* bootstrap-theme

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

**Custom class with dropdown** 

**CSS** class can be used to customize the **Dropdown** control appearance. Define a **CSS** class as per your requirement and assign the class name to **cssClass** property. The data type of **cssClass** property is string. 

**Configuring the Custom CSS property**

The following steps explains you the configuration of **cssClass** properties in **DropdownList**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;       &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b>// Initialize the control in <b>JavaScript</b><b> </b>&lt;script type="text/javascript"&gt;$(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>cssClass</b>: "customclass"            });        });&lt;/script&gt;</td></tr>
</table>


* Configure the **CSS** styles to apply on **DropdownList**



{% highlight css %}

[CSS]  
  <style type="text/css">
        .customclass {
            background-color: #FFFFCC;
            font-weight: bold;
            font-family: sans-serif;
        }
    </style>


{% endhighlight %}



* Output of the above steps


{% include image.html url="/js/DropDownList/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img7.png" Caption=""%}

_Figure 26: Dropdown with cssClass property_  

