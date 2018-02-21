---
layout: post
title: Template support with DropDownTree widget for Syncfusion Essential JS
description: Template Support with DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: Template Support, DropDownTree, dropdowntree, Header Template
api: /api/js/ejDropDownTree
---

# Template Support

By default, you can add any text or image to the DropDownTree list item. To customize the items layout or to create your own visualized elements use this template support.

You can create the popup header by using [headerTemplate](https://help.syncfusion.com/api/js/ejdropdowntree#members:headertemplate) property and footer by using [footerTemplate](https://help.syncfusion.com/api/js/ejdropdowntree#members:footertemplate). You can add any HTML content in header and footer template.


## Template Field

Create a set of div containers with common syntax or elements, and assign it to the `template` property of the [`treeViewSettings`](https://help.syncfusion.com/api/js/ejdropdowntree#members:treeviewsettings) property. You can add any HTML mark-up element inside the DropDownTree list using this property.

In the demo, a JSON array is created with text, imgId, role and country initialized with dataSource property. Content template is created by using the corresponding fields, and assigned in template property. The content template is customized with images and custom CSS styles to visualize the items in popup.

{% highlight html %}

<input type="text" id="empList" />

{% endhighlight %}

{% highlight css %}
	
.e-treeview .e-node-hover, .e-treeview .e-active {
    background: transparent;
    border-color: transparent;
}

.e-treeview .e-node-hover {
    opacity: 0.8;
}
.header, .footer {
    background-color: #a9a9a9;
    font-family: "Trajan Pro";
    font-size: 15px;
    color: white;
    text-align: center;
    height: 25px;
    text-transform: uppercase;
    padding-top: 9px;
    }
.footer {
                background-color: #dadada;
}
.eimg {
                margin: 0;
                padding: 3px 10px 3px 3px;
                border: 0 none;
                width: 60px;
                height: 60px;
                float: left;
}

.ename {
    font-weight: bold;
    padding: 6px 3px 1px 3px;
}

.cont {
    font-size: smaller;
    padding: 3px 3px -1px 0px;
}


{% endhighlight %}

{% highlight javascript %}
<script id="treeTemplate" type="text/x-jsrender">
    {{if hasChild}}
    <div class={{>cls}}>{{>text}}</div>
    {{else}}
    <div class="cont-list">
        <img class="eimg" src="../content/images/combobox/{{>eimg}}.png" alt="employee" />
        <div class="ename"> {{>text}} </div>
        <div class="cont"> {{>country}} </div>
    </div>
    {{/if}}
</script>
$(function() {

    var treeData = [{
            id: 1,
            text: "Software Engineer",
            hasChild: true,
            expanded: true
        },
        {
            id: 2,
            pid: 1,
            imgId: "3",
            text: "Erik Linden",
            eimg: "3",
            country: "England"
        },
        {
            id: 3,
            pid: 1,
            imgId: "8",
            text: "Louis",
            eimg: "7",
            country: "Australia"
        },
        {
            id: 4,
            text: "Tester",
            hasChild: true,
            expanded: true
        },
        {
            id: 5,
            pid: 4,
            imgId: "6",
            text: "John Linden",
            eimg: "6",
            country: "Norway"
        },
        {
            id: 6,
            pid: 4,
            imgId: "7",
            text: "Lawrence",
            eimg: "8",
            country: "India"
        }
    ];



    $('#selectCar').ejDropDownTree({
        watermarkText: "Select a car",
        width: "30%",
        headerTemplate: '<div class="header"><span>Employees </span></div>',
        footerTemplate: '<div class="footer"> <span>End of list</span></div>',
        treeViewSettings: {
            fields: {
                dataSource: treeData,
                id: "id",
                parentId: "pid",
                text: "text",
                hasChild: "hasChild"
            },
            template: "#treeTemplate"
        }
    });

    var treeObj = $("#treeview").data("ejTreeView");
});

{% endhighlight %}

N> Images for this sample are available in (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\samples\web\themes\images<br/>

![](TemplateSupport_images/template-support.png)

