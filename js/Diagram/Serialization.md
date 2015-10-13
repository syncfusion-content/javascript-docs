---
layout: post
title: Serialization
description: serialization
platform: js
control: Diagram
documentation: ug
---

# Serialization

**Serialization** is the process of saving and loading for state persistence of diagram.

## Save 

The Diagram is serialized as JSON data while saving. The client side method `save` helps to serialize the diagram as JSON. The following code illustrates how to save diagram.

{% highlight js %}

	var diagram = $("#Diagram").ejDiagram("instance");
    	
	//save() returns serialized JSON data of diagram	
	var json = diagram.save();

{% endhighlight %}

This json data can be converted to string and stored for future use. The following snippet illustrates how to save the serialized JSON into local storage.

{% highlight js %}
    
     //Save the json object in to local storage
     localStorage.setItem("diagram", JSON.stringify(json));
   
{% endhighlight %}  

Diagram can also be saved as raster or vector image files. For more information about saving diagram as images,  refer [Exporting](/js/Diagram/Exporting).


## Load

Diagram is loaded from the Serialized JSON data. The client side method `load` helps you to load the diagram from the serialized JSON. The following code illustrates how to load diagram from serialized JSON data. 

{% highlight js %}

     //Retrieive the json object from local storage
     json = JSON.parse(localStorage.getItem("diagram"));

	 //load the diagram from saved json data 	
	 diagram.load(json);

{% endhighlight %}

N> Before loading a new diagram, existing diagram will be cleared.

## Limitation

There are some limitations in saving/loading diagrams and they are listed below.

* Events could be serialized if and only if they are defined as string. Also the functions need to be maintained in the application level. 
If they are defined as function, it won't be serialized.

{% highlight js %}

        function nodeCollectionChange(args) {
        }

        $("#diagram").ejDiagram({
            //Event will be serialized, since it is defined as string
            nodeCollectionChange: "nodeCollectionChange"
        });

        $("#diagram").ejDiagram({
            //Event will not be serialized, since it is defined as a function
            nodeCollectionChange: nodeCollectionChange
        });
	
{% endhighlight %}
	
* Html / Native template needs to be retained in the application level, while loading the native and html node.

{% highlight html %}
 
    <!-- Template content needs to be retained while loading the diagram.-->
    <script id="htmlTemplate" type="text/x-jsrender">
        <div>
            <input type="button" value="button" style="color: #ffffff; background-color: #fbb139; border-color: #f89b1c" />
        </div>
    </script>
        
{% endhighlight %}
 
{% highlight js %}
 
    diagram.load(json);
 
{% endhighlight %}

* Css classes have to be retained in the application level, while loading the diagram.
	
{% highlight html %}

    <style>
	 <!-- css class needs to be retained while loading the diagram.-->
        .nodeCss {
            fill: black;
            stroke: cyan;
        }
    </style>
         
{% endhighlight %}
 
{% highlight js %}
 
     diagram.load(json);
 
{% endhighlight %}