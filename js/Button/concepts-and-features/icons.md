---
layout: post
title: icons
description: icons
platform: js
control: Button
documentation: ug
---

# Icons

The **Essential Studio for JavaScript** provide icons library that contains the number of in-built icons that can be applied for CSS class names to elements and refer “ej.widgets.all.core.min.css” file. Use the following syntax to apply class names.

**Syntax**: .e-icon .e-[icon description]

.e-icon .e-search

## Adding icon in Button

For example, you can render the desired icon in the button by using the following table that contains the listed icons’ CSS class names in the “prefixIcon” property of button component. Also, use “contentType” property to display the icon in the button. In the following code example, specify the “contentType” of the button as imageonly.    

Refer to the following link to know what are the values passed in the “contentType” property

[http://help.syncfusion.com/UG/JS_CR/global.html#ContentType](http://help.syncfusion.com/UG/JS_CR/global.html)

Also in the button sample, you can use the icon class names as follows,

{% highlight js %}

[JS]

$("#buttonid").ejButton({
                contentType: "imageonly",
**prefixIcon: "e-handup"**
            });



{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\Button\concepts-and-features\icons_images\icons_img1.png" Caption="Figure 12: Icon library used in button component"%}

## List of Icons

The complete list of icons is listed in the following table.

_Table_ _1__: List of icons_

<table>
<tr>
<td>
e-unpin</td><td>
<img src="icons_images\icons_img2.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-pin</td><td>
<img src="icons_images\icons_img3.png" alt="" width="14pt" height="16pt"</td></tr>
<tr>
<td>
e-upload</td><td>
<img src="icons_images\icons_img4.png" alt="" width="17pt" height="15pt"</td></tr>
<tr>
<td>
e-reload</td><td>
<img src="icons_images\icons_img5.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-collaps</td><td>
<img src="icons_images\icons_img6.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-cancel</td><td>
<img src="icons_images\icons_img7.png" alt="" width="15pt" height="18pt"</td></tr>
<tr>
<td>
e-expand</td><td>
<img src="icons_images\icons_img8.png" alt="" width="16pt" height="10pt"</td></tr>
<tr>
<td>
e-minimize</td><td>
<img src="icons_images\icons_img9.png" alt="" width="16pt" height="10pt"</td></tr>
<tr>
<td>
e-login</td><td>
<img src="icons_images\icons_img10.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-orientationlanscape</td><td>
<img src="icons_images\icons_img11.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-alignleft</td><td>
<img src="icons_images\icons_img12.png" alt="" width="15pt" height="16pt"</td></tr>
<tr>
<td>
e-aligncenter</td><td>
<img src="icons_images\icons_img13.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-alignright</td><td>
<img src="icons_images\icons_img14.png" alt="" width="15pt" height="16pt"</td></tr>
<tr>
<td>
e-alignjustify</td><td>
<img src="icons_images\icons_img15.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-alignnone</td><td>
<img src="icons_images\icons_img16.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-filterset</td><td>
<img src="icons_images\icons_img17.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-filternone</td><td>
<img src="icons_images\icons_img18.png" alt="" width="11pt" height="13pt"</td></tr>
<tr>
<td>
e-arrowheadup-2x</td><td>
<img src="icons_images\icons_img19.png" alt="" width="14pt" height="13pt"</td></tr>
<tr>
<td>
e-arrowheaddown-2x</td><td>
 <img src="icons_images\icons_img20.png" alt="" width="12pt" height="14pt"</td></tr>
<tr>
<td>
e-arrowheadleft-2x</td><td>
 <img src="icons_images\icons_img21.png" alt="" width="10pt" height="12pt"</td></tr>
<tr>
<td>
e-arrowheadright-2x</td><td>
 <img src="icons_images\icons_img22.png" alt="" width="10pt" height="14pt"</td></tr>
<tr>
<td>
e-numbering</td><td>
<img src="icons_images\icons_img23.png" alt="" width="14pt" height="16pt"</td></tr>
<tr>
<td>
e-bullets</td><td>
<img src="icons_images\icons_img24.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-maximize</td><td>
<img src="icons_images\icons_img25.png" alt="" width="13pt" height="12pt"</td></tr>
<tr>
<td>
e-delete</td><td>
<img src="icons_images\icons_img26.png" alt="" width="12pt" height="17pt"</td></tr>
<tr>
<td>
e-scroll</td><td>
<img src="icons_images\icons_img27.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-right-scroll</td><td>
<img src="icons_images\icons_img28.png" alt="" width="16pt" height="16pt"</td></tr>
<tr>
<td>
e-search</td><td>
<img src="icons_images\icons_img29.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-mediaback</td><td>
<img src="icons_images\icons_img30.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-mediaforward</td><td>
<img src="icons_images\icons_img31.png" alt="" width="11pt" height="14pt"</td></tr>
<tr>
<td>
e-medianext</td><td>
<img src="icons_images\icons_img32.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-mediaprev</td><td>
<img src="icons_images\icons_img33.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-mediaeject</td><td>
<img src="icons_images\icons_img34.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-mediaclose</td><td>
<img src="icons_images\icons_img35.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-mediapause</td><td>
<img src="icons_images\icons_img36.png" alt="" width="12pt" height="13pt"</td></tr>
<tr>
<td>
e-mediaplay</td><td>
<img src="icons_images\icons_img37.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-righttick</td><td>
<img src="icons_images\icons_img38.png" alt="" width="15pt" height="12pt"</td></tr>
<tr>
<td>
e-smile</td><td>
<img src="icons_images\icons_img39.png" alt="" width="16pt" height="16pt"</td></tr>
<tr>
<td>
e-information</td><td>
<img src="icons_images\icons_img40.png" alt="" width="16pt" height="15pt"</td></tr>
<tr>
<td>
e-left-arrow</td><td>
 <img src="icons_images\icons_img41.png" alt="" width="12pt" height="14pt"</td></tr>
<tr>
<td>
e-right-arrow</td><td>
 <img src="icons_images\icons_img42.png" alt="" width="10pt" height="13pt"</td></tr>
<tr>
<td>
e-file-delete</td><td>
 <img src="icons_images\icons_img43.png" alt="" width="12pt" height="17pt"</td></tr>
<tr>
<td>
e-file-percentage-success</td><td>
 <img src="icons_images\icons_img44.png" alt="" width="15pt" height="12pt"</td></tr>
<tr>
<td>
e-file-cancel</td><td>
 <img src="icons_images\icons_img45.png" alt="" width="11pt" height="13pt"</td></tr>
<tr>
<td>
e-file-percentage-failed</td><td>
 <img src="icons_images\icons_img46.png" alt="" width="11pt" height="13pt"</td></tr>
<tr>
<td>
e-file-retry</td><td>
 <img src="icons_images\icons_img47.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-resize-handle</td><td>
  <img src="icons_images\icons_img48.png" alt="" width="12pt" height="14pt"</td></tr>
<tr>
<td>
e-down-arrow</td><td>
 <img src="icons_images\icons_img49.png" alt="" width="14pt" height="12pt"</td></tr>
<tr>
<td>
e-time</td><td>
 <img src="icons_images\icons_img50.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-up-arrow</td><td>
 <img src="icons_images\icons_img51.png" alt="" width="12pt" height="12pt"</td></tr>
<tr>
<td>
e-date</td><td>
 <img src="icons_images\icons_img52.png" alt="" width="14pt" height="17pt"</td></tr>
<tr>
<td>
e-datetime</td><td>
 <img src="icons_images\icons_img53.png" alt="" width="16pt" height="18pt"</td></tr>
<tr>
<td>
e-collapse-arrow</td><td>
 <img src="icons_images\icons_img54.png" alt="" width="13pt" height="11pt"</td></tr>
<tr>
<td>
e-expand-arrow</td><td>
 <img src="icons_images\icons_img55.png" alt="" width="12pt" height="14pt"</td></tr>
<tr>
<td>
e-restore</td><td>
 <img src="icons_images\icons_img56.png" alt="" width="16pt" height="19pt"</td></tr>
<tr>
<td>
e-plus</td><td>
 <img src="icons_images\icons_img57.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-minus</td><td>
 <img src="icons_images\icons_img58.png" alt="" width="16pt" height="10pt"</td></tr>
<tr>
<td>
e-handup</td><td>
 <img src="icons_images\icons_img59.png" alt="" width="12pt" height="14pt"</td></tr>
<tr>
<td>
e-clock</td><td>
 <img src="icons_images\icons_img60.png" alt="" width="13pt" height="11pt"</td></tr>
<tr>
<td>
e-cursor</td><td>
 <img src="icons_images\icons_img61.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-hyperlink</td><td>
<img src="icons_images\icons_img62.png" alt="" width="20pt" height="12pt"</td></tr>
<tr>
<td>
e-hyperlinkbreak</td><td>
 <img src="icons_images\icons_img63.png" alt="" width="20pt" height="14pt"</td></tr>
<tr>
<td>
e-settings</td><td>
  <img src="icons_images\icons_img64.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-shoppingcart</td><td>
 <img src="icons_images\icons_img65.png" alt="" width="16pt" height="17pt"</td></tr>
<tr>
<td>
e-palette</td><td>
  <img src="icons_images\icons_img66.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-warningmessage</td><td>
 <img src="icons_images\icons_img67.png" alt="" width="15pt" height="16pt"</td></tr>
<tr>
<td>
e-cut</td><td>
  <img src="icons_images\icons_img68.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-copy</td><td>
 <img src="icons_images\icons_img69.png" alt="" width="14pt" height="17pt"</td></tr>
<tr>
<td>
e-paste</td><td>
 <img src="icons_images\icons_img70.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-edit</td><td>
<img src="icons_images\icons_img71.png" alt="" width="18pt" height="13pt"</td></tr>
<tr>
<td>
e-swapleft</td><td>
 <img src="icons_images\icons_img72.png" alt="" width="16pt" height="15pt"</td></tr>
<tr>
<td>
e-swapright</td><td>
<img src="icons_images\icons_img73.png" alt="" width="16pt" height="15pt"</td></tr>
<tr>
<td>
e-swapup</td><td>
 <img src="icons_images\icons_img74.png" alt="" width="16pt" height="17pt"</td></tr>
<tr>
<td>
e-swapdown</td><td>
<img src="icons_images\icons_img75.png" alt="" width="16pt" height="17pt"</td></tr>
<tr>
<td>
e-zoomin</td><td>
<img src="icons_images\icons_img76.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-zoomout</td><td>
<img src="icons_images\icons_img77.png" alt="" width="16pt" height="17pt"</td></tr>
<tr>
<td>
e-star</td><td>
 <img src="icons_images\icons_img78.png" alt="" width="12pt" height="11pt"</td></tr>
<tr>
<td>
e-home</td><td>
<img src="icons_images\icons_img79.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-clipboard</td><td>
 <img src="icons_images\icons_img80.png" alt="" width="14pt" height="18pt"</td></tr>
<tr>
<td>
e-userlogin</td><td>
 <img src="icons_images\icons_img81.png" alt="" width="15pt" height="14pt"</td></tr>
<tr>
<td>
e-dataexport</td><td>
<img src="icons_images\icons_img82.png" alt="" width="19pt" height="15pt"</td></tr>
<tr>
<td>
e-arrowheadright</td><td>
 <img src="icons_images\icons_img83.png" alt="" width="14pt" height="15pt"</td></tr>
<tr>
<td>
e-arrowheaddown</td><td>
<img src="icons_images\icons_img84.png" alt="" width="13pt" height="14pt"</td></tr>
<tr>
<td>
e-undo</td><td>
 <img src="icons_images\icons_img85.png" alt="" width="13pt" height="15pt"</td></tr>
<tr>
<td>
e-redo</td><td>
<img src="icons_images\icons_img86.png" alt="" width="16pt" height="13pt"</td></tr>
<tr>
<td>
e-bold</td><td>
<img src="icons_images\icons_img87.png" alt="" width="14pt" height="14pt"</td></tr>
<tr>
<td>
e-italic</td><td>
<img src="icons_images\icons_img88.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-underline</td><td>
<img src="icons_images\icons_img89.png" alt="" width="17pt" height="17pt"</td></tr>
<tr>
<td>
e-strikethrough</td><td>
 <img src="icons_images\icons_img90.png" alt="" width="16pt" height="14pt"</td></tr>
<tr>
<td>
e-font</td><td>
<img src="icons_images\icons_img91.png" alt="" width="15pt" height="15pt"</td></tr>
<tr>
<td>
e-rarrowdown</td><td>
 <img src="icons_images\icons_img92.png" alt="" width="11pt" height="13pt"</td></tr>
<tr>
<td>
e-rarrowleft</td><td>
<img src="icons_images\icons_img93.png" alt="" width="16pt" height="15pt"</td></tr>
<tr>
<td>
e-rarrowup</td><td>
<img src="icons_images\icons_img94.png" alt="" width="14pt" height="11pt"</td></tr>
<tr>
<td>
e-rarrowright</td><td>
<img src="icons_images\icons_img95.png" alt="" width="14pt" height="16pt"</td></tr>
<tr>
<td>
e-calender</td><td>
 <img src="icons_images\icons_img96.png" alt="" width="14pt" height="17pt"</td></tr>
<tr>
<td>
e-save</td><td>
<img src="icons_images\icons_img97.png" alt="" width="17pt" height="16pt"</td></tr>
</table>


