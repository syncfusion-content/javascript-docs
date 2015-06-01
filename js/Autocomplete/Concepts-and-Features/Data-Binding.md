---
layout: post
title: Data-Binding
description: data-binding
platform: js
control: AutoComplete
documentation: ug
---

# Data-Binding

In order to render the **AutoComplete** control, the data needs to be bound to it in a proper way. The following sub-properties provide a way to bind either the local or remote data to the **AutoComplete** widget by binding the appropriate data fields to the corresponding options.

## Fields

### dataSource 

This property assigns the local **json** data or remote data that is the **url** binding to the **AutoComplete** control.

### query 

It accepts the data of object type usually the query string to fetch the required data from a specific table based on certain condition. This property is optional hence when it is not specified the entire records that are initially assigned through **dataSource** are taken into consideration.

### key

It maps the corresponding **key** field name from the data table or **json** data that is assigned to the **dataSource** with the **key** property of the **AutoComplete** control. The **key** value that is fetched from the table is unique for each records.

### text

It maps the corresponding **text** field name from the data table or **json** data that is assigned to the **dataSource** with the **text** property of the **AutoComplete** control. The text value that is fetched from the table gets the value to be displayed in the **AutoComplete** textbox.

### category

It maps the **category** field name from the data table or **json** data that is assigned to the **dataSource**. The **category** value that is fetched from the table is made available when **Grouping** is enabled.

### htmlAttributes

This allows you to map the **CSS** styles or classes to the corresponding data from table or **json** data with the **AutoComplete** items. The **htmlAttributes** value customizes the **AutoComplete** items based on **html** styling or class assigned to it. 

## Local data

**AutoComplete** provides extensive data binding support to populate **AutoComplete** items, so that the values are mapped to the **AutoComplete** fields, namely **key** and **text**. **DataBinding** helps you bind a key value pair to **AutoComplete** textbox. **Key** field takes the unique **id** of the **dataSource** elements. **Text** field gets the value to be displayed in the **AutoComplete** textbox.

### Defining the Local data for AutoComplete

The following steps explain local data binding to an **AutoComplete** textbox.

1. In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.

{% highlight html %}

**[HTML]**
         **<input type="text" id="autocomplete" />**

**[JavaScript]**
**\\** Define local dataSource elements using the **key** and **text** fields.
var states = [
 { index: "s1", countryName: "Alabama" }, { index: "s2", countryName: "Alaska" },
 { index: "s3", countryName: "Arizona" }, { index: "s4", countryName: "Arkansas" },
 { index: "s5", countryName: "California" },{index: "s6",countryName: "Colorado" },
 { index: "s7", countryName: "Connecticut" },{index: "s8",countryName: "Delaware" },
 { index: "s9", countryName: "Florida" }, { index: "s10", countryName: "Georgia" },
 { index: "s11", countryName: "Hawaii" }, { index: "s12", countryName: "Idaho" },
 { index: "s13", countryName: "Illinois" },{ index: "s14",countryName: "Indiana" },
 { index: "s15", countryName: "Iowa" }, { index: "s16", countryName: "Kansas" },
 { index: "s17", countryName: "Kentucky" },{index: "s18", countryName:"Louisiana" },
 { index: "s19", countryName: "Maine" }, { index: "s20", countryName: "Maryland" },
 { index: "s21", countryName: "Massachusetts" }, { index: "s22", countryName: "Michigan" },
 { index: "s23", countryName: "Montana" }, {index: "s24",countryName:"New Mexico" },
 { index: "25", countryName: "New York" }, { index: "26", countryName: "North Carolina" },
 { index: "s27", countryName: "Nevada" }, {index: "s28",countryName: "New Jersey" }                 
];

**[JavaScript]**
\\ Map local dataSource to corresponding fields in AutoComplete.

    $('#autocomplete').ejAutocomplete({
**dataSource: states,**
                fields: { key: "index", text: "countryName" },
                width: 205
            });


{% endhighlight %}





The following image is the output for **AutoComplete** control with local data binding.

{% include image.html url="/js/Autocomplete/Concepts-and-Features/Data-Binding_images/Data-Binding_img1.png" Caption="AutoComplete with local data-binding"%}

## Remote data

**AutoComplete** provides remote data binding support to populate **AutoComplete** items, so that the values are mapped to the **AutoComplete** fields from a remote web service using **DataManager** and **Query**. 

**DataManager** is used to manage relational data in **JavaScript**. It supports **CRUD** that is Create, Read, Update, and Destroy, in individual requests and batches. **DataManager** uses two different classes, **ej.DataManager,** for processing and **ej.Query,** for serving data. **ej.DataManager** communicates with **dataSource** and **ej.Query** generates data queries that are read by the **DataManager**.

### Configuring remote data for AutoComplete

The following steps explain the remote data binding to an **AutoComplete** textbox.

1. In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.

{% highlight html %}

**[HTML]**
         <input type="text" id="autocomplete" />


{% endhighlight %}



2. Define **DataManager** and assign remote data source to it. Initialize query for binding data to **AutoComplete** text. Here **DataManager** gets the remote web service and filters the data using **Query**. The **select** property of **ejQuery** is used to retrieve the specified columns from the dataSource.

{% highlight js %}

**[JavaScript]**
var dataManger = **ej.DataManager**({
            // Web service host
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // Query creation
var query = **ej.Query().**from("Suppliers").select("SupplierID", "ContactName");



{% endhighlight %}

****

3. Assign **dataSource** and **Query** property values to bind the remote data. Map the corresponding fields for **text** and **key** value in **AutoComplete** control as follows.

{% highlight js %}

**[JavaScript]**
    $('#autocomplete').ejAutocomplete({
**dataSource: dataManger,**
                **query: query,**
                **fields: { text: "ContactName", key: "SupplierID" },**
                filterType: ej.filterType.StartsWith,
                width: 205
            });



{% endhighlight %}



The following image is the output for **AutoComplete** control with remote data binding.

{% include image.html url="/js/Autocomplete/Concepts-and-Features/Data-Binding_images/Data-Binding_img2.png" Caption="AutoComplete with remote data binding"%}

