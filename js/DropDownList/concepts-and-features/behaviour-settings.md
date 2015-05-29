---
layout: post
title: behaviour-settings
description: behaviour settings
platform: js
control: DropDownList
documentation: ug
---

# Behaviour Settings

The following are some miscellaneous properties that helps you to change the behaviour of **DropdownList** control 

**Target ID**

You can append a list with dropdown textbox by using **targetIDId** property. You need to define a &lt;ul&gt;, &lt; li&gt; tag that you want to show on **Dropdown List** and then set the id of parent &lt;ul&gt; tag to **targetIDId** property. Its data type is string. 

The following steps explains you the configuration of **targetID** property in **Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **Dropdownlist** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;       &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                <b>targetID</b>: "list"            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").**TargetID**("list") 

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;



     &lt;ej:DropDownList ID="dropdownlist" Width="200px" TargetID="list" runat="server"&gt;



        &lt;/ej:DropDownList&gt;



   &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;

    &lt;/div&gt;

**Number of items in the list**

**Dropdown** widget provides you support to customize the items visible on popup visible. The **itemsCount** property defines the number of items that is displayed on **DropdownList****Dropdown List**. Its data type is number.

The following steps explains you the configuration of **itemsCount** property in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>itemsCount</b>: 3                            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**ItemsCount**(3)



        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

       &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" ItemsCount="3" runat="server"&gt;

      &lt;/ej:DropDownList&gt;

       &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;

    &lt;/div&gt;



Output of the above steps



![](behaviour-settings_images\behaviour-settings_img1.png)


_Figure_ _40__14__: Dropdown with itemsCount property_  

**Select the value by index** 

Dropdown widget provides you support to select an item by mentioning the index of the item. The **selectedItemIndex** property helps you to select the particular item from the list. Its date type is number. 

The following steps explains you the configuration of **selectedItemIndex** property in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                itemsCount: 3,                <b>selectedItemIndex</b>: 1                            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**SelectedItemIndex**(1)

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



  &lt;div class="control"&gt;



     &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" SelectedItemIndex="1" runat="server"&gt;



        &lt;/ej:DropDownList&gt;



   &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;

    &lt;/div&gt;





Output of the above steps


![](behaviour-settings_images\behaviour-settings_img2.png)

_Figure_ _41__15__: Dropdown with selecteditemindex property_  

**Show Popup on load**

You can display the popup panel when page load itself using **showPopupOnLoad** property. Its data type is Boolean. 

The following steps explains you the configuration of **showPopupOnLoad** property in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>showPopupOnLoad</b>: true            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**ShowPopupOnLoad**(true)

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" ShowPopupOnLoad="true" runat="server"&gt;

       &lt;/ej:DropDownList&gt;

            &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;

&lt;/div&gt;

    &lt;/div&gt;

**Multiple selection through index** 

You can select the list of items from the **DropdownList****Dropdownlist** using **selectedItems** property. Its data type is array. To achieve this, you need to set true to **checkbox** property in **DropdownList****Dropdownlist**. 

The following steps explains you the configuration of **selectedItems** property in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;      $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>selectedItems</b>: [0, 1],                <b>showCheckbox</b>:true            });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@{List<int> indexList = new List<int>();

  indexList.Add(0);

  indexList.Add(1);

}

@Html.EJ().DropDownList("dropdownlist").TargetID("list").ShowCheckbox(true).SelectedItems(indexList)



&lt;div id="list"&gt;

    &lt;ul&gt;

        <li>Art</li>

        <li>Architecture</li>

        <li>Biography</li>

        <li>Comics</li>

        <li>Sports</li>

        <li>Science</li>

    &lt;/ul&gt;

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b>// Add Dropdown list widget in ASPX page&lt;div class="control"&gt;      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" ShowCheckbox="true"  runat="server"&gt;      &lt;/ej:DropDownList&gt;&lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>Comics</li>                <li>Sports</li>                <li>Science</li>             &lt;/ul&gt;     &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[C#]  // Add list items for the control in CS page        protected void Page_Load(object sender, EventArgs e)        {            List<int> list = new List<int>();            list.Add(0);            list.Add(1);            dropdownlist.<b>SelectedItems</b> = list;           }</td></tr>
</table>


Output of the above steps


![](behaviour-settings_images\behaviour-settings_img3.png)

_Figure_ _42__16__: Dropdown with selecteditems property_  

**Read-only**

This feature supports to make the dropdown as readable. That is, you can make the dropdown as editable or non-editable by setting Boolean type value to **readOnly** property.

The following steps explains you the configuration of **readOnly** property in **DropdownList****Dropdownlist.**

1. In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;       &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>readOnly</b>: true            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**ReadOnly**(true)

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px"  ReadOnly="true" runat="server"&gt;

      &lt;/ej:DropDownList&gt;

     &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

             &lt;/ul&gt;

     &lt;/div&gt;



**Enable or Disable the Dropdown Widget**

This features enables you to set the enable or disable options for dropdown by setting Boolean type value to **enabled** property. 

The following steps explains you the configuration of **enabled** property in **DropdownList****Dropdownlist**.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;       &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>enabled</b>: false            });        });   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**Enabled**(false)

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Enabled="false" Width="200px" runat="server"&gt;

      &lt;/ej:DropDownList&gt;

     &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

             &lt;/ul&gt;

     &lt;/div&gt;

&lt;/div&gt;



Output of the above steps 


![C:\Users\ApoorvahR\Desktop\3.png](behaviour-settings_images\behaviour-settings_img4.png)

_Figure_ _43__17__: Dropdown with enable property_  

**Persistence support** 

This features enables you to save current model value to browser cookies for state maintains. When you refresh the **DropDownList** control page, it retains the model value apply from browser cookies. The date type of **enablePersistence** is Boolean type. 

The following steps explains you the configuration of **enablePersistence** property in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;  &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>enablePersistence</b>: true,            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**EnablePersistence**(true)

        &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" EnablePersistence="true" Width="200px" runat="server"&gt;

      &lt;/ej:DropDownList&gt;

     &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

             &lt;/ul&gt;

     &lt;/div&gt;

&lt;/div&gt;



