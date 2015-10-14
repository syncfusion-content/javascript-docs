---
layout: post
title: Tooltip-Support
description: tooltip support
platform: js
control: ListBox
documentation: ug
---

# Tooltip Support

The following steps explains you the configuration of **tooltip** properties in **ListBox**.

In an **HTML** page, add a &lt;ul&gt; element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


    jQuery(function($) {
       var skillset = [{
          skill: "ASP.NET",
          tooltip: "ASP.NET"
       }, {
          skill: "ActionScript",
          tooltip: "ActionScript"
       }, {
          skill: "Basic",
          tooltip: "Basic"
       }, {
          skill: "C++",
          tooltip: "C++"
       }, {
          skill: "C#",
          tooltip: "C#"
       }, {
          skill: "dBase",
          tooltip: "dBase"
       }, {
          skill: "Delphi",
          tooltip: "Delphi"
       }, {
          skill: "ESPOL",
          tooltip: "ESPOL"
       }, {
          skill: "F#",
          tooltip: "F#"
       }, {
          skill: "FoxPro",
          tooltip: "FoxPro"
       }, {
          skill: "Java",
          tooltip: "Java"
       }, {
          skill: "J#",
          tooltip: "J#"
       }, {
          skill: "Lisp",
          tooltip: "Lisp"
       }, {
          skill: "Logo",
          tooltip: "Logo"
       }, {
          skill: "PHP",
          tooltip: "PHP"
       }];
       $("#listboxSample").ejListBox({
          dataSource: skillset,
          width: "350",
          enableTooltip: true,
          fields: {
             text: "skill",
             toolTipText: "tooltip"
          }
       });
    });


{% endhighlight %}

Output of the above steps.

![]("/js/ListBox/Tooltip-Support_images/Tooltip-Support_img1.png")

