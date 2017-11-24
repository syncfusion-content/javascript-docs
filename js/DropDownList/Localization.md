---
layout: post
title: Localization in DropDownList widget for Syncfusion Essential JS
description: Localization in DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: Localization, DropDownList, dropdown
api: /api/js/ejdropdownlist
---
# Localization

The DropDownList provides option to localize its strings, it is used to adapting the DropDownList to a particular local language. By default, the DropDownList will use the US English (en-US) as its language.

N> The culture name has to be specified in a standard format such as [Language Code]-[County/Region Code].

To localize the dropdownlist’s strings with your own localization, copy the default language informations and localize the strings in the values column. For example, to localize the DropDownList in German language (“de-DE”).

{% highlight javascript %}

    ej.DropDownList.Locale["de-DE"] = {
        emptyResultText: "Keine Vorschläge" //replace with your text  
    };
    
{% endhighlight %}

Set the [locale](https://help.syncfusion.com/api/js/ejdropdownlist#members:locale) property of the DropDownList to the new language.


{% highlight javascript %}

    <input type="text" id="selectCompany" />

    $(function () {
        var dataList = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Customers" });
        $('#selectCompany').ejDropDownList({
            dataSource: dataList,
            fields: { text: "CompanyName", value: 'ContactName' },
            width: 260,
            showCheckbox: true,
            locale: "de-DE",
            enableFilterSearch: true,
            enablePopupResize: true

        });

    });
    ej.DropDownList.Locale["de-DE"] = {
        emptyResultText: "Keine Vorschläge" //replace with your text  
    };
    
{% endhighlight %}
