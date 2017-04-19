---
layout: post
title: Localization of Syncfusion Essential JS PDF viewer.
description: Localization of Syncfusion Essential JS PDF viewer.
platform: js
control: PDF viewer
documentation: ug
keywords: ejPdfViewer
api: /api/js/ejpdfviewer
---

## Localization

We can localize the tooltip of the default toolbar in the ejPdfViewer widget with the collection of localized strings using ej.PdfViewer.Locale for different cultures. By default, ejPdfViewer is localized in “**en-US**” culture.

Following table shows the default tooltip values in ‘en-US’ culture

<table>
<tr>
<td>
{{'**Function**'| markdownify }}
</td>
<td>
{{'**Keywords**'| markdownify }}
</td>
<td>
{{'**Values**'| markdownify }}
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
first
</td>
<td>
headerText
</td>
<td>
First
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Go to the first page of the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
previous
</td>
<td>
headerText
</td>
<td>
Previous
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Go to the previous page of the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
next
</td>
<td>
headerText
</td>
<td>
Next
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Go to the next page of the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
last
</td>
<td>
headerText
</td>
<td>
Last
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Go to the last page of the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
zoomIn
</td>
<td>
headerText
</td>
<td>
Zoom-In
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Zoom in to the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
zoomOut
</td>
<td>
headerText
</td>
<td>
Zoom-Out
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Zoom out of the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
pageIndex
</td>
<td>
headerText
</td>
<td>
Page Number
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Current page number in view.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
zoom
</td>
<td>
headerText
</td>
<td>
Zoom
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Zoom in or out on the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
fitToWidth
</td>
<td>
headerText
</td>
<td>
Fit to Width
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Fit the PDF page to the width of the container.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
fitToPage
</td>
<td>
headerText
</td>
<td>
Fit to Page
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Fit the PDF page to the container.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
print 
</td>
<td>
headerText
</td>
<td>
Print
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Print the PDF document.
</td>
</tr>
<tr>
<td colspan="1" rowspan="2">
download
</td>
<td>
headerText
</td>
<td>
Download
</td>
</tr>
<tr>
<td>
contentText
</td>
<td>
Download the PDF document.
</td>
</tr>
</table>

The following code snippet illustrates you to change the localization to German culture “**de-DE**”

{% highlight html %}
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
//--
<body>
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <table style="width:100%">
                    <tr>
                        <td>
                            <div class="control">
                                <div id="container"></div>
                            </div>
                        </td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#container").ejPdfViewer({serviceUrl: "/api/PdfViewerAPI" , locale: 'de-DE' });
            ej.PdfViewer.Locale["de-DE"] = {
                toolbar: {
                    first: {
                        headerText: 'Erste',
                        contentText: 'Gehen Sie auf die erste Seite des PDF-Dokument.'
                    },
                    previous: {
                        headerText: 'Zurück',
                        contentText: 'Gehen Sie auf die vorherige Seite des PDF-Dokuments.'
                    },
                    next: {
                        headerText: 'Nächster',
                        contentText: 'Gehen Sie auf die nächste Seite des PDF-Dokuments.'
                    },
                    last: {
                        headerText: 'Letzte',
                        contentText: 'Gehen Sie auf die letzte Seite des PDF-Dokuments.'
                    },
                    zoomIn: {
                        headerText: 'Hineinzoomen',
                        contentText: 'Vergrößern Sie das PDF-Dokument.'
                    },
                    zoomOut: {
                        headerText: 'Rauszoomen',
                        contentText: 'Zoom aus dem PDF-Dokument.'
                    },
                    pageIndex: {
                        headerText: 'Seitennummer',
                        contentText: 'Aktuelle Seitenzahl, um zu sehen.'
                    },
                    zoom: {
                        headerText: 'Zoom',
                        contentText: 'Vergrößern oder Verkleinern auf dem PDF-Dokument.'
                    },
                    fittoWidth: {
                        headerText: 'An Breite anpassen',
                        contentText: 'Montieren Sie die PDF-Seite an die Breite des Behälters.'
                    },
                    fittopage: {
                        headerText: 'An Seite anpassen',
                        contentText: 'Montieren Sie die PDF-Seite in den Behälter.'
                    },
                    print: {
                        headerText: ' Drucken',
                        contentText: ' Drucken Sie das PDF-Dokument.'
                    },
                    download: {
                        headerText: ' Herunterladen',
                        contentText: ' Laden Sie das PDF-Dokument'
                    },

                },
            };
        });
    </script>
    <style>
        .frame {
            height: 600px;
            width: 950px;
        }
    </style>
</body>
</html>
{% endhighlight %}

The following screenshot shows the PDF viewer with tooltip in German language.

![](Localization_images/Localization_img1.png)

