---
layout: post
title: drag-and-drop-support
description: drag and drop support
platform: js
control: Uploadbox
documentation: ug
---

# Drag and Drop Support

The **UploadBoxUploadbox** control provides the drag and drop support. You can simply drag-and-drop files, directly from the computer and can be dropped into the droppable area. A list of files can be dragged and dropped when you enable the **multipleFilesSelection**.

The following screenshot displays the drag and drop support.



{% include image.html url="\js\UploadBox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img1.png" Caption="Figure 128: Drag and drop the files"%}

## Enable drag and drop 

You can enable or disable drag and drop by using the **allowDragAndDrop** property. By default the **allowDragAndDrop** property is set as **False** in the **UploadBoxUploadbox** control. You can enable drag and drop by setting the **allowDragAndDrop** property as **True**. When you want to drag and drop multiple files, you can enable multiple file selection by setting **multipleFilesSelection** as **True** in the****UploadBoxUploadbox****control.

The following steps explain how to enable the drag and drop in the **UploadBoxUploadbox** control.

* In the **HTML** page, add a **&lt;div&gt;** element to enable the drag and drop in UploadBoxUploadbox control.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="frame"&gt;     &lt;div class="control"&gt;            &lt;div id="Uploadbox"&gt;&lt;/div&gt;       &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the <b>UploadBox</b> by using the following code example.&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Uploadbox").ejUploadbox({                saveUrl: "http://js.syncfusion.com/demos/web/uploadbox/saveFiles.ashx",                removeUrl: "http://js.syncfusion.com/demos/web/uploadbox/removeFiles.ashx",                <b>allowDragAndDrop</b>: true,                multipleFilesSelection: true            });        }); &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the following code example to the corresponding **CSHTML** page to render UploadBox with drag and drop support



&lt;div class="frame"&gt;

          &lt;div class="control"&gt;                @Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("UploadBox/Remove").**AllowDragAndDrop(true).MultipleFilesSelection(true)**

               &lt;/div&gt;

  &lt;/div&gt;





To know about file action, refer to the following link: [http://help.syncfusion.com/ug/js/default.htm#!documents/fileactions.htm](http://help.syncfusion.com/ug/js/default.htm)

* In CSS, configure the custom styles for drag and drop.

{% highlight css %}

**[CSS]**
<style>
        .frame {
            width: 500px;
            height: 100px;
            margin-top: 10%;
        }

        .control {
            width: 100%;
            height: 100%;
        }
  </style>


{% endhighlight %}



* The following screenshot displays the output for the above code.

{% include image.html url="\js\UploadBox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img2.png" Caption="Figure 129: Enable the drag and drop"%}

## Drag Area text

You can change the drag area text by using the **dragAreaText** property.  By default, the **dragAreaText** (string) property is **Drop files or click to upload** in the UploadBoxUploadbox control.

* In the **HTML** page, add a **&lt;div&gt;** element to enable the drag and drop in the **UploadBoxUploadbox** control.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="frame"&gt;     &lt;div class="control"&gt;            &lt;div id="Uploadbox"&gt;&lt;/div&gt;       &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the UploadBox using the following code example.&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Uploadbox").ejUploadbox({                saveUrl: "http://js.syncfusion.com/demos/web/uploadbox/saveFiles.ashx",                removeUrl: "http://js.syncfusion.com/demos/web/uploadbox/removeFiles.ashx",                allowDragAndDrop: true,                <b>dragAreaText:"Drop files here",</b>                multipleFilesSelection: true            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** Add the following code example to the corresponding **CSHTML** page to render UploadBox with drag and drop support



&lt;div class="frame"&gt;

                      &lt;div class="control"&gt;                        @Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").AllowDragAndDrop(true).MultipleFilesSelection(true).**DragAreaText("Drop files here")**

                      &lt;/div&gt;

&lt;/div&gt;



* In CSS, configure the custom styles for drag and drop.

{% highlight css %}

**[CSS]**
<style>
        .frame {
            width: 500px;
            height: 100px;
            margin-top: 10%;
        }

        .control {
            width: 100%;
            height: 100%;
        }
  </style>


{% endhighlight %}



*  The following screenshot displays the output for the above code.

{% include image.html url="\js\UploadBox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img3.png" Caption="Figure 230: Drag area text"%}

## Adjust Drop area size

The **UploadBoxUploadbox** control provides the ability to change or adjust the drop area size. The **dropAreaHeight and****dropAreaWidth** properties in the **UploadBoxUploadbox** control allows you to set the maximum height and maximum width for the drop area. The value set to this property is string****or****number type.

The following steps explain you on how to adjust the Drop Area Size.

* In the **HTML** page, add a **&lt;div&gt;** element to enable the drag and drop in **UploadBoxUploadbox** control.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;     &lt;div id="Uploadbox"&gt;&lt;/div&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the UploadBoxUploadbox using the following code example.    &lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Uploadbox").ejUploadbox({                saveUrl: "http://js.syncfusion.com/demos/web/uploadbox/saveFiles.ashx",                removeUrl: "http://js.syncfusion.com/demos/web/uploadbox/removeFiles.ashx",                allowDragAndDrop: true,                multipleFilesSelection: true,	<b>         dropAreaHeight:"300px",</b><b>	         dropAreaWidth:"600px" </b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**//** Add the following code example to the corresponding **CSHTML** page to render UploadBox with drag and drop support.



&lt;div class="frame"&gt;

                      &lt;div class="control"&gt;

                          @Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").AllowDragAndDrop(true).MultipleFilesSelection(true).**DropAreaHeight("300px").DropAreaWidth("600px")**

                      &lt;/div&gt;

                  &lt;/div&gt;



* The following screenshot displays the output for the above code.

{% include image.html url="\js\UploadBox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img4.png" Caption="Figure 231: Adjusting drop area size"%}

## Drop area with Browse button behavior

You can click anywhere in the droppable area to browse and upload the files. The droppable area behaves like a browse button.

### Droppable area behavior

Enable the **allowDragAndDrop** property to achieve this feature. Next, set the **showBrowseButton** as **False** in UploadBoxUploadbox Control.

The following steps explains the droppable area containing the browse button behavior

* In the **HTML** page, add a **&lt;div&gt;** element to enable drag and drop in the **UploadBoxUploadbox** control.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="frame"&gt;     &lt;div class="control"&gt;            &lt;div id="Uploadbox"&gt;&lt;/div&gt;       &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the UploadBoxUploadbox by using the following code example.&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Uploadbox").ejUploadbox({                saveUrl: "http://js.syncfusion.com/demos/web/uploadbox/saveFiles.ashx",                removeUrl: "http://js.syncfusion.com/demos/web/uploadbox/removeFiles.ashx",                <b>allowDragAndDrop</b>: true,                <b>showBrowseButton:false</b>,                multipleFilesSelection: true            });        }); &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the following code example to the corresponding **CSHTML** page to render UploadBox with drag and drop support.



  &lt;div class="frame"&gt;

                      &lt;div class="control"&gt;                      @Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").AllowDragAndDrop(true).MultipleFilesSelection(true).**ShowBrowseButton(false)**

                      &lt;/div&gt;

    &lt;/div&gt;           



* In CSS, configure the custom styles for drag and drop.

{% highlight css %}

**[CSS]**
<style>
        .frame {
            width: 500px;
            height: 100px;
            margin-top: 10%;
        }

        .control {
            width: 100%;
            height: 100%;
        }
  </style>


{% endhighlight %}



* The following screenshot displays the output for the above code.



{% include image.html url="\js\UploadBox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img5.png" Caption="Figure 3222: Droppable area behavior"%}

