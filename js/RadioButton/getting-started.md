---
layout: post
title: getting-started
description: getting started
platform: js
control: RadioButton
documentation: ug
---

# Getting Started

This section briefly describes you on how to create a **QuizApp** and **RegistrationApp** using **Essential JavaScript** and **ASP.NET MVC RadioButton** control and use the features available in it.

## Create your first RadioButton in JavaScript

**Essential JavaScript****RadioButton** supports RTL, custom skins and events to display customized **RadioButtons**.  In this example, you can learn how to use **RadioButton** in a Quiz application. The following guidelines show you how to use the **RadioButton** to select the answers in the application and get the selected items. The following screenshot displays a sample Quiz application.


{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img1.png" Caption="Figure 1: Quiz application"%}

### Create a RadioButton in a Quiz Application

**Essential JavaScript RadioButton** is created by using a simple input textbox element as follows.

* Create an **HTML** file and add the following template to the **HTML** file to create **RadioButton**.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
      <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)">
</script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add RadioButton element here --> 
</body>
</html>



{% endhighlight %}





Add input element to render a **RadioButton**.



{% highlight html %}

  <div>
        1. What is the Expansion for MVC ? <br />
        <table>
            <tr>
                <td >
                    <input type="radio" name="small1" id="Radio1" /><label for="Radio1" >Model View Controller</label></td>
                <td  colspan="2">
                    <input type="radio" name="small1" id="Radio2" /><label for="Radio2" >Model Virtual Container</label></td>
                <td colspan="2">
                    <input type="radio" name="small1" id="Radio3" /><label for="Radio3" >Model Visual Controller</label></td>
            </tr>
        </table>
        <br><br><br>
        2.  What is the Expanson for USB ?<br />
        <table>
            <tr>
                <td >
                    <input type="radio" name="small2" id="Radio4" /><label for="Radio4" >Universal serialized Buffer</label></td>
                <td>
                    <input type="radio" name="small2" id="Radio5" /><label for="Radio5" >Universal Serial Buffer</label></td>
                <td>
                    <input type="radio" name="small2" id="Radio6" /><label for="Radio6" >Universal Serial Bus</label></td>
            </tr>
        </table>
        <br><br><br>
        3.   What is the Expanson for HTML ?<br />
        <table>
            <tr>
                <td>
                    <input type="radio" name="small3" id="Radio7" /><label for="Radio7" >Hyper Text Makeup Language</label></td>
                <td>
                    <input type="radio" name="small3" id="Radio8" /><label for="Radio8" >Hyper Text Markup Language</label></td>
                <td>
                    <input type="radio" name="small3" id="Radio9" /><label for="Radio9" >Hyper Text Makeup Loader</label></td>
            </tr>
        </table>
        <br><br><br>

        <button id="submitid" onclick="button()">Submit</button>

    </div>


{% endhighlight %}



* Initialize **RadioButton** in script.



{% highlight js %}

<script type="text/javascript">
        $(function () {
            // declaration
            $("#Radio1").ejRadioButton({ size: "medium" });
            $("#Radio2").ejRadioButton({ size: "medium" });
            $("#Radio3").ejRadioButton({ size: "medium" });
            $("#Radio4").ejRadioButton({ size: "medium" });
            $("#Radio5").ejRadioButton({ size: "medium" });
            $("#Radio6").ejRadioButton({ size: "medium" });
            $("#Radio7").ejRadioButton({ size: "medium" });
            $("#Radio8").ejRadioButton({ size: "medium" });
            $("#Radio9").ejRadioButton({ size: "medium" });

        });

        function button()
        {
            var checkeditem = [];
            $(".e-radiobtn:checked").each(function () {
                checkeditem.push($(this).parent().siblings().html());
            });
            alert(checkeditem);
        }

    </script>


{% endhighlight %}



* Add the following styles.



{% highlight css %}

<style>
    html, body {
        width: 100%;
        margin: 0;
    }

    .frame {
        width: 80%;
    }
</style>


{% endhighlight %}


The following screenshot displays the output for the above code.



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img2.png" Caption="Figure 2: Quiz application"%}

## Create your first RadioButton in MVC

**ASP.NET MVC RadioButton** provides support to display the **RadioButton** within your webpage, and allows you to pick your choice. Using the following guidelines, you can customize **RadioButton** for a real-time QuizApp and RegistrationApp scenarios. This allows you to select the corresponding choice for each question.



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img3.png" Caption="Figure 3: RadioButton in QuizApp"%}

**Create your QuizApp**

**Essential Studio ASP.NET MVC****RadioButton** widget has a built-in feature to select a single option from the QuizApp. You can create the **RadioButton** widget using the following steps.

* Create an **MVC** Project and add necessary assemblies and scripts to it.

Refer [MVC-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

Add the following code example to the corresponding view page to render **RadioButton**.



&lt;div class="frame"&gt;

        &lt;div&gt;

            &lt;div &gt;

                &lt;br /&gt;

               1. What is the Expansion for MVC<br />



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio1").Name("rad1").Size(RadioButtonSize.Small).Checked(false).Enabled(true)&lt;!--Creates a small Radio Button--&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Model View Controller

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td  &gt;

                            @Html.EJ().RadioButton("Radio2").Name("rad1").Size(RadioButtonSize.Small).Checked(false).Enabled(true)

                            &lt;label for="Radio2" class="clslab"&gt;

                                Model Virtual Container

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio3").Name("rad1").Size(RadioButtonSize.Small).Checked(false).Enabled(true)

                            &lt;label for="Radio3" class="clslab"&gt;

                                Model Visual Controller

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;

               2.What is the Expansion for USB<br />



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio4").Name("rad2").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)&lt;!--Creates a Medium size Radio Button--&gt;

                            &lt;label for="Radio4" class="clslab"&gt;

                                Universal Serial Bus

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio5").Name("rad2").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)

                            &lt;label for="Radio5" class="clslab"&gt;

                                Universal Serial Buffer

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().RadioButton("Radio6").Name("rad2").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)

                            &lt;label for="Radio6" class="clslab"&gt;

                                Universal Serialized Buffer

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br/&gt;

                &lt;br /&gt;

                3.What is the Expansion for JS<br />



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio7").Name("rad3").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)

                            &lt;label for="Radio7" class="clslab"&gt;

                                Jquery Script

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio8").Name("rad3").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)

                            &lt;label for="Radio8" class="clslab"&gt;

                                Java Script

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;



                            @Html.EJ().RadioButton("Radio9").Name("rad3").Size(RadioButtonSize.Medium).Checked(false).Enabled(true)

                            &lt;label for="Radio9" class="clslab"&gt;

                                Json Script

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;



                &lt;/table&gt;

                &lt;center&gt;

                    &lt;table&gt;

                        @Html.EJ().Button("Submit").Width("100px").Size(ButtonSize.Large).Text("Submit").ClientSideEvents(s => s.Click("button"))

                &lt;/center&gt; 

                      &lt;/table&gt; 



                &lt;br /&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

**Add Script**

&lt;script type="text/javascript"&gt;



    function button()

    {

        var checkeditem = [];

            $(".e-radiobtn:checked").each(function (index, Element) {

                //if ($(this).ejRadioButton('isChecked')) {

                    checkeditem.push($(this).parent().siblings().html());

                //}

            });

            alert(checkeditem);

    }

    &lt;/script&gt;

**Configure Style**

Add the following code example in the index page.

&lt;style&gt;

        .frame {

            width: 80%;

        }

    &lt;/style&gt;


 Execute the above code example to render the following output.


{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img4.png" Caption="Figure 4: QuizApp"%}

**Create RegistrationApp**

{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img5.png" Caption="Figure 5: RegistrationApp"%}

&lt;div class="frame"&gt;

        &lt;div&gt;

            &lt;div &gt;

                &lt;br /&gt;

               1. Are you a Fresher ?&lt;br /&gt;



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td &gt;

                            @Html.EJ().RadioButton("Radio1").Name("rad1").Size(RadioButtonSize.Small).Checked(false).Enabled(true)&lt;!--Creates a small Radio Button--&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                               Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td  &gt;

                            @Html.EJ().RadioButton("Radio2").Name("rad1").Size(RadioButtonSize.Small).Checked(false).Enabled(true)

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;



                2. Do you complete any .NET certification courses ?&lt;br /&gt;



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            @Html.EJ().RadioButton("Radio3").Name("rad2").Size(RadioButtonSize.Small).Checked(false).Enabled(true)&lt;!--Creates a small Radio Button--&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().RadioButton("Radio4").Name("rad2").Size(RadioButtonSize.Small).Checked(false).Enabled(true)

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;



                3. Are you interested to work in .NET platform ?&lt;br /&gt;



                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            @Html.EJ().RadioButton("Radio5").Name("rad3").Size(RadioButtonSize.Small).Checked(false).Enabled(true)&lt;!--Creates a small Radio Button--&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().RadioButton("Radio6").Name("rad3").Size(RadioButtonSize.Small).Checked(false).Enabled(true)

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;









                &lt;center&gt;

                    &lt;table&gt;

                        @Html.EJ().Button("Submit").Width("100px").Size(ButtonSize.Large).Text("Submit").ClientSideEvents(s => s.Click("button"))

                &lt;/center&gt; 

                      &lt;/table&gt; 



                &lt;br /&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

**Add Script**

&lt;script type="text/javascript"&gt;



    function button()

    {

        var checkeditem = [];

            $(".e-radiobtn:checked").each(function (index, Element) {

                //if ($(this).ejRadioButton('isChecked')) {

                checkeditem.push( $(this).parent().siblings().html());



                //}

            });

            alert(checkeditem);

    }

    &lt;/script&gt;

**Add Style**

&lt;style&gt;

        .frame {

            width: 80%;

        }

    &lt;/style&gt;



Execute the above code example to render the following outputs.



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img6.png" Caption="Figure 6: RegistrationApp"%}



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img7.png" Caption="Figure 7: Output"%}

## Create your first RadioButton in ASP.NET

Using **ASP.NET WebForms RadioButton** supports RTL, custom skins and events to display customized **RadioButtons**.  In this example, you can learn how to use **RadioButton** in a Quiz application. The following guidelines illustrate you on how to use the **RadioButton** to select the answers in the application and get the selected items. The following screenshot shows a sample Quiz application.



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img8.png" Caption="Figure 8: Quiz application"%}

**Create a RadioButton in a Quiz Application**

**ASP.NET WebForms RadioButton** provides support to display the **RadioButton** within your webpage, and allows you to pick your choice. Using the following guidelines, you can customize **RadioButton** for a real-time **QuizApp** and **RegistrationApp** scenarios. This allows you to select the corresponding choice for each question.

Using the following steps, you can create a **RadioButton** control.

1. You can create an **ASP.NET Project** and add necessary **Dll** and script with the help of the given [WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code to render **RadioButton**.



**[ASPX]**

&lt;div&gt;

        1. What is the Expansion for MVC ?

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    <ej:RadioButton Name="question1" Size="Medium" ID="RadioButton1" Text="Model View Controller"

                        runat="server">

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio1"&gt;

                        Model View Container</label>

                &lt;/td&gt;

                &lt;td colspan="2"&gt;

                    <ej:RadioButton Name="question1" Size="Medium" ID="RadioButton2" Text="Model Virtual Container"

                        runat="server">

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio2"&gt;

                        Model Virtual Container</label>

                &lt;/td&gt;

                &lt;td colspan="2"&gt;

                    <ej:RadioButton Name="question1" Size="Medium" ID="RadioButton3" Text="Model Visual Controller"

                        runat="server">

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio3"&gt;

                        Model Visual Controller</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        2. What is the Expanson for USB ?&lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question2" Size="Medium" ID="RadioButton4" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio4"&gt;

                        Universal serialized Buffer</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question2" Size="Medium" ID="RadioButton5" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio5"&gt;

                        Universal Serial Buffer</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question2" Size="Medium" ID="RadioButton6" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio6"&gt;

                        Universal Serial Bus</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        3. What is the Expanson for HTML ?&lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question3" Size="Medium" ID="RadioButton7" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio7"&gt;

                        Hyper Text Makeup Language</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question3" Size="Medium" ID="RadioButton8" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio8"&gt;

                        Hyper Text Markup Language</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="question3" Size="Medium" ID="RadioButton9" runat="server"&gt;

                    &lt;/ej:RadioButton&gt;

                    &lt;label for="Radio9"&gt;

                        Hyper Text Makeup Loader</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;button id="submitid" onclick="button()"&gt;

            Submit</button>

    &lt;/div&gt;

**Configure Style**

* Add the following styles.



**[CSS]**

&lt;style&gt;

        html, body

        {

            width: 100%;

            margin: 0;

        }



        .frame

        {

            width: 80%;

        }

    &lt;/style&gt;



The following screenshot displays the output for the above code.

{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img9.png" Caption="Figure 9: Quiz application"%}

**Create RegistrationApp**

{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img10.png" Caption="Figure 10: RegistrationApp"%}

In this section, you can learn how to create a **RegistrationApp** scenario as shown in the above screenshot.

Using the following steps, you can create a **RegistrationApp** using **RadioButton** control.

* Add the following code to render **RadioButton**.



**[ASPX]**

    &lt;div class="frame"&gt;

        &lt;div&gt;

            &lt;div&gt;

                &lt;br /&gt;

                1. Are you a Fresher ?&lt;br /&gt;

                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question1" Size="Small" ID="RadioButton1" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question1" Size="Small" ID="RadioButton2" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;

                2. Do you complete any .NET certification courses ?&lt;br /&gt;

                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question2" Size="Small" ID="RadioButton3" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question2" Size="Small" ID="RadioButton4" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;

                3. Are you interested to work in .NET platform ?&lt;br /&gt;

                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question3" Size="Small" ID="RadioButton5" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio1" class="clslab"&gt;

                                Yes

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            <ej:RadioButton Name="question3" Size="Small" ID="RadioButton6" Checked="false" Enabled="true"

                                runat="server">

                            &lt;/ej:RadioButton&gt;

                            &lt;label for="Radio2" class="clslab"&gt;

                                No

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;br /&gt;

                &lt;br /&gt;

                &lt;center&gt;

                    <ej:Button ID="button1" Type="Submit" Width="100px" Size="Large" Text="Submit" ClientSideOnClick="buttonClicked"

                        runat="server">

                    &lt;/ej:Button&gt;

                &lt;/center&gt;

                &lt;br /&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

**Add Script**

* Add the following ClientSide event for submit button to get the selected items.



**[Script]**

&lt;script type="text/javascript"&gt;

        function buttonClicked() {

            var checkeditem = "";

            $(".e-radiobtn:checked").each(function () {

                checkeditem += $(this).parent().siblings().html();

            });

            if (checkeditem != "")

                alert("The form is submitted with the following Selection" + checkeditem);

            else

                alert("Please select any options.");

        }

    &lt;/script&gt;

**Configure Style**

1. Add the following styles.



**[CSS]**

&lt;style&gt;

        .frame

        {

            width: 80%;

        }

    &lt;/style&gt;



Execute the above code example to render the following output.

{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img11.png" Caption="Figure 11: RegistrationApp"%}

The below screenshot displays your selection when clicking submit button.



{% include image.html url="\js\RadioButton\getting-started_images\getting-started_img12.png" Caption="Figure 12: Output"%}

