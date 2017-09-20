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
