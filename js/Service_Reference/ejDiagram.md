---
layout: post
title: Service reference for ejDiagram widget
description: Services used in Essential JavaScript Diagram.
documentation: api
platform: js
keywords: ejDiagram, Services, Essential JS Diagram, Diagram, CRUD Service
metaname: 
metacontent:
control: ejDiagram
---

#Diagram CRUD services

## Read Nodes DataSource

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetShapeData](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetShapeData)

### Parameter
Empty

### Request

{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetShapeData',
});

{% endhighlight %}

### Response 

####Code:  200

####Content-Type: application/json;

####Response (JSON):

{% highlight js %}
    [{
        "Id": 4,
        "Name": "orgchart",
        "Description": "Organizational Chart",
        "Color": "#88C600"
    }, {
        "Id": 18,
        "Name": "layout",
        "Description": "Layout",
        "Color": "#916DAF"
    }]
{% endhighlight %}

## New Shapes

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertShape)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the newly added shapes as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertShape',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes75E",
        "Description": "Diagram",
        "Color": "red"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

## Updated Shapes

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateShape)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the updated shapes as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateShape',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes76E",
        "Description": "Diagram",
        "Color": "red"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

## Deleted Shapes

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteShape)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the deleted shapes as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteShape',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes76E",
        "Description": "Diagram",
        "Color": "red"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

## Read Connectors DataSource

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetConnectorData](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetConnectorData)

### Parameter
Empty

### Request

{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/GetConnectorData',
});

{% endhighlight %}

### Response 

####Code:  200

####Content-Type: application/json;

####Response (JSON):

{% highlight js %}
[{
    "Id": 22,
    "Name": "nodeHsI1",
    "SourceNode": "orgchart",
    "TargetNode": "layout"
}]
{% endhighlight %}

## New Connectors

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertConnector)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the newly added connectors as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertConnector',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

## Updated Connectors

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateConnector)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the updated connectors as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateConnector',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

## Deleted Connectors

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteConnector)

### Parameter

<table>
<tr>
<td>
**Name**</td><td>
**Type**</td><td>
**Description**</td></tr>
<tr>
<td>
data</td><td>
Array</td><td>
Send the deleted connectors as a collection of array.</td></tr>
</table>

### Request

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteConnector',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

### Response 

####Code:  204

####Content-Type: null;

####Response Text: Empty

