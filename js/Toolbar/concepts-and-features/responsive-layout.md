---
layout: post
title: responsive-layout
description: responsive layout
platform: js
control: Toolbar
documentation: ug
---

# Responsive Layout

**Responsive Layout** is aimed at crafting sites to provide an optimal viewing experience—easy reading and navigation with a minimum of resizing, panning, and scrolling—across a wide range of devices (from mobile phones to desktop computer monitors). You can achieve **Responsive Layout** by using default functionality of **Toolbar** with **isResponsive** as **true** and also you need to give **Toolbar** width as in percentage value and add **ej.responsive.css** file in this sample. **CDN** link for the responsive css file is as follows.

[http://cdn.syncfusion.com/13.1.0.21/js/web/responsive-css/ej.responsive.css](http://cdn.syncfusion.com/13.1.0.21/js/web/responsive-css/ej.responsive.css)

Add the above **css** link in the code sample.        

* Add the following code example in your **HTML** page.

{% highlight html %}

**[HTML]**
<div class="control">
    <!—list of toolbar items-->
    <div id="ToolbarItem">
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
</div>
[CSS]
<style type="text/css" class="cssStyles">
    .e-tooltxt .PdfDocument.e-icon {
        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');
        background-repeat: no-repeat;
        display: block;
        height: 30px;
        width: 30px;
    }

        .e-tooltxt .PdfDocument.e-icon:hover {
            background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon-white.png');
        }

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
</style>

**[Javascript]**
<script type="text/javascript">
    $(function () {
        $("#ToolbarItem").ejToolbar({
            width: "50%", // width of the Toolbar
            height: "33px", // height of the Toolbar
            isResponsive: true // responsive support for toolbar
        });
        var percentList = ["10%", "25%", "50%", "100%", "400%", "800%", "1600%", "3200%", "6400%"];
        $('#selectPercent').ejDropDownList({
            width: "90px",
            height: "27px",
            dataSource: percentList, // Assign List of Dropdown value to data Source
            value: "100%" // Initialize drop down value.
        });
    });
</script>


{% endhighlight %}



**[CSHTML]**

&lt;div class="control"&gt;

    @Html.EJ().Toolbar("ToolbarItem").Width("50%").Height("33px").IsResponsive(true).Items(s =>

    {

        s.Add().Id("OtherFormat").SpriteCssClass("PdfDocument e-icon convertToOthers ").TooltipText("Convert PDF files to Word or Excel Online..");

        s.Add().Id("PDFOnline").SpriteCssClass("PdfDocument e-icon convertToPdf ").TooltipText("Convert files to PDF Online");

        s.Add().Id("Signature").SpriteCssClass("PdfDocument e-icon signature ").TooltipText("Sign, add text or send a document for signature");

        s.Add().Id("Save").SpriteCssClass("PdfDocument e-icon save ").TooltipText("Save file ( Ctrl+S )");

        s.Add().Id("Print").SpriteCssClass("PdfDocument e-icon print ").TooltipText("Print file ( Ctrl+P )");

        s.Add().Id("Message").SpriteCssClass("PdfDocument e-icon msg ").TooltipText("Message");

    }).Items(s1 =>

    {

        s1.Add().Id("Previous").SpriteCssClass("PdfDocument e-icon previous ").TooltipText("Show previous page ( Left Arrow )");

        s1.Add().Id("Next").SpriteCssClass("PdfDocument e-icon next ").TooltipText("Show next page ( Right Arrow )");

        s1.Add().Id("page").SpriteCssClass("PdfDocument ").ContentTemplate(@&lt;input type="text" value="1" /&gt;);

        s1.Add().Id("count").ContentTemplate(@&lt;span&gt;/1</span>);

    }).Items(s2 =>

    {

        s2.Add().Id("ZoomOut").SpriteCssClass("PdfDocument e-icon zoomOut ").TooltipText("Zoom Out");

        s2.Add().Id("ZoomIn").SpriteCssClass("PdfDocument e-icon zoomIn ").TooltipText("Zoom In");

        s2.Add().Id("ZoomValue").SpriteCssClass("PdfDocument ").ContentTemplate(@&lt;div&gt;

            @dropdown()

        &lt;/div&gt;);

    }).Items(s3 =>

{

    s3.Add().Id("FitFull").SpriteCssClass("PdfDocument e-icon fitOne ").TooltipText("Fit one full page to window");

    s3.Add().Id("StickyNote").SpriteCssClass("PdfDocument e-icon sticky ").TooltipText("Add stick note ( Ctrl+6 ) ");

    s3.Add().Id("ReadMode").SpriteCssClass("PdfDocument e-icon readMode ").TooltipText("View File in Read Mode");

})

    @helper dropdown()

{

    &lt;div id="percentlist"&gt;

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

    @Html.EJ().DropDownList("selectPercent").Width("90").Value("100%").TargetID("percentlist")

}

&lt;/div&gt;

[CSS]

&lt;style type="text/css" class="cssStyles"&gt;

    .e-tooltxt .PdfDocument.e-icon {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');

        background-repeat: no-repeat;

        display: block;

        height: 30px;

        width: 30px;

    }



        .e-tooltxt .PdfDocument.e-icon:hover {

            background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon-white.png');

        }



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

&lt;/style&gt;



**[ASPX]**

&lt;ej:Toolbar ID="ToolbarItem" runat="server" Width="50%" Height="33px" IsResponsive="true"&gt;

    &lt;items&gt;

        &lt;ej:toolbaritem id="OtherFormat" spritecssclass="PdfDocument e-icon convertToOthers " tooltiptext="Convert PDF files to Word or Excel Online.."&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="PDFOnline" spritecssclass="PdfDocument e-icon convertToPdf " tooltiptext="Convert files to PDF Online"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="Signature" spritecssclass="PdfDocument e-icon signature " tooltiptext="Sign, add text or send a document for signature"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="Save" spritecssclass="PdfDocument e-icon save " tooltiptext="Save file ( Ctrl+S )"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="Print" spritecssclass="PdfDocument e-icon print " tooltiptext="Print file ( Ctrl+P )"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="Message" spritecssclass="PdfDocument e-icon msg " tooltiptext="Message" isseparator="true"&gt;&lt;/ej:toolbaritem&gt;

    &lt;/items&gt;

    &lt;items&gt;

        &lt;ej:toolbaritem id="Previous" spritecssclass="PdfDocument e-icon previous " tooltiptext="Show previous page ( Left Arrow )"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="Next" spritecssclass="PdfDocument e-icon next " tooltiptext="Show next page ( Right Arrow )"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="pages" spritecssclass="PdfDocument "&gt;

            &lt;template&gt;

                &lt;input type="text" value="1" /&gt;

            &lt;/template&gt;

        &lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="count" isseparator="true"&gt;

            &lt;template&gt;

                &lt;span&gt;/1</span>

            &lt;/template&gt;

        &lt;/ej:toolbaritem&gt;

    &lt;/items&gt;

    &lt;items&gt;

        &lt;ej:toolbaritem id="ZoomOut" spritecssclass="PdfDocument e-icon zoomOut " tooltiptext="Zoom Out"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="ZoomIn" spritecssclass="PdfDocument e-icon zoomIn " tooltiptext="Zoom In"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="ZoomValue" spritecssclass="PdfDocument " isseparator="true"&gt;

            &lt;template&gt;

                &lt;ej:DropDownList ID="selectPercent" runat="server" Width="90px" Height="27px" Value="100%"&gt;

                    &lt;items&gt;

                        &lt;ej:dropdownlistitem text="10%" value="10%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="25%" value="25%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="50%" value="50%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="100%" value="100%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="400%" value="400%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="800%" value="800%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="1600%" value="1600%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="3200%" value="3200%"&gt;&lt;/ej:dropdownlistitem&gt;

                        &lt;ej:dropdownlistitem text="6400%" value="6400%"&gt;&lt;/ej:dropdownlistitem&gt;

                    &lt;/items&gt;

                &lt;/ej:DropDownList&gt;

            &lt;/template&gt;

        &lt;/ej:toolbaritem&gt;

    &lt;/items&gt;

    &lt;items&gt;

        &lt;ej:toolbaritem id="FitFull" spritecssclass="PdfDocument e-icon fitOne " tooltiptext="Fit one full page to window"&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="StickyNote" spritecssclass="PdfDocument e-icon sticky " tooltiptext="Add stick note ( Ctrl+6 ) "&gt;&lt;/ej:toolbaritem&gt;

        &lt;ej:toolbaritem id="ReadMode" spritecssclass="PdfDocument e-icon readMode " tooltiptext="View File in Read Mode" isseparator="true"&gt;&lt;/ej:toolbaritem&gt;

    &lt;/items&gt;

&lt;/ej:Toolbar&gt;

[CSS]

&lt;style type="text/css" class="cssStyles"&gt;

    .e-tooltxt .PdfDocument.e-icon {

        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');

        background-repeat: no-repeat;

        display: block;

        height: 30px;

        width: 30px;

    }



        .e-tooltxt .PdfDocument.e-icon:hover {

            background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon-white.png');

        }



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



    #pages .PdfDocument input {

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

&lt;/style&gt;



Execute the above code to render the following output.

{% include image.html url="\js\Toolbar\concepts-and-features\responsive-layout_images\responsive-layout_img1.png" Caption="Figure 3318: Toolbar with Responsive Support"%}













