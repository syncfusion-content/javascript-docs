---
layout: post
title: How To section of Uploadbox widget for Syncfusion Essential JS
description: How To section of Uploadbox widget
platform: JS
control: Uploadbox
documentation: ug
keywords : ejUploadbox, Uploadbox, js Uploadbox, Uploadbox widget
api: /api/js/ejUploadbox
---

# How To

## Display uploaded filename and download it

The uploaded file names can be displayed below the upload button through client side success event of ejUploadbox. Refer to the following code.

{% highlight html %}

    <div id="ControlRegion">
        <div class="frame">
         <div class="control"></div>
          <div id="UploadDefault"></div>
    </div>
       <button onclick="download()">Download</button>
    </div>
       <div id="files" style="display:none">

    </div>
    <script>
        var filename;
        $(function () {
            $("#UploadDefault").ejUploadbox({
                extensionsAllow:".pdf",
                saveUrl: "@Url.Action("UploadFiles")",
                dialogAction: { closeOnComplete: true },
                success: function (args) {
                    $("#files").append('<tr><td>' + args.files.name + " has been uploaded successfully" + '</td></tr>');
                    $("#files").css("display", "block");
                    filename = args.files.name;
                }
            });
        });

    </script>
        
{% endhighlight %}

Uploaded file can be downloaded using another button through onclick event to invoke the download handler in the controller.  Also, you need to pass the filename to the controller for downloading the file. 

{% highlight html %}
  
     <script>
        var filename;
        $(function () {
            $("#UploadDefault").ejUploadbox({
                extensionsAllow:".pdf",
                saveUrl: "@Url.Action("UploadFiles")",
                dialogAction: { closeOnComplete: true },
                success: function (args) {
                    $("#files").append('<tr><td>' + args.files.name + " has been uploaded successfully" + '</td></tr>');
                    $("#files").css("display", "block");
                    filename = args.files.name;
                }
            });
        });

        function download() {
            var url = "/Upload/Download?filename=" + filename;
            window.location.href = url;
        }
    </script>
    
{% endhighlight %}

{% highlight c# %}

    public partial class UploadController : Controller
    {
        public ActionResult UploadFeatures()
        {
            return View();
        }
        private IHostingEnvironment hostingEnv;
        public UploadController(IHostingEnvironment env)
        {
            this.hostingEnv = env;
        }
        [HttpPost]
        public IActionResult UploadFiles(IList<IFormFile> UploadDefault)
        {
            long size = 0;
            foreach (var file in UploadDefault)
            {
                var filename = ContentDispositionHeaderValue
                                .Parse(file.ContentDisposition)
                                .FileName
                                .Trim('"');
                filename = hostingEnv.WebRootPath + $@"\{filename}";
                ViewBag.FileName = filename;
                size += file.Length;
                using (FileStream stream = System.IO.File.Create(filename))
                {
                    file.CopyTo(stream);
                    stream.Flush();
                }
            }
            return View("UploadFeatures");
        }

        [HttpGet]
        public FileResult Download(string filename)
        {
            var filePath = Path.Combine(
                      Directory.GetCurrentDirectory(),
                              "wwwroot");
            IFileProvider provider = new PhysicalFileProvider(filePath);
            IFileInfo fileInfo = provider.GetFileInfo(filename);
            var readStream = fileInfo.CreateReadStream();
            var mimeType = "application/pdf";
            return File(readStream, mimeType, filename);
        }     
       
    }
{% endhighlight %}

 [Sample](http://www.syncfusion.com/downloads/support/directtrac/215167/ze/Upload145137776)         

## Pass custom data to server action in Uploadbox

 You can pass custom data to controller action through the begin event of Uploadbox. Refer to the following code.

 {% highlight html %}
          
    <div class="control">
        Select a file to upload
               <div class="upload">
                   <div id="UploadDefault"></div>
               </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#UploadDefault").ejUploadbox({
                saveUrl: "https://js.syncfusion.com/ejServices/api/uploadbox/Save",
                removeUrl: "https://js.syncfusion.com/ejServices/api/uploadbox/Remove",
                begin: function (args) {
                    args.data = "Name";
                }
            });
        });
    </script>

 {% endhighlight %}

Refer to the sample [here](https://jsplayground.syncfusion.com/vbew2qvj)

Refer to the below KB links for more details 

[Pass additional data](https://www.syncfusion.com/kb/5150/how-to-pass-additional-data-to-save-handler-in-uploadbox)

[Add request header](https://www.syncfusion.com/kb/10137/add-request-header-for-upload-action)