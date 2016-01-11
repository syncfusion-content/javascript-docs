---
layout: post
title: Backstage-Page
description: backstage page 
platform: js
control: Ribbon
documentation: ug
---

# Backstage Page 

Ribbon control has Backstage page support.The left side of the backstage page contains backstage tab and button items,right side of the backstage page contains UserControl items.To render ribbon with backstage page set _**applicationTab**_’s _**Type**_ as _**"BackStagePage"**_ and _**text**_ property in _**applicationTab**_ to set text for Apllication tab.

We can set height and width to backstage page using properties _**backStageHeight**_ and _**backStageWidth**_.

* _**id**_ **–** Specify id of backstage tab and button.
* _**text**_**–** Specify text of backstage tab and button.
* _**contentId**_ **–**Specify id of UserControl’s Parent item.
* _**backStageItemType**_ **–**Specify the type of backstage page item to render backstage tab or button. _**ej.Ribbon.backStageItemType.tab**_—to render backstage tab. _**ej.Ribbon.backStageItemType.button**_-to render backstage button.
* _**enableSeparator**_ **–**Set true to enable separator between backstage button and tab items .

{% highlight html %}

    <!-- ... -->
    <head>
    </head>
    <!-- ... -->
    <body>
       <div id="Ribbon"></div>
       <div id="infoCon">Info Tab</div>
       <div id="newCon">New Tab</div>
       <div id="accountCon">Account Tab</div>
       <div id="ribbonContent">Home control</div>
       <script type="text/javascript">
        $(function() {
            $("#Ribbon").ejRibbon({
                width: "500px",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.backstage,
                     backstageSettings: {
                    text: "FILE",
                    height: 230,
                    width: 500,
                    headerWidth: 125,
                    Pages: [{
                        id: "info",
                        text: "Info",
                        contentID: "infoCon",
                        itemType: ej.Ribbon.itemType.tab
                    }, {
                        id: "new",
                        text: "New",
                        contentID: "newCon"
                    }, {
                        id: "close",
                        text: "Close",
                        enableSeparator: true,
                        itemType: ej.Ribbon.itemType.tab
                    }, {
                        id: "account",
                        text: "Office Account",
                        contentID: "accountCon"
                    }]
                    
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "New",
                        type: "custom",
                        contentID: "ribbonContent"
                    }]
                }]
            });
        });
    </script>
    </body>
    <!-- ... -->

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](/js/Ribbon/Backstage-Page_images/Backstage-Page_img1.png)