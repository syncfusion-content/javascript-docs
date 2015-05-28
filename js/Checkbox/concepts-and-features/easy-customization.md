---
layout: post
title: easy-customization
description: easy customization
platform: js
control: Checkbox
documentation: ug
---

# Easy customization

## Checked status

Using **checked** property, you can set the state of **Checkbox**. When checked property is true then tick mark is displayed and **Checkbox** is in checked state. When it is false, the tick mark is not displayed and **Checkbox** is in unchecked state. When you want to use this **checked** property, then checkbox should be in non Tri-state and **enableTriState** property should be false.

The following steps explains you the details about rendering the **Checkbox** with above mentioned checked options, when the checkbox is in non tri-state.

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_nonchecked" /&gt;        <label for="checkbox_nonchecked" class="clslab">Music</label>        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_checked" /&gt;        <label for="checkbox_checked" class="clslab">Music</label>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            //disable the checked status            $("#checkbox_nonchecked").ejCheckBox({ <b>checked: false</b> });            //enables the checked status            $("#checkbox_checked").ejCheckBox({ <b>checked: true</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control


@* set the state for non Tri-state checkbox using Checked property*@                

    @Html.EJ().CheckBox("checkbox_unchecked").**Checked(false)**

    <label for="checkbox_unchecked" class="clslab">Music</label>

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_checked").**Checked(true)**

    <label for="checkbox_checked" class="clslab">Music</label>



**[aspx]**

// Add the code in ASPX page to configure Checkbox widget

  &lt;%--set the state for non Tri-state checkbox using Checked property--%&gt;

    <ej:CheckBox ID="UnChecked_CheckBox" runat="server" **Checked="false"**>Music</ej:CheckBox>

    &lt;br /&gt;

    <ej:CheckBox ID="Checked_CheckBox" runat="server" **Checked="true"**>Music</ej:CheckBox>



Execute the above code to render the following output.



![](easy-customization_images\easy-customization_img1.png)![](easy-customization_images\easy-customization_img2.png)

_Figure_ _12__4__: Checkbox in binary states_

## Enable Tri-State

Sometimes, it is essential for you to represent the answer in partially true state. To represent the partially true types, an indeterminate state option is present. The state between checked and unchecked state is called indeterminate state. For example, a **Checkbox** presented to select files to send via [FTP](http://en.wikipedia.org/wiki/File_Transfer_Protocol) can use a [tree view](http://en.wikipedia.org/wiki/Tree_view) so that files can be selected one at a time, or by folder. When only some of the files in a folder are selected, then the checkbox for that folder could be in indeterminate state.

When you enable Tri-state, then the **Checkbox** includes the indeterminate state. The **Checkbox** has three states. **enableTriState** property specifies to enable or disable the Tri-State option for **Checkbox**. 

The following steps explains you the details about rendering the **Checkbox** with Tri-state options.

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_nonTriState" /&gt;        <label for="checkbox_nonTriState" class="clslab">Music</label>        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_triState" /&gt;        <label for="checkbox_triState" class="clslab">Music</label>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //disables the Tri- state for checkbox            $("#checkbox_nonTriState").ejCheckBox({ <b>enableTriState: false</b> });            //enables the Tri- state for checkbox            $("#checkbox_triState").ejCheckBox({ enableTriState: true, checkState:"indeterminate" });$("#checkbox_triState").ejCheckBox({ <b>enableTriState: true</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control



@* Enable or disable the Tri-state using EnableTriState property *@

    @Html.EJ().CheckBox("checkbox_nonTriState").**EnableTriState(false)**

    <label for="checkbox_nonTriState" class="clslab">Music</label>

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_triState").**EnableTriState(true)**

    <label for="checkbox_triState" class="clslab">Music</label>



**[aspx]**

// Add the code in ASPX page to configure Checkbox widget

&lt;%--Enable or disable the Tri-state using EnableTriState property --%&gt;

    &lt;ej:CheckBox ID="NonTriState_CheckBox" runat="server" EnableTriState="false"&gt; Music</ej:CheckBox>

    &lt;br /&gt;

    &lt;ej:CheckBox ID="TriState_CheckBox" runat="server" EnableTriState="true"&gt; Music</ej:CheckBox>



Execute the above code to render the following output.



![](easy-customization_images\easy-customization_img3.png)![](easy-customization_images\easy-customization_img4.png)

_Figure_ _13__5__: Checkbox with Non-Tri state and_ _Tri-state_

## Check State

You require an option to set indeterminate state for **Checkbox**. By using **checkState** property, you can set any state that is illustrated in following table. Before using this property, enable the Tri-state for **Checkbox**. **enableTriState** property****is set true.

_Table_ _1__: List of check states_

<table>
<tr>
<td>
check</td><td>
Check box will be in checked state</td></tr>
<tr>
<td>
uncheck</td><td>
Check box will be in un-checked state</td></tr>
<tr>
<td>
indeterminate</td><td>
Check box will be in indeterminate state</td></tr>
</table>


The following steps explains you the details about rendering the **Checkbox** with specified checked state, when the checkbox is in tri-state.

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>  &lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="check" /&gt;        <label for="check" class="clslab">Checked state</label>        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="uncheck" /&gt;        <label for="uncheck" class="clslab">Unchecked state</label>        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="indeterminate" /&gt;        <label for="indeterminate" class="clslab">Indeterminate state</label>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //checkState property used to mention the state of checkbox            $("#check").ejCheckBox({ enableTriState: true<b>, checkState: "check"</b> });            $("#uncheck").ejCheckBox({ enableTriState: true<b>, checkState: "uncheck"</b> });            $("#indeterminate").ejCheckBox({ enableTriState: true<b>, checkState: "indeterminate"</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control



@*set the state of Tri-state checkbox using CheckState property*@

  @Html.EJ().CheckBox("checkbox_check").EnableTriState(true).**CheckState(CheckState.Check)**

    <label for="checkbox_check" class="clslab">Checked state</label>

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_uncheck").EnableTriState(true).**CheckState(CheckState.Uncheck)**

    <label for="checkbox_uncheck" class="clslab">Unchecked state</label>

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_indeterminate").EnableTriState(true).**CheckState(CheckState.Indeterminate)**

    <label for="checkbox_indeterminate" class="clslab">Indeterminate state</label>



[aspx]

// Add the code in ASPX page to configure Checkbox widget

&lt;%--set the state of Tri-state checkbox using CheckState property--%&gt;



    &lt;ej:CheckBox ID="Checked_CheckBox" runat="server" EnableTriState="true" CheckState="Check"&gt; Checked state</ej:CheckBox>

    &lt;br /&gt;

      &lt;ej:CheckBox ID="UnChecked_CheckBox" runat="server" EnableTriState="false" CheckState="Uncheck"&gt; Unchecked state</ej:CheckBox>

    &lt;br /&gt;

    &lt;ej:CheckBox ID="Indeterminate_CheckBox" runat="server" EnableTriState="true" CheckState="Indeterminate"&gt; Indeterminate state</ej:CheckBox>



Execute the above code to render the following output.


![](easy-customization_images\easy-customization_img5.png)

_Figure_ _14__6__: Checkbox in three different states_

## Checkbox Size

You can render **Checkbox** in different sizes. The following table contains some predefined size option for rendering a **Checkbox** in easiest way. Each size option has different height and width. Mainly it avoids the complexity in rendering **Checkbox** with complex **CSS** class. 

_Table_ _2__: List of checkbox size_

<table>
<tr>
<td>
<b>small</b></td><td>
Creates checkbox with inbuilt small size height, width specified.</td></tr>
<tr>
<td>
<b>medium</b></td><td>
Creates checkbox with inbuilt medium size height, width specified.</td></tr>
</table>


The following steps explains you the details about rendering the **Checkbox** with different size.

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_small" /&gt;        <label for="checkbox_small" class="clslab">Small size</label>        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_medium" /&gt;        <label for="checkbox_medium" class="clslab">Medium size</label>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //size property is used to specify the checkbox size            $("#checkbox_small").ejCheckBox({ <b>size: "small"</b> });            $("#checkbox_medium").ejCheckBox({ <b>size: "medium"</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control



    @* set the size of checkbox using Size property *@

    @Html.EJ().CheckBox("checkbox_small").**Size(Size.Small)**

    <label for="checkbox_small" class="clslab">Small size</label>

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_medium").**Size(Size.Medium)**

    <label for="checkbox_medium" class="clslab">Medium size</label>



[aspx]

// Add the code in ASPX page to configure Checkbox widget

    &lt;%--set the size of checkbox using Size property--%&gt;



    <ej:CheckBox ID="SmallSize_Checkbox" runat="server" **Size="Small"**>Small size</ej:CheckBox>

    &lt;br /&gt;

    <ej:CheckBox ID="MediumSize_Checkbox" runat="server" **Size="Medium"**>Medium size</ej:CheckBox>



Execute the above code to render the following output.


![](easy-customization_images\easy-customization_img6.png)

_Figure_ _15__7__: Checkbox in different sizes_

## Text

It specifies the text content for **Checkbox**. In previous programs, separate label for each **Checkbox** is created. You can also set the text for checkbox using **text** property. Therefore, it is not essential to add label tag for each checkbox in **HTML** code.

The following steps explains you the details about rendering the **Checkbox** with text content and without writing label tag in **HTML** code

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_text" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            //size property is used to set text for checkbox            $("#checkbox_text").ejCheckBox({ <b>text: "Music"</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control

    @*set text for checkbox using Text property *@

    @Html.EJ().CheckBox("checkbox_text").**Text("Music")** 



**[aspx]**

// Add the code in ASPX page to configure Checkbox widget

&lt;%--set text for checkbox using Text property--%&gt;

    &lt;ej:CheckBox ID="CheckBox_Text" runat="server" Text="Music"&gt;&lt;/ej:CheckBox&gt;



Execute the above code to render the following output.


![](easy-customization_images\easy-customization_img7.png)

_Figure_ _16__8__: Checkbox with text content_

## Rounded corner for checkbox

Specifies the corner of **Checkbox** in rounded shape. Checkbox doesn’t have rounded corner by default. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Checkbox** with rounded corner.

* In the **HTML** page, add the following input elements to configure **Checkbox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div class="align"&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_normalCorner" /&gt;        &lt;br /&gt;        &lt;br /&gt;        &lt;input type="checkbox" class="nodetext" id="checkbox_roundedCorner" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            $("#checkbox_normalCorner").ejCheckBox({ <b>showRoundedCorner: false</b> });            $("#checkbox_roundedCorner").ejCheckBox({ <b>showRoundedCorner: true</b> });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure and initialize the control



    @*set the rounded corner for checkbox *@

    @Html.EJ().CheckBox("checkbox_normalCorner").**ShowRoundedCorner(false).**Text("checkbox without rounded corner")

    &lt;br /&gt;

    @Html.EJ().CheckBox("checkbox_roundedCorner").**ShowRoundedCorner(true).**Text("checkbox with rounded corner")



[aspx]

// Add the code in ASPX page to configure Checkbox widget

&lt;%--set the rounded corner for checkbox--%&gt;

    &lt;ej:CheckBox ID="NormalCorner_Checkbox" runat="server" ShowRoundedCorner="false" Text="checkbox without rounded corner"&gt;&lt;/ej:CheckBox&gt;

    &lt;br /&gt;

    &lt;ej:CheckBox ID="RoundedCorner_Checkbox" runat="server" ShowRoundedCorner="true" Text="checkbox with rounded corner"&gt;&lt;/ej:CheckBox&gt;


Execute the above code to render the following output.


![](easy-customization_images\easy-customization_img8.png)

_Figure_ _17__9__: Checkbox with non-rounded & rounded corner_

