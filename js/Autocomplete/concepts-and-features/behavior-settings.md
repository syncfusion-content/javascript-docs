---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: AutoComplete
documentation: ug
---

# Behavior Settings

## Filtering Type

**AutoComplete** textbox supports a wide range of filtering options to search items in the **PopUp** list. The **filterType** takes **enum** or **string** values, like **startswith**, the default value contain endswith, lessthan, greaterthan, greaterthanorequal, lessthanorequal, equal and notequal.

### Defining the Filter type

The following steps explain the configuration of the filtering conditions for an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Configure filter type for **AutoComplete** control as follows.



{% highlight js %}

**[JavaScript]**

    <script type="text/javascript">
       // Define the local JSON data
        var carList = [
                    "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                    "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                    "Chevrolet Camaro", "Cadillac ",
                    "Duesenberg J ", "Dodge Sprinter",
                    "Elantra", "Excavator",
                    "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
                    "GAZ Siber",
                    "Honda S2000", "Hyundai Santro",
                    "Isuzu Swift", "Infiniti Skyline",
                    "Jaguar XJS",
                    "Kia Sedona EX", "Koenigsegg Agera",
                    "Lotus Esprit", "Lamborghini Diablo ",
                    "Mercedes-Benz ", "Mercury Coupe", "Maruti Alto 800",
                    "Nissan Qashqai",
                    "Oldsmobile S98", "Opel Superboss",
                    "Porsche 356 ", "Pontiac Sunbird",
                    "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
                    "Triumph Spitfire ", "Toyota 2000GT",
                    "Volvo P1800", "Volkswagen Shirako"
        ];
        $(function () {
            // declaration
            $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
                filterType: "endswith"
            });
        });
    </script>


{% endhighlight %}





The following image is the output for **AutoComplete** control that filters list items based on the **endswith** option.

![](behavior-settings_images\behavior-settings_img1.png)

_Figure 10: AutoComplete using "endswith" filterType_

## AutoFill

The **AutoComplete** textbox****widget offers an **AutoFill** option. This feature is used to automatically fill the item when text is entered when **enableAutoFill** is set to ‘**True**’. The first Item in the suggestions list that matches the entered text is automatically displayed in the **AutoComplete** textbox. The search text is selected in the **AutoComplete** textbox for identification. 

This feature reduces the need to type the entire text and makes the search box more efficient. This is used only with filterType “**startswith**”, since text is filled automatically based on the text entered.

### Configure AutoFill property in AutoComplete 	

The following steps explain how to enable the **AutoFill** property for an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Enable **AutoFill** for AutoComplete control as follows.



{% highlight js %}

**[JavaScript]**

   // Here define CarList local data as per the previous the code block.

    $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
                filterType: "startswith",
**enableAutoFill**: **true**
            });



{% endhighlight %}



The following image is the output for **AutoComplete** when **enableAutoFill** is set to ‘**True**’.

![](behavior-settings_images\behavior-settings_img2.png)

_Figure 11: AutoComplete with AutoFill_

## Sorting Items

**AutoComplete** widget allows you to sort the suggestions list items and set the sorting order. To enable sorting, set **allowSorting** to ‘**True**’. It is enabled by default. The **sortOrder** property takes **enum** values, either in ascending or descending order.

### Steps to define sorting order and distinct

The following steps explain how to enable the **sorting** property for an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Configure the **Sorting** property for **AutoComplete** control as follows.



{% highlight js %}

**[JavaScript]**

// Here define CarList local data as per the previous the code block.

    $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
                filterType: "startswith",
**allowSorting:true,**
                **sortOrder: "descending",**
            });



{% endhighlight %}





The following image is the output for **AutoComplete** when “**sortOrder**” is configured.



![](behavior-settings_images\behavior-settings_img3.png)

_Figure 12: AutoComplete PopUp sorted in descending order_

## Distinct List items

**AutoComplete** widget provides an option to extract repeating items in the **PopUp** list. By setting **enableDistinct** property to ‘**True**’, you can prevent the duplicate items in the suggestions list.

### Steps to enable distinct items

The following steps explain you how to enable the **distinct** property for an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.



{% highlight html %}

**[HTML]**
<div style="margin-right: 20px;">
    <div class="txt">Distinct disabled</div>
    <input type="text" id="autocomplete">
 </div>
 <div>
     <div class="txt">Distinct enabled</div>
      <input type="text" id="autocompletedistinct">
 </div>



{% endhighlight %}



* Configure the Distinct property for **AutoComplete** control as follows,



{% highlight js %}

**[JavaScript]**

     <script type="text/javascript">
        var carList = [
                    "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                    "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                    "Chevrolet Camaro", "Cadillac ",
                    "Duesenberg J ", "Dodge Sprinter",
                    "Elantra", "Excavator",
                    "Ford Boss 302", "Ford Boss 302", "Ferrari 360", "Ferrari 360", "Ford Thunderbird ",
                    "GAZ Siber",
                    "Honda S2000", "Hyundai Santro",
                    "Isuzu Swift", "Infiniti Skyline",
                    "Jaguar XJS",
                    "Kia Sedona EX", "Koenigsegg Agera",
                    "Lotus Esprit", "Lamborghini Diablo ",
                    "Mercedes-Benz ", "Mercury Coupe", "Maruti Alto 800",
                    "Nissan Qashqai",
                    "Oldsmobile S98", "Opel Superboss",
                    "Porsche 356 ", "Pontiac Sunbird",
                    "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
                    "Triumph Spitfire ", "Toyota 2000GT",
                    "Volvo P1800", "Volkswagen Shirako"
        ];
        $(function () {
            // declaration
            $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList
            });
            $('#autocompletedistinct').ejAutocomplete({
                width: 205,
                dataSource: carList,
                enableDistinct: true
            });
        });
    </script>


{% endhighlight %}





The following images are the outputs for **AutoComplete** when **enableDistinct** is set to “**True”** and “**False**”.



![](behavior-settings_images\behavior-settings_img4.png)

_Figure 13: AutoComplete PopUp items with Distinct property disabled and enabled_

## Show Popup button

**Show Popup button** property provides you with an option to display an icon, to show the popup list in the **AutoComplete** widget.

### Enabling Popup button

The following steps explains you how to configure the **Popup****button** for an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Enable **showPopupButton** for **AutoComplete** control as follows.



{% highlight js %}

**[JavaScript]**

// Here define CarList local data as per the previous the code block.

$('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
**showPopupButton:true,**
            });



{% endhighlight %}





The following image is the output for **AutoComplete** when **showPopupButton** is enabled.

![](behavior-settings_images\behavior-settings_img5.png)

_Figure 14: AutoComplete with popup icon_

## Restrict editing

**AutoComplete** textbox widget provides **readOnly** property to disable editing in the control, so that the value set to **AutoComplete** can only be read and cannot be modified by the user. The value property allows you to set the default value for **AutoComplete** widget, when it is created.

### Configure AutoComplete textbox to restrict editing

The following steps help you to disable editing in an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Configure **readOnly** property in **AutoComplete** control as follows.



{% highlight js %}

**[JavaScript]**

// Here define CarList local data as per the previous the code block.

    $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
**readOnly:true,**
                showPopupButton:true,
                value:"BMW 7"
            });



{% endhighlight %}





The following image is the output for the **AutoComplete** textbox configured to restrict editing.

![](behavior-settings_images\behavior-settings_img6.png)

_Figure 15: AutoComplete with readOnly property_

## Empty Result settings

The **AutoComplete** widget allows you to configure the display message when the list doesn’t return any values. By default, **showEmptyResultText** is set to ‘**True**’ and **emptyResultText** is set to the string value “**No suggestions**_”._ 

### Configure Empty result setting

The following steps allow you to set text for **empty****results** of an **AutoComplete** textbox.

* In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.



{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



* Set text to **emptyResultText** property in **AutoComplete** control as follows.



{% highlight js %}

**[JavaScript]**

// Here define CarList local data as per the previous the code block.

    $('#autocomplete').ejAutocomplete({
                width: 310,
                dataSource: carList,
**showEmptyResultText: true,**
                **emptyResultText:"Item not found in list"**
            });



{% endhighlight %}





The following image is the output of the **AutoComplete** textbox when the list doesn’t return any value.

![](behavior-settings_images\behavior-settings_img7.png)

_Figure 16: AutoComplete with customized emptyResultText_

