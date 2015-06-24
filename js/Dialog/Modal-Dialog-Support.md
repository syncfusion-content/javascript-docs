---
layout: post
title: Modal-Dialog-Support
description: modal dialog support
platform: js
control: Dialog
documentation: ug
---

# Modal Dialog Support

The modal dialog is used like an alert window that disables the main window and explore its content for the purpose of interacting with others. 

## Configure Modal Dialog

The following steps explains you the implementation of modal dialog. 

In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 

{% highlight html %}




<div id="dialogLoginForm" title="Login Form">
   <table>
      <tr>
         <td>User Name
            <input type="text" id="txtName" class="ejinputtext" style="width: 100%" />
         </td>
      </tr>
      <tr>
         <td>Password
            <input type="text" id="Text1" class="ejinputtext" style="width: 100%" />
         </td>
      </tr>
      <tr>
         <td align="center">
            <input type="button" id="downloadBtn" value="Login" class="e-btn" style="width: 100px; height: 30px" />
         </td>
      </tr>
      <tr>
         <td align="center">
            <a href="#">Forgot Password</a>
         </td>
      </tr>
   </table>
</div>



{% endhighlight %}

{% highlight js %}

    // Set enableModal property as true in the Dialog function. The default value of enableModal is false in the Dialog widget
    $("#dialogLoginForm").ejDialog({
        width: 250,
        height: 250,
        enableModal: true
    });

{% endhighlight %}

The output of modal dialog control. 

{% include image.html url="/js/Dialog/Modal-Dialog-Support_images/Modal-Dialog-Support_img1.png" %}

