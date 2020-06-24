---
layout: post
title: Toolbar customization of Syncfusion Essential JS PDF viewer.
description: Learn here about toolbar customization in Syncfusion Essential JS PDF Viewer control and more details.
platform: js
control: PDF viewer
documentation: ug
keywords: ejPdfViewer
api: /api/js/ejpdfviewer
---

# Toolbar Customization in Javascript PdfViewer

**Customizing default toolbar**

The default toolbar is grouped into the following set of tools.
<table>
<tr>
<td>
{{'**MagnificationTools**'| markdownify }}
</td>
<td>
Contains ZoomIn, ZoomOut, Zoom, FitPage, and FitWidth tools.
</td>
</tr>
<tr>
<td>
{{'**NavigationTools**'| markdownify }}
</td>
<td>
Contains GoToNext and GoToPrevious tools.
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
Contains download tool.
</td>
</tr>
<tr>
<td>
{{'**TextSearchTool**'| markdownify }}
</td>
<td>
Contains text search tool.
</td>
</tr>
<tr>
<td>
{{'**TextMarkupAnnotationTools**'| markdownify }}
</td>
<td>
Contains text markup annotation tools.
</td>
</tr>
<tr>
<td>
{{'**SignatureTool**'| markdownify }}
</td>
<td>
Contains signature tool.
</td>
</tr>
<tr>
<td>
{{'**SelectionTool**'| markdownify }}
</td>
<td>
Contains selection tool.
</td>
</tr>
</table>

The ejPdfViewer control has an option to show or hide these grouped items in the default toolbar. You can hide or display any of these tools by using the [toolbarSettings](https://help.syncfusion.com/api/js/ejpdfviewer#members:toolbarsettings "toolbarSettings property") property. The following code snippet describes how to show the magnification tools in the widget.

{% highlight javascript %}
$(function () {
    var obj = $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", toolbarSettings: {toolbarItems : ej.PdfViewer.ToolbarItems.MagnificationTools}});
});
{% endhighlight %}

The ejPdfViewer control also has an option to show or hide the complete default toolbar. You can achieve this by using the [showToolbar(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showtoolbar "showToolbar method") method. The following code snippet describes how to hide the default toolbar in the widget.

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).showToolbar(false);
{% endhighlight %}

### Magnification tools

The magnification tools of the ejPdfViewer contain ZoomIn, ZoomOut, Zoom, FitPage, and FitWidth tools in the default toolbar. The ejPdfViewer control also has an option to show or hide the magnification tools in the default toolbar. You can achieve this by using the [showMagnificationTools(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#showmagnificationtoolsshow "showMagnificationTools method") method. The following code snippet describes how to hide the magnification tools in the default toolbar in the widget.

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).showMagnificationTools(false);
{% endhighlight %}

**APIs available for Magnification tools**

fitToPage()

You can fit the page size of the PDF document loaded in the ejPdfViewer control using the [fitToPage()](https://help.syncfusion.com/api/js/ejpdfviewer#fittopage "fitToPage method") method. 
 
{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).fitToPage();
{% endhighlight %}

fitToWidth()

You can fit the page width of the PDF document loaded in the ejPdfViewer control using the [fitToWidth()](https://help.syncfusion.com/api/js/ejpdfviewer#fittowidth "fitToWidth method") method. 

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).fitToWidth();
{% endhighlight %}

zoomIn()

You can zoom the PDF document page loaded in the ejPdfViewer control using [zoomIn()](https://help.syncfusion.com/api/js/ejpdfviewer#zoomin "zoomIn method") method. The maximum zoom percentage is 400%.

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).zoomIn();
{% endhighlight %}

zoomOut()

You can zoom out the PDF document page loaded in the ejPdfViewer control using the [zoomOut()](https://help.syncfusion.com/api/js/ejpdfviewer#zoomout "zoomOut method") method. The minimum zoom percentage is 50%.

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).zoomOut();
{% endhighlight %}

zoomTo(zoomValue)

The PDF document page loaded in the PDF viewer control can be zoomed to a specific value using the [zoomTo(zoomValue)](https://help.syncfusion.com/api/js/ejpdfviewer#zoomtozoomvalue "zoomTo method") method.

{% highlight javascript %}
$(“#container).data(“ejPdfViewer”).zoomTo(154);
{% endhighlight %}

zoomPercentage

The [zoomPercentage](https://help.syncfusion.com/api/js/ejpdfviewer#zoompercentage-number "zoomPercentage property") property of the PDF viewer control returns the current zoom value of the PDF document.

{% highlight javascript %}
    var pdfviewer = $("#container").data(“ejPdfViewer”);
    var zoomValue = pdfviewer. zoomPercentage;
{% endhighlight %}

zoomChange

When the zoom value of the PDF document is changed using the magnification tools, the zoomChange event will be triggered. We can define the event method using the [zoomChange](https://help.syncfusion.com/api/js/ejpdfviewer#zoomchange "zoomChange Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", zoomChange: "zoomChanged" });
});
function zoomChanged(args) {
    alert("The magnification changes from " + args.previousZoomPercentage + " to" + args.currentZoomPercentage);
}
{% endhighlight %}

### Navigation Tools

The navigation tools of the PDF viewer contain GoToNext, GoToPrevious, and current page number tools in the default toolbar. The PDF viewer control also has an option to show or hide the navigation tools in the default toolbar. You can achieve this by using the [showPageNavigationTools(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#showpagenavigationtoolsshow "showPageNavigationTools method") method. The following code snippet describes how to hide the navigation tools in the default toolbar in the widget.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showPageNavigationTools(false);
{% endhighlight %}

**APIs available for Navigation Tools**

goToPreviousPage()

The previous page of the PDF document from the current page can be navigated in the ejPdfViewer using [goToPreviousPage()](https://help.syncfusion.com/api/js/ejpdfviewer#gotopreviouspage "goToPreviousPage method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).goToPreviousPage();
{% endhighlight %}

goToNextPage()

The next page of the PDF document from the current page can be navigated in the ejPdfViewer using the [goToNextPage()](https://help.syncfusion.com/api/js/ejpdfviewer#gotonextpage "goToNextPage method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).goToNextPage();
{% endhighlight %}

goToFirstPage()

The first page of the PDF document can be navigated in the ejPdfViewer using the [goToFirstPage()](https://help.syncfusion.com/api/js/ejpdfviewer#gotofirstpage "goToFirstPage method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).goToFirstPage();
{% endhighlight %}

goToLastPage()

The last page of the PDF document can be navigated in the ejPdfViewer using the [goToLastPage()](https://help.syncfusion.com/api/js/ejpdfviewer#gotolastpage "goToLastPage method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).goToLastPage();
{% endhighlight %}

goToPage(pageNumber)

The specific page in the PDF document can be navigated using the [goToPage(pageNumber)](https://help.syncfusion.com/api/js/ejpdfviewer#gotopagepagenumber "goToPage method") method. If the page is not available for the given pageNumber, the PDF viewer retains the existing page in view.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).goToPage(4);
{% endhighlight %}

pageClick

When a page of the PDF document is clicked, the pageClick event will be triggered. We can define the event method using the [pageClick](https://help.syncfusion.com/api/js/ejpdfviewer#pageclick "pageClick Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", pageClick: "pageClicked" });
});
function pageClicked (args) {
    alert("The page is clicked”);
}
{% endhighlight %}

### Text Markup Annotation Tools

The text markup annotation tools of the ejPdfViewer contain strikeout, highlight, and underline tools in the default toolbar. The ejPdfViewer control also has an option to show or hide the text markup annotation tools in the default toolbar. You can achieve this by using the [showTextMarkupAnnotationTools(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showtextmarkupannotationtools "showTextMarkupAnnotationTools method") method. The following code snippet describes how to hide the text markup annotation tools in the default toolbar in the widget.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showTextMarkupAnnotationTools(false);
{% endhighlight %}

### Print Tool

The print tool of the ejPdfViewer contains an option to print the PDF document. When the print button is clicked, the changes made in the PDF document will be printed along with the document using the browser’s default printer settings. The ejPdfViewer control provides the option to show or hide the print tool in the default toolbar. You can achieve this by using the [showPrintTools(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showprinttools "showPrintTools method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showPrintTools(false);
{% endhighlight %}

The printing of the PDF document can be achieved in the client side by calling the [print()](https://help.syncfusion.com/api/js/ejpdfviewer#print "print method") method. 

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).print();
{% endhighlight %}

*beforePrint*

When the print option is clicked, the beforePrint event will be triggered before printing the PDF document from the ejPdfViewer control. We can define the event method using the [beforePrint](https://help.syncfusion.com/api/js/ejpdfviewer#events:beforeprint "beforePrint event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", beforePrint: "beforePrint" });
});
function beforePrint(args) {
    alert("The PDF document is made ready for printing.");
}
{% endhighlight %}

*afterPrint*

After the printing process is completed, the afterPrint event will be triggered. We can define the event method using the [afterPrint](https://help.syncfusion.com/api/js/ejpdfviewer#events:afterprint "afterPrint Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", afterPrint: "afterPrint" });
});
function afterPrint (args) {
    alert("Printing completed successfully");
}
{% endhighlight %}

### Download Tool

The download tool of the ejPdfViewer contains an option to download the PDF document. When the download button is clicked, the changes made in the PDF document will be saved in a copy of the original PDF document and it will be downloaded in the browser. The ejPdfViewer control provides the option to show or hide the download tool in the default toolbar. You can achieve this by using the [showDownloadTool(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showdownloadtool "showDownloadTool method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showDownloadTool(false);
{% endhighlight %}

The PDF document can be downloaded in the client side by calling the [download()](https://help.syncfusion.com/api/js/ejpdfviewer#methods:download "download method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).download();
{% endhighlight %}

### Signature tool

The signature tool of the ejPdfViewer contains an option to include handwritten signatures in the PDF document. The ejPdfViewer control provides the option to show or hide the signature tool in the default toolbar. You can achieve this by using the [showSignatureTool(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showsignaturetool "showSignatureTool method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showSignatureTool(false);
{% endhighlight %}

### Selection tool

The selection tool of the ejPdfViewer control contains options for selection and panning interaction modes. The ejPdfViewer control provides the option to show or hide the selection tool in the default toolbar. You can achieve this by using the [showSelectionTool(bool)](https://help.syncfusion.com/api/js/ejpdfviewer#methods:showselectiontool "showSelectionTool method") method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showSelectionTool(false);
{% endhighlight %}

### Text Search tool

The text search tool of the ejPdfViewer control is used to initiate and close the text search process in the control. The ejPdfViewer control provides the option to show or hide the text search tool in the default toolbar. You can achieve this by using the showTextSearchTool(bool) method.

{% highlight javascript %}
$(“#container”).data(“ejPdfViewer”).showTextSearchTool(false);
{% endhighlight %}

**APIs available for Text Search tool**

searchText(targetText)

[searchText(targetText)](https://help.syncfusion.com/api/js/ejpdfviewer#searchtexttargettext "searchText method") method allows us to search the target text in the PDF document and highlights the occurrences in the pages.

{% highlight javascript %}
$(“#container”).data("ejPdfViewer").searchText("name");
{% endhighlight %}

searchNext()

The next occurrences of the searched text from the current occurrence can be searched using the [searchNext()](https://help.syncfusion.com/api/js/ejpdfviewer#searchnext "searchNext method") method.

{% highlight javascript %}
$(“#container”).data("ejPdfViewer").searchNext();
{% endhighlight %}

searchPrevious()

The previous occurrence of the searched text from the current occurrence can be searched using the [searchPrevious()](https://help.syncfusion.com/api/js/ejpdfviewer#searchprevious "searchPrevious method") method.

{% highlight javascript %}
$(“#container”).data("ejPdfViewer").searchPrevious();
{% endhighlight %}

matchCase(enableMatchCase)

The target text in the PDF document can be searched with its casing using the [matchCase(enableMatchCase)](https://help.syncfusion.com/api/js/ejpdfviewer#matchcaseenablematchcase "matchCase method") method.

{% highlight javascript %}
$(“#container”).data("ejPdfViewer").matchCase(true);
{% endhighlight %}

cancelSearchText()

The text search can be canceled and the highlighted occurrences from the ejPdfViewer can be removed using the [cancelSearchText()](https://help.syncfusion.com/api/js/ejpdfviewer#cancelsearchtext "cancelSearchText method") method.

{% highlight javascript %}
$(“#container”).data("ejPdfViewer").cancelSearchText();
{% endhighlight %}

**Adding Custom toolbar**

The toolbar can be customized by hiding the existing toolbar.
The following code snippet shows how to create a customer toolbar by using the [client side APIs](https://help.syncfusion.com/api/js/ejpdfviewer "ejPdfViewer API documentation").

{% highlight html %}
<body>
    <div>
        <div id="toolbarDiv" style="height:38px;width:100%;border:solid black 1px" class="toolbarclass " role="toolbar">
            <div style="float:left; padding:5px;">
                <div class="e-pdfviewer-icon e-pdfviewer-gotoprevious" id="viewer-previous" onclick="callClientSideMethod('previous')"></div>
                <div class="e-pdfviewer-icon e-pdfviewer-gotonext" id="viewer-next" onclick="callClientSideMethod('next')"></div>
                <input id="currentPage" class="e-pdfviewer-pagenumber e-pdfviewer-elementalignments" type="text" onkeypress="updatePageNumber(event)" />
                <span id="totalPageCount" class="e-pdfviewer-labelpageno"></span>
                <div class="e-pdfviewer-icon e-pdfviewer-zoomin" id="viewer-zoomin" onclick="callClientSideMethod('zoomin')"></div>
                <div class="e-pdfviewer-icon e-pdfviewer-zoomout" id="viewer-zoomout" onclick="callClientSideMethod('zoomout')"></div>
                <div class="e-pdfviewer-icon e-pdfviewer-fitwidth" id="viewer-fitwidth" onclick="callClientSideMethod('fitwidth')"></div>
                <div class="e-pdfviewer-icon e-pdfviewer-fitpage" id="viewer-fitpage" onclick="callClientSideMethod('fitpage')"></div>
            </div>
            <div style="float:right; padding:5px;">
                <div class="e-pdfviewer-icon e-pdfviewer-print" id="viewer-print" onclick="callClientSideMethod('print')"></div>
                <div class="e-pdfviewer-icon e-pdfviewer-download" id="viewer-download" onclick="callClientSideMethod('download')"></div>
            </div>
        </div>

        <div style="width:100%;height:780px;margin-top:3px">
            <div id="viewer"></div>
        </div>
    </div>
    <script type="text/javascript">
        var currentPageNumber = 1;
        $(function () {
            $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', documentLoad: "onDocumentLoad", pageChange: "pageChange" });
            var pdfviewer = $('#viewer').data('ejPdfViewer');
            document.getElementById('currentPage').value = 1;
            document.getElementById('totalPageCount').innerHTML = "/" + pdfviewer.pageCount;
            pdfviewer.showToolbar(false);
        });

        function onDocumentLoad() {
            var _ejPdfViewer = $('#viewer').data('ejPdfViewer');
            document.getElementById('totalPageCount').innerHTML = "/" + _ejPdfViewer.pageCount;
        }
        function pageChange(args) {
            currentPageNumber = args.currentPageNumber;
            document.getElementById('currentPage').value = args.currentPageNumber;
        }
        function updatePageNumber(event) {
            var _ejPdfViewer = $('#viewer').data("ejPdfViewer");
            currentPageNumber = document.getElementById('currentPage').value;
            if (event.which == 13) {
                if (currentPageNumber > 0 && currentPageNumber <= _ejPdfViewer.pageCount) {
                    _ejPdfViewer.goToPage(currentPageNumber);
                } else {
                    currentPageNumber = _ejPdfViewer.currentPageNumber;
                }
            }
        }
        function callClientSideMethod(apiName) {
            var _ejPdfViewer = $('#viewer').data("ejPdfViewer");
            switch (apiName) {
                case 'print':
                    _ejPdfViewer.print();
                    break;
                case 'zoomin':
                    _ejPdfViewer.zoomIn();
                    break;
                case 'zoomout':
                    _ejPdfViewer.zoomOut();
                    break;
                case 'fitpage':
                    _ejPdfViewer.fitToPage();
                    break;
                case 'fitwidth':
                    _ejPdfViewer.fitToWidth();
                    break;
                case 'previous':
                    _ejPdfViewer.goToPreviousPage();
                    break;
                case 'next':
                    _ejPdfViewer.goToNextPage();
                    break;
                case 'download':
                    _ejPdfViewer.download();
                    break;
            }
        }
    </script>
    <style>
        #totalPageCount {
            float: none !important;
        }
    </style>
</body>
{% endhighlight %}

Run the sample. You can view the PDF viewer with custom toolbar.

**Sample:**

<http://www.syncfusion.com/downloads/support/directtrac/general/ze/PdfViewer_ToolbarCustomization63328491>