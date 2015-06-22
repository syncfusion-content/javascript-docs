---
layout: post
title: Rating-Customization
description: rating customization
platform: js
control: Rating
documentation: ug
---

# Rating Customization

## Setting Value

The **Value** property sets the display value of the Rating. For example, when the **Value** property is set to be **four**, the Rating control renders four ratings. By default, **Value** property’s value is **one**.

The following code example is used to render the **Rating** control with customized value.

 Add the following HTML to render Rating with customized value.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}

        // Add the following script to render Rating with customized value.
  
        $("#rating").ejRating({ value: 4 });
 
{% endhighlight %}

The following screenshot illustrates the **Rating** with custom defined value.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img1.png" Caption="Rating with Value"%}

### Min Value

**EJ Rating** control provides support for setting **minimum** **value**. This is achieved by adding minValue property. When the minValue property is set, the Ratin value starts with **minValue**+1.

The following code example is used to render the **Rating** control with **minimum** **rating**.

 Add the following HTML to render Rating with minimum value.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}


        // Add the following script to render Rating with minimum value.

        $("#rating").ejRating({ minValue: 3});
   
{% endhighlight %}

The following screenshot illustrates **Rating** with **minimum** **value**.         

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img2.png" Caption="Rating with minimum value"%}

### Max Value

**EJ** **Rating** **control** provides support for setting **maximum** **value**. This is achieved by adding the **maxValue** property**.** By default, maxValue is five.

The following code example is used to render the Rating control with **maximum** **rating**.

 Add the following HTML to render Rating with maximum value.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}

        // Add the following script to render Rating with minimum value.

        $("#rating").ejRating({ maxValue: 10});
    
{% endhighlight %}

The following screenshot illustrates the **Rating** with **maximum** **value**.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img3.png" Caption="Rating with maximum value"%}

## Set Precision

In a real-time movie **Rating** scenario, you can set **Precision** between two whole numbers such as 2.5 or 3.7 and it is done using the property **Precision** by changing the value to **ej.Rating.Precision.Half** or **ej.Rating.Precision.Exact.** By default, **Precision** is **Full.**

The following code example is used to render the **Rating** control with **Precision**.

 Add the following HTML to render Rating with Precision.
{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Full Precision:
                </td>
                <td>
                    <input id="rating" type="text" />
                   
                </td>
            </tr>   
            <tr>
                <td valign="top">Half Precision:
                </td>
                <td>
                    <input id="halfRating" type="text" />
                   
                </td>
            </tr>  
            <tr>
                <td valign="top">Exact Precision:
                </td>
                <td>
                    <input id="exactRating" type="text" />
                   
                </td>
            </tr>         
        </table>
    </div>
    
{% endhighlight %}

{% highlight js %}

    
        // Add the following script to render Rating with Precision.
  
        $("#rating").ejRating({ value: 4 });
        $("#halfRating").ejRating({ precision: ej.Rating.Precision.Half, value: 3.5 });
        $("#exactRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 3.7 });

{% endhighlight %}

The following screenshot illustrates the **Rating** with **Precision**.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img4.png" Caption="Rating with Precision"%}

## Increment Step

**EJ Rating** control supports customized **increment** value for Rating. This is achieved by adding the **incrementStep** property.

The following code example is used to render the **Rating** control with customized **increment**.

 Add the following HTML to render Rating with customized increment.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}

    // Add the following script to render Rating with customized increment.

    $("#rating").ejRating({ incrementStep: 2, maxValue: 10});
 
{% endhighlight %}

The following screenshot illustrates the **Rating** with customized increment.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img5.png" Caption="Rating with customized increment"%}

## Resetting values

**EJ Rating** control provides support for value **reset** at runtime. This is achieved by enabling the **allowReset** property to be **‘True’.** By default, the property value is set to **‘True’.**

The following code example is used to render the **Rating** control with **allowReset**.

 Add the following HTML to render Rating with allowReset.

{% highlight js %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                   
                </td>
            </tr>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                     <input id="rest" type="text" />                    
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}


       // Add the following script to render Rating with allowReset.

       $("#rating").ejRating({ allowReset: true });
       $("#rest").ejRating({ allowReset: false });


{% endhighlight %}

The following screenshot illustrates the **Rating** with **allowReset**.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img6.png" Caption="Rating with allowReset"%}

## Read only

**Rating** control provides support for changeable or unchangeable values for **Rating** control. This is achieved by the **readOnly** property. When this property is set to **‘True’** the **Rating** value becomes unchangeable. By default, this property value is set to **‘False’.**

The following code example is used to render the **Rating** control with **readOnly**.

 Add the following HTML to render Rating with readOnly.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %}

{% highlight js %}

     // Add the following script to render Rating with readOnly .

     $("#rating").ejRating({ readOnly: true });
 
{% endhighlight %}


The following screenshot illustrates the **Rating** with **readOnly.**

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img7.png" Caption="Rating with readOnly"%}

## Enable or Disable

**Rating** control provides support to **enable** or **disable** the control. This is achieved by the **enabled** property. By default the property value is **‘True’.**

The following code example is used to render the **Rating** control with **enable** or **disable** support.

 Add the following HTML to render Rating with enable or disable support.

{% highlight html %}

   <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>
    
{% endhighlight %}

{% highlight js %}

       // Add the following script to render Rating in disabled form.

       $("#rating").ejRating({ enabled: false });
  
{% endhighlight %}



The following screenshot illustrates the **Rating** in **disabled** form.

{% include image.html url="/js/Rating/Rating-Customization_images/Rating-Customization_img8.png" Caption="Rating in disabled form"%}

