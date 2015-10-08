---
layout: post
title: ejRibbon
documentation: API
platform: js
metaname: 
metacontent: 
---

The ribbon can be easily configured to the DOM element, such as div. you can create a ribbon with a highly customizable look and feel.










$(element).ejRibbon<span class="signature">(options)</span>







<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for ribbon</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Ribbon"></div> 
<script>
// Create Ribbon
$('#Ribbon').ejRibbon();         
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.min.js


* module:jquery.globalize.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.dropdownlist.js


* module:ej.button.js


* module:ej.tab.js


* module:ej.splitbutton.js


* module:ej.ribbon.js


* module:ej.menu.js


* module:ej.scroller.js


* module:ej.checkbox.js


* module:ej.togglebutton.js




## Members








### allowResizing<span class="type-signature type boolean">boolean</span>
{:#members:allowresizing}








Property to enable the ribbon resize feature.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="ribbonmenu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
     width: "100%",
                allowResizing:true,
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "ribbonmenu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Clipboard", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "cut",
                        text: "Cut"
                    },
                                        {
                        id: "copy",
                        text: "Copy"
                    },
                                                {
                        id: "paste",
                       text: "Paste"
                    }],
                                                 defaults: {
                       type: ej.Ribbon.type.button,
                       height: 70,
                                                   width: 75
                   }
                }]
           },
                   {
                text: "Font", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "bold",
                        text: "Bold"
                    },
                                        {
                        id: "italic",
                        text: "Italic"
                    },
                                        {
                        id: "underline",
                        text: "Underline"
                    }], 
                                                defaults: {
                       type: ej.Ribbon.type.button,
                       height: 70,
                                                   width: 75
                   }
                }]
           },
                           {
                text: "Alignment", alignType: ej.Ribbon.alignType.rows,content: [{
                   groups: [{
                        id: "left",
                        text: " Left"
                   },
                                        {
                       id: "center",
                        text: "Center"
                   },
                                        {
                        id: "right",
                        text: "Right"
                    }], 
                                                defaults: {
                      type: ej.Ribbon.type.button,
                       height: 70,
                                           width: 75
                   }
               }]
           }]
       }]
  });
});             
</script>  {% endhighlight %}







### applicationTab<span class="type-signature type object">object</span>
{:#members:applicationtab}








Specify the application tab to contain application menu or backstage page in the ribbon control.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### applicationTab.backstageSettings<span class="type-signature type object">object</span>
{:#members:applicationtab-backstageSettings}








To specify the ribbon backstage page items.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}








### applicationTab.backstageSettings.text<span class="type-signature type string">string</span>
{:#members:applicationtab-backstageSettings-text}








To specify the display text of application tab.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}








### applicationTab.backstageSettings.height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:applicationtab-backstageSettings-height}








To specify the height of ribbon backstage page.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}






### applicationTab.backstageSettings.width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:applicationtab-backstageSettings-width}








To specify the width of ribbon backstage page.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages<span class="type-signature type array">array</span>
{:#members:applicationtab-backstageSettings-pages}








To specify the ribbon backstage page with its tab and button elements.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages.id<span class="type-signature type string">string</span>
{:#members:applicationtab-backstageSettings-pages-id}








To specify the id for ribbon backstage page's tab and button elements.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages.text<span class="type-signature type string">string</span>
{:#members:applicationtab-backstageSettings-pages-text}








To specify the text for ribbon backstage page's tab header and button elements.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages.itemType<span class="type-signature type enum">enum</span>
{:#members:applicationtab-backstageSettings-pages-itemType}








To specify the type for ribbon backstage page's contents.Set "ej.Ribbon.backStageItemType.tab" to render the tab or "ej.Ribbon.backStageItemType.button" to render the button.




Default Value:
{:.param}






* ej.Ribbon.itemType.tab








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages.contentID<span class="type-signature type string">string</span>
{:#members:applicationtab-backstageSettings-pages-contentID}








To specify the id of html elements(like div,ul,etc..,) as ribbon backstage page's tab content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.pages.enableSeparator<span class="type-signature type boolean">boolean</span>
{:#members:applicationtab-backstageSettings-pages-enableSeparator}








To specify the separator between backstage page's tab and button elements.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}







### applicationTab.backstageSettings.headerWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:applicationtab-backstageSettings-headerWidth}








To specify the width of backstage page header which contains tabs and buttons.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
</script>{% endhighlight %}








### applicationTab.menuItemID<span class="type-signature type string">string</span>
{:#members:applicationtab-menuItemID}








Specify the ID of 'ul' list to create application menu in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button </button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### applicationTab.menuSettings<span class="type-signature type object">object</span>
{:#members:applicationtab-menusettings}








Specify the menu members,events using the menu settings for the menu in the application tab.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### applicationTab.type<span class="type-signature type enum">enum</span>
{:#members:applicationtab-type}








To specify the application menu or backstage page.Specify the type of application tab as "ej.Ribbon.applicationTabType.menu" to render the application menu or "ej.Ribbon.applicationTabType.backstage" to render backstage page in the ribbon control.




Default Value:
{:.param}






*  ej.Ribbon.applicationTabType.menu








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### contextualTabs<span class="type-signature type array">array</span>
{:#members:contextualtabs}








Specify the contextual tabs and tabset to the ribbon control with the background color and border color.Please refer the tabs section for adding tabs into the contextual tab and contextual tab set.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<button id="design">Design button</button>
<button id="div1">First button</button>
<button id="div2">Second button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
        contextualTabs:
                     [{
                          backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                          tabs:[{
                          id: "Design", text: "DESIGN",groups: [{
                                    text: "Table Style Options", type: "custom", contentID: "design"
                                }
                                ]
                              }]
                       },
                        {
                           borderColor: "lightblue",backgroundColor:"blue",
                            tabs:[{
                                id: "tabset1", text: "Tabset1", 
                                groups: [
                                { text: "Tabset1 Styles", type: "custom", contentID: "div1"
                                }]
                           },
                            {
                                id: "tabset2", text: "Tabset2",
                                groups: [
                                    { text: "Tabset2 Styles", type: "custom", contentID: "div2"
                                    }
                                ]
                           }]
}]
  });
});             
</script>  {% endhighlight %}







### contextualTabs.backgroundColor<span class="type-signature type string">string</span>
{:#members:contextualtabs-backgroundcolor}








Specify the backgroundColor of the contextual tabs and tabset in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<button id="design">Design button</button>
<button id="div1">First button</button>
<button id="div2">Second button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
        contextualTabs:
                     [{
                          backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                          tabs:[{
                          id: "Design", text: "DESIGN",groups: [{
                                    text: "Table Style Options", type: "custom", contentID: "design"
                                }
                                ]
                              }]
                       },
                        {
                           borderColor: "lightblue",backgroundColor:"blue",
                            tabs:[{
                                id: "tabset1", text: "Tabset1", 
                                groups: [
                                { text: "Tabset1 Styles", type: "custom", contentID: "div1"
                                }]
                           },
                            {
                                id: "tabset2", text: "Tabset2",
                                groups: [
                                    { text: "Tabset2 Styles", type: "custom", contentID: "div2"
                                    }
                                ]
                           }]
}]
  });
});             
</script>  {% endhighlight %}







### contextualTabs.borderColor<span class="type-signature type string">string</span>
{:#members:contextualtabs-bordercolor}








Specify the borderColor of the contextual tabs and tabset in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<button id="design">Design button</button>
<button id="div1">First button</button>
<button id="div2">Second button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
        contextualTabs:
                     [{
                          backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                          tabs:[{
                          id: "Design", text: "DESIGN",groups: [{
                                    text: "Table Style Options", type: "custom", contentID: "design"
                                }
                                ]
                              }]
                       },
                        {
                           borderColor: "lightblue",backgroundColor:"blue",
                            tabs:[{
                                id: "tabset1", text: "Tabset1", 
                                groups: [
                                { text: "Tabset1 Styles", type: "custom", contentID: "div1"
                                }]
                           },
                            {
                                id: "tabset2", text: "Tabset2",
                                groups: [
                                    { text: "Tabset2 Styles", type: "custom", contentID: "div2"
                                    }
                                ]
                           }]
}]
  });
});             
</script>  {% endhighlight %}







### contextualTabs.tabs<span class="type-signature type array">array</span>
{:#members:contextualtabs-tabs}








Specify the tabs to present in the contectual tabs and tab set.Please refer the tabs section for adding tabs into the contextual tabs and tab set.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<button id="design">Design button</button>
<button id="div1">First button</button>
<button id="div2">Second button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
        contextualTabs:
                     [{
                          backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                          tabs:[{
                          id: "Design", text: "DESIGN",groups: [{
                                    text: "Table Style Options", type: "custom", contentID: "design"
                                }
                                ]
                              }]
                       },
                        {
                           borderColor: "lightblue",backgroundColor:"blue",
                            tabs:[{
                                id: "tabset1", text: "Tabset1", 
                                groups: [
                                { text: "Tabset1 Styles", type: "custom", contentID: "div1"
                                }]
                           },
                            {
                                id: "tabset2", text: "Tabset2",
                                groups: [
                                    { text: "Tabset2 Styles", type: "custom", contentID: "div2"
                                    }
                                ]
                           }]
}]
  });
});             
</script>  {% endhighlight %}







### disabledItemIndex<span class="type-signature type array">array</span>
{:#members:disableditemindex}








Specify the index or indexes to disable the given index tab or indexes tabs in the ribbon control.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button<button>
<button id="insert">Insert button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
     width: "100%",
// Set the disabledItemIndex during initialization. 
 disabledItemIndex: [1,2],
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        },
       {
                id: "insert", text: "INSERT", groups: [{
                text: "Insert group", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"insert"
           }]
       }
]
  });
});             
</script>  {% endhighlight %}







### enabledItemIndex<span class="type-signature type array">array</span>
{:#members:enableditemindex}








Specify the index or indexes to enable the given index tab or indexes tabs in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button<button>
<button id="insert">Insert button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        },
       {
                id: "insert", text: "INSERT", groups: [{
                text: "Insert group", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"insert"
           }]
       }
]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
   ribbonObj.option({ disabledItemIndex: [1, 2] });
        // Enable the required ribbon tab from the ribbon control.
        ribbonObj.option({ enabledItemIndex: [1] });
</script>  {% endhighlight %}







### selectedItemIndex<span class="type-signature type number">number</span>
{:#members:selecteditemindex}








Specify the index of the ribbon tab to select the given index tab item in the ribbon control.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button<button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
     width: "100%",
// Set the selectedItemIndex during initialization. 
       selectedItemIndex : 2,
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        },
       {
                id: "insert", text: "INSERT", groups: [{
                text: "Insert group", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"insert"
           }]
       }
      ]
  });
});             
</script>  {% endhighlight %}







### tabs<span class="type-signature type array">array</span>
{:#members:tabs}








Specify the tabs and its groups,controls to the ribbon control.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<button id="insert">Insert button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        },
                    {
                                id: "insert", text: "INSERT", groups: [{
                text: "Insert group", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"insert"
           }]
                    }
           ]
  });
});             
</script>  {% endhighlight %}







### tabs.groups<span class="type-signature type array">array</span>
{:#members:tabs-groups}








Specify single group or multiple groups and its contents to each tab in the ribbon control.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.alignType<span class="type-signature type enum">enum</span>
{:#members:tabs-groups-aligntype}








Specify the alignment of controls in the groups in 'row' type or 'column' type.Value for row type is "ej.Ribbon.alignType.rows" and Value for column type is "ej.Ribbon.alignType.columns".




Default Value:
{:.param}






* ej.Ribbon.alignType.rows








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content<span class="type-signature type array">array</span>
{:#members:tabs-groups-content}








Specify the syncfusion button,split button,dropdown list,toggle button,gallery,custom controls to the groups in the ribbon control.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.defaults<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-defaults}








Specify the height,width,type,isBig property to the controls in the group commonly.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                         buttonSettings: {
                         width: 100,
                         }
                    },
                                                {
                        id: "font",
                        text: "Font",
                        toolTip: "Font",
                        buttonSettings: {
                        width: 150,
                        }
                    }],
                                                 defaults: {
                       type: ej.Ribbon.type.button,
                       height: 70
                   }
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups<span class="type-signature type array">array</span>
{:#members:tabs-groups-content-groups}








Specify the controls such as syncfusion button,split button,dropdown list,toggle button,gallery,custom controls in the subgroup of the ribbon tab .




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.buttonSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-buttonsettings}








Specify the syncfusion button members,events using this buttonSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        isBig:true,
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 100,
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.columns<span class="type-signature type number">number</span>
{:#members:tabs-groups-content-groups-columns}








It is used to set the count of gallery contents in a row.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.contentID<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-contentid}








Specify the custom items such as div,table,controls as custom controls with the type "ej.Ribbon.type.custom" in the groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<input id="fontcolor"/> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    },
                     {
                                             id: "fontcolor",
                                             text: "Font Color",
                                             toolTip: "Font Color",
                                             type: ej.Ribbon.type.custom,
                                             contentID:"fontcolor"
                                         }]
                }]
           }]
        }],
        create: "createControl",
  });
});             
  function createControl(args) {
   $("#fontcolor").ejColorPicker({ value: "#FFFF00", modelType: "palette", cssClass: "e-ribbon", 
     toolIcon: "e-icon e-fontcoloricon"});
   }
</script>  {% endhighlight %}







### tabs.groups.content.groups.cssClass<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-cssclass}








Specify the css class property to apply styles to the button,split,dropdown controls in the groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<style>
.e-cssclass {
     margin-left: 20px;
}
</style>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        cssClass:"e-cssclass",
                        isBig:true,
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 100,
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems<span class="type-signature type array">array</span>
{:#members:tabs-groups-content-groups-customgalleryitems}








Specify the syncfusion button and menu as gallery extra items.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.buttonSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-customgalleryitems-buttonsettings}








Specify the syncfusion button members,events using buttonSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                     customToolTip:{
                                                         title: "<u>Save</u>",
                            content: "<i>Save Selection as new quick style</i>",
                                                         prefixIcon:"e-expander",
                                                        },
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.customItemType<span class="type-signature type enum">enum</span>
{:#members:tabs-groups-content-groups-customgalleryitems-customitemtype}








Specify the type as ej.Ribbon.customItemType.menu or ej.Ribbon.customItemType.button to render synfusion button and menu.




Default Value:
{:.param}






* ej.Ribbon.customItemType.button








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                     customToolTip:{
                                                         title: "<u>Save</u>",
                            content: "<i>Save Selection as new quick style</i>",
                                                         prefixIcon:"e-expander",
                                                        },
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.customToolTip<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-customgalleryitems-customtooltip}








Specify the custom tooltip for gallery extra item's button.Please refer ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                     customToolTip:{
                                                         title: "<u>Save</u>",
                            content: "<i>Save Selection as new quick style</i>",
                                                         prefixIcon:"e-expander",
                                                        },
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.menuId<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customgalleryitems-menuid}








Specify the UL list id to render menu as gallery extra item.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                     customToolTip:{
                                                         title: "<u>Save</u>",
                            content: "<i>Save Selection as new quick style</i>",
                                                         prefixIcon:"e-expander",
                                                        },
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.menuSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-customgalleryitems-menusettings}








Specify the syncfusion menu members,events using menuSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                     customToolTip:{
                                                         title: "<u>Save</u>",
                            content: "<i>Save Selection as new quick style</i>",
                                                         prefixIcon:"e-expander",
                                                        },
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.text<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customgalleryitems-text}








Specify the text for gallery extra item's button.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customGalleryItems.toolTip<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customgalleryitems-tooltip}








Specify the tooltip for gallery extra item's button.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customToolTip<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-customtooltip}








Provide custom tooltip for button,split button,dropdown list,toggle button,custom controls in the sub groups.We have provided text and html support for title and content.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [
                                {
                text: "Expand", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                                                customToolTip:{
                                                        title: "<i&amp;gtExpand</i>",
                           content: "<h5&amp;gtExpand content</h5>",
                                                        prefixIcon:"e-expander",
                                                                }
                    },
                                        {
                        id: "new",
                        text: "New Button",
                                                        customToolTip:{
                                                                title: "New",
                               content: "New content"
                                                                }
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customToolTip.content<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customtooltip-content}








It is used to set content to the custom tooltip.We have provided text and html support for content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [
                                {
                text: "Expand", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                                                customToolTip:{
                                                        title: "<i>Expand</i>",
                           content: "<h5>Expand content</h5>",
                                                        prefixIcon:"e-expander",
                                                                }
                    },
                                        {
                        id: "new",
                        text: "New Button",
                                                        customToolTip:{
                                                                title: "New",
                               content: "New content"
                                                                }
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customToolTip.prefixIcon<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customtooltip-prefixicon}








It is used to set icon to the custom tooltip content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [
                                {
                text: "Expand", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                                                customToolTip:{
                                                        title: "<i>Expand</i>",
                           content: "<h5>Expand content</h5>",
                                                        prefixIcon:"e-expander",
                                                                }
                    },
                                        {
                        id: "new",
                        text: "New Button",
                                                        customToolTip:{
                                                                title: "New",
                               content: "New content"
                                                                }
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.customToolTip.title<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-customtooltip-title}








It is used to set title to the custom tooltip.We have provided text and html support for title and the title will be in bold for text format.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
            id: "home", text: "HOME", groups: [
                                {
                text: "Expand", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "expand",
                        text: "Expand Button",
                                                customToolTip:{
                                                        title: "<i>Expand</i>",
                           content: "<h5>Expand content</h5>",
                                                        prefixIcon:"e-expander",
                                                                }
                    },
                                        {
                        id: "new",
                        text: "New Button",
                                                        customToolTip:{
                                                                title: "New",
                               content: "New content"
                                                                }
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.dropdownSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-dropdownsettings}








Specify the syncfusion dropdown list members,events using this dropdownSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<style>
.e-cssclass {
     margin-left: 20px;
}
</style>
<script type="text/javascript">  
var fontfamily = ["Segoe UI", "Arial", "Times New Roman", "Tahoma", "Helvetica"];          
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                       id: "fontfamily",
                       toolTip: "Font",
                                                type: ej.Ribbon.type.dropDownList,
                       dropdownSettings: {
                            dataSource: fontfamily,
                            value: "Segoe UI",
                            width: 150
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.enableSeparator<span class="type-signature type boolean">boolean</span>
{:#members:tabs-groups-content-groups-enableseparator}








Specify the separator to the control which is in row type group.The separator separate the control from the next control in the group.Set "true" to enable the separator.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        enableSeparator: true,
                         buttonSettings: {
                         width: 100,
                         }
                    },
                                                {
                        id: "font",
                        text: "Font",
                        toolTip: "Font",
                        buttonSettings: {
                        width: 150,
                        }
                    }],
                                                 defaults: {
                       type: ej.Ribbon.type.button,
                       height: 70
                   }
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.expandedColumns<span class="type-signature type number">number</span>
{:#members:tabs-groups-content-groups-expandedcolumns}








It is used to set the count of gallery contents in a row,when the gallery is in expanded state.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.galleryItems<span class="type-signature type array">array</span>
{:#members:tabs-groups-content-groups-galleryitems}








It is used to define each gallery content.




Default Value:
{:.param}






* array








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.galleryItems.buttonSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-galleryitems-buttonsettings}








Specify the syncfusion button members,events using buttonSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
.e-gallerycontent1{
  font-style: italic;
}
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1",
                                                    buttonSettings:{cssClass:"e-gallerycontent1"}
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.galleryItems.customToolTip<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-galleryitems-customtooltip}








It is used to specify the custom tooltip for gallery content.Please refer ejRibbon#tabs->groups->content->groups->customToolTip for its inner properties.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                    customToolTip:{
                                                         title: "<u>GalleryContent</u>",
                            content: "<b>GalleryContent 1</b>",
                                                         prefixIcon:"e-expander",
                                                        }
                         },
                                                {
                            text:"Content2",
                                                         toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                         toolTip:"GalleryContent3"
                        },
                                                {
                           text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                           text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                           text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.galleryItems.text<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-galleryitems-text}








It is used to set text for the gallery content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.galleryItems.toolTip<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-galleryitems-tooltip}








It is used to set tooltip for the gallery content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.id<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-id}








Specify the Id for button,split button,dropdown list,toggle button,gallery,custom controls in the sub groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.isBig<span class="type-signature type boolean">boolean</span>
{:#members:tabs-groups-content-groups-isbig}








Specify the size for button,split button controls.set "true" for big size and "false" for small size.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        isBig:true,
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 100
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.itemHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:tabs-groups-content-groups-itemheight}








It is used to set the height of each gallery content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.itemWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:tabs-groups-content-groups-itemwidth}








It is used to set the width of each gallery content.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<style>
.e-extracontent .e-extrabtnstyle{
 padding-left: 28px;
 text-align: left;
 }
</style>
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="custommenu">
                        <li><a>New Quick Step</a>
            <ul>
            <li><a>Move to new folder</a></li>
            <li><a>Categorize &amp; Move</a></li>
            <li><a>Flag &amp; Move</a></li>
                </ul>
            </li>
       </ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
        tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                       id: "Gallery",
                                                columns:3,
                                                itemHeight:65,
                                                itemWidth:68,
                                                expandedColumns:4,
                                            type:ej.Ribbon.type.gallery,
                       galleryItems: [{
                           text:"Content1",
                                                        toolTip:"GalleryContent1"
                         },
                                                {
                            text:"Content2",
                                                                toolTip:"GalleryContent2"
                       },
                                            {
                            text:"Content3",
                                                        toolTip:"GalleryContent3"
                        },
                                                {
                            text:"Content4",
                                                        toolTip:"GalleryContent4"
                        },
                                                {
                               text:"Content5",
                                                        toolTip:"GalleryContent5"
                        },
                                                {
                            text:"Content6",
                                                        toolTip:"GalleryContent6"
                        }
                                                ],
                                                customGalleryItems:[{
                                                        customItemType:ej.Ribbon.customItemType.menu,
                                                        menuId:"custommenu",
                                                        menuSettings:{ openOnClick: false}
                        },
                                                {
                            text:"Save Selection as new quick style",
                                                        toolTip:"Save Selection as new quick style",
                                                        customItemType:ej.Ribbon.customItemType.button,
                                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
                        }]
                   }]
                }]
           }]
                }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.splitButtonSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-splitbuttonsettings}








Specify the syncfusion split button members,events using this splitButtonSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<ul id="split">
<li><span>Paste</span></li>
</ul>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        isBig:true,
                        type: ej.Ribbon.type.splitButton,
                        splitButtonSettings: {
                        targetID: "split",
                        buttonMode: "dropdown",
                        arrowPosition:"bottom"
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.text<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-text}








Specify the text for button,split button,toggle button controls in the sub groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.toggleButtonSettings<span class="type-signature type object">object</span>
{:#members:tabs-groups-content-groups-togglebuttonsettings}








Specify the syncfusion toggle button members,events using this toggleButtonSettings.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "bold",
                        toolTip: "Bold",
                        isBig:true,
                        type: ej.Ribbon.type.toggleButton,
                        toggleButtonSettings: {
                        defaultText: "Bold",
                        activeText: "BoldTog"
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.toolTip<span class="type-signature type string">string</span>
{:#members:tabs-groups-content-groups-tooltip}








Specify the tooltip for button,split button,dropdown list,toggle button,custom controls in the sub groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.content.groups.type<span class="type-signature type enum">enum</span>
{:#members:tabs-groups-content-groups-type}








Specify the type as "ej.Ribbon.type.button" or "ej.Ribbon.type.splitButton" or "ej.Ribbon.type.dropDownList" or "ej.Ribbon.type.toggleButton" or "ej.Ribbon.type.custom" or "ej.Ribbon.type.gallery" to render button,split,dropdown,toggle button,gallery,custom controls.




Default Value:
{:.param}






* ej.Ribbon.type.button








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,content: [{
                    groups: [{
                        id: "new",
                        text: "New",
                        toolTip: "New",
                        type: ej.Ribbon.type.button,
                        buttonSettings: {
                        width: 160,
                        height: 50
                        }
                    }]
                }]
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.contentID<span class="type-signature type string">string</span>
{:#members:tabs-groups-contentid}








Specify the ID of custom items to place into the groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.customContent<span class="type-signature type string">string</span>
{:#members:tabs-groups-customcontent}








Specify the HTML contents to place into the groups.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", type: "custom", customContent: "<button id='customContent'>Custom Content</button>"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.enableGroupExpander<span class="type-signature type boolean">boolean</span>
{:#members:tabs-groups-enablegroupexpander}








Specify the group expander for groups in the ribbon control.Set "true" to enable the group expander.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",enableGroupExpander: true,contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.text<span class="type-signature type string">string</span>
{:#members:tabs-groups-text}








Specify the text to the groups in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.groups.type<span class="type-signature type string">string</span>
{:#members:tabs-groups-type}








Specify the custom items such as div,table,controls using the type "custom".




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.id<span class="type-signature type string">string</span>
{:#members:tabs-id}








Specify the ID for each tab's content panel.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### tabs.text<span class="type-signature type string">string</span>
{:#members:tabs-text}








Specify the text of the tab in the ribbon control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}







### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}








Specify the width to the ribbon control.we can set width in string or number format.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
</script>  {% endhighlight %}





## Methods








### addContextualTabs<span class="signature">(contextualTabSet, index)</span>
{:#methods:addcontextualtabs}








It is used to add contextual tab or contextual tab set dynamically in the ribbon control with contextualtabs object and index position.if index is null,ribbon contextual tab or contextual tab set will be added at the last index.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
contextualTabSet{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">contextual tab or contextual tab set object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the contextual tab or contextual tab set,this is optional.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<div id="design">ContextualTab</div>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});
      var cTab={
                                                    backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                            tabs: [
                           {
                                 id: "Design", text: "DESIGN", groups: [{
                                    text: "Table Style", type: "custom", contentID: "design"
                                }
                                ]
                           }]
                       }
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon"); 
        // Add new contextual tab or contextual tab set with given list
         ribbonObj.addContextualTabs(cTab,2);
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<div id="design">ContextualTab</div>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});
      var cTab={
                                                    backgroundColor:"#FCFBEB",borderColor: "#F2CC1C",
                            tabs: [
                           {
                                 id: "Design", text: "DESIGN", groups: [{
                                    text: "Table Style", type: "custom", contentID: "design"
                                }
                                ]
                           }]
                       }   
$("#Ribbon").ejRibbon("addContextualTabs",cTab,2); 
</script>  {% endhighlight %}







### addTab<span class="signature">(tabText, ribbonGroups, index)</span>
{:#methods:addtab}








It is used to add tab dynamically in the ribbon control with given name,tab group array and index position.if index is null,ribbon tab will be added at the last index.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
tabText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">ribbon tab display text.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ribbonGroups{% endhighlight %}</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">groups to be displayed in ribbon tab .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the ribbon tab,this is optional.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
        var tabGroup=[{
               text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "new",
                       text: "New",
                        toolTip: "New"
                   }
                    ],
                    defaults: {
                       type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }];
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon"); 
        // Add new ribbon tab with given list
         ribbonObj.addTab("Tab2",tabGroup,2);
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                     
        var tabGroup=[{
               text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "new",
                       text: "New",
                        toolTip: "New"
                   }
                    ],
                    defaults: {
                       type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }];          
$("#Ribbon").ejRibbon("addTab","Tab2",tabGroup,2); 
</script>  {% endhighlight %}







### addTabGroup<span class="signature">(tabIndex, tabGroup, grpIndex)</span>
{:#methods:addtabgroup}








It is used to add tab group dynamically in the ribbon control with given tab index,tab group object and group index position.if group index is null,ribbon group will be added at the last index.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
tabIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tabGroup{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">group to be displayed in ribbon tab .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
grpIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the ribbon group,this is optional.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {$("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
               text: "One", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "one",
                       text: "one"
                   },{
                       id: "two",
                       text: "two"
                   }],
                    defaults: {
                      type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }]
       }]
  });    
});       
       var ribbonGrp={
                text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "new",
                        text: "New"
                    }],
                    defaults: {
                        type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
                }]
       };
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon"); 
        // Add new ribbon group with given list
        ribbonObj.addTabGroup(1,ribbonGrp,0);
</script>  {% endhighlight %}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {$("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
               text: "One", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "one",
                       text: "one"
                   },{
                       id: "two",
                       text: "two"
                   }],
                    defaults: {
                      type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }]
       }]
  });         
});         
       var ribbonGrp={
                text: "New", alignType: ej.Ribbon.alignType.rows, content: [{
                    groups: [{
                        id: "new",
                        text: "New"
                    }],
                    defaults: {
                        type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
                }]
       };
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon"); 
        $("#Ribbon").ejRibbon("addTabGroup",1,ribbonGrp,0); 
$("#Ribbon").ejRibbon("addTab","Tab2",tabGroup,2); 
</script>  {% endhighlight %}







### addTabGroupContent<span class="signature">(tabIndex, grpIndex, subGrpIndex, content, contentIndex)</span>
{:#methods:addtabgroupcontent}








It is used to add group content dynamically in the ribbon control with given tab index,group index,sub group index,content, content index position.if content index is null,content will be added at the last index.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
tabIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon tab index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
grpIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon group index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
subGrpIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">sub group index in the ribbon group,</td>
</tr>
<tr>
<td class="name">{% highlight html %}
content{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">content to be displayed in the ribbon group.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
contentIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ribbon content index .this is optional.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {$("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
               text: "One", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "one",
                       text: "one"
                   },{
                       id: "two",
                       text: "two"
                   }],
                    defaults: {
                      type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }]
       }]
  });
});       
 var content= {
                   id: "new",
                   text: "new",
               };
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon"); 
        // Add new ribbon content with given list
         ribbonObj.addTabGroupContent(1,0,0,content,2);
</script>  {% endhighlight %}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<script type="text/javascript">   
$(function () {$("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
               text: "One", alignType: ej.Ribbon.alignType.rows, content: [{
                   groups: [{
                       id: "one",
                       text: "one"
                   },{
                       id: "two",
                       text: "two"
                   }],
                    defaults: {
                      type: ej.Ribbon.type.button,
                        width: 60,
                        height: 70
                    }
               }]
           }]
       }]
  });        
});         
 var content= {
                   id: "new",
                   text: "new",
               };
//initialize the Ribbon object
        $("#Ribbon").ejRibbon("addTabGroupContent",1,0,0,content,2); 

</script>  {% endhighlight %}






### hideBackstage<span class="signature">()</span>
{:#methods:hideBackstage}








It is used to hide the ribbon backstage page.





Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // hide the ribbon backstage page.
        ribbonObj.hideBackstage();
</script>{% endhighlight %}
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
$("#Ribbon").ejRibbon("hideBackstage");
</script>{% endhighlight %}







### collapse<span class="signature">()</span>
{:#methods:collapse}








It is used to collapse the ribbon tab content.





Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // collapse the ribbon control.
        ribbonObj.collapse();
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("collapse"); 
</script>  {% endhighlight %}







### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the ribbon widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<script>
var ribbonObj = $("#Ribbon").data("ejRibbon");
ribbonObj.destroy(); // destroy the ribbon
</script>{% endhighlight %}


{% highlight html %}
 
<script>
// destroy the ribbon
$("#Ribbon").ejRibbon("destroy");        
</script>{% endhighlight %}







### expand<span class="signature">()</span>
{:#methods:expand}








It is used to expand the ribbon tab content.





Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // expand the ribbon control.
        ribbonObj.collapse();
        ribbonObj.expand();
</script> {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "700px",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("collapse"); 
$("#Ribbon").ejRibbon("expand"); 
</script>  {% endhighlight %}







### getTabText<span class="signature">(index)</span>
{:#methods:gettabtext}








It is used to get text of the given index tab in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of the tab item.</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

of the given index tab in the ribbon control.


Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // To get text of the given index tab in the ribbon control.
        ribbonObj.getTabText(1);
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                 
$("#Ribbon").ejRibbon("getTabText",1); 
</script>  {% endhighlight %}







### hideTab<span class="signature">(string)</span>
{:#methods:hidetab}








It is used to hide the given text tab in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">srting</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // hide the given text tab item in the ribbon control.
        ribbonObj.hideTab("HOME");
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("hideTab","HOME"); 
</script>  {% endhighlight %}







### isEnable<span class="signature">(string)</span>
{:#methods:isenable}








It is used to check given text tab in the ribbon control is enabled or not.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">srting</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

if it is in enabled state,false if it is in disabled state.


Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        //  To check given text tab in the ribbon control is enabled or not.
        ribbonObj.isEnable("HOME");
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                
$("#Ribbon").ejRibbon("isEnable","HOME"); 
</script>  {% endhighlight %}







### isVisible<span class="signature">(string)</span>
{:#methods:isvisible}








It is used to check given text tab in the ribbon control is visible or not.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">srting</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

if it is visible,false if it is invisible


Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        //  To check given text tab in the ribbon control is visible or not.
        ribbonObj.isVisible("HOME");
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">  
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                   
$("#Ribbon").ejRibbon("isVisible","HOME"); 
</script>  {% endhighlight %}







### removeTab<span class="signature">(index)</span>
{:#methods:removetab}








It is used to remove the given index tab item from the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of tab item.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // Remove the given index tab item from the ribbon control.
        ribbonObj.removeTab(1);
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("removeTab",1); 
</script>  {% endhighlight %}







### setTabText<span class="signature">(string, string)</span>
{:#methods:settabtext}








It is used to set new text to the given text tab in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">current text of the tab item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">new text of the tab item.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // Set new text to the given text tab in the ribbon control.
        ribbonObj.setTabText("HOME","NEW");
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("setTabText","HOME","NEW"); 
</script>  {% endhighlight %}






### showBackstage<span class="signature">()</span>
{:#methods:showBackstage}








It is used to show the ribbon backstage page.





Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
//initialize the Ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // show the ribbon backstage page.
        ribbonObj.showBackstage();
</script>{% endhighlight %}

{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }]
    });
});    
$("#Ribbon").ejRibbon("showBackstage");
</script>{% endhighlight %}







### showTab<span class="signature">(string)</span>
{:#methods:showtab}








It is used to show the given text tab in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
string{% endhighlight %}</td>
<td class="type"><span class="param-type">srting</span></td>
<td class="description last">text of the tab item.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});             
//initialize the ribbon object
        var ribbonObj = $("#Ribbon").data("ejRibbon");
        // hide the given text tab item in the ribbon control.
        ribbonObj.showTab("HOME");
</script>  {% endhighlight %}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }]
  });
});                    
$("#Ribbon").ejRibbon("showTab","HOME"); 
</script>  {% endhighlight %}





## Events








### beforeTabRemove
{:#events:beforetabremove}








Triggered before the ribbon tab item remove.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current tab item index in the ribbon control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      beforeTabRemove: function (args) {}
  });
});             
</script>  {% endhighlight %}







### create
{:#events:create}








Triggered before the ribbon control create.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Ribbon.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      create: function (args) {}
  });
});             
</script>  {% endhighlight %}







### destroy
{:#events:destroy}








Triggered before the ribbon control destroy.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
deleteIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current ribbon tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
       destroy: function (args) {}
  });
});             
</script>  {% endhighlight %}







### groupClick
{:#events:groupclick}








Triggered when the control in the group is clicked successfully .

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the control clicked in the group.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      groupClick: function (args) {}
  });
});             
</script>  {% endhighlight %}







### groupExpand
{:#events:groupexpand}








Triggered when the groupexpander in the group is clicked successfully .

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the clicked groupexpander.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      groupExpand: function (args) {}
  });
});             
</script>  {% endhighlight %}







### galleryItemClick
{:#events:galleryItemClick}








Triggered when an item in the Gallery control is clicked successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.galleryModel{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gallery model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the item clicked in the gallery.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{

       text: "Gallery", alignType: ej.Ribbon.alignType.rows, content: [{
           groups: [{
              id: "Gallery",
                                columns:3,
                                itemHeight:65,
                                itemWidth:68,
                                expandedColumns:4,
                            type:ej.Ribbon.type.gallery,
               galleryItems: [{
                   text:"Content1",
                                        toolTip:"GalleryContent1"
                 },
                                {
                   text:"Content2",
                                         toolTip:"GalleryContent2"
              },
                            {
                   text:"Content3",
                                         toolTip:"GalleryContent3"
               },
                                {
                   text:"Content4",
                                        toolTip:"GalleryContent4"
                },
                                {
                   text:"Content5",
                                        toolTip:"GalleryContent5"
               },
                                {
                  text:"Content6",
                                        toolTip:"GalleryContent6"
               }
                                ],
                                customGalleryItems:[{
                                        customItemType:ej.Ribbon.customItemType.menu,
                                        menuId:"custommenu",
                                        menuSettings:{ openOnClick: false}
                },
                                {
                    text:"Save Selection as new quick style",
                                     
                                        customItemType:ej.Ribbon.customItemType.button,
                                        buttonSettings:{cssClass:"e-extrabtnstyle"}
               }]
          }]
       }]
  }]
        }],
      galleryItemClick: function (args) {}
  });
});             
</script>  {% endhighlight %}






### backstageItemClick
{:#events:backstageItemClick}








Triggered when a tab or button in the backstage page is clicked successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the item clicked in the gallery.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the id of the target item.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the text of the target item.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="content1">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Info</div>
<li>Protect Workbook</li>
<li>Inspect Workbook</li>
<li>Versions</li>
<li>Browser View Options</li>
</ul>
</div>
<div id="content2">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Open</div>
<li>Recent Workbooks</li>
<li>Computer</li>
</ul>
</div>
<div id="content3">
<ul style="list-style:none"><div style="margin-left:30px;font-size:20px">Export</div>
<li>Create PDF/XPS Document</li>
<li>Change File Type</li>
</ul>
</div>
<div id="Ribbon"></div>
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function() {
    $("#Ribbon").ejRibbon({
        width: "500px",
        applicationTab: {
            type: ej.Ribbon.applicationTabType.backstage,
            backstageSettings: {
                text: "FILE",
                height: 250,
                width: 600,
                headerWidth: 125,
                pages: [{
                    id: "info",
                    text: "Info",
                    itemType: ej.Ribbon.itemType.tab,
                    contentID: "content1"
                }, {
                    id: "open",
                    text: "Open",
                    contentID: "content2"
                }, {
                    id: "export",
                    text: "Export",
                    contentID: "content3",
                    enableSeparator: true
                }, {
                    id: "exit",
                    text: "Exit",
                    itemType: ej.Ribbon.itemType.button
                }]
            }
        },
        tabs: [{
            id: "home",
            text: "HOME",
            groups: [{
                text: "New",
                alignType: ej.Ribbon.alignType.rows,
                type: "custom",
                contentID: "btn"
            }]
        }],
      backstageItemClick : function (args) {}
    });
});   
</script>{% endhighlight %}






### collapse
{:#events:collapse}








Triggered when the ribbon control is collapsed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      collapse: function (args) {}
  });
});             
</script>  {% endhighlight %}






### expand
{:#events:expand}








Triggered when the ribbon control is expanded.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      expand: function (args) {}
  });
});             
</script>  {% endhighlight %}







### tabAdd
{:#events:tabAdd}








Triggered after adding the new ribbon tab item.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tabHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns new added tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tabContent{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns new added tab content panel.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      tabAdd: function (args) {}
  });
});             
</script>  {% endhighlight %}







### tabClick
{:#events:tabClick}








Triggered when tab is clicked successfully in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
     tabClick: function (args) {}
  });
});             
</script>  {% endhighlight %}







### tabCreate
{:#events:tabCreate}








Triggered before the ribbon tab create.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
deleteIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current ribbon tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      tabCreate: function (args) {}
  });
});             
</script>  {% endhighlight %}







### tabRemove
{:#events:tabRemove}








Triggered after the tab item removed from the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
removedIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the removed index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      tabRemove: function (args) {}
  });
});             
</script>  {% endhighlight %}







### tabSelect
{:#events:tabSelect}








Triggered after the ribbon tab item selected in the ribbon control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
    tabSelect: function (args) {}
  });
});             
</script>  {% endhighlight %}







### toggleButtonClick
{:#events:toggleButtonClick}








Triggered when the expand/collapse button is clicked successfully .

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ribbon model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the expand/collapse button.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="menu">
<li><a>FILE </a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
<li><a>Save</a></li>
<li><a>Save as</a></li>
<li><a>Print</a></li>
</ul></li></ul>
<div id="Ribbon"></div> 
<button id="btn">Home button</button>
<script type="text/javascript">   
$(function () {
    $("#Ribbon").ejRibbon({
// Set the width during initialization.         
     width: "100%",
       applicationTab: { type: ej.Ribbon.applicationTabType.menu, menuItemID: "menu", menuSettings: { openOnClick: false } },
       tabs: [{
           id: "home", text: "HOME", groups: [{
                text: "New", alignType: ej.Ribbon.alignType.rows,type:"custom",contentID:"btn"
           }]
        }],
      toggleButtonClick: function (args) {}
  });
});             
</script>  {% endhighlight %}




