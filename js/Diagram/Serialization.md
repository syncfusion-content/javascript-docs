---
layout: post
title: Serialize the Diagram as JSON and load Diagram from serialized JSON
description: How to save and load the Diagram?
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Serialization

**Serialization** is the process of saving and loading for state persistence of the Diagram.

## Save

The Diagram is serialized as JSON data while saving. The client side method, `save` helps to serialize the Diagram as JSON. The following code illustrates how to save the Diagram.

{% highlight javascript %}

var diagram = $("#Diagram").ejDiagram("instance");

//save() returns serialized JSON data of the Diagram
var json = diagram.save();

{% endhighlight %}

This JSON data can be converted to string and stored for future use. The following snippet illustrates how to save the serialized JSON into local storage.

{% highlight javascript %}

//Saves the JSON object in to local storage
localStorage.setItem("diagram", JSON.stringify(json));

{% endhighlight %}

Diagram can also be saved as raster or vector image files. For more information about saving the Diagram as images, refer to [Exporting](/js/Diagram/Exporting "Exporting").


## Load

Diagram is loaded from the Serialized JSON data. The client side method, `load` helps you to load the Diagram from the serialized JSON. The following code illustrates how to load the Diagram from serialized JSON data.

{% highlight javascript %}

//Retrieves the json object from local storage
json = JSON.parse(localStorage.getItem("diagram"));

//Loads the Diagram from saved json data
diagram.load(json);

{% endhighlight %}

N> Before loading a new Diagram, existing Diagram is cleared.

## Limitation

There are some limitations in saving/loading the Diagrams and they are listed as follows.

* Events could be serialized only when they are defined as string. Also, the functions need to be maintained in the application level.
When they are defined as function, it is not serialized.

{% highlight javascript %}

function nodeCollectionChange(args) {
}

$("#diagram").ejDiagram({
	//Event is serialized, since it is defined as string
	nodeCollectionChange: "nodeCollectionChange"
});

$("#diagram").ejDiagram({
	//Event is not serialized, since it is defined as a function
	nodeCollectionChange: nodeCollectionChange
});

{% endhighlight %}

* HTML / Native template needs to be retained in the application level, while loading the Native and HTML node.

{% highlight html %}

<!-- Template content needs to be retained while loading the diagram.-->
<script id="htmlTemplate" type="text/x-jsrender">
	<div>
		<input type="button" value="button" style="color: #ffffff; background-color: #fbb139; border-color: #f89b1c" />
	</div>
</script>

{% endhighlight %}

{% highlight javascript %}

diagram.load(json);

{% endhighlight %}

* CSS classes have to be retained in the application level, while loading the Diagram.

{% highlight html %}

<style>
	<!-- css class needs to be retained while loading the Diagram.-->
	.nodeCss {
		fill: black;
		stroke: cyan;
	}
</style>

{% endhighlight %}

{% highlight javascript %}

diagram.load(json);

{% endhighlight %}