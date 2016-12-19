---
layout: post
title: webAPI reference for ejDiagram
description: webAPI reference for ejDiagram
documentation: ug
platform: js
keywords: ejDiagram, Diagram, syncfusion, ejDiagram webapi
---

## GetNodes

[GET] [/Api/Diagram/GetNodes](http://js.syncfusion.com/demos/ejServices/api/Diagram/GetNodes)

It fetches the collection of records from database and further it will be used to generate the shapes.

### Response information 

Code: 200

Content-Type: application/json;

Response (JSON):   

{% highlight js %}
[{
    "Id": 4,
    "Name": "orgchart",
    "Description": "Organizational Chart",
    "Color": "#88C600"
 }, 
 {
    "Id": 18,
    "Name": "layout",
    "Description": "Layout",
    "Color": "#916DAF"
}]

{% endhighlight %}


### Code example 


{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/GetNodes',
});

{% endhighlight %}


{% highlight c# %}

public List<HierarchicalData> GetNodes()
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    return context.HierarchicalDatas.ToList();
}

{% endhighlight %}

## GetConnectors

[GET] [/Api/Diagram/GetNodes](http://js.syncfusion.com/demos/ejServices/api/Diagram/GetConnectors)

It fetches the collection of records from database and further it will be used to generate the connectors.

### Response information 

Code: 200

Content-Type: application/json;

Response (JSON):   

{% highlight js %}
[{
    "Id": 22,
    "Name": "nodeHsI1",
    "SourceNode": "orgchart",
    "TargetNode": "layout"
}]

{% endhighlight %}

### Code example 


{% highlight js %}

$.ajax({

    type: 'GET',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/GetConnectors',
});

{% endhighlight %}


{% highlight c# %}

public List<HierarchicalDetails> GetConnectors()
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    return context.HierarchicalDetails.ToList();
}

{% endhighlight %}

## AddNodes

[POST] [/Api/Diagram/AddNodes](http://js.syncfusion.com/demos/ejServices/api/Diagram/AddNodes)

It is used to send one or more shapes which needs to be inserted into database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|Send the shapes which needs to be inserted.|

### Response information 

Code: 200

Content-Type: application/json;

Response (JSON):   

{% highlight js %}
[{
    "Id": 22,
    "Name": "nodeHsI1",
    "SourceNode": "orgchart",
    "TargetNode": "layout"
}]

{% endhighlight %}

### Code example 


{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/AddNodes',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes75E",
        "Description": "Diagram",
        "Color": "red"
    }])
});
{% endhighlight %}


{% highlight c# %}

public void AddNodes(List<HierarchicalData> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalData hdata in data)
    {
        context.HierarchicalDatas.InsertOnSubmit(hdata);
        context.SubmitChanges();
    }
}

{% endhighlight %}

## UpdateNodes

[POST] [/Api/Diagram/UpdateNodes](http://js.syncfusion.com/demos/ejServices/api/Diagram/UpdateNodes)

It is used to one or more shapes which needs to be modified into database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|Send the shapes which needs to be modified.|

### Response information 

Code: 204

### Code example 

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/UpdateNodes',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes76E",
        "Description": "Diagram",
        "Color": "red"
    }])
});

{% endhighlight %}

{% highlight c# %}

public void UpdateNodes(List<HierarchicalData> data)
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

## DeleteNodes

[POST] [/Api/Diagram/DeleteNodes](http://js.syncfusion.com/demos/ejServices/api/Diagram/DeleteNodes)

It is used to one or more shapes which needs to be deleted from database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|Send the shapes which needs to be deleted.|

### Response information 

Code: 204

### Code example 

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/DeleteNodes',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "nodes76E",
        "Description": "Diagram",
        "Color": "red"
    }])
});

{% endhighlight %}

{% highlight c# %}

public void DeleteNodes(List<HierarchicalData> data)
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

## AddConnectors

[POST] [/Api/Diagram/AddConnectors](http://js.syncfusion.com/demos/ejServices/api/Diagram/AddConnectors)

It is used to one or more connectors which needs to be inserted into database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|Send the connectors which needs to be inserted.|

### Response information 

Code: 204

### Code example 

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/AddConnectors',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

{% highlight c# %}

public void AddConnectors(List<HierarchicalDetails> data)
{
    DiagramContextDataContext context = new DiagramContextDataContext();
    foreach (HierarchicalDetails hdata in data)
    {
        context.HierarchicalDetails.InsertOnSubmit(hdata);
        context.SubmitChanges();
    }
}

{% endhighlight %}


## UpdateConnectors

[POST] [/Api/Diagram/UpdateConnectors](http://js.syncfusion.com/demos/ejServices/api/Diagram/UpdateConnectors)

It is used to one or more connectors which needs to be modified into database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|Send the connectors which needs to be modified.|

### Response information 

Code: 204

### Code example 

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/UpdateConnectors',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

{% highlight c# %}

public void UpdateConnectors(List<HierarchicalDetails> data)
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

## DeleteConnectors

[POST] [/Api/Diagram/UpdateConnectors](http://js.syncfusion.com/demos/ejServices/api/Diagram/DeleteConnectors)

It is used to one or more connectors which needs to be deleted from database.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|data|Array|It is used to the connectors which needs to be deleted.|

### Response information 

Code: 204

### Code example 

{% highlight js %}

$.ajax({

    type: 'POST',

    contentType: 'application/json',

    url: 'http://js.syncfusion.com/demos/ejServices/api/Diagram/DeleteConnectors',

    dataType: "json",
    data: JSON.stringify([{
        "Name": "connector1",
        "SourceNode": "Diagram",
        "TargetNode": "Layout"
    }])
});

{% endhighlight %}

{% highlight c# %}

public void DeleteConnectors(List<HierarchicalDetails> data)
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


