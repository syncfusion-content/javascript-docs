---
layout: post
title: behavior settings
description: behavior settings
platform: js
control: Pager
documentation: ug
api: /api/js/ejpager
---

# Behavior Settings

##Page Size

The **pageSize** property of the pager control allows an option to gets or sets a value that indicates whether to define the number of records displayed per page.

{% highlight javascript %}

   $(function () {

        $("#pager").ejPager({
         pageSize: 2
        
        })

    });

{% endhighlight %}


##Page Count

The **pageCount** property of the pager control allows an option to gets or sets a value that indicates whether to define the number of pages displayed in the pager for navigation.

{% highlight javascript %}

   $(function () {

        $("#pager").ejPager({
         pageCount: 5
        
        })

    });

{% endhighlight %}


##Total Pages

The **totalPages** property of the pager control allows an option to gets or sets a value of total number of pages in the pager. The totalPages value is calculated based on page size and total records.

{% highlight javascript %}

   $(function () {

        $("#pager").ejPager({
         totalPages:1
        
        })

    });

{% endhighlight %}


##Total Records count

The **totalRecordsCount** property of the pager control allows an option to get the value of total number of records which is bound to a data item.

{% highlight javascript %}

   $(function () {

        $("#pager").ejPager({
         totalRecordsCount: 10 
        
        })

    });

{% endhighlight %}

##current page

The **currentPage** property of the pager control allows an option to gets or sets a value that indicates whether to define which page to display currently in pager.

{% highlight javascript %}

   $(function () {

        $("#pager").ejPager({
         currentPage: 1 
        
        })

    });

{% endhighlight %}


## Page Size List

The **pageSizeList** property of the pager control allows an option to have multiple options of page size values. By defining **pageSizeList**, a dropdown will render in a pager with given values along with the current pageSize as selected value in dropdown.

Selected value in a dropdown will be set to pageSize API and pager will refresh based on this new pageSize.

{% highlight javascript %}

   $(function () {

        // creates pager control with pageSizeList

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount:3,

                // set pageSizeList value for pager.
                pageSizeList: [1,2,3]

            });

        });

{% endhighlight %}

![](/js/Pager/Behavior-Settings_images/pageSizeList.png)

## Page Size Message

The **pageSizeMessage** property allows to show a message along with the dropdown when **pageSizeList** API of pager control is defined. In the below sample, the **pageSizeMessage** of pager displays the current **pageSize** value of the pager control and will also be updated whenever the pageSize value is changed by selecting a value from the dropdown.

{% highlight javascript %}

     $(function () {

          // creates pager control with pageSizeMessage

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageCount: 3,

                pageSize: 1,

                pageSizeList: [1,2,3],

                pageSizeSelected: "pageSizeInfo", // sets handler to change in pageSizeList dropdown. 

                pageSizeMessage: "PageSize value: 1" // sets pageSizeMessage for the pager.

            });

        });

function pageSizeInfo(e) {

                   // creating instance for pager. 
                   var a = $("#Pager").ejPager("instance");

                   //pageSize value of pager will be updated for each change of value in dropdown
                   a.option("pageSizeMessage", "PageSize value: " + e.pageSize);
                   
               }

{% endhighlight %}

![](/js/Pager/Behavior-Settings_images/pageSizeMessage.png)

## Responsive

The pager control has responsive support such that control also fit with mobile resolutions. By enabling **isResponsive** API, you can make the pager control responsive. While resizing the browser window, the inner elements in the pager control will adjust automatically to equalize the size. By default, **isResponsive** API value is false. 

{% highlight javascript %}

      $(function () {

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                currentPage:1,

                pageCount:3,

                isResponsive: true

            });

        });

{% endhighlight %}

![](/js/Pager/Behavior-Settings_images/pager_Responsive.png)

## Current Page

The **currentPage** value of the pager determines which page to be displayed currently. The default value of the **currentPage** API is 1

{% highlight javascript %}

        $(function () {

            // create a pager control defining  the current page value

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageSize: 1,

                pageCount:3,

                currentPage: 2

            });

        });

{% endhighlight %}

![](/js/Pager/Behavior-Settings_images/pager_Currentpage.png)

## Enable/Disable

You can enable or disable pager control by using **enabled** property. Setting enabled API value as false will disable the user interaction with the pager control.

{% highlight javascript %}

        $(function () {

            // Creates a pager control initially disabled

            $("#pager").ejPager({

                totalRecordsCount: 20,

                pageCount: 3,

                pageSize: 1,

                //disables the pager control
                enabled: false

            });

        });


{% endhighlight %}
