---
layout: post
title: Template
description: template 
platform: js
control: Rotator
documentation: ug
api: /api/js/ejrotator
---

# Template 

The Rotator widget’s appearance can be customized based on different needs using templates. The desired templates can be defined using the “template” property.

You can refer the following code example of template in Rotator.


  {% highlight html %}
  
            <div class="cols-sample-area">
                <div class="frame">
                    <ul id="sliderContent">                        
                    </ul>
                </div>
            </div>


  {% endhighlight %}
    
  {% highlight javascript %}

  $(function () {		
		    var themesList = [
				{ text: "Colorful-Night", url: "../content/images/rotator/snowfall.jpg" },
				{ text: "Technology", url: "../content/images/rotator/tablet.jpg" },
				{ text: "Nature", url: "../content/images/rotator/nature.jpg" },
				{ text: "Snow Fall", url: "../content/images/rotator/snowfall.jpg" },
				{ text: "Credit Card", url: "../content/images/rotator/card.jpg" },
				{ text: "Beautiful Bird", url: "../content/images/rotator/bird.jpg" },
				{ text: "Amazing Sculptures", url: "../content/images/rotator/sculpture.jpg" }				
				];

        $("#sliderContent").ejRotator({
			    dataSource: themesList,
          slideWidth: "100%",
          frameSpace: "0px",
				  slideHeight: "auto",
				  template: '<div class="image"><img src = ${url} title = ${text} class="image"/> </div>' 				
        });
    });


  {% endhighlight %}


