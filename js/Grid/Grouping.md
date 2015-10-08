---
layout: post
title: Grouping
description: grouping
platform: js
control: Grid
documentation: ug
---

# Grouping

**Grouping** is an important feature in **Grid**. If you want to analysis any particular records, based on its category, you can simply group that column and analyse records based on category. There are several flexible options, such as grouped buttons, group close etc. To enable **Grouping** in **Grid**, add [`allowGrouping`](/js/api/ejgrid#members:allowgrouping "allowGrouping") at **Grid Initialize**. 

## Initial Grouping

In **ejGrid**, there is an option to group columns at **Grid Initialize** that is rendered through [`groupedColumns`](/js/api/ejgrid#members:groupsettings-groupedcolumns "groupedColumns") and [`allowGrouping`](/js/api/ejgrid#members:allowgrouping "allowGrouping") property in **Grid**. This is an important option because in some scenarios, need to analyse **Grid** records with **Grouping** may arise, at the time of initialize.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          //window.gridData is refered from jsondata.min.js
          dataSource: window.gridData,
          groupSettings: { groupedColumns: ["ShipCity"] },
          allowGrouping: true,
          allowPaging: true,
  
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

![]("/js/Grid/Grouping_images/Grouping_img1.png")

## Group Buttons

Group buttons is one of the features under Grouping. It is helpful to do Grouping easily without doing drag and drop. To enable this feature use [`showToggleButton`](/js/api/ejgrid#members:groupsettings-showgroupedcolumn "showToggleButton") at **Grid Initialize**.  

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          //window.gridData is refered from jsondata.min.js
          dataSource: window.gridData,
          allowGrouping: true,
          groupSettings: { showToggleButton: true, groupedColumns: ["ShipCity"] },
          allowPaging: true,
  
      });
  });
  
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

![]("/js/Grid/Grouping_images/Grouping_img2.png")

## Hide Ungroup Button

In **GroupDropArea**, grouped columns have an option to ungroup a column using **GroupButton**. It is easier than using Drag and Drop to ungroup columns.  By default this **UngroupButton** is visible. If you want to hide this button, you can use [`showUngroupButton`](/js/api/ejgrid#members:groupsettings-showungroupbutton "showUngroupButton") property to hide columns.

![]("/js/Grid/Grouping_images/Grouping_img3.png")

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          //window.gridData is refered from jsondata.min.js
          dataSource: window.gridData,
          groupSettings: { showUngroupButton: false, groupedColumns: ["ShipCity"] },
          allowGrouping: true,
          allowPaging: true,
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

![]("/js/Grid/Grouping_images/Grouping_img4.png")

## AutoSize Drop Area

If you drag any header to Group column in Grid, it expands smoothly its Group Drop Area portion. In some scenarios, you need to stop this type of animation while grouping. You can use the [`enableDropAreaAutoSizing`](/js/api/ejgrid#members:groupsettings-enabledropareaautosizing "enableDropAreaAutoSizing") property to stop animation in Group Drop Area.

{% highlight html %}

    
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          //window.gridData is refered from jsondata.min.js
          dataSource: window.gridData,
          groupSettings: { enableDropAreaAutoSizing: false },
          allowGrouping: true,
          allowPaging: true,
      });
  });
</script>



{% endhighlight %}



The following output is displayed as a result of the above code example.

![]("/js/Grid/Grouping_images/Grouping_img5.png")

## Hide Group Drop Area from Grid

In **ejGrid**, there is an option to hide the **Group Drop Area** at **Grid Initialize** that is achieved through the [`showDropArea`](/js/api/ejgrid#members:groupsettings-showdroparea "showDropArea") property of a [`groupSettings`](/js/api/ejgrid#members:groupsettings "groupSettings") in **the Grid.** The default value is **true**. By using this property, you can avoid ungrouping or further grouping of a column after the initial column grouping.

When the [`showDropArea`](/js/api/ejgrid#members:groupsettings-showdroparea "showDropArea") property is set to **false**, the **groupDropArea** is hidden. 

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowGrouping: true,
          groupSettings: { groupedColumns: ["ShipCountry"],showDropArea: false }
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

![]("/js/Grid/Grouping_images/Grouping_img6.png")

