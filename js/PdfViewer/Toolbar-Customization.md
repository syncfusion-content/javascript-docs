---
layout: post
title: Toolbar customization of Syncfusion Essential JS PDF viewer.
description: Toolbar customization of Syncfusion Essential JS PDF viewer.
platform: js
control: PDF viewer
documentation: ug
keywords: ejPdfViewer
api: /api/js/ejpdfviewer
---

## Toolbar Customization

**Customizing default toolbar**

The default toolbar is grouped into the following set of tools.
<table>
<tr>
<td>
{{'**MagnificationTools**'| markdownify }}
</td>
<td>
Contains ZoomIn, ZoomOut, Zoom, FitPage and FitWidth tools
</td>
</tr>
<tr>
<td>
{{'**NavigationTools**'| markdownify }}
</td>
<td>
Contains GoToFirst, GoToLast, GoToNext and GoToLast tools
</td>
</tr>
<tr>
<td>
{{'**PrintTools**'| markdownify }}
</td>
<td>
Contains print tool.
</td>
</tr>
<tr>
<td>
{{'**DownloadTool**'| markdownify }}
</td>
<td>
Contains download tool
</td>
</tr>
</table>

The ejPdfViewer has an option to show or hide these grouped items in the default toolbar.  You can hide/display any of these tools by using the toolbarSettings property.
The below code snippet describes how to hide the magnification tools in the widget.

{% highlight javascript %}
$(function () {
            var obj = $("#container").ejPdfViewer({serviceUrl: "/api/PdfViewerAPI", toolbarSettings: {toolbarItems : ~ej.PdfViewer.ToolbarItems.MagnificationTools}});
        });
{% endhighlight %}

**Adding Custom toolbar**

The toolbar can be customized as per the application’s needs, by hiding the existing toolbar.
Hide the default toolbar of the ejPdfViewer, by using the below code snippet.

{% highlight javascript %}
$(function () {
$("#container").ejPdfViewer({serviceUrl: "/api/PdfViewerAPI"}).data("ejPdfViewer").showToolbar(false);
});
{% endhighlight %}

The below code snippet shows how to create a customer toolbar by using the client side APIs.

{% highlight html %}
<body>
  <div id="container" onmousemove="mousemovefunction(event)" style="width: 100%; height: 680px;"></div>
        <!--"-->
        <div id="magnificationDiv" class="toolbarclass" role="toolbar">
            <div class="round-button-circle" style=" position:absolute;top:20px;">
                <div class=" e-pdfviewer-customtoolbar-print "onclick=" callClientSideMethod('print')"></div>
            </div>
              <div class="round-button-circle" style=" position:absolute;top:70px;">
                <div class=" e-pdfviewer-customtoolbar-download "onclick=" callClientSideMethod('download')"></div>
            </div>
            <div class="round-button-circle" style=" position:absolute;top:120px;">
                <div class=" e-pdfviewer-customtoolbar-zoomin "  onclick=" callClientSideMethod('zoomin')"></div>
            </div>
            <div class="round-button-circle" style="position:absolute;top:170px;">
                <div class="  e-pdfviewer-customtoolbar-zoomout "  onclick="callClientSideMethod('zoomout')"></div>
            </div>
            <div class="round-button-circle" style="position:absolute;top:220px;">
                <div class=" e-pdfviewer-customtoolbar-fitpage "  onclick="callClientSideMethod('fitpage')"></div>
            </div>
            <div class="round-button-circle" style="position:absolute;top:270px;">
                <div class=" e-pdfviewer-customtoolbar-fitwidth "  onclick="callClientSideMethod('fitwidth')"></div>
            </div>
        </div>
        <div id="toolbarDiv" class="toolbarclass " role="toolbar" style="background-color:#c8c8c8;width:98.5%;">
            <div style="padding:10px;float:left">
                <span id="pdfName"></span>
            </div>
            <div style ="left:45%;position:absolute;padding:5px;">
                <table>
                <tr>
                    <td style="width:34px;"><div class=" round-button-circle"><div class=" e-pdfviewer-customtoolbar-previous " onclick=" callClientSideMethod('previous')"></div></div></td>
                    <td><input id="currentPage" class="e-pdfviewer-pagenumber" type="text" value="1" data-role="none" onclick="textboxOnclick(event)" onkeypress="goToPage(event)" style="background-color:#c8c8c8;border:#c8c8c8;font-size:16px;margin:-5px;"></td>
                    <td style="width:20px;"><span id="totalPageCount"></span></td>
                    <td><div class=" round-button-circle"><div class=" e-pdfviewer-customtoolbar-next " onclick=" callClientSideMethod('next')"></div></div></td>
                </tr>
                </table>
            </div>
        </div>
        <script type="text/javascript">
            $(function () {
                $("#container").ejPdfViewer({serviceUrl: "/api/PdfViewerAPI", pageChange: "pageChange" }).data("ejPdfViewer").showToolbar(false);
            });
            var isTextFieldInFocus = false;
            var mousePosX, mousePosY, height, width;
            var currentPage = 1;
            var toolbarInView = false;
            height = parseInt(document.getElementById("container").style.height);
            width = window.innerWidth;
            showCustomToolbar();
            function mousemovefunction(args) {
               mousePosX = args.clientX;
               mousePosY = args.clientY;
                if (!toolbarInView) {
                    if ((mousePosY < height - 400 && mousePosX < 200) || (mousePosY <= 70 && mousePosX <= width)) {
                        showCustomToolbar();
                    }
                    else {
                    }
                }
            }
            function showCustomToolbar() {
                $("#magnificationDiv").css({ left: 0, "position": "absolute", "display": "block", "height": 300 + "px", "top": (height - 600) + "px" }).animate({ "left": 100 + "px" }, "slow");
                $("#toolbarDiv").css({ left: 0, "top": 0 + "px", "position": "absolute" }).animate({ "height": 40 + "px", top: 0 }, "slow");
                toolbarInView = true;
            }
            function hideCustomToolbar() {
                $("#toolbarDiv").css({ height: 40 + "px" }).animate({ "top": -40 + "px" }, "slow");
                $("#magnificationDiv").css({ left: 100 + "px" }).animate({ "left": -50 + "px" }, "slow");
                toolbarInView = false;
            }
            setInterval(function () { hideToolbar() }, 5000);
            function hideToolbar() {
                if (((mousePosY < height - 400 && mousePosX < 200) || (mousePosY <= 70 && mousePosX <= width))) {
                } else {
                    if ((toolbarInView) && (!isTextFieldInFocus)) {
                        hideCustomToolbar();
                    }
                }
            }
            function callClientSideMethod(apiName) {
                var obj = $("#container").data("ejPdfViewer");
                switch (apiName) {
                    case 'zoomin':
                        obj.zoomIn();
                        break;
                    case 'zoomout':
                        obj.zoomOut();
                        break;
                    case 'fitpage':
                        obj.fitToPage();
                        break;
                    case 'fitwidth':
                        obj.fitToWidth();
                        break;
                    case 'previous':
                        obj.goToPreviousPage();
                        break;
                    case 'next':
                        obj.goToNextPage();
                        break;
                    case 'print':
                        obj.print();
                        break;
                    case 'download':
                        obj.download();
                        break;
                }
            }
            function pageChange(args) {
                $("#currentPage").val(args.currentPageNumber);
                currentPage = document.getElementById("currentPage").value;
            }
            $(function () {
                var obj = $("#container").data("ejPdfViewer");
                var pagecount = obj.pageCount;
                $("#totalPageCount").html("/" + pagecount);
                var filename = (obj.fileName).split("\\");
                var pdf = filename[filename.length - 1];
                $("#pdfName").html(pdf);
            });
            function goToPage(event) {
                var obj = $("#container").data("ejPdfViewer");
                if (event.keyCode == 13) {
                    try {
                        var val = parseInt($(event.currentTarget).val());
                        if (val > 0 && val <= obj.pageCount)
                            obj.goToPage(val);
                        else
                            $(event.currentTarget).val(currentPage);
                    } catch (err) {
                    }
                }
            }
            function textboxOnclick(event) {
                if (event.target.id == "currentPage")
                    $('#currentPage').select();
            };
            $('#currentPage').keypress(function (event) {
                if ((event.which < 48 || event.which > 57) && event.which != 8 && event.which != 13) {
                    return false;
                }
                else {
                    return true;
                }
            });
            $("#currentPage").focusin(function () {
                isTextFieldInFocus = true;
                var $this = $(this);
                 $this.select();
                 window.setTimeout(function () {
                    $this.select();
                }, 1);
                  function mouseUpHandler() {
                    $this.off("mouseup", mouseUpHandler);
                    return false;
                }
                $this.mouseup(mouseUpHandler);
            });
            $("#currentPage").focusout(function () {
                isTextFieldInFocus = false;
            });
        </script>
        <style>
            .round-button-circle {
                width: 30px;
                height: 30px;
                border-radius: 50%;
                background-color: #c8c8c8;
                /*overflow: hidden;*/
            }
            .round-button-circle:hover {
                    background: #86cbea;
            }         
    .e-pdfviewer-customtoolbar-zoomin:before{
      content: url('../images/pdfviewer/CustomToolbarImages/zoomin.png');
          }
    .e-pdfviewer-customtoolbar-zoomout:before{
      content: url('../images/pdfviewer/CustomToolbarImages/zoomout.png');
        }
    .e-pdfviewer-customtoolbar-previous:before{
        content: url('../images/pdfviewer/CustomToolbarImages/previous.png');
        }
    .e-pdfviewer-customtoolbar-next:before{
        content: url('../images/pdfviewer/CustomToolbarImages/next.png');
        }
    .e-pdfviewer-customtoolbar-fitwidth:before{
        content: url('../images/pdfviewer/CustomToolbarImages/fitwidth.png');
        }
    .e-pdfviewer-customtoolbar-print:before{
        content: url('../images/pdfviewer/CustomToolbarImages/print.png');
        }
    .e-pdfviewer-customtoolbar-download:before{
        content: url('../images/pdfviewer/CustomToolbarImages/download.png');
        }

    .e-pdfviewer-customtoolbar-fitpage:before{
        content: url('../images/pdfviewer/CustomToolbarImages/fitpage.png');
        }
    </style>
</body>
{% endhighlight %}


N> Ensure the icon images available in the referred location for the custom toolbar.

Run the sample. You can view the ejPdfViewer with custom toolbar.
