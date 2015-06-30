---
layout: post
title: Context-Menu
description: context menu
platform: js
control: PivotGrid
documentation: ug
---

# Context Menu

**Cell Context** support in **PivotGrid** allows you to choose the right-click event to access each cell for any desired operation. Context Menu is enabled by setting the [enableCellContext](/js/api/ejPivotGrid#enablecellcontextspan-classtype-signature-type-booleanbooleanspan) property to ‘**True**’.

The following code example illustrates how to create the **PivotGrid** control with the enabled Context Menu. Here, the Cell Context event displays a pop-up menu as follows.

{% highlight css %}
 
        .menuItem {
            padding:5px 50px 5px 20px;
        }
        .row .cols-prop-area {min-height: 170px !important;}
        .contextMenuPopup {
            position: absolute;
            background-color: #e6e6e6;
            border: #BBBCBB solid 1px;
            padding: 1px;
            color:#565656;
        }
        .activeMenuItemBlue {
            background-color:#66C1DC;
            color:white;
        }
        .activeMenuItemGreen {
            background-color:#AECF49;
            color:white;
        }
        .activeMenuItemOrange {
            background-color:#F9920B;
            color:white;
        }

{% endhighlight %}

{% highlight js %}
 $(function() {
    $(document).bind("click", function() {
        $(".contextMenuPopup").remove();
    });
    $("#PivotGrid1").ejPivotGrid({
        url: "../wcf/CellContextService.svc",
        enableCellContext: true,
        cellContext: "cell_RightClick"
    });
});
cell_RightClick = function(evt) {
    $(".contextMenuPopup").remove();
    var contextMenu = $('<div class="contextMenuPopup"></div>');
    $(contextMenu[0]).html('<div class="menuItem">Cell Type</div><div class="menuItem">Position</div><div class="menuItem">Value</div>');
    $(contextMenu[0]).css("left", evt.args.args.clientX + 10).css("top", evt.args.args.clientY + 10);
    $("#PivotGrid1").append(contextMenu[0]);
    $(".menuItem").bind("mouseenter", function(e) {
        var bgColor = ($(".summary").css("background-color") != "transparent" && $(".summary").css("background-color") != "rgb(31, 31, 31)") ? $(".summary").css("background-color") : $(".summary").css("color");
        if (bgColor == "rgb(204, 237, 255)" || bgColor == "rgb(94, 171, 222)" || bgColor == "rgb(104, 195, 222)")
            $(this).addClass("activeMenuItemBlue")
        else if (bgColor == "rgb(247, 252, 182)" || bgColor == "rgb(145, 170, 41)" || bgColor == "rgb(169, 199, 78)")
            $(this).addClass("activeMenuItemGreen")
        else if (bgColor == "rgb(255, 238, 169)" || bgColor == "rgb(250, 161, 19)" || bgColor == "rgb(255, 187, 96)")
            $(this).addClass("activeMenuItemOrange")
    });
    $(".menuItem").bind("mouseleave", function(e) {
        $(this).removeClass("activeMenuItemBlue").removeClass("activeMenuItemGreen").removeClass("activeMenuItemOrange");
    });
    $(".menuItem").click(function(e) {
        alert("click event occurs");
    });
}
{% endhighlight %}

The output of the above code creates a **PivotGrid** with **Cell Context** options as shown in the following screenshot.

{% include image.html url="/js/PivotGrid/Context-Menu_images/Context-Menu_img1.png" %}

