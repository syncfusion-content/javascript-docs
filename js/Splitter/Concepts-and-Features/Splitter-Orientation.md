---
layout: post
title: Splitter-Orientation
description: splitter orientation
platform: js
control: Splitter
documentation: ug
---

# Splitter Orientation

The **Splitter** supports both vertical and horizontal orientation of the pane. You can declare the orientation by using **enum**, **ej.Orientation.Vertical** or **ej.Orientation.Horizontal**, that have the corresponding value of vertical and horizontal as a string.

## Configure Splitter Orientation

 The following steps explain the implementation of **Splitter** orientation option.

* In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** widget. 

{% highlight html %}

        <div id="splitter">
            <div>
                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>
            </div>
            <div>
                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>
            </div>
        </div>

{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
	        $("#splitter").ejSplitter({
            height: 280, width: 400,
            orientation: ej.Orientation.Vertical,
        });  
</script>

{% endhighlight %}


The output for **Splitter** with **ej.Orientation.Vertical**.

{% include image.html url="/js/Splitter/Concepts-and-Features/Splitter-Orientation_images/Splitter-Orientation_img1.png" Caption="Figure 5: Splitter with vertical orientation "%}

The output for **Splitter** with **ej.Orientation.Horizontal**.



{% include image.html url="/js/Splitter/Concepts-and-Features/Splitter-Orientation_images/Splitter-Orientation_img2.png" Caption="Figure 6: Splitter with horizontal orientation"%}

