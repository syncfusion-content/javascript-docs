---
layout: post
title: How to section in Dialog widget for Essential JS? 
description: How to achieve specific requirements in Dialog widget for Essential JS
platform: js
control: Dialog
documentation: ug
keywords : ejdialog, js dialog, jquery dialog, dialog, dialog ui, web dialog, ej dialog, essential javascript dialog, dialog widget,
api: /api/js/ejdialog
---
# How To?


## Create Multiple Dialogs

Essential JS library supports multiple Dialog widgets in the same web page with different contents at different position using [position](https://help.syncfusion.com/api/js/ejdialog#members:position) property and different functionalities.

Initialize the Dialog widgets by adding the script section as below.

{% highlight html %}


    <!--dialog 1-->
    <div id="dialog1" title="Dialog">
        <p>
            This is a simple dialog
        </p>
    </div>
    <!--dialog 2-->
    <div id="dialog2" title="Window">
        <p>
            This is a different dialog
        </p>
    </div>
    <!--dialog 3-->
    <div id="dialog3" title="PopUp">
        <p>
            This is an another dialog
        </p>
    </div>

    <script>
        $(function () {
            $("#dialog1").ejDialog({
                width: 250,
                position: {
                    X: 20,
                    Y: 20
                }
            });
            $("#dialog2").ejDialog({
                width: 250,
                position: {
                    X: 300,
                    Y: 20
                }
            });
            $("#dialog3").ejDialog({
                width: 250,
                position: {
                    X: 150,
                    Y: 150
                }
            });
        });
    </script>


{% endhighlight %}



N>If the position of the dialog is not set as above, all the three dialogs will be overlapped with each other.
{%seealso%}[position](https://help.syncfusion.com/api/js/ejdialog#members:position){%endseealso%}

![Create Multiple Dialogs](how-to_images\create-multiple-dialogs_img1.png)

## Create Nested Dialog

A Dialog widget can be nested within another Dialog widget.

Create a div element to render the child Dialog widget and use it as a content of parent Dialog widget.

{% highlight html %}

     <!—button to open the dialog-->
     <button id="button1">Open Dialog</button>    
     <div id="dialog">
        <!— button to open the nested dialog -->
        <button id="button2" class="ejButton">Open Nested Dialog</button>
        <!—nested dialog-->
        <div id="nestedDialog">
                This is a nested Dialog
         </div>
      </div>


{% endhighlight %}

Initialize both the Dialog widgets by adding the script section as below.

{% highlight javascript %}


        $(function () {
            $("#button1").ejButton({ click: "openDialog" });
            $("#button2").ejButton({ click: "openNestedDialog" });

            $("#dialog").ejDialog({
                title: "Dialog",
                showOnInit: false,
                width: 500, height: 400,
                actionButtons: ["close", "collapsible", "maximize", "minimize", "pin"]
            });
            $("#nestedDialog").ejDialog({
                title: "Nested Dialog",
                showOnInit: false,
                width: 300, height: 200
            });
        });

        function openDialog(args) {
            $("#dialog").ejDialog("open");
        }
        function openNestedDialog(args) {
            $("#nestedDialog").ejDialog("open");
        }   



{% endhighlight %}



## Create Confirmation Dialog with Footer option.

Essential JS library supports Alert Dialog widgets.

Using [showFooter](https://help.syncfusion.com/api/js/ejdialog#members:showfooter) property to render Alert Dialog with Footers in Dialog widget.

Initialize the Dialog widget using the below code.

{% highlight html %}

    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <input class="e-btn" id="btnOpen" value="Click to open dialog" />
                <div class="control">
                    <div id="basicDialog" title="Confirmation Dialog">
                        Do you really leave the session?
                    </div>
                </div>
            </div>
        </div>
    </div>

{% endhighlight %}

Initialize Footer in Dialog widgets by adding the script section in JsRender as below.

{% highlight javascript %}

    <script id="sample" type="text/x-jsrender">
    <div class="footerspan" style="float:right">
      <button id='btn1'>OK</button>
      <button id='btn2'>Cancel</button>
    </div>
    <div class="condition" style="float:left; margin-left:15px">
    <input type="check" id="check1"></div>
    </script>
   

{% endhighlight %}

Add the below script to render the Dialog widget and map the render template Id into the footer content using [footerTemplateId](https://help.syncfusion.com/api/js/ejdialog#members:footertemplateid) property.

{% highlight javascript %}
	
        $(window).load(function () {
            // declaration
            $("#basicDialog").ejDialog({               
                close: "onDialogClose",
                target: ".control",
                showFooter: true,
                footerTemplateId: "sample"
            });
			$("#check1").ejCheckBox({text:"Don't ask me this again"})
            $("#btnOpen").ejButton({ size: "medium", click: "onOpen", type: "button", height: 30, width: 150 });           
			$("#btn1").ejButton({ size:"mini",height: 30, width: 70});
			$("#btn2").ejButton({ size:"mini",height: 30, width: 70});
        });
       
        function onDialogClose(args) {
            $("#btnOpen").show();
        }
        function onOpen() {
            $("#btnOpen").hide();
            $("#basicDialog").ejDialog("open");
        }
    </script>

{% endhighlight %}

![Create Alert Dialog](how-to_images\dialog-footer1.png)