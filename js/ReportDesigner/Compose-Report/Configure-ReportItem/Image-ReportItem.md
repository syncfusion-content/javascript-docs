---
layout: post
title: Image report item with Syncfusion Web Report Designer
description: How to add image report item with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---
# Image

An image report item contains a reference to an image that is embedded in the report or stored in a database.

## Adding Image to the Report

1. To add an image to the report, **Image** report item can be used.

2. Drag and drop an image report item from item panel to the design area. You can add an image report item to header, footer and body of the report.

    ![](Image-ReportItem/Image-Drag.png)

3. Click on the `Properties` icon in the configuration panel. Now, an image report item properties will be displayed like below.

    ![](Image-ReportItem/Image-Properties.png)

    * **Basic Settings** : 

        ![](Image-ReportItem/Basic-settings.png)

        * **Source** : 

            ![](Image-ReportItem/Source-Dropdown.png)

            * **External Image** : Include stored images in a report by specifying a URL to an image.

                ![](Image-ReportItem/External-Image.png)

            * **Embedded Image** : Using this property, you can add an image from the embedded images list in the report.

                To know how to embed an image, see [Embed Image](/js/ReportDesigner/Image-Manager/Add-image)

                Now, an embedded images in the report will be listed in the value dropdown.

                ![](Image-ReportItem/Value-Dropdown.png)

                Select an image from the list to design the report.

                ![](Image-ReportItem/Embed-Snap.png)

            * **Database Image** : Specify an image that is stored in a database.

                ![](Image-ReportItem/Database-Image.png)

                * In the source field choose **Database**.

                * In the value field dropdown, choose the field that contains images. For example, `=First(Fields!LargePhoto.Value,"Dataset1")`.

                ![](Image-ReportItem/Value-Database.png)

                * In the MIME type choose the file format.

                ![](Image-ReportItem/Database-Value.png)

    * **Sizing** : To set the display size of an image.

        * **AutoSize** : 

            ![](Image-ReportItem/Size-Auto.png)

            ![](Image-ReportItem/AutoSize-Output.png)

        * **Fit** : 

            ![](Image-ReportItem/Size-Fit.png)

            ![](Image-ReportItem/Size-Fit-Output.png)

        * **FitProportional** : 

            ![](Image-ReportItem/Size-FitProp-Option.png)

            ![](Image-ReportItem/Size-FitProp.png)

        * **Clip** : 

            ![](Image-ReportItem/Size-Clip.png)

            ![](Image-ReportItem/Size-Clip-Option.png)

    * **Position**: You can change an image size and position under this category.  

        ![](Image-ReportItem/Image-Position.png)
    
        * **Position** : To adjust the position of an image in the designer area.

        * **Size** : To adjust the height and width of an image.

        You can also achieve the above behavior with the resizer.

    * **Visibility**: Select this option to indicate how the report item is initially displayed in the report.

        ![](Image-ReportItem/Visibility.png)

        * Enable  the checkbox to show an image report item.
        * Disable the checkbox to hide an image report item.
        * Show or hide based on an expression

        Click on the icon in the right corner and select **Expression** to edit an expression.

        ![](Image-ReportItem/Visibility2.png)


