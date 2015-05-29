---
layout: post
title: getting-started
description: getting started
platform: js
control: Toolbar
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Toolbar** in your application with **JavaScript**, **ASP.NET MVC and ASP.NET.**.**.**

## Create your first Toolbar in JavaScript

### Create Toolbar for PDF Reader

**Toolbar** control supports displaying a list of tools in a Web page. This control is capable of customizing toolbar items with any functionality by using enriched **client-side** methods. This control consists of a collection of **unordered****lists** contains text and images into a **&lt;div&gt;.** From the following section, you can learn how to customize **toolbar** control for a **PDF reader** scenario. The following screen shot shows the appearance of **toolbar** in **PDF reader** simulator application.

{% include image.html url="\js\Toolbar\getting-started_images\getting-started_img1.png" Caption="Figure 1: PDF Reader"%}

#### Create a Toolbar

The **Essential JavaScript Ttoolbar** control can be easily configured with **HTML &lt;DIV&gt;** and **&lt;UL&gt;&lt;LI&gt;** elements. The basic rendering of **Essential JS Toolbar** is achieved by the default functionality.

* Create an HTML file and add the following template into the **HTML** file for **Toolbar** creation.



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add toolbar element here -->
</body>
</html>



{% endhighlight %}



* Add div or span element for **Toolbar** rendering.



{% highlight html %}


<div id="ToolbarItem"> </div>



{% endhighlight %}



* Initialize the **Toolbar** in script



{% highlight js %}


<script type="text/javascript">

        $(function () {// document ready

// simple Toolbar control creation

               $("#ToolbarItem").**ejToolbar()**;

        });

</script>



{% endhighlight %}



* Output of the above steps



![](getting-started_images\getting-started_img2.png)



_Figure_ _2__: Toolbar without toolbar items_

#### Initialize Toolbar Items

**Toolbar** consists of a list of items. From the following section, you can learn how to initialize the toolbar items with **UL LI** template. 							

Initialize the Toolbar items with **UL LI** template as follows. 

{% highlight html %}

**[HTML]**
<div class="control">

        <div id="ToolbarItem">

            <!--list of toolbar items-->

            <ul>
                <li id="OtherFormat" title="Convert PDF files to Word or Excel Online..">
                    <div class="PdfDocument e-icon convertToOthers "></div>
                </li>
                <li id="PDFOnline" title="Convert files to PDF Online">
                    <div class="PdfDocument e-icon convertToPdf "></div>
                </li>
                <li id="Signature" title="Sign, add text or send a document for signature">
                    <div class=" PdfDocument e-icon signature "></div>
                </li>
                <li id="Save" title="Save file ( Ctrl+S )">
                    <div class=" PdfDocument e-icon save "></div>
                </li>
                <li id="Print" title="Print file ( Ctrl+P ) ">
                    <div class=" PdfDocument e-icon print "></div>
                </li>

                <li id="Message" title="Message">
                    <div class=" PdfDocument e-icon msg "></div>
                </li>
            </ul>

        </div>

    </div>


{% endhighlight %}



Apply the given styles in the code table to show the **toolbar items** as follows. You can refer images from any location. In the following code sample, the images are referred from the given location.

[http://js.syncfusion.com/UG/Web/Content/](http://js.syncfusion.com/UG/Web/Content/)

{% highlight css %}


<style type="text/css" class="cssStyles">

        .e-tooltxt .PdfDocument.e-icon {
             background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');
            background-repeat: no-repeat;
            display: block;
            height: 30px;
            width: 30px;
        }

        .e-tooltxt .PdfDocument.e-icon:hover {
            background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon-white.png');        }

        .PdfDocument.e-icon.convertToOthers {
            background-position: -349px 0px;
        }

        .PdfDocument.e-icon.convertToPdf {
            background-position: -527px 0px;
        }

        .PdfDocument.e-icon.signature {
            background-position: 2px 0px;
        }

        .PdfDocument.e-icon.save {
            background-position: -87px 0px;
        }

        .PdfDocument.e-icon.msg {
            background-position: -483px 0px;
        }

</style>



{% endhighlight %}



After updating the **Toolbar****items** with their **CSS** styles, you can render the toolbar inside **&lt;script&gt;** tag.



{% highlight js %}


<script type="text/javascript">

        $(function () {// document ready

       // Toolbar control creation 

         $("#ToolbarItem").ejToolbar({
                width: "auto", // width of the Toolbar
                height: "33px", // height of the Toolbar
            });    

        });

</script>



{% endhighlight %}



Execute the code to render a toolbar with a list of **toolbar items**.



![](getting-started_images\getting-started_img3.png)



_Figure_ _3__: Toolbar with list of toolbar items_

#### Render remaining Toolbar items

In the above output only few **toolbar items** are rendered, but you need to render all the **toolbar items** to achieve the requirements. You can separate or group the toolbar items. The separation or grouping of toolbar items is achieved when you give toolbar items as a list of **UL LI** values inside the toolbar **&lt;div&gt;** or **span** element. From the following section, you can learn how to initialize the remaining toolbar items with **UL LI** template and how to group the toolbar items. 

Initialize the Toolbar items with **UL LI** template as follows.

{% highlight html %}

**[HTML]**
<div id="ToolbarItem">

        <!--Initializes toolbar items from above code example -->
       <!-- Separator is added at the end of each ul inside the toolbar element-->
        <!-- list of Remaining toolbar items with item separator -->

        <ul>
            <li id="Previous" title="Show previous page ( Left Arrow )">
                <div class=" PdfDocument e-icon previous "></div>
            </li>
            <li id="Next" title="Show next page ( Right Arrow )">
                <div class="PdfDocument e-icon next "></div>
            </li>
            <li id="page">
                <div class="PdfDocument">
                    <input type="text" value="1" />
                </div>
            </li>
            <li id="count">
                <span>/ 1</span>
            </li>
        </ul>

        <ul>
            <li id="ZoomOut" title="Zoom Out">
                <div class=" PdfDocument e-icon zoomOut "></div>
            </li>
            <li id="ZoomIn" title="Zoom In">
                <div class=" PdfDocument e-icon zoomIn "></div>
            </li>
            <li id="ZoomValue">
                <div class=" PdfDocument">
                    <!-- input element for rendering Zoom value dropdown  -->
                    <input type="text" id="selectPercent" />
                </div>
            </li>
        </ul>

        <ul>
            <li id="FitFull" title="Fit one full page to window">
                <div class=" PdfDocument e-icon fitOne "></div>
            </li>

            <li id="StickyNote" title="Add stick note ( Ctrl+6 ) ">
                <div class=" PdfDocument e-icon sticky "></div>
            </li>
            <li id="ReadMode" title="View File in Read Mode">
                <div class=" PdfDocument e-icon readMode "></div>
            </li>
        </ul>

    </div>


{% endhighlight %}



Add the following styles in the code table to display the toolbar items as follows. 





    /*Additional style for Remaining toolbar items*/



       .PdfDocument.e-icon.previous {

            background-position: -395px 0px;

        }



        .PdfDocument.e-icon.next {

            background-position: -439px 0px;

        }



        .PdfDocument.e-icon.zoomIn {

            background-position: -175px 0px;

        }



        .PdfDocument.e-icon.zoomOut {

            background-position: -219px 0px;

        }



        .PdfDocument.e-icon.fitOne {

            background-position: -264px 0px;

        }



        .PdfDocument.e-icon.sticky {

            background-position: -131px -1px;

        }



        .PdfDocument.e-icon.readMode {

            background-position: -308px 0px;

        }



        .PdfDocument.e-icon.print {

            background-position: -43px 0px;

        }



        #ZoomValue .PdfDocument {

            width: 90px;

        }



        #page .PdfDocument input {

            text-align: center;

            width: 20px;

            height: 21px;

        }



        #count span {

            width: 30px;

            height: 30px;

            position: relative;

            top: 2px;

            text-align: center;

            vertical-align: middle;

        }





After updating the Toolbar items with their **CSS** styles, you can render the toolbar inside the **&lt;script&gt;** tag and also need to render the drop down list control for **select zoom value**. Basically, dropdown list control is rendered with input element. **Set Zoom value** is one of the items in the toolbar. The following code example shows how to render and initialize **drop down control** with list of **zoom values**.

{% highlight js %}

**[JavaScript]**
  <script type="text/javascript">

        $(function () {
            // declaration

            // List of Dropdown value
            var percentList = ["10%", "25%", "50%", "100%", "400%", "800%", "1600%", "3200%", "6400%"];

            // Dropdown control creation

            $('#selectPercent').ejDropDownList({
                width: "90px",
                height: "27px",
                dataSource: percentList, // Assigns List of Dropdown value to data Source
                value: "100%" // Initializes drop down value.
            });

            // Toolbar control creation

            $("#ToolbarItem").ejToolbar({
                width: "auto",
                height: "33px",
                enableSeparator: true
            });
        });

    </script>


{% endhighlight %}



Execute the code to render a **toolbar items** with separator.



![C:\Users\labuser\Desktop\a.png](getting-started_images\getting-started_img4.png)

_Figure_ _4__: Toolbar items with separator_

#### Add Actions to Toolbar Items

Now the **toolbar** is rendered so you need to render the header and content area to create a **PDF reader**. From the following section, you can learn how to render the **header** (Toolbar), **content****section** (PDF viewer area) and how to set the action to toolbar items.

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img5.jpeg)_**Note: You are not going to deal with PDF reading or rendering task here. You will only simulate the PDF Reader app to demonstrate the Toolbar control usage and will completely ignore the PDF rendering area.**_



Initialize the content area and header as specified in the code table.

{% highlight html %}


<!-- control class used for aligns the pdf reader in center of a page. -->
<div class="control">  

<div class="ctrllabel"></div>

<!-- Here Initialize the Toolbar items as like above code sample -->

   <div id="contentSection">
            <textarea id="content" rows="10" cols="30"> 
   Description:
   Toolbar control supports displaying a list of tools within a Web page.This control is capable of 
   customizing toolbar items with any functionality by using enriched client-side methods.This control 
   is composed of collection of unordered lists containing text and images contained into a div.
</textarea>
        </div>

</div>




{% endhighlight %}



You can apply the following styles with the above styles to design the **PDF header** and **content area**. The desired output is shown as follows.



{% highlight css %}


<style type="text/css" class="cssStyles">

        #content {
            float: left;
            height: 300px;
            width: 628px;
            position: absolute;
        }

        .control {
            margin: 110px 320px 0;
            position: relative;
        }

        .ctrllabel {
            background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-header.png');
            background-repeat: no-repeat;
            width: 634px;
            height: 32px;
        }

</style>



{% endhighlight %}



Execute the given code to render a **PDF reader** as follows.



{% include image.html url="\js\Toolbar\getting-started_images\getting-started_img6.png" Caption="Figure 5: PDF Reader Appearance"%}



So far, you have added the required toolbar items and configured its appearance. When you click on **toolbar items**, the operation is performed through **client slide click event**. The following code example explains how to perform operations when you click on the **toolbar items**.

{% highlight js %}

**[JavaScript]**
<script type="text/javascript">

        $(function () {// document ready

            //Initializes Drop Down control as per above steps.

            // Toolbar control creation

            $("#ToolbarItem").ejToolbar({
                width: "auto",
                height: "33px",
                enableSeparator: true,
                click: "onItemclick" // Binds click event to onclick function
            });

        });

        function onItemclick(args) {

            //Finds Out the Item that was Clicked in Toolbar

            //args.currentTarget returns the clicked Toolbar element

            var option = args.currentTarget.id; //Finds Out the Id of Clicked item.

            switch (option) {
                case "OtherFormat":
                    //writes a code for Convert pdf files to Other format.
                case "PDFOnline":
                    //writes a code for Convert files to Pdf online.
                case "Signature":
                    //writes a code for Send a document for signature.
                case "Save":
                    //writes a code for Save content.
                case "Print":
                    //writes a code for Print content.
                case "Message":
                    //writes a code for Send a Message.
                case "Previous":
                    //writes a code for Show previous page.
                case "Next":
                    //writes a code for Show Next page.
                case "ZoomOut":
                    //writes a code for Zoom out the page.
                case "ZoomIn":
                    //writes a code for Zoom In the page.
                case "FitFull":
                    //writes a code for Fit one full page to window.
                case "StickyNote":
                    //writes a code for Add Sticky Note.
                case "ReadMode":
                    //writes a code for view file in read mode.
            }

        }
    </script>


{% endhighlight %}



## Create your first Toolbar in MVC

**Create Toolbar for PDF Reader**

**Toolbar** control displays a list of tools in a webpage. It is used to customize **Toolbar** items of any functionality, by using enriched **client-side** methods. This control consists of a collection of unordered lists, containing text and images into a **&lt;div&gt;.** From the following section, you can learn how to customize **Toolbar** control for a **PDF Reader** scenario. The following screen shot shows the appearance of **Toolbar** in **PDF Reader** simulator application.

Here, the **Toolbar** consists of a **Toolbar** with title and text area as **PDF Reader**.

{% include image.html url="\js\Toolbar\getting-started_images\getting-started_img7.png" Caption="Figure 6: PDF Reader Toolbar"%}



**Create a Toolbar**

Using the following steps, you can create a **Toolbar** control. The basic rendering of **ASP.NET MVC Toolbar** is achieved with default functionality.



1. You can create an **MVC Project** and add necessary **Dll** and script with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.



2. Add the mentioned code to the corresponding view page for **RichTextEditor** rendering.



**[CSHTML]**     

@Html.EJ().Toolbar("ToolbarItem")





The following output is displayed.



![](getting-started_images\getting-started_img8.png)



_Figure_ _7__: Toolbar without Toolbar items_

**Initialize Toolbar Items**

**Toolbar** consists of a list of items. From the following guidelines, you can learn how to initialize the **Toolbar****items** with **&lt;UL&gt; &lt;LI&gt;** template. 								

Initialize the **Toolbar****items** with **&lt;UL&gt; &lt;LI&gt;** template as follows. 

**[CSHTML]**

&lt;div id="ToolbarItem"&gt;

    &lt;!--list of toolbar items--&gt;



    &lt;ul&gt;

        &lt;li id="OtherFormat" title="Convert PDF files to Word or Excel Online.."&gt;

            &lt;div class="PdfDocument e-icon convertToOthers "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="PDFOnline" title="Convert files to PDF Online"&gt;

            &lt;div class="PdfDocument e-icon convertToPdf "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="Signature" title="Sign, add text or send a document for signature"&gt;

            &lt;div class=" PdfDocument e-icon signature "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="Save" title="Save file ( Ctrl+S )"&gt;

            &lt;div class=" PdfDocument e-icon save "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="Print" title="Print file ( Ctrl+P ) "&gt;

            &lt;div class=" PdfDocument e-icon print "&gt;&lt;/div&gt;

        &lt;/li&gt;



        &lt;li id="Message" title="Message"&gt;

            &lt;div class=" PdfDocument e-icon msg "&gt;&lt;/div&gt;

        &lt;/li&gt;

    &lt;/ul&gt;

&lt;/div&gt;

    @Html.EJ().Toolbar("ToolbarItem").Width("auto").EnableSeparator(true).Height("33px")

Apply the given styles in the code table to show the **Toolbar items** as follows. You can refer images from any location. For the following code example, the images have been referred from the given location.

[http://js.syncfusion.com/UG/Web/Content/](http://js.syncfusion.com/UG/Web/Content/)pdf-icon.png

.

**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;



    .e-tooltxt .e-icon {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');

        background-repeat: no-repeat;

        display: block;

        height: 30px;

        width: 30px;

    }



    .convertToOthers {

        background-position: -349px 0px;

    }



    .convertToPdf {

        background-position: -527px 0px;

    }



    .signature {

        background-position: 2px 0px;

    }



    .save {

        background-position: -87px 0px;

    }



    .print {

        background-position: -43px 0px;

    }



    .msg {

        background-position: -483px 0px;

    }

&lt;/style&gt;





Execute the code to render a **Toolbar** with a list of **Toolbar items**.



![C:\Users\Rajaveni\Desktop\imagesacc\firsttool.PNG](getting-started_images\getting-started_img9.png)

_Figure_ _8__: Toolbar with list of toolbar items_



**Render remaining Toolbar Items**

To achieve the requirements, you need to render all the **Toolbar items**. You can separate or group the **Toolbar items**. The separation or grouping of **Toolbar items** is achieved when you give **Toolbar items** as a list of **&lt;UL&gt; &lt;LI&gt;** values inside the toolbar **&lt;div&gt;** or **span** element. From the following sections, you can learn how to initialize the remaining **Toolbar items** with **&lt;UL&gt; &lt;LI&gt;** template and how to group the toolbar items. 

Initialize the **Toolbar** items with **&lt;UL&gt; &lt;LI&gt;** template as follows.





&lt;div id="ToolbarItem"&gt;



    &lt;!--Initialize toolbar items from above code snippet --&gt;



    &lt;!-- Separator will be added at the end of each ul inside the toolbar element--&gt;



    &lt;!-- list of Remaining toolbar items with item separator --&gt;



    &lt;ul&gt;

        &lt;li id="Previous" title="Show previous page ( Left Arrow )"&gt;

            &lt;div class=" PdfDocument e-icon previous "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="Next" title="Show next page ( Right Arrow )"&gt;

            &lt;div class="PdfDocument e-icon next "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="page"&gt;

            &lt;div class="PdfDocument"&gt;

                &lt;input type="text" value="1" /&gt;

            &lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="count"&gt;

            &lt;span&gt;/ 1</span>&lt;/li&gt;

    &lt;/ul&gt;



    &lt;ul&gt;

        &lt;li id="ZoomOut" title="Zoom Out"&gt;

            &lt;div class=" PdfDocument e-icon zoomOut "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="ZoomIn" title="Zoom In"&gt;

            &lt;div class=" PdfDocument e-icon zoomIn "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="ZoomValue"&gt;

            &lt;div id="carlist"&gt;

                &lt;ul&gt;

                    <li>10%&lt;/li&gt;

                    <li>25%&lt;/li&gt;

                    <li>50%&lt;/li&gt;

                    <li>100%&lt;/li&gt;

                    <li>400%&lt;/li&gt;

                    <li>800%&lt;/li&gt;

                    <li>1600%&lt;/li&gt;

                    <li>3200%&lt;/li&gt;

                    <li>6400%&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;

            @Html.EJ().DropDownList("car").Width("90").Value("100%").TargetID("carlist")

        &lt;/li&gt;

    &lt;/ul&gt;



    &lt;ul&gt;

        &lt;li id="FitFull" title="Fit one full page to window"&gt;

            &lt;div class=" PdfDocument e-icon fitOne "&gt;&lt;/div&gt;

        &lt;/li&gt;



        &lt;li id="StickyNote" title="Add stick note ( Ctrl+6 ) "&gt;

            &lt;div class=" PdfDocument e-icon sticky "&gt;&lt;/div&gt;

        &lt;/li&gt;

        &lt;li id="ReadMode" title="View File in Read Mode"&gt;

            &lt;div class=" PdfDocument e-icon readMode "&gt;&lt;/div&gt;

        &lt;/li&gt;

    &lt;/ul&gt;



&lt;/div&gt;



Add the following styles in the code table to display the **Toolbar items** as follows. 





    /*Additional style for Remaining toolbar items*/

&lt;style&gt;

    .zoomIn {

        background-position: -175px 0px;

    }

    .readMode {

         background-position: -307px -1px;

    }

    .zoomOut {

        background-position: -219px 0px;

    }



    .fitOne {

        background-position: -264px 0px;

    }



    .sticky {

        background-position: -131px -1px;

    }



    #ZoomValue.e-tooltxt .e-icon {

        background-image: none;

    }



    #page .PdfDocument input {

        text-align: center;

        width: 20px;

        height: 21px;

    }



    #count span {

        width: 30px;

        height: 30px;

        position: relative;

        top: 2px;

        text-align: center;

        vertical-align: middle;

        background-image: none;

    }



    .PdfDocument.e-icon.previous {

        background-position: -395px 0px;

    }



    .PdfDocument.e-icon.next {

        background-position: -439px 0px;

    }

&lt;/style&gt;



**Set Zoom value** is one of the items in the **Toolbar**. You need to render the **Dropdown****list** control for **select zoom value**. **Dropdown****list** control is rendered with **&lt;UL&gt; &lt;LI&gt;** elements. The **ASP.NET MVC****Dropdown control** with a list of **zoom values** is used to render **Set Zoom value** in the above sample code. Refer to the provided link for **Dropdown** creation.

[Dropdown – GettingStarted](http://help.syncfusion.com/aspnetmvc/)

Execute the code to render **Toolbar items** with separator.



{% include image.html url="\js\Toolbar\getting-started_images\getting-started_img10.png" Caption="Figure 9: Toolbar Items with separator"%}

**Add Actions to Toolbar Items**

Now that the **Toolbar** is rendered, you need to render the header and content area to create a **PDF Reader**. In the following section, you can learn how to render the **header** (Toolbar), **content****section** (PDF viewer area) and how to set the action to **Toolbar items**.

![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img11.jpeg)_**Note: PDF reading or rendering is not shown here. Simulation of the PDF Reader app to demonstrate the usage of Toolbar control is provided. PDF rendering area is ignored.**_



Initialize the **content****area** and **header** as specified in the code table.



&lt;!-- control class used for aligns the pdf reader in center of a page. --&gt;

&lt;div class="control"&gt;



    &lt;div class="ctrllabel"&gt;&lt;/div&gt;

    &lt;div id="ToolbarItem"&gt;



    &lt;!--Add toolbar items from above code snippet --&gt;



    &lt;/div&gt;



    &lt;!-- Here Initialize the Toolbar items as like above code sample --&gt;

    &lt;div id="contentSection"&gt;

        &lt;textarea id="content" rows="10" cols="30"&gt; 

   Description:

   Toolbar control supports displaying a list of tools within a Web page.This control is capable of 

   customizing toolbar items with any functionality by using enriched client-side methods.This control 

   is composed of collection of unordered lists containing text and images contained into a div.

&lt;/textarea&gt;

    &lt;/div&gt;



&lt;/div&gt; 



You can apply the following styles with the above styles to design the **PDF header** and **content area**. 





&lt;style type="text/css" class="cssStyles"&gt;

    #content {

        float: left;

        height: 300px;

        width: 633px;

        position: absolute;

    }



    .control {

        margin: 110px 320px 0;

        position: relative;

    }



    .ctrllabel {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-header.png');

        background-repeat: no-repeat;

        width: 638px;

        height: 32px;

    }

&lt;/style&gt;



Execute the code example to render a **PDF Reader** as follows.



{% include image.html url="\js\Toolbar\getting-started_images\getting-started_img12.png" Caption="Figure 10: PDF Reader Appearance"%}

So far, you have added the required toolbar items and configured its appearance. When you click on **Toolbar items**, the operation is performed through **client-slide** click event. The following code example explains how to perform operations, when you click on the **Toolbar items**.

**[ASPX]**

&lt;div id="ToolbarItem"&gt;



    &lt;!--Add toolbar items from above code snippet --&gt;



&lt;/div&gt;



&lt;!-- Here Initialize the Toolbar items as shown in above code sample and add Clientside Event as follows --&gt;

@Html.EJ().Toolbar("ToolbarItem").ClientSideEvents(e => e.Click("onItemclick")).Width("auto").EnableSeparator(true)







&lt;script type="text/javascript"&gt;



    function onItemclick(args) {





        //Finds Out the Item that was Clicked in Toolbar





        //args.currentTarget returns the clicked Toolbar element





        var option = args.currentTarget.id; /* Find Out the Id of Clicked item. */







        switch (option) {



            case "OtherFormat":



                //writes a code for Convert pdf files to Other format.



            case "PdfOnline":



                //writes a code for Convert files to Pdf online.



            case "Signature":



                //writes a code for Send a document for signature.



            case "Save":



                //writes a code for Save content.



            case "Print":



                //writes a code for Print content.



            case "Message":



                //writes a code for Send a Message.



            case "Previous":



                //writes a code for Show previous page.



            case "Next":



                //writes a code for Show Next page.



            case "ZoomOut":



                //writes a code for Zoom out the page.



            case "ZoomIn":



                //writes a code for Zoom In the page.



            case "FitFull":



                //writes a code for Fit one full page to window.



            case "StickyNote":



                //writes a code for Add Sticky Note.



            case "ReadMode":



                //writes a code for view file in read mode.

        }



    }



&lt;/script&gt;

## Create your first Toolbar in ASP.NET

**Create Toolbar for PDF Reader**

**Toolbar** control displays a list of tools in a webpage. It is used to customize **Toolbar** items of any functionality, by using enriched **client-side** methods. This control consists of a collection of unordered lists, containing text and images. From the following section, you can learn how to customize **Toolbar** control for a **PDF Reader** scenario. The following screen shot displays the appearance of **Toolbar** in **PDF Reader** simulator application.

Here, the **Toolbar** consists of a **Toolbar** with title and text area as **PDF Reader**.

![C:\Users\Rajaveni\Desktop\JS Docs\Accordion\new\fffffff1.PNG](getting-started_images\getting-started_img13.png)

_Figure_ _11__: PDF Reader Toolbar_



**Create a Toolbar**

You can create a **Toolbar** control using the following steps. The basic rendering of **ASP.NET Toolbar** is achieved with default functionality.



1. You can create an **ASP.NET Project** and add necessary **Dll** and script with the help of the given [WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the mentioned code to the corresponding **ASPX** page for **Toolbar** rendering.



**[ASPX]**     



&lt;ej:Toolbar ID="PdfSimulator"  runat="server" Width="637px"&gt;

&lt;/ej:Toolbar&gt; 



The following output is displayed.



![](getting-started_images\getting-started_img14.png)

_Figure_ _12__: Toolbar without Toolbar items_



**Initialize Toolbar Items**

**Toolbar** consists of a list of items. From the following guidelines, you can learn how to initialize **Toolbar** with the **Toolbar****items**. 

**[ASPX]**

&lt;ej:Toolbar ID="PdfSimulator" EnableSeparator="true"  runat="server" Width="220px"&gt;

    &lt;Items&gt;

        &lt;ej:ToolbarItem Id="OtherFormat" SpriteCssClass="PdfDocument e-icon convertToOthers " TooltipText="Convert PDF files to Word or Excel Online.."&gt;&lt;/ej:ToolbarItem&gt;

        &lt;ej:ToolbarItem Id="PDFOnline" SpriteCssClass="PdfDocument e-icon convertToPdf" TooltipText="Convert files to PDF Online"&gt;&lt;/ej:ToolbarItem&gt;

        &lt;ej:ToolbarItem Id="signature"  SpriteCssClass="PdfDocument e-icon signature" TooltipText="Sign, add text or send a document for signature"&gt;&lt;/ej:ToolbarItem&gt;

        &lt;ej:ToolbarItem Id="Save" SpriteCssClass="PdfDocument e-icon save " TooltipText="Save file ( Ctrl+S )"&gt;&lt;/ej:ToolbarItem&gt;

        &lt;ej:ToolbarItem Id="Print" SpriteCssClass="PdfDocument e-icon print" TooltipText="Print file ( Ctrl+P ) "&gt;&lt;/ej:ToolbarItem&gt;

        &lt;ej:ToolbarItem Id="Message" IsSeparator="true" SpriteCssClass="PdfDocument e-icon msg" TooltipText="Message"&gt;&lt;/ej:ToolbarItem&gt;

    &lt;/Items&gt;

&lt;/ej:Toolbar&gt;



Apply the styles specified in the code table to show the **Toolbar items** as follows. You can refer images from any location. For the following code example, the images are referred from the following location.

[http://js.syncfusion.com/UG/Web/Content/](http://js.syncfusion.com/UG/Web/Content/)pdf-icon.png



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;



    .e-tooltxt .e-icon {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');

        background-repeat: no-repeat;

        display: block;

        height: 30px;

        width: 30px;

    }



    .convertToOthers {

        background-position: -349px 0px;

    }



    .convertToPdf {

        background-position: -527px 0px;

    }



    .signature {

        background-position: 2px 0px;

    }



    .save {

        background-position: -87px 0px;

    }



    .print {

        background-position: -43px 0px;

    }



    .msg {

        background-position: -483px 0px;

    }

&lt;/style&gt;





Execute the above code to render a **Toolbar** with a list of **Toolbar items**.



![C:\Users\Rajaveni\Desktop\JS Docs\toolbar\simple toolbar.PNG](getting-started_images\getting-started_img15.png)

_Figure_ _13__: Toolbar with list of toolbar items_

**Render remaining Toolbar Items**

To achieve the requirements, you need to render all the **Toolbar items**. You can separate or group the **Toolbar items**. The separation or grouping of **Toolbar items** is achieved by setting **EnableSeprator property** as true for the **Toolbar** control. Set **IsSeparator** property as true for the **ToolbarItem** that needs to be separated with other ToolbarItem. From the following sections, you can learn how to initialize the remaining **Toolbar items** and how to group the toolbar items. 

Initialize and group the **Toolbar** items as follows.

**[ASPX]**

&lt;ej:Toolbar ID="PdfSimulator" EnableSeprator="true" runat="server" Width="637px"&gt;

        &lt;Items&gt;

            <ej:ToolbarItem Id="OtherFormat" SpriteCssClass="PdfDocument e-icon convertToOthers "

                TooltipText="Convert PDF files to Word or Excel Online..">

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="PDFOnline" SpriteCssClass="PdfDocument e-icon convertToPdf" TooltipText="Convert files to PDF Online"&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="signature" SpriteCssClass="PdfDocument e-icon signature" TooltipText="Sign, add text or send a document for signature"&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="Save" SpriteCssClass="PdfDocument e-icon save " TooltipText="Save file ( Ctrl+S )"&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="Print" SpriteCssClass="PdfDocument e-icon print" TooltipText="Print file ( Ctrl+P ) "&gt;

            &lt;/ej:ToolbarItem&gt;

            <ej:ToolbarItem Id="Message" IsSeparator="true" SpriteCssClass="PdfDocument e-icon msg"

                TooltipText="Message">

            &lt;/ej:ToolbarItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:ToolbarItem Id="Previous" SpriteCssClass=" PdfDocument e-icon previous " TooltipText="Show previous page ( Left Arrow )"&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="Next" SpriteCssClass="PdfDocument e-icon next " TooltipText="Show next page ( Right Arrow ) "&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="pager" SpriteCssClass="PdfDocument" TooltipText="Message"&gt;

                &lt;Template&gt;

                    &lt;input type="text" style="width: 22px" value="1" /&gt;

                &lt;/Template&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem IsSeparator="true" Id="count"&gt;

                &lt;Template&gt;

                    <span>1</span>&lt;/Template&gt;

            &lt;/ej:ToolbarItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:ToolbarItem Id="ZoomOut" SpriteCssClass=" PdfDocument e-icon zoomOut " TooltipText="Show next page ( Right Arrow ) "&gt;

            &lt;/ej:ToolbarItem&gt;

            <ej:ToolbarItem Id="ZoomIn" SpriteCssClass="PdfDocument e-icon zoomIn " IsSeparator="true"

                TooltipText="Message">

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="ZoomValue" IsSeparator="true"&gt;

                &lt;Template&gt;

                    &lt;ej:DropDownList ID="zoom" Width="90" Value="100%" runat="server"&gt;

                        &lt;Items&gt;

                            &lt;ej:DropDownListItem Value="10%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="25%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="50%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="100%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="400%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="800%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="1600%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="3200%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Value="6400%"&gt;

                            &lt;/ej:DropDownListItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:DropDownList&gt;

                &lt;/Template&gt;

            &lt;/ej:ToolbarItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:ToolbarItem Id="FitFull" SpriteCssClass="PdfDocument e-icon fitOne" TooltipText="Fit one full page to window"&gt;

            &lt;/ej:ToolbarItem&gt;

            &lt;ej:ToolbarItem Id="StickyNote" SpriteCssClass="PdfDocument e-icon sticky" TooltipText="Add stick note ( Ctrl+6 ) "&gt;

            &lt;/ej:ToolbarItem&gt;

            <ej:ToolbarItem Id="ReadMode" SpriteCssClass="PdfDocument e-icon readMode" IsSeparator="true"

                TooltipText="View File in Read Mode">

            &lt;/ej:ToolbarItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Toolbar&gt;



Add the following styles in the code table to display the **Toolbar items** as follows. 



[CSS]

&lt;style&gt;

        /*Additional style for Remaining toolbar items*/

        .zoomIn

        {

            background-position: -175px 0px;

        }



        .readMode

        {

            background-position: -307px -1px;

        }



        .zoomOut

        {

            background-position: -219px 0px;

        }



        .fitOne

        {

            background-position: -264px 0px;

        }



        .sticky

        {

            background-position: -131px -1px;

        }



        #&lt;%=ZoomValue.ClientID%&gt;.e-tooltxt .e-icon

        {

            background-image: none;

        }



        #page .PdfDocument input

        {

            text-align: center;

            width: 20px;

            height: 21px;

        }



        #<%=PdfSimulator.ClientID%>_zoom_dropdown .e-icon

        {

            background-image: none;

        }



        #<%=PdfSimulator.ClientID%>_count span

        {

            width: 30px;

            height: 30px;

            position: relative;

            top: 2px;

            text-align: center;

            vertical-align: middle;

            background-image: none;

        }



        .PdfDocument.e-icon.previous

        {

            background-position: -395px 0px;

        }

        .PdfDocument.e-icon.next

        {

            background-position: -439px 0px;

        }

        span#&lt;%=PdfSimulator.ClientID%&gt;

        {

            display: none !important;

        }

    &lt;/style&gt;



**Set Zoom value** as it is one of the items in the **Toolbar**. You need to render the **Dropdown****list** control for **select zoom value**. **Dropdown****list** control is rendered with **DropDownListItem** elements. The **ASP.NET Dropdown control** with a list of **zoom values** is used to render **Set Zoom value** in the above sample code. Refer the following link for **Dropdown** creation. 

[Dropdown – GettingStarted](http://help.syncfusion.com/aspnetmvc/)

Execute the above code to render **Toolbar items** with separator.

![C:\Users\Rajaveni\Desktop\JS Docs\toolbar\ssssssssss.PNG](getting-started_images\getting-started_img16.png)

_Figure_ _14__: Toolbar Items with separator_



**Add Actions to Toolbar Items**

Now the **Toolbar** is rendered and you need to render the header and content area to create a **PDF Reader**. In the following section, you can learn how to render the **header** (Toolbar), **content****section** (PDF viewer area) and how to set the action to **Toolbar items**.



![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img17.jpeg)_**Note: PDF reading or rendering is not illustrated here. Simulation of the PDF Reader app to demonstrate the usage of Toolbar control is provided. PDF rendering area is ignored.**_



Initialize the **content****area** and **header** as specified in the following code table.



**[ASPX]**

&lt;!-- control class used for aligns the pdf reader in center of a page. --&gt;

&lt;div class="control"&gt;



    &lt;div class="ctrllabel"&gt;&lt;/div&gt;

    &lt;!-- Here Initialize the Toolbar items as shown in above code sample and add Clientside Event as follows --&gt;





    &lt;ej:Toolbar ID="PdfSimulator" EnableSeprator="true" runat="server" Width="637px"&gt;

    &lt;!--Add toolbar items from above code snippet --&gt;



    &lt;/ej:Toolbar&gt;   



    &lt;div id="contentSection"&gt;

        &lt;textarea id="content" rows="10" cols="30"&gt; 

   Description:

   Toolbar control supports displaying a list of tools within a Web page.This control is capable of 

   customizing toolbar items with any functionality by using enriched client-side methods. This control 

   is composed of collection of unordered lists containing text and images contained into a div.

&lt;/textarea&gt;

    &lt;/div&gt;



&lt;/div&gt; 



You can apply the following styles with the above styles to design the **PDF header** and **content area**. 



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

    #content {

        float: left;

        height: 300px;

        width: 633px;

        position: absolute;

    }



    .control {

        margin: 110px 320px 0;

        position: relative;

    }



    .ctrllabel {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-header.png');

        background-repeat: no-repeat;

        width: 638px;

        height: 32px;

    }

     #contentSection {

         padding-top: 5px;

     }



&lt;/style&gt;





Execute the above code to render the **PDF Reader** as follows.



![C:\Users\Rajaveni\Desktop\JS Docs\Accordion\new\ggggggggggggg.PNG](getting-started_images\getting-started_img18.png)_Figure_ _15__: PDF Reader Appearance_



Now the required toolbar items are added and its appearance is configured. When you click on **Toolbar items**, the operation is performed through **client-slide** click event. The following code example explains you on how to perform operations, when you click on the **Toolbar items**.



**[ASPX]**

&lt;ej:Toolbar ID="PdfSimulator" EnableSeparator="true" ClientSideOnClick="onItemclick" runat="server" Width="637px"&gt;

&lt;!--Add toolbar items from above code snippet --&gt;



&lt;/ej:Toolbar&gt;  



&lt;script type="text/javascript"&gt;



    function onItemclick(args) {





        //Finds Out the Item that was Clicked in Toolbar





        //args.currentTarget returns the clicked Toolbar element





        var option = args.currentTarget.id; /* Find Out the Id of Clicked item. */





        switch (option) {



            case "OtherFormat":



                //writes a code for Convert pdf files to Other format.



            case "PdfOnline":



                //writes a code for Convert files to Pdf online.



            case "Signature":



                //writes a code for Send a document for signature.



            case "Save":



                //writes a code for Save content.



            case "Print":



                //writes a code for Print content.



            case "Message":



                //writes a code for Send a Message.



            case "Previous":



                //writes a code for Show previous page.



            case "Next":



                //writes a code for Show Next page.



            case "ZoomOut":



                //writes a code for Zoom out the page.



            case "ZoomIn":



                //writes a code for Zoom In the page.



            case "FitFull":



                //writes a code for Fit one full page to window.



            case "StickyNote":



                //writes a code for Add Sticky Note.



            case "ReadMode":



                //writes a code for view file in read mode.



        }



    }



&lt;/script&gt;



