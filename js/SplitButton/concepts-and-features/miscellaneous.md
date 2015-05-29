---
layout: post
title: miscellaneous
description: miscellaneous
platform: js
control: Split Button
documentation: ug
---

# Miscellaneous

## Text

It is necessary to display the user defined text for **Split Button**. Using **text** property, you can easily set text content for **Split Button**. This text property overwrites the text that is provided on input button element.

The following steps explains you the details about rendering the **Split Button** with specified text.

* In the **HTML** page, add the following button elements to configure **Split Button** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="spltspan"&gt;        <button id="spltbutton_text">login</button>        &lt;ul id="Ul11"&gt;            &lt;li&gt;<span>User</span>&lt;/li&gt;            &lt;li&gt;<span>Guest</span>&lt;/li&gt;            &lt;li&gt;<span>Admin</span>&lt;/li&gt;        &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#spltbutton_text").ejSplitButton({                //used to set the text content for split button<b>                text: "signin",</b>                size: "small",                                                targetID: "Ul11"                        });        });    &lt;/script&gt;</td></tr>
</table>




**[CSHTML]**

//Add the code in the CSHTML page to configure and initialize the control



    @*Set the text for split button control as follows. *@

    &lt;div class="spltspan"&gt;

        @Html.EJ().SplitButton("spltbutton_text").**Text("signin").**Size(ButtonSize.Small).TargetID("Ul11")

        &lt;ul id="Ul11"&gt;

            &lt;li&gt;<span>User</span>&lt;/li&gt;

            &lt;li&gt;<span>Guest</span>&lt;/li&gt;

            &lt;li&gt;<span>Admin</span>&lt;/li&gt;

        &lt;/ul&gt;

    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Split Button widget



    &lt;%--Set the text for split button control as follows--%&gt;

    &lt;div class="page-align"&gt;

        &lt;ej:SplitButton ID="SplitButton_Text" runat="server" Text="signin" Size="Small"&gt;

            &lt;Items&gt;

                &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

                &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

                &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

            &lt;/Items&gt;

        &lt;/ej:SplitButton&gt;

    &lt;/div&gt;



Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .spltspan {
            margin-left: 120px;
        }
    </style>


{% endhighlight %}


Execute the above code to render the following output.

{% include image.html url="\js\SplitButton\concepts-and-features\miscellaneous_images\miscellaneous_img1.png" Caption="Figure 1411: Split button with new text"%}

In output “login” text in **Split Button** is replaced by text property value.

## Show Rounded Corner

Specifies the corner of **Split Button** in rounded shape. By default, the edges of **Split Button** is not rounded. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Split Button** with rounded corner.

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="spltspan"&gt;        <button id="spltbutton_roundedCorner">login</button>        &lt;ul id="Ul11"&gt;            &lt;li&gt;<span>User</span>&lt;/li&gt;            &lt;li&gt;<span>Guest</span>&lt;/li&gt;            &lt;li&gt;<span>Admin</span>&lt;/li&gt;        &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;        $(function () {            $("#spltbutton_roundedCorner").ejSplitButton({                               size: "small",                    //Enable or disable the rounded corner for split button            <b>                showRoundedCorner: true,</b>                targetID: "Ul11"                        });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in the CSHTML page to configure and initialize the control



    @*Enable the rounded corner for split button control as follows.*@

    &lt;div class="spltspan"&gt;

        @Html.EJ().SplitButton("spltbutton_roundedCorner").Text("login").Size(ButtonSize.Small).**ShowRoundedCorner(true)**.TargetID("Ul11")

        &lt;ul id="Ul11"&gt;

            &lt;li&gt;<span>User</span>&lt;/li&gt;

            &lt;li&gt;<span>Guest</span>&lt;/li&gt;

            &lt;li&gt;<span>Admin</span>&lt;/li&gt;

        &lt;/ul&gt;



    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Split Button widget



&lt;%--Enable the rounded corner for split button control as follows--%&gt;

    &lt;div class="page-align"&gt;

        &lt;ej:SplitButton ID="SplitButton_RoundedCorner" runat="server" Text="login" ShowRoundedCorner="true" Size="Small"&gt;

            &lt;Items&gt;

                &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

                &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

                &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

            &lt;/Items&gt;

        &lt;/ej:SplitButton&gt;

    &lt;/div&gt;



Configure the styles 



{% highlight css %}

[CSS]
    <style>
        .spltspan {
            margin-left: 120px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\SplitButton\concepts-and-features\miscellaneous_images\miscellaneous_img2.png" Caption="Figure 1512: Split button with rounded corner"%}



