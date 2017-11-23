---
layout: post
title: How to - ProgressBar widget for Syncfusion Essential JS
description: How To Section in ProgressBar widget for Syncfusion Essential JS
platform: js
control: ProgressBar
documentation: ug
keywords: ProgressBar, events, 
api: /api/js/ejprogressbar
---

# How To

## How to increment & show the progressbar movement

You can increment the progress percentage and show case the movement by using the below code with the help of [change](https://help.syncfusion.com/api/js/ejprogressbar#events:change), [complete](https://help.syncfusion.com/api/js/ejprogressbar#events:complete) and [start](https://help.syncfusion.com/api/js/ejprogressbar#events:start) events.

{% highlight html %}

        <div class="frame">
            <div class="control">
                <div id="progressBar"></div>
            </div>
            <div class="startButton">
                <input type="checkbox" id="startButton" />
                 <label for="startButton">Toggle</label>
            </div>
        </div>  
         <div class="cols-prop-area event-tracer">
                    <div class="heading">
                        <span>Event Trace</span>
                        <div class="pull-right">
                            <select name="selectevtprops" id="selectControls">
                                <option value="start">start</option>
                                <option value="complete">complete</option>
                                <option value="change">change</option>
                            </select>
                        </div>
                    </div>
					<div class="prop-grid content">
						<div class="eventarea">
							<div class="EventLog" id="EventLog">
							</div>
						</div>
						<div class="evtbtn">
							<input type="button" class="eventclear e-btn" value="Clear" onclick="onClear()" />
						</div>
					</div>    
            </div> 
     
{% endhighlight %}

{% highlight javascript %}

       var progressObj, buttonObj, k = 10, timer = window.clearInterval(timer),showComplete=true ;
        $(function () {
            // declaration
            $("#progressBar").ejProgressBar({
                height: 22,
                value: 10,
                start: "onStart",
                change: "onChange",
                complete: "completed"
            });
            progressObj = $("#progressBar").data("ejProgressBar");
            progressObj.option("text", progressObj.getPercentage() + " %");

            $("#startButton").ejToggleButton({
                defaultText: "Start",
                activeText: "Pause",
                size: "small",
                click: "startProcess"
            });
            buttonObj = $("#startButton").data("ejToggleButton");

            $("#selectControls").ejDropDownList({
                popupShown: "adjustPopUpPosition",
                showCheckbox: true,
                checkAll: true,
                change: "propCheckEvent"
            });
        });

        function propCheckEvent(args) {
            if (args.isChecked) {
                switch (args.value) {
                    case "start": progressObj.option(args.value, "onStart"); break;
                    case "change": progressObj.option(args.value, "onChange"); break;
                    case "complete": showComplete=true; break;
                }
            }
            else if(args.value=="complete") 
			{             
                 showComplete=false; 
            }
            else
			   progressObj.option(args.value, null)            
        }

        function startProcess(args) {
            if (args.isChecked) 
                timer = window.setInterval(draw, 100);
            else {
                buttonObj.setModel({ "defaultText": "Start" });
                timer = window.clearInterval(timer);
            }
        }
        function draw() {
            progressObj.option("text", ++k + " %");
            progressObj.option("percentage", k);
        }
        function completed(args) {
            progressObj.option("text", "Completed");
            timer = window.clearInterval(timer);
            k = 0;
            if(showComplete)
            onComplete(args);
            buttonObj.setModel({ "toggleState": false, "defaultText": "Restart" });
        }

        function onComplete(args) {
                jQuery.addEventLog("The process has been <span class='eventTitle'>completed</span> successfully.</br>");
        }
        function onStart(args) {
            jQuery.addEventLog("Progressbar has been <span class='eventTitle'>started</span>.</br>");
        }
        function onChange(args) {
            jQuery.addEventLog("Progressbar value has been <span class='eventTitle'>changed</span> to " + args.percentage + "%.</br>");
        }
        function onClear() {
            $("#EventLog").html("");
        }
    
 
{% endhighlight %}

{% highlight css %}

     <style type="text/css" class="cssStyles">
        .frame {
            border: 1px solid #BBBCBB;
            border-radius: 10px 10px 10px 10px;
            padding: 50px 60px;
            margin-top: 40px;
            width: 400px;
            }
       
        .txt {
           font-size: 20px;
           margin-top: 12px;
           text-align: center;
           }
        .startButton {
             margin-left: 155px;
           }
    </style>

{% endhighlight %}

The progress bar movement will be as shown below:

![](HowTo_images/HowTo_img1.jpeg)

![](HowTo_images/HowTo_img2.jpeg)