---
layout: post
title: appearance-and-styling-
description: appearance and styling 
platform: js
control: Splitter
documentation: ug
---

# Appearance and Styling 

## Responsive

The **enableAutoResize** option allows the **Splitter** control to adapt its rendering based on the parent container where it is actually placed. When this option is set to true, the **Splitter** control adjusts its height and width based on the outer container that contains it, and also the sub-elements within it adjust to its height, width and position, appropriately.

## Enabling Auto Resize

The following steps explain the implementation of **AutoResize** option in the **Splitter** control. 

* In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner splitter control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="outersplitter"&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;                &lt;/div&gt;            &lt;/div&gt;            &lt;div id="innersplitter"&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Tools &lt;/h3&gt;                        Essential Tools is an collection of user interface components used to create interactive                                    ASP.NET MVC applications.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Grid &lt;/h3&gt;                        Essential Mvc Grid offers full featured a Grid control with extensive support for                                    Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Set the <b>width</b> value as <b>100%</b> and <b>enableAutoResize</b> as “<b>True</b>” in <b>Splitter</b> function.    &lt;script type="text/javascript"&gt;        $("#outersplitter").ejSplitter({            height: 280, <b>width: "100%",</b>            orientation: ej.Orientation.Verticalorientation: ej.orientation.Vertical,            properties: [{ paneSize: 60 }],            <b>enableAutoResize: true,</b>        });        $("#innersplitter").ejSplitter({                       <b>enableAutoResize: true           </b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



        @{Html.EJ().Splitter("outterSplitter").Height("280")

**.Width("100%").**Orientation(Orientation.Vertical).**EnableAutoResize(true)**

**.**PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                &lt;div class="content" style="padding: 0px 15px;"&gt;

                    &lt;h3 class="h3"&gt;

                        ASP.NET MVC

                    &lt;/h3&gt;

                &lt;/div&gt;

            &lt;/div&gt;).PaneSize("60");

        p.Add().ContentTemplate(

            @&lt;div style="height: 100%; width: 100%"&gt;

                @innerSplitter()

            &lt;/div&gt;);

    }).Render();}



@helper innerSplitter()

{

    @Html.EJ().Splitter("innerSplitter").**EnableAutoResize(true)**.PaneProperties(p1=>

                {

                    p1.Add().ContentTemplate(@&lt;div&gt;

                        &lt;div class="content"&gt;

                            &lt;h3 class="h3"&gt;

                                Tools

                            &lt;/h3&gt;

                            Essential Tools is an collection of user interface components used to create interactive

                            ASP.NET MVC applications.

                        &lt;/div&gt;

                    &lt;/div&gt;);



                    p1.Add().ContentTemplate(@&lt;div&gt;

            &lt;div class="content"&gt;

                &lt;h3 class="h3"&gt;

                    Grid

                &lt;/h3&gt;

                Essential Mvc Grid offers full featured a Grid control with extensive support for

                Grouping and the display of hierarchical data.

            &lt;/div&gt;

        &lt;/div&gt;);

                });

}



[CSS]

&lt;style type="text/css"&gt;

    #outterSplitter {

        margin: 0 auto;

    }

    .h3 {

        font-size: 14px;

    }

    #innerSplitter {

        border: 0 none;

    }

    .content {

        padding: 15px;

    }

&lt;/style&gt;





**[ASPX]**



         &lt;ej:Splitter Height="280" Width="100%" ID="outersplitter" EnableAutoResize="true" Orientation="Vertical" runat="server"&gt;

             &lt;ej:SplitPane PaneSize="60"&gt;

                         &lt;div&gt;

                &lt;div style="padding: 0px 15px;"&gt;

                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;

                &lt;/div&gt;

            &lt;/div&gt;

             &lt;/ej:SplitPane&gt;



       &lt;ej:SplitPane&gt;

            &lt;ej:Splitter ID="innersplitter" EnableAutoResize="true"  runat="server"&gt;

                &lt;ej:SplitPane&gt;

                                 &lt;div&gt;

                    &lt;div style="padding: 0px 15px;"&gt;

                        <h3 class="h3">Tools </h3>Essential Tools is an collection of user interface components used to create interactive ASP.NET MVC applications.

                   &lt;/div&gt;

                &lt;/div&gt;



                &lt;/ej:SplitPane&gt;

              &lt;ej:SplitPane&gt;

                  &lt;div&gt;

                           &lt;div style="padding: 0px 15px;"&gt;

                        <h3 class="h3">Grid &lt;/h3&gt;

                        Essential Mvc Grid offers full featured a Grid control with extensive support for Grouping and the display of hierarchical data.

                    &lt;/div&gt;

                    &lt;/div&gt;

              &lt;/ej:SplitPane&gt;

            &lt;/ej:Splitter&gt;

      &lt;/ej:SplitPane&gt;



    &lt;/ej:Splitter&gt;



The output for **Splitter** when **enableAutoResize** is “**True**”.



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img1.png" Caption="Figure 1410: Splitter initially"%}



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img2.png" Caption="Figure 151: Automatically resized pane after window resizing"%}

## Animation Support

The **Splitter** provides you animation support when you expand or collapse the pane. The animation speed can be modified by using the **animationSpeed** property, that has values in milliseconds.

### Enabling Animation with Animation speed

The following steps explain the implementation of **enableAnimation** option in the **Splitter** widget.

* In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>            &lt;/div&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Set the <b>enableAnimation </b>property as “<b>True</b>” and set the <b>animationSpeed</b> property with some milliseconds value in the <b>ejSplitter</b> function. The default values for <b>enableAnimation</b> is “<b>True”</b> and <b>animationSpeed</b> is <b>300</b>.    &lt;script type="text/javascript"&gt;        $("#splitter").ejSplitter({            height: 200, width: 200,<b>            enableAnimation: true,</b><b>            animationSpeed: 300           </b>        });       &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@{Html.EJ().Splitter("Splitter").Height("200").Width("200").**EnableAnimation(true)**.**AnimationSpeed(300)**.PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;);

        p.Add().ContentTemplate(

            @&lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;);

    }).Render();}     



**[ASPX]**



         &lt;ej:Splitter ID="splitter" AnimationSpeed="300" Height="200px" Width="200px" EnableAnimation="true" runat="server"&gt;

                &lt;ej:SplitPane&gt;

             &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;

         &lt;/ej:SplitPane&gt;

              &lt;ej:SplitPane&gt;

             &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;

         &lt;/ej:SplitPane&gt;

          &lt;/ej:Splitter&gt;



The output for **Splitter** when **enableAnimation** is “**True**”. Expanding or collapsing the outer pane in the **Splitter** produces the animation effect with the animation speed.



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img3.png" Caption="Figure 162: Splitter with enableAnimation"%}



## Adjusting Splitter Size

### Height

The height of **Splitter** can be modified by using the **height** property. The default value for **height** property is **null** in **Splitter**. You can set the **height** property by pixel or percentage values.

### Width

The width of **Splitter** can be modified by using the **width** property. The default value for **width** property is **null** in **Splitter**. You can set the **width** property by pixel or percentage values.

### Max Size

Defines the maximum resizable size of the pane when you resize the **Splitter** widget. The default value of **maxSize** is **null** in **Splitter**. You can set the **maxSize** property by pixel values.

### Min Size

Defines the minimum resizable size of the pane when you resize  the **Splitter** widget. The default value of **minSize** is **10** in **Splitter**. You can set the **minSize** property by pixel values.

### Pane Size

Defines the pane size in the **Splitter** widget. The default value of **paneSize** is **0px** in **Splitter**. You can set the **paneSize** property by pixel or percentage values.

## Resizable

Defines whether the pane in the **Splitter** is resizable or not. Setting the **resizable** property as “**False”** disables the resize option to the pane. The default value of **resizable** property is true in **Splitter**.

The following steps explain the implementation of **Splitter** properties. 

* In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** widget.



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>            &lt;/div&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>            &lt;/div&gt;        &lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set properties to the pane in the <b>ejSplitter</b> function.  The default values of the properties are <b>{ collapsible : true, minSize: true, maxSize: null, paneSize: 0, resizable: true }</b>.    &lt;script type="text/javascript"&gt;        $("#splitter").ejSplitter({<b>            height:200, width:200,</b><b>            properties: [{}, { collapsible: true, minSize: 10, maxSize: 40, paneSize: 80, resizable: true }]</b><b>        });</b>    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



@{Html.EJ().Splitter("Splitter").**Height("200").Width("200").**PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;);

        p.Add().ContentTemplate(

            @&lt;div&gt;

                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

 &lt;/div&gt;).**Collapsible(true).MinSize("10").MaxSize("40").PaneSize("80").Resizable(true)**;

    }).Render();}





**[ASPX]**



  &lt;ej:Splitter ID="splitter" Height="200"  Width="200" CssClass="customCss" runat="server"&gt;

                &lt;ej:SplitPane PaneSize="80" MinSize="10" MaxSize="40" Collapsible="true" Resizable="true"&gt;

                                            &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;



                &lt;/ej:SplitPane&gt;

                &lt;ej:SplitPane PaneSize="80" MinSize="10" MaxSize="40" Collapsible="true" Resizable="true"&gt;

                            &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;

&lt;/ej:SplitPane&gt;

&lt;/ej:Splitter&gt;



The output for **Splitter** after adding the properties.



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img4.png" Caption="Figure 173: Splitter at initial"%}



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img5.png" Caption="Figure 184: Splitter after collapsing"%}



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img6.png" Caption="Figure 195: Splitter with minSize"%}{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img7.png" Caption="Figure 195: Splitter with minSize"%}



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img8.png" Caption="Figure 1620: Splitter with maxSize"%}

## Theme

**Splitter** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Splitter** control, refer 2 files namely: **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for Autocomplete control namely

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark



### CSS Class

The CSS properties can be customized by using **cssClass** in the **Splitter** widget. The following steps explain the implementation of **cssClass** option in the **Splitter** widget.

* In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>            &lt;/div&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>            &lt;/div&gt;        &lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass </b>property in the <b>ejSplitter</b> function. The default value for the <b>cssClass</b> property is empty string (“ ”).    &lt;script type="text/javascript"&gt;        $("#splitter").ejSplitter({            height: 200, width: 200,            <b>cssClass: "customCSS"</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@{Html.EJ().Splitter("Splitter").Height("200").Width("200").**CssClass("customCSS").**PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;);

        p.Add().ContentTemplate(

            @&lt;div&gt;

                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;).Collapsible(true).MinSize("10").MaxSize("40").PaneSize("80").Resizable(true);

    }).Render();}





**[ASPX]**



        &lt;ej:Splitter ID="splitter" Height="200" Width="200" CssClass="customCSS" runat="server"&gt;

                &lt;ej:SplitPane&gt;

             &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;

         &lt;/ej:SplitPane&gt;

              &lt;ej:SplitPane&gt;

             &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;

         &lt;/ej:SplitPane&gt;

          &lt;/ej:Splitter&gt;





* Customize the **CSS** class by setting **CSS** properties. 



{% highlight css %}

**[CSS]**

    <style>
        .customCSS {            
            border-color: #661e19;
        }

        /*Customize Splitbar*/
        .customCSS .e-splitbar {
            background-color: #f9c89f;
        }

        /*Customize Splitter pane*/
        .customCSS .e-pane {
            color: #b21010;
            background-color: #f6e492;
        }     
    </style>



{% endhighlight %}



The output for **Splitter** after customizing the CSS class.



{% include image.html url="\js\Splitter\concepts-and-features\appearance-and-styling-_images\appearance-and-styling-_img9.png" Caption="Figure 2117: Splitter with cssClass"%}

