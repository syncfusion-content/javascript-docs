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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/GetNodes](http://js.syncfusion.com/demos/ejservices/api/Diagram/GetNodes)

### Parameter
Empty

### Request

{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/GetNodes',
});

{% endhighlight %}

#### Action getting invoked in C Sharp 

{% highlight c# %}

public List<HierarchicalData> GetNodes()
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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/AddNodes](http://js.syncfusion.com/demos/ejservices/api/Diagram/AddNodes)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/AddNodes',

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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateNodes](http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateNodes)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateNodes',

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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteNodes](http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteNodes)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteNodes',

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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/GetConnectors](http://js.syncfusion.com/demos/ejservices/api/Diagram/GetConnectors)

### Parameter
Empty

### Request

{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/GetConnectors',
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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/AddConnectors](http://js.syncfusion.com/demos/ejservices/api/Diagram/AddConnectors)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/AddConnectors',

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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateConnectors](http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateConnectors)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/UpdateConnectors',

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
[http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteConnectors](http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteConnectors)

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

    url: 'http://js.syncfusion.com/demos/ejservices/api/Diagram/DeleteConnectors',

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