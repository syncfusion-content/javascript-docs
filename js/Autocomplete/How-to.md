---
layout: post
title: How to | Syncfusion | Autocomplete
description: The how to section explain more functionalities or informations about Essential Javascript autocomplete control. 
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,   
api: /api/js/ejautocomplete
---

# How to

## How to set autocomplete default value

You can set a value into autocomplete at initial rendering using [`value`](https://help.syncfusion.com/api/js/ejautocomplete#members:value) property.  It is used to select a single value from the autocomplete widget at initial rendering state. 

Refer to the following code.

{% highlight html %}

<input type="text" id="selectState" />
           
<script type="text/javascript" class="jsScript">
        $(function () {
            var states = [
                 { index: "s1", countryName: "Alabama" }, 
                 { index: "s2", countryName: "Alaska" },
                 { index: "s3", countryName: "Arizona" } 
            ];

            $('#selectState').ejAutocomplete({
                dataSource: states,
                fields: { key: "index", text: "countryName" },
    	        value: "Arizona"
            });
         });
</script>

{% endhighlight %}

The following output is displayed as a result of the previous code example.

![howto](how-to_images/howto1.png)

If you set autocomplete [`value`](https://help.syncfusion.com/api/js/ejautocomplete#members:value) property as a string that is present in the data source, the hidden input value holds the corresponding [`key`](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) value.  This is used for validation purpose in the autocomplete.  For example, ‘Arizona’ text holds the key value of `s3`.  The autocomplete default value `Arizona` is present in the `countryName` of data source and also this field is mapped for autocomplete [`text`](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) property. So, hidden input value holds the `s3` value.

The following screenshot illustrates the previous hidden input state of code.

![howto](how-to_images/howto2.png)

If you set autocomplete [`value`](https://help.syncfusion.com/api/js/ejautocomplete#members:value) property as a string that is not present in the data source, the hidden input value holds the autocomplete value.  For example, if autocomplete default value is `New York` and not present in the `countryName` of data source, the hidden input value holds the `New York` string. 

Refer to the following code sample.

{% highlight html %}

<input type="text" id="selectState" />
           
<script type="text/javascript" class="jsScript">
        $(function () {
            var states = [
                 { index: "s1", countryName: "Alabama" }, 
                 { index: "s2", countryName: "Alaska" },
                 { index: "s3", countryName: "Arizona" } 
            ];

            $('#selectState').ejAutocomplete({
                dataSource: states,
                fields: { key: "index", text: "countryName" },
	            value: "New York"
            });
         });
</script>

{% endhighlight %}

The following screenshot illustrates the previous hidden input state of code.

![howto](how-to_images/howto3.png)

### Remote data

The remote data also allows you to set the default value into autocomplete using [`value`](https://help.syncfusion.com/api/js/ejautocomplete#members:value) property. 

Refer to the following code sample.

{% tabs %}

{% highlight html %}

<input type="text" id="selectCar" />

<script type="text/javascript" class="jsScript">
        $(function () {
            var dataManger = ej.DataManager({
                url: "/Autocomplete/GetOutletsForAutocomplete", crossDomain: true, adaptor: new ej.UrlAdaptor() });
            $('#selectCar').ejAutocomplete({
                dataSource: dataManger,
                fields: { key: "Id", text: "Name" },
    	        value: "Two"
            });
        });
</script>

{% endhighlight  %}

{% highlight c# %}

public ActionResult GetOutletsForAutocomplete(DataManager value)
        {
            var models = GetTestData();

            IEnumerable Data = GetTestData();
            Syncfusion.JavaScript.DataSources.DataOperations operation = new Syncfusion.JavaScript.DataSources.DataOperations();
            if (value.Where != null && value.Where.Count > 0) //Filtering 
            {
                data = operation.PerformWhereFilter(models, value.Where, value.Where[0].Operator);
            }
            return Json(data, JsonRequestBehavior.AllowGet);
        }

  public class AutocompleteModel
    {
        [Display(Name = "Id")]
        public string Id { get; set; }
        [Display(Name = "Name")]
        public string Name { get; set; }
    }

     private List<AutocompleteModel> GetTestData()
        {
            var list = new List<AutocompleteModel>();
            list.Add(new AutocompleteModel(){ Id = "1", Name = "One"});
            list.Add(new AutocompleteModel(){ Id = "2", Name = "Two"});
            list.Add(new AutocompleteModel(){ Id = "3", Name = "Three"});
            return list;
        }

{% endhighlight  %}

{% endtabs %}

The autocomplete [`value`](https://help.syncfusion.com/api/js/ejautocomplete#members:value) property triggers a server-side post when using remote data in the autocomplete.  The server side data manger holds `where` query which contains field `name` as autocomplete [`text`](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) property.

Find the following screenshot for the data manager where query.

![howto](how-to_images/howto6.png)

Find the following output for the previous code.

![howto](how-to_images/howto7.png)

## How to show text on autocomplete using key value

You can set the value of autocomplete text box based on a given key value.  The [`selectValueByKey`](https://help.syncfusion.com/api/js/ejautocomplete#members:selectvaluebykey) property is used to select autocomplete value based on the specified key value. 

Refer to the following code sample. 

{% highlight html %}

<input type="text" id="selectState" />
           
<script type="text/javascript" class="jsScript">
        $(function () {
            var states = [
                 { index: "s1", countryName: "Alabama" }, 
                 { index: "s2", countryName: "Alaska" },
                 { index: "s3", countryName: "Arizona" } 
            ];

            $('#selectState').ejAutocomplete({
                dataSource: states,
                fields: { key: "index", text: "countryName" },
	            selectValueByKey: "s2"
            });
         });
</script>

{% endhighlight %}

For example, If [`selectValueByKey`](https://help.syncfusion.com/api/js/ejautocomplete#members:selectvaluebykey) property specified the value as `s2`, the corresponding [`text`](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) value `Alaska` is shown in the autocomplete text.

The following output is displayed as a result of the previous code example.

![howto](how-to_images/howto4.png)

If you are specifying the [`selectValueByKey`](https://help.syncfusion.com/api/js/ejautocomplete#members:selectvaluebykey) property into autocomplete control, the hidden input value holds a specified key value. 

Refer to the following screenshot. 

![howto](how-to_images/howto5.png)

### Remote data

The remote data also allows you to set the default value into autocomplete based on a given key value using the [`selectValueByKey`](https://help.syncfusion.com/api/js/ejautocomplete#members:selectvaluebykey) property.

Refer to the following code snippet.

{% tabs %}

{% highlight html %}

<input type="text" id="selectCar" />

<script type="text/javascript" class="jsScript">
        $(function () {
            var dataManger = ej.DataManager({
                url: "/Autocomplete/GetOutletsForAutocomplete", crossDomain: true, adaptor: new ej.UrlAdaptor() });
            $('#selectCar').ejAutocomplete({
                dataSource: dataManger,
                fields: { key: "Id", text: "Name" },
	            selectValueByKey: "2"
            });
        });
        
    </script>

{% endhighlight  %}

{% highlight c# %}

      public ActionResult GetOutletsForAutocomplete(DataManager value)
        {
            var models = GetTestData();

            IEnumerable Data = GetTestData();
            Syncfusion.JavaScript.DataSources.DataOperations operation = new Syncfusion.JavaScript.DataSources.DataOperations();

            var data = operation.Execute(models, value);
            if (value.Where != null && value.Where.Count > 0) //Filtering 
            {
                data = operation.PerformWhereFilter(models, value.Where, value.Where[0].Operator);
            }
            return Json(data, JsonRequestBehavior.AllowGet);
        }

public class AutocompleteModel
    {
        [Display(Name = "Id")]
        public string Id { get; set; }
        [Display(Name = "Name")]
        public string Name { get; set; }
    }

   private List<AutocompleteModel> GetTestData()
        {
            var list = new List<AutocompleteModel>();
            list.Add(new AutocompleteModel(){ Id = "1", Name = "One"});
            list.Add(new AutocompleteModel(){ Id = "2", Name = "Two"});
            list.Add(new AutocompleteModel(){ Id = "3", Name = "Three"});
            return list;
        }

{% endhighlight  %}

{% endtabs %}

The autocomplete [`selectValueByKey`](https://help.syncfusion.com/api/js/ejautocomplete#members:selectvaluebykey) property triggers a server-side post when using remote data on autocomplete.  The server side data manger holds `where` query which contains field `name` as autocomplete [`key`](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) property.

Find the following screenshot for the data manager where query.

![howto](how-to_images/howto8.png)

Find the output for the previously given code as follows.

![howto](how-to_images/howto9.png)

## How to enable Autofill with filter type  `contains` in Autocomplete

By default, the Autofill property works with filter type `StartsWith`. However,Autofill behavior can be achieved with `contains` filter type using the open event of Autocomplete. 

Refer to the following code.

{% highlight html %}

     <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <div class="control">
                        <input type="text" id="selectCar" />
                    </div>
                </div>
            </div>
        </div>
    </div>
    <script type="text/javascript" class="jsScript">
        $(function () {
            // declaration
            var carList = [
                "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                "BMW 7","Chevrolet Camaro", "Cadillac",
                "Duesenberg J", "Dodge Sprinter",
                "Elantra", "Excavator",
                "Ford Boss 302", "Ferrari 360", "Ford Thunderbird",
                "GAZ Siber",
                "Honda S2000", "Hyundai Santro",
                "Isuzu Swift", "Infiniti Skyline",
                "Jaguar XJS",
                "Kia Sedona EX", "Koenigsegg Agera",
                "Lotus Esprit", "Lamborghini Diablo",
                "Mercedes-Benz", "Mercury Coupe", "Maruti Alto 800",
                "Nissan Qashqai",
                "Oldsmobile S98", "Opel Superboss",
                "Porsche 356", "Pontiac Sunbird",
                "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
                "Triumph Spitfire", "Toyota 2000GT",
                "Volvo P1800", "Volkswagen Shirako"
            ];

             $('#selectCar').ejAutocomplete({
                width: "100%",
                watermarkText: "Select a car",
                dataSource: carList, 
                enableAutoFill : true, 
                filterType: "contains", 
                open: Open
            });
          
           function Open(args){
              	$('#selectCar').ejAutocomplete("option", "value", this.suggestionListItems[0])
              }
        });   
    </script>

{% endhighlight  %}

Refer to the sample [here](https://jsplayground.syncfusion.com/ys01ehax)