---
layout: post
title: Essential Theme Studio for JavaScript
description: Essential Theme Studio for JavaScript
platform: js
control: General Topics 
documentation: ug
---

# Overview

Essential [Theme Studio](http://js.syncfusion.com/themestudio/) for JavaScript allows us to build a new theme based on an existing themes for Syncfusion Essential JavaScript controls except Data visualization controls like Chart, Diagram, Gauge, Range Navigator, Barcode, Maps. Also, you can import your customized theme into the Theme studio and customize the colors and download.

## How to create a new theme based on existing built-in themes?

**Step 1:**

  You can make use of built-in themes in theme studio. In that, you can choose the built-in theme as Flat-Azure theme under the `Personalize` menu and customize theme based on your application.  

You can apply Flat-Azure theme as shown below,

![](/js/ThemeStudio_images/Built-In-Themes.png)


**Step 2:**

The following options of the control can be customized.

* Header

* Content

* Default State

* Hover State

* Active State

* Miscellaneous

![](/js/ThemeStudio_images/Customization.png)

**Step 3:**

Essential Theme Studio for JavaScript provides a `Filter` option to customize theme for the specific controls. In this, you can filter the Dialog control and customize theme of it. 

You can find the filter option in theme studio as shown below:

![](/js/ThemeStudio_images/Filter-01.png)

![](/js/ThemeStudio_images/Filter-02.png)

![](/js/ThemeStudio_images/Filter-03.png)

**Step 4:**

Once you customize the theme for the Dialog control, then you can download the customized theme files directly through the `Download` option in theme studio.
 
You can find the Download option in theme studio as shown below:

![](/js/ThemeStudio_images/Download-01.png)

![](/js/ThemeStudio_images/Download-02.png)

In the Download dialog popup provide a name to the file to be generated. Once the Download button is clicked, it will download the customized theme files. The downloaded theme files consist as follows:

<table>
<tr>
<th>Files<br/><br/></th>
<th>Details<br/><br/></th>
</tr>
<tr>
<td>
ej.theme.less<br/><br/></td><td>
You can manually change the color code in this less file and generate the css by using less to CSS generator.<br/><br/></td>
</tr>
<tr>
<td>properties.json<br/><br/></td>
<td>It contains the configuration of the customized theme. You can reuse the customized theme by importing this file in theme studio and customize the theme further.<br/><br/></td>
</tr>
<tr>
<td>ej.theme.min.css,ej.widgets.core.min.css<br/><br/></td>
<td>It’s used for production purpose.<br/><br/></td>
</tr>
<tr>
<td>ej.theme.css,ej.widgets.core.css<br/><br/></td>
<td>It’s used for development purpose.<br/><br/></td>
</tr>
</table>



Downloaded theme file is in the below structure:

![](/js/ThemeStudio_images/Download-03.png)

You can refer these customized unminified/minified theme files to display the Dialog control in your application.

N> You can filter multiple desired controls and customize their theme as per your needs. Then download the corresponding customized theme files.

## How to import our own customized theme to Theme Studio?

**Step 1:**

Our own customized theme of the Dialog control can be again customized by using this `Import` option in theme studio. 

You can find the import option in theme studio as shown below:

![](/js/ThemeStudio_images/Import-01.png)

![](/js/ThemeStudio_images/Import-02.png)

**Step 2:**

Import **properties.json** file which is customized theme of Dialog control earlier as shown below:

![](/js/ThemeStudio_images/Import-03.png)

**Step 3:**

You can display the Dialog control which is applied the customized theme of Dialog control by importing the properties.json file.

![](/js/ThemeStudio_images/Import-04.png)

Now, you can customize the Dialog control with your desired theme as shown below:

![](/js/ThemeStudio_images/Import-05.png)

**Step 4:**

After customizing theme, you can export or download the customized theme files.

![](/js/ThemeStudio_images/Import-06.png)