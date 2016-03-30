---
title: ejPdfViewer
description: API reference for ejPdfViewer
platform: js
control: ejPdfViewer
documentation: API
keywords: pdfviewer, ejPdfViewer, pdfviewer api, syncfusion, pdf viewer
---
# ejPdfViewer

PDF viewer JS is visualization component to view PDF documents. It is powered by HTML5/JavaScript and provides various control customizations.

#### Syntax

$(element).ejPdfViewer({serviceUrl: ‘../api/PdfViewer’});

#### Example

{% tabs %}
{% highlight html %}

<div id="viewer"></div>
<script type="text/javascript">
        $(function () {
            $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer'});
});
</script>

{% endhighlight %}
{% endtabs %}

#### Requires

* module:jquery.js
* module:jquery.easing.min.js
* module:ej.core.js
* module:ej.pdfviewer.js
* module:ej.dropdownlist.js
* module:ej.toolbar.js
* module:ej.button.js
* module:ej.waitingpopup.js
* module:ej.scroller.js

## Members

### locale `String`
{:#members:locale}

Specifies the locale information of the PDF viewer.

**Default Value**: “en-US”

#### Example:

{% tabs %}
{% highlight html %}

<div id="viewer"></div>
<script type="text/javascript">
        $(function () {
            $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', locale:"fr-FR" });
        });
</script>

{% endhighlight %}
{% endtabs %}

### toolbarSettings `Object`
{:#members:toolbarsettings}

Specifies the toolbar settings.

### toolbarSettings.showToolTip `Boolean`
{:#members:toolbarsettings-showtooltip}

Shows or hides the tooltip of the toolbar items.

**Default Value**: true

#### Example:

{% tabs %}
{% highlight html %}

<div id="viewer"></div>
<script type="text/javascript">
        $(function () {
            $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', toolbarSettings: { showTooltip: false } });
        });
</script>

{% endhighlight %}
{% endtabs %}

### toolbarItems `enum`
{:#members:toolbarsettings-toolbaritem}

<ts name="ej.PdfViewer.ToolbarItems"/>

Shows or hides the grouped items in the toolbar with the help of enum ej.PdfViewer.ToolbarItems

<table class="params">
<thead>
<tr>
<th>
Name
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
MagnificationTools
</td>
<td class="description">
Shows only magnification tools in the toolbar.
</td>
</tr>
<tr>
<td class="name">
PageNavigationTools
</td>
<td class="description">
Shows only page navigation tools in the toolbar.
</td>
</tr>
<tr>
<td class="name">
All
</td>
<td class="description">
Shows all the toolbar items.
</td>
</tr>
</tbody>
</table>

**Default value:** ej.PdfViewer.ToolbarItems.All

#### Example:

Below code snippet shows only the magnification tools in the toolbar.

{% tabs %}
{% highlight html %}

<div id="viewer"></div>
<script type="text/javascript">
        $(function () {
           $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', toolbarSettings: { toolbarItem: ej.PdfViewer.ToolbarItems.MagnificationTools } });
        });
</script>

{% endhighlight %}
{% endtabs %}

### serviceUrl `String`
{:#members:serviceurl}

### pageCount `Number`
{:#members:pagecount}

Gets the total number of pages in PDF document.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
var totalPages = pdfviewerObj.pageCount;

{% endhighlight %}
{% endtabs %}

### currentPageNumber `Number`
{:#members:currentpagenumber}

Gets the number of the page being displayed in the PDF Viewer. 

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
var currentPage = pdfviewerObj.currentPageNumber;

{% endhighlight %}
{% endtabs %}

### zoomPercentage `Number`

{:#members:zoompercentage}

Gets the current zoom percentage of the PDF document in viewer.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
var currentZoom = pdfviewerObj.zoomPercentage;

{% endhighlight %}
{% endtabs %}

### pdfService `enum`
{:#members:pdfservice}

<ts name="ej.PdfViewer.PdfService"/>

Specifies the location of the supporting PDF service

<table class="params">
<thead>
<tr>
<th>
Name
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Local
</td>
<td class="description">
Denotes that the service is located in the local project
</td>
</tr>
<tr>
<td class="name">
Remote
</td>
<td class="description">
Denotes that the service is hosted in the remote server
</td>
</tr>
</tbody>
</table>

**Default value:** ej.PdfViewer.PdfService.Local

#### Example:

The below code snippet shows the service accessed from remote server.

{% tabs %}
{% highlight js %}
<div id="viewer"></div>
<script type="text/javascript">
        $(function () {
           $("#viewer").ejPdfViewer({serviceUrl: 'http://mvc.syncfusion.com/PDFViewer/pdfviewer.asmx/PostViewerAction', pdfService : ej.PdfViewer.PdfService.Remote});
        });
</script>
{% endhighlight %}
{% endtabs %}

## Methods

### goToPage(pageNumber) `Number`
{:#methods:gotopage}

Navigates to the specific page in the PDF document. If the page is not available for the given pageNumber, PDF viewer retains the existing page in view. 

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.goToPage(4);

{% endhighlight %}
{% endtabs %}

### goToLastPage()
{:#methods:gotolastpage}

Navigates to the last page of the PDF document.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.goToLastPage();

{% endhighlight %}
{% endtabs %}

### goToFirstPage()
{:#methods:gotofirstpage}

Navigates to the first page of PDF document.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.goToFirstPage();

{% endhighlight %}
{% endtabs %}

### goToNextPage()
{:#methods:gotonextpage}

Navigates to the next page of the PDF document.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.goToNextPage();

{% endhighlight %}
{% endtabs %}

### goToPreviousPage()
{:#methods:gotopreviouspage}

Navigates to the previous page of the PDF document.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.goToPreviousPage();

{% endhighlight %}
{% endtabs %}

### showPageNavigationTools(show) `Boolean`
{:#methods:showpagenavigationtools}

Shows/hides the page navigation tools in the toolbar

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.showPageNavigationTools(false);

{% endhighlight %}
{% endtabs %}

### showMagnificationTools(show) `Boolean`
{:#methods:showmagnificationtools}

Shows/hides the zoom tools in the tool bar.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.showMagnificationTools(false);

{% endhighlight %}
{% endtabs %}

### showToolbar(show) `Boolean`
{:#methods:showtoolbar}

Shows/hides the tool bar in the PDF viewer.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.showToolbar(false);

{% endhighlight %}
{% endtabs %}

### load(fileName) `String`
{:#methods:load}

Loads the document with the filename and displays it in PDF viewer.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.load("Manual");

{% endhighlight %}
{% endtabs %}

### fitToPage()
{:#methods:fittopage}

Scales the page to fit the page in the container in the control.
#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.fitToPage();

{% endhighlight %}
{% endtabs %}

### fitToWidth()
{:#methods:fittowidth}

Scales the page to fit the page width to the width of the container in the control.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.fitToWidth();

{% endhighlight %}
{% endtabs %}

### zoomIn()
{:#methods:zoomin}

Magnifies the page to the next value in the zoom drop down list.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.zoomIn();

{% endhighlight %}
{% endtabs %}

### zoomOut()
{:#methods:zoomout}

Shrinks the page to the previous value in the magnification in the drop down list.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.zoomOut();

{% endhighlight %}
{% endtabs %}

### zoomTo(zoomValue) `Number`
{:#methods:zoomto}

Scales the page to the specified percentage ranging from 50 to 400. If the given zoomValue is less than 50 or greater than 400; the PDF viewer scales the page to 50 and 400 respectively.

#### Example:

{% tabs %}
{% highlight js %}

var pdfviewerObj = $("#viewer").data("ejPdfViewer");
pdfviewerObj.zoomTo(130);

{% endhighlight %}
{% endtabs %}

## Events

### documentLoad
{:#events:documentload}

Triggers when the PDF document gets loaded and is ready to view in the Control.

<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument
</td>
<td class="type">
object
</td>
<td class="description">
Event parameters from PDF viewer
<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel
</td>
<td class="type">
boolean
</td>
<td class="description">
true, if the event should be canceled; otherwise, false.
</td>
</tr>
<tr>
<td class="name">
model
</td>
<td class="type">
object
</td>
<td class="description">
Returns the PDF viewer model
</td>
</tr>
<tr>
<td class="name">
type
</td>
<td class="type">
string
</td>
<td class="description">
Returns the name of the event
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example:

{% tabs %}
{% highlight html %}

<script type="text/javascript">
        $(function () {
            var obj = $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', documentLoad:"documentLoaded" });
        });
        function documentLoaded(args) {
            alert("The document is ready to view");
        }
</script>

{% endhighlight %}
{% endtabs %}

### pageChange
{:#events:pagechange}

Triggers when there is change in current page number.
<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument
</td>
<td class="type">
object
</td>
<td class="description">
Event parameters from PDF viewer
<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel
</td>
<td class="type">
boolean
</td>
<td class="description">
true, if the event should be canceled; otherwise, false.
</td>
</tr>
<tr>
<td class="name">
model
</td>
<td class="type">
object
</td>
<td class="description">
Returns the PDF viewer model
</td>
</tr>
<tr>
<td class="name">
type
</td>
<td class="type">
string
</td>
<td class="description">
Returns the name of the event
</td>
</tr>
<tr>
<td class="name">
currentPageNumber
</td>
<td class="type">
number
</td>
<td class="description">
Returns the current page number in view.
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example:

{% tabs %}
{% highlight html %}

<script type="text/javascript">
        $(function () {
            var obj = $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', pageChange:"currentPageChanged" });
        });
        function currentPageChanged(args) {
            alert("The current page number is " + args.currentPageNumber);
        }
</script>

{% endhighlight %}
{% endtabs %}

### zoomChange
{:#events:zoomchange}

Triggers when there is change in the magnification value.

<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Argument
</td>
<td class="type">
object
</td>
<td class="description">
Event parameters from PDF viewer
<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel
</td>
<td class="type">
boolean
</td>
<td class="description">
true, if the event should be canceled; otherwise, false.
</td>
</tr>
<tr>
<td class="name">
model
</td>
<td class="type">
object
</td>
<td class="description">
Returns the PDF viewer model
</td>
</tr>
<tr>
<td class="name">
type
</td>
<td class="type">
string
</td>
<td class="description">
Returns the name of the event.
</td>
</tr>
<tr>
<td class="name">
previousZoomPercentage
</td>
<td class="type">
number
</td>
<td class="description">
Returns the previous zoom percentage of the PDF viewer control
</td>
</tr>
<tr>
<td class="name">
currentZoomPercentage
</td>
<td class="type">
number
</td>
<td class="description">
Returns the current zoom percentage of the PDF viewer control
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example:

{% tabs %}
{% highlight html %}

<script type="text/javascript">
        $(function () {
            var obj = $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', zoomChange: "zoomChanged" });
        });
        function zoomChanged(args) {
            alert("The magnification changes from " + args.previousZoomPercentage + " to" + args.currentZoomPercentage);
        }
</script>

{% endhighlight %}
{% endtabs %}

### destroy
{:#events:destroy}

Triggers when PDF viewer control is destroyed successfully.

<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument
</td>
<td class="type">
object
</td>
<td class="description">
Event parameters from PDF Viewer
<table>
<thead>
<tr>
<th>
{{'**Name**'| markdownify }}
</th>
<th>
{{'**Type**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel
</td>
<td class="type">
boolean
</td>
<td class="description">
True, if the event should be canceled; otherwise, false.
</td>
</tr>
<tr>
<td class="name">
model
</td>
<td class="type">
object
</td>
<td class="description">
Returns the PDF viewer model
</td>
</tr>
<tr>
<td class="name">
type
</td>
<td class="type">
string
</td>
<td class="description">
Returns the name of the event
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example:

{% tabs %}
{% highlight html %}

<script type="text/javascript">
        $(function () {
            var obj = $("#viewer").ejPdfViewer({ serviceUrl: '../api/PdfViewer', destroy: "destroy" });
        });
        function destroy(args) {
            alert("The control is destroyed successfully");
        }
</script>

{% endhighlight %}
{% endtabs %}