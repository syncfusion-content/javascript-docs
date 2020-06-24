---
layout: post
title: Pdfium rendering engine in Syncfusion Essential JS PDF viewer.
description: Learn here about how Syncfusion Essential JS PDF viewer uses Pdfium rendering engine to render and print PDF files.
platform: js
control: PDF viewer
documentation: ug
keywords: ejPdfViewer, PDF Viewer
api: /api/js/ejpdfviewer
---

# How to use pdfium rendering engine in PDF viewer

From the **Essential Studio 2018 Volume 4 release(16.4.0.42)**, the PDF Viewer provides a robust rendering of PDF document using the Pdfium rendering engine.

**PDF Viewer provides the following support with Pdfium rendering engine:**

* Rendering the PDF documents in PDF Viewer. 

* Exporting PDFs as Raster Images. 

* Extracting the text from the PDF document. 

N> Scripts and the assemblies must be referred with same version in the project to avoid the blank rendering of the documents.

#### Switching between the Syncfusion rendering engine and Pdfium rendering engine

Pdfium is the **default rendering engine** of the PDF Viewer. You can switch between the Syncfusion rendering engine and Pdfium rendering engine using the **RenderingEngine enum**.

The following code snippet describes how to set the RenderingEngine

{% highlight c# %}
//Renders the PDF document using Syncfusion rendering engine
PdfViewerHelper.RenderingEngine = PdfViewerHelper.PdfRenderingEngine.EJPdf;
{% endhighlight %}

#### Exporting PDFs as raster images
   
The PDF Viewer Web allows the PDF document pages to be exported as raster images using the Pdfium rendering engine. Exporting can be done using the ExportAsImage() method. This option helps to convert a PDF into an image. The APIs available to export the PDF document pages as images are listed as follows:

**ExportAsImage(int pageindex)**

Exports the specified page as image using the Pdfium rendering engine.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly   
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document.
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf"); 
//Exports the first page of the PDF document into image  
Bitmap image = viewer.ExportAsImage(0); 
 //To save the image             
image.Save(dataPathBase + @"JavaScript_Succinctly.png", System.Drawing.Imaging.ImageFormat.Png);
{% endhighlight %}

**ExportAsImage(int pageIndex, float dpiX, float dpiY)**

Exports the specified page as image with respect to the specified DPI values.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
//Exports the first page of the PDF document as image with the specified DPI values
Bitmap image = viewer.ExportAsImage(0, 200, 200); 
//To save the image             
image.Save(dataPathBase + @"JavaScript_Succinctly.png", System.Drawing.Imaging.ImageFormat.Png);
{% endhighlight %}

**ExportAsImage(int pageIndex, SizeF customSize, bool keepAspectRatio)**

Exports the specified page as image with respect to the specified custom size. 

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
//Exports the first page of the PDF document as image with the custom size
Bitmap image = viewer.ExportAsImage(0, new SizeF(200, 300), true); 
//To save the image             
image.Save(dataPathBase + @"JavaScript_Succinctly.png", System.Drawing.Imaging.ImageFormat.Png);
{% endhighlight %}

**ExportAsImage(int pageIndex, SizeF customSize, float dpiX, float dpiY, bool keepAspectRatio)**

Exports the specified page as image with respect to the custom size and the specified DPI values.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
//Exports the first page of the PDF document as image with the custom size and the specified DPI values
Bitmap image = viewer.ExportAsImage(0, new SizeF(200, 300),200,200, true);
//To save the image             
image.Save(dataPathBase + @"JavaScript_Succinctly.png", System.Drawing.Imaging.ImageFormat.Png);
{% endhighlight %}

**ExportAsImage(int startIndex, int endIndex)**

Exports the specified pages as images using the Pdfium rendering engine.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
//Exports the PDF document pages as images 
Bitmap[] image = viewer.ExportAsImage(0, viewer.PageCount - 1); 
for (int i = 0; i < viewer.PageCount - 1; i++)
	{
	//To save the image             
    image[i].Save(dataPathBase + @"JavaScript_Succinctly_" + i + ".png", System.Drawing.Imaging.ImageFormat.Png);
	}
{% endhighlight %}

**ExportAsImage(int startIndex, int endIndex, float dpiX, float dpiY)**

Exports the specified pages as images with respect to the specified DPI values.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
// Exports the PDF document pages as images 
Bitmap[] image = viewer.ExportAsImage(0, viewer.PageCount – 1, 200, 200); 
for (int i = 0; i < viewer.PageCount - 1; i++)
	{
	//To save the image             
    image[i].Save(dataPathBase + @"JavaScript_Succinctly_" + i + ".png", System.Drawing.Imaging.ImageFormat.Png);
	}
{% endhighlight %}

**ExportAsImage(int startIndex, int endIndex, SizeF customSize, bool keepAspectRatio)**

Exports the specified pages as images with respect to the specified custom size. 

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
// Exports the PDF document pages as images 
Bitmap[] image = viewer.ExportAsImage(0, viewer.PageCount – 1, new SizeF(200, 300), false);
for (int i = 0; i < viewer.PageCount - 1; i++)
	{
	//To save the image             
    image[i].Save(dataPathBase + @"JavaScript_Succinctly_" + i + ".png", System.Drawing.Imaging.ImageFormat.Png);
	}
{% endhighlight %}

**ExportAsImage(int startIndex, int endIndex, SizeF customSize, float dpiX, float dpiY, bool keepAspectRatio)**

Exports the specified pages as images with respect to the custom size and the specified DPI values.

{% highlight c# %}
//Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper viewer = new PdfViewerHelper();
//To load the PDF document 
viewer.Load(dataPathBase + @"JavaScript_Succinctly.pdf");
// Exports the PDF document pages as images 
Bitmap[] image = viewer.ExportAsImage(0, viewer.PageCount – 1, new SizeF(200, 300),200,200,false); 
for (int i = 0; i < viewer.PageCount - 1; i++)
	{
	//To save the image             
    image[i].Save(dataPathBase + @"JavaScript_Succinctly_" + i + ".png", System.Drawing.Imaging.ImageFormat.Png);
	}
{% endhighlight %}

#### Extracting the text from the PDF document

PDF Viewer allows you to extract the text from a page along with the bounds using the Pdfium rendering engine.

The following code snippet explains how to extract the text from a page.

{% highlight c# %}
// Uses the Syncfusion.EJ.PdfViewer assembly  
PdfViewerHelper helper = new PdfViewerHelper(); 
helper.Load("JavaScript_Succinctly.pdf");
//Returns the bounds of the text
List<Syncfusion.EJ.PdfViewer.TextData> textCollection = new List<Syncfusion.EJ.PdfViewer.TextData>();
//Extracts the text from the first page of the PDF document along with its bounds
string text = helper.ExtractText(0, out textCollection);
System.IO.File.WriteAllText("../../output/" + data + ".txt", text);
{% endhighlight %}

N> By default, the ExportAsImage() and ExtractText() functionalities occurs with Pdfium rendering engine, irrespective of the RenderingEngine mode.