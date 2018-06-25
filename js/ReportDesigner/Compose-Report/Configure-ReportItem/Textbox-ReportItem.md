---
layout: post
title: Textbox to design a report with Syncfusion Web Report Designer
description: How to use textbox to design a report with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# TextBox

To display static text for titles, highlight key information, descriptions and labels or dynamic text based on expressions textbox can be used.

## To add textbox

 Drag and drop the `Textbox` from the item panel.

![](Textbox-images/Textbox-Drag.png)

You can add textbox in header, footer, and body area.

![](Textbox-images/Multiple-Textbox.png)

## Add effects to the textbox

To edit the textbox, place the cursor inside the textbox.

![](Textbox-images/Textbox-Edit.png)

To add effects focus on the textbox, click the `Properties` icon in the configuration panel.

![](Textbox-images/Properties-Icon.png)

You can add effects to 
   
* The overall textbox element.

  ![](Textbox-images/Textbox-Properties.png)

* Each words in a content.

  ![](Textbox-images/Textbox-Selectedtext.png)

  To switchover from selected text properties to textbox properties, click the `Move` icon.

  ![](Textbox-images/Switch-Move-icon.png)

**Basic settings**

![](Textbox-images/BasicSettings-Field.png)

* **Font family**: 

    You can select the font family of the text.

    ![](Textbox-images/Font-Family.png)

  > Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/report-platform/ReportDesigner/Web/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

* **Font color**:

   Click the color palette icon to open the `Color Palette`. You can select the font color of the text.

   ![](Textbox-images/Color-Palette.png)

* **Font size**:

   Click the up/down arrow to increase/decrease the font size.

   ![](Textbox-images/Font-Size.png)

* **Font style**:

   Click the drop-down list to set the font style of the text.

   * Default
   * Normal
   * Italic

   ![](Textbox-images/FOnt-Style.png)

* **Text decoration**:

   ![](Textbox-images/Text-Decoration.png)
   
   To remove text decoration, select `None` from the drop-down list.

 **Format**: You can set format to the text using the **Format** property.

  ![](Textbox-images/Format-Textbox.png)
  
Click the highlighted button in the above image to open `Format` dialog.

To demonstrate an example, here **Currency** format is applied to the text run.

![](Textbox-images/Apply-Format.png)

Refer [Format Data](/js/ReportDesigner/Compose-Report/Format-Data) section for more details on how to format data.

**Alignment**

![](Textbox-images/Textbox-Alignment.png)

* **Text alignment**:

   **Center**

     ![](Textbox-images/Center-ALignment.png)

   **Left**

    ![](Textbox-images/Left-Alignment.png)

   **Right**

    ![](Textbox-images/Right-Alignment.png)

   To remove alignment, set text alignment as **Default**.

 * **Vertical alignment**:

     **Top**

    ![](Textbox-images/Top-Alignment.png)

      **Middle**

      ![](Textbox-images/Middle-Alignment.png)

      **Bottom**
           
      ![](Textbox-images/Bottom-Alignment.png)

    To remove alignment, set vertical alignment as **Default**.

  * **Padding**: Click the up/down arrow to increase/decrease the  text padding.
    
    ![](Textbox-images/Padding-Alignment.png)

**Appearance**: Set the background color, border style, and border width using the appearance property.

  ![](Textbox-images/Appearance.png)

  ![](Textbox-images/Appearance-Textbox.png)

**Enable Link**: You can add link or file path in the text using this property. 

To define a hyperlink, or a drill through action to the textbox refer [Link Data](/js/ReportDesigner/Compose-Report/Link-Data).

  ![](Textbox-images/EnableLink-URL-Save.png)

On report **Preview** action:

  ![](Textbox-images/Enable-Link-URLGrid.png)

Click the `www.syncfusion.com` text will open the link in new tab of the browser.

**Position**: You can change the textbox size and position under this category.  

![](Textbox-images/Position.png)
    
   * **Position** : To adjust the position of the textbox in the designer area.

   * **Size** : To adjust the height and width of the textbox.

You can also achieve the above behavior with the resizer.

**Visibility**: Select this option to indicate how the report item is initially displayed in the report.

![](Textbox-images/Visibility.png)

* Enable  the checkbox to show the report item.
* Disable the checkbox to hide the report item.
* Show or hide based on an expression

Click on the icon in the right corner and select **Expression** to edit the expression.

![](Textbox-images/Visibility2.png)

**Miscellaneous**

![](Textbox-images/Miscellenous.png)

 **Can Grow**: Enabling this property will increase the **Textbox Height** based on the **Text Height** while previewing the text.

**Can Shrink**: Enabling this property will shrink the text inside the **Textbox Height** while previewing the text.

   * Disable Can Grow

      ![](Textbox-images/Can-Grow-disableField.png)

      ![](Textbox-images/Can-Grow-disable.png)

      **On preview**:

        ![](Textbox-images/Preview-CanGrow.png)

  * Enable Can Grow

      ![](Textbox-images/Can-Grow-enable.png)

      **On preview**:

      ![](Textbox-images/Preview-CanGrowEnable.png)

 

