---
layout: post
title: getting-started-
description: getting started 
platform: js
control: Tab Control
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Tab** Control in your application with **JavaScript** and **ASP.NET MVC**.

## Create your first Tab Control in JavaScript

The **Essential JavaScript Tab** control is an interface that displays the content in multiple sections. Each **TabPanel** consists of **HeaderText** or **HeaderTemplate** as well as a **ContentTemplate**. **Tab** is useful for a dashboard that is having limited space. The following section guides you to on-demand customize the **Tab** for displaying Hotel menu items, its rating details and ingredients.



![](getting-started-_images\getting-started-_img1.png)![](getting-started-_images\getting-started-_img2.png)

_Figure_ _1__:_ _Tab_ _control with Hotel Menu items_

**Create Tab Control**

**Essential JavaScript Tab** widget basically builds a dynamic interactive menu-driven interface from your content. The content can be text, graphics or HTML. You can create the **Tab** headers using &lt;UL&gt; and &lt;LI&gt; tags and content panels using &lt;div&gt; tags. 

The following steps describe the creation of **Tab** control.  

* Create an **HTML** file and add the following template in the HTML file for creating **Tab** control.

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
    <!--add tab element here-->
</body>
</html>


{% endhighlight %}



* Add **Tab** header within &lt;body&gt; tag.



{% highlight html %}


<div id="dishType" style="width: 550px">
  <ul>
     <li><a href="#pizza">Pizza Menu</a></li>
     <li><a href="#sandwich">Sandwich Menu</a></li>
     <li><a href="#pasta">Pasta Menu</a></li>
  </ul>
</div>


{% endhighlight %}



* Initialize **Tab** in &lt;script&gt; tag.



{% highlight js %}


<script type="text/javascript">
$(function () {
// document ready
// simple Tab header creation
	$("#dishType").ejTab();       
});
</script>


{% endhighlight %}



The following screen shot illustrates the **Tab** control with Header.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img3.png" Caption="Figure 2: Tab control with Header"%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img4.png" Caption="Figure 2: Tab control with Header"%}

**Configure Content**

In this application a detailed description is provided to each item. You can specify the contents in the **Tab** section within the &lt;div&gt; element. 



{% highlight html %}


<div id="pizza" style="background-color: #F5F5F5">
<!—Food item description-->
         <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
</div>



{% endhighlight %}



You can provide more customization to the **Tab** with **rating** control as content in it for describing the item rating value. 

**Create the Rating** 

The **Essential JavaScript Rating** control provides you an intuitive rating experience that allows you to select the number of stars that represents the rating. For more information about the rating please refer the following link: 

[http://help.syncfusion.com/ug/js/default.htm#!Documents/gettingstarted25.htm](http://help.syncfusion.com/ug/js/default.htm)

The following code example explains you the **rating** control creation. The input element is used to create the **rating** control. Render the input element as **rating** control using the input element id. The code example can be placed within the content description &lt;div&gt; element to declare the rating control and description in the **Tab** section and it can be appended with the header initialization code section &lt;div&gt; element.



{% highlight html %}


<div id="pizza" style="background-color: #F5F5F5">
         <p>Rating:</p>
         <!--Rating control declaration-->
**<div class="dishRating">**
               **<input id="pizzaRating" type="text" class="rating" />**
         **</div>**
          <!--Food item description-->
         <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
</div>


{% endhighlight %}



To render the **rating** controls in the first **Tab** element refer the styles mentioned in the following code example.



{% highlight css %}


<style type="text/css" class="cssStyles">
        .dishRating {
            position: absolute;
            margin: -31px 0px 0px 80px;
        }        
    </style>


{% endhighlight %}



The following code example is used for rendering the content with **rating** control within the first **Tab** content section.



{% highlight js %}


<script type="text/javascript">
$(function () {
	$("#dishType").ejTab();       
       $("#pizzaRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.9 });
});
</script>


{% endhighlight %}



The following screenshot illustrates the **Tab** content with rating control. 



![C:\Users\ApoorvahR\Pictures\3.png](getting-started-_images\getting-started-_img5.png)![](getting-started-_images\getting-started-_img6.png)

_Figure_ _3__:_ _First Tab content section with Rating Control_

**Ajax Content Load (Load On Demand)** 

You can change the contents in sub **Tab** element periodically and you are provided with a support to change the contents without any problems. To achieve the content load, use the Load on Demand concept.

In Load On-Demand, the external HTML file with the necessary details is referred in &lt;href&gt; section during **Tab** header declaration section. When you click the **Tab** header, the Ajax automatically calls the content from the external files and displays in a **Tab** content section.

**Sub Tab with Ajax Content**

Each item is having a variety of options and these options are also specified in the limited space. So you can choose the **Tab** control that is used within the root **Tab** to specify more details.

The following code example illustrates to create the **Tab** control within the root **Tab** element. This HTML code is appended within the previous HTML code section. To render the child **Tab** with its header, add this code example within the first **Tab** &lt;div&gt; element.



{% highlight html %}

<!--sub Tab control, the contents loaded with load on demand-->
<div id="pizzaType">
   <ul>
                <li><span class="cornSpinach"></span>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/cornSpainach.html">Corn & Spinach </a></li>
       <li><span class="chickenDelite"></span>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/ChickenDelite.html">Chicken Delite </a></li>   
            </ul>
</div>


{% endhighlight %}



* The Load On-Demand supported **HTML** file content (cornSpinach.html)



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
        <img src=" http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach">
        <div class="ingredients">
            Rate    : $70<br/> Ingredients : cheese, sweet corn &amp; green capsicums. 
            <br /> 
            Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.                    </div>
    </div>    
</body>
</html>


{% endhighlight %}



* The Load On Demand supported html file content (chickenDelite.html)



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
        <img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite">
        <div class="ingredients">
            Rate    : $100<br /> Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.   <br />  
             Description: This is a tasty, elegant chicken dish that is easy to prepare. 
        </div>
    </div>
</body>
</html>


{% endhighlight %}

> ![C:\Users\labuser\Desktop\note.jpg](getting-started-_images\getting-started-_img7.jpeg)_**Note: In Load On Demand, when the external files are referred from local the following error occurs.**_

XMLHttpRequest cannot load [http://js.syncfusion.com/UG/Web/Tab-Content/cornSpainach.html?_=1399883825133](http://js.syncfusion.com/UG/Web/Tab-Content/cornSpainach.html?_=1399883825133). No 'Access-Control-Allow-Origin' header is present on the requested resource. 

To avoid these errors, the external files are hosted in the server to run this application.

The following code example is used to position the image and content in Load On Demand.



{% highlight css %}

<style type="text/css" class="cssStyles">
       /*reuse the previous rating control style section code*/                
       .ingredients {
            height: 180px;
            margin-top: 8px;
        }
        img {           
            float: left;        
            margin: 10px 26px 5px 1px;
        }
    </style>


{% endhighlight %}



The sub **Tab** control rendering script is represented in the following code example.



{% highlight js %}


<script type="text/javascript">
   $(function () {
        // To reuse the previous script section to render first tab with contents
        $("#pizzaType").ejTab();
});
</script>



{% endhighlight %}



At the time of Ajax call, the content fetched from external file referenced location is illustrated in the following screenshot.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img8.png" Caption="Figure 4: Ajax Call"%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img9.png" Caption="Figure 4: Ajax Call"%}



The following screenshot illustrates the First **Tab** with the sub **Tab** control using Load on Demand.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img10.png" Caption="Figure 5: first Tab section with sub Tab control using Load on Demand."%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img11.png" Caption="Figure 5: first Tab section with sub Tab control using Load on Demand."%}

**Orientation Change**

In this application, the sub **Tab** orientation needs to be vertical. By default, **Tab** control renders in horizontal orientation. Change the orientation to vertical using the “**headerPosition**” property. The **Tab** header orientation is set as “**left**”.

The following code example is used to render the sub **Tab** element in the vertical orientation.



{% highlight js %}


<script type="text/javascript">
        $(function () {          
             $("#dishType").ejTab();       
             $("#pizzaRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.9 });
             // set the orientation on sub tab element.       
             $("#pizzaType").ejTab({
**headerPosition**: "left",
                height: "221px"
            });                                                  
        });
</script>


{% endhighlight %}



The following screenshot illustrates the sub **Tab** with vertical orientation.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img12.png" Caption="Figure 6: Sub Tab customized orientation"%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img13.png" Caption="Figure 6: Sub Tab customized orientation"%}

**Header Image Customization**

In this application, you have to set the **Tab** header image for each Tab item to specify image in &lt;span&gt; tag element during the **Tab** header declaration time.	

The following code example is used for customizing the header image.



{% highlight css %}


<style type="text/css" class="cssStyles">
        .dish {
            display: inline-block;
            vertical-align: middle;
            margin: 0px -9px 0px 9px;            
        }
        .pizzaImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_chicken-delite.png") no-repeat;
            height: 25px;
            width: 25px;
        }
        /*reuse the previous header orientation code*/                
</style>



{% endhighlight %}



The following code example is used to add the header image for the root **Tab** header element.



{% highlight html %}


<div id="dishType" style="width: 550px">
      <ul>
         <li><span class="dish pizzaImg"></span><a href="#pizza">Pizza Menu</a></li>  
         <!—- reuse the remaining tab header -->       
       </ul>
       <!—- reuse the previously defined first tab html content section-->
</div>



{% endhighlight %}



The following screenshot illustrates the **Tab** with the customized header image.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img14.png" Caption="Figure 7: Header Image Customization"%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img15.png" Caption="Figure 7: Header Image Customization"%}

**Configuring Contents to remaining Tab items**

The second and third **Tab** contents are declared in the same method as of the first **Tab** content declaration. These **Tabs** also consist of rating and sub **Tab** controls. The sub **Tab** control contents are loaded in Load On Demand support.

The following code example can be placed within the previous image customization **HTML** code section.



{% highlight html %}


           <!—reuse the first tab header defined in previous image customization -->
     <li><span class="dish sandwichImg"></span><a href="#sandwich">Sandwich Menu</a></li>
     <li><span class="dish pastaImg"></span><a href="#pasta">Pasta Menu</a></li>


{% endhighlight %}



Add the second **Tab** contents in &lt;div&gt; element during initialization.



{% highlight html %}


     <div id="sandwich" style="background-color: #F5F5F5">
          <p>Rating:</p>
          <!--Rating control declaration-->
          <div class="dishRating">
                <input id="sandwichRating" type="text" class="rating" />
          </div>
         <!--dish description-->
          <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
          <!--sub Tab control, the contents loaded with load on demand-->
          <div id="sandwichType">
              <ul>
                  <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/gardenVeggie.html"> Garden Veggie </a></li>
                   <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/chickenTikka.html"> Chicken Tikka </a></li>
                   <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/paneerTikka.html"> Paneer Tikka </a></li>             
              </ul>
           </div>
     </div>


{% endhighlight %}



Add third **Tab** contents in &lt;div&gt; element during initialization.



{% highlight html %}


      <div id="pasta" style="background-color: #F5F5F5">
          <p>Rating:</p>
          <!--Rating control declaration-->
          <div class="dishRating">
              <input id="pastaRating" type="text" class="rating" />
          </div>
          <!--dish description-->
          <p>Pasta cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
           <!--sub Tab control, the contents loaded with load on demand-->
           <div id="pastaType">
               <ul>
                   <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/khemmaPasta.html">Kheema Pasta </a></li>
                   <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/tunaPasta.html">Tuna Pasta</a></li>
                   <li>
<a href="http://js.syncfusion.com/UG/Web/Tab-Content/channaPasta.html">Channa Pasta
</a></li>                
               </ul>
            </div>
       </div>


{% endhighlight %}



Apply the following styles to the **Tab**.



{% highlight css %}

<style type="text/css" class="cssStyles">
        /*to reuse the previous style section code and following css*/        
       .sandwichImg, .pastaImg {
            height: 25px;
            width: 25px;
        }
        .sandwichImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-fresh.png") no-repeat;                       
        }
        .pastaImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-veggie.png") no-repeat;                 
        }  
</style>


{% endhighlight %}



After the content declaration of all the **Tab** control, render the final output using the following code example.



{% highlight js %}


<script type="text/javascript">
        $(function () {
            // declaration       
            $("#dishType").ejTab();        // Overall Tab Container   
            $("#pizzaType").ejTab({        // First sub child Tab Container  
                headerPosition: "left",
                height: "221px"
            });                                                  
            $("#pizzaRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.9 });  
            $("#sandwichType").ejTab({     // Second sub child Tab Container   
                headerPosition: "left",
                height: "221px"
            });                                                                              
            $("#sandwichRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 3.9 });    
            $("#pastaType").ejTab({       // Third sub child Tab Container  
                headerPosition: "left",
                height: "221px"
            });                                                                
            $("#pastaRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 4.5 }); 
        });
    </script>                 


{% endhighlight %}



The following screenshot illustrates you the second **Tab** contents in **Tab** and the final hotel menu with rating, description and ingredients of the item in the Tab interface.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img16.png" Caption="Figure 8: Tab represents different items with load on demand support"%}{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img17.png" Caption="Figure 8: Tab represents different items with load on demand support"%}



## Create your first Tab Control in MVC

The **ASP.NET MVC****Tab** control is an interface that displays the content in multiple sections. A **TabPanel** consists of HeaderText or HeaderTemplate as well as a ContentTemplate. **Tab** is useful for a dashboard that is having limited space. The following section guides you to customize the **Tab** for displaying Hotel menu items, its rate details and the ingredients on demand.



![](getting-started-_images\getting-started-_img18.png)

_Figure_ _9__: Tab control with Hotel Menu items_

**Create Tab Control**

The **ASP.NET MVC****Tab** widget basically builds a dynamic, interactive, menu-driven interface from your content. The content can be text, graphics or HTML. You can create the **Tab** headers using **&lt;UL&gt;** and **&lt;LI&gt;** tags and content panels using **&lt;div&gt;** tags. 

The following steps are used to create **Tab** control.  

1. You can create an **MVC Project** and add necessary **Dll** and script with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the mentioned code to the corresponding view page for **Tab** rendering.



&lt;div id="DishType" style="width: 550px"&gt;

        &lt;ul&gt;

            &lt;li&gt;<a href="#PizzaType">Pizza Menu</a>&lt;/li&gt;

            &lt;li&gt;<a href="#SandwichType">Sandwich Menu</a>&lt;/li&gt;

            &lt;li&gt;<a href="#PastaType">Pasta Menu</a>&lt;/li&gt;

        &lt;/ul&gt;

        @Html.EJ().Tab("DishType")

&lt;/div&gt;



The following output is displayed.



![](getting-started-_images\getting-started-_img19.png)

_Figure_ _10__: Tab control with Header_

**Configure Content**

In this application, a detailed description is provided to each item. You can specify the contents in the **Tab** section within the **&lt;div&gt;** element. 



    &lt;div id="DishType" style="width: 550px"&gt;

        &lt;ul&gt;

            &lt;li&gt;<a href="#PizzaType">Pizza Menu</a>&lt;/li&gt;

            &lt;li&gt;<a href="#SandwichType">Sandwich Menu</a>&lt;/li&gt;

            &lt;li&gt;<a href="#PastaType">Pasta Menu</a>&lt;/li&gt;

        &lt;/ul&gt;

        @Html.EJ().Tab("DishType")

             &lt;!--Tab elements description--&gt;

        &lt;div id="PizzaType" style="background-color: #F5F5F5"&gt;

            &lt;!--Food item description--&gt;

            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

             &lt;!—Add sub Tab control description--&gt;

            &lt;/div&gt;

        &lt;/div&gt;





You can provide more customization to the **Tab** by using **rating** control, to describe an item’s price.

**Create the Rating** 

The **ASP.NET MVC****Rating** control provides an intuitive rating experience that allows you to select the number of stars that represents the rating. The following code example explains you the creation of **rating** control. The input element is used to create the **rating** control. Render the input element as **rating** control using the input element id. The code example can be placed within the content description **&lt;div&gt;** element to declare the rating control and description in the **Tab** section and it can be appended with the header initialization code section **&lt;div&gt;** element.

For more information about rating, refer to the following link: 

[http://help.syncfusion.com/aspnetmvc/](http://help.syncfusion.com/aspnetmvc/)



&lt;!--Use the following codes with above Html contents--&gt;

@Html.EJ().Tab("DishType")



        &lt;div id="PizzaType" style="background-color: #F5F5F5"&gt;

            &lt;!--Rating control declaration--&gt;

            Rating:            

         @Html.EJ().**Rating**("RatingPizza").Value(4).Precision(Precision.Exact)



            &lt;!--Food item description--&gt;

            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

        &lt;/div&gt;



The following screenshot is the output for the given code example.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img20.png" Caption="Figure 11: First Tab content section with Rating Control"%}

**Sub Tab with Content** 

Each item has a variety of options, and these options are also specified in the limited space. So you can choose the **Tab** control that is used within the root **Tab** to specify more details.

The following code sample illustrates how to create the **Tab** control, within the root **Tab** element. This **HTML** code is appended within the previous **HTML** code section. To render the **Child****Tab** with its header, add this code sample within the first **Tab****&lt;div&gt;** element.

The following code example represents sub **Tab** control rendering.



&lt;!--Use the following codes with in the  above Html --&gt;



&lt;div id="PizzaType" style="background-color: #F5F5F5"&gt;

            &lt;!--Rating control declaration--&gt;

            Rating:            

         @Html.EJ().Rating("RatingPizza").Value(4).Precision(Precision.Exact)



            &lt;!--Food item description--&gt;

            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            @firstTab()





            @helper firstTab()

{

                @Html.EJ().Tab("PizzaMenu").Items(data =>

    {

        data.Add().ID("Corn-Spinach").Text("Corn Spinach").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src=" http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $70<br />

                Ingredients : cheese, sweet corn &amp; green capsicums. 

            &lt;br /&gt;

                Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.  

            &lt;/div&gt;

        &lt;/div&gt;

);



        data.Add().ID("ChickenDelite").Text("Chicken-Delite").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $100<br />

                Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.  

                &lt;br /&gt;

                Description: This is a tasty, elegant chicken dish that is easy to prepare. 

            &lt;/div&gt;

        &lt;/div&gt;

        );

    })

            } 



The following code example is used to position the image and content.



&lt;style type="text/css" class="cssStyles"&gt;

       /*reuse the previous rating control style section code*/                

       .ingredients {

            height: 180px;

            margin-top: 8px;

        }

        img {           

            float: left;        

            margin: 10px 26px 5px 1px;

        }

    &lt;/style&gt;



The following screenshot illustrates the first **Tab** with the sub **Tab** control.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img21.png" Caption="Figure 12: First Tab section with sub Tab control"%}

**Orientation Change**

Now, you can learn how to set the sub **Tab** orientation to vertical. By default, **Tab** control is rendered in horizontal orientation. You can change this orientation to vertical by using the **HeaderPosition** property. In the following code section, set the **Tab** header orientation as **Left**.

The following code section renders the sub **Tab** element in the vertical orientation.



&lt;!--Use the following codes with in the  above Html --&gt;

&lt;div id="PizzaType" style="background-color: #F5F5F5"&gt;

            &lt;!--Rating control declaration--&gt;

            Rating:            

         @Html.EJ().Rating("RatingPizza").Value(4).Precision(Precision.Exact)



            &lt;!--Food item description--&gt;

            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

            @firstTab()





            @helper firstTab()

{

                @Html.EJ().Tab("PizzaMenu")**.HeaderPosition(HeaderPosition.Left)**.Height("221").Items(data =>

    {

        data.Add().ID("Corn-Spinach").Text("Corn Spinach").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src=" http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $70<br />

                Ingredients : cheese, sweet corn &amp; green capsicums. 

            &lt;br /&gt;

                Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.  

            &lt;/div&gt;

        &lt;/div&gt;

);



        data.Add().ID("ChickenDelite").Text("Chicken-Delite").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $100<br />

                Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.  

                &lt;br /&gt;

                Description: This is a tasty, elegant chicken dish that is easy to prepare. 

            &lt;/div&gt;

        &lt;/div&gt;

        );

    })

            }



        &lt;/div&gt;



The following screenshot is the output of above steps.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img22.png" Caption="Figure 13: Sub Tab customized orientation"%}

**Header Image Customization**

In this application, you have to set the **Tab** header image for each Tab item, to specify image in **&lt;span&gt;** tag element during the **Tab** header declaration time.

Use the following code example to customize the header image.





&lt;style type="text/css" class="cssStyles"&gt;

.dish {

        display: inline-block;

        vertical-align: middle;

        margin: 0px -9px 0px 9px;

    }



    .pizzaImg {

        background: url("http://js.syncfusion.com/UG/Web/Content/rsz_chicken-delite.png") no-repeat;

        height: 25px;

        width: 25px;

    }

        /*reuse the previous header orientation code*/                

&lt;/style&gt;



The following code example is used to add the header image for the root **Tab** header element.



&lt;div id="DishType" style="width: 550px"&gt;

      &lt;ul&gt;

         &lt;li&gt;&lt;span class="dish pizzaImg"&gt;&lt;/span&gt;<a href="#PizzaType">Pizza Menu</a>&lt;/li&gt;  

         &lt;!—- reuse the remaining tab header --&gt;       

       &lt;/ul&gt;

       &lt;!—- reuse the previously defined first tab html content section--&gt;

&lt;/div&gt;





The following screenshot illustrates the **Tab** with the customized header image.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img23.png" Caption="Figure 14: Header Image Customization"%}

**Configure Contents to remaining Tab items**

The second and third **Tab** contents are declared in the same method as of the first **Tab** content declaration. These **Tabs** also consist of rating and sub **Tab** controls. 

The following code example is placed within the previous image customization of **HTML** code section.



           &lt;!—reuse the first tab header defined in previous image customization --&gt;

     &lt;li&gt;&lt;span class="dish sandwichImg"&gt;&lt;/span&gt;<a href="#SandwichType">Sandwich Menu</a>&lt;/li&gt;

     &lt;li&gt;&lt;span class="dish pastaImg"&gt;&lt;/span&gt;<a href="#PastaType">Pasta Menu</a>&lt;/li&gt;



Add second **Tab** contents in **&lt;div&gt;** element during initialization.



     &lt;div id="SandwichType" style="background-color: #F5F5F5"&gt;



        &lt;!--Rating control declaration--&gt;

        Rating: 

         @Html.EJ().Rating("RatingSandwich").Value(4).Precision(Precision.Exact)

        &lt;!--Food item description--&gt;

        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

        @secondTab()    



@helper secondTab()

{

                @Html.EJ().Tab("SandwichMenu").HeaderPosition(HeaderPosition.Left).Height("221").Items(data =>

    {

        data.Add().ID("GardenVeggie").Text("Garden Veggie").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/garden-veggie.png" alt="garden-veggie "&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $55<br />

                Ingredients : grilled chicken, corn &amp;olives. 

            &lt;br /&gt;

                Description: To make an appetizer pizza made with crescent roll dough, baked and topped with flavored cream cheese and crispy fresh vegetables. Broccoli, carrots, and bell peppers make this a wonderfully delicious vegetarian treat 

            &lt;/div&gt;



        &lt;/div&gt;

);

        data.Add().ID("ChickenTikka").Text("Chicken Tikka ").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-tikka.png" alt="chicken-tikka"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $100<br />

                Ingredients : onions, grilled chicken, chicken salami &amp; tomatoes.  

                &lt;br /&gt;

                Description: Juicy chunks of boneless chicken roasted on open fire.This takeaway favourite is freezer-friendly and quick to reheat, giving you the chance to get ahead. 

            &lt;/div&gt;

        &lt;/div&gt;





);

        data.Add().ID("PaneerTikka").Text("Paneer Tikka  ").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/paneer-tikka.png" alt="paneer-tikka"&gt;

            &lt;div class="ingredients"&gt;

                Rate    : $150

                &lt;br /&gt;

                Ingredients : onions, paneer & tomatoes.  

                &lt;br /&gt;

                Description: Delve into the tasty Paneer Tikka Kebabs made from marinated paneer or cottage cubes. Relish these grilled delicacies with green mint chutney and onion rings. 

            &lt;/div&gt;

        &lt;/div&gt;

);



    })



            }

        &lt;/div&gt;



Add third **Tab** contents in **&lt;div&gt;** element during initialization.



&lt;div id="PastaType" style="background-color: #F5F5F5"&gt;

        &lt;!--Rating control declaration--&gt;

        Rating:

        @Html.EJ().Rating("RatingPasta").Value(4).Precision(Precision.Exact)

        &lt;!--Food item description--&gt;

        <p>Pasta cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

        @thirdTab()



        @helper thirdTab()

{

            @Html.EJ().Tab("PastaMenu").HeaderPosition(HeaderPosition.Left).Height("221").Items(data =>

    {

        data.Add().ID("KheemaPasta").Text("Kheema Pasta ").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach.png" alt="kheema-pasta "&gt;

            &lt;div class="ingredients"&gt;

                &lt;p&gt;

                    Rate : $30<br />

                    Ingredients : chicken, onions, chilly, garlic &amp; tomatoes.&lt;br /&gt;

                    Description: Kheema pasta dish make with veg or non-veg type.It is delicious and can be served for dinner, brunch or evening snack. 

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/div&gt;

);

        data.Add().ID("TunaPasta").Text("Tuna Pasta").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/garden-fresh.png" alt="tuna-pasta"&gt;

            &lt;div class="ingredients"&gt;

                &lt;p&gt;

                    Rate : $55<br />

                    Ingredients : tomato ,olive, oninor &amp;garlic.&lt;br /&gt;

                    Description: Canned tuna is used to make this yummy tomato sauce.

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/div&gt;

 );

        data.Add().ID("ChannaPasta").Text("Channa Pasta").ContentTemplate(@&lt;div class="e-content"&gt;

            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/zesty-mushroons-and-tomatoes.png" alt="channa-asta"&gt;

            &lt;div class="ingredients"&gt;

                &lt;p&gt;

                    Rate : $30<br />

                    Ingredients : sautered spinach mix, sweet corn, parsley &amp;mozarella cheese. .&lt;br /&gt;

                    Description: This is a pasta dish make with leftover channa masala (chole). This can be made from scratch too by making the channa masala first and then tossing in the cooked pasta.

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/div&gt;



);

    })



        }

    &lt;/div&gt;



Apply the following styles to the **Tab**.



&lt;style type="text/css" class="cssStyles"&gt;

        /*to reuse the previous style section code and following css*/        

       .sandwichImg, .pastaImg {

            height: 25px;

            width: 25px;

        }

        .sandwichImg {

            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-fresh.png") no-repeat;                       

        }

        .pastaImg {

            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-veggie.png") no-repeat;                 

        }        

&lt;/style&gt;



The following screenshot illustrates the second **Tab** contents in **Tab** and the final hotel menu with rating, description and ingredients of the item in the **Tab** interface.



{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img24.png" Caption="Figure 15: Tab represents different items with load on demand support"%}

## Create your first Tab Control in ASP.NET	

The **ASP.NET Tab** control is an interface that displays the content in multiple sections. Each **TabPanel** consists of **HeaderText** or **HeaderTemplate** as well as a **ContentTemplate**. **Tab** is useful for a dashboard that contains limited space. The following section guides you to customize the **Tab** for displaying Hotel menu items, its rating details and ingredients.



![](getting-started-_images\getting-started-_img25.png)

_Figure_ _16__: Tab control with Hotel Menu items_

**Create Tab Control**

The **ASP.NET Tab** basically builds a dynamic interactive menu-driven interface from your content. The content can be text, graphics or HTML. You can create the **Tab** headers using the following tags. 

The following steps describe the creation of **Tab** control.  

1. You can create an **ASP** **Project** and add necessary **Dll** and script with the help of the given [ASP-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code example to the corresponding ASP page for **Tab** rendering.



**[ASPX]**

    &lt;form id="form1" runat="server"&gt;

        &lt;div&gt;

            &lt;ej:Tab ID="DishType" runat="server" Width="600px"&gt;

                &lt;Items&gt;

                    &lt;ej:TabItem Id="PizzaType" Text="Pizza Menu"&gt;

                        &lt;ContentSection&gt;

                            &lt;%-- Enter your contents here --%&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

                    &lt;ej:TabItem Id="SandwichType" Text="Sandwich Menu"&gt;

                        &lt;ContentSection&gt;

                            &lt;%-- Enter your contents here --%&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

                    &lt;ej:TabItem Id="PastaType" Text="Pasta Menu"&gt;

                        &lt;ContentSection&gt;

                            &lt;%-- Enter your contents here --%&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;

        &lt;/div&gt;

    &lt;/form&gt;



3.  Output of the above steps.



![](getting-started-_images\getting-started-_img26.png)

_Figure_ _17__: Tab control with Header only_

**Configure Content**

In this application a detailed description is provided to each item. You can specify the contents in the **Tab** section within the <**ContentSection** >using the following format. 



**[ASPX]**

&lt;!--Use the following codes with above Html --&gt;   

&lt;ej:Tab ID="DishType" runat="server" Width="500px"&gt;

                &lt;Items&gt;

                    &lt;ej:TabItem Id="PizzaType" Text="Pizza Menu"&gt;

                        &lt;ContentSection&gt;

                            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

&lt;!--Reuse remaining Tab contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;

You can provide more customization to the **Tab** with rating control as content to describe the item rating value.

The following screenshot is the output of the above code example:

{% include image.html url="\js\Tab\getting-started-_images\getting-started-_img27.png" Caption="Figure 18: First Tab content section with Rating Control"%}

**Create the Rating** 

The **ASP.NET Rating** control provides you an intuitive rating experience that allows you to select the number of stars that represents the rating. The following code example explains you the rating control creation. Render the rating control using the &lt;ej:Rating&gt; tag. The code example is placed within the content description( &lt;ContentSection &gt; )element to declare the rating control and description in the **Tab** section and it can be appended with the control initialization code section &lt;ej:Tab&gt; element using the following format.

**[ASPX]**

&lt;!--Use the following codes with above Html --&gt;   

&lt;ej:Tab ID="DishType" runat="server" Width="500px"&gt;

                &lt;Items&gt;

                    &lt;ej:TabItem Id="PizzaType" Text="Pizza Menu"&gt;

                        &lt;ContentSection&gt;

                            &lt;div&gt;

                                Rating : 

                                 &lt;div&gt;                                     &lt;ej:Rating ID="GardenPizza" Precision="Exact" Value="4.9" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;                                

                            &lt;/div&gt;

                            <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

 &lt;!--Reuse remaining Tab contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;                 



The following screenshot is the output of above code example:

![](getting-started-_images\getting-started-_img28.png)

_Figure_ _19__:____First Tab content section with Rating Control_

**Sub Tab with Content** 

Each item is having a variety of options and these options are also specified in the limited space. So you can choose the **Tab** control that is used within the root Tab to specify more details.

The following code example illustrates how to create the **Tab** control within the root Tab element. This HTML code is appended within the previous HTML code section. To render the child **Tab** with its header, add this code example within the &lt;ej:Tab &gt; tag using the following format.

The sub **Tab** control rendering is represented in the following code example.

**[ASPX]**

&lt;!--Use the following codes with in the  above Html --&gt;

&lt;ej:Tab ID="DishType" runat="server" Width="500px"&gt;

    &lt;Items&gt;

        &lt;ej:TabItem Id="PizzaType" Text="Pizza Menu"&gt;

            &lt;ContentSection&gt;

                &lt;div&gt;

                    Rating : 

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="GardenPizza" Precision="Exact" Value="4.9" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                &lt;/div&gt;

                <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;ej:Tab ID="PizzaTab" runat="server"&gt;

                    &lt;Items&gt;

                        &lt;ej:TabItem Id="PizzaMenu" Text="Corn Spinach"&gt;

                            &lt;ContentSection&gt;

                                &lt;img src=" http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"&gt;

                                &lt;div class="ingredients"&gt;

                                    Rate    : $70<br />

                                    Ingredients : cheese, sweet corn &amp; green capsicums.&lt;br /&gt;

                                    Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.  

                                &lt;/div&gt;

                            &lt;/ContentSection&gt;

                        &lt;/ej:TabItem&gt;

                        &lt;ej:TabItem Id="PizzaMenu1" Text="Chicken-Delite"&gt;

                            &lt;ContentSection&gt;

                                &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite"&gt;

                                &lt;div class="ingredients"&gt;

                                    Rate    : $100<br />

                                    Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.&lt;br /&gt;

                                    Description: This is a tasty, elegant chicken dish that is easy to prepare. 

                                &lt;/div&gt;

                            &lt;/ContentSection&gt;

                        &lt;/ej:TabItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:Tab&gt;



            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

&lt;!--Reuse remaining Tab contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;



The following code example positions the image and content.

**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;       

       .ingredients {

            height: 180px;

            margin-top: 8px;

        }

        img {           

            float: left;        

            margin: 10px 26px 5px 1px;

        }

    &lt;/style&gt;



The following screenshot illustrates the first **Tab** with the sub **Tab** control.

![](getting-started-_images\getting-started-_img29.png)

_Figure_ _20__:_ ___first Tab section with sub Tab control._

**Orientation Change**

Now, you can learn how to set the sub **Tab** orientation to vertical. By default, **Tab** control is rendered in horizontal orientation. You can change this orientation to vertical by using the **HeaderPosition** property. In the following code section, set the **Tab** header orientation as **Left**.

The following code section renders the sub **Tab** element in the vertical orientation.



**[ASPX]**

&lt;!--Use the following codes with in the  above Html --&gt;

&lt;ej:Tab ID="DishType" runat="server" Width="500px"&gt;

    &lt;Items&gt;

        &lt;ej:TabItem Id="PizzaType" Text="Pizza Menu"&gt;

            &lt;ContentSection&gt;

                &lt;div&gt;

                    Rating : 

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="gardenPizza" Precision="Exact" Value="4.9" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                &lt;/div&gt;

                <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                &lt;ej:Tab ID="PizzaTab" runat="server" HeaderPosition="Left" Height="221px"&gt;

                    &lt;Items&gt;

                        &lt;ej:TabItem Id="PizzaMenu" Text="Corn Spinach"&gt;

                            &lt;ContentSection&gt;

                                &lt;img src=" http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"&gt;

                                &lt;div class="ingredients"&gt;

                                    Rate    : $70<br />

                                    Ingredients : cheese, sweet corn &amp; green capsicums.&lt;br /&gt;

                                    Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.  

                                &lt;/div&gt;

                            &lt;/ContentSection&gt;

                        &lt;/ej:TabItem&gt;

                        &lt;ej:TabItem Id="PizzaMenu1" Text="Chicken-Delite"&gt;

                            &lt;ContentSection&gt;

                                &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite"&gt;

                                &lt;div class="ingredients"&gt;

                                    Rate    : $100<br />

                                    Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.&lt;br /&gt;

                                    Description: This is a tasty, elegant chicken dish that is easy to prepare. 

                                &lt;/div&gt;

                            &lt;/ContentSection&gt;

                        &lt;/ej:TabItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:Tab&gt;

            &lt;/ContentSection&gt;

        &lt;/ej:TabItem&gt;

&lt;!--Reuse remaining Tab contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;



The following screenshot is the output of the above steps.

![](getting-started-_images\getting-started-_img30.png)

_Figure_ _21__:  Sub Tab customized orientation_

**Header Image Customization**

In this application, you have to set the **Tab** header image for each **Tab** item to specify image in “**ImageCssClass”** property during the **Tab** header declaration time.

Use the following code example to customize the header image.

**[CSS]**



&lt;style type="text/css" class="cssStyles"&gt;

.dish {

        display: inline-block;

        vertical-align: middle;

        margin: 0px -9px 0px 9px;

    }

    .pizzaImg {

        background: url("http://js.syncfusion.com/UG/Web/Content/rsz_chicken-delite.png") no-repeat;

        height: 25px;

        width: 25px;

    }

        /*reuse the previous code*/                

&lt;/style&gt;



The following code example is used to add the header image for the root tab header element.

**[ASPX]** 

****

&lt;!--Use the following codes with in the  above Html --&gt; 

&lt;ej:TabItem Id="pizzaType" Text="Pizza Menu" ImageCssClass="dish pizzaImg"&gt;

                        &lt;ContentSection&gt;

                            &lt;!—- reuse the previously defined first tab html content section--&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

&lt;!—- reuse the remaining tab contents --&gt;

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;   



The following screenshot illustrates the **Tab** with the customized header image.

![](getting-started-_images\getting-started-_img31.png)

    _Figure_ _22__:  Header Image Customization_

**Configure Contents to remaining Tab items**

The second and third **Tab** contents are declared in the same method as of the first **Tab** content declaration. These **Tabs** also consist of rating and sub **Tab** controls. 

Add second **Tab** contents with header image in &lt;ej:Tab &gt; element during initialization.

**[ASPX]**

&lt;!--Use the following codes with in the  above Html --&gt;                 

&lt;ej:TabItem Id="SandwichType" Text="Sandwich Menu" ImageCssClass="dish sandwichImg"&gt;

                        &lt;ContentSection&gt;

                            &lt;div&gt;

                                Rating : 

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="RatingSandwich" Value="4.9" Precision="Exact" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                            &lt;/div&gt;

                            <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                            &lt;ej:Tab ID="SandwichTab" runat="server" HeaderPosition="Left" Height="221px"&gt;

                                &lt;Items&gt;

                                    &lt;ej:TabItem Id="GardenVeggie" Text="Garden Veggie"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/garden-veggie.png" alt="garden-veggie "&gt;

                                            &lt;div class="ingredients"&gt;

                                                Rate    : $55<br />

                                                Ingredients : grilled chicken, corn &amp;olives.&lt;br /&gt;

                                                Description: To make an appetizer pizza made with crescent roll dough, baked and topped with flavored cream cheese and crispy fresh vegetables. Broccoli, carrots, and bell peppers make this a wonderfully delicious vegetarian treat 

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                    &lt;ej:TabItem Id="ChickenTikka" Text="Chicken Tikka"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-tikka.png" alt="chicken-tikka"&gt;

                                            &lt;div class="ingredients"&gt;

                                                Rate    : $100<br />

                                                Ingredients : onions, grilled chicken, chicken salami &amp; tomatoes.&lt;br /&gt;

                                                Description: Juicy chunks of boneless chicken roasted on open fire. This takeaway favourite is freezer-friendly and quick to reheat, giving you the chance to get ahead. 

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                    &lt;ej:TabItem Id="paneerTikka" Text="Paneer Tikka"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/paneer-tikka.png" alt="paneer-tikka"&gt;

                                            &lt;div class="ingredients"&gt;

                                                Rate    : $150

                                                &lt;br /&gt;

                                                Ingredients : onions, paneer & tomatoes.

                                                &lt;br /&gt;

                                                Description: Delve into the tasty Paneer Tikka Kebabs made from marinated paneer or cottage cubes. Relish these grilled delicacies with green mint chutney and onion rings. 

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                &lt;/Items&gt;

                            &lt;/ej:Tab&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

&lt;!--Reuse remaining Tab contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;



Add third **Tab** contents with header image in &lt;ej:Tab &gt; element during initialization.

**[ASPX]**

&lt;ej:TabItem Id="PastaType" Text="Pasta Menu" ImageCssClass="dish pastaImg"&gt;

                        &lt;ContentSection&gt;

                            &lt;div&gt;

                                Rating : 

                                 &lt;div&gt;

                                     &lt;ej:Rating ID="Rating1" Value="4.9" Precision="Exact" runat="server"&gt;&lt;/ej:Rating&gt;

                                 &lt;/div&gt;

                            &lt;/div&gt;

                            <p>Pasta cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.&lt;/p&gt;

                            &lt;ej:Tab ID="Tab2" runat="server" HeaderPosition="Left" Height="221px"&gt;

                                &lt;Items&gt;

                                    &lt;ej:TabItem Id="kheemaPasta" Text="Kheema Pasta"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach.png" alt="kheema-pasta "&gt;

                                            &lt;div class="ingredients"&gt;

                                                &lt;p&gt;

                                                    Rate : $30<br />

                                                    Ingredients : chicken, onions, chilly, garlic &amp; tomatoes.&lt;br /&gt;

                                                    Description: Kheema pasta dish make with veg or non-veg type.It is delicious and can be served for dinner, brunch or evening snack. 

                                                &lt;/p&gt;

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                    &lt;ej:TabItem Id="tunaPasta" Text="Tuna Pasta"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/garden-fresh.png" alt="tuna-pasta"&gt;

                                            &lt;div class="ingredients"&gt;

                                                &lt;p&gt;

                                                    Rate : $55<br />

                                                    Ingredients : tomato ,olive, oninor &amp;garlic.&lt;br /&gt;

                                                    Description: Canned tuna is used to make this yummy tomato sauce.

                                                &lt;/p&gt;

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                    &lt;ej:TabItem Id="channaPasta" Text="Channa Pasta"&gt;

                                        &lt;ContentSection&gt;

                                            &lt;img src="http://js.syncfusion.com/demos/web/images/accordion/zesty-mushroons-and-tomatoes.png" alt="channa-asta"&gt;

                                            &lt;div class="ingredients"&gt;

                                                &lt;p&gt;

                                                    Rate : $30<br />

                                                    Ingredients : sautered spinach mix, sweet corn, parsley &amp;mozarella cheese. .&lt;br /&gt;

                                                    Description: This is a pasta dish make with leftover channa masala (chole). This can be made from scratch too by making the channa masala first and then tossing in the cooked pasta.

                                                &lt;/p&gt;

                                            &lt;/div&gt;

                                        &lt;/ContentSection&gt;

                                    &lt;/ej:TabItem&gt;

                                &lt;/Items&gt;

                            &lt;/ej:Tab&gt;

                        &lt;/ContentSection&gt;

                    &lt;/ej:TabItem&gt;

&lt;!--Reuse remaining contents--&gt;  

                &lt;/Items&gt;

            &lt;/ej:Tab&gt;



Apply the following styles to the **Tab**.

**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

        /*to reuse the previous style section code and following css*/        

       .sandwichImg, .pastaImg {

            height: 25px;

            width: 25px;

        }

        .sandwichImg {

            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-fresh.png") no-repeat;                       

        }

        .pastaImg {

            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-veggie.png") no-repeat;                 

        }        

&lt;/style&gt;



The following screenshot illustrates you the second **Tab** contents in **Tab** and the final hotel menu with rating, description and ingredients of the item in the **Tab** interface.

![](getting-started-_images\getting-started-_img32.png)

_Figure_ _23__:  Tab represents different items_

