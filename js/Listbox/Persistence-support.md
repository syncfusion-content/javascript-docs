---
layout: post
title: Persistence-support
description: persistence support 
platform: js
control: ListBox
documentation: ug
---

# Persistence support 

This features enables you to save current model value to browser cookies for state maintains. When you refresh the **ListBox** control page, it retains the model value apply from browser cookies. The date type of **enablePersistence** is Boolean type. 

The following steps explains you the configuration of **enablePersistence** property in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       // JSON data declaration
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       //Render ListBox by mapping fields with JSON data
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          enablePersistence: true
       });
    });

{% endhighlight %}

