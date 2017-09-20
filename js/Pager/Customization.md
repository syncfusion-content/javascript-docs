---
layout: post
title: customization
description: customization
platform: js
control: Pager
documentation: ug
api: /api/js/ejpager
---

# Customization

## Show Go To Page

The **showGoToPage** property of pager renders a textbox within the pager element. The current page of the pager  control will be navigated with the value of the go to textbox.

{% highlight javascript %}

        $(function () {

            // creates pager control with showGoToPage textbox

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount:3,

                showGoToPage:true

            });

        });
     
{% endhighlight %}

Run the above code to get the below output.

![](/js/Pager/Customization_images/showGoToPage.png)
        
## Show Page Info

The **showPageInfo** property of the pager control defines whether to show the page info of the pager control which displays details of total records count, total pages and current page.


{% highlight javascript %}

        $(function () {

            // creates pager control without page information 

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount:3,

                showPageInfo:false // Hides the page information available in the pager control.

            });

        });

{% endhighlight %}

Run the above code to get the below output.

![](/js/Pager/Customization_images/pageInfo.png)

## Custom Text

The **customText** property of pager allows to add the custom text along with numeric values in the pager numeric elements that are used for navigation in pager control.


{% highlight javascript %}

        $(function () {

            // creates pager control with custom text added to numeric elements.

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageCount: 3,

                pageSize: 1,

                customText: "page"

            });

        });

{% endhighlight %}

Run the above code to get the below output.

![](/js/Pager/Customization_images/customText.png)

## External Message

The pager control also allows to define a external message using externalMessage API to display an additional information. To use external message, we need to enable it using enableExternalMessage API. In the sample below, the externalMessage of pager is used to show the current active page of the pager control. Whenever the current page value of the pager changes, the externalMessage will be updated with the current page value.


{% highlight javascript %}

       $(function () {

           // creates pager with an external message displaying currentpage value.

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,
                
                pageCount: 3,

                change: "onChange", // sets handler to listen change in currentpage value

                enableExternalMessage: true, // enabling external message

                externalMessage: "CurrentPage: 1" // sets external message for pager control
            });

        });

function onChange(e) {

                   // Creating a instance of pager.
                   var a = $("#Pager").ejPager("instance");
                   // updating the external message with respective currentpage value.
                   a.option("externalMessage","CurrentPage: "+e.currentPage);

               }

{% endhighlight %}

Run the above code to get the below output.

![](/js/Pager/Customization_images/externalMessage.png)

## Custom CSS

Pager control allows you to customize the appearance using user defined CSS and custom skin options such as colors and backgrounds. To apply custom themes, we can make use of cssClass property. Using cssClass property, we can override the existing theme styles. In the following sample, value for cssClass property is set as customCss and this root class is used to customize the pager control theme.


{% highlight javascript %}

       $(function () {

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount:3,

                cssClass: "customCss"

            });

        });

{% endhighlight %}

Defining custom class.

{% highlight html %}

<style>
        .e-pager.customCss .e-link.e-currentitem{
                background:lightblue;
        }
        .e-pager.customCss .e-numericitem, .e-pager.customCss .e-pagermsg{
            font-family:monospace;
        }
        .e-pager.customCss .e-pagercontainer,.e-pager.customCss .e-link ,.e-pager.customCss .e-icon {
            background-color: rgba(33,33,33,0.35);
        }
        .e-pager.customCss {
            color:white;
            background-color: rgba(33,33,33,0.30);
        }
        .e-pager.customCss :hover {
             color:white
        }
        .e-pager.customCss .e-hover.e-numericitem, .e-pager.customCss .e-hover.e-icon{
            background-color:rgba(173,216,230,0.30);
        }
        .e-pager.customCss .e-hover.e-icon.e-disable {
             background-color: rgba(33,33,33,0.35);
          
        }
        .e-pager.customCss .e-icon, .e-pager.customCss .e-numericitem{
            color:white;
            border-right-color: #777;
        }
</style>

{% endhighlight %}

Run the above code to get the below output.

![](/js/Pager/Customization_images/cssClass.png)
