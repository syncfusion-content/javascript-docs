---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Checkbox
documentation: ug
api : /api/js/ejcheckbox
---

# Getting Started

This section explains briefly about how to create a **Checkbox** in your application with **JavaScript**.**Essential JavaScript Checkbox** provides support for multiple selections, within your web page and allows you to specify an option from the list. From the following guidelines, you can select Multiple or Single Selection List Receiving App using **Checkbox**. The following screenshot demonstrates the functionality with Checkbox button action.



![](/js/Checkbox/Getting-Started_images/Getting-Started_img1.png) 

In the above screenshot, you can select Hobbies, Interests list and Social networks Receiving App using Checkbox, **Tri-state** **Checkbox** and perform the action to render the checked values when the button is clicked.

## Create a Checkbox 

**Essential JavaScript** **Checkbox** widget has built-in features like intermediate selections. You can easily create the Checkbox widget by using a simple input Checkbox element as follows.

Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
      <title>Getting Started Essential JS</title>
      <!-- Style sheet for default theme (flat azure) -->
      <lin khref="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"rel="stylesheet"/>
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add checkbox element here -->
   </body>
</html>

{% endhighlight %}

Add input element to render the **Checkbox.**


{% highlight html %}

<div class="frame">
    Hobbies <br /><br />
    <table>
        <tr>
            <td class="checkbox">
                <input type="checkbox" id="check1" value="Music" />
                <label for="check1">Music</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox3" value="Sports" />
                <label for="Checkbox3">Sports</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox4" value="Bike riding" />
                <label for="Checkbox4" class="clslab">Bike Riding</label>
            </td>
        </tr>
    </table><br /><br />
    Favorite Search Engines<br /><br />
    <table>
        <tr>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox1" value="playing Games" />
                <label for="Checkbox1">Playing Games</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox5" value="Hearing Songs" />
                <label for="Checkbox5">Hearing Songs</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox6" value="Watching TV" />
                <label for="Checkbox6">Watching TV</label>
            </td>
        </tr>
    </table><br /><br />
    Media Player<br /><br />
    <table>
        <tr>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox2" value="Video" />
                <label for="Checkbox2">Video</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox7" value="Audio" />
                <label for="Checkbox7">Audio</label>
            </td>
            <td class="checkbox">
                <input type="checkbox" id="Checkbox8" value="Picture" />
                <label for="Checkbox8">Picture</label>
            </td>
        </tr>
    </table>
   <br />
   <div>
      <button id="button11">SUBMIT</button>
   </div>
</div>


{% endhighlight %}



Add the following styles to show the **Checkbox** control in an order.



{% highlight css %}

 <style>

  .frame
    {
        width: 80%;
    }
    .checkbox 
    {
        width: 150px;
    }

</style>


{% endhighlight %}



Initialize **Checkbox** in script.



{% highlight javascript %}

    
    // Simple checkbox creation    
    $(function () {
        // declaration
        $("#check1").ejCheckBox({ checked:true });
        $("#Checkbox3").ejCheckBox();
        $("#Checkbox4").ejCheckBox();
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
    $(document).ready(function () {      //Document ready
        $("button").click(function () {
             var checkedItem = [];               
             $("input[type=checkbox]").each(function () {
                 if ($("#" + $(this)[0].id).ejCheckBox("option", "checked"))
                    checkedItem.push($(this).val());
              });
              alert(checkedItem);
         });
     });


{% endhighlight %}



The following screenshot displays a **Checkbox** control.


![](/js/Checkbox/Getting-Started_images/Getting-Started_img3.png) 

## File Selection in Media Player

You can get the file type of Media player applications such as video, audio and picture using **Checkbox.** Follow the given steps to get media player file types.

Add the following code in the **&lt;body&gt;** element of the corresponding view page.



{% highlight html %}

  <div class="frame">
   Audio <br /><br />
   <table>
      <tr>
         <td >
            <input type="checkbox"  id="Checkbox1" value="Mp3" />
            <label for="Checkbox1"  >*.Mp3</label>
         </td>
         <td >
            <input type="checkbox"  id="Checkbox2"value= "WAV" />
            <label for="Checkbox2"  >*.WAV</label>
         </td>
      </tr>
   </table>
   <br /><br />
   Video<br /><br />
   <table>
      <tr>
         <td >
            <input type="checkbox" id="Checkbox3" value="AVI" />
            <label for="Checkbox3"  >*.AVI</label>
         </td>
         <td >
            <input type="checkbox" id="Checkbox4" value="MP4" />
            <label for="Checkbox4"  >*.MP4</label>
         </td>
      </tr>
   </table>
   <br /><br />
   Picture<br /><br />
   <table>
      <tr>
         <td>
            <input type="checkbox" id="Checkbox5" value="PNG" />
            <label for="Checkbox5" >*.PNG</label>
         </td>
         <td>
            <input type="checkbox" id="Checkbox6" value="JPG" />
            <label for="Checkbox6" >*.JPG</label>
         </td>
       </tr>
   </table>
   <br />
   <div>
      <button id="button11">SUBMIT</button>
   </div>
</div>


{% endhighlight %}



 Initialize **Checkbox** in the script.



{% highlight javascript %}

    // Simple checkbox creation  
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
    	    var checkedItem = []; 
            $("input[type=checkbox]").each(function () {
                 if ($("#" + $(this)[0].id).ejCheckBox("option", "checked"))
                    checkedItem.push($(this).val());
             });
             alert(checkedItem);
       });
    });


{% endhighlight %}


Execute the code to render the resultant output.

![](/js/Checkbox/Getting-Started_images/Getting-Started_img4.png) 

