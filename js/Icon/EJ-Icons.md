---
layout: post
title: Essential Studio for JavaScript:Icon Package
description: Essential Studio for JavaScript:Icon Package
platform: js
control: General Topics 
documentation: ug
api : /api/js/
---

# EJ Icon Package

The **Essential Studio for JavaScript** provides a set of icons that can be utilized in your application by applying the Unicode Content in element. To make it simple and standard, you have to create the custom icon class by defining the unicode content and refer that class with prefix of `e-icon`. 

## How to use EJ icons in your application?

**Step 1:**

To use the icon fonts in your application, you need to maintain the folder structure of the theme files and the corresponding images for icons.

You have to include the common-images folder in the specified theme folder for displaying icons and refer theme files in your application.

**For example**:

“default-theme” folder CSS which contains the “ej.widgets.all.min.css/ej.web.all.min.css” and “ej.theme.min.css” file. The “ej.widgets.core.min.css” file is in the outside of the default theme folder as shown below:

![](/js/Icon/IconLibrary_images/themefolder.png)

Theme files are available in the following location:

(Installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\css\web\default-theme.


**Step 2:**

The following example showcases to display the EJ Icon by using their corresponding unicode content.

{% tabs %}
{% highlight html %}

<!doctype html>
<html>
<head>
    <title>Essential Studio for JavaScript : EJ Icon Package</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
</head>
<body>
  <div class="icons">
   <ul>
     <li>
       <div class="e-icon e-custom-search"></div>
     </li>
     <li>
       <div class="e-icon e-custom-settings"></div>
     </li>
     <li>
       <div class="e-icon e-custom-upload"></div>
     </li>
     <li>
       <div class="e-icon e-custom-font"></div>
     </li>
   </ul>
   <ul>
      <li>
        <div class="e-icon e-custom-indent"></div>
      </li>
      <li>
        <div class="e-icon e-custom-outdent"></div>
      </li>
      <li>
        <div class="e-icon e-custom-redo"></div>
      </li>
      <li>
        <div class="e-icon e-custom-undo"></div>
      </li>
     </ul>
  </div>
</body>
</html>

{% endhighlight %}

{% highlight css %}

<style type="text/css" class="cssStyles">
   div.icons li
        {
            display: inline-block;
            vertical-align: middle;
            padding: 20px;
            list-style: none;
           
        }
    .e-custom-search:before{
    content: "\e82e"
    }

   .e-custom-settings:before{
    content: "\e644"
    }

   .e-custom-upload:before{
    content: "\e678"
    }

   .e-custom-font:before{
    content: "\e632"
    }

   .e-custom-indent:before{
   content: "\e603"
    }

  .e-custom-outdent:before{
     content: "\e604"
    }

   .e-custom-redo:before{
     content: "\e606"
    }
   .e-custom-undo:before{
     content: "\e607"
    }
</style>

{% endhighlight %}
{% endtabs %}

N>  Make sure the CSS file (ej.widgets.all.min.css/ej.web.all.min.css) is referred in your application.

Execute the above code to render the following output.

![](/js/Icon/IconLibrary_images/output.png)

**Step 3:**

The complete list of EJ icons are listed in the following table. You have to use the below Unicode content in your application.

  <style type="text/css" class="cssStyles"> 
      table {
          width: 730px;
      } 
      .txt{
	    margin-top: 5px;
        text-align:center;
        font-size: small;
        word-wrap: break-word;
       }
	  .spriteimage {
         background-image: url('IconLibrary_images/spritesheet.png');			
		 height: 50px;
		 width: 50px;
		 background-repeat: no-repeat;
		 display: block;
         margin: 0 auto;
	   }

.icon-media-small-screen {
  background-position: 6px 10px;
}
.icon-media-backward {
  background-position: -42px 8px;
}
.icon-media-download {
  background-position: -88px 8px;
}
.icon-media-forward {
  background-position: -132px 8px;
}
.icon-media-full-screen {
  background-position: -184px 8px;
}
.icon-media-mute {
  background-position: -232px 8px;
}
.icon-media-next {
  width: 32px;
  height: 32px;
  background-position: -288px 0;
}
.icon-media-next-item {
  width: 32px;
  height: 32px;
  background-position: -336px 0;
}
.icon-media-pause {
  width: 32px;
  height: 32px;
  background-position: -384px 0;
}
.icon-uniE109 {
  width: 32px;
  height: 32px;
  background-position: -432px 0;
}
.icon-uniE10A {
  width: 32px;
  height: 32px;
  background-position: -480px 0;
}
.icon-uniE10B {
  width: 32px;
  height: 32px;
  background-position: -528px 0;
}
.icon-media-play {
  width: 32px;
  height: 32px;
  background-position: -576px 0;
}
.icon-uniE111 {
  width: 32px;
  height: 32px;
  background-position: -624px 0;
}
.icon-uniE112 {
  width: 32px;
  height: 32px;
  background-position: -672px 0;
}
.icon-media-Playlist {
  width: 32px;
  height: 32px;
  background-position: -720px 0;
}
.icon-uniE115 {
  width: 32px;
  height: 32px;
  background-position: 0 -48px;
}
.icon-uniE116 {
  width: 32px;
  height: 32px;
  background-position: -48px -48px;
}
.icon-uniE117 {
  width: 32px;
  height: 32px;
  background-position: -96px -48px;
}
.icon-uniE118 {
  width: 32px;
  height: 32px;
  background-position: -144px -48px;
}
.icon-media-previous {
  width: 32px;
  height: 32px;
  background-position: -192px -48px;
}
.icon-media-previous-item {
  width: 32px;
  height: 32px;
  background-position: -240px -48px;
}
.icon-media-repeat {
  width: 32px;
  height: 32px;
  background-position: -288px -48px;
}
.icon-media-select {
  width: 32px;
  height: 32px;
  background-position: -336px -48px;
}
.icon-media-settings {
  width: 32px;
  height: 32px;
  background-position: -384px -48px;
}
.icon-media-shuffle {
  width: 32px;
  height: 32px;
  background-position: -432px -48px;
}
.icon-media-snapshot {
  width: 32px;
  height: 32px;
  background-position: -480px -48px;
}
.icon-media-stop {
  width: 32px;
  height: 32px;
  background-position: -528px -48px;
}
.icon-media-volume {
  width: 32px;
  height: 32px;
  background-position: -576px -48px;
}
.icon-uniE128 {
  width: 29px;
  height: 32px;
  background-position: -624px -48px;
}
.icon-uniE129 {
  width: 29px;
  height: 32px;
  background-position: -672px -48px;
}
.icon-uniE12A {
  width: 29px;
  height: 32px;
  background-position: -720px -48px;
}
.icon-media-repeat-updated {
  width: 40px;
  height: 32px;
  background-position: 0 -96px;
}
.icon-uniE130 {
  width: 24px;
  height: 32px;
  background-position: -48px -96px;
}
.icon-uniE131 {
  width: 24px;
  height: 32px;
  background-position: -96px -96px;
}
.icon-media-next1 {
  width: 29px;
  height: 32px;
  background-position: -144px -96px;
}
.icon-media-previous1 {
  width: 29px;
  height: 32px;
  background-position: -192px -96px;
}
.icon-a-54 {
  width: 24px;
  height: 32px;
  background-position: -240px -96px;
}
.icon-a-55 {
  width: 28px;
  height: 32px;
  background-position: -288px -96px;
}
.icon-a-56 {
  width: 49px;
  height: 32px;
  background-position: -336px -96px;
}
.icon-a-57 {
  width: 49px;
  height: 32px;
  background-position: -432px -96px;
}
.icon-a-58 {
  width: 28px;
  height: 32px;
  background-position: -528px -96px;
}
.icon-a-59 {
  width: 44px;
  height: 32px;
  background-position: -576px -96px;
}
.icon-a-60 {
  width: 40px;
  height: 32px;
  background-position: -672px -96px;
}
.icon-a-61 {
  width: 46px;
  height: 32px;
  background-position: 0 -144px;
}
.icon-a-62 {
  width: 36px;
  height: 32px;
  background-position: -96px -144px;
}
.icon-a-63 {
  width: 19px;
  height: 32px;
  background-position: -144px -144px;
}
.icon-uniE150 {
  width: 48px;
  height: 32px;
  background-position: -192px -144px;
}
.icon-uniE151 {
  width: 48px;
  height: 32px;
  background-position: -288px -144px;
}
.icon-uniE152 {
  width: 48px;
  height: 32px;
  background-position: -384px -144px;
}
.icon-uniE153 {
  width: 48px;
  height: 32px;
  background-position: -480px -144px;
}
.icon-uniE600 {
  width: 32px;
  height: 32px;
  background-position: -576px -144px;
}
.icon-uniE601 {
  width: 32px;
  height: 32px;
  background-position: -624px -144px;
}
.icon-uniE602 {
  width: 32px;
  height: 32px;
  background-position: -672px -144px;
}
.icon-uniE603 {
  width: 32px;
  height: 32px;
  background-position: -720px -144px;
}
.icon-uniE604 {
  width: 32px;
  height: 32px;
  background-position: 0 -192px;
}
.icon-uniE605 {
  width: 32px;
  height: 32px;
  background-position: -48px -192px;
}
.icon-uniE606 {
  width: 32px;
  height: 32px;
  background-position: -96px -192px;
}
.icon-uniE607 {
  width: 32px;
  height: 32px;
  background-position: -144px -192px;
}
.icon-uniE608 {
  width: 32px;
  height: 32px;
  background-position: -192px -192px;
}
.icon-uniE609 {
  width: 32px;
  height: 32px;
  background-position: -240px -192px;
}
.icon-uniE60A {
  width: 32px;
  height: 32px;
  background-position: -288px -192px;
}
.icon-uniE60B {
  width: 32px;
  height: 32px;
  background-position: -336px -192px;
}
.icon-uniE60C {
  width: 32px;
  height: 32px;
  background-position: -384px -192px;
}
.icon-uniE60D {
  width: 32px;
  height: 32px;
  background-position: -432px -192px;
}
.icon-uniE60E {
  width: 32px;
  height: 32px;
  background-position: -480px -192px;
}
.icon-uniE60F {
  width: 32px;
  height: 32px;
  background-position: -528px -192px;
}
.icon-uniE610 {
  width: 32px;
  height: 32px;
  background-position: -576px -192px;
}
.icon-uniE611 {
  width: 32px;
  height: 32px;
  background-position: -624px -192px;
}
.icon-uniE612 {
  width: 32px;
  height: 32px;
  background-position: -672px -192px;
}
.icon-uniE613 {
  width: 32px;
  height: 32px;
  background-position: -720px -192px;
}
.icon-uniE614 {
  width: 32px;
  height: 32px;
  background-position: 0 -240px;
}
.icon-uniE615 {
  width: 32px;
  height: 32px;
  background-position: -48px -240px;
}
.icon-uniE616 {
  width: 32px;
  height: 32px;
  background-position: -96px -240px;
}
.icon-uniE617 {
  width: 32px;
  height: 32px;
  background-position: -144px -240px;
}
.icon-uniE618 {
  width: 32px;
  height: 32px;
  background-position: -192px -240px;
}
.icon-uniE619 {
  width: 32px;
  height: 32px;
  background-position: -240px -240px;
}
.icon-uniE61A {
  width: 32px;
  height: 32px;
  background-position: -288px -240px;
}
.icon-uniE61B {
  width: 32px;
  height: 32px;
  background-position: -336px -240px;
}
.icon-uniE61C {
  width: 32px;
  height: 32px;
  background-position: -384px -240px;
}
.icon-uniE61D {
  width: 32px;
  height: 32px;
  background-position: -432px -240px;
}
.icon-uniE61E {
  width: 32px;
  height: 32px;
  background-position: -480px -240px;
}
.icon-uniE61F {
  width: 32px;
  height: 32px;
  background-position: -528px -240px;
}
.icon-uniE620 {
  width: 32px;
  height: 32px;
  background-position: -576px -240px;
}
.icon-uniE621 {
  width: 32px;
  height: 32px;
  background-position: -624px -240px;
}
.icon-uniE622 {
  width: 32px;
  height: 32px;
  background-position: -672px -240px;
}
.icon-uniE623 {
  width: 32px;
  height: 32px;
  background-position: -720px -240px;
}
.icon-uniE624 {
  width: 32px;
  height: 32px;
  background-position: 0 -288px;
}
.icon-uniE625 {
  width: 32px;
  height: 32px;
  background-position: -48px -288px;
}
.icon-uniE626 {
  width: 32px;
  height: 32px;
  background-position: -96px -288px;
}
.icon-uniE627 {
  width: 32px;
  height: 32px;
  background-position: -144px -288px;
}
.icon-uniE628 {
  width: 32px;
  height: 32px;
  background-position: -192px -288px;
}
.icon-uniE629 {
  width: 32px;
  height: 32px;
  background-position: -240px -288px;
}
.icon-uniE62A {
  width: 32px;
  height: 32px;
  background-position: -288px -288px;
}
.icon-uniE62B {
  width: 32px;
  height: 32px;
  background-position: -336px -288px;
}
.icon-uniE62C {
  width: 32px;
  height: 32px;
  background-position: -384px -288px;
}
.icon-uniE62D {
  width: 32px;
  height: 32px;
  background-position: -432px -288px;
}
.icon-uniE62E {
  width: 32px;
  height: 32px;
  background-position: -480px -288px;
}
.icon-uniE62F {
  width: 32px;
  height: 32px;
  background-position: -528px -288px;
}
.icon-uniE630 {
  width: 32px;
  height: 32px;
  background-position: -576px -288px;
}
.icon-uniE631 {
  width: 32px;
  height: 32px;
  background-position: -624px -288px;
}
.icon-uniE632 {
  width: 32px;
  height: 32px;
  background-position: -672px -288px;
}
.icon-uniE633 {
  width: 32px;
  height: 32px;
  background-position: -720px -288px;
}
.icon-uniE634 {
  width: 32px;
  height: 32px;
  background-position: 0 -336px;
}
.icon-uniE635 {
  width: 32px;
  height: 32px;
  background-position: -48px -336px;
}
.icon-uniE636 {
  width: 32px;
  height: 32px;
  background-position: -96px -336px;
}
.icon-uniE637 {
  width: 32px;
  height: 32px;
  background-position: -144px -336px;
}
.icon-uniE638 {
  width: 32px;
  height: 32px;
  background-position: -192px -336px;
}
.icon-uniE639 {
  width: 32px;
  height: 32px;
  background-position: -240px -336px;
}
.icon-uniE63A {
  width: 32px;
  height: 32px;
  background-position: -288px -336px;
}
.icon-uniE63B {
  width: 32px;
  height: 32px;
  background-position: -336px -336px;
}
.icon-uniE63C {
  width: 32px;
  height: 32px;
  background-position: -384px -336px;
}
.icon-uniE63D {
  width: 32px;
  height: 32px;
  background-position: -432px -336px;
}
.icon-uniE63E {
  width: 32px;
  height: 32px;
  background-position: -480px -336px;
}
.icon-uniE63F {
  width: 32px;
  height: 32px;
  background-position: -528px -336px;
}
.icon-uniE640 {
  width: 32px;
  height: 32px;
  background-position: -576px -336px;
}
.icon-uniE641 {
  width: 32px;
  height: 32px;
  background-position: -624px -336px;
}
.icon-uniE642 {
  width: 32px;
  height: 32px;
  background-position: -672px -336px;
}
.icon-uniE643 {
  width: 32px;
  height: 32px;
  background-position: -720px -336px;
}
.icon-uniE644 {
  width: 32px;
  height: 32px;
  background-position: 0 -384px;
}
.icon-uniE645 {
  width: 32px;
  height: 32px;
  background-position: -48px -384px;
}
.icon-uniE646 {
  width: 32px;
  height: 32px;
  background-position: -96px -384px;
}
.icon-uniE647 {
  width: 32px;
  height: 32px;
  background-position: -144px -384px;
}
.icon-uniE648 {
  width: 32px;
  height: 32px;
  background-position: -192px -384px;
}
.icon-uniE649 {
  width: 32px;
  height: 32px;
  background-position: -240px -384px;
}
.icon-uniE64A {
  width: 32px;
  height: 32px;
  background-position: -288px -384px;
}
.icon-uniE64B {
  width: 32px;
  height: 32px;
  background-position: -336px -384px;
}
.icon-uniE64C {
  width: 32px;
  height: 32px;
  background-position: -384px -384px;
}
.icon-uniE64D {
  width: 32px;
  height: 32px;
  background-position: -432px -384px;
}
.icon-uniE64E {
  width: 32px;
  height: 32px;
  background-position: -480px -384px;
}
.icon-uniE64F {
  width: 32px;
  height: 32px;
  background-position: -528px -384px;
}
.icon-uniE650 {
  width: 32px;
  height: 32px;
  background-position: -576px -384px;
}
.icon-uniE651 {
  width: 32px;
  height: 32px;
  background-position: -624px -384px;
}
.icon-uniE652 {
  width: 32px;
  height: 32px;
  background-position: -672px -384px;
}
.icon-uniE653 {
  width: 32px;
  height: 32px;
  background-position: -720px -384px;
}
.icon-uniE654 {
  width: 32px;
  height: 32px;
  background-position: 0 -432px;
}
.icon-uniE655 {
  width: 32px;
  height: 32px;
  background-position: -48px -432px;
}
.icon-uniE656 {
  width: 32px;
  height: 32px;
  background-position: -96px -432px;
}
.icon-uniE657 {
  width: 32px;
  height: 32px;
  background-position: -144px -432px;
}
.icon-uniE658 {
  width: 32px;
  height: 32px;
  background-position: -192px -432px;
}
.icon-uniE659 {
  width: 32px;
  height: 32px;
  background-position: -240px -432px;
}
.icon-uniE65A {
  width: 32px;
  height: 32px;
  background-position: -288px -432px;
}
.icon-uniE65B {
  width: 32px;
  height: 32px;
  background-position: -336px -432px;
}
.icon-uniE65C {
  width: 32px;
  height: 32px;
  background-position: -384px -432px;
}
.icon-uniE65D {
  width: 32px;
  height: 32px;
  background-position: -432px -432px;
}
.icon-uniE65E {
  width: 32px;
  height: 32px;
  background-position: -480px -432px;
}
.icon-uniE65F {
  width: 32px;
  height: 32px;
  background-position: -528px -432px;
}
.icon-uniE660 {
  width: 32px;
  height: 32px;
  background-position: -576px -432px;
}
.icon-uniE661 {
  width: 32px;
  height: 32px;
  background-position: -624px -432px;
}
.icon-uniE662 {
  width: 32px;
  height: 32px;
  background-position: -672px -432px;
}
.icon-uniE663 {
  width: 32px;
  height: 32px;
  background-position: -720px -432px;
}
.icon-uniE664 {
  width: 32px;
  height: 32px;
  background-position: 0 -480px;
}
.icon-uniE665 {
  width: 32px;
  height: 32px;
  background-position: -48px -480px;
}
.icon-uniE666 {
  width: 32px;
  height: 32px;
  background-position: -96px -480px;
}
.icon-uniE667 {
  width: 32px;
  height: 32px;
  background-position: -144px -480px;
}
.icon-uniE668 {
  width: 32px;
  height: 32px;
  background-position: -192px -480px;
}
.icon-uniE669 {
  width: 32px;
  height: 32px;
  background-position: -240px -480px;
}
.icon-uniE66A {
  width: 32px;
  height: 32px;
  background-position: -288px -480px;
}
.icon-uniE66B {
  width: 32px;
  height: 32px;
  background-position: -336px -480px;
}
.icon-uniE66C {
  width: 32px;
  height: 32px;
  background-position: -384px -480px;
}
.icon-uniE66D {
  width: 32px;
  height: 32px;
  background-position: -432px -480px;
}
.icon-uniE66E {
  width: 32px;
  height: 32px;
  background-position: -480px -480px;
}
.icon-uniE66F {
  width: 32px;
  height: 32px;
  background-position: -528px -480px;
}
.icon-uniE670 {
  width: 32px;
  height: 32px;
  background-position: -576px -480px;
}
.icon-uniE671 {
  width: 32px;
  height: 32px;
  background-position: -624px -480px;
}
.icon-uniE672 {
  width: 32px;
  height: 32px;
  background-position: -672px -480px;
}
.icon-uniE673 {
  width: 32px;
  height: 32px;
  background-position: -720px -480px;
}
.icon-uniE674 {
  width: 32px;
  height: 32px;
  background-position: 0 -528px;
}
.icon-uniE675 {
  width: 32px;
  height: 32px;
  background-position: -48px -528px;
}
.icon-uniE676 {
  width: 32px;
  height: 32px;
  background-position: -96px -528px;
}
.icon-uniE677 {
  width: 32px;
  height: 32px;
  background-position: -144px -528px;
}
.icon-uniE678 {
  width: 32px;
  height: 32px;
  background-position: -192px -528px;
}
.icon-uniE679 {
  width: 32px;
  height: 32px;
  background-position: -240px -528px;
}
.icon-uniE67A {
  width: 32px;
  height: 32px;
  background-position: -288px -528px;
}
.icon-uniE67B {
  width: 32px;
  height: 32px;
  background-position: -336px -528px;
}
.icon-uniE67C {
  width: 32px;
  height: 32px;
  background-position: -384px -528px;
}
.icon-uniE67D {
  width: 32px;
  height: 32px;
  background-position: -432px -528px;
}
.icon-uniE67E {
  width: 32px;
  height: 32px;
  background-position: -480px -528px;
}
.icon-uniE67F {
  width: 32px;
  height: 32px;
  background-position: -528px -528px;
}
.icon-uniE680 {
  width: 32px;
  height: 32px;
  background-position: -576px -528px;
}
.icon-uniE681 {
  width: 32px;
  height: 32px;
  background-position: -624px -528px;
}
.icon-uniE682 {
  width: 32px;
  height: 32px;
  background-position: -672px -528px;
}
.icon-uniE683 {
  width: 32px;
  height: 32px;
  background-position: -720px -528px;
}
.icon-uniE684 {
  width: 32px;
  height: 32px;
  background-position: 0 -576px;
}
.icon-uniE685 {
  width: 33px;
  height: 32px;
  background-position: -48px -576px;
}
.icon-uniE686 {
  width: 32px;
  height: 32px;
  background-position: -96px -576px;
}
.icon-uniE687 {
  width: 32px;
  height: 32px;
  background-position: -144px -576px;
}
.icon-uniE688 {
  width: 20px;
  height: 32px;
  background-position: -192px -576px;
}
.icon-uniE689 {
  width: 20px;
  height: 32px;
  background-position: -240px -576px;
}
.icon-uniE68A {
  width: 33px;
  height: 32px;
  background-position: -288px -576px;
}
.icon-uniE68B {
  width: 17px;
  height: 32px;
  background-position: -336px -576px;
}
.icon-uniE68C {
  width: 33px;
  height: 32px;
  background-position: -384px -576px;
}
.icon-uniE68D {
  width: 33px;
  height: 32px;
  background-position: -432px -576px;
}
.icon-uniE68E {
  width: 33px;
  height: 32px;
  background-position: -480px -576px;
}
.icon-uniE68F {
  width: 33px;
  height: 32px;
  background-position: -528px -576px;
}
.icon-uniE690 {
  width: 33px;
  height: 32px;
  background-position: -576px -576px;
}
.icon-uniE691 {
  width: 33px;
  height: 32px;
  background-position: -624px -576px;
}
.icon-uniE692 {
  width: 33px;
  height: 32px;
  background-position: -672px -576px;
}
.icon-uniE693 {
  width: 33px;
  height: 32px;
  background-position: 0 -624px;
}
.icon-uniE694 {
  width: 33px;
  height: 32px;
  background-position: -48px -624px;
}
.icon-uniE695 {
  width: 33px;
  height: 32px;
  background-position: -96px -624px;
}
.icon-uniE696 {
  width: 33px;
  height: 32px;
  background-position: -144px -624px;
}
.icon-uniE697 {
  width: 33px;
  height: 32px;
  background-position: -192px -624px;
}
.icon-uniE698 {
  width: 33px;
  height: 32px;
  background-position: -240px -624px;
}
.icon-uniE699 {
  width: 33px;
  height: 32px;
  background-position: -288px -624px;
}
.icon-uniE69A {
  width: 33px;
  height: 32px;
  background-position: -336px -624px;
}
.icon-uniE69B {
  width: 17px;
  height: 32px;
  background-position: -384px -624px;
}
.icon-uniE69C {
  width: 32px;
  height: 32px;
  background-position: -432px -624px;
}
.icon-uniE69D {
  width: 26px;
  height: 32px;
  background-position: -480px -624px;
}
.icon-uniE69E {
  width: 32px;
  height: 32px;
  background-position: -528px -624px;
}
.icon-uniE69F {
  width: 32px;
  height: 32px;
  background-position: -576px -624px;
}
.icon-uniE6A0 {
  width: 42px;
  height: 32px;
  background-position: -624px -624px;
}
.icon-uniE6A1 {
  width: 32px;
  height: 32px;
  background-position: 0 -672px;
}
.icon-uniE6A2 {
  width: 32px;
  height: 32px;
  background-position: -48px -672px;
}
.icon-uniE6A3 {
  width: 26px;
  height: 32px;
  background-position: -96px -672px;
}
.icon-uniE6A4 {
  width: 32px;
  height: 32px;
  background-position: -144px -672px;
}
.icon-uniE6A5 {
  width: 32px;
  height: 32px;
  background-position: -192px -672px;
}
.icon-uniE6A6 {
  width: 32px;
  height: 32px;
  background-position: -240px -672px;
}
.icon-uniE6A7 {
  width: 32px;
  height: 32px;
  background-position: -288px -672px;
}
.icon-uniE6A8 {
  width: 32px;
  height: 32px;
  background-position: -336px -672px;
}
.icon-uniE6A9 {
  width: 32px;
  height: 32px;
  background-position: -384px -672px;
}
.icon-uniE6AA {
  width: 32px;
  height: 32px;
  background-position: -432px -672px;
}
.icon-uniE6AB {
  width: 32px;
  height: 32px;
  background-position: -480px -672px;
}
.icon-uniE6AC {
  width: 32px;
  height: 32px;
  background-position: -528px -672px;
}
.icon-uniE6AD {
  width: 32px;
  height: 32px;
  background-position: -576px -672px;
}
.icon-uniE6AE {
  width: 32px;
  height: 32px;
  background-position: -624px -672px;
}
.icon-uniE6AF {
  width: 32px;
  height: 32px;
  background-position: -672px -672px;
}
.icon-uniE6B0 {
  width: 32px;
  height: 32px;
  background-position: -720px -672px;
}
.icon-uniE6B1 {
  width: 32px;
  height: 32px;
  background-position: 0 -720px;
}
.icon-uniE6B2 {
  width: 32px;
  height: 32px;
  background-position: -48px -720px;
}
.icon-uniE6B3 {
  width: 32px;
  height: 32px;
  background-position: -96px -720px;
}
.icon-uniE6B4 {
  width: 32px;
  height: 32px;
  background-position: -144px -720px;
}
.icon-uniE6B5 {
  width: 32px;
  height: 32px;
  background-position: -192px -720px;
}
.icon-uniE6B6 {
  width: 32px;
  height: 32px;
  background-position: -240px -720px;
}
.icon-uniE6B7 {
  width: 32px;
  height: 32px;
  background-position: -288px -720px;
}
.icon-uniE6B8 {
  width: 32px;
  height: 32px;
  background-position: -336px -720px;
}
.icon-uniE6B9 {
  width: 32px;
  height: 32px;
  background-position: -384px -720px;
}
.icon-uniE6BA {
  width: 32px;
  height: 32px;
  background-position: -432px -720px;
}
.icon-uniE6BB {
  width: 32px;
  height: 32px;
  background-position: -480px -720px;
}
.icon-uniE6BC {
  width: 32px;
  height: 32px;
  background-position: -528px -720px;
}
.icon-uniE6BD {
  width: 32px;
  height: 32px;
  background-position: -576px -720px;
}
.icon-uniE6BE {
  width: 32px;
  height: 32px;
  background-position: -624px -720px;
}
.icon-uniE6BF {
  width: 32px;
  height: 32px;
  background-position: -672px -720px;
}
.icon-uniE6C0 {
  width: 32px;
  height: 32px;
  background-position: -720px -720px;
}
.icon-uniE6C1 {
  width: 32px;
  height: 32px;
  background-position: 0 -768px;
}
.icon-uniE6C2 {
  width: 32px;
  height: 32px;
  background-position: -48px -768px;
}
.icon-uniE6C3 {
  width: 32px;
  height: 32px;
  background-position: -96px -768px;
}
.icon-uniE6C4 {
  width: 32px;
  height: 32px;
  background-position: -144px -768px;
}
.icon-uniE6C5 {
  width: 32px;
  height: 32px;
  background-position: -192px -768px;
}
.icon-uniE6C6 {
  width: 32px;
  height: 32px;
  background-position: -240px -768px;
}
.icon-uniE6C7 {
  width: 32px;
  height: 32px;
  background-position: -288px -768px;
}
.icon-uniE6C8 {
  width: 32px;
  height: 32px;
  background-position: -336px -768px;
}
.icon-uniE6C9 {
  width: 32px;
  height: 32px;
  background-position: -384px -768px;
}
.icon-uniE6CA {
  width: 32px;
  height: 32px;
  background-position: -432px -768px;
}
.icon-uniE6CB {
  width: 32px;
  height: 32px;
  background-position: -480px -768px;
}
.icon-uniE6CC {
  width: 32px;
  height: 32px;
  background-position: -528px -768px;
}
.icon-uniE6CD {
  width: 32px;
  height: 32px;
  background-position: -576px -768px;
}
.icon-uniE6CE {
  width: 32px;
  height: 32px;
  background-position: -624px -768px;
}
.icon-uniE6CF {
  width: 32px;
  height: 32px;
  background-position: -672px -768px;
}
.icon-uniE6D0 {
  width: 32px;
  height: 32px;
  background-position: -720px -768px;
}
.icon-uniE6D1 {
  width: 32px;
  height: 32px;
  background-position: 0 -816px;
}
.icon-uniE6D2 {
  width: 32px;
  height: 32px;
  background-position: -48px -816px;
}
.icon-uniE6D3 {
  width: 32px;
  height: 32px;
  background-position: -96px -816px;
}
.icon-uniE6D4 {
  width: 32px;
  height: 32px;
  background-position: -144px -816px;
}
.icon-uniE6D5 {
  width: 32px;
  height: 32px;
  background-position: -192px -816px;
}
.icon-uniE6D6 {
  width: 32px;
  height: 32px;
  background-position: -240px -816px;
}
.icon-uniE6D7 {
  width: 32px;
  height: 32px;
  background-position: -288px -816px;
}
.icon-uniE6D8 {
  width: 32px;
  height: 32px;
  background-position: -336px -816px;
}
.icon-uniE6D9 {
  width: 32px;
  height: 32px;
  background-position: -384px -816px;
}
.icon-uniE6DA {
  width: 32px;
  height: 32px;
  background-position: -432px -816px;
}
.icon-uniE6DB {
  width: 32px;
  height: 32px;
  background-position: -480px -816px;
}
.icon-uniE6DC {
  width: 32px;
  height: 32px;
  background-position: -528px -816px;
}
.icon-uniE6DD {
  width: 32px;
  height: 32px;
  background-position: -576px -816px;
}
.icon-uniE6DE {
  width: 32px;
  height: 32px;
  background-position: -624px -816px;
}
.icon-uniE6DF {
  width: 32px;
  height: 32px;
  background-position: -672px -816px;
}
.icon-uniE6E0 {
  width: 32px;
  height: 32px;
  background-position: -720px -816px;
}
.icon-uniE6E1 {
  width: 32px;
  height: 32px;
  background-position: 0 -864px;
}
.icon-uniE6E2 {
  width: 32px;
  height: 32px;
  background-position: -48px -864px;
}
.icon-uniE6E3 {
  width: 32px;
  height: 32px;
  background-position: -96px -864px;
}
.icon-uniE6E4 {
  width: 32px;
  height: 32px;
  background-position: -144px -864px;
}
.icon-uniE6E5 {
  width: 32px;
  height: 32px;
  background-position: -192px -864px;
}
.icon-uniE6E6 {
  width: 32px;
  height: 32px;
  background-position: -240px -864px;
}
.icon-uniE6E7 {
  width: 32px;
  height: 32px;
  background-position: -288px -864px;
}
.icon-uniE6E8 {
  width: 32px;
  height: 32px;
  background-position: -336px -864px;
}
.icon-uniE6E9 {
  width: 32px;
  height: 32px;
  background-position: -384px -864px;
}
.icon-uniE6EA {
  width: 32px;
  height: 32px;
  background-position: -432px -864px;
}
.icon-uniE6EB {
  width: 32px;
  height: 32px;
  background-position: -480px -864px;
}
.icon-uniE6EC {
  width: 32px;
  height: 32px;
  background-position: -528px -864px;
}
.icon-uniE6ED {
  width: 32px;
  height: 32px;
  background-position: -576px -864px;
}
.icon-uniE6EE {
  width: 32px;
  height: 32px;
  background-position: -624px -864px;
}
.icon-uniE6EF {
  width: 32px;
  height: 32px;
  background-position: -672px -864px;
}
.icon-uniE6F0 {
  width: 32px;
  height: 32px;
  background-position: -720px -864px;
}
.icon-uniE6F1 {
  width: 32px;
  height: 32px;
  background-position: 0 -912px;
}
.icon-uniE6F2 {
  width: 32px;
  height: 32px;
  background-position: -48px -912px;
}
.icon-uniE6F3 {
  width: 32px;
  height: 32px;
  background-position: -96px -912px;
}
.icon-uniE6F4 {
  width: 32px;
  height: 32px;
  background-position: -144px -912px;
}
.icon-uniE6F5 {
  width: 32px;
  height: 32px;
  background-position: -192px -912px;
}
.icon-uniE6F6 {
  width: 32px;
  height: 32px;
  background-position: -240px -912px;
}
.icon-uniE6F7 {
  width: 32px;
  height: 32px;
  background-position: -288px -912px;
}
.icon-uniE6F8 {
  width: 32px;
  height: 32px;
  background-position: -336px -912px;
}
.icon-uniE6F9 {
  width: 32px;
  height: 32px;
  background-position: -384px -912px;
}
.icon-uniE6FA {
  width: 11px;
  height: 32px;
  background-position: -432px -912px;
}
.icon-uniE6FB {
  width: 11px;
  height: 32px;
  background-position: -480px -912px;
}
.icon-uniE6FC {
  width: 32px;
  height: 32px;
  background-position: -528px -912px;
}
.icon-uniE6FD {
  width: 32px;
  height: 32px;
  background-position: -576px -912px;
}
.icon-uniE6FE {
  width: 32px;
  height: 32px;
  background-position: -624px -912px;
}
.icon-uniE6FF {
  width: 34px;
  height: 32px;
  background-position: -672px -912px;
}
.icon-uniE700 {
  width: 32px;
  height: 32px;
  background-position: 0 -960px;
}
.icon-uniE701 {
  width: 32px;
  height: 32px;
  background-position: -48px -960px;
}
.icon-uniE702 {
  width: 32px;
  height: 32px;
  background-position: -96px -960px;
}
.icon-uniE703 {
  width: 32px;
  height: 32px;
  background-position: -144px -960px;
}
.icon-uniE704 {
  width: 30px;
  height: 32px;
  background-position: -192px -960px;
}
.icon-uniE705 {
  width: 32px;
  height: 32px;
  background-position: -240px -960px;
}
.icon-uniE706 {
  width: 32px;
  height: 32px;
  background-position: -288px -960px;
}
.icon-uniE707 {
  width: 32px;
  height: 32px;
  background-position: -336px -960px;
}
.icon-uniE708 {
  width: 32px;
  height: 32px;
  background-position: -384px -960px;
}
.icon-uniE709 {
  width: 32px;
  height: 32px;
  background-position: -432px -960px;
}
.icon-uniE70A {
  width: 32px;
  height: 32px;
  background-position: -480px -960px;
}
.icon-uniE70B {
  width: 32px;
  height: 32px;
  background-position: -528px -960px;
}
.icon-uniE70C {
  width: 32px;
  height: 32px;
  background-position: -576px -960px;
}
.icon-uniE70D {
  width: 32px;
  height: 32px;
  background-position: -624px -960px;
}
.icon-uniE70E {
  width: 32px;
  height: 32px;
  background-position: -672px -960px;
}
.icon-uniE70F {
  width: 32px;
  height: 32px;
  background-position: -720px -960px;
}
.icon-uniE710 {
  width: 32px;
  height: 32px;
  background-position: 0 -1008px;
}
.icon-uniE711 {
  width: 32px;
  height: 32px;
  background-position: -48px -1008px;
}
.icon-uniE712 {
  width: 32px;
  height: 32px;
  background-position: -96px -1008px;
}
.icon-uniE713 {
  width: 27px;
  height: 32px;
  background-position: -144px -1008px;
}
.icon-uniE714 {
  width: 27px;
  height: 32px;
  background-position: -192px -1008px;
}
.icon-uniE715 {
  width: 32px;
  height: 32px;
  background-position: -240px -1008px;
}
.icon-uniE716 {
  width: 32px;
  height: 32px;
  background-position: -288px -1008px;
}
.icon-uniE717 {
  width: 32px;
  height: 32px;
  background-position: -336px -1008px;
}
.icon-uniE718 {
  width: 32px;
  height: 32px;
  background-position: -384px -1008px;
}
.icon-uniE719 {
  width: 32px;
  height: 32px;
  background-position: -432px -1008px;
}
.icon-uniE71A {
  width: 32px;
  height: 32px;
  background-position: -480px -1008px;
}
.icon-uniE71B {
  width: 32px;
  height: 32px;
  background-position: -528px -1008px;
}
.icon-uniE71C {
  width: 32px;
  height: 32px;
  background-position: -576px -1008px;
}
.icon-uniE71D {
  width: 32px;
  height: 32px;
  background-position: -624px -1008px;
}
.icon-uniE71E {
  width: 32px;
  height: 32px;
  background-position: -672px -1008px;
}
.icon-uniE71F {
  width: 32px;
  height: 32px;
  background-position: -720px -1008px;
}
.icon-uniE720 {
  width: 32px;
  height: 32px;
  background-position: 0 -1056px;
}
.icon-uniE721 {
  width: 32px;
  height: 32px;
  background-position: -48px -1056px;
}
.icon-uniE722 {
  width: 32px;
  height: 32px;
  background-position: -96px -1056px;
}
.icon-uniE723 {
  width: 32px;
  height: 32px;
  background-position: -144px -1056px;
}
.icon-uniE724 {
  width: 32px;
  height: 32px;
  background-position: -192px -1056px;
}
.icon-uniE725 {
  width: 32px;
  height: 32px;
  background-position: -240px -1056px;
}
.icon-uniE726 {
  width: 32px;
  height: 32px;
  background-position: -288px -1056px;
}
.icon-uniE727 {
  width: 32px;
  height: 32px;
  background-position: -336px -1056px;
}
.icon-uniE728 {
  width: 32px;
  height: 32px;
  background-position: -384px -1056px;
}
.icon-uniE729 {
  width: 29px;
  height: 32px;
  background-position: -432px -1056px;
}
.icon-uniE72A {
  width: 30px;
  height: 32px;
  background-position: -480px -1056px;
}
.icon-uniE72B {
  width: 32px;
  height: 32px;
  background-position: -528px -1056px;
}
.icon-uniE72C {
  width: 32px;
  height: 32px;
  background-position: -576px -1056px;
}
.icon-uniE72D {
  width: 36px;
  height: 32px;
  background-position: -624px -1056px;
}
.icon-uniE72E {
  width: 32px;
  height: 32px;
  background-position: -672px -1056px;
}
.icon-uniE72F {
  width: 32px;
  height: 32px;
  background-position: -720px -1056px;
}
.icon-uniE730 {
  width: 32px;
  height: 32px;
  background-position: 0 -1104px;
}
.icon-uniE731 {
  width: 32px;
  height: 32px;
  background-position: -48px -1104px;
}
.icon-uniE732 {
  width: 32px;
  height: 32px;
  background-position: -96px -1104px;
}
.icon-uniE733 {
  width: 32px;
  height: 32px;
  background-position: -144px -1104px;
}
.icon-uniE734 {
  width: 32px;
  height: 32px;
  background-position: -192px -1104px;
}
.icon-uniE735 {
  width: 32px;
  height: 32px;
  background-position: -240px -1104px;
}
.icon-uniE736 {
  width: 32px;
  height: 32px;
  background-position: -288px -1104px;
}
.icon-uniE737 {
  width: 32px;
  height: 32px;
  background-position: -336px -1104px;
}
.icon-uniE738 {
  width: 32px;
  height: 32px;
  background-position: -384px -1104px;
}
.icon-uniE739 {
  width: 32px;
  height: 32px;
  background-position: -432px -1104px;
}
.icon-uniE73A {
  width: 32px;
  height: 32px;
  background-position: -480px -1104px;
}
.icon-uniE73B {
  width: 35px;
  height: 32px;
  background-position: -528px -1104px;
}
.icon-uniE73C {
  width: 46px;
  height: 32px;
  background-position: -576px -1104px;
}
.icon-uniE73D {
  width: 45px;
  height: 32px;
  background-position: -672px -1104px;
}
.icon-uniE73E {
  width: 32px;
  height: 32px;
  background-position: 0 -1152px;
}
.icon-uniE73F {
  width: 31px;
  height: 32px;
  background-position: -48px -1152px;
}
.icon-uniE740 {
  width: 31px;
  height: 32px;
  background-position: -96px -1152px;
}
.icon-uniE741 {
  width: 32px;
  height: 32px;
  background-position: -144px -1152px;
}
.icon-uniE742 {
  width: 32px;
  height: 32px;
  background-position: -192px -1152px;
}
.icon-uniE743 {
  width: 32px;
  height: 32px;
  background-position: -240px -1152px;
}
.icon-uniE744 {
  width: 32px;
  height: 32px;
  background-position: -288px -1152px;
}
.icon-uniE745 {
  width: 32px;
  height: 32px;
  background-position: -336px -1152px;
}
.icon-uniE746 {
  width: 32px;
  height: 32px;
  background-position: -384px -1152px;
}
.icon-uniE747 {
  width: 32px;
  height: 32px;
  background-position: -432px -1152px;
}
.icon-uniE748 {
  width: 32px;
  height: 32px;
  background-position: -480px -1152px;
}
.icon-uniE749 {
  width: 32px;
  height: 32px;
  background-position: -528px -1152px;
}
.icon-uniE74A {
  width: 32px;
  height: 32px;
  background-position: -576px -1152px;
}
.icon-uniE74B {
  width: 32px;
  height: 32px;
  background-position: -624px -1152px;
}
.icon-uniE74C {
  width: 32px;
  height: 32px;
  background-position: -672px -1152px;
}
.icon-uniE74D {
  width: 32px;
  height: 32px;
  background-position: -720px -1152px;
}
.icon-uniE74E {
  width: 32px;
  height: 32px;
  background-position: 0 -1200px;
}
.icon-uniE74F {
  width: 32px;
  height: 32px;
  background-position: -48px -1200px;
}
.icon-uniE750 {
  width: 32px;
  height: 32px;
  background-position: -96px -1200px;
}
.icon-uniE751 {
  width: 55px;
  height: 32px;
  background-position: -144px -1200px;
}
.icon-uniE752 {
  width: 32px;
  height: 32px;
  background-position: -240px -1200px;
}
.icon-uniE753 {
  width: 32px;
  height: 32px;
  background-position: -288px -1200px;
}
.icon-uniE754 {
  width: 32px;
  height: 32px;
  background-position: -336px -1200px;
}
.icon-uniE755 {
  width: 32px;
  height: 32px;
  background-position: -384px -1200px;
}
.icon-uniE756 {
  width: 32px;
  height: 32px;
  background-position: -432px -1200px;
}
.icon-uniE757 {
  width: 32px;
  height: 32px;
  background-position: -480px -1200px;
}
.icon-uniE758 {
  width: 32px;
  height: 32px;
  background-position: -528px -1200px;
}
.icon-uniE759 {
  width: 32px;
  height: 32px;
  background-position: -576px -1200px;
}
.icon-uniE75A {
  width: 32px;
  height: 32px;
  background-position: -624px -1200px;
}
.icon-uniE75B {
  width: 32px;
  height: 32px;
  background-position: -672px -1200px;
}
.icon-uniE75C {
  width: 32px;
  height: 32px;
  background-position: -720px -1200px;
}
.icon-uniE75D {
  width: 36px;
  height: 32px;
  background-position: 0 -1248px;
}
.icon-uniE75E {
  width: 32px;
  height: 32px;
  background-position: -48px -1248px;
}
.icon-uniE75F {
  width: 32px;
  height: 32px;
  background-position: -96px -1248px;
}
.icon-uniE760 {
  width: 32px;
  height: 32px;
  background-position: -144px -1248px;
}
.icon-uniE761 {
  width: 32px;
  height: 32px;
  background-position: -192px -1248px;
}
.icon-uniE762 {
  width: 32px;
  height: 32px;
  background-position: -240px -1248px;
}
.icon-uniE763 {
  width: 32px;
  height: 32px;
  background-position: -288px -1248px;
}
.icon-uniE764 {
  width: 32px;
  height: 32px;
  background-position: -336px -1248px;
}
.icon-uniE765 {
  width: 32px;
  height: 32px;
  background-position: -384px -1248px;
}
.icon-uniE766 {
  width: 32px;
  height: 32px;
  background-position: -432px -1248px;
}
.icon-uniE767 {
  width: 32px;
  height: 32px;
  background-position: -480px -1248px;
}
.icon-uniE768 {
  width: 32px;
  height: 32px;
  background-position: -528px -1248px;
}
.icon-uniE769 {
  width: 32px;
  height: 32px;
  background-position: -576px -1248px;
}
.icon-uniE76A {
  width: 32px;
  height: 32px;
  background-position: -624px -1248px;
}
.icon-uniE76B {
  width: 32px;
  height: 32px;
  background-position: -672px -1248px;
}
.icon-uniE76C {
  width: 32px;
  height: 32px;
  background-position: -720px -1248px;
}
.icon-uniE76D {
  width: 32px;
  height: 32px;
  background-position: 0 -1296px;
}
.icon-uniE76E {
  width: 32px;
  height: 32px;
  background-position: -48px -1296px;
}
.icon-uniE76F {
  width: 37px;
  height: 32px;
  background-position: -96px -1296px;
}
.icon-uniE770 {
  width: 37px;
  height: 32px;
  background-position: -144px -1296px;
}
.icon-uniE771 {
  width: 37px;
  height: 32px;
  background-position: -192px -1296px;
}
.icon-uniE772 {
  width: 32px;
  height: 32px;
  background-position: -240px -1296px;
}
.icon-uniE773 {
  width: 32px;
  height: 32px;
  background-position: -288px -1296px;
}
.icon-uniE774 {
  width: 32px;
  height: 32px;
  background-position: -336px -1296px;
}
.icon-uniE775 {
  width: 32px;
  height: 32px;
  background-position: -384px -1296px;
}
.icon-uniE776 {
  width: 32px;
  height: 32px;
  background-position: -432px -1296px;
}
.icon-uniE777 {
  width: 32px;
  height: 32px;
  background-position: -480px -1296px;
}
.icon-uniE778 {
  width: 32px;
  height: 32px;
  background-position: -528px -1296px;
}
.icon-uniE779 {
  width: 32px;
  height: 32px;
  background-position: -576px -1296px;
}
.icon-uniE77A {
  width: 32px;
  height: 32px;
  background-position: -624px -1296px;
}
.icon-uniE77B {
  width: 144px;
  height: 32px;
  background-position: 0 -1344px;
}
.icon-uniE77C {
  width: 32px;
  height: 32px;
  background-position: -192px -1344px;
}
.icon-uniE77D {
  width: 32px;
  height: 32px;
  background-position: -240px -1344px;
}
.icon-uniE77E {
  width: 36px;
  height: 32px;
  background-position: -288px -1344px;
}
.icon-copy {
  width: 32px;
  height: 32px;
  background-position: -336px -1344px;
}
.icon-js-playground {
  width: 32px;
  height: 32px;
  background-position: -384px -1344px;
}
.icon-agenda {
  width: 32px;
  height: 32px;
  background-position: -432px -1344px;
}
.icon-allday {
  width: 32px;
  height: 32px;
  background-position: -480px -1344px;
}
.icon-edit {
  width: 32px;
  height: 32px;
  background-position: -528px -1344px;
}
.icon-repeat {
  width: 32px;
  height: 32px;
  background-position: -576px -1344px;
}
.icon-uniE785 {
  width: 40px;
  height: 32px;
  background-position: -624px -1344px;
}
.icon-uniE786 {
  width: 32px;
  height: 32px;
  background-position: -672px -1344px;
}
.icon-uniE787 {
  width: 32px;
  height: 32px;
  background-position: -720px -1344px;
}
.icon-uniE788 {
  width: 32px;
  height: 32px;
  background-position: 0 -1392px;
}
.icon-uniE789 {
  width: 32px;
  height: 32px;
  background-position: -48px -1392px;
}
.icon-uniE78A {
  width: 32px;
  height: 32px;
  background-position: -96px -1392px;
}
.icon-uniE78B {
  width: 32px;
  height: 32px;
  background-position: -144px -1392px;
}
.icon-uniE78C {
  width: 32px;
  height: 32px;
  background-position: -192px -1392px;
}
.icon-uniE78D {
  width: 32px;
  height: 32px;
  background-position: -240px -1392px;
}
.icon-uniE78E {
  width: 32px;
  height: 32px;
  background-position: -288px -1392px;
}
.icon-uniE78F {
  width: 32px;
  height: 32px;
  background-position: -336px -1392px;
}
.icon-uniE790 {
  width: 32px;
  height: 32px;
  background-position: -384px -1392px;
}
.icon-uniE791 {
  width: 32px;
  height: 32px;
  background-position: -432px -1392px;
}
.icon-uniE792 {
  width: 32px;
  height: 32px;
  background-position: -480px -1392px;
}
.icon-uniE793 {
  width: 32px;
  height: 32px;
  background-position: -528px -1392px;
}
.icon-uniE794 {
  width: 32px;
  height: 32px;
  background-position: -576px -1392px;
}
.icon-uniE795 {
  width: 32px;
  height: 32px;
  background-position: -624px -1392px;
}
.icon-uniE796 {
  width: 32px;
  height: 32px;
  background-position: -672px -1392px;
}
.icon-uniE797 {
  width: 32px;
  height: 32px;
  background-position: -720px -1392px;
}
.icon-uniE798 {
  width: 32px;
  height: 32px;
  background-position: 0 -1440px;
}
.icon-uniE799 {
  width: 32px;
  height: 32px;
  background-position: -48px -1440px;
}
.icon-uniE79A {
  width: 32px;
  height: 32px;
  background-position: -96px -1440px;
}
.icon-uniE79B {
  width: 32px;
  height: 32px;
  background-position: -144px -1440px;
}
.icon-uniE79C {
  width: 32px;
  height: 32px;
  background-position: -192px -1440px;
}
.icon-uniE79D {
  width: 32px;
  height: 32px;
  background-position: -240px -1440px;
}
.icon-uniE79E {
  width: 32px;
  height: 32px;
  background-position: -288px -1440px;
}
.icon-uniE79F {
  width: 32px;
  height: 32px;
  background-position: -336px -1440px;
}
.icon-uniE7A0 {
  width: 32px;
  height: 32px;
  background-position: -384px -1440px;
}
.icon-uniE7A1 {
  width: 32px;
  height: 32px;
  background-position: -432px -1440px;
}
.icon-uniE7A2 {
  width: 32px;
  height: 32px;
  background-position: -480px -1440px;
}
.icon-uniE7A3 {
  width: 32px;
  height: 32px;
  background-position: -528px -1440px;
}
.icon-uniE7A4 {
  width: 32px;
  height: 32px;
  background-position: -576px -1440px;
}
.icon-uniE7A5 {
  width: 32px;
  height: 32px;
  background-position: -624px -1440px;
}
.icon-uniE7A6 {
  width: 32px;
  height: 32px;
  background-position: -672px -1440px;
}
.icon-uniE7A7 {
  width: 32px;
  height: 32px;
  background-position: -720px -1440px;
}
.icon-uniE7A8 {
  width: 32px;
  height: 32px;
  background-position: 0 -1488px;
}
.icon-uniE7A9 {
  width: 32px;
  height: 32px;
  background-position: -48px -1488px;
}
.icon-uniE7AA {
  width: 32px;
  height: 32px;
  background-position: -96px -1488px;
}
.icon-uniE7AB {
  width: 32px;
  height: 32px;
  background-position: -144px -1488px;
}
.icon-uniE7AC {
  width: 32px;
  height: 32px;
  background-position: -192px -1488px;
}
.icon-uniE7AD {
  width: 32px;
  height: 32px;
  background-position: -240px -1488px;
}
.icon-uniE7AE {
  width: 32px;
  height: 32px;
  background-position: -288px -1488px;
}
.icon-uniE7AF {
  width: 32px;
  height: 32px;
  background-position: -336px -1488px;
}
.icon-uniE7B0 {
  width: 32px;
  height: 32px;
  background-position: -384px -1488px;
}
.icon-uniE7B1 {
  width: 32px;
  height: 32px;
  background-position: -432px -1488px;
}
.icon-uniE7B2 {
  width: 32px;
  height: 32px;
  background-position: -480px -1488px;
}
.icon-uniE7B3 {
  width: 32px;
  height: 32px;
  background-position: -528px -1488px;
}
.icon-uniE7B4 {
  width: 32px;
  height: 32px;
  background-position: -576px -1488px;
}
.icon-uniE7B5 {
  width: 32px;
  height: 32px;
  background-position: -624px -1488px;
}
.icon-uniE7B6 {
  width: 32px;
  height: 32px;
  background-position: -672px -1488px;
}
.icon-Recurrence {
  width: 43px;
  height: 32px;
  background-position: 0 -1536px;
}
.icon-RecurrenceEdit {
  width: 43px;
  height: 32px;
  background-position: -96px -1536px;
}
.icon-uniE7B9 {
  width: 32px;
  height: 32px;
  background-position: -192px -1536px;
}
.icon-uniE7BA {
  width: 32px;
  height: 32px;
  background-position: -240px -1536px;
}
.icon-uniE7BB {
  width: 32px;
  height: 32px;
  background-position: -288px -1536px;
}
.icon-uniE7BC {
  width: 32px;
  height: 32px;
  background-position: -336px -1536px;
}
.icon-uniE7BD {
  width: 32px;
  height: 32px;
  background-position: -384px -1536px;
}
.icon-uniE7BE {
  width: 32px;
  height: 32px;
  background-position: -432px -1536px;
}
.icon-uniE781 {
  width: 32px;
  height: 32px;
  background-position: -480px -1536px;
}
.icon-uniE782 {
  width: 32px;
  height: 32px;
  background-position: -528px -1536px;
}
.icon-uniE783 {
  width: 32px;
  height: 32px;
  background-position: -576px -1536px;
}
.icon-uniE784 {
  width: 32px;
  height: 32px;
  background-position: -624px -1536px;
}
.icon-uniE7852 {
  width: 32px;
  height: 32px;
  background-position: -672px -1536px;
}
.icon-uniE7862 {
  width: 32px;
  height: 32px;
  background-position: -720px -1536px;
}
.icon-uniE7872 {
  width: 32px;
  height: 32px;
  background-position: 0 -1584px;
}
.icon-uniE7882 {
  width: 32px;
  height: 32px;
  background-position: -48px -1584px;
}
.icon-uniE7892 {
  width: 32px;
  height: 32px;
  background-position: -96px -1584px;
}
.icon-uniE78A2 {
  width: 32px;
  height: 32px;
  background-position: -144px -1584px;
}
.icon-uniE78B2 {
  width: 32px;
  height: 32px;
  background-position: -192px -1584px;
}
.icon-uniE78C2 {
  width: 32px;
  height: 32px;
  background-position: -240px -1584px;
}
.icon-uniE78D2 {
  width: 32px;
  height: 32px;
  background-position: -288px -1584px;
}
.icon-down-arrow-icon {
  width: 32px;
  height: 32px;
  background-position: -336px -1584px;
}
.icon-dropdown {
  width: 40px;
  height: 32px;
  background-position: -384px -1584px;
}
.icon-qat-icon {
  width: 61px;
  height: 32px;
  background-position: -432px -1584px;
}
.icon-tick {
  width: 42px;
  height: 32px;
  background-position: -528px -1584px;
}
.icon-Pdf_Print {
  width: 32px;
  height: 32px;
  background-position: -624px -1584px;
}
.icon-Pdf_First {
  width: 32px;
  height: 32px;
  background-position: -672px -1584px;
}
.icon-PDf_Previous {
  width: 32px;
  height: 32px;
  background-position: -720px -1584px;
}
.icon-Pdf_Next {
  width: 32px;
  height: 32px;
  background-position: 0 -1632px;
}
.icon-Pdf_Last {
  width: 32px;
  height: 32px;
  background-position: -48px -1632px;
}
.icon-Pdf_ZoomIn {
  width: 32px;
  height: 32px;
  background-position: -96px -1632px;
}
.icon-Pdf_ZoomOut {
  width: 32px;
  height: 32px;
  background-position: -144px -1632px;
}
.icon-Pdf_FitPage {
  width: 32px;
  height: 32px;
  background-position: -192px -1632px;
}
.icon-Pdf_FitWidth {
  width: 32px;
  height: 32px;
  background-position: -240px -1632px;
}
.icon-X16ICONS_UnFreeze {
  width: 32px;
  height: 32px;
  background-position: -288px -1632px;
}
.icon-X16ICONS_FREEZE_Freeze {
  width: 32px;
  height: 32px;
  background-position: -336px -1632px;
}
.icon-X16ICONS_FreezeColumnsBefore {
  width: 32px;
  height: 32px;
  background-position: -384px -1632px;
}
.icon-Chart_Bubble {
  width: 32px;
  height: 32px;
  background-position: -432px -1632px;
}
.icon-Chart_Doughnut {
  width: 32px;
  height: 32px;
  background-position: -480px -1632px;
}
.icon-Chart_radar {
  width: 32px;
  height: 32px;
  background-position: -528px -1632px;
}
.icon-Chart_Scatter {
  width: 32px;
  height: 32px;
  background-position: -576px -1632px;
}
.icon-Chart-07 {
  width: 32px;
  height: 32px;
  background-position: -624px -1632px;
}
.icon-uniE7E1 {
  width: 32px;
  height: 32px;
  background-position: -672px -1632px;
}
.icon-uniE7E2 {
  width: 32px;
  height: 32px;
  background-position: -720px -1632px;
}
.icon-uniE7E3 {
  width: 32px;
  height: 32px;
  background-position: 0 -1680px;
}
.icon-uniE7E4 {
  width: 32px;
  height: 32px;
  background-position: -48px -1680px;
}
.icon-uniE7E5 {
  width: 32px;
  height: 32px;
  background-position: -96px -1680px;
}
.icon-uniE7E6 {
  width: 32px;
  height: 32px;
  background-position: -144px -1680px;
}
.icon-uniE7E7 {
  width: 32px;
  height: 32px;
  background-position: -192px -1680px;
}
.icon-uniE7E8 {
  width: 32px;
  height: 32px;
  background-position: -240px -1680px;
}
.icon-uniE7E9 {
  width: 32px;
  height: 32px;
  background-position: -288px -1680px;
}
.icon-uniE7EA {
  width: 32px;
  height: 32px;
  background-position: -336px -1680px;
}
.icon-uniE7EB {
  width: 32px;
  height: 32px;
  background-position: -384px -1680px;
}
.icon-uniE7EC {
  width: 32px;
  height: 32px;
  background-position: -432px -1680px;
}
.icon-uniE7ED {
  width: 32px;
  height: 32px;
  background-position: -480px -1680px;
}
.icon-uniE7EE {
  width: 32px;
  height: 32px;
  background-position: -528px -1680px;
}
.icon-uniE7EF {
  width: 32px;
  height: 32px;
  background-position: -576px -1680px;
}
.icon-uniE7F0 {
  width: 32px;
  height: 32px;
  background-position: -624px -1680px;
}
.icon-uniE7F1 {
  width: 32px;
  height: 32px;
  background-position: -672px -1680px;
}
.icon-uniE7F2 {
  width: 32px;
  height: 32px;
  background-position: -720px -1680px;
}
.icon-uniE7F3 {
  width: 32px;
  height: 32px;
  background-position: 0 -1728px;
}
.icon-uniE7F4 {
  width: 32px;
  height: 32px;
  background-position: -48px -1728px;
}
.icon-uniE7F5 {
  width: 32px;
  height: 32px;
  background-position: -96px -1728px;
}
.icon-uniE7F6 {
  width: 32px;
  height: 32px;
  background-position: -144px -1728px;
}
.icon-uniE7f7 {
  width: 32px;
  height: 32px;
  background-position: -192px -1728px;
}
.icon-uniE7f8 {
  width: 32px;
  height: 32px;
  background-position: -240px -1728px;
}
.icon-uniE7f9 {
  width: 32px;
  height: 32px;
  background-position: -288px -1728px;
}
.icon-uniE7fa {
  width: 32px;
  height: 32px;
  background-position: -336px -1728px;
}
.icon-uniE7fb {
  width: 32px;
  height: 32px;
  background-position: -384px -1728px;
}
.icon-uniE7fc {
  width: 32px;
  height: 32px;
  background-position: -432px -1728px;
}
.icon-uniE7fd {
  width: 32px;
  height: 32px;
  background-position: -480px -1728px;
}
.icon-uniE7fe {
  width: 32px;
  height: 32px;
  background-position: -528px -1728px;
}
.icon-uniE7ff {
  width: 32px;
  height: 32px;
  background-position: -576px -1728px;
}
.icon-uniE800 {
  width: 32px;
  height: 32px;
  background-position: -624px -1728px;
}
.icon-uniE801 {
  width: 32px;
  height: 32px;
  background-position: -672px -1728px;
}
.icon-uniE802 {
  width: 32px;
  height: 32px;
  background-position: -720px -1728px;
}
.icon-uniE803 {
  width: 32px;
  height: 32px;
  background-position: 0 -1776px;
}
.icon-uniE804 {
  width: 32px;
  height: 32px;
  background-position: -48px -1776px;
}
.icon-uniE805 {
  width: 32px;
  height: 32px;
  background-position: -96px -1776px;
}
.icon-uniE806 {
  width: 32px;
  height: 32px;
  background-position: -144px -1776px;
}
.icon-uniE807 {
  width: 32px;
  height: 32px;
  background-position: -192px -1776px;
}
.icon-uniE808 {
  width: 32px;
  height: 32px;
  background-position: -240px -1776px;
}
.icon-unie809 {
  width: 32px;
  height: 32px;
  background-position: -288px -1776px;
}
.icon-uniE80a {
  width: 32px;
  height: 32px;
  background-position: -336px -1776px;
}
.icon-uniE80b {
  width: 32px;
  height: 32px;
  background-position: -384px -1776px;
}
.icon-uniE80c {
  width: 32px;
  height: 32px;
  background-position: -432px -1776px;
}
.icon-uniE80d {
  width: 32px;
  height: 32px;
  background-position: -480px -1776px;
}
.icon-uniE80e {
  width: 32px;
  height: 32px;
  background-position: -528px -1776px;
}
.icon-print-icon-02 {
  width: 32px;
  height: 32px;
  background-position: -576px -1776px;
}
.icon-uniE810 {
  width: 32px;
  height: 32px;
  background-position: -624px -1776px;
}
.icon-a-051 {
  width: 59px;
  height: 32px;
  background-position: -672px -1776px;
}
.icon-a-061 {
  width: 30px;
  height: 32px;
  background-position: 0 -1824px;
}
.icon-filter-031 {
  width: 36px;
  height: 32px;
  background-position: -48px -1824px;
}
.icon-filter-042 {
  width: 36px;
  height: 32px;
  background-position: -96px -1824px;
}
.icon-backarrow-08 {
  width: 18px;
  height: 32px;
  background-position: -144px -1824px;
}
.icon-BurgerMenu_iOS {
  width: 32px;
  height: 32px;
  background-position: -192px -1824px;
}
.icon-Icon-03 {
  width: 32px;
  height: 32px;
  background-position: -240px -1824px;
}
.icon-Icon-04 {
  width: 32px;
  height: 32px;
  background-position: -288px -1824px;
}
.icon-Icon-05 {
  width: 32px;
  height: 32px;
  background-position: -336px -1824px;
}
.icon-Icon-06 {
  width: 32px;
  height: 32px;
  background-position: -384px -1824px;
}
.icon-uniE81b {
  width: 32px;
  height: 32px;
  background-position: -432px -1824px;
}
.icon-uniE81c {
  width: 32px;
  height: 32px;
  background-position: -480px -1824px;
}
.icon-Adopt__Down-arrow {
  width: 32px;
  height: 32px;
  background-position: -528px -1824px;
}
.icon-Adopt__up-arrow {
  width: 32px;
  height: 32px;
  background-position: -576px -1824px;
}
.icon-download-pdf {
  width: 32px;
  height: 32px;
  background-position: -624px -1824px;
}
.icon-arrow--down1 {
  width: 64px;
  height: 32px;
  background-position: -672px -1824px;
}
.icon-arrow--up1 {
  width: 64px;
  height: 32px;
  background-position: 0 -1872px;
}
.icon-CriticalTask_Taskbar_Icon_Solid {
  width: 32px;
  height: 32px;
  background-position: -96px -1872px;
}
.icon-sort-by-icon-01 {
  width: 32px;
  height: 32px;
  background-position: -144px -1872px;
}
.icon-Icon_descending {
  width: 32px;
  height: 32px;
  background-position: -192px -1872px;
}
.icon-Icon_ascending {
  width: 32px;
  height: 32px;
  background-position: -240px -1872px;
}
.icon-previous-page-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -288px -1872px;
}
.icon-next-page-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -336px -1872px;
}
.icon-zoomout-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -384px -1872px;
}
.icon-zoomin-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -432px -1872px;
}
.icon-fitwidth-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -480px -1872px;
}
.icon-fitpage-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -528px -1872px;
}
.icon-print-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -576px -1872px;
}
.icon-download-pdf-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -624px -1872px;
}
.icon-search-icon-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -672px -1872px;
}
.icon-search-prev-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -720px -1872px;
}
.icon-search-next-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: 0 -1920px;
}
.icon-uniE831 {
  width: 36px;
  height: 32px;
  background-position: -48px -1920px;
}
.icon-uniE832 {
  width: 36px;
  height: 32px;
  background-position: -96px -1920px;
}
.icon-uniE833 {
  width: 32px;
  height: 32px;
  background-position: -144px -1920px;
}
.icon-uniE834 {
  width: 32px;
  height: 32px;
  background-position: -192px -1920px;
}
.icon-uniE835 {
  width: 32px;
  height: 32px;
  background-position: -240px -1920px;
}
.icon-uniE836 {
  width: 32px;
  height: 32px;
  background-position: -288px -1920px;
}
.icon-search-close-pdfviewer {
  width: 32px;
  height: 32px;
  background-position: -336px -1920px;
}
.icon-waterfall {
  width: 32px;
  height: 32px;
  background-position: -384px -1920px;
}
.icon-Database {
  width: 32px;
  height: 32px;
  background-position: -432px -1920px;
}
.icon-Remove-DB-report {
  width: 32px;
  height: 32px;
  background-position: -480px -1920px;
}
.icon-Rename-DB-report {
  width: 32px;
  height: 32px;
  background-position: -528px -1920px;
}
.icon-Save-As {
  width: 32px;
  height: 32px;
  background-position: -576px -1920px;
}
.icon-back-icon {
  width: 32px;
  height: 32px;
  background-position: -624px -1920px;
}
.icon-uniE83e {
  width: 32px;
  height: 32px;
  background-position: -672px -1920px;
}
.icon-uniE83f {
  width: 32px;
  height: 32px;
  background-position: -720px -1920px;
}
.icon-uniE840 {
  width: 32px;
  height: 32px;
  background-position: 0 -1968px;
}
.icon-uniE841 {
  width: 32px;
  height: 32px;
  background-position: -48px -1968px;
}
.icon-ColumnFreeze {
  width: 32px;
  height: 32px;
  background-position: -96px -1968px;
}
.icon-AdvancedFiltering {
  width: 32px;
  height: 32px;
  background-position: -144px -1968px;
}
.icon-Cell-context {
  width: 32px;
  height: 32px;
  background-position: -192px -1968px;
}
.icon-ExcelExporting {
  width: 32px;
  height: 32px;
  background-position: -240px -1968px;
}
.icon-PDFExporting {
  width: 32px;
  height: 32px;
  background-position: -288px -1968px;
}
.icon-CSVExporting {
  width: 32px;
  height: 32px;
  background-position: -336px -1968px;
}
.icon-FrozenHeaders {
  width: 32px;
  height: 32px;
  background-position: -384px -1968px;
}
.icon-Summary-types {
  width: 32px;
  height: 32px;
  background-position: -432px -1968px;
}
.icon-ColumnheaderHyperlink {
  width: 32px;
  height: 32px;
  background-position: -480px -1968px;
}
.icon-CalculatedFields {
  width: 32px;
  height: 32px;
  background-position: -528px -1968px;
}
.icon-Hyperlink {
  width: 32px;
  height: 32px;
  background-position: -576px -1968px;
}
.icon-RTL {
  width: 32px;
  height: 32px;
  background-position: -624px -1968px;
}
.icon-WordExporting {
  width: 32px;
  height: 32px;
  background-position: -672px -1968px;
}
.icon-Exporting {
  width: 32px;
  height: 32px;
  background-position: -720px -1968px;
}
.icon-ConditionalFormatting {
  width: 32px;
  height: 32px;
  background-position: 0 -2016px;
}
.icon-ColumnResizing {
  width: 32px;
  height: 32px;
  background-position: -48px -2016px;
}
.icon-SummaryCustomization {
  width: 32px;
  height: 32px;
  background-position: -96px -2016px;
}
.icon-RowFreeze {
  width: 32px;
  height: 32px;
  background-position: -144px -2016px;
}
.icon-Paging {
  width: 32px;
  height: 32px;
  background-position: -192px -2016px;
}
.icon-CellEditing {
  width: 32px;
  height: 32px;
  background-position: -240px -2016px;
}
.icon-CellSelection {
  width: 32px;
  height: 32px;
  background-position: -288px -2016px;
}
.icon-NumberFormats {
  width: 32px;
  height: 32px;
  background-position: -336px -2016px;
}
.icon-Tooltip {
  width: 32px;
  height: 32px;
  background-position: -384px -2016px;
}
.icon-ExcelLikeLayout {
  width: 32px;
  height: 32px;
  background-position: -432px -2016px;
}
.icon-ValueCellHyperlink {
  width: 32px;
  height: 32px;
  background-position: -480px -2016px;
}
.icon-SummaryCellHyperlink {
  width: 32px;
  height: 32px;
  background-position: -528px -2016px;
}
.icon-RowHeaderHyperlink {
  width: 32px;
  height: 32px;
  background-position: -576px -2016px;
}
.icon-CollapseByDefault {
  width: 32px;
  height: 32px;
  background-position: -624px -2016px;
}
.icon-15 {
  width: 32px;
  height: 32px;
  background-position: -672px -2016px;
}
.icon-16 {
  width: 32px;
  height: 32px;
  background-position: -720px -2016px;
}
.icon-17 {
  width: 32px;
  height: 32px;
  background-position: 0 -2064px;
}
.icon-18 {
  width: 32px;
  height: 32px;
  background-position: -48px -2064px;
}
.icon-19 {
  width: 32px;
  height: 32px;
  background-position: -96px -2064px;
}
.icon-20 {
  width: 32px;
  height: 32px;
  background-position: -144px -2064px;
}
.icon-uniE864 {
  width: 32px;
  height: 32px;
  background-position: -192px -2064px;
}
.icon-uniE865 {
  width: 32px;
  height: 32px;
  background-position: -240px -2064px;
}
.icon-22 {
  width: 32px;
  height: 32px;
  background-position: -288px -2064px;
}
.icon-23 {
  width: 32px;
  height: 32px;
  background-position: -336px -2064px;
}
.icon-24 {
  width: 32px;
  height: 32px;
  background-position: -384px -2064px;
}
.icon-25 {
  width: 32px;
  height: 32px;
  background-position: -432px -2064px;
}
.icon-D-disable-icon {
  width: 32px;
  height: 32px;
  background-position: -480px -2064px;
}
.icon-Text-Selection {
  width: 32px;
  height: 32px;
  background-position: -528px -2064px;
}
.icon-Text-Strike {
  width: 32px;
  height: 32px;
  background-position: -576px -2064px;
}
.icon-Text-Underline {
  width: 32px;
  height: 32px;
  background-position: -624px -2064px;
}
.icon-PDF-viewer-JS_Arrow {
  width: 48px;
  height: 32px;
  background-position: -672px -2064px;
}
.icon-Calculated-member_-Toolbar-Black-Color-Icon {
  width: 32px;
  height: 32px;
  background-position: 0 -2112px;
}
.icon-Calculated-member_-Tree-View-Black-Color-Icon {
  width: 32px;
  height: 32px;
  background-position: -48px -2112px;
}
.icon-Disable-Cross-Hair {
  width: 32px;
  height: 32px;
  background-position: -96px -2112px;
}
.icon-Enable-Cross-Hair {
  width: 32px;
  height: 32px;
  background-position: -144px -2112px;
}
.icon-Hide {
  width: 32px;
  height: 32px;
  background-position: -192px -2112px;
}
.icon-Icon_Collapse {
  width: 32px;
  height: 32px;
  background-position: -240px -2112px;
}
.icon-Icon_Drill-Through {
  width: 32px;
  height: 32px;
  background-position: -288px -2112px;
}
.icon-Icon_Expand {
  width: 32px;
  height: 32px;
  background-position: -336px -2112px;
}
.icon-Interaction {
  width: 32px;
  height: 32px;
  background-position: -384px -2112px;
}
.icon-Layout {
  width: 32px;
  height: 32px;
  background-position: -432px -2112px;
}
.icon-Legend {
  width: 32px;
  height: 32px;
  background-position: -480px -2112px;
}
.icon-Marker {
  width: 32px;
  height: 32px;
  background-position: -528px -2112px;
}
.icon-Multiple-Rows {
  width: 32px;
  height: 32px;
  background-position: -576px -2112px;
}
.icon-No-Summary-Layout {
  width: 32px;
  height: 32px;
  background-position: -624px -2112px;
}
.icon-Normal-Layout {
  width: 32px;
  height: 32px;
  background-position: -672px -2112px;
}
.icon-Rotate-45 {
  width: 32px;
  height: 32px;
  background-position: -720px -2112px;
}
.icon-Rotate-90 {
  width: 32px;
  height: 32px;
  background-position: 0 -2160px;
}
.icon-Smart-Labels {
  width: 32px;
  height: 32px;
  background-position: -48px -2160px;
}
.icon-Top-Summary-Layout {
  width: 32px;
  height: 32px;
  background-position: -96px -2160px;
}
.icon-Track-Ball {
  width: 32px;
  height: 32px;
  background-position: -144px -2160px;
}
.icon-Trim {
  width: 32px;
  height: 32px;
  background-position: -192px -2160px;
}
.icon-Wrap-By-Word {
  width: 32px;
  height: 32px;
  background-position: -240px -2160px;
}
.icon-Wrap {
  width: 32px;
  height: 32px;
  background-position: -288px -2160px;
}
.icon-Zoom-In {
  width: 32px;
  height: 32px;
  background-position: -336px -2160px;
}
.icon-Zoom-Out {
  width: 32px;
  height: 32px;
  background-position: -384px -2160px;
}
.icon-uniE8d1 {
  width: 32px;
  height: 32px;
  background-position: -432px -2160px;
}
.icon-uniE8d2 {
  width: 32px;
  height: 32px;
  background-position: -480px -2160px;
}
.icon-Base-line_Hide {
  width: 32px;
  height: 32px;
  background-position: -528px -2160px;
}
.icon-Base-line_Show {
  width: 32px;
  height: 32px;
  background-position: -576px -2160px;
}
.icon-RTL_Dark {
  width: 32px;
  height: 32px;
  background-position: -624px -2160px;
}
.icon-Signature-icon-03 {
  width: 30px;
  height: 32px;
  background-position: -672px -2160px;
}
.icon-selection-icon-03 {
  width: 32px;
  height: 32px;
  background-position: -720px -2160px;
}
.icon-selection-icon-05 {
  width: 32px;
  height: 32px;
  background-position: 0 -2208px;
}
.icon-b-79 {
  width: 32px;
  height: 32px;
  background-position: -48px -2208px;
}
.icon-b-80 {
  width: 32px;
  height: 32px;
  background-position: -96px -2208px;
}
.icon-b-81 {
  width: 32px;
  height: 32px;
  background-position: -144px -2208px;
}
.icon-b-82 {
  width: 32px;
  height: 32px;
  background-position: -192px -2208px;
}
.icon-b-83 {
  width: 32px;
  height: 32px;
  background-position: -240px -2208px;
}
.icon-b-84 {
  width: 32px;
  height: 32px;
  background-position: -288px -2208px;
}
.icon-b-85 {
  width: 32px;
  height: 32px;
  background-position: -336px -2208px;
}
.icon-b-86 {
  width: 29px;
  height: 32px;
  background-position: -384px -2208px;
}
.icon-b-87 {
  width: 32px;
  height: 32px;
  background-position: -432px -2208px;
}
.icon-b-88 {
  width: 32px;
  height: 32px;
  background-position: -480px -2208px;
}
.icon-b-89 {
  width: 32px;
  height: 32px;
  background-position: -528px -2208px;
}
.icon-uniE912 {
  width: 32px;
  height: 32px;
  background-position: -576px -2208px;
}
.icon-uniE913 {
  width: 32px;
  height: 32px;
  background-position: -624px -2208px;
}
.icon-a-70 {
  width: 32px;
  height: 32px;
  background-position: -672px -2208px;
}
.icon-a-71 {
  width: 32px;
  height: 32px;
  background-position: -720px -2208px;
}
.icon-v-92 {
  width: 32px;
  height: 32px;
  background-position: 0 -2256px;
}
.icon-v-93 {
  width: 32px;
  height: 32px;
  background-position: -48px -2256px;
}
.icon-xAxis-title {
  width: 32px;
  height: 32px;
  background-position: -96px -2256px;
}
.icon-yAxis-title {
  width: 32px;
  height: 32px;
  background-position: -144px -2256px;
}


	
</style>  
<table>
<tr>
<td>
<div class="spriteimage icon-media-small-screen"></div>
 <div class="txt">Unicode:"e100"</div>
</td>
<td>
<div class="spriteimage icon-media-backward"></div>
<div class="txt">Unicode:"e101"</div>
</td>
<td>
<div class="spriteimage icon-media-download"></div>
<div class="txt">Unicode:"e102"</div>
</td>
<td>
<div class="spriteimage icon-media-forward"></div>
<div class="txt">Unicode:"e103"</div>
</td>
<td>
<div class="spriteimage icon-media-full-screen"></div>
<div class="txt">Unicode:"e104"</div>
</td>
</tr>

 <tr>
<td>
 <div class="spriteimage icon-media-mute"></div>
<div class="txt">Unicode:"e105"</div>
</td>
<td>
<div class="spriteimage icon-media-next"></div>
<div class="txt">Unicode:"e106"</div>
 </td>
 <td>
<div class="spriteimage icon-media-next-item"></div>
<div class="txt">Unicode:"e107"</div>
</td>
<td>
<div class="spriteimage icon-media-pause"></div>
<div class="txt">Unicode:"e108"</div>
</td>
<td>
<div class="spriteimage icon-uniE109"></div>
<div class="txt">Unicode:"e109"</div>
</td>
</tr>

<tr>
 <td>
<div class="spriteimage icon-uniE10A"></div>
<div class="txt">Unicode:"e10a"</div>
</td>
<td>
<div class="spriteimage icon-uniE10B"></div>
<div class="txt">Unicode:"e10b"</div>
</td>
<td>
<div class="spriteimage icon-media-play"></div>
<div class="txt">Unicode:"e110"</div>
</td>
<td>
<div class="spriteimage icon-uniE111"></div>
<div class="txt">Unicode:"e111"</div>
</td>
<td>
<div class="spriteimage icon-uniE112"></div>
<div class="txt">Unicode:"e112"</div>
</td>	
</tr>

<tr>
<td>
<div class="spriteimage icon-media-Playlist"></div>
<div class="txt">Unicode:"e113"</div>
</td>
<td>
<div class="spriteimage icon-uniE115"></div>
<div class="txt">Unicode:"e115"</div>
</td>
<td>
<div class="spriteimage icon-uniE116"></div>
<div class="txt">Unicode:"e116"</div>
</td>
<td>
<div class="spriteimage icon-uniE117"></div>
<div class="txt">Unicode:"e117"</div>
</td>
<td>
<div class="spriteimage icon-uniE118"></div>
<div class="txt">Unicode:"e118"</div>
</td>
</tr> 

<tr>
 <td>
<div class="spriteimage icon-media-previous"></div>
<div class="txt">Unicode:"e119"</div>
</td>
 <td>
<div class="spriteimage icon-media-previous-item"></div>
<div class="txt">Unicode:"e120"</div>
</td>
 <td>
<div class="spriteimage icon-media-repeat"></div>
<div class="txt">Unicode:"e121"</div>
</td>
 <td>
<div class="spriteimage icon-media-select"></div>
<div class="txt">Unicode:"e122"</div>
</td>
 <td>
<div class="spriteimage icon-media-settings"></div>
<div class="txt">Unicode:"e123"</div>
</td>
</tr>

<tr>
 <td>
<div class="spriteimage icon-media-shuffle"></div>
<div class="txt">Unicode:"e124"</div>
</td>
 <td>
<div class="spriteimage icon-media-snapshot"></div>
<div class="txt">Unicode:"e125"</div>
</td>
 <td>
<div class="spriteimage icon-media-stop"></div>
<div class="txt">Unicode:"e126"</div>
</td>
 <td>
<div class="spriteimage icon-media-volume"></div>
<div class="txt">Unicode:"e127"</div>
</td>
 <td>
<div class="spriteimage icon-uniE128"></div>
<div class="txt">Unicode:"e128"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE129"></div>
<div class="txt">Unicode:"e129"</div>
</td>
<td>
<div class="spriteimage icon-uniE12A"></div>
<div class="txt">Unicode:"e12a"</div>
</td>
<td>
<div class="spriteimage icon-media-repeat-updated"></div>
<div class="txt">Unicode:"e12b"</div>
</td>
<td>
<div class="spriteimage icon-uniE130"></div>
<div class="txt">Unicode:"e130"</div>
</td>
<td>
<div class="spriteimage icon-uniE131"></div>
<div class="txt">Unicode:"e131"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-media-next1"></div>
<div class="txt">Unicode:"e132"</div>
</td>
<td>
<div class="spriteimage icon-media-previous1"></div>
<div class="txt">Unicode:"e134"</div>
</td>
<td>
<div class="spriteimage icon-a-54"></div>
<div class="txt">Unicode:"e135"</div>
</td>
<td>
<div class="spriteimage icon-a-55"></div>
<div class="txt">Unicode:"e136"</div>
</td>
<td>
<div class="spriteimage icon-a-56"></div>
<div class="txt">Unicode:"e137"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-a-57"></div>
<div class="txt">Unicode:"e138"</div>
</td>
<td>
<div class="spriteimage icon-a-58"></div>
<div class="txt">Unicode:"e139"</div>
</td>
<td>
<div class="spriteimage icon-a-59"></div>
<div class="txt">Unicode:"e140"</div>
</td>
<td>
<div class="spriteimage icon-a-60"></div>
<div class="txt">Unicode:"e141"</div>
</td>
<td>
<div class="spriteimage icon-a-61"></div>
<div class="txt">Unicode:"e142"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-a-62"></div>
<div class="txt">Unicode:"e143"</div>
</td>
<td>
<div class="spriteimage icon-a-63"></div>
<div class="txt">Unicode:"e144"</div>
</td>
<td>
<div class="spriteimage icon-uniE150"></div>
<div class="txt">Unicode:"e150"</div>
</td>
<td>
<div class="spriteimage icon-uniE151"></div>
<div class="txt">Unicode:"e151"</div>
</td>
<td>
<div class="spriteimage icon-uniE152"></div>
<div class="txt">Unicode:"e152"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE153"></div>
<div class="txt">Unicode:"e153"</div>
</td>
<td>
<div class="spriteimage icon-uniE600"></div>
<div class="txt">Unicode:"e600"</div>
</td>
<td>
<div class="spriteimage icon-uniE601"></div>
<div class="txt">Unicode:"e601"</div>
</td>
<td>
<div class="spriteimage icon-uniE602"></div>
<div class="txt">Unicode:"e602"</div>
</td>
<td>
<div class="spriteimage icon-uniE603"></div>
<div class="txt">Unicode:"e603"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE604"></div>
<div class="txt">Unicode:"e604"</div>
</td>
<td>
<div class="spriteimage icon-uniE605"></div>
<div class="txt">Unicode:"e605"</div>
</td>
<td>
<div class="spriteimage icon-uniE606"></div>
<div class="txt">Unicode:"e606"</div>
</td>
<td>
<div class="spriteimage icon-uniE607"></div>
<div class="txt">Unicode:"e607"</div>
</td>
<td>
<div class="spriteimage icon-uniE608"></div>
<div class="txt">Unicode:"e608"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE609"></div>
<div class="txt">Unicode:"e609"</div>
</td>
<td>
<div class="spriteimage icon-uniE60A"></div>
<div class="txt">Unicode:"e60a"</div>
</td>
<td>
<div class="spriteimage icon-uniE60B"></div>
<div class="txt">Unicode:"e60b"</div>
</td>
<td>
<div class="spriteimage icon-uniE60C"></div>
<div class="txt">Unicode:"e60c"</div>
</td>
<td>
<div class="spriteimage icon-uniE60D"></div>
<div class="txt">Unicode:"e60d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE60E"></div>
<div class="txt">Unicode:"e60e"</div>
</td>
<td>
<div class="spriteimage icon-uniE60F"></div>
<div class="txt">Unicode:"e60f"</div>
</td>
<td>
<div class="spriteimage icon-uniE610"></div>
<div class="txt">Unicode:"e610"</div>
</td>
<td>
<div class="spriteimage icon-uniE611"></div>
<div class="txt">Unicode:"e611"</div>
</td>
<td>
<div class="spriteimage icon-uniE612"></div>
<div class="txt">Unicode:"e612"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE613"></div>
<div class="txt">Unicode:"e613"</div>
</td>
<td>
<div class="spriteimage icon-uniE614"></div>
<div class="txt">Unicode:"e614"</div>
</td>
<td>
<div class="spriteimage icon-uniE615"></div>
<div class="txt">Unicode:"e615"</div>
</td>
<td>
<div class="spriteimage icon-uniE616"></div>
<div class="txt">Unicode:"e616"</div>
</td>
<td>
<div class="spriteimage icon-uniE617"></div>
<div class="txt">Unicode:"e617"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE618"></div>
<div class="txt">Unicode:"e618"</div>
</td>
<td>
<div class="spriteimage icon-uniE619"></div>
<div class="txt">Unicode:"e619"</div>
</td>
<td>
<div class="spriteimage icon-uniE61A"></div>
<div class="txt">Unicode:"e61a"</div>
</td>
<td>
<div class="spriteimage icon-uniE61B"></div>
<div class="txt">Unicode:"e61b"</div>
</td>
<td>
<div class="spriteimage icon-uniE61C"></div>
<div class="txt">Unicode:"e61c"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE61D"></div>
<div class="txt">Unicode:"e61d"</div>
</td>
<td>
<div class="spriteimage icon-uniE61E"></div>
<div class="txt">Unicode:"e61e"</div>
</td>
<td>
<div class="spriteimage icon-uniE61F"></div>
<div class="txt">Unicode:"e61f"</div>
</td>
<td>
<div class="spriteimage icon-uniE620"></div>
<div class="txt">Unicode:"e620"</div>
</td>
<td>
<div class="spriteimage icon-uniE621"></div>
<div class="txt">Unicode:"e621"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE622"></div>
<div class="txt">Unicode:"e622"</div>
</td>
<td>
<div class="spriteimage icon-uniE623"></div>
<div class="txt">Unicode:"e623"</div>
</td>
<td>
<div class="spriteimage icon-uniE624"></div>
<div class="txt">Unicode:"e624"</div>
</td>
<td>
<div class="spriteimage icon-uniE625"></div>
<div class="txt">Unicode:"e625"</div>
</td>
<td>
<div class="spriteimage icon-uniE626"></div>
<div class="txt">Unicode:"e626"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE627"></div>
<div class="txt">Unicode:"e627"</div>
</td>
<td>
<div class="spriteimage icon-uniE628"></div>
<div class="txt">Unicode:"e628"</div>
</td>
<td>
<div class="spriteimage icon-uniE629"></div>
<div class="txt">Unicode:"e629"</div>
</td>
<td>
<div class="spriteimage icon-uniE62A"></div>
<div class="txt">Unicode:"e62a"</div>
</td>
<td>
<div class="spriteimage icon-uniE62B"></div>
<div class="txt">Unicode:"e62b"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE62C"></div>
<div class="txt">Unicode:"e62c"</div>
</td>
<td>
<div class="spriteimage icon-uniE62D"></div>
<div class="txt">Unicode:"e62d"</div>
</td>
<td>
<div class="spriteimage icon-uniE62E"></div>
<div class="txt">Unicode:"e62e"</div>
</td>
<td>
<div class="spriteimage icon-uniE62F"></div>
<div class="txt">Unicode:"e62f"</div>
</td>
<td>
<div class="spriteimage icon-uniE630"></div>
<div class="txt">Unicode:"e630"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE631"></div>
<div class="txt">Unicode:"e631"</div>
</td>
<td>
<div class="spriteimage icon-uniE632"></div>
<div class="txt">Unicode:"e632"</div>
</td>
<td>
<div class="spriteimage icon-uniE633"></div>
<div class="txt">Unicode:"e633"</div>
</td>
<td>
<div class="spriteimage icon-uniE634"></div>
<div class="txt">Unicode:"e634"</div>
</td>
<td>
<div class="spriteimage icon-uniE635"></div>
<div class="txt">Unicode:"e635"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE636"></div>
<div class="txt">Unicode:"e636"</div>
</td>
<td>
<div class="spriteimage icon-uniE637"></div>
<div class="txt">Unicode:"e637"</div>
</td>
<td>
<div class="spriteimage icon-uniE638"></div>
<div class="txt">Unicode:"e638"</div>
</td>
<td>
<div class="spriteimage icon-uniE639"></div>
<div class="txt">Unicode:"e639"</div>
</td>
<td>
<div class="spriteimage icon-uniE63A"></div>
<div class="txt">Unicode:"e63a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE63B"></div>
<div class="txt">Unicode:"e63b"</div>
</td>
<td>
<div class="spriteimage icon-uniE63C"></div>
<div class="txt">Unicode:"e63c"</div>
</td>
<td>
<div class="spriteimage icon-uniE63D"></div>
<div class="txt">Unicode:"e63d"</div>
</td>
<td>
<div class="spriteimage icon-uniE63E"></div>
<div class="txt">Unicode:"e63e"</div>
</td>
<td>
<div class="spriteimage icon-uniE63F"></div>
<div class="txt">Unicode:"e63f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE640"></div>
<div class="txt">Unicode:"e640"</div>
</td>
<td>
<div class="spriteimage icon-uniE641"></div>
<div class="txt">Unicode:"e641"</div>
</td>
<td>
<div class="spriteimage icon-uniE642"></div>
<div class="txt">Unicode:"e642"</div>
</td>
<td>
<div class="spriteimage icon-uniE643"></div>
<div class="txt">Unicode:"e643"</div>
</td>
<td>
<div class="spriteimage icon-uniE644"></div>
<div class="txt">Unicode:"e644"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE645"></div>
<div class="txt">Unicode:"e645"</div>
</td>
<td>
<div class="spriteimage icon-uniE646"></div>
<div class="txt">Unicode:"e646"</div>
</td>
<td>
<div class="spriteimage icon-uniE647"></div>
<div class="txt">Unicode:"e647"</div>
</td>
<td>
<div class="spriteimage icon-uniE648"></div>
<div class="txt">Unicode:"e648"</div>
</td>
<td>
<div class="spriteimage icon-uniE649"></div>
<div class="txt">Unicode:"e649"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE64A"></div>
<div class="txt">Unicode:"e64a"</div>
</td>
<td>
<div class="spriteimage icon-uniE64B"></div>
<div class="txt">Unicode:"e64b"</div>
</td>
<td>
<div class="spriteimage icon-uniE64C"></div>
<div class="txt">Unicode:"e64c"</div>
</td>
<td>
<div class="spriteimage icon-uniE64D"></div>
<div class="txt">Unicode:"e64d"</div>
</td>
<td>
<div class="spriteimage icon-uniE64E"></div>
<div class="txt">Unicode:"e64e"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE64F"></div>
<div class="txt">Unicode:"e64f"</div>
</td>
<td>
<div class="spriteimage icon-uniE650"></div>
<div class="txt">Unicode:"e650"</div>
</td>
<td>
<div class="spriteimage icon-uniE651"></div>
<div class="txt">Unicode:"e651"</div>
</td>
<td>
<div class="spriteimage icon-uniE652"></div>
<div class="txt">Unicode:"e652"</div>
</td>
<td>
<div class="spriteimage icon-uniE653"></div>
<div class="txt">Unicode:"e653"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE654"></div>
<div class="txt">Unicode:"e654"</div>
</td>
<td>
<div class="spriteimage icon-uniE655"></div>
<div class="txt">Unicode:"e655"</div>
</td>
<td>
<div class="spriteimage icon-uniE656"></div>
<div class="txt">Unicode:"e656"</div>
</td>
<td>
<div class="spriteimage icon-uniE657"></div>
<div class="txt">Unicode:"e657"</div>
</td>
<td>
<div class="spriteimage icon-uniE658"></div>
<div class="txt">Unicode:"e658"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE659"></div>
<div class="txt">Unicode:"e659"</div>
</td>
<td>
<div class="spriteimage icon-uniE65A"></div>
<div class="txt">Unicode:"e65a"</div>
</td>
<td>
<div class="spriteimage icon-uniE65B"></div>
<div class="txt">Unicode:"e65b"</div>
</td>
<td>
<div class="spriteimage icon-uniE65C"></div>
<div class="txt">Unicode:"e65c"</div>
</td>
<td>
<div class="spriteimage icon-uniE65D"></div>
<div class="txt">Unicode:"e65d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE65E"></div>
<div class="txt">Unicode:"e65e"</div>
</td>
<td>
<div class="spriteimage icon-uniE65F"></div>
<div class="txt">Unicode:"e65f"</div>
</td>
<td>
<div class="spriteimage icon-uniE660"></div>
<div class="txt">Unicode:"e660"</div>
</td>
<td>
<div class="spriteimage icon-uniE661"></div>
<div class="txt">Unicode:"e661"</div>
</td>
<td>
<div class="spriteimage icon-uniE662"></div>
<div class="txt">Unicode:"e662"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE663"></div>
<div class="txt">Unicode:"e663"</div>
</td>
<td>
<div class="spriteimage icon-uniE664"></div>
<div class="txt">Unicode:"e664"</div>
</td>
<td>
<div class="spriteimage icon-uniE665"></div>
<div class="txt">Unicode:"e665"</div>
</td>
<td>
<div class="spriteimage icon-uniE666"></div>
<div class="txt">Unicode:"e666"</div>
</td>
<td>
<div class="spriteimage icon-uniE667"></div>
<div class="txt">Unicode:"e667"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE668"></div>
<div class="txt">Unicode:"e668"</div>
</td>
<td>
<div class="spriteimage icon-uniE669"></div>
<div class="txt">Unicode:"e669"</div>
</td>
<td>
<div class="spriteimage icon-uniE66A"></div>
<div class="txt">Unicode:"e66a"</div>
</td>
<td>
<div class="spriteimage icon-uniE66B"></div>
<div class="txt">Unicode:"e66b"</div>
</td>
<td>
<div class="spriteimage icon-yAxis-title"></div>
<div class="txt">Unicode:"e918"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE66C"></div>
<div class="txt">Unicode:"e66c"</div>
</td>
<td>
<div class="spriteimage icon-uniE66D"></div>
<div class="txt">Unicode:"e66d"</div>
</td>
<td>
<div class="spriteimage icon-uniE66E"></div>
<div class="txt">Unicode:"e66e"</div>
</td>
<td>
<div class="spriteimage icon-uniE66F"></div>
<div class="txt">Unicode:"e66f"</div>
</td>
<td>
<div class="spriteimage icon-uniE670"></div>
<div class="txt">Unicode:"e670"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE671"></div>
<div class="txt">Unicode:"e671"</div>
</td>
<td>
<div class="spriteimage icon-uniE672"></div>
<div class="txt">Unicode:"e672"</div>
</td>
<td>
<div class="spriteimage icon-uniE673"></div>
<div class="txt">Unicode:"e673"</div>
</td>
<td>
<div class="spriteimage icon-uniE674"></div>
<div class="txt">Unicode:"e674"</div>
</td>
<td>
<div class="spriteimage icon-uniE675"></div>
<div class="txt">Unicode:"e675"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE676"></div>
<div class="txt">Unicode:"e676"</div>
</td>
<td>
<div class="spriteimage icon-uniE677"></div>
<div class="txt">Unicode:"e677"</div>
</td>
<td>
<div class="spriteimage icon-uniE678"></div>
<div class="txt">Unicode:"e678"</div>
</td>
<td>
<div class="spriteimage icon-uniE679"></div>
<div class="txt">Unicode:"e679"</div>
</td>
<td>
<div class="spriteimage icon-uniE67A"></div>
<div class="txt">Unicode:"e67a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE67B"></div>
<div class="txt">Unicode:"e67b"</div>
</td>
<td>
<div class="spriteimage icon-uniE67C"></div>
<div class="txt">Unicode:"e67c"</div>
</td>
<td>
<div class="spriteimage icon-uniE67D"></div>
<div class="txt">Unicode:"e67d"</div>
</td>
<td>
<div class="spriteimage icon-uniE67E"></div>
<div class="txt">Unicode:"e67e"</div>
</td>
<td>
<div class="spriteimage icon-uniE67F"></div>
<div class="txt">Unicode:"e67f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE680"></div>
<div class="txt">Unicode:"e680"</div>
</td>
<td>
<div class="spriteimage icon-uniE681"></div>
<div class="txt">Unicode:"e681"</div>
</td>
<td>
<div class="spriteimage icon-uniE682"></div>
<div class="txt">Unicode:"e682"</div>
</td>
<td>
<div class="spriteimage icon-uniE683"></div>
<div class="txt">Unicode:"e683"</div>
</td>
<td>
<div class="spriteimage icon-uniE684"></div>
<div class="txt">Unicode:"e684"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE685"></div>
<div class="txt">Unicode:"e685"</div>
</td>
<td>
<div class="spriteimage icon-uniE686"></div>
<div class="txt">Unicode:"e686"</div>
</td>
<td>
<div class="spriteimage icon-uniE687"></div>
<div class="txt">Unicode:"e687"</div>
</td>
<td>
<div class="spriteimage icon-uniE688"></div>
<div class="txt">Unicode:"e688"</div>
</td>
<td>
<div class="spriteimage icon-uniE689"></div>
<div class="txt">Unicode:"e689"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE68A"></div>
<div class="txt">Unicode:"e68a"</div>
</td>
<td>
<div class="spriteimage icon-uniE68B"></div>
<div class="txt">Unicode:"e68b"</div>
</td>
<td>
<div class="spriteimage icon-uniE68C"></div>
<div class="txt">Unicode:"e68c"</div>
</td>
<td>
<div class="spriteimage icon-uniE68D"></div>
<div class="txt">Unicode:"e68d"</div>
</td>
<td>
<div class="spriteimage icon-uniE68E"></div>
<div class="txt">Unicode:"e68e"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE68F"></div>
<div class="txt">Unicode:"e68f"</div>
</td>
<td>
<div class="spriteimage icon-uniE690"></div>
<div class="txt">Unicode:"e690"</div>
</td>
<td>
<div class="spriteimage icon-uniE691"></div>
<div class="txt">Unicode:"e691"</div>
</td>
<td>
<div class="spriteimage icon-uniE692"></div>
<div class="txt">Unicode:"e692"</div>
</td>
<td>
<div class="spriteimage icon-uniE693"></div>
<div class="txt">Unicode:"e693"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE694"></div>
<div class="txt">Unicode:"e694"</div>
</td>
<td>
<div class="spriteimage icon-uniE695"></div>
<div class="txt">Unicode:"e695"</div>
</td>
<td>
<div class="spriteimage icon-uniE696"></div>
<div class="txt">Unicode:"e696"</div>
</td>
<td>
<div class="spriteimage icon-uniE697"></div>
<div class="txt">Unicode:"e697"</div>
</td>
<td>
<div class="spriteimage icon-uniE698"></div>
<div class="txt">Unicode:"e698"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE699"></div>
<div class="txt">Unicode:"e699"</div>
</td>
<td>
<div class="spriteimage icon-uniE69A"></div>
<div class="txt">Unicode:"e69a"</div>
</td>
<td>
<div class="spriteimage icon-uniE69B"></div>
<div class="txt">Unicode:"e69b"</div>
</td>
<td>
<div class="spriteimage icon-uniE69C"></div>
<div class="txt">Unicode:"e69c"</div>
</td>
<td>
<div class="spriteimage icon-uniE69D"></div>
<div class="txt">Unicode:"e69d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE69E"></div>
<div class="txt">Unicode:"e69e"</div>
</td>
<td>
<div class="spriteimage icon-uniE69F"></div>
<div class="txt">Unicode:"e69f"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A0"></div>
<div class="txt">Unicode:"e6a0"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A1"></div>
<div class="txt">Unicode:"e6a1"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A2"></div>
<div class="txt">Unicode:"e6a2"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6A3"></div>
<div class="txt">Unicode:"e6a3"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A4"></div>
<div class="txt">Unicode:"e6a4"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A5"></div>
<div class="txt">Unicode:"e6a5"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A6"></div>
<div class="txt">Unicode:"e6a6"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A7"></div>
<div class="txt">Unicode:"e6a7"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6A8"></div>
<div class="txt">Unicode:"e6a8"</div>
</td>
<td>
<div class="spriteimage icon-uniE6A9"></div>
<div class="txt">Unicode:"e6a9"</div>
</td>
<td>
<div class="spriteimage icon-uniE6AA"></div>
<div class="txt">Unicode:"e6aa"</div>
</td>
<td>
<div class="spriteimage icon-uniE6AB"></div>
<div class="txt">Unicode:"e6ab"</div>
</td>
<td>
<div class="spriteimage icon-uniE6AC"></div>
<div class="txt">Unicode:"e6ac"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6AD"></div>
<div class="txt">Unicode:"e6ad"</div>
</td>
<td>
<div class="spriteimage icon-uniE6AE"></div>
<div class="txt">Unicode:"e6ae"</div>
</td>
<td>
<div class="spriteimage icon-uniE6AF"></div>
<div class="txt">Unicode:"e6af"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B0"></div>
<div class="txt">Unicode:"e6b0"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B1"></div>
<div class="txt">Unicode:"e6b1"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6B2"></div>
<div class="txt">Unicode:"e6b2"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B3"></div>
<div class="txt">Unicode:"e6b3"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B4"></div>
<div class="txt">Unicode:"e6b4"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B5"></div>
<div class="txt">Unicode:"e6b5"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B6"></div>
<div class="txt">Unicode:"e6b6"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6B7"></div>
<div class="txt">Unicode:"e6b7"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B8"></div>
<div class="txt">Unicode:"e6b8"</div>
</td>
<td>
<div class="spriteimage icon-uniE6B9"></div>
<div class="txt">Unicode:"e6b9"</div>
</td>
<td>
<div class="spriteimage icon-uniE6BA"></div>
<div class="txt">Unicode:"e6ba"</div>
</td>
<td>
<div class="spriteimage icon-uniE6BB"></div>
<div class="txt">Unicode:"e6bb"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6BC"></div>
<div class="txt">Unicode:"e6bc"</div>
</td>
<td>
<div class="spriteimage icon-uniE6BD"></div>
<div class="txt">Unicode:"e6bd"</div>
</td>
<td>
<div class="spriteimage icon-uniE6BE"></div>
<div class="txt">Unicode:"e6be"</div>
</td>
<td>
<div class="spriteimage icon-uniE6BF"></div>
<div class="txt">Unicode:"e6bf"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C0"></div>
<div class="txt">Unicode:"e6c0"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6C1"></div>
<div class="txt">Unicode:"e6c1"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C2"></div>
<div class="txt">Unicode:"e6c2"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C3"></div>
<div class="txt">Unicode:"e6c3"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C4"></div>
<div class="txt">Unicode:"e6c4"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C5"></div>
<div class="txt">Unicode:"e6c5"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6C6"></div>
<div class="txt">Unicode:"e6c6"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C7"></div>
<div class="txt">Unicode:"e6c7"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C8"></div>
<div class="txt">Unicode:"e6c8"</div>
</td>
<td>
<div class="spriteimage icon-uniE6C9"></div>
<div class="txt">Unicode:"e6c9"</div>
</td>
<td>
<div class="spriteimage icon-uniE6CA"></div>
<div class="txt">Unicode:"e6ca"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6CB"></div>
<div class="txt">Unicode:"e6cb"</div>
</td>
<td>
<div class="spriteimage icon-uniE6CC"></div>
<div class="txt">Unicode:"e6cc"</div>
</td>
<td>
<div class="spriteimage icon-uniE6CD"></div>
<div class="txt">Unicode:"e6cd"</div>
</td>
<td>
<div class="spriteimage icon-uniE6CE"></div>
<div class="txt">Unicode:"e6ce"</div>
</td>
<td>
<div class="spriteimage icon-uniE6CF"></div>
<div class="txt">Unicode:"e6cf"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6D0"></div>
<div class="txt">Unicode:"e6d0"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D1"></div>
<div class="txt">Unicode:"e6d1"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D2"></div>
<div class="txt">Unicode:"e6d2"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D3"></div>
<div class="txt">Unicode:"e6d3"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D4"></div>
<div class="txt">Unicode:"e6d4"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6D5"></div>
<div class="txt">Unicode:"e6d5"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D6"></div>
<div class="txt">Unicode:"e6d6"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D7"></div>
<div class="txt">Unicode:"e6d7"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D8"></div>
<div class="txt">Unicode:"e6d8"</div>
</td>
<td>
<div class="spriteimage icon-uniE6D9"></div>
<div class="txt">Unicode:"e6d9"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6DA"></div>
<div class="txt">Unicode:"e6da"</div>
</td>
<td>
<div class="spriteimage icon-uniE6DB"></div>
<div class="txt">Unicode:"e6db"</div>
</td>
<td>
<div class="spriteimage icon-uniE6DC"></div>
<div class="txt">Unicode:"e6dc"</div>
</td>
<td>
<div class="spriteimage icon-uniE6DD"></div>
<div class="txt">Unicode:"e6dd"</div>
</td>
<td>
<div class="spriteimage icon-uniE6DE"></div>
<div class="txt">Unicode:"e6de"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6DF"></div>
<div class="txt">Unicode:"e6df"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E0"></div>
<div class="txt">Unicode:"e6e0"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E1"></div>
<div class="txt">Unicode:"e6e1"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E2"></div>
<div class="txt">Unicode:"e6e2"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E3"></div>
<div class="txt">Unicode:"e6e3"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6E4"></div>
<div class="txt">Unicode:"e6e4"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E5"></div>
<div class="txt">Unicode:"e6e5"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E6"></div>
<div class="txt">Unicode:"e6e6"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E7"></div>
<div class="txt">Unicode:"e6e7"</div>
</td>
<td>
<div class="spriteimage icon-uniE6E8"></div>
<div class="txt">Unicode:"e6e8"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6E9"></div>
<div class="txt">Unicode:"e6e9"</div>
</td>
<td>
<div class="spriteimage icon-uniE6EA"></div>
<div class="txt">Unicode:"e6ea"</div>
</td>
<td>
<div class="spriteimage icon-uniE6EB"></div>
<div class="txt">Unicode:"e6eb"</div>
</td>
<td>
<div class="spriteimage icon-uniE6EC"></div>
<div class="txt">Unicode:"e6ec"</div>
</td>
<td>
<div class="spriteimage icon-uniE6ED"></div>
<div class="txt">Unicode:"e6ed"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6EE"></div>
<div class="txt">Unicode:"e6ee"</div>
</td>
<td>
<div class="spriteimage icon-uniE6EF"></div>
<div class="txt">Unicode:"e6ef"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F0"></div>
<div class="txt">Unicode:"e6f0"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F1"></div>
<div class="txt">Unicode:"e6f1"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F2"></div>
<div class="txt">Unicode:"e6f2"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6F3"></div>
<div class="txt">Unicode:"e6f3"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F4"></div>
<div class="txt">Unicode:"e6f4"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F5"></div>
<div class="txt">Unicode:"e6f5"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F6"></div>
<div class="txt">Unicode:"e6f6"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F7"></div>
<div class="txt">Unicode:"e6f7"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6F8"></div>
<div class="txt">Unicode:"e6f8"</div>
</td>
<td>
<div class="spriteimage icon-uniE6F9"></div>
<div class="txt">Unicode:"e6f9"</div>
</td>
<td>
<div class="spriteimage icon-uniE6FA"></div>
<div class="txt">Unicode:"e6fa"</div>
</td>
<td>
<div class="spriteimage icon-uniE6FB"></div>
<div class="txt">Unicode:"e6fb"</div>
</td>
<td>
<div class="spriteimage icon-uniE6FC"></div>
<div class="txt">Unicode:"e6fc"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE6FD"></div>
<div class="txt">Unicode:"e6fd"</div>
</td>
<td>
<div class="spriteimage icon-uniE6FE"></div>
<div class="txt">Unicode:"e6fe"</div>
</td>
<td>
<div class="spriteimage icon-uniE6FF"></div>
<div class="txt">Unicode:"e6ff"</div>
</td>
<td>
<div class="spriteimage icon-uniE700"></div>
<div class="txt">Unicode:"e700"</div>
</td>
<td>
<div class="spriteimage icon-uniE701"></div>
<div class="txt">Unicode:"e701"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE702"></div>
<div class="txt">Unicode:"e702"</div>
</td>
<td>
<div class="spriteimage icon-uniE703"></div>
<div class="txt">Unicode:"e703"</div>
</td>
<td>
<div class="spriteimage icon-uniE704"></div>
<div class="txt">Unicode:"e704"</div>
</td>
<td>
<div class="spriteimage icon-uniE705"></div>
<div class="txt">Unicode:"e705"</div>
</td>
<td>
<div class="spriteimage icon-uniE706"></div>
<div class="txt">Unicode:"e706"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE707"></div>
<div class="txt">Unicode:"e707"</div>
</td>
<td>
<div class="spriteimage icon-uniE708"></div>
<div class="txt">Unicode:"e708"</div>
</td>
<td>
<div class="spriteimage icon-uniE709"></div>
<div class="txt">Unicode:"e709"</div>
</td>
<td>
<div class="spriteimage icon-uniE70A"></div>
<div class="txt">Unicode:"e70a"</div>
</td>
<td>
<div class="spriteimage icon-uniE70B"></div>
<div class="txt">Unicode:"e70b"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE70C"></div>
<div class="txt">Unicode:"e70c"</div>
</td>
<td>
<div class="spriteimage icon-uniE70D"></div>
<div class="txt">Unicode:"e70d"</div>
</td>
<td>
<div class="spriteimage icon-uniE70E"></div>
<div class="txt">Unicode:"e70e"</div>
</td>
<td>
<div class="spriteimage icon-uniE70F"></div>
<div class="txt">Unicode:"e70f"</div>
</td>
<td>
<div class="spriteimage icon-uniE710"></div>
<div class="txt">Unicode:"e710"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE711"></div>
<div class="txt">Unicode:"e711"</div>
</td>
<td>
<div class="spriteimage icon-uniE712"></div>
<div class="txt">Unicode:"e712"</div>
</td>
<td>
<div class="spriteimage icon-uniE713"></div>
<div class="txt">Unicode:"e713"</div>
</td>
<td>
<div class="spriteimage icon-uniE714"></div>
<div class="txt">Unicode:"e714"</div>
</td>
<td>
<div class="spriteimage icon-uniE715"></div>
<div class="txt">Unicode:"e715"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE716"></div>
<div class="txt">Unicode:"e716"</div>
</td>
<td>
<div class="spriteimage icon-uniE717"></div>
<div class="txt">Unicode:"e717"</div>
</td>
<td>
<div class="spriteimage icon-uniE718"></div>
<div class="txt">Unicode:"e718"</div>
</td>
<td>
<div class="spriteimage icon-uniE719"></div>
<div class="txt">Unicode:"e719"</div>
</td>
<td>
<div class="spriteimage icon-uniE71A"></div>
<div class="txt">Unicode:"e71a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE71B"></div>
<div class="txt">Unicode:"e71b"</div>
</td>
<td>
<div class="spriteimage icon-uniE71C"></div>
<div class="txt">Unicode:"e71c"</div>
</td>
<td>
<div class="spriteimage icon-uniE71D"></div>
<div class="txt">Unicode:"e71d"</div>
</td>
<td>
<div class="spriteimage icon-uniE71E"></div>
<div class="txt">Unicode:"e71e"</div>
</td>
<td>
<div class="spriteimage icon-uniE71F"></div>
<div class="txt">Unicode:"e71f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE720"></div>
<div class="txt">Unicode:"e720"</div>
</td>
<td>
<div class="spriteimage icon-uniE721"></div>
<div class="txt">Unicode:"e721"</div>
</td>
<td>
<div class="spriteimage icon-uniE722"></div>
<div class="txt">Unicode:"e722"</div>
</td>
<td>
<div class="spriteimage icon-uniE723"></div>
<div class="txt">Unicode:"e723"</div>
</td>
<td>
<div class="spriteimage icon-uniE724"></div>
<div class="txt">Unicode:"e724"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE725"></div>
<div class="txt">Unicode:"e725"</div>
</td>
<td>
<div class="spriteimage icon-uniE726"></div>
<div class="txt">Unicode:"e726"</div>
</td>
<td>
<div class="spriteimage icon-uniE727"></div>
<div class="txt">Unicode:"e727"</div>
</td>
<td>
<div class="spriteimage icon-uniE728"></div>
<div class="txt">Unicode:"e728"</div>
</td>
<td>
<div class="spriteimage icon-uniE729"></div>
<div class="txt">Unicode:"e729"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE72A"></div>
<div class="txt">Unicode:"e72a"</div>
</td>
<td>
<div class="spriteimage icon-uniE72B"></div>
<div class="txt">Unicode:"e72b"</div>
</td>
<td>
<div class="spriteimage icon-uniE72C"></div>
<div class="txt">Unicode:"e72c"</div>
</td>
<td>
<div class="spriteimage icon-uniE72D"></div>
<div class="txt">Unicode:"e72d"</div>
</td>
<td>
<div class="spriteimage icon-uniE72E"></div>
<div class="txt">Unicode:"e72e"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE72F"></div>
<div class="txt">Unicode:"e72f"</div>
</td>
<td>
<div class="spriteimage icon-uniE730"></div>
<div class="txt">Unicode:"e730"</div>
</td>
<td>
<div class="spriteimage icon-uniE731"></div>
<div class="txt">Unicode:"e731"</div>
</td>
<td>
<div class="spriteimage icon-uniE732"></div>
<div class="txt">Unicode:"e732"</div>
</td>
<td>
<div class="spriteimage icon-uniE733"></div>
<div class="txt">Unicode:"e733"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE734"></div>
<div class="txt">Unicode:"e734"</div>
</td>
<td>
<div class="spriteimage icon-uniE735"></div>
<div class="txt">Unicode:"e735"</div>
</td>
<td>
<div class="spriteimage icon-uniE736"></div>
<div class="txt">Unicode:"e736"</div>
</td>
<td>
<div class="spriteimage icon-uniE737"></div>
<div class="txt">Unicode:"e737"</div>
</td>
<td>
<div class="spriteimage icon-uniE738"></div>
<div class="txt">Unicode:"e738"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE739"></div>
<div class="txt">Unicode:"e739"</div>
</td>
<td>
<div class="spriteimage icon-uniE73A"></div>
<div class="txt">Unicode:"e73a"</div>
</td>
<td>
<div class="spriteimage icon-uniE73B"></div>
<div class="txt">Unicode:"e73b"</div>
</td>
<td>
<div class="spriteimage icon-uniE73C"></div>
<div class="txt">Unicode:"e73c"</div>
</td>
<td>
<div class="spriteimage icon-uniE73D"></div>
<div class="txt">Unicode:"e73d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE73E"></div>
<div class="txt">Unicode:"e73e"</div>
</td>
<td>
<div class="spriteimage icon-uniE73F"></div>
<div class="txt">Unicode:"e73f"</div>
</td>
<td>
<div class="spriteimage icon-uniE740"></div>
<div class="txt">Unicode:"e740"</div>
</td>
<td>
<div class="spriteimage icon-uniE741"></div>
<div class="txt">Unicode:"e741"</div>
</td>
<td>
<div class="spriteimage icon-uniE742"></div>
<div class="txt">Unicode:"e742"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE743"></div>
<div class="txt">Unicode:"e743"</div>
</td>
<td>
<div class="spriteimage icon-uniE744"></div>
<div class="txt">Unicode:"e744"</div>
</td>
<td>
<div class="spriteimage icon-uniE745"></div>
<div class="txt">Unicode:"e745"</div>
</td>
<td>
<div class="spriteimage icon-uniE746"></div>
<div class="txt">Unicode:"e746"</div>
</td>
<td>
<div class="spriteimage icon-uniE747"></div>
<div class="txt">Unicode:"e747"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE748"></div>
<div class="txt">Unicode:"e748"</div>
</td>
<td>
<div class="spriteimage icon-uniE749"></div>
<div class="txt">Unicode:"e749"</div>
</td>
<td>
<div class="spriteimage icon-uniE74A"></div>
<div class="txt">Unicode:"e74a"</div>
</td>
<td>
<div class="spriteimage icon-uniE74B"></div>
<div class="txt">Unicode:"e74b"</div>
</td>
<td>
<div class="spriteimage icon-uniE74C"></div>
<div class="txt">Unicode:"e74c"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE74D"></div>
<div class="txt">Unicode:"e74d"</div>
</td>
<td>
<div class="spriteimage icon-uniE74E"></div>
<div class="txt">Unicode:"e74e"</div>
</td>
<td>
<div class="spriteimage icon-uniE74F"></div>
<div class="txt">Unicode:"e74f"</div>
</td>
<td>
<div class="spriteimage icon-uniE750"></div>
<div class="txt">Unicode:"e750"</div>
</td>
<td>
<div class="spriteimage icon-uniE751"></div>
<div class="txt">Unicode:"e751"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE752"></div>
<div class="txt">Unicode:"e752"</div>
</td>
<td>
<div class="spriteimage icon-uniE753"></div>
<div class="txt">Unicode:"e753"</div>
</td>
<td>
<div class="spriteimage icon-uniE754"></div>
<div class="txt">Unicode:"e754"</div>
</td>
<td>
<div class="spriteimage icon-uniE755"></div>
<div class="txt">Unicode:"e755"</div>
</td>
<td>
<div class="spriteimage icon-uniE756"></div>
<div class="txt">Unicode:"e756"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE757"></div>
<div class="txt">Unicode:"e757"</div>
</td>
<td>
<div class="spriteimage icon-uniE758"></div>
<div class="txt">Unicode:"e758"</div>
</td>
<td>
<div class="spriteimage icon-uniE759"></div>
<div class="txt">Unicode:"e759"</div>
</td>
<td>
<div class="spriteimage icon-uniE75A"></div>
<div class="txt">Unicode:"e75a"</div>
</td>
<td>
<div class="spriteimage icon-uniE75B"></div>
<div class="txt">Unicode:"e75b"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE75C"></div>
<div class="txt">Unicode:"e75c"</div>
</td>
<td>
<div class="spriteimage icon-uniE75D"></div>
<div class="txt">Unicode:"e75d"</div>
</td>
<td>
<div class="spriteimage icon-uniE75E"></div>
<div class="txt">Unicode:"e75e"</div>
</td>
<td>
<div class="spriteimage icon-uniE75F"></div>
<div class="txt">Unicode:"e75f"</div>
</td>
<td>
<div class="spriteimage icon-uniE760"></div>
<div class="txt">Unicode:"e760"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE761"></div>
<div class="txt">Unicode:"e761"</div>
</td>
<td>
<div class="spriteimage icon-uniE762"></div>
<div class="txt">Unicode:"e762"</div>
</td>
<td>
<div class="spriteimage icon-uniE763"></div>
<div class="txt">Unicode:"e763"</div>
</td>
<td>
<div class="spriteimage icon-uniE764"></div>
<div class="txt">Unicode:"e764"</div>
</td>
<td>
<div class="spriteimage icon-uniE765"></div>
<div class="txt">Unicode:"e765"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE766"></div>
<div class="txt">Unicode:"e766"</div>
</td>
<td>
<div class="spriteimage icon-uniE767"></div>
<div class="txt">Unicode:"e767"</div>
</td>
<td>
<div class="spriteimage icon-uniE768"></div>
<div class="txt">Unicode:"e768"</div>
</td>
<td>
<div class="spriteimage icon-uniE769"></div>
<div class="txt">Unicode:"e769"</div>
</td>
<td>
<div class="spriteimage icon-uniE76A"></div>
<div class="txt">Unicode:"e76a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE76B"></div>
<div class="txt">Unicode:"e76b"</div>
</td>
<td>
<div class="spriteimage icon-uniE76C"></div>
<div class="txt">Unicode:"e76c"</div>
</td>
<td>
<div class="spriteimage icon-uniE76D"></div>
<div class="txt">Unicode:"e76d"</div>
</td>
<td>
<div class="spriteimage icon-uniE76E"></div>
<div class="txt">Unicode:"e76e"</div>
</td>
<td>
<div class="spriteimage icon-uniE76F"></div>
<div class="txt">Unicode:"e76f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE770"></div>
<div class="txt">Unicode:"e770"</div>
</td>
<td>
<div class="spriteimage icon-uniE771"></div>
<div class="txt">Unicode:"e771"</div>
</td>
<td>
<div class="spriteimage icon-uniE772"></div>
<div class="txt">Unicode:"e772"</div>
</td>
<td>
<div class="spriteimage icon-uniE773"></div>
<div class="txt">Unicode:"e773"</div>
</td>
<td>
<div class="spriteimage icon-uniE774"></div>
<div class="txt">Unicode:"e774"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE775"></div>
<div class="txt">Unicode:"e775"</div>
</td>
<td>
<div class="spriteimage icon-uniE776"></div>
<div class="txt">Unicode:"e776"</div>
</td>
<td>
<div class="spriteimage icon-uniE777"></div>
<div class="txt">Unicode:"e777"</div>
</td>
<td>
<div class="spriteimage icon-uniE778"></div>
<div class="txt">Unicode:"e778"</div>
</td>
<td>
<div class="spriteimage icon-uniE779"></div>
<div class="txt">Unicode:"e779"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE77A"></div>
<div class="txt">Unicode:"e77a"</div>
</td>
<td>
<div class="spriteimage icon-uniE77B"></div>
<div class="txt">Unicode:"e77b"</div>
</td>
<td>
<div class="spriteimage icon-uniE77C"></div>
<div class="txt">Unicode:"e77c"</div>
</td>
<td>
<div class="spriteimage icon-uniE77D"></div>
<div class="txt">Unicode:"e77d"</div>
</td>
<td>
<div class="spriteimage icon-uniE77E"></div>
<div class="txt">Unicode:"e77e"</div>
</td>
</tr>


<tr>
<td>
<div class="spriteimage icon-copy"></div>
<div class="txt">Unicode:"e77f"</div>
</td>
<td>
<div class="spriteimage icon-js-playground"></div>
<div class="txt">Unicode:"e780"</div>
</td>
<td>
<div class="spriteimage icon-agenda"></div>
<div class="txt">Unicode:"e781"</div>
</td>
<td>
<div class="spriteimage icon-allday"></div>
<div class="txt">Unicode:"e782"</div>
</td>
<td>
<div class="spriteimage icon-edit"></div>
<div class="txt">Unicode:"e783"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-repeat"></div>
<div class="txt">Unicode:"e784"</div>
</td>
<td>
<div class="spriteimage icon-uniE785"></div>
<div class="txt">Unicode:"e785"</div>
</td>
<td>
<div class="spriteimage icon-uniE786"></div>
<div class="txt">Unicode:"e786"</div>
</td>
<td>
<div class="spriteimage icon-uniE787"></div>
<div class="txt">Unicode:"e787"</div>
</td>
<td>
<div class="spriteimage icon-uniE788"></div>
<div class="txt">Unicode:"e788"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE789"></div>
<div class="txt">Unicode:"e789"</div>
</td>
<td>
<div class="spriteimage icon-uniE78A"></div>
<div class="txt">Unicode:"e78a"</div>
</td>
<td>
<div class="spriteimage icon-uniE78B"></div>
<div class="txt">Unicode:"e78b"</div>
</td>
<td>
<div class="spriteimage icon-uniE78C"></div>
<div class="txt">Unicode:"e78c"</div>
</td>
<td>
<div class="spriteimage icon-uniE78D"></div>
<div class="txt">Unicode:"e78d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE78E"></div>
<div class="txt">Unicode:"e78e"</div>
</td>
<td>
<div class="spriteimage icon-uniE78F"></div>
<div class="txt">Unicode:"e78f"</div>
</td>
<td>
<div class="spriteimage icon-uniE790"></div>
<div class="txt">Unicode:"e790"</div>
</td>
<td>
<div class="spriteimage icon-uniE791"></div>
<div class="txt">Unicode:"e791"</div>
</td>
<td>
<div class="spriteimage icon-uniE792"></div>
<div class="txt">Unicode:"e792"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE793"></div>
<div class="txt">Unicode:"e793"</div>
</td>
<td>
<div class="spriteimage icon-uniE794"></div>
<div class="txt">Unicode:"e794"</div>
</td>
<td>
<div class="spriteimage icon-uniE795"></div>
<div class="txt">Unicode:"e795"</div>
</td>
<td>
<div class="spriteimage icon-uniE796"></div>
<div class="txt">Unicode:"e796"</div>
</td>
<td>
<div class="spriteimage icon-uniE797"></div>
<div class="txt">Unicode:"e797"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE798"></div>
<div class="txt">Unicode:"e798"</div>
</td>
<td>
<div class="spriteimage icon-uniE799"></div>
<div class="txt">Unicode:"e799"</div>
</td>
<td>
<div class="spriteimage icon-uniE79A"></div>
<div class="txt">Unicode:"e79a"</div>
</td>
<td>
<div class="spriteimage icon-uniE79B"></div>
<div class="txt">Unicode:"e79b"</div>
</td>
<td>
<div class="spriteimage icon-uniE79C"></div>
<div class="txt">Unicode:"e79c"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE79D"></div>
<div class="txt">Unicode:"e79d"</div>
</td>
<td>
<div class="spriteimage icon-uniE79E"></div>
<div class="txt">Unicode:"e79e"</div>
</td>
<td>
<div class="spriteimage icon-uniE79F"></div>
<div class="txt">Unicode:"e79f"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A0"></div>
<div class="txt">Unicode:"e7a0"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A1"></div>
<div class="txt">Unicode:"e7a1"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7A2"></div>
<div class="txt">Unicode:"e7a2"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A3"></div>
<div class="txt">Unicode:"e7a3"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A4"></div>
<div class="txt">Unicode:"e7a4"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A5"></div>
<div class="txt">Unicode:"e7a5"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A6"></div>
<div class="txt">Unicode:"e7a6"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7A7"></div>
<div class="txt">Unicode:"e7a7"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A8"></div>
<div class="txt">Unicode:"e7a8"</div>
</td>
<td>
<div class="spriteimage icon-uniE7A9"></div>
<div class="txt">Unicode:"e7a9"</div>
</td>
<td>
<div class="spriteimage icon-uniE7AA"></div>
<div class="txt">Unicode:"e7aa"</div>
</td>
<td>
<div class="spriteimage icon-uniE7AB"></div>
<div class="txt">Unicode:"e7ab"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7AC"></div>
<div class="txt">Unicode:"e7ac"</div>
</td>
<td>
<div class="spriteimage icon-uniE7AD"></div>
<div class="txt">Unicode:"e7ad"</div>
</td>
<td>
<div class="spriteimage icon-uniE7AE"></div>
<div class="txt">Unicode:"e7ae"</div>
</td>
<td>
<div class="spriteimage icon-uniE7AF"></div>
<div class="txt">Unicode:"e7af"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B0"></div>
<div class="txt">Unicode:"e7b0"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7B1"></div>
<div class="txt">Unicode:"e7b1"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B2"></div>
<div class="txt">Unicode:"e7b2"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B3"></div>
<div class="txt">Unicode:"e7b3"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B4"></div>
<div class="txt">Unicode:"e7b4"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B5"></div>
<div class="txt">Unicode:"e7b5"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7B6"></div>
<div class="txt">Unicode:"e7b6"</div>
</td>
<td>
<div class="spriteimage icon-Recurrence"></div>
<div class="txt">Unicode:"e7b7"</div>
</td>
<td>
<div class="spriteimage icon-RecurrenceEdit"></div>
<div class="txt">Unicode:"e7b8"</div>
</td>
<td>
<div class="spriteimage icon-uniE7B9"></div>
<div class="txt">Unicode:"e7b9"</div>
</td>
<td>
<div class="spriteimage icon-uniE7BA"></div>
<div class="txt">Unicode:"e7ba"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7BB"></div>
<div class="txt">Unicode:"e7bb"</div>
</td>
<td>
<div class="spriteimage icon-uniE7BC"></div>
<div class="txt">Unicode:"e7bc"</div>
</td>
<td>
<div class="spriteimage icon-uniE7BD"></div>
<div class="txt">Unicode:"e7bd"</div>
</td>
<td>
<div class="spriteimage icon-uniE7BE"></div>
<div class="txt">Unicode:"e7be"</div>
</td>
<td>
<div class="spriteimage icon-uniE781"></div>
<div class="txt">Unicode:"e7bf"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE782"></div>
<div class="txt">Unicode:"e7c0"</div>
</td>
<td>
<div class="spriteimage icon-uniE783"></div>
<div class="txt">Unicode:"e7c1"</div>
</td>
<td>
<div class="spriteimage icon-uniE784"></div>
<div class="txt">Unicode:"e7c2"</div>
</td>
<td>
<div class="spriteimage icon-uniE7852"></div>
<div class="txt">Unicode:"e7c3"</div>
</td>
<td>
<div class="spriteimage icon-uniE7862"></div>
<div class="txt">Unicode:"e7c4"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7872"></div>
<div class="txt">Unicode:"e7c5"</div>
</td>
<td>
<div class="spriteimage icon-uniE7882"></div>
<div class="txt">Unicode:"e7c6"</div>
</td>
<td>
<div class="spriteimage icon-uniE7892"></div>
<div class="txt">Unicode:"e7c7"</div>
</td>
<td>
<div class="spriteimage icon-uniE78A2"></div>
<div class="txt">Unicode:"e7c8"</div>
</td>
<td>
<div class="spriteimage icon-uniE78B2"></div>
<div class="txt">Unicode:"e7c9"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE78C2"></div>
<div class="txt">Unicode:"e7ca"</div>
</td>
<td>
<div class="spriteimage icon-uniE78D2"></div>
<div class="txt">Unicode:"e7cb"</div>
</td>
<td>
<div class="spriteimage icon-down-arrow-icon"></div>
<div class="txt">Unicode:"e7cc"</div>
</td>
<td>
<div class="spriteimage icon-dropdown"></div>
<div class="txt">Unicode:"e7cd"</div>
</td>
<td>
<div class="spriteimage icon-qat-icon"></div>
<div class="txt">Unicode:"e7ce"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-tick"></div>
<div class="txt">Unicode:"e7cf"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_Print"></div>
<div class="txt">Unicode:"e7d0"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_First"></div>
<div class="txt">Unicode:"e7d1"</div>
</td>
<td>
<div class="spriteimage icon-PDf_Previous"></div>
<div class="txt">Unicode:"e7d2"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_Next"></div>
<div class="txt">Unicode:"e7d3"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Pdf_Last"></div>
<div class="txt">Unicode:"e7d4"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_ZoomIn"></div>
<div class="txt">Unicode:"e7d5"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_ZoomOut"></div>
<div class="txt">Unicode:"e7d6"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_FitPage"></div>
<div class="txt">Unicode:"e7d7"</div>
</td>
<td>
<div class="spriteimage icon-Pdf_FitWidth"></div>
<div class="txt">Unicode:"e7d8"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-X16ICONS_UnFreeze"></div>
<div class="txt">Unicode:"e7d9"</div>
</td>
<td>
<div class="spriteimage icon-X16ICONS_FREEZE_Freeze"></div>
<div class="txt">Unicode:"e7da"</div>
</td>
<td>
<div class="spriteimage icon-X16ICONS_FreezeColumnsBefore"></div>
<div class="txt">Unicode:"e7db"</div>
</td>
<td>
<div class="spriteimage icon-Chart_Bubble"></div>
<div class="txt">Unicode:"e7dc"</div>
</td>
<td>
<div class="spriteimage icon-Chart_Doughnut"></div>
<div class="txt">Unicode:"e7dd"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Chart_radar"></div>
<div class="txt">Unicode:"e7de"</div>
</td>
<td>
<div class="spriteimage icon-Chart_Scatter"></div>
<div class="txt">Unicode:"e7df"</div>
</td>
<td>
<div class="spriteimage icon-Chart-07"></div>
<div class="txt">Unicode:"e7e0"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E1"></div>
<div class="txt">Unicode:"e7e1"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E2"></div>
<div class="txt">Unicode:"e7e2"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7E3"></div>
<div class="txt">Unicode:"e7e3"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E4"></div>
<div class="txt">Unicode:"e7e4"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E5"></div>
<div class="txt">Unicode:"e7e5"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E6"></div>
<div class="txt">Unicode:"e7e6"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E7"></div>
<div class="txt">Unicode:"e7e7"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7E8"></div>
<div class="txt">Unicode:"e7e8"</div>
</td>
<td>
<div class="spriteimage icon-uniE7E9"></div>
<div class="txt">Unicode:"e7e9"</div>
</td>
<td>
<div class="spriteimage icon-uniE7EA"></div>
<div class="txt">Unicode:"e7ea"</div>
</td>
<td>
<div class="spriteimage icon-uniE7EB"></div>
<div class="txt">Unicode:"e7eb"</div>
</td>
<td>
<div class="spriteimage icon-uniE7EC"></div>
<div class="txt">Unicode:"e7ec"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7ED"></div>
<div class="txt">Unicode:"e7ed"</div>
</td>
<td>
<div class="spriteimage icon-uniE7EE"></div>
<div class="txt">Unicode:"e7ee"</div>
</td>
<td>
<div class="spriteimage icon-uniE7EF"></div>
<div class="txt">Unicode:"e7ef"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F0"></div>
<div class="txt">Unicode:"e7f0"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F1"></div>
<div class="txt">Unicode:"e7f1"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7F2"></div>
<div class="txt">Unicode:"e7f2"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F3"></div>
<div class="txt">Unicode:"e7f3"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F4"></div>
<div class="txt">Unicode:"e7f4"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F5"></div>
<div class="txt">Unicode:"e7f5"</div>
</td>
<td>
<div class="spriteimage icon-uniE7F6"></div>
<div class="txt">Unicode:"e7f6"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7f7"></div>
<div class="txt">Unicode:"e7f7"</div>
</td>
<td>
<div class="spriteimage icon-uniE7f8"></div>
<div class="txt">Unicode:"e7f8"</div>
</td>
<td>
<div class="spriteimage icon-uniE7f9"></div>
<div class="txt">Unicode:"e7f9"</div>
</td>
<td>
<div class="spriteimage icon-uniE7fa"></div>
<div class="txt">Unicode:"e7fa"</div>
</td>
<td>
<div class="spriteimage icon-uniE7fb"></div>
<div class="txt">Unicode:"e7fb"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE7fc"></div>
<div class="txt">Unicode:"e7fc"</div>
</td>
<td>
<div class="spriteimage icon-uniE7fd"></div>
<div class="txt">Unicode:"e7fd"</div>
</td>
<td>
<div class="spriteimage icon-uniE7fe"></div>
<div class="txt">Unicode:"e7fe"</div>
</td>
<td>
<div class="spriteimage icon-uniE7ff"></div>
<div class="txt">Unicode:"e7ff"</div>
</td>
<td>
<div class="spriteimage icon-uniE800"></div>
<div class="txt">Unicode:"e800"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE801"></div>
<div class="txt">Unicode:"e801"</div>
</td>
<td>
<div class="spriteimage icon-uniE802"></div>
<div class="txt">Unicode:"e802"</div>
</td>
<td>
<div class="spriteimage icon-uniE803"></div>
<div class="txt">Unicode:"e803"</div>
</td>
<td>
<div class="spriteimage icon-uniE804"></div>
<div class="txt">Unicode:"e804"</div>
</td>
<td>
<div class="spriteimage icon-uniE805"></div>
<div class="txt">Unicode:"e805"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE806"></div>
<div class="txt">Unicode:"e806"</div>
</td>
<td>
<div class="spriteimage icon-uniE807"></div>
<div class="txt">Unicode:"e807"</div>
</td>
<td>
<div class="spriteimage icon-uniE808"></div>
<div class="txt">Unicode:"e808"</div>
</td>
<td>
<div class="spriteimage icon-unie809"></div>
<div class="txt">Unicode:"e809"</div>
</td>
<td>
<div class="spriteimage icon-uniE80a"></div>
<div class="txt">Unicode:"e80a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE80b"></div>
<div class="txt">Unicode:"e80b"</div>
</td>
<td>
<div class="spriteimage icon-uniE80c"></div>
<div class="txt">Unicode:"e80c"</div>
</td>
<td>
<div class="spriteimage icon-uniE80d"></div>
<div class="txt">Unicode:"e80d"</div>
</td>
<td>
<div class="spriteimage icon-uniE80e"></div>
<div class="txt">Unicode:"e80e"</div>
</td>
<td>
<div class="spriteimage icon-print-icon-02"></div>
<div class="txt">Unicode:"e80f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE810"></div>
<div class="txt">Unicode:"e810"</div>
</td>
<td>
<div class="spriteimage icon-a-051"></div>
<div class="txt">Unicode:"e811"</div>
</td>
<td>
<div class="spriteimage icon-a-061"></div>
<div class="txt">Unicode:"e812"</div>
</td>
<td>
<div class="spriteimage icon-filter-031"></div>
<div class="txt">Unicode:"e813"</div>
</td>
<td>
<div class="spriteimage icon-filter-042"></div>
<div class="txt">Unicode:"e814"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-backarrow-08"></div>
<div class="txt">Unicode:"e815"</div>
</td>
<td>
<div class="spriteimage icon-BurgerMenu_iOS"></div>
<div class="txt">Unicode:"e816"</div>
</td>
<td>
<div class="spriteimage icon-Icon-03"></div>
<div class="txt">Unicode:"e817"</div>
</td>
<td>
<div class="spriteimage icon-Icon-04"></div>
<div class="txt">Unicode:"e818"</div>
</td>
<td>
<div class="spriteimage icon-Icon-05"></div>
<div class="txt">Unicode:"e819"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Icon-06"></div>
<div class="txt">Unicode:"e81a"</div>
</td>
<td>
<div class="spriteimage icon-uniE81b"></div>
<div class="txt">Unicode:"e81b"</div>
</td>
<td>
<div class="spriteimage icon-uniE81c"></div>
<div class="txt">Unicode:"e81c"</div>
</td>
<td>
<div class="spriteimage icon-Adopt__Down-arrow"></div>
<div class="txt">Unicode:"e81d"</div>
</td>
<td>
<div class="spriteimage icon-Adopt__up-arrow"></div>
<div class="txt">Unicode:"e81e"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-download-pdf"></div>
<div class="txt">Unicode:"e81f"</div>
</td>
<td>
<div class="spriteimage icon-arrow--down1"></div>
<div class="txt">Unicode:"e820"</div>
</td>
<td>
<div class="spriteimage icon-arrow--up1"></div>
<div class="txt">Unicode:"e821"</div>
</td>
<td>
<div class="spriteimage icon-CriticalTask_Taskbar_Icon_Solid"></div>
<div class="txt">Unicode:"e822"</div>
</td>
<td>
<div class="spriteimage icon-sort-by-icon-01"></div>
<div class="txt">Unicode:"e823"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Icon_descending"></div>
<div class="txt">Unicode:"e824"</div>
</td>
<td>
<div class="spriteimage icon-Icon_ascending"></div>
<div class="txt">Unicode:"e825"</div>
</td>
<td>
<div class="spriteimage icon-previous-page-pdfviewer"></div>
<div class="txt">Unicode:"e826"</div>
</td>
<td>
<div class="spriteimage icon-next-page-pdfviewer"></div>
<div class="txt">Unicode:"e827"</div>
</td>
<td>
<div class="spriteimage icon-zoomout-pdfviewer"></div>
<div class="txt">Unicode:"e828"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-zoomin-pdfviewer"></div>
<div class="txt">Unicode:"e829"</div>
</td>
<td>
<div class="spriteimage icon-fitwidth-pdfviewer"></div>
<div class="txt">Unicode:"e82a"</div>
</td>
<td>
<div class="spriteimage icon-fitpage-pdfviewer"></div>
<div class="txt">Unicode:"e82b"</div>
</td>
<td>
<div class="spriteimage icon-print-pdfviewer"></div>
<div class="txt">Unicode:"e82c"</div>
</td>
<td>
<div class="spriteimage icon-download-pdf-pdfviewer"></div>
<div class="txt">Unicode:"e82d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-search-icon-pdfviewer"></div>
<div class="txt">Unicode:"e82e"</div>
</td>
<td>
<div class="spriteimage icon-search-prev-pdfviewer"></div>
<div class="txt">Unicode:"e82f"</div>
</td>
<td>
<div class="spriteimage icon-search-next-pdfviewer"></div>
<div class="txt">Unicode:"e830"</div>
</td>
<td>
<div class="spriteimage icon-uniE831"></div>
<div class="txt">Unicode:"e831"</div>
</td>
<td>
<div class="spriteimage icon-uniE832"></div>
<div class="txt">Unicode:"e832"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE833"></div>
<div class="txt">Unicode:"e833"</div>
</td>
<td>
<div class="spriteimage icon-uniE834"></div>
<div class="txt">Unicode:"e834"</div>
</td>
<td>
<div class="spriteimage icon-uniE835"></div>
<div class="txt">Unicode:"e835"</div>
</td>
<td>
<div class="spriteimage icon-uniE836"></div>
<div class="txt">Unicode:"e836"</div>
</td>
<td>
<div class="spriteimage icon-search-close-pdfviewer"></div>
<div class="txt">Unicode:"e837"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-waterfall"></div>
<div class="txt">Unicode:"e838"</div>
</td>
<td>
<div class="spriteimage icon-Database"></div>
<div class="txt">Unicode:"e839"</div>
</td>
<td>
<div class="spriteimage icon-Remove-DB-report"></div>
<div class="txt">Unicode:"e83a"</div>
</td>
<td>
<div class="spriteimage icon-Rename-DB-report"></div>
<div class="txt">Unicode:"e83b"</div>
</td>
<td>
<div class="spriteimage icon-Save-As"></div>
<div class="txt">Unicode:"e83c"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-back-icon"></div>
<div class="txt">Unicode:"e83d"</div>
</td>
<td>
<div class="spriteimage icon-uniE83e"></div>
<div class="txt">Unicode:"e83e"</div>
</td>
<td>
<div class="spriteimage icon-uniE83f"></div>
<div class="txt">Unicode:"e83f"</div>
</td>
<td>
<div class="spriteimage icon-uniE840"></div>
<div class="txt">Unicode:"e840"</div>
</td>
<td>
<div class="spriteimage icon-uniE841"></div>
<div class="txt">Unicode:"e841"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-ColumnFreeze"></div>
<div class="txt">Unicode:"e842"</div>
</td>
<td>
<div class="spriteimage icon-AdvancedFiltering"></div>
<div class="txt">Unicode:"e843"</div>
</td>
<td>
<div class="spriteimage icon-Cell-context"></div>
<div class="txt">Unicode:"e844"</div>
</td>
<td>
<div class="spriteimage icon-ExcelExporting"></div>
<div class="txt">Unicode:"e845"</div>
</td>
<td>
<div class="spriteimage icon-PDFExporting"></div>
<div class="txt">Unicode:"e846"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-CSVExporting"></div>
<div class="txt">Unicode:"e847"</div>
</td>
<td>
<div class="spriteimage icon-FrozenHeaders"></div>
<div class="txt">Unicode:"e848"</div>
</td>
<td>
<div class="spriteimage icon-Summary-types"></div>
<div class="txt">Unicode:"e849"</div>
</td>
<td>
<div class="spriteimage icon-ColumnheaderHyperlink"></div>
<div class="txt">Unicode:"e84a"</div>
</td>
<td>
<div class="spriteimage icon-CalculatedFields"></div>
<div class="txt">Unicode:"e84b"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Hyperlink"></div>
<div class="txt">Unicode:"e84c"</div>
</td>
<td>
<div class="spriteimage icon-RTL"></div>
<div class="txt">Unicode:"e84d"</div>
</td>
<td>
<div class="spriteimage icon-WordExporting"></div>
<div class="txt">Unicode:"e84e"</div>
</td>
<td>
<div class="spriteimage icon-Exporting"></div>
<div class="txt">Unicode:"e84f"</div>
</td>
<td>
<div class="spriteimage icon-ConditionalFormatting"></div>
<div class="txt">Unicode:"e850"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-ColumnResizing"></div>
<div class="txt">Unicode:"e851"</div>
</td>
<td>
<div class="spriteimage icon-SummaryCustomization"></div>
<div class="txt">Unicode:"e852"</div>
</td>
<td>
<div class="spriteimage icon-RowFreeze"></div>
<div class="txt">Unicode:"e853"</div>
</td>
<td>
<div class="spriteimage icon-Paging"></div>
<div class="txt">Unicode:"e854"</div>
</td>
<td>
<div class="spriteimage icon-CellEditing"></div>
<div class="txt">Unicode:"e855"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-CellSelection"></div>
<div class="txt">Unicode:"e856"</div>
</td>
<td>
<div class="spriteimage icon-NumberFormats"></div>
<div class="txt">Unicode:"e857"</div>
</td>
<td>
<div class="spriteimage icon-Tooltip"></div>
<div class="txt">Unicode:"e858"</div>
</td>
<td>
<div class="spriteimage icon-ExcelLikeLayout"></div>
<div class="txt">Unicode:"e859"</div>
</td>
<td>
<div class="spriteimage icon-ValueCellHyperlink"></div>
<div class="txt">Unicode:"e85a"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-SummaryCellHyperlink"></div>
<div class="txt">Unicode:"e85b"</div>
</td>
<td>
<div class="spriteimage icon-RowHeaderHyperlink"></div>
<div class="txt">Unicode:"e85c"</div>
</td>
<td>
<div class="spriteimage icon-CollapseByDefault"></div>
<div class="txt">Unicode:"e85d"</div>
</td>
<td>
<div class="spriteimage icon-15"></div>
<div class="txt">Unicode:"e85e"</div>
</td>
<td>
<div class="spriteimage icon-16"></div>
<div class="txt">Unicode:"e85f"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-17"></div>
<div class="txt">Unicode:"e860"</div>
</td>
<td>
<div class="spriteimage icon-18"></div>
<div class="txt">Unicode:"e861"</div>
</td>
<td>
<div class="spriteimage icon-19"></div>
<div class="txt">Unicode:"e862"</div>
</td>
<td>
<div class="spriteimage icon-20"></div>
<div class="txt">Unicode:"e863"</div>
</td>
<td>
<div class="spriteimage icon-uniE864"></div>
<div class="txt">Unicode:"e864"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE865"></div>
<div class="txt">Unicode:"e865"</div>
</td>
<td>
<div class="spriteimage icon-22"></div>
<div class="txt">Unicode:"e866"</div>
</td>
<td>
<div class="spriteimage icon-23"></div>
<div class="txt">Unicode:"e867"</div>
</td>
<td>
<div class="spriteimage icon-24"></div>
<div class="txt">Unicode:"e868"</div>
</td>
<td>
<div class="spriteimage icon-25"></div>
<div class="txt">Unicode:"e869"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-D-disable-icon"></div>
<div class="txt">Unicode:"e86a"</div>
</td>
<td>
<div class="spriteimage icon-Text-Selection"></div>
<div class="txt">Unicode:"e86b"</div>
</td>
<td>
<div class="spriteimage icon-Text-Strike"></div>
<div class="txt">Unicode:"e86c"</div>
</td>
<td>
<div class="spriteimage icon-Text-Underline"></div>
<div class="txt">Unicode:"e86d"</div>
</td>
<td>
<div class="spriteimage icon-PDF-viewer-JS_Arrow"></div>
<div class="txt">Unicode:"e86e"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Calculated-member_-Toolbar-Black-Color-Icon"></div>
<div class="txt">Unicode:"e86f"</div>
</td>
<td>
<div class="spriteimage icon-Calculated-member_-Tree-View-Black-Color-Icon"></div>
<div class="txt">Unicode:"e870"</div>
</td>
<td>
<div class="spriteimage icon-Disable-Cross-Hair"></div>
<div class="txt">Unicode:"e871"</div>
</td>
<td>
<div class="spriteimage icon-Enable-Cross-Hair"></div>
<div class="txt">Unicode:"e872"</div>
</td>
<td>
<div class="spriteimage icon-Hide"></div>
<div class="txt">Unicode:"e873"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Icon_Collapse"></div>
<div class="txt">Unicode:"e874"</div>
</td>
<td>
<div class="spriteimage icon-Icon_Drill-Through"></div>
<div class="txt">Unicode:"e875"</div>
</td>
<td>
<div class="spriteimage icon-Icon_Expand"></div>
<div class="txt">Unicode:"e876"</div>
</td>
<td>
<div class="spriteimage icon-Interaction"></div>
<div class="txt">Unicode:"e877"</div>
</td>
<td>
<div class="spriteimage icon-Layout"></div>
<div class="txt">Unicode:"e878"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Legend"></div>
<div class="txt">Unicode:"e879"</div>
</td>
<td>
<div class="spriteimage icon-Marker"></div>
<div class="txt">Unicode:"e87a"</div>
</td>
<td>
<div class="spriteimage icon-Multiple-Rows"></div>
<div class="txt">Unicode:"e87b"</div>
</td>
<td>
<div class="spriteimage icon-No-Summary-Layout"></div>
<div class="txt">Unicode:"e87c"</div>
</td>
<td>
<div class="spriteimage icon-Normal-Layout"></div>
<div class="txt">Unicode:"e87d"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Rotate-45"></div>
<div class="txt">Unicode:"e87e"</div>
</td>
<td>
<div class="spriteimage icon-Rotate-90"></div>
<div class="txt">Unicode:"e87f"</div>
</td>
<td>
<div class="spriteimage icon-Smart-Labels"></div>
<div class="txt">Unicode:"e880"</div>
</td>
<td>
<div class="spriteimage icon-Top-Summary-Layout"></div>
<div class="txt">Unicode:"e881"</div>
</td>
<td>
<div class="spriteimage icon-Track-Ball"></div>
<div class="txt">Unicode:"e882"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Trim"></div>
<div class="txt">Unicode:"e883"</div>
</td>
<td>
<div class="spriteimage icon-Wrap-By-Word"></div>
<div class="txt">Unicode:"e884"</div>
</td>
<td>
<div class="spriteimage icon-Wrap"></div>
<div class="txt">Unicode:"e885"</div>
</td>
<td>
<div class="spriteimage icon-Zoom-In"></div>
<div class="txt">Unicode:"e886"</div>
</td>
<td>
<div class="spriteimage icon-Zoom-Out"></div>
<div class="txt">Unicode:"e887"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE8d1"></div>
<div class="txt">Unicode:"e8d1"</div>
</td>
<td>
<div class="spriteimage icon-uniE8d2"></div>
<div class="txt">Unicode:"e8d2"</div>
</td>
<td>
<div class="spriteimage icon-Base-line_Hide"></div>
<div class="txt">Unicode:"e900"</div>
</td>
<td>
<div class="spriteimage icon-Base-line_Show"></div>
<div class="txt">Unicode:"e901"</div>
</td>
<td>
<div class="spriteimage icon-RTL_Dark"></div>
<div class="txt">Unicode:"e902"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-Signature-icon-03"></div>
<div class="txt">Unicode:"e903"</div>
</td>
<td>
<div class="spriteimage icon-selection-icon-03"></div>
<div class="txt">Unicode:"e904"</div>
</td>
<td>
<div class="spriteimage icon-selection-icon-05"></div>
<div class="txt">Unicode:"e905"</div>
</td>
<td>
<div class="spriteimage icon-b-79"></div>
<div class="txt">Unicode:"e906"</div>
</td>
<td>
<div class="spriteimage icon-b-80"></div>
<div class="txt">Unicode:"e907"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-b-81"></div>
<div class="txt">Unicode:"e908"</div>
</td>
<td>
<div class="spriteimage icon-b-82"></div>
<div class="txt">Unicode:"e909"</div>
</td>
<td>
<div class="spriteimage icon-b-83"></div>
<div class="txt">Unicode:"e90a"</div>
</td>
<td>
<div class="spriteimage icon-b-84"></div>
<div class="txt">Unicode:"e90b"</div>
</td>
<td>
<div class="spriteimage icon-b-85"></div>
<div class="txt">Unicode:"e90c"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-b-86"></div>
<div class="txt">Unicode:"e90d"</div>
</td>
<td>
<div class="spriteimage icon-b-87"></div>
<div class="txt">Unicode:"e90e"</div>
</td>
<td>
<div class="spriteimage icon-b-88"></div>
<div class="txt">Unicode:"e90f"</div>
</td>
<td>
<div class="spriteimage icon-b-89"></div>
<div class="txt">Unicode:"e910"</div>
</td>
<td>
<div class="spriteimage icon-uniE912"></div>
<div class="txt">Unicode:"e911"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-uniE913"></div>
<div class="txt">Unicode:"e912"</div>
</td>
<td>
<div class="spriteimage icon-a-70"></div>
<div class="txt">Unicode:"e913"</div>
</td>
<td>
<div class="spriteimage icon-a-71"></div>
<div class="txt">Unicode:"e914"</div>
</td>
<td>
<div class="spriteimage icon-v-92"></div>
<div class="txt">Unicode:"e915"</div>
</td>
<td>
<div class="spriteimage icon-v-93"></div>
<div class="txt">Unicode:"e916"</div>
</td>
</tr>

<tr>
<td>
<div class="spriteimage icon-xAxis-title"></div>
<div class="txt">Unicode:"e917"</div>
</td>
</tr>
</table>