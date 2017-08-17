---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: Slider
documentation: ug
api: /api/js/ejslider
---

# Getting Started 

This section explains briefly about how to create a **Slider** in your application with **JavaScript**.
**Essential JavaScript Slider** widget provides support to display a **Slider** within the web page. Here, you can learn how to use **Sliders** in a real-time application. The example shows you how to use the **Slider** control to select mobile model within the specified price range in a Mobile Purchase Application.

The following screenshot demonstrates the functionality of **Slider** control. By selecting mobile model in the dropdown, you can purchase a mobile at any rate specified in the **Mobile Price Slider**. In addition, you can also specify the number of mobiles you require by using the **Mobile** **Count** **Slider**. Simultaneously, you can observe the changes in the **Mobile Price** and **Count** using **Sliders**.



![](/js/Slider/Getting-Started_images/Getting-Started_img1.png) 

## Create a Slider

**Essential JavaScript Slider** widget allows you to switch between different ranges of input. The basic **Slider** is in horizontal position and has a single handle that is moved by the mouse or the arrow keys. 

Create an **HTML** file and add the following template to the **HTML** file. 



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add Mobile Purshase element element here  -->
</body>
</html>


{% endhighlight %}



Add input element to render a **Slider**.



{% highlight html %}

<div class="content-container-fluid">
   <div class="row">
      <div class="cols-sample-area">
         <div class="frame">
            <div id="priceheading">
               <h3>Mobile Purchase</h3>
               <input type="text" id="selectMobile" />
               <div id="mobileList">
                  <ul>
                     <li>Moto X</li>
                     <li>Moto g</li>
                     <li>Nexus</li>
                     <li>Xperia</li>
                     <li>Samsung</li>
                  </ul>
               </div>
            </div>
            <span class="column-left">
            <span class="price">Price</span>
            </span>
            <span class="column-right">
            <span id="priceText"> </span>
            <span class="value"></span>
            </span>
            <div id="priceSlider">
            </div>
            <span class="column-left">
            <span class="price">Count</span>
            </span>
            <span class="column-right">
            <span id="counttext"></span><span class="value"></span>
            </span>
            <div id="countSlider">
            </div>
            <div id="EventLog"></div>
         </div>
      </div>
   </div>
</div>

{% endhighlight %}



Add the following styles to show the **Mobile Rate Slider** widget in horizontal order.



{% highlight css %}

<style type="text/css" class="cssStyles">
    .frame {
        width: 230px;
        padding: 50px;
    }
    .price, .count {
        margin-top: 5px;
        font-weight: 400;
    }

    .value, #priceText, #counttext {
        float: right;
        position: relative;
        width: auto;
        padding-left: 3px;
    }
    #priceText, #counttext {
        width: auto;
    }
    #result {
        margin-top: 25px;
        text-align: center;
        font-weight: 600;
    }

    .frame .e-slider-wrap {
        display: block;
        margin-top: 40px;
    }

    .column-left {
        width: 35%;
        float: left;
        font-weight: 400;
        margin-top: 10px;
    }

    .column-right {
        width: 65%;
        float: right;
        font-weight: 600;
        margin-top: 14px;
    }

    #priceheading {
        font-family: 'Arial Black', Gadget, sans-serif;
        font-size: larger;
        padding-bottom: 15px;
    }
</style>



{% endhighlight %}



Initialize **Slider** using the following code example.



{% highlight javascript %}

        var priceObj, countObj, priceValue = 0,target;                
        $(function() {
            $('#selectMobile').ejDropDownList({
                targetID: "mobileList",
                width: "150px"
            });
            var priceValue = 25,
                interestValue = 4,
                priceValue = 1;
            $("#priceSlider").ejSlider({
                height: 16,
                value: priceValue,
                minValue: 10000,
                maxValue: 50000,
                incrementStep: 1,
                change: "onChange",
                slide: "onChange"
            });
            $("#countSlider").ejSlider({
                height: 16,
                value: priceValue,
                minValue: 1,
                maxValue: 20,
                incrementStep: 1,
                change: "onChange",
                slide: "onChange"
            });
            mobObj = $("#selectMobile").data('ejDropDownList');
            priceObj = $('#priceSlider').data('ejSlider');
            countObj = $('#countSlider').data('ejSlider');
            calculate();
        });
    
        function onChange(args) {
            this.wrapper.prev().children('span.value').html(args.value);
            calculate();
        }
    
        function calculate() {
            var price = priceObj.getValue();
            var mob = mobObj.getValue();
            var count = countObj.getValue();
            $('#EventLog').html("Mobile is " + mob + "  Price is  Rs" + price + "  Count is  " + count);
        }
            
{% endhighlight %}


The following screenshot displays a **Mobile Purchase** using **Slider**.

![](/js/Slider/Getting-Started_images/Getting-Started_img2.png) 



## Create EMI Calculator

Based on the loan amount, interest rate and tenure, you can calculate **EMI** amount using **Slider**.

Add input element to render a **Slider.**



{% highlight html %}

<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <div class="frame">
                <div id="loanheading">
                    Details of Loan
                </div>

                <span class="column-left">
                    <span class="loan">Loan Amount</span>
                </span>
                <span class="column-right">
                    <span class="value"></span><span id="loanText">Rs </span>
                </span>
                <div id="loanSlider">
                </div>

                <span class="column-left">
                    <span class="interest">Interest Rate</span>
                </span>
                <span class="column-right">
                    <span id="interestText">% pa</span><span class="value"></span>
                </span>
                <div id="interestSlider">
                </div>

                <span class="column-left">
                    <span class="tenure">Tenure</span>
                </span>
                <span class="column-right">
                    <span id="tenuretext">Years</span><span class="value"></span>
                </span>
                <div id="tenureSlider">
                </div>

                <div id="result">
                    Your Monthly EMI Amount is
                    <span id="EventLog"></span>
                </div>
            </div>
        </div>
    </div>
</div>



{% endhighlight %}



Add the following styles to show the **EMI Calculation Slider widget** in horizontal order.

{% highlight css %}

<style type="text/css" class="cssStyles">
    .frame {
        width: 400px;
    }

    .loan, .interest, .tenure {
        margin-top: 5px;
        font-weight: 400;
    }

    .value, #loanText, #interestText, #tenuretext {
        float: right;
        position: relative;
        width: auto;
        padding-left: 3px;
    }

    #loanText, #interestText, #tenuretext {
        width: auto;
    }

    #result {
        margin-top: 25px;
        text-align: center;
        font-weight: 600;
    }

    .frame .e-slider-wrap {
        display: block;
        margin-top: 40px;
    }

    .column-left {
        width: 35%;
        float: left;
        font-weight: 400;
        margin-top: 10px;
    }

    .column-right {
        width: 65%;
        float: right;
        font-weight: 600;
        margin-top: 14px;
    }

    #loanheading {
        font-family: 'Arial Black', Gadget, sans-serif;
        font-size: larger;
        padding-bottom: 15px;
    }
</style>  


{% endhighlight %}



Initialize **Slider** using the following code example.



{% highlight javascript %}

    var loanObj, interestObj, tenureObj, loanValue = 0,
    interestValue = 0,
    tenureValue = 0;
    $(function() {

        var loanValue = 25000,
            interestValue = 4,
            tenureValue = 3;
    
        $("#loanSlider").ejSlider({
            height: 16,
            value: loanValue,
            minValue: 10000,
            maxValue: 1000000,
            incrementStep: 10,
            change: "onChange",
            slide: "onChange"
        });
    
        $("#interestSlider").ejSlider({
            height: 16,
            value: interestValue,
            minValue: 1,
            maxValue: 20,
            incrementStep: 1,
            change: "onChange",
            slide: "onChange"
    
        });
        $("#tenureSlider").ejSlider({
            height: 16,
            value: tenureValue,
            minValue: 1,
            maxValue: 20,
            incrementStep: 1,
            change: "onChange",
            slide: "onChange"
    
        });
    
        loanObj = $('#loanSlider').data('ejSlider');
        interestObj = $('#interestSlider').data('ejSlider');
        tenureObj = $('#tenureSlider').data('ejSlider');
        calculate();
    });

    function onChange(args) {
        this.wrapper.prev().children('span.value').html(args.value);
        calculate();
    }
    
    function calculate() {
        var loan = loanObj.getValue(),
            interest = interestObj.getValue(),
            tenure = tenureObj.getValue();
    
        var P = loan;
        var y = interest / 1200;
        var tenureAmount = tenure * 12;
        //actual processing
        var top = y * (Math.pow((1 + y), tenureAmount));
        var bottom = (Math.pow((1 + y), tenureAmount)) - 1;
        var ans = top / bottom;
        var final = P * ans;
        var z = Math.round(final);
    
        $('#EventLog').html("Rs: " + z);
    }

{% endhighlight %}



The following screenshot displays a **EMI Calculation application** using **Slider.**

![](/js/Slider/Getting-Started_images/Getting-Started_img3.png) 

