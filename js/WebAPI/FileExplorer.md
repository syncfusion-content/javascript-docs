---
layout: post
title: webAPI reference for ejFileExplorer
description: webAPI reference for ejFileExplorer
documentation: ug
platform: js
keywords: fileexplorer, ejfileexplorer, syncfusion, fileexplorer webapi
---

## FileOperations

 [POST] [/Api/FileExplorer/FileOperations](http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations)

It helps to handle the FileExplorer operations like Read, Upload, Download, GetDetails, Rename, Remove etc.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|Action	|String|Specifies the paste operation format which should be “Copy” or ”Move”.These details will be send through AJAX request parameter while performing the paste operation.|
|ActionType|String|Specifies the file operation that need to be performed on this request.For example: Read, Upload, Download, GetDetails, Rename, Remove operations.|
|CaseSensitive|Boolean |Specifies the case sensitive option for filtering the files.Also these details will be send to the parameter through AJAX request while performing search operation.|
|CommonFiles|IEnumerable<object >|It contains the details about already existing files in destination folder, which contains the files in same name and type as same as new files.|
|ExtensionsAllow|String|Specifies the file types that need to be filter at search operation. Also these details will be send to the parameter through AJAX request while performing search and read operations.|
|FileUpload|IEnumerable<Object>|Specifies the file details which is going to upload.Also these details will be send to the parameter through AJAX request while performing upload operation.|
|LocationFrom|String|Specifies the path of source directory.And the details will be send to the parameter through AJAX request while performing paste operation.|
|LocationTo|String|Specifies the path of target directory.These details will be send to the parameter through AJAX request while performing paste operation.|
|Name|String|Specifies the selected item name.|
|Names|String[]|Specifies the selected item names.|
|NewName|String|Specifies the new file name for renaming the file.These details will be send to the parameter through AJAX request while performing rename operation.|
|Path|String|Specifies the path of selected folder.|
|SearchString|String|Specifies the search string for filtering the matched files.These details will be send to the parameter through AJAX request while performing search operation.|
|SelectedItems| IEnumerable<object>|It contains the details of selected folder.|


### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

{% highlight js %}
{
    "cwd":{
        "name":"FileBrowser",
        "type":"Directory",
        "size":0,
        "dateModified":"11/2/2016 6:11:14 AM",
        "hasChild":true,
        "isFile":false,
        "filterPath":null,
        "permission":null
    },
    "files":[
        {
            "name":"DEZ",
            "type":"Directory",
            "size":0,
            "dateModified":"11/2/2016 5:53:05 AM",
            "hasChild":true,
            "isFile":false,
            "filterPath":null,
            "permission":null
        },
        {
            "name":"Employees",
            "type":"Directory",
            "size":0,
            "dateModified":"11/2/2016 6:31:57 AM",
            "hasChild":true,
            "isFile":false,
            "filterPath":null,
            "permission":null
        }
    ],
    "details":null,
    "error":null
}

{% endhighlight %}


### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations   

$.ajax({
    data: JSON.stringify({
        "Name": "",
        "ActionType": "Read",
        "Path": "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/Food/",
        "ExtensionsAllow": "*.png, *.gif, *.jpg, *.jpeg, *.docx",
        "LocationFrom": "",
        "LocationTo": "",
        "Action": "",
        "NewName": "",
        "Names": [],
        "CaseSensitive": false,
        "SearchString": "",
        "FileUpload": null,
        "CommonFiles": null,
        "SelectedItems": []
    }),
    type: "POST",
    url: "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations",
    async: false,
    contentType: "application/json",
    dataType: "json"
})

{% endhighlight %}

## FileOperationsCors

 [GET] /Api/FileExplorer/FileOperationsCors
 
 URL: //js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperationsCors

It helps to handle the FileExplorer operations in cross origin.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|Callback|String|Name of callback function.|
|json|String|File operation related parameters will be send along with that and these parameter details are same like the above request parameters.|

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

{% highlight js %}

{
    "cwd":{
        "name":"FileBrowser",
        "type":"Directory",
        "size":0,
        "dateModified":"11/2/2016 6:11:14 AM",
        "hasChild":true,
        "isFile":false,
        "filterPath":null,
        "permission":null
    },
    "files":[
        {
            "name":"DEZ",
            "type":"Directory",
            "size":0,
            "dateModified":"11/2/2016 5:53:05 AM",
            "hasChild":true,
            "isFile":false,
            "filterPath":null,
            "permission":null
        },
        {
            "name":"Employees",
            "type":"Directory",
            "size":0,
            "dateModified":"11/2/2016 6:31:57 AM",
            "hasChild":true,
            "isFile":false,
            "filterPath":null,
            "permission":null
        }
    ],
    "details":null,
    "error":null
}

{% endhighlight %}

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperationsCors    

$.ajax({
    data: {
        json: JSON.stringify({
            "Name": "",
            "ActionType": "Read",
            "Path": "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/Food/",
            "ExtensionsAllow": "*.png, *.gif, *.jpg, *.jpeg, *.docx",
            "LocationFrom": "",
            "LocationTo": "",
            "Action": "",
            "NewName": "",
            "Names": [],
            "CaseSensitive": false,
            "SearchString": "",
            "FileUpload": null,
            "CommonFiles": null,
            "SelectedItems": []
        })
    },
    type: "GET",
    url: "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperationsCors",    
    async: false,
    contentType: "application/json",
    dataType: "jsonp",
    jsonpCallback: "MyCallbackFunction"
})

{% endhighlight %}