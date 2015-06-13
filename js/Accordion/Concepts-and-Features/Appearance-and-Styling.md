---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Accordion 
documentation: ug
---

# Appearance and Styling

**Adjusting Accordion size**

You can customize the **Accordion** panel height using **heightAdjustMode** property. It can be set to **enum** values like content, fill or auto. By default **heightAdjustMode** is set to **content** so the panel height is adjusted to the content size.

**Configure Height of Accordion panel**

The following steps explains you on how to configure **Accordion** panel height.

1. In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}

   **[HTML]**

     <div id="accordion" style="width: 400px"> 
    <h3>  
        <a href="#">Orubase</a></h3>    
     <div>  <!-- add accordion contents here to load contents under this header -->  
        Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
    </div>  
    <h3>   
        <a href="#">WinRTXAML</a></h3>     
     <div>  <!-- add accordion contents here to load contents under this header --> 
       Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.       
    </div>        
    <h3>     
        <a href="#">Metro Studio</a></h3>   
      <div>  <!-- add accordion contents here to load contents under this header -->   
        Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                      
    </div>                         
     </div>


{% endhighlight %}


{% highlight js %}

[JavaScript]

// Configure heightAdjustMode for accordion

            $("#accordion").ejAccordion({
                heightAdjustMode: "auto"
            });


{% endhighlight %}


2. Output for Accordion control when panel height is set to auto so that the maximum content height and Fill for minimum content height in all the panels is as follows.



{% include image.html url="/js/Accordion/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Accordion height set to auto adjust mode"%}

**Rounded corner**

You can customize the shape of the **Accordion** widget from regular rectangular shape to rounded rectangle shape enabling **roundedCorner property** that is set to false by default.

**Enabling Rounded corner property**

The following steps explains you in enabling the **showRoundedCorner** property for an **Accordion** control.

1. In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}

   **[HTML]**

      <div id="accordion" style="width: 400px"> 
    <h3>  
        <a href="#">Orubase</a></h3>    
      <div>  <!-- add accordion contents here to load contents under this header -->  
            Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
        </div>  
        <h3>   
            <a href="#">WinRTXAML</a></h3>     
      <div>  <!-- add accordion contents here to load contents under this header --> 
           Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.       
        </div>        
        <h3>     
            <a href="#">Metro Studio</a></h3>   
      <div>  <!-- add accordion contents here to load contents under this header -->   
            Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                      
        </div>                         
    </div>


{% endhighlight %}


{% highlight js %}

[JavaScript]

// Enable showRoundedCorner for Accordion

    $("#accordion").ejAccordion({
                showRoundedCorner: true
            }); 


{% endhighlight %}


2. Output for accordion widget when “showRoundedCorner” is set to “true” is as follows.


{% include image.html url="/js/Accordion/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Accordion with Rounded rectangular appearance"%}

**Customize Accordion icon**

**Accordion** widget allows you to customize the icons using **customIcon** option that has two properties **header** and **selectedHeader**. By default, the classes of header and selectedHeader are e-collapse and e-expand respectively. By setting the desired CSS class names for these properties as required overrides the default icons with customized icons.

**Configuring custom icon for Accordion**

The following steps explains you the configuration of icon for an **Accordion** control.

1. In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}

   **[HTML]**

        <div id="accordion" style="width: 400px"> 
            <h3>  
                <a href="#">Orubase</a></h3>    
          <div>  <!-- add accordion contents here to load contents under this header -->  
                Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
            </div>  
            <h3>   
                <a href="#">WinRTXAML</a></h3>     
          <div>  <!-- add accordion contents here to load contents under this header --> 
               Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.       
            </div>        
            <h3>     
                <a href="#">Metro Studio</a></h3>   
          <div>  <!-- add accordion contents here to load contents under this header -->   
                Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                      
            </div>                         
        </div>

{% endhighlight %}


{% highlight js %}

[JavaScript]

// Set the “e-arrowheaddown” and “e-arrowheadup” classes to header and selectedHeader properties.  “e-arrowheaddown” and “e-arrowheadup” are available in ej.widgets.core.min.css file.


$("#accordion").ejAccordion({
      customIcon: {
/*  To set icon for the collapsed accordion headers  */
                    header: "e-arrowheaddown",                     
/*  To set icon for the selected accordion headers  */
                    selectedHeader: "e-arrowheadup" 
                } 
       });


{% endhighlight %}



2. Output for Accordion widget with customized icons is as follows.



{% include image.html url="/js/Accordion/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" Caption="Accordion with customized icons"%}

**Animations**

**Set animation**

By default the **Animation** for expanding and collapsing is enabled. To remove the Animation you can set the **enableAnimation** property to **false**. This restricts customizing animations as well. By default **enableAnimation** is set to **true**.

Following code disables **Animation** for **Accordion**.


{% highlight js %}

**[JavaScript]**
$("#accordion").ejAccordion({
**enableAnimation: false**
       }); 


{% endhighlight %}

**Expand and collapse speed**

This feature allows you to set the speed for expanding and collapsing the **Accordion** panels. By default it is set to 300 in milliseconds. By configuring the animation speed you can optimize the delay in loading the panel content.

The following code sample sets value for **expandSpeed** and **collapseSpeed** properties,

{% highlight js %}

**[JavaScript]**
$("#accordion").ejAccordion({
                **expandSpeed:600,**
                **collapseSpeed:1000,**
                collapsible:true
            }); 


{% endhighlight %}



**Theme**

You can control the style and appearance of **Accordion** control based on **CSS** classes. In order to apply styles to the **Accordion** widget, you can refer two files, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Accordion** control namely

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



**CSS class**

**CSS** class can be used to customize the **Accordion** control appearance. Define a **CSS** class asyou’re your requirement and assign the class name to **cssClass** property.

**Configure AutoComplete textbox using CSS class**

The following steps allows you to configure **CSS** class for an **Accordion** widget.

1. In the HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}

  **[HTML]**
    
    <div id="accordion" style="width: 400px"> 
        <h3>  
            <a href="#">Orubase</a></h3>    
      <div>  <!-- add accordion contents here to load contents under this header -->  
            Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.
        </div>  
        <h3>   
            <a href="#">WinRTXAML</a></h3>     
      <div>  <!-- add accordion contents here to load contents under this header --> 
           Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.       
        </div>        
        <h3>     	
            <a href="#">Metro Studio</a></h3>   
      <div>  <!-- add accordion contents here to load contents under this header -->   
            Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.                      
        </div>                         
    </div>


{% endhighlight %}

{% highlight js %}

[JavaScript]

// Set the cssClass property for Accordion

         $("#accordion").ejAccordion({
                cssClass: "customCss"
            });


{% endhighlight %}

2. Define CSS class for customizing the Accordion.



{% highlight css %}

**[Style]**
<style class="cssStyles">
         .customCss
         {
            font-style: italic;
            text-align:justify;
         }
         .customCss span.e-icon {
            display: none !important;
         }
         .customCss h3
         {
             text-decoration:underline;
             text-align:center;
         }
    </style>



{% endhighlight %}



3. Output for Accordion with customized CSS property to hide the Accordion icon and format its content is as follows.

{% include image.html url="/js/Accordion/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img4.png" Caption="Accordion with Custom CSS property"%}

