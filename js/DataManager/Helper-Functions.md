---
layout: post
title: Helper-Functions
description: helper functions
platform: js
control: DataManager
documentation: ug
---

# Helper Functions

**ej.parseJSON**

This method is used to parse the string to **JSON**. 

**ej.parseTable**

This method is used to parse the **HTML** element into the **JSON** Array and is used commonly in element binding using **DataManager**.

**ej.getGuid**

This method returns the globally unique identifier and it generates unique identifier with the prefix provided as parameter.

**ej.merge**

The ej.merge is used to merge two arrays and the result is merged in the first array. 

**ej.support**

The ej.support property contains a collection of properties representing different browser features or bugs. The property are as follows.

1. cors – represents the cross browser support.

2. enableLocalizedSort – enables the localized sort operation.

3. stableSort – enables stable sort operation.

4. outerHTML – represents the outerHTML support.

**ej.swap**

This method is used to swap the position of element in an array. It accepts three arguments such as input array and two swap positions.

**ej.serverTimeZoneOffset**

This method is used to set the time-zone offset from UTC, in hours

N> Suppose, application has been hosted in IST time zone and client may be in EST, GMT etc. in that case, date will differ from database. The below given solution will fix the conflict. 

<table>
    <tr> 
        Property <br>
        Name: ej.serverTimeZoneOffset 
        Data type: number
        Default Value: 0 
    </tr>
</table>

N> By default, The server time zone will be in UTC, if its other than the UTC, set the proper format time zone offset value to the ej.serverTimeZoneOffset property. <BR>
Please refer the online (link)[http://www.timeanddate.com/worldclock/difference.html?p1=1440] for time zone difference offset value.

<table>
    <tr>
        Time-zone offset calculation from UTC: <br>
        ej.serverTimeZoneOffset = serverTimeZoneDiff(in hours) + ClientSideTimeZoneDiff(in hours); 
    </tr>
</table>

{% highlight html %}

    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div id="Grid"></div>
            </div>
        </div>
    </div>
    <script type="text/javascript">
        var serverTimeZoneDiff = +5.5   // if your server is in IST time zone (UTC +5.5) (in hours)
        var clientSideTimeZoneDiff = new Date().getTimezoneOffset() / 60; // get client time zone differents and convert it to hours;
        ej.serverTimeZoneOffset = serverTimeZoneDiff + clientSideTimeZoneDiff;
        $(function () {
            var dm = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders" });
            $("#Grid").ejGrid({
                dataSource: dm,
                allowPaging: true,
                columns: ["OrderID", "EmployeeID", "CustomerID", "OrderDate", "Freight"]
            });
        });
    </script>

{% endhighlight %}

N> When the DayLight Saving mode is enabled in the sever, take care about this time adjustment with the time-zone offset calculation.

I> Daylight saving time (DST) or summer time is the practice of advancing clocks during summer months by one hour so that evening daylight lasts an hour longer, while sacrificing normal sunrise times. Typically, regions with summer time adjust clocks forward one hour close to the start of spring and adjust them backward in the autumn to standard time. Please refer the (link)[http://www.worldtimezone.com/daylight.html].