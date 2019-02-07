---
layout: post
title: Export | ReportViewer | JavaScript | Syncfusion
description: Control and customize the export behavior using properties and events. 
platform: js
control: ReportViewer
documentation: ug
---

# Export
Report Viewer provides events, properties to control and customize the exporting functionality.

## Export event handling
You can show the progress information, when the exporting takes long time to complete.

1.Set the [`exportProgressChanged`](../api/ejreportviewer#events:exportprogresschanged) in Report Viewer initialization.
2.Implement the function and add code samples to show custom message based on the progress stage. The follow code sample shows the progress message based on the export event status.  

{% highlight javascript %}
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportProgressChanged: "onExportProgressChanged",
                });
        });
        function onExportProgressChanged(args) {
            if (args.stage == "beginExport") {
                console.log(args.stage);
                args.format =
                    $('#reportviewer').ejWaitingPopup({ showOnInit: true, cssClass: "customStyle", text: "Preparing exporting document.. Please wait..." });
            }
            else if (args.stage == "exportStarted") {
                console.log(args.stage);
                var popupObj = $('#reportviewer').data('ejWaitingPopup');
                popupObj.hide();
            }
            else if (args.stage == "preparation") {
                console.log(args.stage);
                console.log(args.format);
                console.log(args.preparationStage);
                if (args.format == "PDF" && args.preparationStage == "documentPreparation") {
                    console.log(args.totalPages);
                    console.log(args.currentPage);
                    if (args.totalPages > 1 && args.currentPage > 1) {
                        var progressPercentage = Math.floor((args.currentPage / args.totalPages) * 100);
                        if (progressPercentage > 0) {
                            var popupObj = $('#reportviewer').data('ejWaitingPopup');
                            popupObj.setModel({ text: "Preparing exporting document.." + progressPercentage + " % completed.. Please wait..." });
                        }
                    }
                }
            }

            args.handled = true;
        }
    </script>

{% endhighlight %}

## Change Excel and Word export format
Allows you to change the default file format to any other file format using [`excelFormat`](../api/ejreportviewer#members:exportsettings-excelformat) and [`wordFormat`](../api/ejreportviewer#members:exportsettings-wordformat) properties. The following code sample changes the default versions.

{% highlight javascript %}
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportSettings: {
                        excelFormat: ej.ReportViewer.ExcelFormats.Excel2013,
                        wordFormat: ej.ReportViewer.WordFormats.Word2013
                    }
                });
        });

    </script>

{% endhighlight %}

## Hide specific export type for report 
Show or hide the default export types available in component using [`exportOptions`](../api/ejreportviewer#members:exportsettings-exportoptions) property. The following code hides the HTML export type from default export options.

{% highlight javascript %}
    <script type="text/javascript">

        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi ",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportSettings: { exportOptions:ej.ReportViewer.ExportOptions.All & ~ej.ReportViewer.ExportOptions.Html }
                });
        });

    </script>

{% endhighlight %}

## PDF export options
The `PDFOptions` provides properties to manage PDF export behaviors. You have to set the properties in `OnInitReportOptions` method of Web API service.

### Export with complex scripts
To export reports with the complex scripts, set the ComplexScript property of `PDFOptions` instance to true.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            reportOption.ReportModel.PDFOptions = new Syncfusion.EJ.ReportWriter.PDFOptions()
            {
                EnableComplexScript = true
            };
        }

{% endhighlight %}

### PDF Conformance
You can export the report as PDF/A-1b document by specifying the conformance level PdfConformanceLevel.Pdf_A1B in `PdfConformanceLevel` property.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            reportOption.ReportModel.PDFOptions = new Syncfusion.EJ.ReportWriter.PDFOptions()
            {
                PdfConformanceLevel = Syncfusion.Pdf.PdfConformanceLevel.Pdf_A1B
            };
        }

{% endhighlight %}

### Add custom PDF fonts
Allows to have custom fonts in the PDF exported document by adding the font streams to `Fonts` collection in `PDFOptions` instance.

1.Add the font .ttf files into your application App_Data folder. 
2.In the solution explore open the properties of the font file and set the Copy to Output Directory property to Copy always.
3.Initialize the Font collection and add the font stream to it.

N> The key value provided in the font collection should be same as in the report item font property. 

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            reportOption.ReportModel.PDFOptions = new Syncfusion.EJ.ReportWriter.PDFOptions()
            {
                Fonts = new Dictionary<string, Stream>
                {
                    { "MS Mincho", File.OpenRead(System.Web.Hosting.HostingEnvironment.MapPath(@"~/App_Data/MSMINCHO.ttf")) },
                }
            };
        }
{% endhighlight %}

N> If any fonts used in the report definition that is not installed or available in the local system then you must load the font stream.

## Word export options
The `WordOptions` provides properties to manage Word document export behaviors.

### Word document type
You can save the report to required document version by setting the `FormatType` property.

{% highlight c# %}
            reportOption.ReportModel.WordOptions = new Syncfusion.EJ.ReportWriter.WordOptions()
            {
                FormatType = Syncfusion.EJ.ReportWriter.WordFormatType.Docx,
            };
{% endhighlight %}

### Word document advance layout for merged cells
Eliminate the tiny columns, rows, merged cells and render the word document elements without any nested layout by setting the LayoutOption as TopLevel.  The `ParagraphSpacing` is the distance value added between two elements in document.

{% highlight c# %}
            reportOption.ReportModel.WordOptions = new Syncfusion.EJ.ReportWriter.WordOptions()
            {
                LayoutOption = Syncfusion.EJ.ReportWriter.WordLayoutOptions.TopLevel,
                ParagraphSpacing = new Syncfusion.EJ.ReportWriter.ParagraphSpacing()
                {
                    Bottom = 0.5f,
                    Top = 0.5f
                },
            };
{% endhighlight %}

I> A paragraph element is inserted between two tables in the exported document to overcome word document auto merging behavior.

N> The table in word document is not a standalone object, if draw two table one after another, it will automatically get merged into single table.  To prevent this merging, added an empty paragraph between two tables.

### Protecting document from editing
You can restrict a Word document from editing either by providing a password or without password. The following are the types of protection,

1.	AllowOnlyComments: You can add/modify only the comments in the Word document.
2.	AllowOnlyFormFields: You can modify the form field values in the Word document.
3.	AllowOnlyRevisions: You can accept or reject the revisions in the Word document.
4.	AllowOnlyReading: You can only view the content in the Word document.
5.	NoProtection: You can access/edit the Word document contents as normally.

{% highlight c# %}
            reportOption.ReportModel.WordOptions = new Syncfusion.EJ.ReportWriter.WordOptions()
            {
                ProtectionType = Syncfusion.DocIO.ProtectionType.AllowOnlyReading,
            };
{% endhighlight %}

## Excel export options
The `ExcelOptions` provides properties to manage Excel document export behaviors.

### Excel document type
You can save the report to required excel version by setting the `ExcelSaveType ` property.

{% highlight c# %}
            reportOption.ReportModel.ExcelOptions = new Syncfusion.EJ.ReportWriter.ExcelOptions()
            {
                ExcelSaveType = Syncfusion.EJ.ReportWriter.ExcelVersion.Excel2013,
            };
{% endhighlight %}

### Excel document advance layout for merged cells
Eliminate the tiny columns, rows, merged cells, to provide clear readability and to perform data manipulations by setting the LayoutOption as IgnoreCellMerge. 

{% highlight c# %}
            reportOption.ReportModel.ExcelOptions = new Syncfusion.EJ.ReportWriter.ExcelOptions()
            {
                LayoutOption = Syncfusion.EJ.ReportWriter.ExcelLayoutOptions.IgnoreCellMerge,
            };
{% endhighlight %}

### Protecting document from editing
You can restrict Excel document from editing either by providing the `ExcelSheetProtection ` or enabling `ReadOnlyRecommended` properties.

{% highlight c# %}
            reportOption.ReportModel.ExcelOptions = new Syncfusion.EJ.ReportWriter.ExcelOptions()
            {
                ReadOnlyRecommended = true,
                ExcelSheetProtection = ExcelSheetProtection.DeletingColumns,
            };
{% endhighlight %}

## PowerPoint export options
You can save the report to required PowerPoint version by setting the ` FormatType ` property.

{% highlight c# %}
            reportOption.ReportModel.PPTOptions = new Syncfusion.EJ.ReportWriter.PPTOptions()
            {
                FormatType = Syncfusion.EJ.ReportWriter.PPTSaveType.PowerPoint2013,
            };
{% endhighlight %}

## CSV export options
The “CsvOptions” allows to change encoding, delimiters, qualifiers, extension and line break of a Csv exported document.

{% highlight c# %}
            reportOption.ReportModel.CsvOptions = new Syncfusion.EJ.ReportWriter.CsvOptions()
            {
                Encoding = System.Text.Encoding.Default,
                FieldDelimiter = ",",
                UseFormattedValues = false,
                Qualifier = "#",
                RecordDelimiter = "@",
                SuppressLineBreaks = true,
                FileExtension = ".txt"
            };
{% endhighlight %}

## HTML export options
You can hide the separator added at end of each page by setting the `HidePageSeparator`property to true.

{% highlight c# %}
            reportOption.ReportModel.HTMLOptions = new Syncfusion.EJ.ReportWriter.HTMLOptions()
            {
                HidePageSeparator = true
            };
{% endhighlight %}

## Password protect exported document
Allows you to protect the exported document such as PDF, Word, Excel, and PowerPoint from unauthorized users by encrypting the document using encryption password. The following code snippet illustrates how to encrypt the exported document with the user defined password.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            //PDF encryption

            reportOption.ReportModel.PDFOptions = new Syncfusion.EJ.ReportWriter.PDFOptions();
            reportOption.ReportModel.PDFOptions.Security = new Syncfusion.Pdf.Security.PdfSecurity()
            {
                UserPassword = "password"
            };

            //Word encryption
            reportOption.ReportModel.WordOptions = new Syncfusion.EJ.ReportWriter.WordOptions()
            {
                EncryptionPassword = "password"
            };

            //Excel encryption

            reportOption.ReportModel.ExcelOptions = new Syncfusion.EJ.ReportWriter.ExcelOptions()
            {
                PasswordToModify = "password",
                PasswordToOpen = "password"
            };
            //PPT encryption
            reportOption.ReportModel.PPTOptions = new Syncfusion.EJ.ReportWriter.PPTOptions()
            {
                EncryptionPassword = "password"
            };
        }
{% endhighlight %}

N> Password protection is not supported for HTML export format.
