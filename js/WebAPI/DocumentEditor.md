---
layout: post
title: webAPI reference for DocumentEditor
description: webAPI reference for DocumentEditor
documentation: webAPI
platform: js-webapi
keywords: documenteditor,syncfusion,documenteditor webapi
---

## Import

<a>POST&nbsp;&nbsp;/Api/DocumentEditor/Import</a>

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

```javascript
{
AbstractLists,
BackgroundColor,
Lists,
Sections
}
```

### Code example 


```javascript

URL: http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/Import

$.ajax({
        type: "POST",
        async: true,
        processData: false,
        contentType: false,
        crossDomain: true,
        data: formData,
        dataType: "JSON",
        url: “http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/Import”,
})

```


## LoadDefault

<a>POST&nbsp;&nbsp;/Api/DocumentEditor/LoadDefault</a>

it loads the default document in DocumentEditor.

### URL parameters

|  Parameter |Data Type|  Description | 
|---|---|---|
| filePath|String|Specifies the path of the input document to be loaded.|

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Encoding: gzip

Content-Type:  application/json; charset=utf-8

Response (JSON):   

```javascript
{
AbstractLists,
BackgroundColor,
Lists,
Sections
}
```

### Code example 

```javascript

URL: http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/LoadDefault 

$.ajax({
        type: "POST",
        async: true,
        processData: false,
        contentType: false,
        crossDomain: true,
        data: formData,
        dataType: "JSON",
        url: “http://js.syncfusion.com/demos/ejServices/api/DocumentEditor/LoadDefault”,
})

```