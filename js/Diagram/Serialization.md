---
layout: post
title: Serialization | Diagram | JavaScript | Syncfusion
description: This section explains how to process saving and loading for state persistence of the ejDiagram.
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Serialization

**Serialization** is the process of saving and loading for state persistence of the Diagram.

## Save

The Diagram is serialized as JSON data while saving. The client side method, [save](/api/js/ejdiagram#methods:save "save") helps to serialize the Diagram as JSON. The following code illustrates how to save the Diagram.

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

## Prevent serializing default model properties.

* While saving the diagram as JSON data, the size of the JSON data will be large when diagram having more number of nodes and connectors. 

* Diagram provides the support to enable/disable serializing default model properties to reduce the size of the saved JSON data through [serializationSettings](/api/js/ejdiagram#members:serializationsettings "serializationSettings") property.

* The serializationSettings [preventDefaultValues](/api/js/ejdiagram#members:serializationsettings-preventdefaultvalues "preventDefaultValues") property is used to specify whether to save the diagram with user defined model properties or entire diagram model properties.

* By default, the preventDefaultValues property value is set as false and all default properties will be serialized. If it is set to true, only user defined properties will be serialized. The following code illustrates how to use preventDefaultValues property.

{% highlight javascript %}

$("#Diagram").ejDiagram({
         //optimize the size of JSON  
         serializationSettings: {
         // serialize user defined model properties when preventDefaultValues is true.  
         preventDefaultValues: true
      }
 });

{% endhighlight %}

## Load

Diagram is loaded from the Serialized JSON data. The client side method, [load](/api/js/ejdiagram#methods:load "load") helps you to load the Diagram from the serialized JSON. The following code illustrates how to load the Diagram from serialized JSON data.

{% highlight javascript %}

//Retrieves the json object from local storage
json = JSON.parse(localStorage.getItem("diagram"));

//Loads the Diagram from saved json data
diagram.load(json);

{% endhighlight %}

N> Before loading a new Diagram, existing Diagram is cleared.

## Upgrade

You can upgrade older version JSON to newer version without loading it. Please refer to below link which shows how to use upgrade method in diagram.

[upgrade](/api/js/ejdiagram#methods:upgrade "upgrade")

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


## Clear

The public method [clear](/api/js/ejdiagram#methods:clear "clear") allows you to remove all the elements from the diagram and [refresh](/api/js/ejdiagram#methods:refresh "refresh") method used to refresh the whole diagram page.