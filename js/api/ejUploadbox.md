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








Enable the dragAndDrop support to the Uploadbox control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set allowDragAndDrop API value during initialization
        $("#uploadbox1").ejUploadbox({ allowDragAndDrop:false});        
</script> {% endhighlight %}







### asyncUpload<span class="type-signature type boolean">boolean</span>
{:#members:asyncupload}








Uploadbox supports both synchronous and asynchronous upload. This can be achieved by this property asyncUpload.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ asyncUpload: false });   
</script>{% endhighlight %}







### autoUpload<span class="type-signature type boolean">boolean</span>
{:#members:autoupload}








Uploadbox supports auto uploading of files after the file selection is done.The auto upload is performed if autoUpload is set to true.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set autoUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ autoUpload: true });     
</script>{% endhighlight %}







### buttonText<span class="type-signature type string">string</span>
{:#members:buttontext}








Specifies the text content for Uploadbox browse button while initialization.




Default Value:
{:.param}






* "Browse"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  browseButtonText API value 
        $("#uploadbox1").ejUploadbox({ buttonText:{ browse:"Choose File", upload:"Upload the File", cancel:"Cancel the Upload"}});      
</script>{% endhighlight %}







### buttonText.browse<span class="type-signature type string">String</span>
{:#members:buttontext-browse}








Sets the text for the Browse button.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File" }});
</script>{% endhighlight %}







### buttonText.cancel<span class="type-signature type string">String</span>
{:#members:buttontext-cancel}








Sets the text for the Cancel button inside the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { cancel: "Cancel the Upload" }});
</script>{% endhighlight %}







### buttonText.Close<span class="type-signature type string">String</span>
{:#members:buttontext-close}








Sets the text for the Close button inside the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { close: "close dialog" }});
</script>{% endhighlight %}







### buttonText.upload<span class="type-signature type string">String</span>
{:#members:buttontext-upload}








Sets the text for the Upload button inside the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { upload: "Upload the File" }});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Set the root class for Uploadbox control theme. This cssClass API helps to use custom skinning option for Uploadbox control.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set cssClass  API value during initialization
        $("#uploadbox1").ejUploadbox({ cssClass : "gradient-lime"});    
</script> {% endhighlight %}







### customFileDetails<span class="type-signature type object">object</span>
{:#members:customfiledetails}








Specifies the custom file details in dialog popup while initialization.




Default Value:
{:.param}






* customFileDetails:{ title:true, name:true, size:true, status:true, action:true}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  customFileDetails API value 
        $("#uploadbox1").ejUploadbox({ customFileDetails:{ title:true, name:true, size:true, status:true, action:true}});       
</script>{% endhighlight %}







### customFileDetails.action<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-action}








Enable the remove/ cancel action in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { action: true}});
</script>{% endhighlight %}







### customFileDetails.name<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-name}








Enable the name in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { name: true }});
</script>{% endhighlight %}







### customFileDetails.size<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-size}








Enable the size in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { size:true}});
</script>{% endhighlight %}







### customFileDetails.status<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-status}








Enable the status in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { status: true}});
</script>{% endhighlight %}







### customFileDetails.title<span class="type-signature type boolean">boolean</span>
{:#members:customfiledetails-title}








Enable the title in File details for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { title: true }});
</script>{% endhighlight %}







### dialogAction<span class="type-signature type object">object</span>
{:#members:dialogaction}








Specifies the actions for dialog popup while initialization.




Default Value:
{:.param}






* dialogAction:{ modal:false, closeOnComplete:false, content:null, drag:true}








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  dialogAction API value 
        $("#uploadbox1").ejUploadbox({ dialogAction:{ modal:false, closeOnComplete:false,resize: false, drag:true, content:"#controlid"}});     
</script>{% endhighlight %}







### dialogAction.closeOnComplete<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-closeoncomplete}








This will close the File details for the dialog popup once upload has performed successfully.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { closeOnComplete: true }});
</script>{% endhighlight %}







### dialogAction.content<span class="type-signature type string">string</span>
{:#members:dialogaction-content}








set the content Container option for File details of dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { content: "#uploadbox1" }});
</script>{% endhighlight %}







### dialogAction.drag<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-drag}








Enable the drag option for File details of dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { drag: true }});
</script>{% endhighlight %}







### dialogAction.modal<span class="type-signature type boolean">boolean</span>
{:#members:dialogaction-modal}








set the modal property for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { modal: true }});
</script>{% endhighlight %}







### dialogPosition<span class="type-signature type jsonobject">JSONobject</span>
{:#members:dialogposition}








Displays the uploadbox dialog window at the given X and Y position. X: Dialog set the left position value. Y: Dialog set the top position value.




Default Value:
{:.param}






* Null








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dialogPosition API value during initialization
        $("#uploadbox1").ejUploadbox({dialogPosition: { X: 300, Y: 10 }});
</script>{% endhighlight %}







### dialogText<span class="type-signature type string">string</span>
{:#members:dialogtext}








Sets the text for the inside the dialog popup.




Default Value:
{:.param}






* UploadBox








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  dialogText API value during initialization
        $("#uploadbox1").ejUploadbox({ dialogText:{title:"Upload File List",name:"File Name",size:"File Size",status:"File Status" }});
</script>{% endhighlight %}







### dialogText.name<span class="type-signature type string">String</span>
{:#members:dialogtext-name}








Sets the Name text for the dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { name: "Name" }});
</script>{% endhighlight %}







### dialogText.size<span class="type-signature type string">String</span>
{:#members:dialogtext-size}








Sets the Size text for dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { size: "Size" }});
</script>{% endhighlight %}







### dialogText.status<span class="type-signature type string">String</span>
{:#members:dialogtext-status}








Sets the Status text for dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { status: "Status" }});
</script>{% endhighlight %}







### dialogText.title<span class="type-signature type string">String</span>
{:#members:dialogtext-title}








Sets the title text dialog popup.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { title: "Upload Box" }});
</script>{% endhighlight %}







### dragAreaText<span class="type-signature type string">string</span>
{:#members:dragareatext}








To specify the text to be displayed when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "Drop files or click to upload"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dragAreaText API value during initialization
        $("#uploadbox1").ejUploadbox({ dragAreaText:"Drop files or click to upload"});  
</script> {% endhighlight %}







### dropAreaHeight<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>
{:#members:dropareaheight}








To specify the dropareaheight when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "100%"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaHeight:"100%"}); 
</script> {% endhighlight %}







### dropAreaWidth<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>
{:#members:dropareawidth}








To specify the dropareawidth when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "100%"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaWidth:"100%");   
</script> {% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








Enables or disables Uploadbox based on boolean value.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set enabled API value during initialization
        $("#uploadbox1").ejUploadbox({ enabled: false });       
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Specifies the Right to Left direction property for Uploadbox control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set enableRTL API value during initialization
        $("#uploadbox1").ejUploadbox({ enableRTL: true});       
</script> {% endhighlight %}







### extensionsAllow<span class="type-signature type string">string</span>
{:#members:extensionsallow}








Specifies the file extension to allow for uploading the file while initialization. This could be mentioned in string format.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsAllow: ".zip"  });     
</script> {% endhighlight %}







### extensionsDeny<span class="type-signature type string">string</span>
{:#members:extensionsdeny}








Specifies the file extension to deny for uploading the file while initialization. This could be mentioned in string format.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set extensionsDeny API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsDeny: ".zip"  });      
</script> {% endhighlight %}







### fileSize<span class="type-signature type number">number</span>
{:#members:filesize}








Specifies the file size for uploading the file while initialization. This could be mentioned in number format.




Default Value:
{:.param}






* 31457280








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ fileSize: 31457280  });  
</script> {% endhighlight %}







### height<span class="type-signature type string">string</span>
{:#members:height}








Sets the browse button height.




Default Value:
{:.param}






* 35px








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set height API value during initialization
        $("#uploadbox1").ejUploadbox({ height:"40px"});
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Sets the culture in uploadbox.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set  asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ locale: vi-VN });        
</script>{% endhighlight %}







### multipleFilesSelection<span class="type-signature type boolean">boolean</span>
{:#members:multiplefilesselection}








Enables to select multiple files




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set multipleFilesSelection API value during initialization
        $("#uploadbox1").ejUploadbox({ multipleFilesSelection: false });
</script> {% endhighlight %}







### pushFile<span class="type-signature type data">data</span>
{:#members:pushfile}








We can push the file into upload box in client side in xhr supported browsers alone.




Default Value:
{:.param}






* files- rawfiles








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To push new files via API value during initialization
        $("#uploadbox1").ejUploadbox({ pushFile: files });      
</script>{% endhighlight %}







### removeUrl<span class="type-signature type string">string</span>
{:#members:removeurl}








Specifies the remove action which has to be performed after the file uploading is completed. Here we have to mention the server address which has to perform this action.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set removeUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ removeUrl: "http://js.syncfusion.com/demos/beta/removeFiles.ashx"});     
</script>{% endhighlight %}







### saveUrl<span class="type-signature type string">string</span>
{:#members:saveurl}








Specifies the save action which has to be performed after the file is pushed for uploading. Here we have to mention the server address which has to perform this action.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set saveUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx"}); 
</script>{% endhighlight %}







### showBrowseButton<span class="type-signature type boolean">boolean</span>
{:#members:showbrowsebutton}








Enable the browse button support to the Uploadbox control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set showBrowseButton API value during initialization
        $("#uploadbox1").ejUploadbox({ showBrowseButton:true}); 
</script> {% endhighlight %}







### showFileDetails<span class="type-signature type boolean">boolean</span>
{:#members:showfiledetails}








Specifies to display the file details of files while selected for uploading can be done when showFileDetails set to true.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set showFileDetails API value during initialization
        $("#uploadbox1").ejUploadbox({ showFileDetails: false });       
</script>{% endhighlight %}







### uploadName<span class="type-signature type string">string</span>
{:#members:uploadname}








Set the Name for Uploadbox control . This API helps to Map the action in code behind to retrieve the files.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set uploadName property value during initialization
        $("#uploadbox1").ejUploadbox({ uploadName : "Uploadbox"});      
</script> {% endhighlight %}







### width<span class="type-signature type string">string</span>
{:#members:width}








Sets the browse button width.




Default Value:
{:.param}






* 100px








Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set width API value during initialization
        $("#uploadbox1").ejUploadbox({ width:"120px"});
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the Upload control all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Destroy Upload
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.destroy(); // destroy the Upload control
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// destroy the Upload control
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("destroy");        
</script>{% endhighlight %}







### disable<span class="signature">()</span>
{:#methods:disable}








To disable the Uploadbox control





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Disable Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.disable(); // disable the Uploadbox
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// disable the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("disable");        
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








To enable the Uploadbox control





Example
{:.example}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// enable Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.enable(); // enable the Uploadbox
</script>{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// enable the Uploadbox
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
//begin event for Uploadbox
$("#uploadbox1").ejUploadbox({
   begin: function (args) {}
});   
</script>   {% endhighlight %}







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
//cancel event for Uploadbox
$("#uploadbox1").ejUploadbox({
   cancel: function (args) {}
});
</script>     {% endhighlight %}







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
<tr>
<td class="name">{% highlight html %}
files{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns file entries and its details</td>
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
//complete event for Uploadbox
$("#uploadbox1").ejUploadbox({
   complete: function (args) {}
});   
</script>   {% endhighlight %}







### create
{:#events:create}








Fires when Uploadbox control is created.

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
//create event for Uploadbox
$("#uploadbox1").ejUploadbox({
   create: function (args) {}
});   
</script>   {% endhighlight %}







### destroy
{:#events:destroy}








Fires when Uploadbox control is destroyed.

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
//destroy event for Uploadbox
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
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the action name</td>
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
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
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




