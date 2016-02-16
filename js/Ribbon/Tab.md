---
layout: post
title:  Tab
description:tab 
documentation: ug
platform: js
keywords: ribbon tab
---

# Tab

Tab is a collection of control [`groups`](http://help.syncfusion.com/js/api/ejribbon#members:tabs-groups) which enables you to organize related commands into single view.  Tabs can be added to Ribbon using [`tabs`](http://help.syncfusion.com/js/api/ejribbon#members:tabs) property. [`id`](http://help.syncfusion.com/js/api/ejribbon#members:tabs-id) & [`text`](http://help.syncfusion.com/js/api/ejribbon#members:tabs-text) properties are used to set unique ID and header text to Tab. 

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbonmenu">
        <li>
            <a>FILE</a>
            <ul>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
    <div id="sendReceive">
        Send/Receive All Folders
    </div>
    <script type="text/javascript">
        $(function () {
            $("#Ribbon").ejRibbon({
                width: "500px",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonmenu"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Save",
                        content: [{
                            groups: [{
                                text: "Save",
                                isBig: true,
                                buttonSettings: {
                                    prefixIcon: "e-icon e-save",
                                    contentType: ej.ContentType.ImageOnly
                                }
                            }]
                        }]
                    }, {
                        text: "Print",
                        content: [{
                            groups: [{
                                text: "Print",
                                isBig: true,
                                type: ej.Ribbon.type.toggleButton,
                                toggleButtonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    defaultText: "Print",
                                    activeText: "Print",
                                    defaultPrefixIcon: "e-icon e-print",
                                    activePrefixIcon: "e-icon e-print",
                                }
                            }]
                        }]
                    }]
                }, {
                    id: "sendrec",
                    text: "Send/Receive",
                    groups: [{
                        type: "custom",
                        contentID: "sendReceive"
                    }]
                }]
            });
        });
    </script>

   
{% endhighlight %}

![](/js/Ribbon/Tab_images/Tab_img1.png)

