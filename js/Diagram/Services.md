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

# Diagram CRUD services

## Get Shape Data

### Description

Fetch the collection of records from database and further it will be used to generate the shapes.

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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public List<HierarchicalData> GetShapeData()
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    return context.HierarchicalDatas.ToList();
}

{% endhighlight %}

### Response 

#### Code:  200

#### Content-Type: application/json;

#### Response (JSON):

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

## Insert Shape

### Description

Send one or more shapes which needs to be inserted into database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertShape)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the shapes which needs to be inserted.</td></tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void InsertShape(List<HierarchicalData> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    context.HierarchicalDatas.InsertAllOnSubmit(data);
    foreach (HierarchicalData hdata in data)
    {
        context.HierarchicalDatas.InsertOnSubmit(hdata);
        context.SubmitChanges();
    }
}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty

## Update Shape

### Description

Send one or more shapes which needs to be modified into database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateShape)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the shapes which needs to be modified.</td>
</tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void UpdateShape(List<HierarchicalData> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalData hdata in data)
    {
        HierarchicalData originalData = context.HierarchicalDatas.Single(h => h.Name == hdata.Name);
        originalData.Description = hdata.Description;
        originalData.Color = hdata.Color;
        context.SubmitChanges();
    }

}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty

## Delete Shape

### Description

Send one or more shapes which needs to be deleted from database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteShape](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteShape)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the shapes which needs to be deleted.</td>
</tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void DeleteShape(List<HierarchicalData> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalData hdata in data)
    {
        HierarchicalData originalData = context.HierarchicalDatas.Single(h => h.Name == hdata.Name);
        context.HierarchicalDatas.DeleteOnSubmit(originalData);
        context.SubmitChanges();
    }
}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty

## Get Connector Data

### Description

Fetch the collection of records from database and further it will be used to generate the connectors.

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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public List<HierarchicalDetails> GetConnectorData()
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    return context.HierarchicalDetails.ToList();
}

{% endhighlight %}

### Response 

#### Code:  200

#### Content-Type: application/json;

#### Response (JSON):

{% highlight js %}
[{
    "Id": 22,
    "Name": "nodeHsI1",
    "SourceNode": "orgchart",
    "TargetNode": "layout"
}]
{% endhighlight %}

## Insert Connector

### Description

Send one or more connectors which needs to be inserted into database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/InsertConnector)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the connectors which needs to be inserted.</td>
</tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void InsertConnector(List<HierarchicalDetails> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalDetails hdata in data)
    {
        context.HierarchicalDetails.InsertOnSubmit(hdata);
        context.SubmitChanges();
    }
}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty

## Update Connector

### Description

Send one or more connectors which needs to be modified into database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/UpdateConnector)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the connectors which needs to be modified.</td>
</tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void UpdateConnector(List<HierarchicalDetails> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalDetails hdata in data)
    {
        HierarchicalDetails originalData = context.HierarchicalDetails.Single(h => h.Name == hdata.Name);
        originalData.SourceNode = hdata.SourceNode;
        originalData.TargetNode = hdata.TargetNode;
        context.SubmitChanges();
    }
}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty

## Delete Connector

### Description

Send one or more connectors which needs to be deleted from database.

### URL 
[http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteConnector](http://js.syncfusion.com/demos/ejservices/api/JSDiagram/DeleteConnector)

### Parameter

<table>
<tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
</tr>
<tr>
    <td>data</td>
    <td>Array</td>
    <td>Send the connectors which needs to be deleted.</td>
</tr>
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

#### Action getting invoked in C Sharp 

{% highlight c# %}

public void DeleteConnector(List<HierarchicalDetails> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalDetails hdata in data)
    {
        HierarchicalDetails originalData = context.HierarchicalDetails.Single(h => h.Name == hdata.Name);
        context.HierarchicalDetails.DeleteOnSubmit(originalData);
        context.SubmitChanges();
    }
}

{% endhighlight %}

### Response 

#### Code:  204

#### Content-Type: null;

#### Response Text: Empty