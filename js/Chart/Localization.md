---
layout: post
title: Localization
description: localization
platform: js
control: Chart
documentation: ug
---

# Localization

EjChart supports localization for its axis labels and tooltip. To render the chart with specific culture you have to refer the corresponding **globalize** culture script and need to specify the culture name in [locale](../api/ejchart#members:locale) property of chart.   

{% highlight html %}


<head> 
<!--Refer french globalize culture script-->
<script src="../scripts/cultures/globalize.culture.fr-FR.min.js"></script>
</head>

<body>
    <div id="chartcontainer"></div>
   
<script>
      $("#chartcontainer").ejChart({
                  //  ...
                  //Render chart in french locale
                  locale: 'fr-FR',
      });
  </script>

</body>


{% endhighlight %}

![](/js/Chart/Localization_images/Localization_img1.png)

Chart with french localization
{:.caption}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/localization) here to view the localization chart online demo sample.


