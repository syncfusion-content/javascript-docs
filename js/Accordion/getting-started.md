---
layout: post
title: getting-started
description: getting started
platform: js
control: Accordion 
documentation: ug
---

# Getting Started

This section explains briefly about how to create an **Accordion** in your application with **JavaScript** and **ASP.NET MVC**.

## Create your first Accordion in JavaScript

**Configure Accordion**

This section encompasses the details on how you can configure the **Accordion** control in your application and customize it with various properties such as multiple open, rounded corner and icons for the **Accordion** header according to your requirement.

The following screenshot illustrates you the usage of **Accordion** control in listing the controls under the Essential Studio products. 

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img1.png" Caption="Figure 1:  Accordion control used to list controls under Essential Studio products"%}

The usage of **Accordion** control is described in the following sections.

**Create a Simple Accordion**

* Create an **HTML** file and add the following references to the required libraries.

{% highlight html %}

**[HTML]**
<html>
<head>
    <title>Essential Studio for JavaScript : Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- Add Accordion element here. -->
</body>
</html><div id="accordion" style="width: 400px">
        <h3>
            <a href="#">Essential Studio ASP.NET</a>
        </h3>
        <div>
            <!-- add accordion contents here to load contents under this header -->
            <ul>
                <li>
                    <h4>DocIO</h4>
                </li>
                <li>
                    <h4>Pdf  </h4>
                </li>
                <li>
                    <h4>Gauge  </h4>
                </li>
                <li>
                    <h4>Schedule  </h4>
                </li>
                <li>
                    <h4>Diagram  </h4>
                </li>
                <li>
                    <h4>Tools </h4>
                </li>
            </ul>
        </div>
        <h3>
            <a href="#">Essential Studio ASP.NET MVC</a>
        </h3>
        <div>
            <!-- add accordion contents here to load contents under this header -->
            <ul>
                <li>
                    <h4>Chart </h4>
                </li>
                <li>
                    <h4>Grid  </h4>
                </li>
                <li>
                    <h4>Gantt  </h4>
                </li>
                <li>
                    <h4>Schedule  </h4>
                </li>
                <li>
                    <h4>Diagram  </h4>
                </li>
            </ul>
        </div>
        <h3>
            <a href="#">Essential Studio Javascript</a>
        </h3>
        <div>
            <!-- add accordion contents here to load contents under this header -->
            <ul>
                <li>
                    <h4>Chart </h4>
                </li>
                <li>
                    <h4>Grid  </h4>
                </li>
                <li>
                    <h4>Gantt  </h4>
                </li>
                <li>
                    <h4>Schedule  </h4>
                </li>
                <li>
                    <h4>Diagram  </h4>
                </li>
            </ul>
        </div>
    </div>


{% endhighlight %}



* Add a **&lt;div&gt;** element. It is a container for Accordion control.



{% highlight html %}

**[HTML]**

<body>
<div id="accordion" style="width: 400px">
<h3>
<a href="#">Essential Studio ASP.NET</a></h3>
<div><!-- add accordion contents here to load contents under this header -->
<ul>
<li>
<h4>DocIO</h4>
</li>
<li>
<h4>Pdf  </h4>
</li>
<li>
<h4>Gauge  </h4>
</li>
<li>
<h4>Schedule  </h4>
</li>
<li>
<h4>Diagram  </h4>
</li>
<li>
<h4>Tools </h4>
</li>
</ul>

</div>
<h3>
<a href="#">Essential Studio ASP.NET MVC</a></h3>
<div><!-- add accordion contents here to load contents under this header -->
<ul>
<li>
<h4>Chart </h4>
</li>
<li>
<h4>Grid  </h4>
</li>
<li>
<h4>Gantt  </h4>
</li>
<li>
<h4>Schedule  </h4>
</li>
<li>
<h4>Diagram  </h4>
</li>
</ul>
</div>
<h3>
<a href="#">Essential Studio Javascript</a></h3>
<div><!-- add accordion contents here to load contents under this header -->
<ul>
<li>
<h4>Chart </h4>
</li>
<li>
<h4>Grid  </h4>
</li>
<li>
<h4>Gantt  </h4>
</li>
<li>
<h4>Schedule  </h4>
</li>
<li>
<h4>Diagram  </h4>
</li>
</ul>
</div>
</div>
</body>



{% endhighlight %}



* Create the **Accordion** control as follows.



{% highlight js %}

**[JavaScript]**
  <script type="text/javascript">
        $(function () {
            // document ready
            // Initialize Accordion control creation.
            $("#accordion").ejAccordion();
        });
    </script>


{% endhighlight %}



* You can execute the above code example to display the **Accordion** control with simple control list.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img2.png" Caption="Figure 2: Simple Accordion content"%}

You can customize the **Accordion** control using various properties. The **Accordion** control properties and its default values are described in the following section.

**Configure Multiple Open**

You can have multiple **Accordion** tabs opened to view all products at a time. To achieve this set the **enableMultipleOpen**property of the **Accordion** control to true.

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img3.jpeg)_**Note: enableMultipleOpenproperty is false by default.**_ 



You can also open all the panels during initialization using the **selectedItems** property of the **Accordion** control. The following code sample illustrates the opening of multiple tabs by passing the tab index values of tab.

{% highlight js %}

**[JavaScript]**
    <script type="text/javascript">
        $(function () {
            $("#accordion").ejAccordion({
                enableMultipleOpen: true, /* To set the multiple content panels  active at a time   */
                selectedItems: [0, 1, 2] /* To set the selected panels  active at a time   */
            });
        });
    </script>


{% endhighlight %}



**Accordion** control with **enableMultipleOpen** property is illustrated in the following screen shot.

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img4.png" Caption="Figure 3: Accordion control with multiple open"%}

**Setting rounded corner**

**Accordion** control, by default, is rendered in a regular rectangle. You can modify the regular rectangles with rounded corners by setting the **showRoundedCorner** property to **True**.

> ![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img5.jpeg)_**Note: showRoundedCornerproperty is False by default.**_



{% highlight js %}

**[JavaScript]**
    <script type="text/javascript">
        $(function () {
            $("#accordion").ejAccordion({
                enableMultipleOpen: true,
                selectedItems: [0, 1, 2],
                showRoundedCorner: true/* To set rounded corner for the accordion headers   */
            });
        });
    </script>


{% endhighlight %}





The following screenshot illustrates the **Accordion** control with rounded corners.

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img6.png" Caption="Figure 4: Accordion with rounded corner"%}

**Customize Icon**

You can customize the **Header** icon using **customIcon** property. This property has two features such as **header** and **selectedHeade**r. By default, the classes of **header** and **selectedHeader** are **e-collapse** and **e-expand** respectively**.**

You can change the + and- symbols in the **Accordion**header, that are the default icons with Up or Down arrow icons. 

Up or Down arrow icons are available in **e-arrowheadup** and **e- arrowheaddown** classes respectively in the ej.widjets.core.min.css stylesheets from the sample. 

You can set the Up or Down arrow icon to **Accordion** header, by adding **e-arrowheadup** and **e-arrowheaddown** class to **selectedHeader** and **header** properties respectively.

{% highlight js %}

**[JavaScript]**
    <script type="text/javascript">
        $(function () {
            $("#accordion").ejAccordion({
                enableMultipleOpen: true,
                selectedItems: [0, 1, 2],
                showRoundedCorner: true,
                customIcon: {
                    header: "e-arrowheaddown", /*  To set icon for the collapsed accordion headers  */
                    selectedHeader: "e-arrowheadup"/*  To set icon for the selected accordion headers  */
                }
            });
        });
    </script>


{% endhighlight %}



The following screenshot illustrates the customization of **selectedHeader** and **header** of the **Accordion** control.

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img7.png" Caption="Figure 5: Accordion with customized icon style"%}

## Create your first Accordion in MVC 

The **ASP.NET MVC Accordion** control allows you to provide multiple panes and display them one at a time. In this section, you can learn how the **Accordion** control is configured and how to use it in your application. 

**Configure Accordion**

This section explains you the details on how to configure the **Accordion** control in your application and how to customize it with various properties such as multiple open, rounded corner and icons for the **Accordion** header according to your requirement.

The following screenshot illustrates you the usage of **Accordion** control in listing the controls under the Essential Studio products. 

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img8.png" Caption="Figure 6:  Accordion control used to list controls under Essential Studio products"%}

In the above screenshot , the **Accordion** contains a template for its Header and its content. In this **Accordion** application, you can list the controls under Essential Studio.

The usage of **Accordion** control is described in the following sections.

**Create a Simple Accordion**

**ASP.NET MVC Accordion** basically renders using a div element. The following step describes the creation of **Accordion** control.

1. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code sample to the corresponding view page for **Accordion** rendering.

3. Add a **&lt;div&gt;** element. It is a container for **Accordion** control. Render the **Accordion** control as follows.



**[CSHTML]**

&lt;div id ="ProductsAccordion" style="width: 400px"&gt;

    &lt;h3&gt;

        <a href ="#">Essential Studio ASP.NET</a>

    &lt;/h3&gt;

    &lt;div&gt;

        &lt;!-- add accordion contents here to load contents under this header --&gt;

        &lt;ul&gt;

            &lt;li&gt;

                <h4>DocIO</h4>

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Pdf  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Gauge  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Schedule  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Diagram  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Tools &lt;/h4&gt;

            &lt;/li&gt;

        &lt;/ul&gt;



    &lt;/div&gt;

    &lt;h3&gt;

        <a href ="#">Essential Studio ASP.NET MVC</a>

    &lt;/h3&gt;

    &lt;div&gt;

        &lt;!-- add accordion contents here to load contents under this header --&gt;

        &lt;ul&gt;

            &lt;li&gt;

                <h4>Chart &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Grid  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Gantt  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Schedule  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Diagram  &lt;/h4&gt;

            &lt;/li&gt;

        &lt;/ul&gt;

    &lt;/div&gt;

    &lt;h3&gt;

        <a href ="#">Essential Studio Javascript</a>

    &lt;/h3&gt;

    &lt;div&gt;

        &lt;!-- add accordion contents here to load contents under this header --&gt;

        &lt;ul&gt;

            &lt;li&gt;

                <h4>Chart &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Grid  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Gantt  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Schedule  &lt;/h4&gt;

            &lt;/li&gt;

            &lt;li&gt;

                <h4>Diagram  &lt;/h4&gt;

            &lt;/li&gt;

        &lt;/ul&gt;

    &lt;/div&gt;

    &lt;/div&gt;





    @Html.EJ().Accordion("ProductsAccordion")



4. Execute the above code example to display the **Accordion**control with simple control list.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img9.png" Caption="Figure 7: Simple Accordion content"%}

You can customize the **Accordion** control using various properties. The **Accordion** control properties and its default values are described in the following section.

**Configure Multiple Open**

You can open multiple **Accordion** tabs to view all products at a time. To render this set the **EnableMultipleOpen** property of the **Accordion** control to true.



![http://help.syncfusion.com/UG/orubase/ImagesExt/image751_4.png](getting-started_images\getting-started_img10.png)_**Note: EnableMultipleOpenproperty is false by default.**_ 



You can also open all the panels during initialization using the **SelectedItems** property of the **Accordion** control. The following code sample illustrates the opening of multiple tabs by passing the tab index values of tab.

[CSHTML]

&lt;div id="ProductsAccordion" style="width: 400px"&gt;

    &lt;!--Add Accordion contents as like from the above code snippet --&gt;

&lt;/div&gt;





@{

    List<int> selecteditem = new List<int>() { 0, 1, 2 };

}

@Html.EJ().Accordion("ProductsAccordion").EnableMultipleOpen(true).SelectedItems(selecteditem)





**Accordion** control with **EnableMultipleOpen**property is illustrated in the following screenshot.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img11.png" Caption="Figure 8: Accordion control with multiple open"%}

**Set Rounded corner**

**Accordion** control by default is rendered in a regular rectangle. You can modify the regular rectangles with rounded corners by setting the **ShowRoundedCorner** property to true.



![http://help.syncfusion.com/UG/orubase/ImagesExt/image751_4.png](getting-started_images\getting-started_img12.png)_**Note: ShowRoundedCorner property is false by default.**_





**[CSHTML]**

&lt;div id="ProductsAccordion" style="width: 400px"&gt;

    &lt;!--Add Accordion contents as like from the above code snippet --&gt;

&lt;/div&gt;





@{

    List<int> selecteditem = new List<int>() { 0, 1, 2 };

}

@Html.EJ().Accordion("ProductsAccordion").EnableMultipleOpen(true).SelectedItems(selecteditem).ShowRoundedCorner(true)



The following screenshot illustrates the **Accordion** control with rounded corners.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img13.png" Caption="Figure 9: Accordion with rounded corner"%}

**Customize Icon**

You can customize the **Header**icon using **CustomIcon**property.This property is having two features such as**Header** and **SelectedHeade**r. By default, the classes of **Header** and **SelectedHeader** are **e-collapse** and**e-expand**respectively**.**

You can change the + and - symbols in the **Accordion**header, that are default icons with Up and Down arrow icons. 

Up and Down arrow icons are available in **e-arrowheadup** and **e- arrowheaddown** classes respectively in the **ej.widjets.core.min.css** stylesheets from the sample. 

You can set the Up/Down arrow icon to **Accordion** header, by adding **e-arrowheadup** and **e-arrowheaddown** class to **SelectedHeader**and **Header** properties respectively.

[CSHTML]

&lt;div id="ProductsAccordion" style="width: 400px"&gt;

    &lt;!--Add Accordion contents as like from the above code snippet --&gt;

&lt;/div&gt;





@{

    List<int> selecteditem = new List<int>() { 0, 1, 2 };

}

@Html.EJ().Accordion("ProductsAccordion").EnableMultipleOpen(true).SelectedItems(selecteditem).ShowRoundedCorner(true).CustomIcon(icon => icon.SelectedHeader("e-arrowheadup").Header("e-arrowheaddown"))





The following screenshot illustrates the customization of **SelectedHeader** and **Header** of the **Accordion** control.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img14.png" Caption="Figure 10: Accordion with customized icon style"%}

## Create your first Accordion in ASP.NET

The **ASP.NET WebForms Accordion** control allows you to provide multiple panes and display them one at a time. In this section, you can learn how the **Accordion** controlis configured and how to use it in your application. 

**Configure Accordion**

This section explains you the details on how to configure the **Accordion** control in your application and how to customize it with various properties such as multiple open, rounded corner and icons for the **Accordion** header according to your requirement.

The following screenshot illustrates you the usage of **Accordion** control in listing the controls under the **Essential Studio** products. 



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img15.png" Caption="Figure 11:  Accordion control used to list controls under Essential Studio products"%}

In the above screenshot , the **Accordion** contains a template for its **Header** and its content. In this **Accordion** application, you can list the controls under **Essential Studio**.

**Create a Simple Accordion**

**ASP.NET WebForms Accordion** basically renders with list of **AccordionItem**.The following steps describe the creation of **Accordion** control.

* You can create an **ASP.NET WebForms Project** and add necessary **Dll’s** and **Scripts** with the help of the given [ASP.NET WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* Add the following code example to the corresponding aspx page to render **Accordion**.

* Add **Accordion** widget, and initialize **Accordion** control as follows.



**[ASPX]**

&lt;div id="control" style="width: 400px"&gt;

        &lt;ej:Accordion ID="Accordion1" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:AccordionItem Text="Essential Studio ASP.NET"&gt;

                    &lt;ContentSection&gt;

                        &lt;ul&gt;

                            &lt;li&gt;

                                <h5>DocIO</h5>

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Pdf  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Gauge  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Schedule  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Diagram  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Tools &lt;/h5&gt;

                            &lt;/li&gt;

                        &lt;/ul&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:AccordionItem&gt;

                &lt;ej:AccordionItem Text="Essential Studio ASP.NET MVC"&gt;

                    &lt;ContentSection&gt;

                        &lt;ul&gt;

                            &lt;li&gt;

                                <h5>Chart &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Grid  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Gantt  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Schedule  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Diagram  &lt;/h5&gt;

                            &lt;/li&gt;

                        &lt;/ul&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:AccordionItem&gt;

                &lt;ej:AccordionItem Text="Essential Studio Javascript"&gt;

                    &lt;ContentSection&gt;

                        &lt;ul&gt;

                            &lt;li&gt;

                                <h5>Chart &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Grid  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Gantt  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Schedule  &lt;/h5&gt;

                            &lt;/li&gt;

                            &lt;li&gt;

                                <h5>Diagram  &lt;/h5&gt;

                            &lt;/li&gt;

                        &lt;/ul&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:AccordionItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Accordion&gt;

    &lt;/div&gt;





* Execute the above code sample to display the **Accordion** control with simple control list.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img16.png" Caption="Figure 12: Simple Accordion content"%}

You can customize the **Accordion** control using various properties. The **Accordion** control properties and its default values are described in the following section.

**Configure Multiple Open**

You can open multiple **Accordion** tabs to view all products at a time. To render this set the **EnableMultipleOpen** property of the **Accordion** control to true



![http://help.syncfusion.com/UG/orubase/ImagesExt/image751_4.png](getting-started_images\getting-started_img17.png)_**Note: EnableMultipleOpen property is false by default.**_ 



You can also open all the panels during initialization using the **SelectedItems** property of the **Accordion** control. The following code sample illustrates the opening of multiple tabs by passing the tab index values to **SelectedItems**property.



**[ASPX]**

&lt;div id="control" style="width: 400px"&gt;

    &lt;ej:Accordion ID="Accordion1" runat="server" EnableMultipleOpen="true"&gt;

        &lt;Items&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>DocIO</h5>

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Pdf  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gauge  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Tools &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET MVC"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio Javascript"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



**Accordion** control with **EnableMultipleOpen** property with value as true is illustrated in the following screenshot.



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img18.png" Caption="Figure 13: Accordion control with EnableMultipleOpen as true"%}

**SettingRounded corner**

**Accordion** control by default is renders in a regular rectangle. You can modify the regular rectangles with rounded corners by setting the**ShowRoundedCorner**property to **“True”**.



![http://help.syncfusion.com/UG/orubase/ImagesExt/image751_4.png](getting-started_images\getting-started_img19.png)_**Note: ShowRoundedCorner property is False by default.**_

> 

**[ASPX]**

&lt;div id="control" style="width: 400px"&gt;

    &lt;ej:Accordion ID="Accordion1" runat="server" EnableMultipleOpen="true" ShowRoundedCorner="true"&gt;

        &lt;Items&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>DocIO</h5>

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Pdf  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gauge  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Tools &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET MVC"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio Javascript"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



The following screenshot illustrates the **Accordion** control with rounded corners



{% include image.html url="\js\Accordion\getting-started_images\getting-started_img20.png" Caption="Figure 14: Accordion with rounded corner"%}

**Customize Icon**

You can customize the **Header**icon using **CustomIcon**property.This property is having two features such as**Header** and **SelectedHeade**r. By default, the classes of **Header** and **SelectedHeader** are **e-collapse** and**e-expand**respectively**.**

You can change the +/- symbol in the **Accordion** header, that are default icons with Up/Down arrow icon. 

Up/Down arrow icons are available in **e-arrowheadup** and **e- arrowheaddown** classes respectively in the **ej.widjets.core.min.css** stylesheets from the sample. 

You can set the Up/Down arrow icon to **Accordion** header, by adding **e-arrowheadup** and **e-arrowheaddown** class to **SelectedHeader** and **Header** properties respectively.



**[ASPX]**

&lt;div id="control" style="width: 400px"&gt;

    &lt;ej:Accordion ID="Accordion1" runat="server" EnableMultipleOpen="true" ShowRoundedCorner="true"&gt;

        &lt;CustomIcon Header="e-arrowheaddown" SelectedHeader="e-arrowheadup"/&gt;

        &lt;Items&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>DocIO</h5>

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Pdf  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gauge  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Tools &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio ASP.NET MVC"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

            &lt;ej:AccordionItem Text="Essential Studio Javascript"&gt;

                &lt;ContentSection&gt;

                    &lt;ul&gt;

                        &lt;li&gt;

                            <h5>Chart &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Grid  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Gantt  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Schedule  &lt;/h5&gt;

                        &lt;/li&gt;

                        &lt;li&gt;

                            <h5>Diagram  &lt;/h5&gt;

                        &lt;/li&gt;

                    &lt;/ul&gt;

                &lt;/ContentSection&gt;

            &lt;/ej:AccordionItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Accordion&gt;

&lt;/div&gt;



The following screenshot illustrates the customization of **SelectedHeader** and **Header** of the **Accordion** control.

{% include image.html url="\js\Accordion\getting-started_images\getting-started_img21.png" Caption="Figure 15: Accordion with customized icon style"%}

