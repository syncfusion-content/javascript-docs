---
layout: post
title: Client-Side-APIs
description: client-side-api’s
platform: js
control: Dialog
documentation: ug
---

# Client-Side-API’s

The **Dialog** Widget provides some Client side Methods to process the control from script side.

_Client side API for Dialog Table_

<table>
<tr>
<td>
<b>Methods</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
open</td><td>
This method allows you to open the Dialog widget</td></tr>
<tr>
<td>
close</td><td>
This method allows you to close the Dialog widget</td></tr>
<tr>
<td>
isOpened</td><td>
This method will check whether the Dialog widget is in open state or not and return the Boolean value</td></tr>
<tr>
<td>
destroy</td><td>
This method destroy the Dialog widget</td></tr>
</table>

## Open and Close

To open or close the **Dialog** widget by using client side API:

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. Render input button controls for performing open and close actions.

{% highlight html %}

**[HTML]**

     <div id="dialogAPI" title="Essential Grid">
        <p>
            Essential Grid for ASP.NET MVC is a <span>lightweight, AJAX-enabled, high-performance grid component</span> built especially to suit the programming model of the ASP.NET MVC framework.
        </p>
        <p>It has a rich feature set that includes <span>hierarchies, grouping, sorting, paging, data binding, editing, filtering, and several built-in styles.</span> </p>
        <p>Essential Grid is designed for performance and can easily handle millions of records. </p>
        <p>AJAX is extensively used to reduce traffic—only the required data is sent between the client and server, minimizing data transfer and response time.</p>
    </div>

    <input type="button" id="btnDialogOpen" class="e-btn" value="Dialog Open" />
    <input type="button" id="btnDialogClose" class="e-btn" value="Dialog Close" />


{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Set the width and height to the Dialog function and get the Dialog object. Call the open and close methods in the corresponding input button’s click event
   
   <script type="text/javascript">
        $("#dialogAPI").ejDialog({
            width: 500,
            height: 300
        });

        eDialog = $("#dialogAPI").data("ejDialog"); /* getting ejDialog object */

        $("#btnDialogOpen").ejButton({ "click": "onOpen", width: "95px" });
        $("#btnDialogClose").ejButton({ "click": "onClose", width: "95px" });

        function onOpen() {
            if (eDialog.model) 
                eDialog.open(); /* open the ejDialog widget */                       
        }

        function onClose() {
            eDialog.close(); /* close the ejDialog widget */
        }   
     </script>

{% endhighlight %}

2. The output of **Dialog** open is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Client-Side-APIs_images/Client-Side-APIs_img1.png" Caption=""%}

_Dialog is opened_

3. The output of Dialog close is as follows.                                     

{% include image.html url="/js/Dialog/Concepts-and-Features/Client-Side-APIs_images/Client-Side-APIs_img2.png" Caption=""%}

_Dialog is closed_                                                                     

## IsOpened and Destroy

To check the **Dialog** widget state by using client side API:

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. Render input button controls for performing open and close actions.



{% highlight html %}

**[HTML]**

    <div id="dialogAPI" title="Essential Grid">
        <p>
            Essential Grid for ASP.NET MVC is a <span>lightweight, AJAX-enabled, high-performance grid component</span> built especially to suit the programming model of the ASP.NET MVC framework.
        </p>
        <p>It has a rich feature set that includes <span>hierarchies, grouping, sorting, paging, data binding, editing, filtering, and several built-in styles.</span> </p>
        <p>Essential Grid is designed for performance and can easily handle millions of records. </p>
        <p>AJAX is extensively used to reduce traffic—only the required data is sent between the client and server, minimizing data transfer and response time.</p>
    </div>

    <input type="button" id="btnDialogOpen" class="e-btn" value="Dialog Open" />
    <input type="button" id="btnDialogClose" class="e-btn" value="Dialog Close" />
    <input type="button" id="btnDialogIsOpen" class="e-btn" value="Dialog IsOpen" />
    <input type="button" id="btnDialogDestroy" class="e-btn" value="Dialog Destroy" />
    <input type="button" id="btnDialogRestore" class="e-btn" value="Dialog Restore" />


{% endhighlight %}



2. Set the width and height to the **Dialog** function and get the **Dialog** object. Call the isOpened and destroy methods in the corresponding input button’s click event. 



{% highlight js %}

**[JavaScript]**

   <script type="text/javascript">
        $("#dialogAPI").ejDialog({
            width: 500,
            height: 300
        });

        eDialog = $("#dialogAPI").data("ejDialog"); /* getting ejDialog object */

        $("#btnDialogOpen").ejButton({ "click": "onOpen", width: "95px" });
        $("#btnDialogClose").ejButton({ "click": "onClose", width: "95px" });
        $("#btnDialogIsOpen").ejButton({ "click": "onIsOpen", width: "95px" });
        $("#btnDialogDestroy").ejButton({ "click": "onDestroy", width: "95px" });
        $("#btnDialogRestore").ejButton({ "click": "onRestore", width: "95px" });

       function onOpen() {
            if (eDialog.model) 
                eDialog.open(); /* open the ejDialog widget */                       
        }

        function onClose() {
            eDialog.close(); /* close the ejDialog widget */
        }   

        function onIsOpen() {
            if (eDialog.model) {
                var _isopen = eDialog.isOpened(); /* checking the state of ejDialog widget */ 
                if (_isopen)
                    alert("Dialog Open");
                else
                    alert("Dialog Closed");
            }
            else
                alert("Dialog is in Destoryed state");
        }

        function onDestroy() {
            eDialog.destroy(); /* destroy the ejDialog widget */
        }

        function onRestore() {
            $("#dialogAPI").ejDialog({
                width: 500,
                height: 300
            });
            eDialog = $("#dialogAPI").data("ejDialog");            
        }
     </script>


{% endhighlight %}



3. The output of **Dialog** open is as follows.    

{% include image.html url="/js/Dialog/Concepts-and-Features/Client-Side-APIs_images/Client-Side-APIs_img3.png" Caption=""%}

_Dialog is in open state_            



4. The output of Dialog close is as follows.



{% include image.html url="/js/Dialog/Concepts-and-Features/Client-Side-APIs_images/Client-Side-APIs_img4.png" Caption=""%}

_Dialog is in closed state_

5. The output of **Dialog** destroyed is as follows.


{% include image.html url="/js/Dialog/Concepts-and-Features/Client-Side-APIs_images/Client-Side-APIs_img5.png" Caption=""%}

_Dialog in destroyed state_

