---
layout: post
title: How-To
description: how to
platform: js
control: Dialog
documentation: ug
---
# How To?


## Create Multiple Dialogs

Essential JS library supports multiple Dialog widgets in the same web page with different contents and different functionalities.

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
{%seealso%}[position](http://help.syncfusion.com/js/api/ejdialog#members:position){%endseealso%}

![Create Multiple Dialogs](how-to_images\create-multiple-dialogs_img1.png)

### Create Nested Dialog

A Dialog widget can be nested within another Dialog widget.

Create a div element to render the child Dialog widget and use it as a content of parent Dialog widget.

{% highlight html %}

     <!—button to open the dialog-->
     <button id="button1">Open Dialog</button>    
     <div id="dialog">
        <!— button to open the nested dialog -->
        <button id="button2" class="ejButton">Open Nested Dialog</button>
        <!—nested dialog-->
        <div id="nesteddialog">
                This is a nested Dialog
         </div>
      </div>


{% endhighlight %}

Initialize both the Dialog widgets by adding the script section as below.

{% highlight js %}


        $(function () {
            $("#button1").ejButton({ click: "openDialog" });
            $("#button2").ejButton({ click: "openNestedDialog" });

            $("#dialog").ejDialog({
                title: "Dialog",
                showOnInit: false,
                width: 500, height: 400,
                actionButtons: ["close", "collapsible", "maximize", "minimize", "pin"]
            });
            $("#nesteddialog").ejDialog({
                title: "Nested Dialog",
                showOnInit: false,
                width: 300, height: 200
            });
        });

        function openDialog(args) {
            $("#dialog").ejDialog("open");
        }
        function openNestedDialog(args) {
            $("#nesteddialog").ejDialog("open");
        }   



{% endhighlight %}