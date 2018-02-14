---
layout: post
title: Cascading in ComboBox widget for Syncfusion Essential JS
description: Describes about the cascading, autofill in ComboBox widget for Syncfusion Essential JS
platform: js
control: ComboBox
documentation: ug
keywords: ComboBox, combobox, Cascading ComboBox, Autofill supported with ComboBox
---

# How To

## Configure the Cascading ComboBox

The cascading ComboBox is a series of ComboBox, where the value of one ComboBox depends upon  another's value. This can be configured by using the [change](https://help.syncfusion.com/api/js/ejcombobox#events:change) event of the parent ComboBox.
Within that change event handler, data has to be loaded to the child ComboBox based on the selected value of the parent ComboBox.

The following example, shows the cascade behavior of country, state, and city ComboBox. Here, the `dataBind` method is used to reflect the property changes immediately
to the ComboBox.

{% highlight html %}
	
    <input type="text" tabindex="1" id="list" /> <br/><br/>
    <input type="text" tabindex="1" id="list2" /> <br/><br/>
    <input type="text" tabindex="1" id="list3" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">
    var country = [
        { countryName: 'United States', countryId: '1' },
        { countryName: 'Australia', countryId: '2' }
    ];
    var state = [
        { stateName: 'New York', countryId: '1', stateId: '101' },
        { stateName: 'Virginia', countryId: '1', stateId: '102' },
        { stateName: 'Washington', countryId: '1', stateId: '103' },
        { stateName: 'Queensland', countryId: '2', stateId: '104' },
        { stateName: 'Tasmania', countryId: '2', stateId: '105' },
        { stateName: 'Victoria', countryId: '2', stateId: '106' }
    ];
    var cities = [
        { cityName: 'Albany', stateId: '101', cityId: 201 },
        { cityName: 'Beacon', stateId: '101', cityId: 202 },
        { cityName: 'Lockport', stateId: '101', cityId: 203 },
        { cityName: 'Alexandria', stateId: '102', cityId: 204 },
        { cityName: 'Hampton', stateId: '102', cityId: 205 },
        { cityName: 'Emporia', stateId: '102', cityId: 206 },
        { cityName: 'Aberdeen', stateId: '103', cityId: 207 },
        { cityName: 'Colville', stateId: '103', cityId: 208 },
        { cityName: 'Pasco', stateId: '103', cityId: 209 },
        { cityName: 'Townsville', stateId: '104', cityId: 210 },
        { cityName: 'Brisbane', stateId: '104', cityId: 211 },
        { cityName: 'Cairns', stateId: '104', cityId: 212 },
        { cityName: 'Hobart', stateId: '105', cityId: 213 },
        { cityName: 'Launceston', stateId: '105', cityId: 214 },
        { cityName: 'Devonport', stateId: '105', cityId: 215 },
        { cityName: 'Melbourne', stateId: '106', cityId: 216 },
        { cityName: 'Healesville', stateId: '106', cityId: 217 },
        { cityName: 'Geelong', stateId: '106', cityId: 218 }
    ];
    $(function () {
        $('#list').ejComboBox({
            dataSource: country,
            fields: { value: 'countryId', text: 'countryName' },
            change: function (e) {
                listObj1 = $('#list2').ejComboBox("instance");
                listObj1.option({ enabled: true, query: new ej.Query().where('countryId', 'equal', e.model.value) ,value:null});
                listObj2 = $('#list3').ejComboBox("instance");
                listObj2.option({ enabled: false, value: null });
            },
            width: '250px',
            placeholder: 'Select a country',
            popupWidth: '250px',
            popupHeight: '83px'
        });
        
        $('#list2').ejComboBox({
            dataSource: state,
            fields: { value: 'stateId', text: 'stateName' },
            enabled: false,
            change: function (e) {
                listObj2 = $('#list3').ejComboBox("instance");
                listObj2.option({ enabled: true, query: new ej.Query().where('stateId', 'equal', e.model.value), value: null });
            },
            width: '250px',
            placeholder: 'Select a state',
            popupWidth: '250px',
            popupHeight: '123px'
        });
        
        $('#list3').ejComboBox({
            dataSource: cities,
            fields: { text: 'cityName',value: 'cityName' },
            enabled: false,
            width: '250px',
            placeholder: 'Select a city',
            popupWidth: '250px',
            popupHeight: '123px'
        });
    });
</script>	
		
{% endhighlight %}

![](HowTo-images/image1.png)

## Show the list items with icons

You can render **icons** to the list items by mapping the [iconCss](https://help.syncfusion.com/api/js/ejcombobox#members:fields-iconcss) &nbsp;field. This `iconCss` field create a span in the list item with mapped class name
to allow styling as per your need.

In the following sample, icon classes are mapped with `iconCss` field.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
var sortFormatData = [
    { class: 'asc-sort', type: 'Sort A to Z', id: '1' },
    { class: 'desc-sort', type: 'Sort Z to A ', id: '2' },
    { class: 'filter', type: 'Filter', id: '3' },
    { class: 'clear', type: 'Clear', id: '4' }
];
$(function () {
    $('#list').ejComboBox({
        dataSource: sortFormatData,
        // map the icon column to iconCSS field.
        fields: { text: 'type', iconCss: 'class', value: 'id' },
        placeholder: 'Select a format'
    });
});	
		
{% endhighlight %}

{% highlight css %}	

    <style>
        #container {
            visibility: hidden;
        }
        #loader {
        color: #008cff;
        height: 40px;
        width: 30%;
        position: absolute;
        top: 45%;
        left: 45%;
        }
        .e-list-icon{
            line-height: 1.3;
            padding-right: 10px;
            text-indent: 5px;
        }
        .asc-sort:before {
            content: '\e73f';
            font-family: 'e-icons';  
            font-size: 20px;

        }
        .desc-sort:before {
            content: '\e721';
            font-family: 'e-icons';   
            font-size: 20px;
        }
        .filter:before {
            content: '\e818';
            font-family: 'e-icons';  
            font-size: 20px;
            opacity: 0.78;
        }
        .clear:before {
            content: '\e7db';
            font-family: 'e-icons';  
            font-size: 20px;
        }
    </style>

{% endhighlight %}

## Autofill supported with ComboBox

The ComboBox supports the `autofill` behavior with the help of [autofill](https://help.syncfusion.com/api/js/ejcombobox#members:autofill) property. Whenever you change the input value, the ComboBox will autocomplete your data by matching the typed character. Suppose, if no matches
found then, comboBox doesn't suggest any item.

In the following sample, showcase that how to work autofill with ComboBox.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
var sportData = [
    { id: 'level1', game: 'American Football' }, { id: 'level2', game: 'Badminton' },
    { id: 'level3', game: 'Basketball' }, { id: 'level4', game: 'Cricket' },
    { id: 'level5', game: 'Football' }, { id: 'level6', game: 'Golf' },
    { id: 'level7', game: 'Hockey' }, { id: 'level8', game: 'Rugby' },
    { id: 'level9', game: 'Snooker' }, { id: 'level10', game: 'Tennis' }
];
$(function () {
    $("#list").ejComboBox({
        dataSource: sportData,
        fields: { text: 'game', value: 'id' },
        width: '250px',
        autofill: true,
        placeholder: 'Select a game',
        index: -1
    });
});			
		
{% endhighlight %}

![](HowTo-images/image2.png)


## Validation of ComboBox using jQuery Validator

Validation of ComboBox can be done on form submission using jQuery Validations by adding name attribute for ComboBox through `htmlAttributes` property. Also, you can remove this error message during item selection through select or change event of ComboBox

N> [jquery.validate.min](http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js) script file should be referred for validation, for more details, refer [here](http://jqueryvalidation.org/documentation).

{% highlight html%}

     <form id="form1">
       <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <div class="control">
                        <input type="text" tabindex="1" id="list" />
                    </div>
                   <label class="message"></label>
                </div>
            </div>
            <button type="submit" id="valid" onclick="validate()"> Validate</button>
        </div>
    </div>
    <script type="text/javascript">
        var empList = [
        { id: 'level1', country: 'American Football' }, { id: 'level2', country: 'Badminton' },
        { id: 'level3', country: 'Basketball' }, { id: 'level4', country: 'Cricket' },
        { id: 'level5', country: 'Football' }, { id: 'level6', country: 'Golf' },
        { id: 'level7', country: 'Hockey' }, { id: 'level8', country: 'Rugby' },
        { id: 'level9', country: 'Snooker' }, { id: 'level10', country: 'Tennis' }
		];
        $(function () {
            $("#list").ejComboBox({
				dataSource: empList,
				fields: { text: 'country', value: 'id' },
				width: '250px',
				placeholder: 'Select a game',
				index: -1,
                htmlAttributes: { name: 'select'},
				popupHeight: '200px',
				popupWidth: '250px',
                select:'select'
			});
        });
        
          function validate()
          {
            var rules = {};
            $("form[id$=form1] input[name$=select]").each(function () {
                rules[this.name] = "required";
            });
            $('form[id$="form1"]').validate({
                rules: rules,
                errorPlacement: function (error, element) {
                    $(error).insertAfter($(".message"));
                }
            });
          }
         function select(args)
          {
            if(args.value!="")
            {
               $("label.error").css("display", "none")  //hide error message when value is selected.
            }
          }
       </script>
     </form>

{% endhighlight%}