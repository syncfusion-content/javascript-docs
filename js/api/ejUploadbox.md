---
layout: post
title: ejUploadbox
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Uploadbox control.










$(element).ejUploadbox<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Create Uploadbox
$('#uploadbox1').ejUploadbox();         
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.uploadbox.js


* module:ej.dialog.js


* module:ej.scroller.js


* module:ej.draggable.js




## Members








### allowDragAndDrop<span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddrop}








Enables the file drag and drop support to the Uploadbox control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the allowDragAndDrop API value on initialization.
    $("#uploadbox1").ejUploadbox({ allowDragAndDrop: false });        
</script>{% endhighlight %}







### asyncUpload<span class="type-signature type boolean">boolean</span>
{:#members:asyncupload}








Uploadbox supports both synchronous and asynchronous upload. This can be achieved by using the asyncUpload property.

Synchronous Upload -
Selected files are sent to the application form post action.	

Asynchronous Upload -
Selected files are sent to the server handler by using the AJAX Post.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ asyncUpload: false });   
</script>{% endhighlight %}







### autoUpload<span class="type-signature type boolean">boolean</span>
{:#members:autoupload}








Uploadbox supports auto uploading of files after the file selection is done.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the autoUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ autoUpload: true });     
</script>{% endhighlight %}







### buttonText<span class="type-signature type string">object</span>
{:#members:buttontext}








Sets the text for each action button.




Default Value:
{:.param}






* {browse: "Browse", upload: "Upload", cancel: "Cancel", close: "Close"}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File", upload: "Upload the File", cancel: "Cancel the Upload"} });        

</script>{% endhighlight %}







### buttonText.browse<span class="type-signature type string">String</span>
{:#members:buttontext-browse}








Sets the text for the browse button.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File" }});
</script>{% endhighlight %}







### buttonText.cancel<span class="type-signature type string">String</span>
{:#members:buttontext-cancel}








Sets the text for the cancel button.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText.cancel API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: { cancel: "Cancel"});        

</script>{% endhighlight %}







### buttonText.Close<span class="type-signature type string">String</span>
{:#members:buttontext-close}








Sets the text for the close button.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText.Close API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: {Close: "close"} });        

</script>{% endhighlight %}







### buttonText.upload<span class="type-signature type string">String</span>
{:#members:buttontext-upload}








Sets the text for the Upload button inside the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { upload: "Upload the File" }});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Sets the root class for the Uploadbox control theme. This cssClass API helps to use custom skinning option for the Uploadbox button and dialog content.





Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the cssClass API value on initialization.
$("#uploadbox1").ejUploadbox({cssClass : "gradient- purple"});        

</script>{% endhighlight %}







### customFileDetails<span class="type-signature type object">object</span>
{:#members:customfiledetails}








Specifies the custom file details in the dialog popup on initialization.




Default Value:
{:.param}






* { title:true, name:true, size:true, status:true, action:true}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the customFileDetails API value on initialization.
$("#uploadbox1").ejUploadbox({customFileDetails:{ title:true, name:true, size:true, status:true, action:true}});        

</script>{% endhighlight %}







### customFileDetails.action<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-action}








Enables the file upload interactions like remove/cancel in File details of the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the customFileDetails.action API value on initialization.
$("#uploadbox1").ejUploadbox({customFileDetails:{action:true}});        

</script>{% endhighlight %}







### customFileDetails.name<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-name}








Enables the name in the File details of the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { name: true }});
</script>{% endhighlight %}







### customFileDetails.size<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-size}








Enables or disables the File size details of the dialog popup.

Note: Details of the File Size is available from IE10+ browser version.






Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { size:true}});
</script>{% endhighlight %}







### customFileDetails.status<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-status}








Enables or disables the file uploading status visibility in the dialog file details content.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { status: true}});
</script>{% endhighlight %}







### customFileDetails.title<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-title}








Enables the title in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { title: true }});
</script>{% endhighlight %}







### dialogAction<span class="type-signature type object">object</span>
{:#members:dialogaction}








Specifies the actions for dialog popup while initialization.




Default Value:
{:.param}






* { modal:false, closeOnComplete:false, content:null, drag:true}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the  dialogAction API value 
        $("#uploadbox1").ejUploadbox({ dialogAction:{ modal:false, closeOnComplete:false,resize: false, drag:true, content:"#controlid"}});     
</script>{% endhighlight %}







### dialogAction.closeOnComplete<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-closeoncomplete}








Once uploaded successfully, the dialog popup closes immediately.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { closeOnComplete: true }});
</script>{% endhighlight %}







### dialogAction.content<span class="type-signature type string">string</span>
{:#members:dialogaction-content}








Sets the content container option to the Uploadbox dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the dialogAction.content API value on initialization.
$("#uploadbox1").ejUploadbox({dialogAction:{ content: "#uploadbox1"}});        

</script>{% endhighlight %}







### dialogAction.drag<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-drag}








Enables the drag option to the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { drag: true }});
</script>{% endhighlight %}







### dialogAction.modal<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-modal}








Enables or disables the Uploadbox dialog’s modal property to the dialog popup.


Note: dialogAction.modal property does not work in synchronous file upload.






Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { modal: true }});
</script>{% endhighlight %}







### dialogPosition<span class="type-signature type object">object</span>
{:#members:dialogposition}








Displays the Uploadbox dialog at the given X and Y positions. X: Dialog sets the left position value. Y: Dialog sets the top position value.




Default Value:
{:.param}






* Null








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogPosition API value during initialization
        $("#uploadbox1").ejUploadbox({dialogPosition: { X: 300, Y: 10 }});
</script>{% endhighlight %}







### dialogText<span class="type-signature type object">object</span>
{:#members:dialogtext}








Property for applying the text to the Dialog title and content headers.




Default Value:
{:.param}






* { title: "Upload Box", name: "Name", size: "Size", status: "Status"}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the  dialogText API value during initialization
        $("#uploadbox1").ejUploadbox({ dialogText:{title:"Upload File List",name:"File Name",size:"File Size",status:"File Status" }});
</script>{% endhighlight %}







### dialogText.name<span class="type-signature type string">String</span>
{:#members:dialogtext-name}








Sets the uploaded file’s Name (header text) to the Dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { name: "Name" }});
</script>{% endhighlight %}







### dialogText.size<span class="type-signature type string">String</span>
{:#members:dialogtext-size}








Sets the upload file Size (header text) to the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { size: "Size" }});
</script>{% endhighlight %}







### dialogText.status<span class="type-signature type string">String</span>
{:#members:dialogtext-status}








Sets the upload file Status (header text) to the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { status: "Status" }});
</script>{% endhighlight %}







### dialogText.title<span class="type-signature type string">String</span>
{:#members:dialogtext-title}








Sets the title text of the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { title: "Upload Box" }});
</script>{% endhighlight %}







### dropAreaText<span class="type-signature type string">string</span>
{:#members:dragareatext}








The dropAreaText is displayed when the draganddrop support is enabled in the Uploadbox control.




Default Value:
{:.param}






* "Drop files or click to upload"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dragAreaText API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaText:"Drop files or click to upload"});
</script> {% endhighlight %}







### dropAreaHeight<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>
{:#members:dropareaheight}








Specifies the dropAreaHeight when the draganddrop support is enabled in the Uploadbox control.




Default Value:
{:.param}






* "100%"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaHeight:"100%"}); 
</script>{% endhighlight %}







### dropAreaWidth<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>
{:#members:dropareawidth}








Specifies the dropAreaWidth when the draganddrop support is enabled in the Uploadbox control.




Default Value:
{:.param}






* "100%"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaWidth:"100%");   
</script> {% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}







Based on the property value, Uploadbox is enabled or disabled.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the enabled API value during initialization
        $("#uploadbox1").ejUploadbox({ enabled: false });       
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Sets the right-to-left direction property for the Uploadbox control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the enableRTL API value during initialization
        $("#uploadbox1").ejUploadbox({ enableRTL: true});       
</script> {% endhighlight %}







### extensionsAllow<span class="type-signature type string">string</span>
{:#members:extensionsallow}








Only the files with the specified extension is allowed to upload. This is mentioned in the string format.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsAllow: ".zip"  });     
</script> {% endhighlight %}







### extensionsDeny<span class="type-signature type string">string</span>
{:#members:extensionsdeny}








Only the files with the specified extension is denied for upload. This is mentioned in the string format.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsDeny API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsDeny: ".zip"  });      
</script> {% endhighlight %}







### fileSize<span class="type-signature type number">number</span>
{:#members:filesize}








Sets the maximum size limit for uploading the file. This is mentioned in the number format.

Note: fileSize represents the size of the individual file.





Default Value:
{:.param}






* 31457280








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ fileSize: 31457280  });  
</script> {% endhighlight %}







### height<span class="type-signature type string">string</span>
{:#members:height}








Sets the height of the browse button.




Default Value:
{:.param}






* 35px








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the height API value during initialization
        $("#uploadbox1").ejUploadbox({ height:"40px"});
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Configures the culture data and sets the culture to the Uploadbox.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
ej.Uploadbox.Locale["nl-BE"] = {
        buttonText: {
            upload: "uploaden",
            browse: "Blader",
            cancel: "Annuleer",
            close: "dicht"
        },
        dialogText: {
            title: "Upload Box",
            name: "naam",
            size: "grootte",
            status: "toestand"
        },
        dropAreaText: "Drop bestanden of klik te uploaden ",
        filedetail: "Het geselecteerde bestand is te groot . Selecteer een bestand in de geldige grootte.",
        denyError: "Bestanden met #Extension extensies zijn niet toegestaan.",
        allowError: "Alleen bestanden met #Extension extensies zijn toegestaan.",
        cancelToolTip: "Annuleer",
        removeToolTip: "verwijderen",
        retryToolTip: "opnieuw proberen",
        completedToolTip: "voltooid",
        failedToolTip: "gefaald",
        closeToolTip: "dicht"
    }; 

    //Sets the locale API value on initialization.
$("#uploadbox1").ejUploadbox({ locale: "nl-BE" });        

</script>{% endhighlight %}







### multipleFilesSelection<span class="type-signature type boolean">boolean</span>
{:#members:multiplefilesselection}








Enables multiple file selection for upload.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the multipleFilesSelection API value during initialization
        $("#uploadbox1").ejUploadbox({ multipleFilesSelection: true });
</script> {% endhighlight %}







### pushFile<span class="type-signature type object">object</span>
{:#members:pushfile}








You can push the file to the Uploadbox in the client-side of the XHR supported browsers alone.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Pushes the new files via API value during initialization
        $("#uploadbox1").ejUploadbox({ pushFile: files });      
</script>{% endhighlight %}







### removeUrl<span class="type-signature type string">string</span>
{:#members:removeurl}








Specifies the remove action to be performed after the file uploading is completed. Here, mention the server address for removal.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the removeUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ removeUrl: "http://js.syncfusion.com/demos/beta/removeFiles.ashx"});     
</script>{% endhighlight %}







### saveUrl<span class="type-signature type string">string</span>
{:#members:saveurl}








Specifies the save action to be performed after the file is pushed for uploading. Here, mention the server address to be saved. 




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the saveUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx"}); 
</script>{% endhighlight %}







### showBrowseButton<span class="type-signature type boolean">boolean</span>
{:#members:showbrowsebutton}








Enables the browse button support to the Uploadbox control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the showBrowseButton API value during initialization
        $("#uploadbox1").ejUploadbox({ showBrowseButton:true}); 
</script> {% endhighlight %}







### showFileDetails<span class="type-signature type boolean">boolean</span>
{:#members:showfiledetails}








Specifies the file details to be displayed when selected for uploading. This can be done when the showFileDetails is set to true.



Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the showFileDetails API value during initialization
        $("#uploadbox1").ejUploadbox({ showFileDetails: false });       
</script>{% endhighlight %}







### uploadName<span class="type-signature type string">string</span>
{:#members:uploadname}








Sets the name for the Uploadbox control. This API helps to Map the action in code behind to retrieve the files.





Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>

    //Sets the uploadName API value on initialization.
  $("#uploadbox1").ejUploadbox({saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx" ,uploadName: "Uploadbox", });      

</script>{% endhighlight %}







### width<span class="type-signature type string">string</span>
{:#members:width}








Sets the width of the browse button.




Default Value:
{:.param}






* 100px








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the width API value during initialization
        $("#uploadbox1").ejUploadbox({ width:"120px"});
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








The destroy method destroys the control and brings the control to a pre-init state. All the events of the Upload control is bound by using this._on unbinds automatically.  





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Destroys Upload
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.destroy(); // destroy the Upload control
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Destroys the Upload control
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("destroy");        
</script>{% endhighlight %}







### disable<span class="signature">()</span>
{:#methods:disable}








Disables the Uploadbox control





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Disables the Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.disable(); // disable the Uploadbox
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Disables the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("disable");        
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








Enables the Uploadbox control





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Enables the Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.enable(); // enable the Uploadbox
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Enables the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("enable"); 
</script>{% endhighlight %}





## Events








### begin
{:#events:begin}








Fires when the upload progress begins.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">To pass additional information to the server.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Selected FileList Object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Begin event for Uploadbox
$("#uploadbox1").ejUploadbox({
   begin: function (args) {}
});   
</script>{% endhighlight %}







### cancel
{:#events:cancel}








Fires when the upload progress is cancelled.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
fileStatus{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Canceled FileList Object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Cancel event for Uploadbox
$("#uploadbox1").ejUploadbox({
   cancel: function (args) {}
});</script>{% endhighlight %}







### complete
{:#events:complete}








Fires when the file upload progress is completed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
e{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">AJAX event argument for reference.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Uploaded file list.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
responseText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">response from the server.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
xhr{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">XHR-AJAX Object for reference.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Complete event for Uploadbox
$("#uploadbox1").ejUploadbox({
   complete: function (args) {}
});   
</script>   {% endhighlight %}






### success
{:#events:complete}








Fires when the file upload progress is completed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
responseText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">response from the server.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
e{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">AJAX event argument for reference.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
success{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">successfully uploaded files list.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Uploaded file list.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
xhr{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">XHR-AJAX Object for reference.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Complete event for Uploadbox
$("#uploadbox1").ejUploadbox({
   complete: function (args) {}
});   
</script>   {% endhighlight %}








### create
{:#events:create}








Fires when the Uploadbox control is created.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//create event for Uploadbox
$("#uploadbox1").ejUploadbox({
   create: function (args) {}
});   
</script>   {% endhighlight %}







### destroy
{:#events:destroy}








Fires when the Uploadbox control is destroyed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Destroy event for Uploadbox
$("#uploadbox1").ejUploadbox({
   destroy: function (args) {}
});  
</script>    {% endhighlight %}







### error
{:#events:error}








Fires when the Upload process ends in Error.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
error{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">details about the error information.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">error event action details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the file details of the file uploaded</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//error event for Uploadbox
$("#uploadbox1").ejUploadbox({
   error: function (args) {}
});  
</script>    {% endhighlight %}







### fileSelect
{:#events:fileselect}








Fires when the file is selected for upload successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns Selected FileList objects</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="uploadbox1"></div> 
 
<script> 
//fileSelect event for Uploadbox
$("#uploadbox1").ejUploadbox({
   fileSelect: function (args) {}
});  
</script>    {% endhighlight %}







### remove
{:#events:remove}








Fires when the uploaded file is removed successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Uploadbox
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
fileStatus{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the file details of the file object</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//remove event for Uploadbox
$("#uploadbox1").ejUploadbox({
   remove: function (args) {}
});  
</script>    {% endhighlight %}




