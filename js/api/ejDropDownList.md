---
layout: post
title: ejDropDownList
documentation: API
platform: js
metaname: 
metacontent: 
---

The DropDownList control provides a list of options to help the user choose an item from the list. It is capable of including other HTML elements such as images, textboxes, check box, radio buttons, and so on.





$(element).ejDropDownList<span class="signature">()</span>






Example
{:.example}


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
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList"});    
</script>{% endhighlight %}
{% highlight html %}
// Another way to render DropDownList control.
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
// Create DropDownList
$('#drpdwn').ejDropDownList();  
</script> {% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:jQuery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.draggable.js

* module:ej.dropdownlist.js

* module:ej.checkbox.js

* module:ej.scroller.js


## Members


### cascadeTo<span class="type-signature type string">string</span>
{:#members:cascadeto}




The cascading DropDownLists is a series of two or more DropDownLists in which each DropDownList is filtered according to the previous DropDownList’s value.


Default Value:
{:.param}



* null




Example
{:.example}


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
</script>
{% endhighlight %}


### caseSensitiveSearch<span class="type-signature type boolean">boolean</span>
{:#members:casesensitivesearch}




Sets the case sensitivity of the search operation. It supports with both enableFilterSearch and enableIncrementalSearch property.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><div id="carsList"><ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div><script>
        // Initializes the DropDownList with the caseSensitiveSearch specified.
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList", 
           enableFilterSearch : true, 
           caseSensitiveSearch: true 
        });

</script>
{% endhighlight %}



### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Dropdown widgets style and appearance can be controlled based on 13 different default built-in themes.  
You can customize the appearance of the dropdown by using the cssClass property. You need to specify a class name in the cssClass property and the same class name should be used before class definitions wherever you apply the custom styles.



Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<head>

    <link href="http://cdn.syncfusion.com/13.3.0.7/js/web/flat-saffron/ej.web.all.min.css" rel="stylesheet" /> 

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




### dataSource<span class="type-signature type data">data</span>
{:#members:datasource}




This property is used to serve data from the data services based on the query provided. To bind data to dropdown widget, the dataSource property should be assigned with the instance of ej.DataManager.


Default Value:
{:.param}



* null




Example
{:.example}


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




### delimiterChar<span class="type-signature type string">string</span>
{:#members:delimiterchar}




Sets the separator when multiSelectMode with delimiter option or checkbox is enabled with the dropdown. If you enter the delimiter value, the texts after the delimiter are considered a separate word or query. The delimiter string should have a single character and must be a symbol. Mostly the delimiter symbol is used as comma (,) or semi-colon (;) or any other special character.


Default Value:
{:.param}



* ','




Example
{:.example}


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


### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}



The enabled Animation property uses the easeOutQuad animation to SlideDown and SlideUp the Popup list in 200 and 100 milliseconds, respectively.  


Default Value:
{:.param}



* false




Example
{:.example}


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




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}



This property is used to indicate whether the DropDownList control responds to the user interaction or not. By default, the control is in the enabled mode, and you can disable it by setting it to false. 


Default Value:
{:.param}



* true




Example
{:.example}


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




### enableIncrementalSearch<span class="type-signature type boolean">boolean</span>
{:#members:enableincrementalsearch}




Specifies to perform incremental search for selection of items from DropDownList can be done with the help of this property, this will helpful in selecting the item using the typed character.


Default Value:
{:.param}



* true




Example
{:.example}


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
 </div>enableFilterSearch <script>          
// Initialize the enableIncrementalSearch with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",enableIncrementalSearch: true });
</script>{% endhighlight %}

### enableFilterSearch <span class="type-signature type boolean">boolean</span>
{:#members:enableincrementalsearch}




This property selects the item in the DropDownList when the item is entered in the Search text box.


Default Value:
{:.param}



* false




Example
{:.example}


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



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Saves current model value to browser cookies for state maintenance. While refreshing the DropDownList control page, retains the model value, and it is applied from the browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}


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

### enablePopupResize <span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




This enables the resize handler to resize the popup to any size. 


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
   <select name="selectIndex" id="drpdwn"><option value="Art">Art</option><option value="Architecture">Architecture</option>
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            enablePopupResize: true 
        });
    </script>
{% endhighlight %}



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Sets the DropDownList textbox direction from right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><div id="carsList"><ul>
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
        </ul>
    </div><script>
        // Initializes the DropDownList with the enableRTL value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            enableRTL: true 
        });

    </script>
{% endhighlight %}


### enableSorting <span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




This property is used to sort the Items in the DropDownList. By default, it will sort the items in an ascending order.


Default Value:
{:.param}



* false




Example
{:.example}


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
    </div><script>
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "list", 
            text: "Computer IT", 
            enableSorting : true, 
            sortOrder : "ascending"  
        });
        
    </script>

{% endhighlight %}


### fields<span class="type-signature type object">object</span>
{:#members:fields}



Specifies mapping fields for the data items of the DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>
        window.countries = [
           { text: "Algeria", flag: "flag-dz" }, 
           { text: "Argentina", flag: "flag-ar" },
           { text: "Armenia", flag: "flag-am" }, 
           { text: "Brazil", flag: "flag-br" },
           { text: "Bangladesh", flag: "flag-bd" }
        ];
        //Sets fields API value during initialization.  
        $("#drpdwn").ejDropDownList(
        { 
             dataSource: window.countries, 
             fields: { text: "text", value: "flag" } 
        }); 

    </script>
{% endhighlight %}




### fields.groupBy<span class="type-signature type string">String</span>
{:#members:fields-groupBy}




Used to group the items. 






### fields.htmlAttributes<span class="type-signature type object">Object</span>
{:#members:fields-htmlattributes}




Defines the HTML attributes such as ID, class, and styles for the item.






### fields.id<span class="type-signature type string">String</span>
{:#members:fields-id}




Defines the ID for the tag.





### fields.imageAttributes<span class="type-signature type string">String</span>
{:#members:fields-imageattributes}



Defines the image attributes such as height, width, styles, and so on.






### fields.imageUrl<span class="type-signature type string">String</span>
{:#members:fields-imageurl}




Defines the imageURL for the image location.






### fields.selected<span class="type-signature type boolean">Boolean</span>
{:#members:fields-selected}




Defines the tag value to be selected initially.






### fields.spriteCssClass<span class="type-signature type string">String</span>
{:#members:fields-spritecssclass}




Defines the sprite css for the image tag.






### fields.tableName<span class="type-signature type string">String</span>
{:#members:fields-tablename}




Defines the table name for tag value or display text while rendering remote data.






### fields.text<span class="type-signature type string">String</span>
{:#members:fields-text}




Defines the text content for the tag.






### fields.value<span class="type-signature type string">String</span>
{:#members:fields-value}




Defines the tag value.

### filterType  <span class="type-signature type enum">Enum</span>
{:#members:filterType}




When the enableFilterSearch property value is set to true, the values in the DropDownList shows the items starting with or containing the key word/letter typed in the Search text box.


Default Value:
{:.param}



* false




Example
{:.example}


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
             filterType: ej.FilterType.Contains 
         });
        
    </script>


{% endhighlight %}

Example
{:.example}


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




### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}




Defines the height of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


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
        //Initializes the DropDownList height property with the value specified.
        $("#drpdwn").ejDropDownList(
        { 
            targetID: "carsList", 
            height: 100 
        });
      </script>
{% endhighlight %}


### htmlAttributes <span class="type-signature type object">Object</span> 
{:#members:htmlAttributes}



It sets the given HTML attributes for the DropDownList control such as ID, name, disabled, etc.


Default Value:
{:.param}



* null




Example
{:.example}


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


### itemsCount<span class="type-signature type number">number</span>
{:#members:itemscount}



Data can be fetched in the DropDownList control by using the DataSource, specifying the number of items.


Default Value:
{:.param}



* 5




Example
{:.example}


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


### maxPopupHeight <span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:maxPopupHeight}




Defines the maximum height of the suggestion box. This property restricts the maximum height of popup when resize is enabled. 


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>
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


### minPopupHeight  <span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:minPopupHeight }




Defines the minimum height of the suggestion box. This property restricts the minimum height of popup when resize is enabled. 


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>

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

### maxPopupWidth   <span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:maxPopupWidth }




Defines the maximum width of the suggestion box. This property restricts the maximum width of popup when resize is enabled. 


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>

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

### minPopupWidth  <span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:minPopupWidth }




Defines the minimum height of the suggestion box. This property restricts the minimum height of popup when resize is enabled. 


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>

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

### multiSelectMode   <span class="type-signature type enum">Enum</span> 
{:#members:minPopupWidth }



With the help of this property, you can make a single or multi selection with the DropDownList and display the text in two modes, delimiter and visual mode. In delimiter mode, you can separate the items by using delimiter character such as comma (,) or semi-colon (;) or any other special character. In the visual mode, the items are showcased like boxes with close icon in textbox. 


Default Value:
{:.param}



*  ej.MultiSelectMode.None




Example
{:.example}


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
        $("#drpdwn").ejDropDownList(
        { 
             targetID: "carsList",  
             multiSelectMode: ej.MultiSelectMode.Delimiter 
        });
    </script>



{% endhighlight %}

Example
{:.example}


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
        $("#drpdwn").ejDropDownList(
        { 
           targetID: "carsList",  
           multiSelectMode: ej.MultiSelectMode.VisualMode 
         });

    </script>



{% endhighlight %}

### popupHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupheight}




Defines the height of the suggestion popup box in the DropDownList control.


Default Value:
{:.param}



* "152px"




Example
{:.example}


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




### popupWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupwidth}




Defines the width of the suggestion popup box in the DropDownList control.


Default Value:
{:.param}



* "auto"




Example
{:.example}


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




### query<span class="type-signature type object">object</span>
{:#members:query}




Specifies the query to retrieve the data from the DataSource.


Default Value:
{:.param}



* null




Example
{:.example}


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




### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Specifies that the DropDownList textbox values should be read-only.


Default Value:
{:.param}



* false




Example
{:.example}


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




### selectedIndex <span class="type-signature type number">number</span>
{:#members:selectedIndex }




Specifies an item to be selected in the DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


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




### selectedIndices <span class="type-signature type integerarray">integerarray</span>
{:#members:selecteditems}




Specifies the selectedItems for DropDownList.


Default Value:
{:.param}



* []




Example
{:.example}


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




### showCheckbox<span class="type-signature type boolean">boolean</span>
{:#members:showcheckbox}




Selects multiple items in the DropDownList with the help of the checkbox control. For this, enable it by setting the showCheckbox option to true.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showPopupOnLoad<span class="type-signature type boolean">boolean</span>
{:#members:showpopuponload}




DropDownList control to be displayed with the popup seen.


Default Value:
{:.param}



* false




Example
{:.example}


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




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




DropDownList textbox to be displayed with the rounded corner style.


Default Value:
{:.param}



* false




Example
{:.example}


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




### targetID<span class="type-signature type string">string</span>
{:#members:targetid}



Specifies the targetID for the DropDownList’s items.


Default Value:
{:.param}



* null




Example
{:.example}


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
        // Initializes the DropDownList with the targetID value specified.
        $("#drpdwn").ejDropDownList(
        { 
          targetID: "carsList"
        });

    </script>
{% endhighlight %}




### template<span class="type-signature type string">string</span>
{:#members:template}



By default, you can add any text or image to the DropDownList item. To customize items layout or to create your own visualized elements, you can use this template support.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
        
// To set template API value during initialization  .   
<input type="text" id="drpdwn" /><script>
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
        });</script><style type="text/css">
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




### text<span class="type-signature type string">string</span>
{:#members:text}



Defines the text value to be displayed in the DropDownList textbox.


Default Value:
{:.param}



* null




Example
{:.example}


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



### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}

Sets the jQuery validation error message in the DropDownList


Default Value:
{:.param}



* null




Example
{:.example}


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




### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}




Set the jquery validation rules in Dropdownlist.


Default Value:
{:.param}



* null




Example
{:.example}


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




### value<span class="type-signature type string">string</span>
{:#members:value}



Specifies the value (text content) for the DropDownList control.


Default Value:
{:.param}



* Null




Example
{:.example}


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




### watermarkText<span class="type-signature type string">string</span>
{:#members:watermarktext}




Specifies a short hint that describes the expected value of the DropDownList control.


Default Value:
{:.param}



* Null




Example
{:.example}


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




### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


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


### virtualScrollMode <span class="type-signature type string">String</span> 
{:#members:width}



The Virtual Scrolling feature is used to display large amount of records in the DropDownList, that is, when scrolling, an Ajax request is sent to fetch some amount of data from the server dynamically. To achieve this scenario with DropDownList, set the allowVirtualScrolling to true. You can set the itemsCount property that represents number of items to be fetched from the server on every Ajax request. 

This property enables the data to load dynamically in two ways. 

In normal mode, the data is loaded only to the corresponding page (display items). When scrolling some other position, it enables the load on demand with DropDownList. 


Default Value:
{:.param}



* "normal"




Example
{:.example}


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

In continuous mode, the data items are loaded from the remote when scroll handle reaches the end of the scrollbar like infinity scrolling. 

Example
{:.example}


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




### addItem<span class="signature">()</span>
{:#methods:additem}




Adding a single item or an array of items into the DropDownList allows you to specify all the fields attributes such as value, template, image URL, and html attributes for those items. 



Example
{:.example}


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

        // Creates DropDownList
        $('#drpdwn').ejDropDownList(
        { 
             dataSource: window.countries, 
             field: { text: "text"}, 
             value: "Algeria" 
        });

        $('#drpdwn').ejDropDownList("addItem", { text :"India"});

    </script>
{% endhighlight %}


Example
{:.example}


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

        // Creates DropDownList
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

### checkAll<span class="signature">()</span>
{:#methods:checkall}



This method is used to select all the items in the DropDownList.



Example
{:.example}


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




### clearText<span class="signature">()</span>
{:#methods:cleartext}




Clears the text in the DropDownList textbox.



Example
{:.example}


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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5" 
        });

        $('#drpdwn').ejDropDownList("clearText");

    </script>
{% endhighlight %}




### destroy<span class="signature">()</span>
{:#methods:destroy}




Destroys the DropDownList widget.



Example
{:.example}


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
        // Creates DropDownList.

        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             value: "Audi A5" 
        });

        $('#drpdwn').ejDropDownList("destroy");

    </script>
{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}



This property is used to disable the DropDownList widget.



Example
{:.example}


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
        // Creates DropDownList

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




### disableItemsByIndices<span class="signature">()</span>
{:#methods:disableItemsByIndices}



This property disables the set of items in the DropDownList.



Example
{:.example}


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
        // Creates DropDownList.

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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList",
            multiSelectMode: "delimiter" 
        });

        $('#drpdwn').ejDropDownList("disableItemsByIndices", "3,5,7");

    </script>
{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




This property enables the DropDownList control.



Example
{:.example}


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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             value: "Audi A5", 
             enable: false 
        });

        $('#drpdwn').ejDropDownList("enable");

    </script>
{% endhighlight %}




### enableItemsByIndices<span class="signature">()</span>
{:#methods:enableItemsByIndices}




To enable an Item or set of Items which are in disable in the DropDownList



Example
{:.example}


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
        // Creates DropDownList.

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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
             targetID: "carsList", 
             multiSelectMode: "delimiter"
             
        });

        $('#drpdwn').ejDropDownList("disableItemsByIndices", "3,5,7");
        $('#drpdwn').ejDropDownList("enableItemsByIndices", "3,7");

    </script>
{% endhighlight %}


### getListData<span class="signature">()</span>
{:#methods:getListData}




This method is used to retrieve the items which has bound with the DropDownList.



Example
{:.example}


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
        // Creates DropDownList.

        $('#drpdwn').ejDropDownList({ text: "Comics"});

        var items = $('#drpdwn').ejDropDownList("getListData");
        for (var i=0;i< items.length; i++)
		       console.log("item" + i + " is " + items[i].text);
    </script>
{% endhighlight %}



### getSelectedItem<span class="signature">()</span>
{:#methods:getselecteditem}




This method is used to get the selected items in DropDownList.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><div id="carsList"><ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul></div><script>
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
      // Create DropDownList
      $('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
      $('#drpdwn').ejDropDownList("getSelectedItem");         
</script>
{% endhighlight %}



### getSelectedValue<span class="signature">()</span>
{:#methods:getselectedvalue}




This method is used to retrieve the items value that are selected in the DropDownList.



Example
{:.example}


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
        // Creates DropDownList.

        $('#drpdwn').ejDropDownList({ text: "Comics"});

        alert($('#drpdwn').ejDropDownList("getSelectedValue"));

    </script>
{% endhighlight %}



### hidePopup<span class="signature">()</span>
{:#methods:hidepopup}




This method hides the suggestion popup in the DropDownList.



Example
{:.example}


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

        // Creates DropDownList
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList", 
            value: "Audi A5",
            showPopupOnLoad :true 
        });

        $('#drpdwn').ejDropDownList("hidePopup");

    </script>
{% endhighlight %}




### selectItemsByIndices<span class="signature">()</span>
{:#methods:selectItemsByIndices}




This method is used to select the list of items in the DropDownList through the Index of the items.



Example
{:.example}


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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true });
        $('#drpdwn').ejDropDownList("selectItemsByIndices", "2,3");

    </script>
{% endhighlight %}


### selectItemByText<span class="signature">()</span>
{:#methods:selectItemByText}



This method is used to select an item in the DropDownList by the given text value.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true});
        $('#drpdwn').ejDropDownList("selectItemByText", "Computer IT ,Comics ");
    </script>  
{% endhighlight %}


### selectItemByValue<span class="signature">()</span>
{:#methods:selectItemByValue}




This method is used to select an item in the DropDownList by the given value.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList({showCheckbox : true});
        $('#drpdwn').ejDropDownList("selectItemByValue", "ComputerIT, Cookery ");
    </script>
{% endhighlight %}




### showPopup<span class="signature">()</span>
{:#methods:showpopup}




This method shows the DropDownList control with the suggestion popup.



Example
{:.example}


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

        DropDownListObj.showPopup(); // hidePopup of the DropDownList.

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

        $('#drpdwn').ejDropDownList("showPopup");

    </script>
{% endhighlight %}




### unCheckAll<span class="signature">()</span>
{:#methods:uncheckall}




This method is used to unselect all the items in the DropDownList.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        { 
            targetID: "carsList",
            selectedIndex:[1]
        });

        $('#drpdwn').ejDropDownList("uncheckAll");
    </script>
{% endhighlight %}




### unselectItemsByIndices<span class="signature">()</span>
{:#methods:unselectItemsByIndices}




This method is used to unselect the list of items in the DropDownList through Index of the items.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemsByIndices", "2,3");
    </script>
{% endhighlight %}




### unselectItemByText<span class="signature">()</span>
{:#methods:unselectitembytext}




This method is used to unselect an item in the DropDownList by the given text value.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemByText", "Computer IT, Cookery ");
    </script>
{% endhighlight %}




### unselectItemByValue<span class="signature">()</span>
{:#methods:unselectitembyvalue}




This method is used to unselect an item in the DropDownList by the given value.



Example
{:.example}


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
        // Creates DropDownList.
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
        // Creates DropDownList.
        $('#drpdwn').ejDropDownList(
        {
            checkAll: true, 
            showCheckbox:true
        });
        $('#drpdwn').ejDropDownList("unselectItemByValue", "ComputerIT, Cookery ");
    </script>
{% endhighlight %}




## Events


### actionComplete
{:#events:actionComplete}




Fires the action when the list of items is bound to the DropDownList by xhr post calling 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.count{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns number of times trying to fetch the data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.query{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.request{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query for data retrieval from the Database </td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.result{% endhighlight %}</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the number of items fetched from remote data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.xhr{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the requested data</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            actionComplete: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}


 ### actionFailure
{:#events:actionFailure}




Fires the action when xhr post calling failed on remote data binding with the DropDownList control.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.error{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error message</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.query{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            actionFailure: function (args) 
            {
                /*Do your changes */               
            }
        });

    </script>

 {% endhighlight %}

### actionSuccess
{:#events:actionSuccess}



Fires the action when xhr post calling succeed on remote data binding with the DropDownList control 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.count{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns number of times trying to fetch the data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.query{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query for data retrieval </td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.request{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the query for data retrieval from the Database </td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.result{% endhighlight %}</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the number of items fetched from remote data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.xhr{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the requested data</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            beforePopupHide: function (args) 
            {
               /*Do your changes */            
            }
        });

    </script>
 {% endhighlight %}




### beforePopupShown
{:#events:beforepopupshown}



Fires the action before the popup is ready to be shown.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            beforePopupShown: function (args) 
            {
                      /*Do your changes */                        
            }
        });

    </script>
   {% endhighlight %}


### cascade
{:#events:cascade}


Fires when cascading happen between two DropDownList exactly after value change in first dropdown and before filtering happen in second Dropdown.   

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cascadeModel{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cascading dropdown model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cascadeValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current selected value in first dropdown.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.requiresDefaultFilter{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the default filter action for second dropdown data should happen or not.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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

        // To set cascadeTo API value during initialization 
        $('#groupsList').ejDropDownList({
            dataSource: groups,
            fields: { value: "parentId", text: "text" },
            cascadeTo: 'countryList',
            cascade: function (args) {/*Do your changes */ }
        });

  {% endhighlight %}

### change
{:#events:change}



Fires the action when the DropDownList control’s value has been changed. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.itemId{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.selectedText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected value.</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            change: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
  {% endhighlight %}




### checkChange
{:#events:checkChange}



Fires the action when the list item checkbox value has been changed. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.itemId{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.selectedText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected value.</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            create: function (args) 
            {
               /*Do your changes */                        
            }
        });

    </script>
 {% endhighlight %}


### dataBound
{:#events:dataBound}



Fires the action when the list items is bound to the DropDownList. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the data that is bound to DropDownList</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
{:#events:popupResize}




Fires the action, when the popup is resizing. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /><script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" })

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
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



Fires the action, once popup is opened.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
{:#events:popupResizeStart}


Fires the action, when resizing a popup starts. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
            enablePopupResize:true, 
            popupResizeStart: function (args) 
            {
                /*Do your changes */
            }
        });

    </script>

{% endhighlight %}

### popupResizeStop
{:#events:popupResizeStop}




Fires the action, when popup resizing is stopped. 

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data from the resizable plugin.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" />
    <script>

        var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" });

        var query = ej.Query().select("ShipName", "ShipCountry");

        // Creates DropDownList.
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



Fires the action before filtering of the list items starts in the DropDownList when the enableFilterSearch is enabled.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.items{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data bound to the DropDownList.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.selectedText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.searchString{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the search string typed in search box.</td>
</tr>
</tbody>
</table>


Example
{:.example}


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




Fires the action, when the list item is selected.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the selected item with checkbox checked or not.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.itemId{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item ID.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.selectedText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected item text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected text.</td>
</tr>
<tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the selected value.</td>
</tr>
<tr>
</tbody>
</table>


Example
{:.example}


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
            showCheckbox: true, 
            select: function (args) 
            {              
               /*Do your changes */                        
            }
        });

    </script>
{% endhighlight %}



