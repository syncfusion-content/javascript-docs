---
layout: post
title: Getting-Started
description: getting started
platform: js
control: RadioButton
documentation: ug
api: /api/js/ejradiobutton
---

# Getting Started

This section briefly describes you on how to create a QuizApp and RegistrationApp using Essential JavaScript RadioButton control and use the features available in it.**Essential JavaScript** **RadioButton** supports RTL, custom skins and events to display customized RadioButtons. In this example, you can learn how to use RadioButtons in a Quiz application. The following guidelines show you how to use the **RadioButton** to select the answers in the application and get the selected items. The following screenshot displays a sample Quiz application.


![](/js/RadioButton/Getting-Started_images/Getting-Started_img1.png) 

## Create a RadioButton in a Quiz Application

**Essential JavaScript RadioButton** is created by using a simple input textbox element as follows.

Create an HTML file and add the following template to the HTML file to create RadioButton.

{% highlight html %}

<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
     <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"rel="stylesheet"/>
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
    <body>
        <!-- Add RadioButton element here --> 
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
    <br/><br/><br/>
    2.  What is the Expansion for USB ?<br />
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
    <br/><br/><br/>
    3.   What is the Expansion for HTML ?<br />
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
    <br/><br/><center>
   <button id="submitid" onclick="button()">Submit</button></center>
</div>
   
{% endhighlight %}



Initializes the RadioButton in script.



{% highlight javascript %}


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
        var checkedItem = [];
        $(".e-radiobtn:checked").each(function () {
            checkedItem.push($(this).parent().siblings().html());
        });
        alert(checkedItem);
    }



{% endhighlight %}



 Add the following styles


{% highlight css %}

<style>
    html, body {
        width: 71%;
        margin: 0;
    }

    .frame {
        width: 80%;
    }
</style>


{% endhighlight %}


The following screenshot displays the output for the above code.



![](/js/RadioButton/Getting-Started_images/Getting-Started_img2.png) 

