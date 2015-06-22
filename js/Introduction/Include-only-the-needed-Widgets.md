---
layout: post
title: Include-only-the-needed-Widgets
description: include only the needed widgets
platform: js
control: Introduction
documentation: ug
---

# Include only the needed Widgets

The users with **Essential Studio Enterprise license** or **Essential Studio for JavaScript license** can make use of the **Custom Script Generator** (CSG) tool to create a single file that packs together only the required scripts and css files together. Referring only the required scripts and stylesheets in your application instead of the default **ej.web.all.js** (which combines the scripts of all the widgets) file, will enhance the performance of the application’s loading time. This utility can be used to generate both the minified and non-minified version of the scripts and CSS files.

## Getting Started with Custom Script Generator

Log into the online CSG [link](http://csg.syncfusion.com/) with your **DirectTrac** credentials. The Custom Script Generator Utility options within the **Desktop** tab will be displayed as shown below,
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img1.png" Caption="Custom Script Generator utility options"%}

Select the required version from the **Version** list and also select the output file type either to be generated as a **minified** or **non-minified** version. Now, click on the Generate button and provide a name to the file to be generated as shown below,
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img2.png" %}

Once the Generate button is clicked, the combining process of selected scripts is executed and this will take several minutes. When the process is done, the **Download** button will become available through which you can download the requested files combined and make use of it in your application as per your needs.
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img3.png" %}


>   **Note**: It is not necessary to sit idle for a long time, you can simply close the above information and proceed with your work, as an e-mail alert with the Custom script downloadable link will be sent to you automatically.


## Settings Customization

### Save the Custom Settings

You can save the frequently used controls to generate custom Script and CSS files, instead of selecting the controls every time. To do this, 

Select the required list of controls, version, output file-type (either minified or non-minified versions) and then click on the **Save Settings** button. Provide a meaningful name to the file and click on the **Save** button.
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img4.png" Caption="Saving the frequently used Custom settings"%}

### Generating the Scripts and CSS from an existing Saved Settings

The steps given below are to be followed, to perform custom Script and CSS file generation using the existing saved settings,

Navigate to the **Settings** Page through the **Settings** option (marked in the below image) as shown below,
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img5.png" %}

Now click on the **Proceed** **icon** to request for the Custom script and css file generation for the required controls.
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img6.png" %}

### Editing and Deleting the Saved Settings

You can also modify or delete the existing controls by making use of the **edit** or **delete** icons.

If you need to edit the settings, click on the **edit** **icon** as shown in the below image, and make the further required changes in the control selection page that appears and then again click on the **Save Settings** button to update the modified one.
{% include image.html url="/js/Introduction/Include-only-the-needed-Widgets_images/Include-only-the-needed-Widgets_img7.png" %}

To delete the unwanted or unused settings, you can make use of the **delete** **icon** in the above image just by clicking on it.

