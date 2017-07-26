---
layout: post
title: webAPI reference for DocumentEditor
description: webAPI reference for 
documentation: ug
platform: js
keywords: documenteditor,syncfusion,documenteditor webapi
api: /api/js/ejdocumenteditor
---

## Import

 [POST] [/Api/DocumentEditor/Import](http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/Import)

It loads the document from specified path in DocumentEditor.

### URL parameters

|  Parameter | Data Type| Description | 
|---|---|---|
|filePath|String|Specifies the path of the input document to be loaded.| 

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Encoding: gzip

Content-Type:  application/json; charset=utf-8

Response (JSON):   

{% highlight js %}
{
AbstractLists,
BackgroundColor,
Lists,
Sections
}
{% endhighlight %}

### Code example 


{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/Import

$.ajax({
        type: "POST",
        async: true,
        processData: false,
        contentType: false,
        crossDomain: true,
        data: formData,
        dataType: "JSON",
        url: "http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/Import",
})

{% endhighlight %}


## LoadDefault

 [POST] [/Api/DocumentEditor/LoadDefault](http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/LoadDefault)

It loads the default document in DocumentEditor.

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Encoding: gzip

Content-Type:  application/json; charset=utf-8

Response (JSON):   

{% highlight js %}
{
AbstractLists,
BackgroundColor,
Lists,
Sections
}
{% endhighlight %}

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/LoadDefault 

$.ajax({
        type: "POST",
        async: true,
        processData: false,
        contentType: false,
        crossDomain: true,
        data: formData,
        dataType: "JSON",
        url: "http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/LoadDefault",
})

{% endhighlight %}