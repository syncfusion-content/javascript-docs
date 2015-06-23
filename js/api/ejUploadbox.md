---
layout: post
title: ejUploadbox
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html Uploadbox control.










#### $(element).ejUploadbox<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Uploadbox
$('#uploadbox1').ejUploadbox();         
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.uploadbox.js


* module:ej.dialog.js


* module:ej.scroller.js


* module:ej.draggable.js




### Members








#### allowDragAndDrop<span class="type-signature type boolean">boolean</span>








Enable the dragAndDrop support to the Uploadbox control.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set allowDragAndDrop API value during initialization
        $("#uploadbox1").ejUploadbox({ allowDragAndDrop:false});        
&lt;/script&gt; </code>
</pre>






#### asyncUpload<span class="type-signature type boolean">boolean</span>








Uploadbox supports both synchronous and asynchronous upload. This can be achieved by this property asyncUpload.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ asyncUpload: false });   
&lt;/script&gt;</code>
</pre>






#### autoUpload<span class="type-signature type boolean">boolean</span>








Uploadbox supports auto uploading of files after the file selection is done.The auto upload is performed if autoUpload is set to true.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set autoUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ autoUpload: true });     
&lt;/script&gt;</code>
</pre>






#### buttonText<span class="type-signature type string">string</span>








Specifies the text content for Uploadbox browse button while initialization.




Default Value:
{:.param}






* "Browse"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  browseButtonText API value 
        $("#uploadbox1").ejUploadbox({ buttonText:{ browse:"Choose File", upload:"Upload the File", cancel:"Cancel the Upload"}});      
&lt;/script&gt;</code>
</pre>






#### buttonText.browse<span class="type-signature type string">String</span>








Sets the text for the Browse button.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { browse: "Choose File" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.cancel<span class="type-signature type string">String</span>








Sets the text for the Cancel button inside the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { cancel: "Cancel the Upload" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.Close<span class="type-signature type string">String</span>








Sets the text for the Close button inside the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { close: "close dialog" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.upload<span class="type-signature type string">String</span>








Sets the text for the Upload button inside the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ buttonText: { upload: "Upload the File" }});
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Set the root class for Uploadbox control theme. This cssClass API helps to use custom skinning option for Uploadbox control.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set cssClass  API value during initialization
        $("#uploadbox1").ejUploadbox({ cssClass : "gradient-lime"});    
&lt;/script&gt; </code>
</pre>






#### customFileDetails<span class="type-signature type object">object</span>








Specifies the custom file details in dialog popup while initialization.




Default Value:
{:.param}






* customFileDetails:{ title:true, name:true, size:true, status:true, action:true}








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  customFileDetails API value 
        $("#uploadbox1").ejUploadbox({ customFileDetails:{ title:true, name:true, size:true, status:true, action:true}});       
&lt;/script&gt;</code>
</pre>






#### customFileDetails.action<span class="type-signature type boolean">boolean</span>








Enable the remove/ cancel action in File details for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { action: true}});
&lt;/script&gt;</code>
</pre>






#### customFileDetails.name<span class="type-signature type boolean">boolean</span>








Enable the name in File details for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { name: true }});
&lt;/script&gt;</code>
</pre>






#### customFileDetails.size<span class="type-signature type boolean">boolean</span>








Enable the size in File details for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { size:true}});
&lt;/script&gt;</code>
</pre>






#### customFileDetails.status<span class="type-signature type boolean">boolean</span>








Enable the status in File details for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { status: true}});
&lt;/script&gt;</code>
</pre>






#### customFileDetails.title<span class="type-signature type boolean">boolean</span>








Enable the title in File details for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set customFileDetails API during initialization  
        $("#uploadbox1").ejUploadbox({ customFileDetails: { title: true }});
&lt;/script&gt;</code>
</pre>






#### dialogAction<span class="type-signature type object">object</span>








Specifies the actions for dialog popup while initialization.




Default Value:
{:.param}






* dialogAction:{ modal:false, closeOnComplete:false, content:null, drag:true}








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  dialogAction API value 
        $("#uploadbox1").ejUploadbox({ dialogAction:{ modal:false, closeOnComplete:false,resize: false, drag:true, content:"#controlid"}});     
&lt;/script&gt;</code>
</pre>






#### dialogAction.closeOnComplete<span class="type-signature type boolean">boolean</span>








This will close the File details for the dialog popup once upload has performed successfully.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { closeOnComplete: true }});
&lt;/script&gt;</code>
</pre>






#### dialogAction.content<span class="type-signature type string">string</span>








set the content Container option for File details of dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { content: "#uploadbox1" }});
&lt;/script&gt;</code>
</pre>






#### dialogAction.drag<span class="type-signature type boolean">boolean</span>








Enable the drag option for File details of dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { drag: true }});
&lt;/script&gt;</code>
</pre>






#### dialogAction.modal<span class="type-signature type boolean">boolean</span>








set the modal property for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dialogAction API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogAction: { modal: true }});
&lt;/script&gt;</code>
</pre>






#### dialogPosition<span class="type-signature type jsonobject">JSONobject</span>








Displays the uploadbox dialog window at the given X and Y position. X: Dialog set the left position value. Y: Dialog set the top position value.




Default Value:
{:.param}






* Null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dialogPosition API value during initialization
        $("#uploadbox1").ejUploadbox({dialogPosition: { X: 300, Y: 10 }});
&lt;/script&gt;</code>
</pre>






#### dialogText<span class="type-signature type string">string</span>








Sets the text for the inside the dialog popup.




Default Value:
{:.param}






* UploadBox








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  dialogText API value during initialization
        $("#uploadbox1").ejUploadbox({ dialogText:{title:"Upload File List",name:"File Name",size:"File Size",status:"File Status" }});
&lt;/script&gt;</code>
</pre>






#### dialogText.name<span class="type-signature type string">String</span>








Sets the Name text for the dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { name: "Name" }});
&lt;/script&gt;</code>
</pre>






#### dialogText.size<span class="type-signature type string">String</span>








Sets the Size text for dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { size: "Size" }});
&lt;/script&gt;</code>
</pre>






#### dialogText.status<span class="type-signature type string">String</span>








Sets the Status text for dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { status: "Status" }});
&lt;/script&gt;</code>
</pre>






#### dialogText.title<span class="type-signature type string">String</span>








Sets the title text dialog popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization  
        $("#uploadbox1").ejUploadbox({ dialogText: { title: "Upload Box" }});
&lt;/script&gt;</code>
</pre>






#### dragAreaText<span class="type-signature type string">string</span>








To specify the text to be displayed when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "Drop files or click to upload"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dragAreaText API value during initialization
        $("#uploadbox1").ejUploadbox({ dragAreaText:"Drop files or click to upload"});  
&lt;/script&gt; </code>
</pre>






#### dropAreaHeight<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>








To specify the dropareaheight when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "100%"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaHeight:"100%"}); 
&lt;/script&gt; </code>
</pre>






#### dropAreaWidth<span class="type-signature type number">number</span> <span class="type-signature type string">string</span>








To specify the dropareawidth when enable the draganddrop support in theUploadbox control.




Default Value:
{:.param}






* "100%"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set dropAreaHeight API value during initialization
        $("#uploadbox1").ejUploadbox({ dropAreaWidth:"100%");   
&lt;/script&gt; </code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








Enables or disables Uploadbox based on boolean value.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set enabled API value during initialization
        $("#uploadbox1").ejUploadbox({ enabled: false });       
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Specifies the Right to Left direction property for Uploadbox control.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set enableRTL API value during initialization
        $("#uploadbox1").ejUploadbox({ enableRTL: true});       
&lt;/script&gt; </code>
</pre>






#### extensionsAllow<span class="type-signature type string">string</span>








Specifies the file extension to allow for uploading the file while initialization. This could be mentioned in string format.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsAllow: ".zip"  });     
&lt;/script&gt; </code>
</pre>






#### extensionsDeny<span class="type-signature type string">string</span>








Specifies the file extension to deny for uploading the file while initialization. This could be mentioned in string format.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set extensionsDeny API value during initialization
        $("#uploadbox1").ejUploadbox({ extensionsDeny: ".zip"  });      
&lt;/script&gt; </code>
</pre>






#### fileSize<span class="type-signature type number">number</span>








Specifies the file size for uploading the file while initialization. This could be mentioned in number format.




Default Value:
{:.param}






* 31457280








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set extensionsAllow API value during initialization
        $("#uploadbox1").ejUploadbox({ fileSize: 31457280  });  
&lt;/script&gt; </code>
</pre>






#### height<span class="type-signature type string">string</span>








Sets the browse button height.




Default Value:
{:.param}






* 35px








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set height API value during initialization
        $("#uploadbox1").ejUploadbox({ height:"40px"});
&lt;/script&gt;</code>
</pre>






#### locale<span class="type-signature type string">string</span>








Sets the culture in uploadbox.




Default Value:
{:.param}






* "en-US"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set  asyncUpload API value during initialization
        $("#uploadbox1").ejUploadbox({ locale: vi-VN });        
&lt;/script&gt;</code>
</pre>






#### multipleFilesSelection<span class="type-signature type boolean">boolean</span>








Enables to select multiple files




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set multipleFilesSelection API value during initialization
        $("#uploadbox1").ejUploadbox({ multipleFilesSelection: false });
&lt;/script&gt; </code>
</pre>






#### pushFile<span class="type-signature type data">data</span>








We can push the file into upload box in client side in xhr supported browsers alone.




Default Value:
{:.param}






* files- rawfiles








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To push new files via API value during initialization
        $("#uploadbox1").ejUploadbox({ pushFile: files });      
&lt;/script&gt;</code>
</pre>






#### removeUrl<span class="type-signature type string">string</span>








Specifies the remove action which has to be performed after the file uploading is completed. Here we have to mention the server address which has to perform this action.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set removeUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ removeUrl: "http://js.syncfusion.com/demos/beta/removeFiles.ashx"});     
&lt;/script&gt;</code>
</pre>






#### saveUrl<span class="type-signature type string">string</span>








Specifies the save action which has to be performed after the file is pushed for uploading. Here we have to mention the server address which has to perform this action.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set saveUrl API value during initialization
        $("#uploadbox1").ejUploadbox({ saveUrl: "http://js.syncfusion.com/demos/beta/saveFiles.ashx"}); 
&lt;/script&gt;</code>
</pre>






#### showBrowseButton<span class="type-signature type boolean">boolean</span>








Enable the browse button support to the Uploadbox control.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set showBrowseButton API value during initialization
        $("#uploadbox1").ejUploadbox({ showBrowseButton:true}); 
&lt;/script&gt; </code>
</pre>






#### showFileDetails<span class="type-signature type boolean">boolean</span>








Specifies to display the file details of files while selected for uploading can be done when showFileDetails set to true.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set showFileDetails API value during initialization
        $("#uploadbox1").ejUploadbox({ showFileDetails: false });       
&lt;/script&gt;</code>
</pre>






#### uploadName<span class="type-signature type string">string</span>








Set the Name for Uploadbox control . This API helps to Map the action in code behind to retrieve the files.




Default Value:
{:.param}






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set uploadName property value during initialization
        $("#uploadbox1").ejUploadbox({ uploadName : "Uploadbox"});      
&lt;/script&gt; </code>
</pre>






#### width<span class="type-signature type string">string</span>








Sets the browse button width.




Default Value:
{:.param}






* 100px








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set width API value during initialization
        $("#uploadbox1").ejUploadbox({ width:"120px"});
&lt;/script&gt;</code>
</pre>




### Methods








#### destroy<span class="signature">()</span>








destroy the Upload control all events bound using this._on will be unbind automatically and bring the control to pre-init state.





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Destroy Upload
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.destroy(); // destroy the Upload control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// destroy the Upload control
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("destroy");        
&lt;/script&gt;</code>
</pre>






#### disable<span class="signature">()</span>








To disable the Uploadbox control





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Disable Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.disable(); // disable the Uploadbox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// disable the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("disable");        
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








To enable the Uploadbox control





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// enable Uploadbox
$("#uploadbox1").ejUploadbox();
var uploadObj = $("#uploadbox1").data("ejUploadbox");
uploadObj.enable(); // enable the Uploadbox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// enable the Uploadbox
$("#uploadbox1").ejUploadbox();
$("#uploadbox1").ejUploadbox("enable"); 
&lt;/script&gt;</code>
</pre>




### Events








#### begin








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//begin event for Uploadbox
$("#uploadbox1").ejUploadbox({
   begin: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






#### cancel








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//cancel event for Uploadbox
$("#uploadbox1").ejUploadbox({
   cancel: function (args) {}
});
&lt;/script&gt;     </code>
</pre>






#### complete








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>files</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns file entries and its details</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//complete event for Uploadbox
$("#uploadbox1").ejUploadbox({
   complete: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






#### create








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//create event for Uploadbox
$("#uploadbox1").ejUploadbox({
   create: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






#### destroy








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//destroy event for Uploadbox
$("#uploadbox1").ejUploadbox({
   destroy: function (args) {}
});  
&lt;/script&gt;    </code>
</pre>






#### error








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the action name</td>
</tr>
<tr>
<td class="name"><code>files</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the file details of the file uploaded</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//error event for Uploadbox
$("#uploadbox1").ejUploadbox({
   error: function (args) {}
});  
&lt;/script&gt;    </code>
</pre>






#### fileSelect








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
//fileSelect event for Uploadbox
$("#uploadbox1").ejUploadbox({
   fileSelect: function (args) {}
});  
&lt;/script&gt;    </code>
</pre>






#### remove








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Uploadbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the file details of the file object</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="uploadbox1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//remove event for Uploadbox
$("#uploadbox1").ejUploadbox({
   remove: function (args) {}
});  
&lt;/script&gt;    </code>
</pre>



