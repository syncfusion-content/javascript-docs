---
layout: post
title: Theme
description: theme
platform: js
control: ListBox
documentation: ug
---

# Theme

**ListBox** control’s style and appearance can be controlled based on **CSS** classes. In order to apply styles to the **ListBox** control, you can refer to two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer to the file **ej.widgets.all.min.css,** it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **ListBox** control namely,

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

The following screenshot illustrates the **ListBox** with Flat-lime and Flat-Saffron built-in themes.

![]("/js/ListBox/Theme_images/Theme_img1.png" Caption="ListBox with Flat-lime Theme")

![]("/js/ListBox/Theme_images/Theme_img2.png" Caption="ListBox with Flat-Saffron Theme")

## Custom class with ListBox

**CSS** class can be used to customize the **ListBox** control appearance. Define a **CSS** class as per your requirement and assign the class name to **cssClass** property. The data type of **cssClass** property is string. 

### Configuring the Custom CSS property

The following steps explains you the configuration of **cssClass** properties in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          cssClass: "customclass"
       });
    });

{% endhighlight %}


Configure the **CSS** styles to apply on **ListBox**.

{% highlight css %}

 
<style>
   .customclass {
       background-color: #FFFFCC;
       font-weight: bold;
       font-family: sans-serif;
   }
</style>


{% endhighlight %}

Output of the above steps.

![]("/js/ListBox/Theme_images/Theme_img3.png")

