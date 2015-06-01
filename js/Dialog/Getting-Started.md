---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Dialog
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Dialog** in your application with **JavaScript**.

## Create your first Dialog in JavaScript

The **Essential JavaScript Dialog** control displays a **Dialog** window within the web page. The **Dialog** control enables you to display a message in the supplementary content like images, text and interactive content such as forms. The **Dialog** control displays the content on **modal dialog**, in which you cannot interact with other items on the page. You can drag and resize the **Dialog**. This section explains you how to customize a **Dialog** for a real time login form scenario. The following screen shot illustrates the appearance of the **Dialog**.



{% include image.html url="/js/Dialog/Getting-Started_images/Getting-Started_img1.png" Caption="Sign Up Form Appearance"%}

### Create a Dialog

**Essential JavaScript Dialog** control is an interface for hosting a page inside a window. **Dialog** content can be text, graphics or **HTML**. It shows the model popup window as model form. You can create a **Dialog** control by using simple **&lt;div&gt;** tag element as follows.

1. Create an HTML file and add the following template in the HTML file. 



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
         <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add dialog element here -->
</body>
</html>



{% endhighlight %}



2. Add &lt;div&gt; or span elements in &lt;body&gt; tag to render Dialog control.  



{% highlight html %}


   <div id="loginForm" title="Sign Up"></div>



{% endhighlight %}



3. Initialize the Dialog control in &lt;script&gt; tag.



{% highlight js %}


    <script type="text/javascript">
        $(function () {
            // document ready
            // Initialize Dialog control creation
            $("#loginForm").ejDialog();
        });
                   </script> 


{% endhighlight %}



4. Execute the above code to render the following output.



{% include image.html url="/js/Dialog/Getting-Started_images/Getting-Started_img2.png" Caption="Dialog Control Appearance without Dialog content"%}

This screenshot illustrates the **Dialog** control without any dialog content.  By default the **Dialog** control shows the header element. The title text is taken from **dialog element title** attribute or **title** property.

### Set content 

To display the content in **Dialog** control, you can add the content in **Dialog** element and design the login page using **Dialog** control. You can create the **HTML** content for login page and add it in the **Dialog** element.

The following code example illustrates how to set the content in **Dialog** control.



{% highlight html %}


  <!-- Dialog control element -->

    <div id="loginForm" title="Sign Up">

        <form method="get" name="signup" id="signup_form">

            <!--title attribute value used to set the title to dialog control header -->

            <!-- Sign up form elements -->

            <div class="heading">
                <div class="text-center">Sign Up</div>
                <div class="text-center content">It's free and always will be</div>
            </div>
            <div class="information">
                <div class="row">
                    <span class="info">
                        <!-- input element for First name field -->
                        <input type="text" id="firstname" name="first name" class="input ejinputtext name" placeholder="First Name" />
                    </span>
                    <span class="info last">
                        <!-- input element for last name field -->
                        <input type="text" id="lastname" name="last name" class="input ejinputtext name" placeholder="Last Name" />
                    </span>
                </div>
                <div class="row">
                    <!-- input element for email field -->
                    <input type="text" id="email" name="email" class="input ejinputtext email" placeholder="Your Email" />
                </div>
                <div class="row">
                    <!-- input element for Re-enter email field -->
                    <input type="text" id="reptemail" name="re-enter email" class="input ejinputtext email" placeholder="Re-enter Email" />
                </div>
                <div class="row">
                    <!-- input element for Password field -->
                    <input type="password" maxlength="8" name="password" id="password" class="input ejinputtext" placeholder="Password" />
                </div>
            </div>
            <div class="signupbtn">
                <!--Sign Up button -->
                <input type="button" onclick="onSignUp()" class="btn btn-lg btn-primary" name="Submit" value="Sign Up" />
            </div>
            <!-- Sign up form elements are ended here-->
        </form>
    </div>



{% endhighlight %}



You can use the following styles to customize the styles of sign up form. You can use **Bootstrap** for aligning the login page header in center and styling the sign up button. You can include **bootstrap.min.css** file from **CDN** location. 



{% highlight css %}


  <style class="cssStyles">

        #loginForm {
        background: linear-gradient(#FFFFFF, #D3D8E8) repeat scroll 0 0 rgba(0, 0, 0, 0);

      }

        .content {
            color: #999999;
        }

        .input {
            width: 100%;
            height: 32px;
            text-indent: 10px;
            border-radius: 3px;
            font-size: larger;
        }

        .heading {
            padding: 10px 0px;
        }

        .heading > div {
            font-size: 30px;
        }

        .heading div.content {
            font-size: 15px;
         }

        .information {
            padding: 5px 20px;
        }

        .signupbtn {
            padding: 10px 20px;
        }

        .information .row {
            padding: 5px 0px;
        }

        .info {
            float: left;
            width: 47%;
        }

       .info.last {
           float: right;
        }

        .signupbtn .btn {
            width: 100%;
        }
    </style>



{% endhighlight %}



Render the dialog inside **&lt;script&gt;** tag after updating the dialog content with CSS styles. 



{% highlight js %}


$(function () {
            // declaration
            $("#loginForm").ejDialog();
        });



{% endhighlight %}



Execute the code to render the following output.



{% include image.html url="/js/Dialog/Getting-Started_images/Getting-Started_img3.png" Caption="Dialog Control Appearance with Sign up form elements"%}

This process enables you to render the **Dialog** control with sign up form elements. The above screen shot displays the **Dialog** control with header and resizable option. These options are enabled in **Dialog** control by default. 

### Configure Dialog 

To remove the header and resizable options from dialog use the **enableResize** and **showHeader** properties. By default the width of the **Dialog** control is based on the content inside it. You can also set the width of the **Dialog** control using **width** property. To render the appearance of sign up control, you can set the width of **Dialog** control.

1. Initialize the **Dialog** control using following code example.



{% highlight js %}


$(function () {
            // declaration
            $("#loginForm").ejDialog({
width:"330px", // To set the width to Dialog control.
                    showHeader:false, // To remove Dialog Header from dialog
enableResize:false // To remove Resizable option from dialog
            });
        });



{% endhighlight %}



2. Execute the code to render the following output_._



{% include image.html url="/js/Dialog/Getting-Started_images/Getting-Started_img4.png" Caption="Dialog Control with Sign up form elements"%}

###  Add Validation

This section explains you to set the validation to each form elements inside the Dialog control. To validate each form element click sign up button. The Dialog closes when the signup button is clicked raising the beforeClose event. The beforeClose event validates each and every form elements manually. Once the validation succeeds, the Dialog closes.

When the validation fails, set args.cancel value as ‘true’. This prevents the Dialog from closing.

1. You can add an HTML element in the form to display the error message in Dialog.



{% highlight html %}


            <!-- element for error message -->

                  <div class="errormsg"></div>  <!-- insert the element at the end of the Sign up form -->



{% endhighlight %}





2. Add the following code example in &lt;script&gt; tag to add validation to form elements.



{% highlight js %}


    <script type="text/javascript">
        $(function () {
            // declaration
            $("#loginForm").ejDialog({
                width: "330px", // To set the width to Dialog control.
                showHeader: false, // To remove Dialog Header from dialog.
                enableResize: false, // To remove Resizable option from dialog.
                beforeClose: "onValidation" //Bind beforeClose event to onValidation function.
            });

        });

        //onSignUp function trigger when click on Sign up Button.

        function onSignUp() {
            var obj = $("#loginForm").data("ejDialog");
            obj.close(); 
        }

        // onValidation function trigger before close the dialog.

        function onValidation(args) {
            var error = [], re, regEmail;
            //Regular expression for validating string type value
            re = /^[A-Za-z]+$/;
            //Regular expression for validating email address value
            regEmail = /^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;

            //Validating FirstName and Lastname field
            $('#loginForm input.name[type=text]').each(function (n, element) {
                if (($(element).val() == ''))
                    error.push('Please enter your ' + element.name);
                else if (!re.test($(element).val()))
                    error.push(element.name + ' must have a string value');
            });

            //Validating email and re-enter email field
            $('#loginForm input.email[type=text]').each(function (n, element) {
                if (($(element).val() == ''))
                    error.push('Please enter your ' + element.name + ' address');
                else if (!regEmail.test($(element).val()))
                    error.push('Please enter a valid email address');
            });
            !($("#loginForm input#email").val() === $("#loginForm input#reptemail").val()) ? error.push("Email address not matched") : "";

            //Validating password field
            if ($("#loginForm input#password").val() == '')
                error.push('Please provide a password');
            else if (($('#loginForm input#password').val().length < 5) || ($('#loginForm input#password').val().length > 8))
                error.push('Your password must be at least 5 and at most 8 characters long');

            //Creating error message and append in dialog 
            ulTag = $(document.createElement('ul'));
            for (var i = 0; i < error.length; i++) {
                liTag = $(document.createElement('li'));
                liTag.append("<span>-" + error[i] + "</span>");
                ulTag.append(liTag);
            }

            //Check Whether valiadation Success or Not
            (error.length != 0) ? ($(".errormsg").html(ulTag), args.cancel = true) // set args.cancel = true prevent dialog close
            : alert("Sign Up Successfully Completed");
        }
    </script>



{% endhighlight %}



3. Add the following styles to customize the styles of error message.



{% highlight css %}


        .errormsg li {
            list-style: none outside none;
        }

        .errormsg span {
            color: #FF0000;
            font-size: 12px;
            font-style: italic;
            margin: 2px 0;
            font-weight: normal;
        }



{% endhighlight %}



4. Execute the code to render the following output.

{% include image.html url="/js/Dialog/Getting-Started_images/Getting-Started_img5.png" Caption="Sign Up form with validation"%}

The above screen shot displays an error message when an invalid input is given to form elements. The dialog is closed when the value is in a valid format or the **Dialog** is open.	 

