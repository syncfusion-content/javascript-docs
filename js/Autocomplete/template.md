---
layout: post
title: Template support in AutoComplete widget for Essential JS
description: Customizes the appearance of the suggestion list using a template
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
---

# Templates

The suggestion list can be customized based on different needs using templates. The desired templates can be defined using the [template](https://help.syncfusion.com/api/js/ejautocomplete#members:template) property.

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Local Data */
                var mobileList = [
                        { pName: "Galaxy Grand 2", quantity: "3" },
                { pName: "Galaxy S6", quantity: "5" },
                { pName: "IPhone S6", quantity: "8" },
                { pName: "IPod Mini", quantity: "3" }, ];
        
        
                $('#autocomplete').ejAutocomplete({
                dataSource: mobileList,
                fields: { text: "pName" },
                template: "<div><div class='product-text'>${pName}</div> <span class='product-quantity' style='font-size:10px'> Quantity : ${quantity}</span></div>"
                });
        
        </script>
        


{% endhighlight %}



![AutoComplete-Template](template_images\template_img1.png)



