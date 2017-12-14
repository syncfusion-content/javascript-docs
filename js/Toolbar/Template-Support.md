---
layout: post
title: Template-Support
description: template support
platform: js
control: Toolbar
documentation: ug
api: /api/js/ejtoolbar
---

# Template Support

Template allows you to insert custom controls inside the toolbar items. Also you can design simple drop down buttons listing the items and radio button inside the **Toolbar**.

Set the list for **DropDown control** inside a list tag and define this tag as a **Toolbar** item. You can use all simple controls as a **Toolbar** item. To add RadioButton and DropDownList to **Toolbar**, use the following code example.

{% highlight html %}

<div id="toolbar">
   <ul>
      <li>
         <div>
            <input type="radio" name="small" id="Radio1" />
         </div>
         Option 1
      </li>
      <li id="Dropdown" title="Dropdown Control">
         <input id="selectCar" type="text" />
        
      </li>
   </ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        // declaration
          var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
        $("#Radio1").ejRadioButton({ size:"medium" });
        $('#selectCar').ejDropDownList({ dataSource: skills, fields: { text: "skill" },watermarkText: "Select your skill",});
        $("#toolbar").ejToolbar({ width: "250px", height: "28px" });
    });


{% endhighlight %}


##Through [items](https://help.syncfusion.com/api/js/ejtoolbar#members:Items) API:

{% highlight html %}

    <div id="toolbar"></div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        
          var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
        $("#toolbar").ejToolbar({
        
			 Items:[
                    {id:"item1",group:"group1",template:"<input type='radio' id='Radio1' name='radio'>Option 1</input>"},
					{id: "item2",group:"group2",template:"<input type='text' id='dropdown1' />"}
					],

             
			  });
               $("#Radio1").ejRadioButton({size:"medium"});
                $('#dropdown1').ejDropDownList({
                dataSource: skills,
                fields: { text: "skill" },
                watermarkText: "Select your skill",
               
            });
    });


{% endhighlight %}

##Through template field in dataSource API:

{% highlight html %}

    <div id="toolbar"></div>

{% endhighlight %}

{% highlight js %}

    $(function () {
      var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
     toolbarItems = [
		  {
               id: "1",
               title:"radio",
			   template:"<input type='radio' id='radio1'>Option 1</input>",
			   groups:"group1"

            },
			 {
			         id:"2",
					 title:"dropdown",
					 template:"<input type='text' id='dropdown2'></div>",
					 group:"group2"
			 }],
        
        $("#toolbar").ejToolbar({
			  dataSource: toolbarItems,
              fields: { id: "id",tooltipText:"title",group:"group",template:"template"},

             
			  });
              $("#radio1").ejRadioButton({size:"medium"});
              $('#dropdown2').ejDropDownList({
                dataSource: skills,
                fields: { text: "skill" },
                watermarkText: "Select your skill",
              
                
            });
    });


{% endhighlight %}

The following screenshot displays a Toolbar with embedded controls.

![](Template-Support_images/Template.JPG)
