---
layout: post
title: Import and Export in RichTextEditor widget for Syncfusion Essential JS
description: Import content from word document into the RichTextEditor and Export the RichTextEditor content into word or PDF document.
platform: js
control: RTE
documentation: ug
keywords: RichTextEditor, server side XHTML Validation, RTE import, RTE export, export to PDF, export to Word
api: /api/js/ejrte
---

# Import and Export in RichTextEditor 

## Import

Import feature provides support to import a word document into the editor `textarea`. To enable import option in the RTE tool bar,  `import` toolbar items needs to be added in RTE toolbar toolsList using `importExport` which adds the tool in the toolbar. In [importSettings](https://help.syncfusion.com/api/js/ejrte#members:importsettings) url option, the server page for import is needed to be mapped. When you click the toolbar import icon, it opens a dialog to browse the select a word file. The selected word file will be imported into the editor `textarea`.

{% highlight html %}

    <textarea id="rteExport" rows="10" cols="30" style="width: 740px; height: 440px">
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;
    </textarea>

    <script type="text/javascript" class="jsScript">
        $(function () {
            $("#rteExport").ejRTE({
                width:"100%",
				minWidth:"150px",
				importSettings: {
                     url: "http://js.syncfusion.com/ejServices/api/RTE/Import" 
                     },
                tools: {
					importExport: ["import"]
                }
            });
        });
    </script>


{% endhighlight  %}

### Import Server configuration

Currently word document can be imported in server-side only, through **EJ's** helper functions in .NET. So, to use RTE import in your projects, it is required to create a server with any of the following web services. 

* Web API 
* WCF Service
* ASP.NET MVC Controller Action 
* ASP.NET WebMethod 

Following code snippet demonstrate import with WebAPI controller.

{% highlight c# %}

     public class RTEController : ApiController
    {
        [HttpPost]
        public string Import()
        {
            string HtmlString = string.Empty;
            if (HttpContext.Current.Request.Files.AllKeys.Any())
            {
                string RTEID = HttpContext.Current.Request.QueryString["rteid"];
                var fileName = RTEID + "_importUpload";
                var httpPostedFile = HttpContext.Current.Request.Files[fileName];
                if (httpPostedFile != null)
                {
                    using (var mStream = new MemoryStream())
                    {
                        new WordDocument(httpPostedFile.InputStream).Save(mStream, FormatType.Html);
                        mStream.Position = 0;
                        HtmlString = new StreamReader(mStream).ReadToEnd();
                    };

                    HtmlString = ExtractBodyContent(HtmlString);

                    foreach (var item in DecodeKeys())
                    {
                        HtmlString = HtmlString.Replace(item.Key, item.Value);
                    }
                }
                else HttpContext.Current.Response.Write("Select any file to upload.");

            }
            return HtmlString;
        }

        public IDictionary<string, string> DecodeKeys()
        {
            IDictionary<string, string> KeyValuePair = new Dictionary<string, string>()
            {
               {"\"", "'"},{"\r", " "},{"\n", "<br/> "},{"\r\n", " "},{"( )+", " "},{"&nbsp;", " "},{"&bull;", "*"},{"&lsaquo;", "<"},
               {"&rsaquo;", ">"},{"&trade;", "(tm)"},{"&copy;", "(c)"},{"&reg;", "(r)"}
            };

            return KeyValuePair;
        }

        public string ExtractBodyContent(string html)
        {
            if (html.Contains("<html") && html.Contains("<body"))
            {
                return html.Remove(0, html.IndexOf("<body>") + 6).Replace("</body></html>", "");

            }
            return html;
        }

    }

{% endhighlight  %}

### Server Dependencies

Full list of assemblies needed for RTE Import are as follows

    1.  Syncfusion.EJ
    2.  Syncfusion.EJ.Export
    3.  Syncfusion.Linq.Base
    4.  Syncfusion.Compression.Base
    5.  Syncfusion.DocIO.Base

![Import Images](ImportAndExport_images/import_images.png)

### Import Limitations

Import feature utilizes the DocIO’s assembly which converts Word Document to the HTML string. The generated string is then appended to the RTE control. DocIO supports only the conversion of Word Documents that are Web Compatible. You can check the compatibility of the any Word document while saving the document. For Example, refer to the following Screenshot.

![Web Compatibility Checker](ImportAndExport_images/web_compatibility_checker.png)

In the above screenshot, there is a compatibility issue with the word document. The text box is preserved with absolute position. While saving the Word document with absolute positioned textbox as HTML, it will be aligned to left or right of the HTML page. So the original format will be altered to support web. Refer to the [DocIO's Word to HTML conversion](https://help.syncfusion.com/file-formats/docio/conversion#customizing-the-word-to-html-conversion) for more information on the supported formats and limitations.

So, in order to have the exact document to be imported into RTE control, make sure that it is compatible with Web.


## Export 

Export feature provides support to export editor `textarea` content into word and PDF files. To enable Export option in the RTE tool bar,  `wordExport` , `pdfExport` toolbar items needs to be added in RTE toolbar toolsList using `importExport` which adds the tool in the toolbar. [exportToWordSettings](https://help.syncfusion.com/api/js/ejrte#members:exporttowordsettings) consists of url and fileName sub properties. In url property, the server page for export to word is needed to be mapped and In fileName property, the name for the exported word file is given. [exportToPdfSettings](https://help.syncfusion.com/api/js/ejrte#members:exporttopdfsettings) consists of url and fileName sub properties. In url property, the server page for export to PDF is needed to be mapped and In fileName property, the name for the exported PDF file is given. When you click the toolbar pdfExport or wordExport icon, the contents of RTE are sent to the server. It performs XHTML Validation on the editor `textarea` content on the server. Once the XHTML validation and formatting is successful, it exports the content into a Word or PDF File.

{% highlight html %}

    <textarea id="rteExport" rows="10" cols="30" style="width: 740px; height: 440px">
        &lt;p&gt;The Rich Text Editor (RTE) control is an easy to render in
        client side. Customer easy to edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. &lt;/p&gt;
    </textarea>

    <script type="text/javascript" class="jsScript">
        $(function () {
            $("#rteExport").ejRTE({
                width:"100%",
				minWidth:"150px",
				exportToWordSettings: {
                     url: "http://js.syncfusion.com/ejServices/api/RTE/ExportToWord", fileName: "WordSample"
                     },
                exportToPdfSettings:{
                     url: "http://js.syncfusion.com/ejServices/api/RTE/ExportToPDF", fileName: "PdfSample" 
                     },
                tools: {
					importExport: ["wordExport", "pdfExport"]
                }
            });
        });
    </script>



{% endhighlight  %}

### Export Server configuration

Currently RTE content can be converted to word or PDF file formats in server-side only, through **EJ's** helper functions in .NET. So, to use exporting in your projects, it is required to create a server with any of the following web services. 

* Web API 
* WCF Service
* ASP.NET MVC Controller Action 
* ASP.NET WebMethod 

Following code snippet demonstrate exporting with WebAPI controller.

{% highlight c# %}

     public class RTEController : ApiController
    {
        //Export to Word Document
        [HttpPost]
        public void ExportToWord()
        {

            string RTEID = HttpContext.Current.Request.QueryString["rteid"];
            string FileName = HttpContext.Current.Request.Params[RTEID + "_inputFile"];
            string htmlText = HttpContext.Current.Request.Params[RTEID + "_inputVal"];
            WordDocument document = GetDocument(htmlText);
            document.Save(FileName + ".docx", FormatType.Docx, HttpContext.Current.Response, HttpContentDisposition.Attachment);
        }
        
        //Export to PDF Document
        [HttpPost]
        public void ExportToPDF()
        {
            string RTEID = HttpContext.Current.Request.QueryString["rteid"];
            string FileName = HttpContext.Current.Request.Params[RTEID + "_inputFile"];
            string htmlText = HttpContext.Current.Request.Params[RTEID + "_inputVal"];
            WordDocument document = GetDocument(htmlText);
            DocToPDFConverter converter = new DocToPDFConverter();
            PdfDocument pdfDocument = converter.ConvertToPDF(document);
            pdfDocument.Save(FileName + ".pdf",HttpContext.Current.Response,HttpReadType.Save);
        }

        public WordDocument GetDocument(string htmlText) 
        {
            WordDocument document = null;
            MemoryStream stream = new MemoryStream();
            StreamWriter writer = new StreamWriter(stream, System.Text.Encoding.Default);
            htmlText = htmlText.Replace("\"", "'");
            XmlConversion XmlText = new XmlConversion(htmlText);
            XhtmlConversion XhtmlText = new XhtmlConversion(XmlText);
            writer.Write(XhtmlText.ToString());
            writer.Flush();
            stream.Position = 0;
            document = new WordDocument(stream, FormatType.Html, XHTMLValidationType.None);
            return document;
        }
    }

{% endhighlight  %}

### Server Dependencies

Export Helper functions are available in the Assembly `Syncfusion.EJ.Export`, which is available in the Essential Studio builds. Full list of assemblies needed for RTE Export as follows

    1.  Syncfusion.EJ
    2.  Syncfusion.EJ.Export
    3.  Syncfusion.Linq.Base
    4.  Syncfusion.Compression.Base
    5.  Syncfusion.DocIO.Base
    6.  Syncfusion.PDF.Base

### Word Export
![Export Word Images](ImportAndExport_images/export_word_images.png)

### PDF Export
![Export PDF Images](ImportAndExport_images/export_pdf_images.png)
