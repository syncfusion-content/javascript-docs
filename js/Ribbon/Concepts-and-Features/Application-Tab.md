---
layout: post
title: Application-Tab
description: application tab
platform: js
control: Ribbon
documentation: ug
---

# Application Tab

The **application menu** support is provided in the Ribbon control application tab. Use **applicationTab** property to define the application tab with menu. In **applicationTab** definition, Type property defines the application menu and the value is **ApplicationMenu**, **itemID** property to specify ID of UL list for application menu and **menuSettings** property to specify all the members and events of the menu.

{% highlight html %}

**[JS]**

**[HTML]**
<!-- ... -->
<head>
</head>
<!-- ... -->
<body>
<div id="Ribbon"></div>
<ul id="menu">
<li><a>FILE</a>
<ul>
<li><a>New</a></li>
<li><a>Open</a></li>
</ul>
</li>
</ul>
<div id="Contents">Custom control</div>
<script type="text/javascript">
$(function () {
$("#Ribbon").ejRibbon({
width: "800px",
applicationTab: { Type: "ApplicationMenu", itemID: "menu", menuSettings: { openOnClick: false } },
tabs: [{
id: "home", text: "HOME", groups: [
{
text: "CustomControls", type: "custom", contentID: "Contents"
}]
}]
});
});
</script>
</body>
<!-- ... -->


{% endhighlight %}



The following screenshot illustrates **Ribbon** with application menu.

{% include image.html url="/js/Ribbon/Concepts-and-Features/Application-Tab_images/Application-Tab_img1.png" Caption="Ribbon control with the application tab menu."%}

