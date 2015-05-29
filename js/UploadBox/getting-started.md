---
layout: post
title: getting-started
description: getting started
platform: js
control: Uploadbox
documentation: ug
---

# Getting Started

This section explains briefly about how to create an **UploadBoxUploadbox** in your application with **JavaScript** and **ASP.NET MVC.**

## Create your first UploadBoxUploadbox in JavaScript

**Essential Java Script UploadBoxUploadbox** widget provides support to upload files or photos within your webpage. From the following guidelines, you can learn how to upload the files that are used in a Resume Upload scenario. This helps you to restrict some file extensions when you upload the resume in server by using **UploadBoxUploadbox** control.

The following screenshot demonstrates the functionality of **UploadBoxUploadbox** with the file extension..



{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img1.png" Caption="Figure 1: UploadBoxUploadbox Control with File restriction"%}{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img2.png" Caption="Figure 1: UploadBoxUploadbox Control with File restriction"%}

In the above screenshot, you can upload a resume that restricts **.htmlpng** and **.txt** files and allows **.HTMLpng**  file extension. This helps you to avoid unsupported resume formats getting uploaded in a server.

> ![](getting-started_images\getting-started_img3.jpeg)_**Note: To get upload the file, you should either run this sample in Visual Studio IDE or host in local IIS..**_

### Create UploadBoxUploadbox widgets

**Essential JavaScript UploadBoxUploadbox** widget basically renders built-in features like upload multiple files, and deletes the files from **UploadBoxUploadbox**. You can know the status of uploading the file whether it is completed or failed and you can retry uploading the files.  You can easily create the **UploadBoxUploadbox** widget by using the following steps.

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add upload box element here  --><!-- add upload box element here  -->
</body>
</html>



{% endhighlight %}



* Add input element to render a **UploadBoxUploadbox.**



{% highlight html %}



<div id="targetElement">
<div id="UploadDefault"></div>

</div>


{% endhighlight %}



* Add the given styles to display the **UploadBoxUploadbox** with margin alignments.



{% highlight css %}


<style>
    #targetElement{
        width: 500px;
        height: 500px;
        margin: 0 auto;
    }
    #UploadDefault{
        margin: 0 auto;
    }
</style><style class="text/css">
        .posupload
        {
            margin-left: 20px;
            margin-top: 20px;
        }
        .frame
        {
            margin-top: 10%;
        }
        .control
        {
            margin-left: 10%;
        }
    </style>



{% endhighlight %}



* Create a new handler file (.ashx) and save it as **saveFiles.ashx** and then copy the following code into it.



{% highlight c# %}

**#SaveFiles.ashx**
public void ProcessRequest(HttpContext context)
    {
        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");
        if (!Directory.Exists(targetFolder))
        {
            Directory.CreateDirectory(targetFolder);
        }
        HttpRequest request = context.Request;
        HttpFileCollection uploadedFiles = context.Request.Files;
        if (uploadedFiles != null && uploadedFiles.Count > 0)
        {
            for (int i = 0; i < uploadedFiles.Count; i++)
            {
                if (uploadedFiles[i].FileName != null && uploadedFiles[i].FileName != "")
                {
                    string fileName = uploadedFiles[i].FileName;
                    int indx = fileName.LastIndexOf("\\");
                    if (indx > -1)
                    {
                        fileName = fileName.Substring(indx + 1);
                    }
                    uploadedFiles[i].SaveAs(targetFolder + "\\" + fileName);
                }
            }
        }

    }    



{% endhighlight %}



* Create a new handler file (.ashx) and save it as **removeFiles.ashx** and then copy the following code into it.



{% highlight c# %}

**#removeFiles.ashx**
public void ProcessRequest(HttpContext context)
    {
        System.Collections.Specialized.NameValueCollection s = context.Request.Params;
        string fileName = s["fileNames"];
        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");
        if (Directory.Exists(targetFolder))
        {
            string physicalPath = targetFolder + "\\" + fileName;
            if (System.IO.File.Exists(physicalPath))
            {
                System.IO.File.Delete(physicalPath);
            }
        }     

    }


{% endhighlight %}



* Initialize the script for **UploadBoxUploadbox.**



{% highlight js %}

**[Script]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#UploadDefault").ejUploadbox({ 
            saveUrl: "saveFiles.ashx",
            removeUrl: " removeFiles.ashx"
        });    
     });
</script>


{% endhighlight %}



The following screenshot displays an **UploadBoxUploadbox** control.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img4.png" Caption="Figure 2: Create an UploadBoxUploadbox Control"%}{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img5.png" Caption="Figure 2: Create an UploadBoxUploadbox Control"%}





* After you upload the files, the following screen shot is displayed. 



{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img6.png" Caption="Figure 3: Upload a file in UploadBoxUploadbox control"%}{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img7.png" Caption="Figure 3: Upload a file in UploadBoxUploadbox control"%}

![](getting-started_images\getting-started_img8.jpeg)_**Note: The above screen shot displays the UploadBoxUploadbox control that shows the files are uploaded successfully.**_

### Set Restriction for File Extension

In a real-time scenario, some file extensions are restricted. You can allow files and restrict files by using the following two properties **extensionsAllow** and **extensionsDeny** enabled in **UploadBoxUploadbox**. 

> ![](getting-started_images\getting-started_img9.jpeg)_**Note: The SaveUrl and RemoveUrl are the same as above (see step 4)**_

* Add the following code example in script section.





&lt;script type="text/javascript"&gt;

    var uploadobject;



    $(function () {



        $("#UploadDefault").ejUploadbox({

            saveUrl: "http://localhost:50510/uploadbox/saveFiles.ashx",

            removeUrl: "http://localhost:50510/uploadbox/removeFiles.ashx"

        });





        uploadobject = $("#UploadDefault").data("ejUploadbox");

        $("#upbutton1").ejButton({

            click: "allowfiletype",

        });





        $("#upbutton2").ejButton({

            click: "denyfiletype",

        });



    });





    function allowfiletype() {

        uploadobject.option(' extensionsAllow ', $("#fileallow").val());

        uploadobject.option(' extensionsDeny ', "");

    }





    function denyfiletype() {

        uploadobject.option(' extensionsAllow ', "");

        uploadobject.option(' extensionsDeny ', $("#filedeny").val());

    }

&lt;/script&gt;



* Add input elements to create elements for file extension.



![](getting-started_images\getting-started_img10.jpeg)_**Note: Add the following input elements and two button elements to give file extensions that should support uploading. This is added after step 2 in the same HTML file.**_



{% highlight html %}


<div id="targetElement">
    <table id="uploadTable">
        <tr>
            <td>
                Extensions:
            </td>
            <td></td>
        </tr>
        <tr>
            <td>
                <input type="text" id="fileallow" class="ejinputtext" placeholder="Format" />
                <input type="button" class="e-btn" id="upbutton1" value="Allow" />
            </td>
            <td></td>
        </tr>
        <tr>
            <td>
                <input type="text" id="filedeny" class="ejinputtext" placeholder="Format" />
                <input type="button" class="e-btn" id="upbutton2" value="Deny" />
            </td>
            <td>
                <div id="UploadDefault"></div>
            </td>
        </tr>
    </table>
</div><div id="sampleProperties">
    <div class="prop-grid">
        <div class="row">
            <div class="col-md-3">
                Extensions:
            </div>
        </div>
        <div class="row">
            <div class="col-md-3">
                <input type="text" id="fileallow" class="tb6 ejinputtext" placeholder="Format" />
            </div>
            <div class="col-md-3">
                <input type="button" class="e-btn" id="upbutton1" value="Allow" />
            </div>
        </div>
        <div class="row">
            <div class="col-md-3">
                <input type="text" id="filedeny" class="tb6 ejinputtext" placeholder="Format" />
            </div>
            <div class="col-md-3">
                <input type="button" class="e-btn" id="upbutton2" value="Deny" />
            </div>
        </div>
    </div>
</div>
        </div>


{% endhighlight %}



* Add the following code example in script section.



{% highlight js %}


<script type="text/javascript">
    var uploadobject;
    $(function () {
        $("#UploadDefault").ejUploadbox({
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx"
        });
        uploadobject = $("#UploadDefault").data("ejUploadbox");
        $("#upbutton1").ejButton({
            click: "allowfiletype",
        });
        $("#upbutton2").ejButton({
            click: "denyfiletype",
        });
    });
    function allowfiletype() {
        uploadobject.option('extensionsAllow', $("#fileallow").val());
        uploadobject.option('extensionsDeny', "");
    }
    function denyfiletype() {
        uploadobject.option('extensionsAllow', "");
        uploadobject.option('extensionsDeny', $("#filedeny").val());
    }
</script>


{% endhighlight %}



* Add the given styles to display the **Uploadbox** with margin alignments.

 Add the following code example in **HTML** to get the Properties panel separately,



{% highlight css %}


<style>
    #targetElement {
        width: 520px;
        height: 500px;
        margin: 0 auto;
    }
    #UploadDefault {
        float: right;
    }
    #uploadTable {
        width: 100%;
    }
    #fileallow, #filedeny {
        width: 150px;
        height: 20px;
        padding: 5px;
    }
</style> 
<script type="text/javascript">
    $("#sampleProperties").ejPropertiesPanel();
</script>



{% endhighlight %}

> ![](getting-started_images\getting-started_img11.jpeg)_**Note: You can restrict one or more files at a time by giving it as .html,.txt**_

The following screenshot displays an **UploadBoxUploadbox** control with the file extension.



![](getting-started_images\getting-started_img12.png)![](getting-started_images\getting-started_img13.png)

_Figure_ _4__:_ _UploadBox__Uploadbox_ _with setting restrictions_

The above screenshot shows the **UploadBoxUploadbox** that allows “.**htmlpng**” files and restricts “**.txt”** and “**.pnghtml”** file formats. You can give the number file formats in both allow and deny textbox elements.

### Upload Multiple Files

You can click the **Browse** button and select the file to upload multiple files in **UploadBoxUploadbox** control. You can see the selected files in **UploadBoxUploadbox** control and you can upload all the files.

The following screenshot displays an **UploadBoxUploadbox** control with multiple files.

![](getting-started_images\getting-started_img14.png)![](getting-started_images\getting-started_img15.png)

_Figure_ _5__: Upload multiple files_

## Create your first UploadBox in MVC

**ASP.NET MVC UploadBox** provides support to upload the files or photos within your webpage. From the following guidelines, you can learn how to upload the file that is used in a Resume Upload scenario. This helps you to restrict some file extensions, while uploading the resume in the server by using **UploadBox** control. The following screenshot demonstrates the functionality of **UploadBox** with file extension.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img16.png" Caption="Figure 6: UploadBox with setting restrictions"%}

In the above screenshot, you can upload a resume. It allows **.png** and **.docx** file extension. This enables you to avoid unsupported resume formats to be uploaded in the server.

**Create UploadBox widgets**

**ASP.NET MVC UploadBox** widget has built-in features like Upload multiple files, Delete files, check the status of the file, whether it shows complete or failed, and retry uploading the files.  You can easily create the **UploadBox** widget by using the following steps.

1. You can create an MVC project and add necessary assemblies, styles, and scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code example to the corresponding view page to render the UploadBox.

**[View]**

@Html.EJ().Uploadbox("UploadDefault").SaveUrl(@Url.Action("Save")).RemoveUrl(@Url.Action("Remove"))



3. Add the following Save ActionResult in your controller page.![](getting-started_images\getting-started_img17.png)

**[CS]**

public ActionResult SaveDefault(IEnumerable<HttpPostedFileBase> UploadDefault)

        {

            foreach (var file in UploadDefault)

            {

                var fileName = Path.GetFileName(file.FileName);

                var destinationPath = Path.Combine(Server.MapPath("~/App_Data"), fileName);

                file.SaveAs(destinationPath);



            }

            return Content("");

        }

    }    



4. Add the following Remove ActionResult in your controller page.

**[CS]**



public ActionResult RemoveDefault(string[] fileNames)

        {

            foreach (var fullName in fileNames)

            {

                var fileName = Path.GetFileName(fullName);

                var physicalPath = Path.Combine(Server.MapPath("~/App_Data"), fileName);

                if (System.IO.File.Exists(physicalPath))

                {

                    System.IO.File.Delete(physicalPath);

                }

            }

            return Content("");

        } 

        string physicalPath = targetFolder + "\\" + fileName;

        if (System.IO.File.Exists(physicalPath))

        {

            System.IO.File.Delete(physicalPath);

        }



    }





5. Execute the code to render the following output.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img18.png" Caption="Figure 7: UploadBox before uploading "%}

6. After file upload, the files are saved in a path. Give the path in local host as follows. Add the following code in the script.



 &lt;script src="@Url.Content("~/Scripts/properties.js")"&gt;&lt;/script&gt;



      &lt;script type="text/javascript"&gt;

          $(function () {



              $("#UploadDefault").ejUploadbox({

                  saveUrl: "http://localhost:50510/MvcApplication2/saveFiles.ashx",

                  removeUrl: "http://localhost:50510/MvcApplication2/removeFiles.ashx"

              })

          });

    &lt;/script&gt;



7. Execute the project to render the following output for the given steps. The file is being uploaded.


![](getting-started_images\getting-started_img19.png)

_Figure_ _8__:_ _UploadBox_ _after uploading_

**Set Restrictions to File Extensions**

In a real-time scenario, some file extensions are restricted. You can allow and restrict files by using the following properties **extensionsAllow** and **extensionDeny** enabled in **UploadBox**.

> ![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img20.png)_**Note: The Save and Remove actions are the same as above (see step 3 and 4)**_

1. Add the following code example in script section.

**[Script]**

&lt;script type="text/javascript"&gt;

        $(function () {

            // declaration

            $("#UploadDefault").ejUploadbox({

                saveUrl: "saveFiles.ashx",

                removeUrl: "removeFiles.ashx",

                multipleFilesSelection: true

            });

            uploadobject = $("#UploadDefault").data("ejUploadbox");

            $("#upbutton1").ejButton({

                click: "allowfiletype",

            });

            $("#upbutton2").ejButton({

                click: "denyfiletype",

            });

        });

        function allowfiletype() {

            uploadobject.option('extensionsAllow', $("#fileallow").val());

            uploadobject.option('extensionsDeny', "");

            $("#filedeny").val('');

        }

        function denyfiletype() {

            uploadobject.option('extensionsAllow', "");

            uploadobject.option('extensionsDeny', $("#filedeny").val());

            $("#fileallow").val('');

        }

    &lt;/script&gt;



2. Add input elements to create elements for file extension.

> ![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img21.png)_**Note:**_ ___**Add the following input elements and two button elements to give file extensions that supports uploading.**_ 

&lt;div class="control"&gt;

        <span>Select a file to upload &lt;/span&gt;

@Html.EJ().Uploadbox("UploadInput").SaveUrl(@Url.Action("Save")).RemoveUrl(@Url.Action("Remove")).MultipleFilesSelection(true)



        &lt;div class="prop-grid"&gt;



            &lt;div class="columns"&gt;

                Extensions:

            &lt;/div&gt;

            &lt;div class="columns"&gt;

                &lt;input type="text" id="fileallow" class="tb6 ejinputtext" placeholder="Format" /&gt;

            &lt;/div&gt;

            &lt;div class="columns"&gt;

                &lt;input type="button" class="e-btn" id="upbutton1" value="Allow" /&gt;

            &lt;/div&gt;

            &lt;div class="columns"&gt;

                &lt;input type="text" id="filedeny" class="tb6 ejinputtext" placeholder="Format" /&gt;

            &lt;/div&gt;

            &lt;div class="columns"&gt;

                &lt;input type="button" class="e-btn" id="upbutton2" value="Deny" /&gt;

            &lt;/div&gt;



        &lt;/div&gt;

    &lt;/div&gt;



3. Add the following code example in HTML to apply CSS styles in your page.

&lt;style type="text/css"&gt;

        .prop-grid {

            border: 1px solid lightgray;            

            width: 200px;

            height: 200px;

            margin-top: 20px;

            border-radius:2px;

        }



        .control {

            margin:20px 0 0 40px;            

        }



        .control span {

            margin-bottom: 10px;

         }



        .columns {

            display: block;

            width: 50%;            

            padding: 5px;

        }

    &lt;/style&gt;

> ![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img22.png)_**Note: You can restrict one or more files at a time by giving it as .html, .txt**_

The following screenshot displays an UploadBox control with the file extension

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img23.png" Caption="Figure 9: UploadBox with setting restrictions"%}

In UploadBox control, either you can allow only files with specified extension by using **extensionAllow** property or deny only files with specified extension by using **extensionDeny** property.

The above screenshot illustrates the **UploadBox** that allows .**docx** and **.png** files.

**Upload Multiple Files**

To upload multiple files in **UploadBox** control, click the **Browse** button to select files. The selected files appear in the **UploadBox** control and you can upload all the files.

The following screenshot displays an **UploadBox** control with multiple files selected.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img24.png" Caption="Figure 10: Multiple files uploaded in UploadBox control"%}

## Create your first UploadBox in ASP.NET

**ASP.NET WebForms UploadBox** provides support to upload the files or photos within your webpage. From the following guidelines, you can learn how to upload the file that is used in a Resume Upload scenario. This helps you to restrict some file extensions, while uploading the resume in the server by using **UploadBox** control. The following screenshot demonstrates the functionality of **UploadBox** with file extension.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img25.png" Caption="Figure 11: UploadBox"%}

In the above screenshot, you can upload a resume. It allows **.png** and .docx file extension. This enables you to avoid unsupported resume formats to be uploaded in server.

**Create UploadBox widgets**

**ASP.NET UploadBox** widget has built-in features like Upload multiple files, Delete files, check the status of the file, whether it shows complete or failed, and retry uploading the files.  You can easily create the **UploadBox** by using the following steps.

4. You can create a Web project and add necessary assemblies, styles, and scripts with the help of the given [ASP-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

5. ![](getting-started_images\getting-started_img26.png)Add the following code example to the aspx page to render the UploadBox.



**[ASPX]**  

&lt;div class="posupload"&gt;

<b>Select a file to upload</b>

        &lt;br /&gt;&lt;br /&gt;

&lt;ej:UploadBox ID="Upload1" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" AutoUpload="false"&gt;&lt;/ej:UploadBox&gt;

&lt;/div&gt;



6. Add the given styles to show the UploadBox with the margin alignments.

**[CSS]**

    &lt;style class="text/css"&gt;

        .posupload

        {

            margin-left: 20px;

            margin-top: 20px;

        }



        .control

        {

            margin-left: 15px;

        }

    &lt;/style&gt;



7. Add the handlers to save and remove the files that you have uploaded by using upload box. 

1. Create a new handler file ”.ashx” and save as **saveFile.ashx** and add the following code in it. 

#SaveFiles.ashx.cs

public void ProcessRequest(HttpContext context)

    {

        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");

        if (!Directory.Exists(targetFolder))

        {

            Directory.CreateDirectory(targetFolder);

        }

        HttpRequest request = context.Request;

        HttpFileCollection uploadedFiles = context.Request.Files;

        if (uploadedFiles != null && uploadedFiles.Count > 0)

        {

            for (int i = 0; i < uploadedFiles.Count; i++)

            {

                if (uploadedFiles[i].FileName != null && uploadedFiles[i].FileName != "")

                {

                    string fileName = uploadedFiles[i].FileName;

                    int indx = fileName.LastIndexOf("\\");

                    if (indx > -1)

                    {

                        fileName = fileName.Substring(indx + 1);

                    }

                    uploadedFiles[i].SaveAs(targetFolder + "\\" + fileName);

                }

            }

        }



    }    





2. Create a new handler file ”.ashx” and save as **removeFile.ashx** and add the following code in it. 

#removeFiles.ashx.cs

public void ProcessRequest(HttpContext context)

    {

        System.Collections.Specialized.NameValueCollection s = context.Request.Params;

        string fileName = s["fileNames"];

        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");

        if (Directory.Exists(targetFolder))

        {

            string physicalPath = targetFolder + "\\" + fileName;

            if (System.IO.File.Exists(physicalPath))

            {

                System.IO.File.Delete(physicalPath);

            }

        }     



    }





8. Execute the code to render the following output.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img27.png" Caption="Figure 12: UploadBox before uploading"%}

9. Execute the project to see the following output for the given steps. The file has been uploaded. 

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img28.png" Caption="Figure 13: UploadBox after uploading"%}

**Set Restrictions to File Extensions**

In a real-time scenario, some file extensions are restricted. You can allow files and restrict files by using the following two properties **fileallow** and **filedeny** enabled in **UploadBox**. 

> ![](getting-started_images\getting-started_img29.jpeg)_**Note: The SaveUrl and RemoveUrl are the same as above (see step 4)**_

10. Add the following code example in script section.

**[Script]**

&lt;script type="text/javascript"&gt;

        var uploadobject;

        function allowfiletype() {

            uploadobject = $("#&lt;%=Upload1.ClientID%&gt;").data("ejUploadbox");

            uploadobject.option('extensionsAllow', $("#fileallow").val());

            uploadobject.option('extensionsDeny', "");

            $("#filedeny").val('');

        }

        function denyfiletype() {

            uploadobject = $("#&lt;%=Upload1.ClientID%&gt;").data("ejUploadbox");

            uploadobject.option('extensionsAllow', "");

            uploadobject.option('extensionsDeny', $("#filedeny").val());

            $("#fileallow").val('');

        }

    &lt;/script&gt;



11. Add input elements to create elements for file extension.

![](getting-started_images\getting-started_img30.jpeg)_**Note: Add the following input elements and two button elements to give file extensions that should support uploading.**_



**[ASPX]**

    &lt;div class="posupload"&gt;

        <b>Select a file to upload</b>

        &lt;br /&gt;

        &lt;br /&gt;

        <ej:UploadBox ID="Upload1" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx"

            ExtensionsAllow=".docx" ExtensionsDeny=".pdf" runat="server">

        &lt;/ej:UploadBox&gt;

        &lt;label id="extdetails"&gt;

            By default, it allow .docx format and deny .pdf format files

        &lt;/label&gt;

    &lt;/div&gt;

    &lt;br /&gt;

    &lt;br /&gt;

    &lt;div style="margin-left: 15px"&gt;

        <b>Setting Restriction</b>&lt;/div&gt;

    &lt;div class="allow_deny"&gt;

        &lt;div class="row"&gt;

            &lt;div class="col-md-3"&gt;

                Extensions:

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;div class="row"&gt;

            &lt;div class="col-md-3"&gt;

                &lt;input type="text" id="fileallow" class="tb6 ejinputtext" /&gt;

            &lt;/div&gt;

            &lt;div class="col-md-3"&gt;

                <ej:Button ID="upbutton1" Type="Button" CssClass="e-btn" Text="Allow" ClientSideOnClick="allowfiletype"

                    runat="server">

                &lt;/ej:Button&gt;

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;div class="row"&gt;

            &lt;div class="col-md-3"&gt;

                &lt;input type="text" id="filedeny" class="tb6 ejinputtext" /&gt;

            &lt;/div&gt;

            &lt;div class="col-md-3"&gt;

                <ej:Button ID="upbutton2" Type="Button" CssClass="e-btn" Text="Deny" ClientSideOnClick="denyfiletype"

                    runat="server">

                &lt;/ej:Button&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;





12. Add the following Styles in aspx page to **allow** or **deny** files.

**[CSS]**

&lt;style class="text/css"&gt;

        .posupload

        {

            margin-left: 20px;

            margin-top: 20px;

        }



        .control

        {

            margin-left: 15px;

        }



        .ctrl

        {

            border: 1px solid #ccc;

            border-radius: 10px;

            width: 150px;

            padding: 50px 100px 50px 100px;

            float: left;

        }



        .allow_deny

        {

            border: 1px solid #ccc;

            border-radius: 10px;

            float: left;

            margin: 10px;

            padding: 15px;

        }

    &lt;/style&gt;



13. Execute the code to render the following output with the file extensions.

> ![](getting-started_images\getting-started_img31.jpeg)_**Note: You can restrict one or more files at a time by giving it as .html,.txt**_

In **UploadBox** control, either you can allow only files with specified extension by using **extensionAllow** property or deny only files with specified extension by using **extensionDeny** property.

The following screenshot displays an **UploadBox** control with the file extension.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img32.png" Caption="Figure 14: UploadBox with file restrictions"%}

**Upload Multiple Files**

To upload multiple files in **UploadBox** control, click the **Browse** button to select files. The selected files appear in the **UploadBox** control and you can upload all the files.

The following screenshot displays an **UploadBox** control with multiple files selected.

{% include image.html url="\js\UploadBox\getting-started_images\getting-started_img33.png" Caption="Figure 15: Multiple files uploaded in UploadBox control"%}

