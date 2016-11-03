---
layout: post
title: Clipboard with Spreadsheet widget for Syncfusion Essential JS
description: How to use the Spreadsheet Clipboard
platform: js
control: Spreadsheet
documentation: ug
---

# Clipboard

The Spreadsheet provides support for the clipboard operations (cut, copy, and paste) in all text, chart and images. You can use [`allowClipboard`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowclipboard "allowClipboard") property to enable/disable this feature. You have following clipboard operations.

* Cut
* Copy
* Paste

## Cut

This function takes the back up of selected range values and removed from the selected range.

You can do this by one of the following ways. 

* By pressing "Ctrl-X" or using Cut button of HOME tab in ribbon to perform cut operation.
* Using [`cut`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlclipboard-cut "cut") method.

## Copy

This function takes the back up of selected range values.

You can do this by one of the following ways. 

* By pressing "Ctrl-C" or using Copy button of HOME tab in ribbon to perform copy operation.
* Using [`copy`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlclipboard-copy "copy") method.

## Paste

This function pastes the content from the back up storage to newly selected range and clears the back up storage. 

You have following options in Paste.

* Paste Special - You can paste the values with formatting.
* Paste - You can paste only the values.

N> The default paste option is Paste Special. This is working only within the current Spreadsheet. If you copy the content from other sources, it will paste only the values in the Spreadsheet.

You can do this by one of the following ways,

* By pressing "Ctrl-V" or using Paste button of HOME tab in ribbon to perform paste operation.
* Using [`paste`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlclipboard-paste "paste") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Spreadsheet"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.min.js'
        sheets: [{
            rangeSettings: [{ dataSource: window.defaultData, startCell: "A1" }],                               
        }],
        allowClipboard: true,
        loadComplete: "loadComplete"
    });
});
function loadComplete() {
    var xlClip = this.XLObj.XLClipboard;
    this.XLObj.performSelection("G1:H3");
    xlClip.cut(); // Cut the selected cells
    //xlClip.copy();//Copy the selected cells.
    this.XLObj.performSelection("J4");
    xlClip.paste();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Clipboard_images/Clipboard_img2.png)