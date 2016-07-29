---
layout: post
title: Properties, Methods and Events of ejDropDownList Widget
description: API reference for ejDropDownList
documentation: API
platform: js
keywords: DropDownList, ejDropDownList, syncfusion, DropDownList api
---

# ejDropDownList


The DropDownList control provides a list of options to choose an item from the list. It can including other HTML elements such as images, textboxes, check box, radio buttons, and so on.



#### Syntax

{% highlight javascript %}

$(element).ejDropDownList()

{% endhighlight %}



#### Example



{% highlight html %}
 
<input type="text" id="drpdwn" />  
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div><script>
// Creates the DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList"});    
</script>{% endhighlight %}
{% highlight html %}
// Another way to render the DropDownList control.
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">ComputerIT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select><script>
// Creates the DropDownList
$('#drpdwn').ejDropDownList();  
</script> 
{% endhighlight %}




#### Requires


* module:jQuery

* module:jQuery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.draggable.js

* module:ej.dropdownlist.js

* module:ej.checkbox.js

* module:ej.scroller.js


## Members

### allowVirtualScrolling `boolean`
{:#members:allowvirtualscrolling}

The Virtual Scrolling(lazy loading) feature is used to display a large amount of data that you require without buffering the entire load of a huge database records in the DropDownList, that is, when scrolling, an AJAX request is sent to fetch some amount of data from the server dynamically. To achieve this scenario with DropDownList, set the allowVirtualScrolling to true.

####  Default Value

* false

#### Example

{% highlight html %}

    <input type="text" id="CompanyNames" />
    var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Customers" });
    $('#CompanyNames').ejDropDownList({
        "dataSource": dm,
        "fields": { text: "CompanyName", value: 'ContactName' },
        "width": 260,
        "itemsCount": 10,
        "allowVirtualScrolling": true
    });
    
{% endhighlight %}

### cascadeTo `string`
{:#members:cascadeto}

The cascading DropDownLists is a series of two or more DropDownLists in which each DropDownList is filtered according to the previous DropDownList’s value.

#### Default Value

*  null

####  Example

{% highlight html %}
    
    <span>Select Group</span><input id="groupsList" type="text"/>
    <span>Select Country</span><input id="countryList" type="text"/><script>
        var groups = [
            { parentId: 'a', text: "Group A" },
            { parentId: 'b', text: "Group B" },
            { parentId: 'c', text: "Group C" },
            { parentId: 'd', text: "Group D" },
            { parentId: 'e', text: "Group E" }
        ];
       
        var countries = [
           { value: 11, parentId: 'a', text: "Algeria"},
           { value: 12, parentId: 'a', text: "Armenia"},
           { value: 13, parentId: 'a', text: "Bangladesh"},
           { value: 14, parentId: 'a', text: "Cuba"},
           { value: 15, parentId: 'b', text: "Denmark"},
           { value: 16, parentId: 'b', text: "Egypt"},
           { value: 17, parentId: 'c', text: "Finland"},
           { value: 18, parentId: 'c', text: "India"},
           { value: 19, parentId: 'c', text: "Malaysia"},
           { value: 20, parentId: 'd', text: "New Zealand"},
           { value: 21, parentId: 'd', text: "Norway"},
           { value: 22, parentId: 'd', text: "Poland"},
           { value: 23, parentId: 'e', text: "Romania"},
           { value: 24, parentId: 'e', text: "Singapore"},
           { value: 25, parentId: 'e', text: "Thailand"},
           { value: 26, parentId: 'e', text: "Ukraine"}
        ];
        //Sets the cascadeTo API value during initialization. 
        $('#groupsList').ejDropDownList(
        {
            dataSource: groups,
            fields: { value: "parentId", text: "text" },
            cascadeTo: 'countryList'
        });
        $('#countryList').ejDropDownList({
            dataSource: countries,
            fields: { value: "value", text: "text" },
            enabled: false
        });
   
{% endhighlight %}

### caseSensitiveSearch `boolean`

{:#members:casesensitivesearch}

Sets the case sensitivity of the search operation. It supports both enableFilterSearch and enableIncrementalSearch property.

####  Default Value

*  false

####  Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /><div id="carsList">
    <ul>
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
    </ul>
    </div>
    <script>
        // Initializes the DropDownList with the caseSensitiveSearch specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           enableFilterSearch : true, 
           caseSensitiveSearch: true 
        });

    </script>
    
{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Dropdown widget's style and appearance can be controlled based on 13 different default built-in themes.  
You can customize the appearance of the dropdown by using the cssClass property. You need to specify a class name in the cssClass property and the same class name is used before the class definitions wherever the custom styles are applied.

#### Default Value

* ""

#### Example

{% highlight html %}
 
    <head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css" rel="stylesheet" /> 
    </head>
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>

        //Initializes the DropDownList with the cssClass value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            cssClass: "flat-saffron"
        });

    </script>
    
{% endhighlight %}

### dataSource `object`
{:#members:datasource}

This property is used to serve data from the data services based on the query provided. To bind the data to the dropdown widget, the dataSource property is assigned with the instance of the ej.DataManager.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <script>
        // DataManager creation.
        var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Customers");

        $('#drpdwn').ejDropDownList(
        {
            dataSource: dataManager,
            fields: { text: "CustomerID" }
        }); 
    </script>
    
{% endhighlight %}

### delimiterChar `string`
{:#members:delimiterchar}

Sets the separator when the multiSelectMode with delimiter option or checkbox is enabled with the dropdown. When you enter the delimiter value, the texts after the delimiter are considered as a separate word or query. The delimiter string is a single character and must be a symbol. Mostly, the delimiter symbol is used as comma (,) or semi-colon (;) or any other special character.

#### Default Value

* ','

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <script>
       window.countries = [
           { text: "Algeria"}, 
           { text: "Argentina"},
           { text: "Armenia"}, 
           { text: "Brazil"},
           { text: "Bangladesh"}
        ];

        //Sets the delimiterChar value during initialization.

        $("#drpdwn").ejDropDownList(
        { 
           delimiterChar: ";", 
           dataSource: window.countries, 
           multiSelectMode: "delimiter" 
        });
    </script>
    
{% endhighlight %}


### enableAnimation `boolean`
{:#members:enableanimation}

The enabled Animation property uses the easeOutQuad animation to SlideDown and SlideUp the Popup list in 200 and 100 milliseconds, respectively.  

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Initializes the enableAnimation with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList", 
             enableAnimation: true 
        });

    </script>
{% endhighlight %}

### enabled `boolean`
{:#members:enabled}

This property is used to indicate whether the DropDownList control responds to the user interaction or not. By default, the control is in the enabled mode and you can disable it by setting it to false. 

#### Default Value

* true

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Initializes the DropDownList with the enabled value specified.
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList", 
             enabled: false 
        });

    </script>
{% endhighlight %}

### enableIncrementalSearch `boolean`
{:#members:enableincrementalsearch}

Specifies to perform incremental search for the selection of items from the DropDownList with the help of this property. This helps in selecting the item by using the typed character.

#### Default Value

* true

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /> 
    enableFilterSearch 
    <div id="carsList">
    <ul>
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
    </ul>
    </div>enableFilterSearch 
    <script>          
        // Initializes the enableIncrementalSearch with the value specified.
        $("#drpdwn").ejDropDownList({targetID: "carsList",enableIncrementalSearch: true });
    </script>
    
{% endhighlight %}

### enableFilterSearch  `boolean`
{:#members:enablefiltersearch}

This property selects the item in the DropDownList when the item is entered in the Search textbox.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Initializes the enableFilterSearch with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList", 
             enableFilterSearch: true 
         });

    </script>
    
{% endhighlight %}

### enablePersistence `boolean`
{:#members:enablepersistence}

Saves the current model value to the browser cookies for state maintenance. While refreshing the DropDownList control page, it retains the model value and it is applied from the browser cookies.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>

        // Initializes the DropDownList with the enablePersistence value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            enablePersistence: true 
        });

    </script>
{% endhighlight %}

### enablePopupResize  `boolean`
{:#members:enablepopupresize}

This enables the resize handler to resize the popup to any size. 

#### Default Value

* false

#### Example

{% highlight html %}

    <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select>
    <script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            enablePopupResize: true 
        });
    </script>
    
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Sets the DropDownList textbox direction from right to left align.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Initializes the DropDownList with the enableRTL value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            enableRTL: true 
        });

    </script>
    
{% endhighlight %}

### enableSorting  `boolean`
{:#members:enableSorting}

This property is used to sort the Items in the DropDownList. By default, it sorts the items in an ascending order.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input id="drpdwn" type="text" /><div id="list">
      <ul>
            <li id="Art">Art</li>
            <li id="Architecture">Architecture</li>
            <li id="Biographies">Biographies</li>
            <li id="ComputerIT">Computer IT</li>
            <li id="Comics">Comics</li>
            <li id="Cookery">Cookery</li>
            <li id="Fiction">Fiction</li>
            <li id="Health">Health</li>
            <li id="Humanities">Humanities</li>
            <li id="Environment">Environment</li>
            <li id="Language">Language</li>
            <li id="Business">Business</li>
      </ul>
    </div>
    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "list", 
            text: "Computer IT", 
            enableSorting : true, 
            sortOrder : "ascending"  
        });
        
    </script>

{% endhighlight %}

### fields `object`
{:#members:fields}

Specifies the mapping fields for the data items of the DropDownList.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /><script>
        window.countries = [
           { text: "Algeria", flag: "flag-dz" }, 
           { text: "Argentina", flag: "flag-ar" },
           { text: "Armenia", flag: "flag-am" }, 
           { text: "Brazil", flag: "flag-br" },
           { text: "Bangladesh", flag: "flag-bd" }
        ];
        //Sets fields with API value during initialization.  
        $("#drpdwn").ejDropDownList(
        { 
             dataSource: window.countries, 
             fields: { text: "text", value: "flag" } 
        }); 

    </script>
    
{% endhighlight %}

### fields.groupBy `string`
{:#members:fields-groupby}

Used to group the items. 

### fields.htmlAttributes `object`
{:#members:fields-htmlattributes}

Defines the HTML attributes such as ID, class, and styles for the item.

### fields.id `string`
{:#members:fields-id}

Defines the ID for the tag.

### fields.imageAttributes `string`
{:#members:fields-imageattributes}

Defines the image attributes such as height, width, styles, and so on.

### fields.imageUrl `string`
{:#members:fields-imageurl}

Defines the imageURL for the image location.

### fields.selected `boolean`
{:#members:fields-selected}

Defines the tag value to be selected initially.

### fields.spriteCssClass `string`
{:#members:fields-spritecssclass}

Defines the sprite CSS for the image tag.

### fields.tableName `string`
{:#members:fields-tablename}

Defines the table name for tag value or display text while rendering remote data.

### fields.text `string`
{:#members:fields-text}

Defines the text content for the tag.

### fields.value `string`
{:#members:fields-value}

Defines the tag value.

### filterType   `enum`
{:#members:filterType}

<ts name="ej.FilterType"/>

When the enableFilterSearch property value is set to true, the values in the DropDownList shows the items starting with or containing the key word/letter typed in the Search textbox.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
contains</td>

<td class="description last">filter the data wherever contains search key </td>
</tr>
<tr>
<td class="name">
startsWith</td>

<td class="description last">filter the data based on search key present at start position</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.FilterType.Contains

#### Example

{% highlight html %}
 
    <input id="drpdwn" type="text" /><div id="list">
      <ul>
        <li id="Art">Art</li>
        <li id="Architecture">Architecture</li>
        <li id="Biographies">Biographies</li>
        <li id="Business">Business</li>
        <li id="ComputerIT">Computer IT</li>
        <li id="Comics">Comics</li>
        <li id="Cookery">Cookery</li>
        <li id="Environment">Environment</li>
        <li id="Fiction">Fiction</li>
        <li id="Health">Health</li>
        <li id="Humanities">Humanities</li>
        <li id="Language">Language</li>
      </ul>
    </div><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "list", 
             text: "Computer IT", 
             enableFilterSearch : true, 
             filterType: ej.FilterType.Contains 
         });
        
    </script>


{% endhighlight %}

#### Example

{% highlight html %}
 
    <input id="drpdwn" type="text" /><div id="list">
      <ul>
        <li id="Art">Art</li>
        <li id="Architecture">Architecture</li>
        <li id="Biographies">Biographies</li>
        <li id="Business">Business</li>
        <li id="ComputerIT">Computer IT</li>
        <li id="Comics">Comics</li>
        <li id="Cookery">Cookery</li>
        <li id="Environment">Environment</li>
        <li id="Fiction">Fiction</li>
        <li id="Health">Health</li>
        <li id="Humanities">Humanities</li>
        <li id="Language">Language</li>
      </ul>
    </div><script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "list", 
             text: "Computer IT", 
             enableFilterSearch : true, 
             filterType: ej.FilterType.StartsWith
        });        
    </script>
    
{% endhighlight %}

### headerTemplate `string`
{:#members:headertemplate}

Used to create visualized header for dropdown items

#### Default Value

* null

#### Example

{% highlight html %}
   
    // Sets the headerTemplate API value during initialization  .   
    <input type="text" id="drpdwn" />
    <script>
        window.countries = [
             { text: "Argentina", flag: "flag-ar" },
             { text: "Armenia", flag: "flag-am" }, 
             { text: "Brazil", flag: "flag-br" },
             { text: "Bangladesh", flag: "flag-bd" },
             { text: "Canada", flag: "flag-ca" }
        ];
        $("#drpdwn").ejDropDownList( 
        {
            dataSource: window.countries, 
            template: '<div class="flag ${flag}"> </div>' + '<div class="txt"> ${text} </div>', width: "200px"
            headerTemplate: "<div class='header'><span class='flag-head'>Flag</span> <span class='con-head'>Countries</span> </div>"
        });
    </script>
    <style type="text/css">
        /* Sprite css for country flags and get the images from JS samples location */
        .flag {
            background: url("images/autocomplete/flags.png") no-repeat;
            float: left;
            height: 15px;
            margin-right: 10px;
            margin-top: 3px;
            width: 25px;
        }
        .header {
            text-align:center;
            font-weight:600;
            height:30px;
            vertical-align:middle;	
            border-bottom:1px solid #c8c8c8;
        }
        .flag-head{
            float: left;
            margin-left: 12px;
            margin-top: 5px;
        }
        .con-head{
            float: right;
            margin-right: 89px;
            margin-top: 5px;
        }
        .flag.flag-am {background-position: -25px 0;}
        .flag.flag-ar {background-position: -50px 0;}
        .flag.flag-bd {background-position: -75px 0;}
        .flag.flag-br {background-position: -100px 0;}
        .flag.flag-ca {background-position: -125px 0;}
    </style>
    
{% endhighlight %}

### height `string|number`
{:#members:height}

Defines the height of the DropDownList textbox.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /><div id="carsList">
    <ul>
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
    </ul>
    </div>
    <script>
        //Initializes the DropDownList height property with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            height: 100 
        });
    </script>
    
{% endhighlight %}

### htmlAttributes  `object` 
{:#members:htmlattributes}

It sets the given HTML attributes for the DropDownList control such as ID, name, disabled, etc.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        //Initializes the DropDownList height property with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList", 
             htmlAttributes : { disabled: "disabled"}
        }); 

    </script>

{% endhighlight %}


### itemsCount `number`
{:#members:itemscount}

Data can be fetched in the DropDownList control by using the DataSource, specifying the number of items.

#### Default Value

* 5

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>

        window.countries = [
             { text: "Argentina", flag: "flag-ar" },
             { text: "Armenia", flag: "flag-am" }, 
             { text: "Brazil", flag: "flag-br" },
             { text: "Bangladesh", flag: "flag-bd" },
             { text: "Canada", flag: "flag-ca" }
        ];

        $("#drpdwn").ejDropDownList( 
        {
            dataSource: window.countries, 
            itemsCount : 2
        });

    </script>
{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the particular country or region language for the DropDownList.

#### Default Value

* "en-US"

#### Example

{% highlight html %}

    <input type="text" id="selectcompany" />

    $(function () {
        var datalist = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Customers" });
        $('#selectcompany').ejDropDownList({
            dataSource: datalist,
            fields: { text: "CompanyName", value: 'ContactName' },
            width: 260,
            showCheckbox: true,
            locale: "de-DE",
            enableFilterSearch: true,
            enablePopupResize: true

        });
    });
    
{% endhighlight %}

### maxPopupHeight  `string|number`
{:#members:maxpopupheight}

Defines the maximum height of the suggestion box. This property restricts the maximum height of the popup when resize is enabled. 

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>
        var dm = ej.DataManager({ url:   "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
           dataSource: dm, 
           query: query, 
           fields: { text: "ShipName", groupBy: "ShipCountry" }, 
           itemsCount : 20,
           maxPopupHeight: "200px", 
           enablePopupResize: true 
        });

    </script>
    
{% endhighlight %}

### minPopupHeight   `string|number`
{:#members:minpopupheight }

Defines the minimum height of the suggestion box. This property restricts the minimum height of the popup when resize is enabled. 

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
           dataSource: dm, 
           query: query, 
           fields: { text: "ShipName", groupBy: "ShipCountry" },  
           itemsCount : 20,  
           minPopupHeight: "150px", 
           enablePopupResize: true 
        });

    </script>

{% endhighlight %}

### maxPopupWidth    `string|number`
{:#members:maxpopupwidth }

Defines the maximum width of the suggestion box. This property restricts the maximum width of the popup when resize is enabled. 

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", groupBy: "ShipCountry" },  
            itemsCount : 20,                                        
            maxPopupWidth: "200px", 
            enablePopupResize: true 
        }); 

    </script>


{% endhighlight %}

### minPopupWidth   `string|number`
{:#members:minpopupwidth }

Defines the minimum height of the suggestion box. This property restricts the minimum height of the popup when resize is enabled. 

#### Default Value

* 0

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", groupBy: "ShipCountry" },
            itemsCount : 20,
            minPopupWidth: "150px", 
            enablePopupResize: true 
        });

    </script>


{% endhighlight %}

### multiSelectMode `enum` 
{:#members:multiselectmode }

<ts name="ej.MultiSelectMode"/>

With the help of this property, you can make a single or multi selection with the DropDownList and display the text in two modes, delimiter and visual mode. In delimiter mode, you can separate the items by using the delimiter character such as comma (,) or semi-colon (;) or any other special character. In the visual mode, the items are showcased like boxes with close icon in the textbox. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
none</td>

<td class="description last"> can select only single item in DropDownList </td>
</tr>
<tr>
<td class="name">
delimiter</td>

<td class="description last">can select multiple items and it's separated by delimiterChar</td>
</tr>
<tr>
<td class="name">
visualMode</td>

<td class="description last"> can select multiple items and it's show's like visual box in textbox</td>
</tr>
</tbody>
</table>


#### Default Value

*  ej.MultiSelectMode.None

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Creates the DropDownList.        
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList",  
             multiSelectMode: ej.MultiSelectMode.Delimiter 
        });
    </script>

{% endhighlight %}

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList",  
           multiSelectMode: ej.MultiSelectMode.VisualMode 
         });

    </script>

{% endhighlight %}

### popupHeight `string|number`
{:#members:popupheight}

Defines the height of the suggestion popup box in the DropDownList control.

#### Default Value

* "152px"

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", groupBy: "ShipCountry" },   
            itemsCount : 20,
            popupHeight: "190px" 
        });

    </script>
    
{% endhighlight %}

### popupWidth `string|number`
{:#members:popupwidth}

Defines the width of the suggestion popup box in the DropDownList control.

#### Default Value

* "auto"

#### Example

{% highlight html %}
 
   <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        //Initializes the DropDownList popupWidth property with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           popupWidth: 200 
        });

    </script>
    
{% endhighlight %}

### query `object`
{:#members:query}

Specifies the query to retrieve the data from the DataSource.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
           dataSource: dm, 
           query: query, 
           fields: { text: "ShipName", groupBy: "ShipCountry" },    
           itemsCount: 20
         });

    </script>
    
{% endhighlight %}

### readOnly `boolean`
{:#members:readonly}

Specifies that the DropDownList textbox values should be read-only.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Initializes the DropDownList with the readOnly value specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           text : "Audi A5",
           readOnly: true 
        });

    </script>
    
{% endhighlight %}

### selectedIndex  `number`
{:#members:selectedindex }

Specifies an item to be selected in the DropDownList.


#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Sets the selectedItems API value during initialization.    
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList",            
            selectedIndex: 1
        });

    </script>
    
{% endhighlight %}

### selectedIndices  `array`
{:#members:selectedindices}

Specifies the selectedItems for the DropDownList.

#### Default Value

* []

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Sets the selectedItems API value during initialization.    
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            showCheckbox: true, 
            selectedIndices: [1, 2] 
        });

    </script>
{% endhighlight %}

### showCheckbox `boolean`
{:#members:showcheckbox}

Selects multiple items in the DropDownList with the help of the checkbox control. To achieve this, enable the showCheckbox option to true.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Initializes the DropDownList with the showCheckbox value specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           showCheckbox: true 
        });

    </script>
    
{% endhighlight %}

### showPopupOnLoad `boolean`
{:#members:showpopuponload}

DropDownList control is displayed with the popup seen.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
        </ul>
    </div>

    <script>
        // Initializes the DropDownList with the showPopupOnLoad value specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           showPopupOnLoad: true 
        });

    </script>
    
{% endhighlight %}

### showRoundedCorner `boolean`
{:#members:showroundedcorner}

DropDownList textbox displayed with the rounded corner style.

#### Default Value

* false

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Initializes the DropDownList with the showRoundedCorner value specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           showRoundedCorner: true 
        });

    </script>
    
{% endhighlight %}

### sortOrder  `enum`
{:#members:sortorder}

<ts name="ej.SortOrder"/>

When the enableSorting property value is set to true, this property helps to sort the items either in ascending or descending order

<table class="params">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
ascending</td>

<td class="description last"> Sort the data in ascending order</td>
</tr>
<tr>
<td class="name">
descending</td>

<td class="description last">Sort the data in descending order</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.sortOrder.Ascending

#### Example

{% highlight html %}
 
    <input id="drpdwn" type="text" /><div id="list">
      <ul>
        <li id="Art">Art</li>
        <li id="Architecture">Architecture</li>
        <li id="Biographies">Biographies</li>
        <li id="ComputerIT">Computer IT</li>
        <li id="Comics">Comics</li>
        <li id="Cookery">Cookery</li>
        <li id="Fiction">Fiction</li>
        <li id="Health">Health</li>
        <li id="Humanities">Humanities</li>
        <li id="Environment">Environment</li>
        <li id="Language">Language</li>
        <li id="Business">Business</li>
      </ul>
    </div>
    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "list", 
            text: "Computer IT", 
            enableSorting : true, 
            sortOrder : ej.sortOrder.Descending  
        });
        
    </script>

{% endhighlight %}

### targetID `string`
{:#members:targetid}

Specifies the targetID for the DropDownList’s items.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /><div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Initializes the DropDownList with the targetID value specified.
        $("#drpdwn").ejDropDownList(
        { 
          targetID: "carsList"
        });

    </script>
    
{% endhighlight %}

### template `string`
{:#members:template}

By default, you can add any text or image to the DropDownList item. To customize the item layout or to create your own visualized elements, you can use this template support.

#### Default Value

* null

#### Example

{% highlight html %}
      
    // Sets the template API value during initialization  .   
    <input type="text" id="drpdwn" />
    <script>
        window.countries = [
             { text: "Argentina", flag: "flag-ar" },
             { text: "Armenia", flag: "flag-am" }, 
             { text: "Brazil", flag: "flag-br" },
             { text: "Bangladesh", flag: "flag-bd" },
             { text: "Canada", flag: "flag-ca" }
        ];
        $("#drpdwn").ejDropDownList( 
        {
            dataSource: window.countries, 
            template: '<div class="flag ${flag}"> </div>' + '<div class="txt"> ${text} </div>', width: "200px"
        });
    </script>
    <style type="text/css">
        /* Sprite css for country flags and get the images from JS samples location */
        .flag {
            background: url("images/autocomplete/flags.png") no-repeat;
            float: left;
            height: 15px;
            margin-right: 10px;
            margin-top: 3px;
            width: 25px;
        }
        .flag.flag-am {background-position: -25px 0;}
        .flag.flag-ar {background-position: -50px 0;}
        .flag.flag-bd {background-position: -75px 0;}
        .flag.flag-br {background-position: -100px 0;}
        .flag.flag-ca {background-position: -125px 0;}
    </style>
    
{% endhighlight %}

### text `string`
{:#members:text}

Defines the text value that is displayed in the DropDownList textbox.

#### Default Value

* null

#### Example

{% highlight html %}
 
  <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Initializes the DropDownList with the text specified.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  targetID: "carsList",
                                  text : "Audi A7"

                              }).data("ejDropDownList");

        console.log("Selected Item's Text - " + DropDownListObj.option("text"));
 
    </script>
{% endhighlight %}

### validationMessage `object`
{:#members:validationmessage}

Sets the jQuery validation error message in the DropDownList


#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" name="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.

        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", groupBy: "ShipCountry" }, 
            itemsCount: 20,
            validationRules: {
                required: true
            },
            validationMessage: {
                required: "Required Dropdown value"
            }
        });

    </script>
    
{% endhighlight %}

### validationRules `object`
{:#members:validationrules}

Sets the jQuery validation rules in the Dropdownlist.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" name="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");
        // Creates DropDownList.

        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", groupBy: "ShipCountry" }, 
            itemsCount: 20,
            validationRules: {
                required: true
            },
            validationMessage: {
                required: "Required Dropdown value"
            }
        });
    </script>
{% endhighlight %}

### value `string`
{:#members:value}

Specifies the value (text content) for the DropDownList control.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        //Initializes the DropDownList value property with the value specified.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  targetID: "carsList",
                                  value: "Audi A7"

                              }).data("ejDropDownList");

        console.log("Selected Item's Value - " + DropDownListObj.option("value")); 

    </script>
{% endhighlight %}

### watermarkText `string`
{:#members:watermarktext}

Specifies a short hint that describes the expected value of the DropDownList control.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
       //Initializes the DropDownList with the watermarkText value specified.
        $("#drpdwn").ejDropDownList(
       { 
           targetID: "carsList", 
           watermarkText: 'Enter text' 
       });

    </script>
{% endhighlight %}

### width `string|number`
{:#members:width}

Defines the width of the DropDownList textbox.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
      //Initializes the DropDownList width property with the width value specified.
        $("#drpdwn").ejDropDownList(
        {
           targetID: "carsList",
           width: 250 
        });

    </script>
{% endhighlight %}

### virtualScrollMode  `enum` 
{:#members:virtualscrollmode}

<ts name="ej.VirtualScrollMode" />

The Virtual Scrolling feature is used to display a large amount of records in the DropDownList, that is, when scrolling, an AJAX request is sent to fetch some amount of data from the server dynamically. To achieve this scenario with DropDownList, set the allowVirtualScrolling to true. You can set the itemsCount property that represents the number of items to be fetched from the server on every AJAX request. 

This property enables the data to load dynamically in two ways. 


<table class="params">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
normal</td>

<td class="description last"> The data is loaded only to the corresponding page (display items). When scrolling some other position, it enables the load on demand with the DropDownList.</td>
</tr>
<tr>
<td class="name">
continuous</td>

<td class="description last">The data items are loaded from the remote when scroll handle reaches the end of the scrollbar like infinity scrolling.</td>
</tr>
</tbody>
</table>

#### Default Value

* "normal"

#### Example - Normal mode

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            allowVirtualScrolling: true 
        });

    </script>

{% endhighlight %}


#### Example - Continuous mode

{% highlight html %}
 
    <input type="text" id="drpdwn" />
    <script>
        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            allowVirtualScrolling: true,
            virtualScrollMode: "continuous" 
        });
    </script>

{% endhighlight %}


## Methods

### addItem(data)
{:#methods:additem}

Adding a single item or an array of items into the DropDownList allows you to specify all the field attributes such as value, template, image URL, and HTML attributes for those items. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type">object|array</td>
<td class="description last"> this parameter should have field attributes with respect to mapped field attributes and it's corresponding values to fields</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <script>
        window.countries = [
            { text: "Algeria"}, 
            { text: "Argentina"},
            { text: "Armenia"}, 
            { text: "Brazil"},
            { text: "Bangladesh"}
        ];

        // Creates the DropDownList
        $('#drpdwn').ejDropDownList(
        { 
             dataSource: window.countries, 
             field: { text: "text"}, 
             value: "Algeria" 
        });

        $('#drpdwn').ejDropDownList("addItem", { text :"India"});

    </script>
{% endhighlight %}


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>
        window.countries = [
            { text: "Algeria"}, 
            { text: "Argentina"},
            { text: "Armenia"}, 
            { text: "Brazil"},
            { text: "Bangladesh"}
        ];

        // Creates the DropDownList
        var dropdownobj = $('#drpdwn').ejDropDownList(
        { 
           dataSource: window.countries, 
           field: { text: "text"}, 
           value: "Algeria" 
        }).data("ejDropDownList");

        //New Country Array. 
       window.newCountries = [
			{ text: "India"},
			{ text: "Pakistan"},
			];
        
       dropdownobj.addItem(newCountries );

    </script>


{% endhighlight %}

### checkAll()
{:#methods:checkall}

This method is used to select all the items in the DropDownList.

#### Example

{% highlight html %}
 

<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>

        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5", 
            showCheckbox: true 
        }).data("ejDropDownList");

        DropDownListObj.checkAll(); // checkAll values the DropDownList.

    </script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5", 
            showCheckbox: true 
        }); 

        $('#drpdwn').ejDropDownList("checkAll");

    </script>
{% endhighlight %}

### clearText()
{:#methods:cleartext}

Clears the text in the DropDownList textbox.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                             { 
                                targetID: "carsList", 
                                value: "Audi A5" 
                             }).data("ejDropDownList");

        DropDownListObj.clearText(); //Clears the DropDownList text.

    </script>
{% endhighlight %}

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5" 
        });

        $('#drpdwn').ejDropDownList("clearText");

    </script>
{% endhighlight %}

### destroy()
{:#methods:destroy}

Destroys the DropDownList widget.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              { 
                                  targetID: "carsList", 
                                  value: "Audi A5"                   
                               }).data("ejDropDownList");

        DropDownListObj.destroy(); //Hides the DropDownList text.

    </script>
{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.

        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             value: "Audi A5" 
        });

        $('#drpdwn').ejDropDownList("destroy");

    </script>
{% endhighlight %}

### disable()
{:#methods:disable}

This property is used to disable the DropDownList widget.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList

        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              { 
                                  targetID: "carsList", 
                                  value: "Audi A5"                                     
                              }).data("ejDropDownList");

        DropDownListObj.disable(); //Hides the DropDownList text.

    </script>
{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5" 
        });

        $('#drpdwn').ejDropDownList("disable");

    </script>
{% endhighlight %}

### disableItemsByIndices(index)
{:#methods:disableitembyindices}

This property disables the set of items in the DropDownList.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> disable the given index list items</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
    
<input type="text" id="drpdwn"/>

    <ul id="carsList">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
    </ul>

    <script>
        // Creates the DropDownList.

        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList",
            multiSelectMode: "delimiter"
        });

        var DropDownListObj = $("#drpdwn").data("ejDropDownList");

        DropDownListObj.disableItemsByIndices("3,5,7");

    </script>
  {% endhighlight %}


{% highlight html %}
 
  <input type="text" id="drpdwn" />

    <ul id="carsList">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
    </ul>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList",
            multiSelectMode: "delimiter" 
        });

        $('#drpdwn').ejDropDownList("disableItemsByIndices", "3,5,7");

    </script>
{% endhighlight %}

### enable()
{:#methods:enable}

This property enables the DropDownList control.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  targetID: "carsList", 
                                  value: "Audi A5",
                                  enable: false 
                              }).data("ejDropDownList");

        DropDownListObj.enable(); //Enables the DropDownList text.

    </script>
{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             value: "Audi A5", 
             enable: false 
        });

        $('#drpdwn').ejDropDownList("enable");

    </script>
{% endhighlight %}

### enableItemsByIndices(index)
{:#methods:enableitembyindices}

Enables an Item or set of Items that are disabled in the DropDownList

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> enable the given index list items if it's disabled</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
   <input type="text" id="drpdwn"/>

    <ul id="carsList">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
    </ul>

    <script>
        // Creates the DropDownList.

        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            multiSelectMode: "delimiter"
         });

        var DropDownListObj = $("#drpdwn").data("ejDropDownList");

        DropDownListObj.disableItemsByIndices("3,5,7");

        DropDownListObj.enableItemsByIndices("3,7");

    </script>
{% endhighlight %}


{% highlight html %}
 
  <input type="text" id="drpdwn" />
    <ul id="carsList">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
    </ul>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             multiSelectMode: "delimiter"
             
        });

        $('#drpdwn').ejDropDownList("disableItemsByIndices", "3,5,7");
        $('#drpdwn').ejDropDownList("enableItemsByIndices", "3,7");

    </script>
{% endhighlight %}



### getItemDataByValue(value)
{:#methods:getItemDataByValue}

This method retrieves the items using given value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">value</td>
<td class="type">string|number|object</td>
<td class="description last"> Return the whole object of data based on given value</td>
</tr>

</tbody>
</table>

####Returns: object 

This method will return the whole object corresponds to given value from datasource 

#### Example

{% highlight html %}
 <input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20
        });
        var DropDownListObj = $("#drpdwn").data("ejDropDownList");
        console.log("Target CompanyName - "+ DropDownListObj.getItemDataByValue("Aria Cruz")[0].CompanyName);

    </script>


{% endhighlight %}

{% highlight html %}
 <input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20
        });
        var data =  $('#drpdwn').ejDropDownList('getItemDataByValue',"Aria Cruz")
        console.log("Target CompanyName - "+ data[0].CompanyName);

    </script>


{% endhighlight %}

### getListData()
{:#methods:getlistdata}

This method is used to retrieve the items that are bound with the DropDownList.

####Returns: 

object 

This method will return the whole data which binds with Dropdownlist control 


#### Example

{% highlight html %}
 
<select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
</select>

    <script>

        // Creates the DropDownList.

        var DropDownListObj = $('#drpdwn').ejDropDownList(
                             { 
                                text: "Comics" 

                             }).data("ejDropDownList");

         var items = DropDownListObj.getListData();
         for (var i=0;i< items.length; i++)
		       console.log("item" + i + " is " + items[i].text);

    </script>
{% endhighlight %}

{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
   
 </select>

    <script>
        // Creates the DropDownList.

        $('#drpdwn').ejDropDownList({ text: "Comics"});

        var items = $('#drpdwn').ejDropDownList("getListData");
        for (var i=0;i< items.length; i++)
		       console.log("item" + i + " is " + items[i].text);
    </script>
{% endhighlight %}

### getSelectedItem()
{:#methods:getselecteditem}

This method is used to get the selected items in the DropDownList.

####Returns: Element 

This method will return the selected item elements 

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" /><div id="carsList"><ul>
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
    </ul></div>
    <script>
        // Create DropDownList
        $('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
        var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
        DropDownListObj.getSelectedItem(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <input type="text" id="drpdwn" /><div id="carsList"><ul>
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
    </ul>
    </div><script>
        // Creates the DropDownList
        $('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
        $('#drpdwn').ejDropDownList("getSelectedItem");         
    </script>

{% endhighlight %}

### getSelectedValue()
{:#methods:getselectedvalue}


This method is used to retrieve the items value that are selected in the DropDownList.

####Returns: string

This method will return the selected Item value and separated by delimiterChar in multi selection mode. 

#### Example

{% highlight html %}
  
<select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
</select>

    <script>

        // Creates the DropDownList.

        var DropDownListObj = $('#drpdwn').ejDropDownList(
                             { 
                                text: "Comics" 

                             }).data("ejDropDownList");

        alert(DropDownListObj.getSelectedValue());

    </script>
{% endhighlight %}

{% highlight html %}
 
   <select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
   
 </select>

    <script>
        // Creates the DropDownList.

        $('#drpdwn').ejDropDownList({ text: "Comics"});

        alert($('#drpdwn').ejDropDownList("getSelectedValue"));

    </script>
{% endhighlight %}

### hidePopup()
{:#methods:hidepopup}

This method hides the suggestion popup in the DropDownList.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>

        // Creates the DropDownList
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              { 
                                 targetID: "carsList", 
                                 value: "Audi A5" ,
                                 showPopupOnLoad :true        
                              }).data("ejDropDownList"); 

        DropDownListObj.hidePopup(); //Hides popup of the DropDownList. 

    </script>
{% endhighlight %}

{% highlight html %}
 
  <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5",
            showPopupOnLoad :true 
        });

        $('#drpdwn').ejDropDownList("hidePopup");

    </script>
{% endhighlight %}

### selectItemsByIndices(indices)
{:#methods:selectitembyindices}

This method is used to select the list of items in the DropDownList through the Index of the items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> select the given index list items</td>
</tr>

</tbody>
</table>


#### Example

{% highlight html %}
 
<select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
</select>

    <script>
        // Creates the DropDownList.
        var DropDownListObj =     
        $('#drpdwn').ejDropDownList({showCheckbox : true }).data("ejDropDownList");

        DropDownListObj.selectItemsByIndices("2,3"); //selectItembyIndex for the DropDownList text.

    </script>
{% endhighlight %}

{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">

        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>

    </select>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true });
        $('#drpdwn').ejDropDownList("selectItemsByIndices", "2,3");

    </script>
{% endhighlight %}

### selectItemByText(text)
{:#methods:selectitembytext}

This method is used to select an item in the DropDownList by using the given text value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> select the list items relates to given text</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %} 
 <select name="selectIndex" id="drpdwn"><option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option></select><script>
        // Creates the DropDownList.
        var DropDownListObj =  
         $('#drpdwn').ejDropDownList(
         {
              showCheckbox : true
         }).data("ejDropDownList");
        DropDownListObj.selectItemByText("Computer IT ,Comics ");
    </script>
{% endhighlight %}

{% highlight html %}
 <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true});
        $('#drpdwn').ejDropDownList("selectItemByText", "Computer IT ,Comics ");
    </script>  
{% endhighlight %}

### selectItemByValue(value)
{:#methods:selectitembyvalue}

This method is used to select an item in the DropDownList by using the given value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> select the list items relates to given values</td>
</tr>

</tbody>
</table>


#### Example

{% highlight html %}
 
 <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        var DropDownListObj = 
            $('#drpdwn').ejDropDownList(
            {
                showCheckbox : true
            }).data("ejDropDownList");
        DropDownListObj.selectItemByValue("ComputerIT, Cookery ");
    </script>
{% endhighlight %}

{% highlight html %}
 
<select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true});
        $('#drpdwn').ejDropDownList("selectItemByValue", "ComputerIT, Cookery ");
    </script>
{% endhighlight %}

### showPopup()
{:#methods:showpopup}

This method shows the DropDownList control with the suggestion popup.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                 targetID: "carsList", 
                                 value: "Audi A5"
                              }).data("ejDropDownList");

        DropDownListObj.showPopup(); // hides Popup of the DropDownList.

    </script>
{% endhighlight %}

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             value: "Audi A5"
        });

        $('#drpdwn').ejDropDownList("showPopup");

    </script>
{% endhighlight %}

### unCheckAll()
{:#methods:uncheckall}

This method is used to unselect all the items in the DropDownList.

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" /><div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div><script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              { 
                                  targetID: "carsList", 
                                  value: "Audi A5" ,  
                                  selectedIndex:[1]
                              }).data("ejDropDownList");

        DropDownListObj.uncheckAll();

    </script>
{% endhighlight %}

{% highlight html %}
 
  <input type="text" id="drpdwn" /><div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList",
            selectedIndex:[1]
        });

        $('#drpdwn').ejDropDownList("uncheckAll");
    </script>
{% endhighlight %}

### unselectItemsByIndices(indices)
{:#methods:unselectitembyindices}

This method is used to unselect the list of items in the DropDownList through Index of the items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> unselect the given index list items</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  checkAll: true,   
                                  showCheckbox:true
                              }).data("ejDropDownList");
        DropDownListObj.unselectItemsByIndices("2,3"); 
    </script>
{% endhighlight %}

{% highlight html %}
 
<select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemsByIndices", "2,3");
    </script>
{% endhighlight %}

### unselectItemByText(text)
{:#methods:unselectitembytext}

This method is used to unselect an item in the DropDownList by using the given text value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> unselect the list items relates to given text</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
 <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  checkAll: true, 
                                  showCheckbox :true
                              }).data("ejDropDownList");
        DropDownListObj.unselectItemByText("Computer IT, Cookery");
    </script>
{% endhighlight %}

{% highlight html %}
 
 <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemByText", "Computer IT, Cookery ");
    </script>
{% endhighlight %}

### unselectItemByValue(value)
{:#methods:unselectitembyvalue}

This method is used to unselect an item in the DropDownList by using the given value.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">index</td>
<td class="type">string|number|array</td>
<td class="description last"> unselect the list items relates to given values</td>
</tr>

</tbody>
</table>

#### Example

{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        var DropDownListObj = $('#drpdwn').ejDropDownList(
                              {
                                  checkAll: true, 
                                  showCheckbox :true
                              }).data("ejDropDownList");

        DropDownListObj.unselectItemByValue("ComputerIT, Cookery ");
    </script>
{% endhighlight %}

{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
        <option value="Art">Art</option>
        <option value="Architecture">Architecture</option>
        <option value="Biographies">Biographies</option>
        <option value="Business">Business</option>
        <option value="ComputerIT">Computer IT</option>
        <option value="Comics">Comics</option>
        <option value="Cookery">Cookery</option>
        <option value="Environment">Environment</option>
        <option value="Fiction">Fiction</option>
        <option value="Health">Health</option>
        <option value="Humanities">Humanities</option>
        <option value="Language">Language</option>
    </select><script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemByValue", "ComputerIT, Cookery ");
    </script>
{% endhighlight %}

## Events

### actionBegin 
{:#events:actionBegin}

Fires the action before the XHR request.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            actionBegin : function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}



### actionComplete
{:#events:actioncomplete}

Fires the action when the list of items is bound to the DropDownList by xhr post calling 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">count</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns number of times trying to fetch the data</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">request</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the query for data retrieval from the Database </td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">result</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns the number of items fetched from remote data</td>
</tr>
<tr>
<td class="name">xhr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the requested data</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            actionComplete: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}


### actionFailure
{:#events:actionfailure}

Fires the action when the xhr post calling failed on remote data binding with the DropDownList control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the error message</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            actionFailure: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}

### actionSuccess
{:#events:actionsuccess}

Fires the action when the xhr post calling succeed on remote data binding with the DropDownList control 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">count</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns number of times trying to fetch the data</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">request</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the query for data retrieval from the Database </td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">result</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns the number of items fetched from remote data</td>
</tr>
<tr>
<td class="name">xhr</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the requested data</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            actionSuccess: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>


 {% endhighlight %}


### beforePopupHide
{:#events:beforepopuphide}

Fires the action before the popup is ready to hide. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected text</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected value</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script> 

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            beforePopupHide: function (args) 
            {
               /*Do your changes */            
            }
        });

    </script>
    
 {% endhighlight %}

### beforePopupShown
{:#events:beforepopupshown}

Fires the action before the popup is ready to be displayed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected text</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected value</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            beforePopupShown: function (args) 
            {
                      /*Do your changes */                        
            }
        });

    </script>
{% endhighlight %}

### cascade
{:#events:cascade}

Fires when the cascading happens between two DropDownList exactly after the value changes in the first dropdown and before filtering in the second Dropdown.   

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">cascadeModel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the cascading dropdown model.</td>
</tr>
<tr>
<td class="name">cascadeValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current selected value in first dropdown.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">requiresDefaultFilter</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the default filter action for second dropdown data should happen or not.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<div style="float: left;">
        <span>Select Group</span>
        <input id="groupsList" type="text" />
    </div>

    <div style="float: right;">
        <span>Select Country</span>
        <input id="countryList" type="text" />
    </div>
    <script>
        var groups = [
            { parentId: 'a', text: "Group A" },
            { parentId: 'b', text: "Group B" },
            { parentId: 'c', text: "Group C" },
            { parentId: 'd', text: "Group D" },
            { parentId: 'e', text: "Group E" }
        ];

        var countries = [
            { value: 11, parentId: 'a', text: "Algeria", flag: "flag-dz" },
            { value: 12, parentId: 'a', text: "Armenia", flag: "flag-am" },
            { value: 13, parentId: 'a', text: "Bangladesh", flag: "flag-bd" },
            { value: 14, parentId: 'a', text: "Cuba", flag: "flag-cu" },
            { value: 15, parentId: 'b', text: "Denmark", flag: "flag-dk" },
            { value: 16, parentId: 'b', text: "Egypt", flag: "flag-eg" },
            { value: 17, parentId: 'c', text: "Finland", flag: "flag-fi" },
            { value: 18, parentId: 'c', text: "India", flag: "flag-in" },
            { value: 19, parentId: 'c', text: "Malaysia", flag: "flag-my" },
            { value: 20, parentId: 'd', text: "New Zealand", flag: "flag-nz" },
            { value: 21, parentId: 'd', text: "Norway", flag: "flag-no" },
            { value: 22, parentId: 'd', text: "Poland", flag: "flag-pl" },
            { value: 23, parentId: 'e', text: "Romania", flag: "flag-ro" },
            { value: 24, parentId: 'e', text: "Singapore", flag: "flag-sg" },
            { value: 25, parentId: 'e', text: "Thailand", flag: "flag-th" },
            { value: 26, parentId: 'e', text: "Ukraine", flag: "flag-ua" }
        ];

        // Sets the cascadeTo API value during initialization 
        $('#groupsList').ejDropDownList({
            dataSource: groups,
            fields: { value: "parentId", text: "text" },
            cascadeTo: 'countryList',
            cascade: function (args) {/*Do your changes */ }
        });

  {% endhighlight %}

### change
{:#events:change}

Fires the action when the DropDownList control’s value is changed. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">itemId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">selectedText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected text.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected value.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            change: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
    
{% endhighlight %}

### checkChange
{:#events:checkchange}

Fires the action when the list item checkbox value is changed. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">itemId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">selectedText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected text.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected value.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            showCheckbox: true, 
            checkChange: function (args) 
            {              
               /*Do your changes */                        
            }
        });

    </script>

  {% endhighlight %}

### create
{:#events:create}

Fires the action once the DropDownList is created.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            create: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
 {% endhighlight %}

### dataBound
{:#events:databound}

Fires the action when the list items is bound to the DropDownList. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the data that is bound to DropDownList</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            dataBound: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}

### destroy
{:#events:destroy}

Fires the action when the DropDownList is destroyed. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            destroy: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
{% endhighlight %}

### popupHide
{:#events:popuphide}

Fires the action, once the popup is closed

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected text</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected value</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>
    <script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            popupHide: function (args) 
            {
               /*Do your changes */                        
            }
        });
    </script>
{% endhighlight %}

### popupResize
{:#events:popupresize}

Fires the action, when the popup is resized. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" /><script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            enablePopupResize: true, 
            popupResize: function (args) 
            {
                /*Do your changes */
            }
        });

    </script>
{% endhighlight %}

### popupShown
{:#events:popupshown}

Fires the action, once the popup is opened.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected text</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected value</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            popupShown: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
{% endhighlight %}


### popupResizeStart
{:#events:popupresizestart}

Fires the action, when resizing a popup starts. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />

    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            enablePopupResize:true, 
            popupResizeStart: function (args) 
            {
                /*Do your changes */
            }
        });

    </script>

{% endhighlight %}

### popupResizeStop
{:#events:popupresizestop}

Fires the action, when the popup resizing is stopped. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" });

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            dataSource: dm, 
            query: query, 
            fields: { text: "ShipName", value: "ShipCountry" }, 
            itemsCount: 20, 
            enablePopupResize:true, 
            popupResizeStop: function (args) 
            {
                /*Do your changes */
            }
        });
    </script>

{% endhighlight %}

### search
{:#events:search}

Fires the action before filtering the list items that starts in the DropDownList when the enableFilterSearch is enabled.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">items</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the data bound to the DropDownList.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">selectedText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">searchString</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the search string typed in search box.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            enableFilterSearch : true, 
            search: function (args) 
            {              
               /*Do your changes */                        
            }
        });

    </script>

{% endhighlight %}

### select
{:#events:select}

Fires the action, when the list of item is selected.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">itemId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">selectedText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected text.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the selected value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <input type="text" id="drpdwn" />

    <div id="carsList">
        <ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div>

    <script>
        // Creates the DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            targetID: "carsList", 
            value: "Audi A5", 
            showCheckbox: true, 
            select: function (args) 
            {              
               /*Do your changes */                        
            }
        });

    </script>
{% endhighlight %}



