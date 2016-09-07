---
layout: post
title: Properties, Methods and Events of ejUploadbox Widget
description: API reference for ejUploadbox
documentation: API
platform: js
keywords: Uploadbox, ejUploadbox, syncfusion, Uploadbox api 
---

# ejUploadbox





The Uploadbox control supports uploading files into the designated server, regardless of the file format and size. The Uploadbox control helps you with the selection of files to upload to the server. 








#### Syntax

{% highlight javascript %}

$(element).ejUploadbox()

{% endhighlight %}













#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Create Uploadbox
$('#uploadbox1').ejUploadbox();         
</script>

{% endhighlight %}







#### Requires



* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.uploadbox.js


* module:ej.dialog.js


* module:ej.scroller.js


* module:ej.draggable.js




## Members








### allowDragAndDrop `boolean`
{:#members:allowdraganddrop}








Enables the file drag and drop support to the Uploadbox control.




#### Default Value







* false








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the allowDragAndDrop API value on initialization.
    $("#uploadbox1").ejUploadbox({ allowDragAndDrop: false });        
</script>

{% endhighlight %}







### asyncUpload `boolean`
{:#members:asyncupload}








Uploadbox supports both synchronous and asynchronous upload. This can be achieved by using the asyncUpload property.

Synchronous Upload -
Selected files are sent to the application form post action.	

Asynchronous Upload -
Selected files are sent to the server handler by using the AJAX Post.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ asyncUpload: false });   
</script>

{% endhighlight %}







### autoUpload `boolean`
{:#members:autoupload}








Uploadbox supports auto uploading of files after the file selection is done.




#### Default Value







* false








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the autoUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ autoUpload: true });     
</script>

{% endhighlight %}







### buttonText `object`
{:#members:buttontext}








Sets the text for each action button.




#### Default Value







* {browse: "Browse", upload: "Upload", cancel: "Cancel", close: "Close"}








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File", upload: "Upload the File", cancel: "Cancel the Upload"} });        

</script>

{% endhighlight %}







### buttonText.browse `string`
{:#members:buttontext-browse}








Sets the text for the browse button.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File" }});
</script>

{% endhighlight %}







### buttonText.cancel `string`
{:#members:buttontext-cancel}








Sets the text for the cancel button.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText.cancel API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: { cancel: "Cancel"});        

</script>
{% endhighlight %}







### buttonText.Close `string`
{:#members:buttontext-close}








Sets the text for the close button.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the buttonText.Close API value on initialization.
$("#uploadbox1").ejUploadbox({ buttonText: {Close: "close"} });        

</script>
{% endhighlight %}







### buttonText.upload `string`
{:#members:buttontext-upload}








Sets the text for the Upload button inside the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { upload: "Upload the File" }});
</script>

{% endhighlight %}







### cssClass `string`
{:#members:cssclass}








Sets the root class for the Uploadbox control theme. This cssClass API helps to use custom skinning option for the Uploadbox button and dialog content.





#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the cssClass API value on initialization.
$("#uploadbox1").ejUploadbox({cssClass : "gradient- purple"});        

</script>

{% endhighlight %}







### customFileDetails `object`
{:#members:customfiledetails}








Specifies the custom file details in the dialog popup on initialization.




#### Default Value







* { title:true, name:true, size:true, status:true, action:true}








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the customFileDetails API value on initialization.
$("#uploadbox1").ejUploadbox({customFileDetails:{ title:true, name:true, size:true, status:true, action:true}});        

</script>

{% endhighlight %}







### customFileDetails.action `boolean`
{:#members:customfiledetails-action}








Enables the file upload interactions like remove/cancel in File details of the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the customFileDetails.action API value on initialization.
$("#uploadbox1").ejUploadbox({customFileDetails:{action:true}});        

</script>

{% endhighlight %}







### customFileDetails.name `boolean`
{:#members:customfiledetails-name}








Enables the name in the File details of the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { name: true }});
</script>
{% endhighlight %}







### customFileDetails.size `boolean`
{:#members:customfiledetails-size}








Enables or disables the File size details of the dialog popup.

N>  Details of the File Size is available from IE10+ browser version.






#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { size:true}});
</script>{% endhighlight %}







### customFileDetails.status `boolean`
{:#members:customfiledetails-status}








Enables or disables the file uploading status visibility in the dialog file details content.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { status: true}});
</script>

{% endhighlight %}







### customFileDetails.title `boolean`
{:#members:customfiledetails-title}








Enables the title in File details for the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { title: true }});
</script>

{% endhighlight %}







### dialogAction `object`
{:#members:dialogaction}








Specifies the actions for dialog popup while initialization.




#### Default Value







* { modal:false, closeOnComplete:false, content:null, drag:true}








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the  dialogAction API value 
        $("#uploadbox1").ejUploadbox({ dialogAction:{ modal:false, closeOnComplete:false,resize: false, drag:true, content:"#controlid"}});     
</script>

{% endhighlight %}







### dialogAction.closeOnComplete `boolean`
{:#members:dialogaction-closeoncomplete}








Once uploaded successfully, the dialog popup closes immediately.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { closeOnComplete: true }});
</script>

{% endhighlight %}







### dialogAction.content `string`
{:#members:dialogaction-content}








Sets the content container option to the Uploadbox dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>
    //Sets the dialogAction.content API value on initialization.
$("#uploadbox1").ejUploadbox({dialogAction:{ content: "#uploadbox1"}});        

</script>

{% endhighlight %}







### dialogAction.drag `boolean`
{:#members:dialogaction-drag}








Enables the drag option to the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { drag: true }});
</script>

{% endhighlight %}







### dialogAction.modal `boolean`
{:#members:dialogaction-modal}








Enables or disables the Uploadbox dialog’s modal property to the dialog popup.


N> dialogAction.modal property does not work in synchronous file upload.






#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { modal: true }});
</script>

{% endhighlight %}







### dialogPosition `object`
{:#members:dialogposition}








Displays the Uploadbox dialog at the given X and Y positions. X: Dialog sets the left position value. Y: Dialog sets the top position value.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dialogPosition API value during initialization
        $("#uploadbox1").ejUploadbox({dialogPosition: { X: 300, Y: 10 }});
</script>

{% endhighlight %}







### dialogText `object`
{:#members:dialogtext}








Property for applying the text to the Dialog title and content headers.




#### Default Value







* { title: "Upload Box", name: "Name", size: "Size", status: "Status"}








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the  dialogText API value during initialization
        $("#uploadbox1").ejUploadbox({ dialogText:{title:"Upload File List",name:"File Name",size:"File Size",status:"File Status" }});
</script>

{% endhighlight %}







### dialogText.name `string`
{:#members:dialogtext-name}








Sets the uploaded file’s Name (header text) to the Dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { name: "Name" }});
</script>

{% endhighlight %}







### dialogText.size `string`
{:#members:dialogtext-size}








Sets the upload file Size (header text) to the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { size: "Size" }});
</script>

{% endhighlight %}







### dialogText.status `string`
{:#members:dialogtext-status}








Sets the upload file Status (header text) to the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { status: "Status" }});
</script>

{% endhighlight %}







### dialogText.title `string`
{:#members:dialogtext-title}








Sets the title text of the dialog popup.





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { title: "Upload Box" }});
</script>

{% endhighlight %}







### dropAreaText `string`
{:#members:dragareatext}








The dropAreaText is displayed when the drag and drop support is enabled in the Uploadbox control.




#### Default Value







* "Drop files or click to upload"








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dragAreaText API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaText:"Drop files or click to upload"});
</script> 

{% endhighlight %}







### dropAreaHeight `number`  `string`
{:#members:dropareaheight}








Specifies the dropAreaHeight when the drag and drop support is enabled in the Uploadbox control.




#### Default Value







* "100%"








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaHeight:"100%"}); 
</script>{% endhighlight %}







### dropAreaWidth `number|string`
{:#members:dropareawidth}








Specifies the dropAreaWidth when the drag and drop support is enabled in the Uploadbox control.




#### Default Value







* "100%"








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaWidth:"100%");   
</script> {% endhighlight %}







### enabled `boolean`
{:#members:enabled}







Based on the property value, Uploadbox is enabled or disabled.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the enabled API value during initialization
        $("#uploadbox1").ejUploadbox({ enabled: false });       
</script>{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Sets the right-to-left direction property for the Uploadbox control.




#### Default Value







* false








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the enableRTL API value during initialization
        $("#uploadbox1").ejUploadbox({ enableRTL: true});       
</script> {% endhighlight %}







### extensionsAllow `string`
{:#members:extensionsallow}








Only the files with the specified extension is allowed to upload. This is mentioned in the string format.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsAllow: ".zip"  });     
</script> {% endhighlight %}







### extensionsDeny `string`
{:#members:extensionsdeny}








Only the files with the specified extension is denied for upload. This is mentioned in the string format.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsDeny API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsDeny: ".zip"  });      
</script> {% endhighlight %}







### fileSize `number`
{:#members:filesize}








Sets the maximum size limit for uploading the file. This is mentioned in the number format.

N> fileSize represents the size of the individual file.





#### Default Value







* 31457280








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ fileSize: 31457280  });  
</script> {% endhighlight %}







### height `string`
{:#members:height}








Sets the height of the browse button.




#### Default Value







* 35px








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the height API value during initialization
        $("#uploadbox1").ejUploadbox({ height:"40px"});
</script>{% endhighlight %}



### htmlAttributes `object`

{:#members:htmlattributes}
 
Specifies the list of HTML attributes to be added to uploadbox control.
 
#### Default Value
 
* {}
 
#### Example 

{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//To set htmlAttributes API value during initialization
        $("#uploadbox1").ejUploadbox({ htmlAttributes:{"aria-label":"uploadbox"} });
</script>{% endhighlight %}



### locale `string`
{:#members:locale}








Configures the culture data and sets the culture to the Uploadbox.




#### Default Value







* "en-US"








#### Example



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







### multipleFilesSelection `boolean`
{:#members:multiplefilesselection}








Enables multiple file selection for upload.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the multipleFilesSelection API value during initialization
        $("#uploadbox1").ejUploadbox({ multipleFilesSelection: true });
</script> {% endhighlight %}







### pushFile `object`
{:#members:pushfile}








You can push the file to the Uploadbox in the client-side of the XHR supported browsers alone.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Pushes the new files via API value during initialization
        $("#uploadbox1").ejUploadbox({ pushFile: files });      
</script>{% endhighlight %}







### removeUrl `string`
{:#members:removeurl}








Specifies the remove action to be performed after the file uploading is completed. Here, mention the server address for removal.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the removeUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ removeUrl: "http://js.syncfusion.com/demos/beta/removeFiles.ashx"});     
</script>{% endhighlight %}







### saveUrl `string`
{:#members:saveurl}








Specifies the save action to be performed after the file is pushed for uploading. Here, mention the server address to be saved. 




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the saveUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx"}); 
</script>{% endhighlight %}







### showBrowseButton `boolean`
{:#members:showbrowsebutton}








Enables the browse button support to the Uploadbox control.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the showBrowseButton API value during initialization
        $("#uploadbox1").ejUploadbox({ showBrowseButton:true}); 
</script> {% endhighlight %}







### showFileDetails `boolean`
{:#members:showfiledetails}








Specifies the file details to be displayed when selected for uploading. This can be done when the showFileDetails is set to true.



#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the showFileDetails API value during initialization
        $("#uploadbox1").ejUploadbox({ showFileDetails: false });       
</script>{% endhighlight %}


### showRoundedCorner `boolean`
{:#members:showroundedcorner} 

Specifies the file details to be displayed when selected for uploading. This can be done when the showFileDetails is set to true.
 
#### Default Value 
 
* true
 
#### Example
 
{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the showRoundedCorner API value during initialization
        $("#uploadbox1").ejUploadbox({ showRoundedCorner: false });       
</script>{% endhighlight %}
 


### uploadName `string`
{:#members:uploadname}








Sets the name for the Uploadbox control. This API helps to Map the action in code behind to retrieve the files.





#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 

<script>

    //Sets the uploadName API value on initialization.
  $("#uploadbox1").ejUploadbox({saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx" ,uploadName: "Uploadbox", });      

</script>{% endhighlight %}







### width `string`
{:#members:width}








Sets the width of the browse button.




#### Default Value







* 100px








#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Sets the width API value during initialization
        $("#uploadbox1").ejUploadbox({ width:"120px"});
</script>{% endhighlight %}





## Methods








### destroy()
{:#methods:destroy}








The destroy method destroys the control and brings the control to a pre-init state. All the events of the Upload control is bound by using this._on unbinds automatically.  





#### Example



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







### disable()
{:#methods:disable}








Disables the Uploadbox control





#### Example



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







### enable()
{:#methods:enable}








Enables the Uploadbox control





#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Enables the Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.enable(); // enable the Uploadbox
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Enables the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("enable"); 
</script>

{% endhighlight %}

### refresh()
{:#methods:refresh}

Refresh the Uploadbox control
 
#### Example
 
{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Refresh the Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.refresh(); // refresh the Uploadbox
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
// Refresh the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("refresh"); 
</script>

{% endhighlight %}





## Events







### beforeSend
{:#events:beforesend}
 
Fires when the upload progress beforeSend.
 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody> 
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Selected FileList Object.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">xhr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">XHR-AJAX Object for reference.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//beforeSend event for Uploadbox
$("#uploadbox1").ejUploadbox({
   beforeSend: function (args) {}
});   
</script>{% endhighlight %}


### begin
{:#events:begin}








Fires when the upload progress begins.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">To pass additional information to the server.</td>
</tr>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Selected FileList Object.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>


#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">fileStatus</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Canceled FileList Object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>


#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">e</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">AJAX event argument for reference.</td>
</tr>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Uploaded file list.</td>
</tr>
<tr>
<td class="name">responseText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">response from the server.</td>
</tr>
<tr>
<td class="name">xhr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">XHR-AJAX Object for reference.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//Complete event for Uploadbox
$("#uploadbox1").ejUploadbox({
   complete: function (args) {}
});   
</script>   {% endhighlight %}






### success
{:#events:success}








Fires when the file upload progress is successed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">responseText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">response from the server.</td>
</tr>
<tr>
<td class="name">e</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">AJAX event argument for reference.</td>
</tr>
<tr>
<td class="name">success</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">successfully uploaded files list.</td>
</tr>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Uploaded file list.</td>
</tr>
<tr>
<td class="name">xhr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">XHR-AJAX Object for reference.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>


#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>



#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">details about the error information.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">error event action details.</td>
</tr>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the file details of the file uploaded</td>
</tr>
</tbody>
</table>




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns Selected FileList objects</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
<div id="uploadbox1"></div> 
 
<script> 
//fileSelect event for Uploadbox
$("#uploadbox1").ejUploadbox({
   fileSelect: function (args) {}
});  
</script>    {% endhighlight %}


### inProgress
{:#events:inprogress}
  
Fires when the file is uploading.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">e</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">AJAX event argument for reference.</td>
</tr>
<tr>
<td class="name">files</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns Selected FileList objects</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">percentage</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current progress percentage.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
 
#### Example

{% highlight html %}
<div id="uploadbox1"></div> 
 
<script> 
//inProgress event for Uploadbox
$("#uploadbox1").ejUploadbox({
   inProgress: function (args) {}
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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">fileStatus</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the file details of the file object</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="uploadbox1"></div> 
 
<script>
//remove event for Uploadbox
$("#uploadbox1").ejUploadbox({
   remove: function (args) {}
});  
</script>    {% endhighlight %} 
 

