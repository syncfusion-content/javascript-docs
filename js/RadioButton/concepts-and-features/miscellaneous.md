---
layout: post
title: miscellaneous
description: miscellaneous
platform: js
control: RadioButton
documentation: ug
---

# Miscellaneous

## Radio ButtonRadioButton ID

**Radio buttonRadioButton id** is not shown in the user interface. Here **id** denotes the **id** attribute of the root element of **Radio****buttonRadioButton** control. This **id** value is unique. You can give **id** through **element** and through the **id property**. When you use two **ids** for a single radio button at initialization, the **element id** is considered.

Set **id** for **Radio****buttonRadioButton** control as follows.



{% highlight js %}

<script type="text/javascript">
        $(function () {
            //set new id value as follows
            $("#RadBtn_Male").ejRadioButton({ name: "Gender", **id: "male_type"** });
            $("#RadBtm_female").ejRadioButton({ name: "Gender", **id: "female_type"** });
        });
    </script>


{% endhighlight %}



[CSHTML]



@*set new id value as follows*@

    @Html.EJ().RadioButton("RadBtn_Male").**Id("male_type")**.Name("Gender")

    &lt;br /&gt;

    @Html.EJ().RadioButton("RadBtm_female").**Id("female_type")**.Name("Gender")





[aspx]

&lt;%--set new id value as follows--%&gt;

    &lt;ej:RadioButton Name="Gender" ID="RadBtn_Male" runat="server" Size="Small" Text="Male"&gt;&lt;/ej:RadioButton&gt;

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="RadBtm_female" runat="server" Size="Small" Text="Female"&gt;&lt;/ej:RadioButton&gt;

## Radio ButtonRadioButton Prefix id

Id prefix value is appended to id value. It is used to mention the prefix for the wrapper’s id attribute. When you assign a value for **idPrefix** property, the older prefix id gets replaced by the new prefix id. 

Setting a new prefix id for **Radio****buttonRadioButton** control is as follows.



{% highlight js %}

  <script type="text/javascript">
        $(function () {
            //set new idPrefix value as follows
            $("#Radio_Male").ejRadioButton({ name: "Gender", **idPrefix:"sync"**  });
            $("#Radio_Female").ejRadioButton({ name: "Gender", **idPrefix:"sync"**  });
        });
    </script>


{% endhighlight %}



[CSHTML]

@*set new idPrefix  value as follows*@

    @Html.EJ().RadioButton("Radio_Male").**IdPrefix("sync_")**.Name("Gender")

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio_Female").**IdPrefix("sync_")**.Name("Gender") 



[aspx]

  &lt;%--set new idPrefix   value as follows--%&gt;

    &lt;ej:RadioButton Name="Gender" ID="RadBtn_Male" IdPrefix="sync_" runat="server" Size="Small" Text="Male"&gt;&lt;/ej:RadioButton&gt;

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="RadBtm_female" IdPrefix="sync_" runat="server" Size="Small" Text="Female"&gt;&lt;/ej:RadioButton&gt;

## Radio ButtonRadioButton Name

The **name** setting tells you where a **Radio****buttonRadioButton** belongs. When you select one button, all other buttons in the same group are unselected. You can have only one group of **Radio****buttonRadioButtons** on each page.

The **name** attribute is also used to identify form data after it has been submitted to the server, or for reference of form data using **JavaScript** on the client’s side. Only form elements with a **name** attribute have their values passed, when submitting a form.

## Radio ButtonRadioButton Value

The **value** setting defines what can be submitted when checked.

For **Radio buttonRadioButtons**, the contents of the value property do not appear in the user interface. The **value** property only has meaning when submitting a form. If a radio button is in the checked state when the form is submitted, the name of the Radio button is sent along with the value of the value property, if the radio button is not checked, no information is sent.

To identify, on the server side, which one was checked, give different values for radio buttons in the same group, 

Set name and value for each radio button control as follows.



{% highlight js %}

<script type="text/javascript">
        $(function () {
            //set name and value for each radio button as follows
            $("#Radio_Male").ejRadioButton({ **name: "Gender", value: "male"**  });
            $("#Radio_Female").ejRadioButton({ **name: "Gender", value: "female"** });
        });
    </script>


{% endhighlight %}



[CSHTML]

@*set name and value for each radio button as follows*@

    @Html.EJ().RadioButton("Radio_Male").**Name("Gender").Value("male")**

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio_Female").**Name("Gender").Value("female")** 



[aspx]

&lt;%--set name and value for each radio button as follows--%&gt;

    &lt;ej:RadioButton ID="RadBtn_Male" runat="server" Size="Small" Text="Male" Name="Gender" Value="male"&gt;&lt;/ej:RadioButton&gt;

    &lt;br /&gt;

    &lt;ej:RadioButton ID="RadBtm_female" runat="server" Size="Small" Text="Female" Name="Gender" Value="female"&gt;&lt;/ej:RadioButton&gt;







