---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: DropDownList
documentation: ug
---

# Getting Started 

This section explains briefly on how to create a **DropDownList** control in your application by using **JavaScript**.

The **DropDownList** control provides a list of options and allows you to choose an item from the list. It includes several other **HTML** elements such as images, textboxes, check box, and radio buttons and so on. It also supports data binding, template options and multi-select options. In this example, you can learn how to customize **DropDownList** in a real time Voting Selection Scenario of World Cup Football. This helps you to display the groups and its countries in the **DropDownList** Selection Item. 

The following screenshot demonstrates the functionality of **DropDownList** with a Cascading feature.

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img1.png")

In the above screenshot, you can select a group from the first **DropDownList** widget. After you select the group, the corresponding countries for that group are listed in the second **DropDownList** widget.Then, you can select a country and press the **Vote** option.  

## Create DropDownList Widgets 

**Essential JavaScript DropDownList** widget basically renders with built-in features.

You can create an **HTML** file and add the following code example to it. 

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"rel="stylesheet"/>
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!— add the DropDownList element here -->
   </body>
</html>
{% endhighlight %}

Add the input element to render **DropDownList** widgets.

{% highlight html %}

<div class="control">
   <div class="ball-icon"></div>
   <div class="ball-txt" style="">WORLD CUP FOOTBALL</div>
   <br />
   <table>
      <tr>
         <td class="tdcls"><span class="txt">
            <label>Select Group</label></span>
         </td>
         <td class="tdcls"><span class="txt">
            <label>Select Country</label></span>
         </td>
      </tr>
      <tr>
         <td class="tdcls">
            <input id="groupsList" type="text" />
         </td>
         <td class="tdcls">
            <input id="countryList" type="text" />
         </td>
      </tr>
   </table>
   <div class="votebox">
      <button class="e-btn" id="voter">Vote </button>
   </div>
</div>

{% endhighlight %}

Add the following style section for the alignment of **DropDownList** widgets. You can add the following location in the **URL** path for the background image http://js.syncfusion.com/UG/Web/Content/football.png

{% highlight css %}

<style type="text/css" class="cssStyles">
   .control
   {
       margin-left: 20px;
       margin-top: 10px;
   }
   .ball-icon
   {
       display: inline-block;
       background-image: url("http://js.syncfusion.com/UG/Web/Content/football.png");
       background-repeat: no-repeat;
       background-size: contain;
       height: 50px;
       width: 50px;
   }
   .ball-txt
   {
       display: inline-block;
       font-size: 20px;
       font-weight: bolder;
       height: 50px;
       position: relative;
       text-align: center;
       top: -20px;
   }
   .votebox
   {
       margin-left: 150px;
       margin-top: 50px;
   }
   .txt
   {
       display: block;
       margin-bottom: 12px;
   }
   .tdcls
   {
       width: 200px;
   } 
</style>


{% endhighlight %}

Initialize the **DropDownList** and other widgets by using the following code example.

{% highlight js %}

    // Declare Necessary variable creation 
    var grpSlct, contrySlct;

    $(function() {
        // document ready
        // simple DropDownList creation 
        $('#groupsList').ejDropDownList({
            watermarkText: "group" // set watermark text
        });

        // simple DropDownList creation
        $('#countryList').ejDropDownList({
            watermarkText: "country" // setting watermark text
        });

        // simple Button creation
        $("#voter").ejButton();

    });
    
{% endhighlight %}

Run this code to render the resultant output of the above steps.

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img2.png") 

## Configure Data Source

You can configure **DropDownList** widgets by using online services. Two different online data services for the two **DropDownList** widgets are created. They are as, _groups_ data service for the group selection **DropDownList** and _countries_ data service for the country selection **DropDownList**. Both the data services are referred from the following service location.

[http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/](http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/)

In the above mentioned scenario, the given data source is mentioned in the **Data** **Source** property. In the first and second **DropDownList** widgets, you can mention the Group widgets and countries Data Source in the **Data** **Source** property respectively. When the **Data** **Source** has different field names, you can map the fields with the **field’s** property.

The following code example explains how to configure the **Data Source**.

{% highlight js %}

     // Declare Necessary variable creation 
     var grpSlct, contrySlct;

     $(function() {
         // document ready

         // DataManager creation
         var dataManger = ej.DataManager({
             url: "http://mvc.syncfusion.com/UGOdataServices/Northwnd.svc/"
         });
         // Query creation for groups table
         var query1 = ej.Query()
             .from("TeamGroups");

         // Query creation for countries table
         var query2 = ej.Query()
             .from("TeamCountries");

         // simple DropDownList creation
         $('#groupsList').ejDropDownList({

             watermarkText: "group", // set watermark text

             // Set Data Source in the Data Source Property
             dataSource: dataManger,

             query: query1, // set query for groups

             // Map the fields in the data source with the fields property if its not having fields as in the fields property
             fields: {
                 text: "GroupName",
                 value: "GroupId"
             }
         });

         // simple DropDownList creation
         $('#countryList').ejDropDownList({

             watermarkText: "country", // set watermark text

             // Set Data Source in the Data Source Property
             dataSource: dataManger,
             query: query2, // setting query for countries
             // Set the popup list width
             popupWidth: "300px",

             // Configure fields with properties
             fields: {
                 text: "CountryName",
                 value: "CountryId",
                 spriteCssClass: "CountryFlag"
             }
         });

         // simple Button creation
         $("#voter").ejButton();

     });


{% endhighlight %}

Execute this code to render the output.

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img3.png") 

## Configure DropDownList with Sprite Icons

To style the **DropDownList** popup with the Country flag, create the **SpriteCSS** styles by using the flag icons from the following image source location. You can add the following location in the **URL** path for the background images.

[http://js.syncfusion.com/UG/Web/Content/countryFootbal.png](http://js.syncfusion.com/UG/Web/Content/countryFootbal.png)

You can load the spirit image icons for the countries in a **DropDownList** by adding the following code example in styles section. 

{% highlight css %}

<style type="text/css" class="cssStyles">
   #countryList_popup_wrapper .e-align
   {
       display: inline-block;
       float: none;
       margin-left: 5px;
       margin-right: 10px;
       vertical-align: middle;
   }
   /*Sprite CSS for the Flags used in DDL widget */
   .flag
   {
       display: block;
       background-image: url(http://js.syncfusion.com/UG/Web/Content/countryFootbal.png); 
       height: 46px;
       width: 70px;
       background-position: center center;
       background-repeat: no-repeat;
   }
   .flag.algeria
   {
       background-position: 0 0;
   }
   .flag.argentina
   {
       background-position: 0 -96px;
   }
   .flag.australia
   {
       background-position: 0 -192px;
   }
   .flag.belgium
   {
       background-position: 0 -288px;
   }
   .flag.bosnia
   {
       background-position: 0 -384px;
   }
   .flag.brazil
   {
       background-position: 0 -480px;
   }
   .flag.cameroon
   {
       background-position: 0 -576px;
   }
   .flag.chile
   {
       background-position: 0 -672px;
   }
   .flag.colombia
   {
       background-position: 0 -768px;
   }
   .flag.costarica
   {
       background-position: 0 -864px;
   }
   .flag.croatia
   {
       background-position: 0 -960px;
   }
   .flag.ecuador
   {
       background-position: 0 -1056px;
   }
   .flag.england
   {
       background-position: 0 -1152px;
   }
   .flag.france
   {
       background-position: 0 -1248px;
   }
   .flag.germany
   {
       background-position: 0 -1344px;
   }
   .flag.ghana
   {
       background-position: 0 -1440px;
   }
   .flag.greece
   {
       background-position: 0 -1536px;
   }
   .flag.honduras
   {
       background-position: 0 -1632px;
   }
   .flag.iran
   {
       background-position: 0 -1728px;
   }
   .flag.italy
   {
       background-position: 0 -1824px;
   }
   .flag.ivoriecote
   {
       background-position: 0 -1920px;
   }
   .flag.japan
   {
       background-position: -120px 0;
   }
   .flag.korea
   {
       background-position: -120px -96px;
   }
   .flag.mexico
   {
       background-position: -120px -192px;
   }
   .flag.netherlands
   {
       background-position: -120px -288px;
   }
   .flag.nigeria
   {
       background-position: -120px -384px;
   }
   .flag.portugal
   {
       background-position: -120px -480px;
   }
   .flag.russia
   {
       background-position: -120px -576px;
   }
   .flag.spain
   {
       background-position: -120px -672px;
   }
   .flag.swiss
   {
       background-position: -120px -768px;
   }
   .flag.uruguay
   {
       background-position: -120px -864px;
   }
   .flag.usa
   {
       background-position: -120px -960px;
   }
</style>

{% endhighlight %}

Run the above code example to render the following **DropDownList** with Data sources.

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img4.png") 

## Set the Cascading Option

In the above scenario, when you select the group in the first **DropDownList**, the corresponding countries for that group are listed in the country **DropDownList.** This is achieved by setting the **“cascadeTo”** that points the **DropDownList**, where the data is loaded dynamically. You can disable the second **DropDownList** till the data is loaded dynamically.

The following code example explains how to set the Cascading Option.

{% highlight js %}

   // Declare Necessary variable creation 
   var grpSlct, contrySlct;

   $(function() {

       // document ready
       // To add DataSource refer the navigated section
       // simple DropDownList creation
       $('#groupsList').ejDropDownList({
           watermarkText: "group", // set watermark text
           // Set Data Source in the Data Source Property
           dataSource: dataManger,
           query: query1, // set query for groups
           // Map the fields in the data source with the fields property if its not having fields as in the fields property
           fields: {
               text: "GroupName",
               value: "GroupId"
           },
           // Set DropDownList id to load the dynamic data
           cascadeTo: 'countryList'
       });

       // simple DropDownList creation 
       $('#countryList').ejDropDownList({
           watermarkText: "country", // setting watermark text
           // Set Data Source in the Data Source Property
           dataSource: dataManger,
           query: query2, // set query for countries
           // Configure fields with properties
           fields: {
               text: "CountryName",
               value: "CountryId",
               spriteCssClass: "CountryFlag"
           },
           // Set the popup list width
           popupWidth: "300px",
           // Disable the dropdownlist until to load the data
           enabled: false
       });
       // simple Button creation
       $("#voter").ejButton();
   });

{% endhighlight %}

Execute this code to render the **DropDownList** with Cascading Option.  

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img5.png") 

Initially, you can select the group from the popup of the first **DropDownList**. After you select the option, selected value is loaded.   


![]("/js/DropDownList/Getting-Started_images/Getting-Started_img6.png") 

Based on the group selection in the first **DropDownList**, the **DataSource** in the second **DropDownList** is loaded and the corresponding Countries are displayed while clicking the drop-down button as follows.


![]("/js/DropDownList/Getting-Started_images/Getting-Started_img7.png") 

From the **DropDownList** “Country”, you can select your desired country.


![]("/js/DropDownList/Getting-Started_images/Getting-Started_img8.png") 

## Set the Vote process in the DropDownList Widget

The voting process is done by clicking the **Vote** button. A button is customized to support the voting process. For more information on button, refer to the following link: <http://help.syncfusion.com/js/button/overview>

The following code example explains how to set the Vote process in the **DropDownList** widget.

{% highlight js %}

     // To addDataSource refer the navigated section
     // Declare Necessary variable creation 
     var grpSlct, contrySlct;

     $(function() {
         // document ready
         // simple DropDownList creation can be referred here 
         // simple Button creation
         $("#voter").ejButton({
             width: "80px", // set the width for the Button
             height: "25px", // set the height for the button
             showRoundedCorner: true, // set the rounded corner option  to true
             contentType: "textandimage", // set the content type for the button
             prefixIcon: "e-uiLight e-userlogin", // set the Prefix icon for button
             click: "selectVoted" // set click event of button
         });
     });

     function selectVoted() {
         grpSlct = $('#groupsList').data("ejDropDownList");
         contrySlct = $('#countryList').data("ejDropDownList");
         alert("You have voted for the " + contrySlct.model.text + " country in " + grpSlct.model.text);
     }
     
{% endhighlight %}

When you run the above code example, it displays the **DropDownList** widgets. You can select the value and click the **Vote** button. The button click event is processed and the values are displayed as follows.

![]("/js/DropDownList/Getting-Started_images/Getting-Started_img9.png") 

