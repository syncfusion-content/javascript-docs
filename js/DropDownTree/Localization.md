---
layout: post
title: Localization in DropDownTree widget for Syncfusion Essential JS
description: Localization in DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: Localization, DropDownTree, dropdowntree
api: /api/js/ejDropDownTree
---
# Localization

The DropDownTree provides an option to localize its strings used to adapt the DropDownTree to a particular local language. By default, the DropDownTree will use the US English (en-US) as its language.

Note: The culture name has to be specified in a standard format such as [Language Code]-[County/Region Code].

To localize the DropDownTree’s strings with your own localization, copy the default language information and localize the strings in the values column. For example, to localize the DropDownTree in German language use (“de-DE”).


{% highlight javascript %}

    ej.DropDownTree.Locale["de-DE"] = {
        emptyResultText: "Keine Vorschläge" //replace with your text  
    };
    
{% endhighlight %}

Set the [locale](https://help.syncfusion.com/api/js/ejDropDownTree#members:locale) property of the DropDownTree to the new language.


{% highlight javascript %}
<input type="text" id="itemList" />

<script type="text/javascript">
        var localData = [
                    { id: 1, name: "Windows Team", hasChild: true, expanded: true },
                    { id: 2, pid: 1, name: "Clark" },
                    { id: 3, pid: 1, name: "Wright" },
                    { id: 4, pid: 1, name: "Lopez" },
                    { id: 6, pid: 1, name: "Anderson" },
                    { id: 7, name: "Web Team", hasChild: true, expanded: true },
                    { id: 8, pid: 7, name: "Joshua" },
                    { id: 9, pid: 7, name: "Matthew" },
                    { id: 10, pid: 7, name: "David" },
                    { id: 11, name: "Build Team", hasChild: true },
                    { id: 12, pid: 11, name: "Ryan" },
                    { id: 13, pid: 11, name: "Justin" },
                    { id: 14, pid: 11, name: "Robert" },
                    { id: 15, pid: 11, name: "Johnson" },
                    { id: 16, name: "WPF Team", hasChild: true },
                    { id: 17, pid: 16, name: "Rock" },
                    { id: 18, pid: 16, name: "Gospel" },
                    { id: 19, pid: 16, name: "Brown" },
                    { id: 20, pid: 16, name: "Miller" }];
        $(function () {
            $('#itemList').ejDropDownTree({
                enableFilterSearch: true,
                treeViewSettings: {
                    fields: { id: "id", parentId: "pid", value: "id", text: "name", hasChild: "hasChild", dataSource: localData, expanded: "expanded" }
                },
                locale: "de-DE",
                watermarkText: "Please select"
            });
        });
    </script>

    
{% endhighlight %}

![](Localization_images/localization.png)