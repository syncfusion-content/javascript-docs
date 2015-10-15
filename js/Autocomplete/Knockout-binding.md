---
layout: post
title: Knockout-binding
description: knockout binding
platform: js
control: AutoComplete
documentation: ug
---

# Knockout binding

**Knockout** support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the AutoComplete widget. The changes made in AutoComplete widget are not reflected and triggered in turn to the observable collection. This kind of binding is applied to all the properties of the AutoComplete widget.

**Two-way binding** supports both the processes. It applies the observable values to the AutoComplete widget properties and also the changes made in the AutoComplete widget are reflected back and triggered within the observable collections. 

For more information about **Knockout** binding, you can refer the online documentation in the following link location,

<http://docs.syncfusion.com/js/knockoutjs>

The following example depicts how you can bind data to the **AutoComplete** widget through **knockout** support that enables and populates data to an AutoComplete widget based on the value set to the other AutoComplete widget.

{% highlight html %}

<!doctype html>
<html>
   <head>
      <title>Essential Studio for JavaScript : Autocomplete - KnockOut</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"> </script>
   </head>
   <body>
      <div class="content-container-fluid">
         <div class="row">
            <div class="control" style="margin: auto; width: 500px;">
               <div class="countryList" style="float: left; width: 45%">
                  <label class="txt">
                  Select Country</label>
                  <input id="country" data-bind='value: countryName, valueUpdate: ["onchange", "input", "blur"]' />
               </div>
               <div class="stateList" style="float: right; width: 45%">
                  <label class="txt">
                  Select State</label>
                  <input id="state" data-bind='value: stateName' />
               </div>
            </div>
         </div>
      </div>
      <script type="text/javascript" class="jsScript">
         var autocomplete;
         $(function () {
             var countryList = ["United States", "Australia", "Austria", "India"];
             $('#country').ejAutocomplete({
                 watermarkText: "Select country",
                 showPopupButton: true,
                 dataSource: countryList
             });
             $('#state').ejAutocomplete({
                 showPopupButton: true
             });
             var stateObj = $('#state').data("ejAutocomplete");
             stateObj.disable();
             // declaration             
             var ViewModel = function () {
                 var usaStates = ["California", "New York", "South Carolina", "Washington"];
                 var australiaStates = ["West Island", "Sydney", "Kingston", "Melbourne"];
                 var austriaStates = ["Burgenland", "Carinthia", "Styria", "Vienna"];
                 var indiaStates = ["Tamil Nadu", "Rajasthan", "West Bengal", "Maharashtra"];
         
                 this.countryName = ko.observable();
                 this.stateName = ko.computed(function () {
                     var source = null;
                     switch (this.countryName()) {
                         case "United States": source = usaStates; break;
                         case "Australia": source = australiaStates; break;
                         case "Austria": source = austriaStates; break;
                         case "India": source = indiaStates; break;
                     }
                     if (source) {
                         stateObj.enable();
                         stateObj.setModel({ dataSource: source });
                         return source[0];
                     }
                     else stateObj.setModel({ dataSource: null });
         
                     return "";
                 }, this);
             };
             ko.applyBindings(new ViewModel());
             autocompleteCountry = $('#country').data("ejAutocomplete");
             autocompleteState = $('#state').data("ejAutocomplete");
         });
      </script>
   </body>
</html>


{% endhighlight %}



The following image is the result of the above code example.

{% include image.html url="/js/Autocomplete/Knockout-binding_images/Knockout-binding_img1.png"%}

