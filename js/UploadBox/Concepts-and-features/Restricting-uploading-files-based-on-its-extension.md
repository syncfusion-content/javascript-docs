---
layout: post
title: Restricting-uploading-files-based-on-its-extension
description: restricting uploading files based on its extension
platform: js
control: Uploadbox
documentation: ug
---

# Restricting uploading files based on its extension

## Allow Extension

Files are filtered before they are uploaded. You can select the files to be filtered by using **browse** button. The **extensionsAllow** property allows upload of the selected extensions only. You can give multiple extensions by using comma (,).  The data type is **string**.

> _**Note: Prepend dot (.) symbol with extension like “.pdf”.**_



The following steps explain the configuration of **extensionsAllow** property in **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}


      <div id="Uploadbox"></div>

{% endhighlight %}

{% highlight js %}



  // Initialize the control in JavaScript.
  <script>
  $(function () {
//Declaration.
            $("#Uploadbox").ejUploadbox({
                saveUrl: "saveFiles.ashx",
                removeUrl: "removeFiles.ashx",
                extensionsAllow: ".docx, .pdf"
            }); 	
        });
</script>

{% endhighlight %}

* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

## Deny Extension

Files are filtered before they are uploaded. You can select the files to be filtered by using **browse** button. The **extensionsDeny** property denies upload of the selected extensions. You can give multiple extensions by using comma (,).  The data type is **string**.

> _**Note: Prepend dot (.) symbol with extension like “.pdf”.**_

The following steps explain the configuration of **extensionsDeny** property in **Uploadbox**

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}


      <div id="Uploadbox"></div>

{% endhighlight %}

{% highlight js %}


 // Initialize the control in JavaScript.
 <script>
  $(function () {
//Declaration.
            $("#Uploadbox").ejUploadbox({
                saveUrl: "saveFiles.ashx",
                removeUrl: "removeFiles.ashx",
                extensionsDeny: ".docx, .pdf"
            }); 
        });
</script>

{% endhighlight %}

* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

