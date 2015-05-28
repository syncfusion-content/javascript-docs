---
layout: post
title: getting-started
description: getting started
platform: js
control: Checkbox
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Checkbox** in your application with **JavaScript** and **ASP.NET MVC**.

## Create your first Checkbox in JavaScript

**Essential JavaScript Checkbox** provides support for multiple selections, within your webpage and allows you to specify an option from the list. From the following guidelines, you can select Multiple or Single Selection List Receiving App using **Checkbox**. The following screenshot demonstrates the functionality with **Checkbox** button action.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img1.png" Caption="Figure 1: Checkbox Control"%}

In the above screenshot, you can select Hobbies, Interests list and Social networks Receiving App using **Checkbox**, **Tri-state****Checkbox** and perform the action to render the checked values when the button is clicked.

### Create a Checkbox 



**Essential JavaScript****Checkbox** widget has built-in features like intermediate selections. You can easily create the **Checkbox** widget by using a simple input **Checkbox** element as follows.

* Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
<title>Getting Started Essential JS</title>
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- Add checkbox element here -->
</body>
</html>


{% endhighlight %}



Add input element to render the **Checkbox.**

![](getting-started_images\getting-started_img2.png)

{% highlight html %}

<div class="frame">           

     Hobbies <br /><br />
     <table>
     <tr>
         <td class="chkrad">
             <input type="checkbox"  id="check1" value="Music" />
             <label for="check1"  >Music</label></td>
         <td class="chkrad">
             <input type="checkbox"  id="Checkbox3"value= "Sports" />
             <label for="Checkbox3"  >Sports</label></td>
         <td class="chkrad">
             <input type="checkbox"  id="Checkbox4" value="Bike riding" />
             <label for="Checkbox4"  class="clslab">Bike Riding</label></td>
     </tr>
     </table><br /><br />
     Favorite Search Engines<br /><br />
     <table>
     <tr>
        <td class="chkrad">
             <input type="checkbox" id="Checkbox1" value="playing Games" />
             <label for="Checkbox1"  >Playing Games</label>
        </td>
        <td class="chkrad">
             <input type="checkbox" id="Checkbox5" value="Hearing Songs" />
             <label for="Checkbox5"  >Hearing Songs</label>
        </td>
        <td class="chkrad">
             <input type="checkbox" id="Checkbox6" value="Watching tv"/>
             <label  for="Checkbox6" >Watching Tv</label>
</td>
          </tr>
        </table><br /><br />
        Media Player<br /><br />
        <table>
        <tr>
        <td class="chkrad">
              <input type="checkbox" id="Checkbox2" value="Video" />
              <label for="Checkbox2" >Video</label>
        </td>
        <td class="chkrad">
              <input type="checkbox" id="Checkbox7" value="Audio" />
              <label for="Checkbox7" >Audio</label>
          </td>
          <td class="chkrad">
              <input type="checkbox" id="Checkbox8" value="Picture" />
              <label for="Checkbox8">Picture</label>
          </td>
           </tr>
            </table><br />
<td class="btnsht">
<button id="button11">SUBMIT</button>
</td>
</div>


{% endhighlight %}



Add the following styles to show the **Checkbox** control in an order.



{% highlight css %}

 <style>

  .frame
    {
     width: 80%;
    }
.chkrad 
    {
     width: 150px;
    }

</style>


{% endhighlight %}



Initialize **Checkbox** in script.



{% highlight js %}

<script type="text/javascript">
   $(function () {
       // declaration
       // simple checkbox creation
       $("#check1").ejCheckBox({ checked:true });
       $("#Checkbox3").ejCheckBox();
       $("#Checkbox4").ejCheckBox();
       $("#Checkbox3").ejCheckBox();
       $("#Checkbox1").ejCheckBox({ size: "medium", checked: true });
       $("#Checkbox5").ejCheckBox({ size: "medium" });
       $("#Checkbox6").ejCheckBox({ size: "medium" });
       $("#Checkbox2").ejCheckBox({ size: "medium", enableTriState: true, checkState:"indeterminate" });
       $("#Checkbox7").ejCheckBox({ size: "medium", enableTriState: true, checkState:"indeterminate"  });
       $("#Checkbox8").ejCheckBox({ size: "medium", enableTriState: true });

       $("#button11").ejButton({
           size: "normal",
           width:"60px",
           showRoundedCorner: true,

       });
   });
$(document).ready(function () {      //Document ready
    $("button").click(function () {      

         var checkeditem = [];    

           $("input[type=checkbox]").each(function () {

               if ($("#" + $(this)[0].id).ejCheckBox("option", "checked"))

                   checkeditem.push($(this).val());
        });

        alert(checkeditem);
});
});
</script>


{% endhighlight %}



The following screenshot displays a **Checkbox** control.

.

{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img3.png" Caption="Figure 2: Checkbox Creation"%}

### File Selection in Media Player

You can get the file type of Media player applications such as video, audio and picture using **Checkbox.** Follow the given steps to get media player file types.

* Add the following code in the **&lt;body&gt;** element of the corresponding view page.



{% highlight html %}

<div class="frame">
        Audio <br /><br />
        <table>
            <tr>
                <td >
                    <input type="checkbox"  id="Checkbox1" value="Mp3" />
                    <label for="Checkbox1"  >*.Mp3</label></td>
                <td >
                    <input type="checkbox"  id="Checkbox2"value= "Wav" />
                    <label for="Checkbox2"  >*.Wav</label></td>
            </tr>
        </table>
        <br /><br />
        Video<br /><br />
        <table>
            <tr>
                <td >
                    <input type="checkbox" id="Checkbox3" value="Avi" />
                    <label for="Checkbox3"  >*.Avi</label>
                </td>
                <td >
                    <input type="checkbox" id="Checkbox4" value="MP4" />
                    <label for="Checkbox4"  >*.MP4</label>
                </td>
            </tr>
        </table><br /><br />
        Picture<br /><br />
        <table>
            <tr>
            <td >
                <input type="checkbox" id="Checkbox5" value="PNG" />
                <label for="Checkbox5" >*.PNG</label>
            </td>
            <td >
                <input type="checkbox" id="Checkbox6" value="JPG" />
                <label for="Checkbox6" >*.JPG</label>
            </td>
        </table>
        <br />
        <td>
            <button id="button11">SUBMIT</button>
        </td>
    </div>


{% endhighlight %}



 Initialize **Checkbox** in the script.



{% highlight js %}

<script type="text/javascript">
    $(function () {
               $("#Checkbox1").ejCheckBox();
$("#Checkbox2").ejCheckBox();
               $("#Checkbox3").ejCheckBox();
               $("#Checkbox4").ejCheckBox();
               $("#Checkbox5").ejCheckBox();
               $("#Checkbox6").ejCheckBox();

$("#button11").ejButton({
                size: "normal",
width:"60px",
                showRoundedCorner: true,
               });
});
$(document).ready(function () {

$("button").click(function () {

					var checkeditem = []; 
                                                            $("input[type=checkbox]").each(function () {

           if ($("#" + $(this)[0].id).ejCheckBox("option", "checked"))

                   checkeditem.push($(this).val());

                   });

alert(checkeditem);

});

});
    </script>


{% endhighlight %}



Execute the code to render the resultant output.

{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img4.png" Caption="Figure 3: File selection in Media player"%}

## Create your first Checkbox in MVC

**ASP.NET MVC Checkbox** provides support to multiple selections within your webpage, and allows you to select options from the list. Refer the following guidelines to create multiple or single selection List Receiving App using **Checkbox** that helps you to get the value of checked **Checkbox** using the button. The following screenshot illustrates the functionality of **Checkbox** with button action.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img5.png" Caption="Figure 4: Checkboxes Control"%}

In the above screenshot, you can select hobbies, interest list and social networks receiving app using **Checkbox**. The **Checkbox** performs the action to render the checked values when button clicked.

**Create a Checkbox**

**ASP.NET MVC Checkbox** widget has built-in features like multiple selections. You can easily create the **Checkbox** widget using simple **HTML** helper “@Html.EJ().CheckBox()” as follows.

* You can create an**MVC** Project and add necessary assemblies, styles and scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

Add the following code to the corresponding view page to render **Checkbox.**



&lt;div class="frame"&gt;

        &lt;div class="control"&gt;

            &lt;div class="chkalign"&gt;

               <h1>Hobbies</h1> 

               &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td class="chkrad"&gt;                           @Html.EJ().CheckBox("check1").Value("Music")

                            &lt;label for="check1" class="clslab"&gt;

                                Music

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td class="chkrad"&gt;                            @Html.EJ().CheckBox("Checkbox3").Value("Sports")

                            &lt;label for="Checkbox3" class="clslab"&gt;

                                Sports

                            &lt;/label&gt;

                        &lt;/td&gt;

                        &lt;td class="chkrad"&gt;

                            @Html.EJ().CheckBox("Checkbox4").Value("Bike Riding")

                            &lt;label for="Checkbox4" class="clslab"&gt;

                                Bike Riding

                            &lt;/label&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                <h1>Interest List</h1>

                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td class="chkrad"&gt;

                            @Html.EJ().CheckBox("Checkbox1").Value("Playing Games").Size(Size.Medium)

<label for="Checkbox1" class="clslab">Playing Games</label>

                        &lt;/td&gt;

                        &lt;td class="chkrad"&gt;

                            @Html.EJ().CheckBox("Checkbox5").Value("Hearing Songs").Size(Size.Medium)

<label for="Checkbox5" class="clslab">Hearing Songs</label>

                        &lt;/td&gt;

                        &lt;td class="chkrad"&gt;

                            @Html.EJ().CheckBox("Checkbox6").Value("Reading Books").Size(Size.Medium)

<label for="Checkbox6" class="clslab">Reading Books</label>

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



Add the following styles to the corresponding view page to show the **Checkbox** in horizontal order.



&lt;style&gt;

    td {

        float: left;

    }

    label

    {

        float: right; margin:5px 10px;

    }

&lt;/style&gt;



Run the above code to render the following output.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img6.png" Caption="Figure 5: Checkbox Creation"%}

**Create a Tri-State Checkbox**

**ASP.NET MVC Tri-State Checkbox** widget renders by setting **enableTriState** property to **True**. You can add the following code to create **Tri-state Checkbox** in the **&lt;div&gt;** element of the corresponding view page.



<h1>Social networks</h1>

&lt;table&gt;

    &lt;tr&gt;

        &lt;td class="chkrad"&gt;            @Html.EJ().CheckBox("Checkbox2").Value("Facebook").Size(Size.Medium).EnableTriState(true).CheckState(CheckState.Indeterminate) <label for="Checkbox2" class="clslab">Facebook</label>

        &lt;/td&gt;

        &lt;td class="chkrad"&gt;            @Html.EJ().CheckBox("Checkbox7").Value("GPlus").Size(Size.Medium).EnableTriState(true).CheckState(CheckState.Uncheck) <label for="Checkbox7" class="clslab">GPlus</label>

        &lt;/td&gt;

        &lt;td class="chkrad"&gt;            @Html.EJ().CheckBox("Checkbox8").Value("Twitter").Size(Size.Medium).EnableTriState(true).CheckState(CheckState.Check) <label for="Checkbox8" class="clslab">Twitter</label>

        &lt;/td&gt;

    &lt;/tr&gt;

&lt;/table&gt;



Run the above code to render the following output.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img7.png" Caption="Figure 6: Tri-state Checkbox Creation"%}

**Receive Hobbies and Interest**

You can receive the **Hobbies** and **Interest** values using **Checkbox**. You can create a button in your corresponding view page **&lt;div&gt;** element using @Html.EJ().Button() and add the script section to the view page. The following steps illustrate how to create and set action to the button.

*  Add the following code for Button creation.





@Html.EJ().Button("buttonnormal").Text("Submit").Size(ButtonSize.Normal)



* Add the script into your view page.



&lt;script&gt;

    $(document).ready(function () {

        $("button").click(function () {

            var checkeditem = [];                                               



          $(".e-checkbox").each(function () {



             if ($("#" + $(this)[0].id).ejCheckBox("option", "checked"))



                 checkeditem.push($("#" + $(this)[0].id).ejCheckBox("option","value"));



                });



            alert(checkeditem);        });

    });

&lt;/script&gt;



* Execute the above code example to render the following output.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img8.png" Caption="Figure 7: Receive hobbies and interest"%}

**Receive Media Player**

You can get the **Media Player** file type application like video, audio and picture using **Checkbox**. You can refer the following steps to render **Media Player** file types.

1. Add the following code in **&lt;div&gt;** element of the corresponding view page.



&lt;table&gt;

    &lt;tr&gt;

        &lt;th class="chkrad"&gt;

         @Html.EJ().CheckBox("Checkboxs1").Value(".mp3")

            &lt;label for="check2" class="clslab"&gt;

                Audio

            &lt;/label&gt;

        &lt;/th&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="chkrad"&gt;

            @Html.EJ().CheckBox("Checkboxs3").Value(".mp3")

            &lt;label for="Checkboxs3" class="clslab"&gt;

                .mp3

            &lt;/label&gt;

        &lt;/td&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="chkrad"&gt;

            @Html.EJ().CheckBox("Checkboxs4").Value(".avi")

            &lt;label for="Checkboxs4" class="clslab"&gt;

                .avi

            &lt;/label&gt;

        &lt;/td&gt;

    &lt;/tr&gt;

&lt;/table&gt;

&lt;table&gt;

    &lt;tr&gt;

        &lt;th class="chkrad"&gt;

            @Html.EJ().CheckBox("Checkboxs2").Value(".mp3").Size(Size.Medium)



            <label for="Checkboxs1" class="clslab">Video</label>

        &lt;/th&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="chkrad"&gt;            @Html.EJ().CheckBox("Checkboxs5").Value(".mp4").Size(Size.Medium)

            &lt;label for="Checkboxs5" class="clslab"&gt;.mp4</label>

        &lt;/td&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="chkrad"&gt;

            @Html.EJ().CheckBox("Checkboxs6").Value(".wave").Size(Size.Medium)

            &lt;label for="Checkboxs6" class="clslab"&gt;.wave</label>

        &lt;/td&gt;

    &lt;/tr&gt;

&lt;/table&gt;



        2. Execute the above code to render the following output.	



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img9.png" Caption="Figure 8: Receive Media player"%}

## Create your first Checkbox in ASP.NET

**ASP.NET Checkbox** provides support for multiple selections, within your webpage and allows you to specify an option from the list. From the following guidelines, you can select Multiple or Single Selection List Receiving App using **Checkbox**. The following screenshot demonstrates the functionality with **Checkbox** button action.



![C:\Users\jeganprakash\Desktop\Documentation\Images\Check\1.PNG](getting-started_images\getting-started_img10.png)

_Figure_ _9__: Checkbox Control_

In the above screenshot, you can select Hobbies, Interests list and Social networks Receiving App using **Checkbox**, **Tri-state****Checkbox** and perform the action to render the checked values when the button is clicked.

**Create a Checkbox** 

**ASP.NET****Checkbox** widget has built-in features like intermediate selections. You can easily create the **Checkbox** widget by using a simple input **Checkbox** element as follows.

* You can create an **ASP.NET** Project and add necessary assemblies, styles and scripts with the help of the given [ASP.NET-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

Create an **ASPX** file and add **ejCheckBox** element to render the **Checkbox.**



[ASPX]

&lt;div class="frame"&gt;

        Hobbies

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox1" runat="server" Value="Music"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox1"&gt;

                        Music</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox3" runat="server" Value="Sports"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox3"&gt;

                        Sports</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox4" runat="server" Value="Bike riding"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox4" class="clslab"&gt;

                        Bike Riding</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        Favorite Search Engines<br />

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox9" runat="server" Value="Playing Games"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox9"&gt;

                        Playing Games</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox5" runat="server" Value="Hearing Songs"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox5"&gt;

                        Hearing Songs</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox6" runat="server" Value="Watching tv"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox6"&gt;

                        Watching Tv</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        Media Player<br />

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox2" runat="server" Value="Video" EnableTriState="true"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox2"&gt;

                        Video</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox7" runat="server" Value="Audio" EnableTriState="true"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox7"&gt;

                        Audio</label>

                &lt;/td&gt;

                &lt;td class="chkrad"&gt;

                    &lt;ej:CheckBox ID="Checkbox8" runat="server" Value="Picture" EnableTriState="true"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox8"&gt;

                        Picture</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td class="btnsht"&gt;

                    <ej:Button ID="Button" runat="server" Text="SUBMIT" Type="Button"

ClientSideOnClick="click" ShowRoundedCorner="true">

                    &lt;/ej:Button&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



Add the following styles to show the **Checkbox** control in an order.



[CSS]

&lt;style&gt;

        .frame

        {

            width: 600px;

            padding: 20px;

            border: 1px solid gray;

        }

        .chkrad

        {

            font-weight: bold;

            width: 200px;

        }

    &lt;/style&gt;





Add the script into your **ASPX** page.



[Script]

&lt;script type="text/javascript"&gt;

        function click() {

            var checkeditem = "";

            $(".e-checkbox").each(function (index, args) {

                if ($(this).data('ejCheckBox').isChecked) {

                    checkeditem += $(this).data('ejCheckBox').model.value;

                }

            });

            alert("Checked items are -"+checkeditem);

        }

    &lt;/script&gt;



![C:\Users\jeganprakash\Desktop\Documentation\Images\Check\2.PNG](getting-started_images\getting-started_img11.png)

_Figure_ _10__:_ _Checkbox Creation_

**File Selection in Media Player**

You can get the file type of Media player applications such as video, audio and picture using **Checkbox.** Follow the given steps to get media player file types.

* Add the following code in the **&lt;body&gt;** element of the corresponding **ASPX** page.



[ASPX]

    &lt;div class="frame"&gt;

        Audio

        &lt;br /&gt;

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox1" runat="server" Value="Mp3"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox1"&gt;

                        *.Mp3</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox2" runat="server" Value="Wav"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox2"&gt;

                        *.Wav</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        Video<br />

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox3" runat="server" Value="Avi"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox3"&gt;

                        *.Avi</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox4" runat="server" Value="MP4"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox4"&gt;

                        *.MP4</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;br /&gt;

        Picture<br />

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox5" runat="server" Value="PNG"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox5"&gt;

                        *.PNG</label>

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:CheckBox ID="Checkbox6" runat="server" Value="JPG"&gt;

                    &lt;/ej:CheckBox&gt;

                    &lt;label for="Checkbox6"&gt;

                        *.JPG</label>

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    <ej:Button ID="Button" runat="server" Text="SUBMIT" Type="Button"

ClientSideOnClick="click" ShowRoundedCorner="true">

                    &lt;/ej:Button&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



 Add the script into your **ASPX** page.



[Script]

    &lt;script type="text/javascript"&gt;

        function click() {

                var checkeditem = "";

                $(".e-checkbox").each(function (index, args) {

                    if ($(this).data('ejCheckBox').isChecked) {

                        checkeditem += $(this).data('ejCheckBox').model.value;

                    }

                });

                alert("Checked Items are -"+checkeditem);

            }   

    &lt;/script&gt;



Add the following styles to show the **Checkbox** control in an order.



 [CSS]

&lt;style&gt;

        .frame

        {

            padding: 20px;

            background: #f1efef;

        }

    &lt;/style&gt;



Execute the code to render the resultant output.



{% include image.html url="\js\Checkbox\getting-started_images\getting-started_img12.png" Caption="Figure 11: File selection in Media player"%}

