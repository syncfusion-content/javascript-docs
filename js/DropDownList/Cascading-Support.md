---
layout: post
title: Cascading-Support
description: cascading support 
platform: js
control: DropDownList
documentation: ug
---

# Cascading Support 

Using **cascade** option, you can create a behaviour of cascade between dropdown list controls. For this, you need to create database with single field as common between two dropdown data fields and then mention that column id in field. With this, you need to set second dropdown id in **cascadeTo** property in first one. 

N>  In case the second dropdown is to disabled, until the first one is selected, you need to set enable property as false in second dropdown, which enables automatically once the value is selected in first one. 

The following steps explains you the behaviour of cascade dropdown. 

In an HTML page, add a **&lt;input&gt;** element to configure DropdownList widget

{% highlight html %}

<div class="control" style="float: left;">
    <span class="txt">Select Group</span>
    <input id="dropdownlist" type="text" />
</div>

<div class="control" style="float: left;">
    <span class="txt">Select Country</span>
    <input id="dropdownlist1" type="text" />
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript
    $(function () {
        // declaration
        var groups = [
      { Id: 'a', text: "Group A" },
      { Id: 'b', text: "Group B" },
      { Id: 'c', text: "Group C" },
      { Id: 'd', text: "Group D" },
      { Id: 'e', text: "Group E" }]
        //first level child
        var countries = [{ value: 11, Id: 'a', text: "Algeria", sprite: "flag-dz" },
       { value: 12, Id: 'a', text: "Armenia" },
       { value: 13, Id: 'a', text: "Bangladesh" },
       { value: 14, Id: 'a', text: "Cuba" },
       { value: 15, Id: 'b', text: "Denmark" },
       { value: 16, Id: 'b', text: "Egypt" },
       { value: 17, Id: 'c', text: "Finland" },
       { value: 18, Id: 'c', text: "India" },
       { value: 19, Id: 'c', text: "Malaysia" },
       { value: 20, Id: 'd', text: "New Zealand" },
       { value: 21, Id: 'd', text: "Norway" },
       { value: 22, Id: 'd', text: "Poland" },
       { value: 23, Id: 'e', text: "Romania" },
       { value: 24, Id: 'e', text: "Singapore" },
       { value: 25, Id: 'e', text: "Thailand" },
       { value: 26, Id: 'e', text: "Ukraine" }]
        $('#dropdownlist').ejDropDownList({
            dataSource: groups,
            fields: { value: "Id" },
            cascadeTo: "dropdownlist1"
        });
        $('#dropdownlist1').ejDropDownList({
            dataSource: countries,
            enabled: false
    
        });
    });
        
{% endhighlight %}

Output of the above steps

![]("/js/DropDownList/Cascading-Support_images/Cascading-Support_img2.png") 

## Multiple Cascading support

Using multi cascade option, you can create a behavior of cascade between dropdown list controls. To achieve this, map the common field from table to “**fields**” property of all the dropdown lists. Also, specify the ID of cascading **DropDownList** in “**cascadeTo”** property of parent **DropDownList**. 

N>  In case, when you want to show the cascading dropdowns in disabled state initially, then set the value of enable property as “false” in each cascading dropdowns. It is then enabled automatically once a value is selected in parent (first) dropdown list.

The following steps explains you the behavior of multiple cascade dropdown.

In an HTML page, add a &lt;input&gt; element to configure DropDownList widget.

{% highlight html %}

<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Continent</span>
    <input id="groupsList" type="text" />
</div>
<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Country</span>
    <input id="countryList" type="text" />
</div>
<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Capital</span>
    <input id="capitalList" type="text" />
</div>
     
 {% endhighlight %}
     
{% highlight js %}

    $(function () {
        // declaration
        var groups = [
        { parentId: 'a', text: "Africa" },
        { parentId: 'b', text: "Asia" },
        { parentId: 'c', text: "Europe" },
        { parentId: 'd', text: "North America" },
        { parentId: 'e', text: "South America" },
        { parentId: 'f', text: "Oceania" },
        { parentId: 'g', text: "Antarctica" }]
        //Countries List
        var countries = [
        { value: 11, parentId: 'a', text: "Algeria" },
        { value: 12, parentId: 'a', text: "Egypt" },
        { value: 13, parentId: 'b', text: "Armenia" },
        { value: 14, parentId: 'b', text: "Bangladesh" },
        { value: 15, parentId: 'b', text: "India" },
        { value: 16, parentId: 'c', text: "Denmark" },
        { value: 17, parentId: 'c', text: "Finland" },
        { value: 18, parentId: 'd', text: "Cuba" },
        { value: 19, parentId: 'd', text: "USA" },
        { value: 20, parentId: 'e', text: "Brazil" },
        { value: 21, parentId: 'e', text: "Peru" },
        { value: 22, parentId: 'f', text: "Australia" },
        { value: 23, parentId: 'f', text: "New Zealand" },
        { value: 24, parentId: 'g', text: "French Southern" },
        { value: 25, parentId: 'g', text: "South Georgia" }]
        //Capital List
        var capital = [
        { value: 111, parentId: 'a', text: "Algiers" },
        { value: 112, parentId: 'a', text: "Cairo" },
        { value: 113, parentId: 'b', text: "Yerevan" },
        { value: 114, parentId: 'b', text: "Dhaka" },
        { value: 115, parentId: 'b', text: "New Delhi" },
        { value: 116, parentId: 'c', text: "Copenhagen" },
        { value: 117, parentId: 'c', text: "Helsinki" },
        { value: 118, parentId: 'd', text: "Havana" },
        { value: 119, parentId: 'd', text: "Washington, D.C." },
        { value: 120, parentId: 'e', text: "Brasília" },
        { value: 121, parentId: 'e', text: "Lima" },
        { value: 122, parentId: 'f', text: "Canberra" },
        { value: 123, parentId: 'f', text: "Wellington" },
        { value: 124, parentId: 'g', text: "Alfred Faure" },
        { value: 125, parentId: 'g', text: "King Edward Point" }]
        $('#groupsList').ejDropDownList({
            dataSource: groups,
            fields: { value: "parentId" },
            cascadeTo: 'countryList,capitalList'
        });
        $('#countryList').ejDropDownList({
            dataSource: countries,
            fields: { value: "parentId" },
            enabled:false
        });
        $('#capitalList').ejDropDownList({
            dataSource: capital,
            fields: { value: "parentId" },
            enabled:false
        });
    });

{% endhighlight %}


The following screenshot displays the output of the above code example.

![]("/js/DropDownList/Cascading-Support_images/Cascading-Support_img4.png") 

