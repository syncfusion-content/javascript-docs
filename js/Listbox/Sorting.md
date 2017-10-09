---
layout: post
title: Sorting
description: sorting support
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Sorting

 We can change ListBox items rendering order either as ascending or descending, by using [ej.SortOrder](https://help.syncfusion.com/api/js/ejlistbox#members:sortorder) property. By default ej.SortOrder will be "None". Please use code as like in below,

 {% tabs %} 
 {% highlight html %}

     <div class="contents">
          <ul id="selectSection"></ul> 
    </div>

 {% endhighlight %}

 {% highlight javascript %}

    <script type="text/javascript">
            jQuery(function ($) {
            var skills = [{ skill: "F#" }, { skill: "ActionScript" }, { skill: "Delphi" }, { skill: "Basic" },
            { skill: "C++" }, { skill: "ESPOL" }, { skill: "C#" }, { skill: "DBase" }, { skill: "ASP.NET" }
            ];
            $("#selectSection").ejListBox({
                width: "220", dataSource: skills,
                fields: { text: "skill" },
                sortOrder:ej.SortOrder.Descending
                 })
                 });
      </script>

  {% endhighlight %}
   {% endtabs %} 
  
  ![Sorting image](Sorting_Images\Sorting_img1.png)
   
Virtual scrolling is not supported with Sorting.
