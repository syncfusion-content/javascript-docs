---
layout: post
title:  Ribbon - Overview
description: Ribbon Localization
documentation: ug
platform: js
keywords: overview
---


# Localization

## Localization

The localization support allows to customize the display of text within the Ribbon in a user-specific culture and locale. The Ribbon control can be localized in specific culture using the common API [`locale`](http://help.syncfusion.com/js/api/ejribbon#members:locale) along with the collection of localized words defined for that culture using the ej.Ribbon.Locale [culture-code].Please find the table with list of properties and its value in locale object.

<table>
<tr>
<th>
Locale key words </th><th>
Text</th></tr>
<tr>
<td>
CustomizeQuickAccess</td><td>
Customize Quick Access Toolbar</td></tr>
<tr>
<td>
RemovefromQuickAccessToolbar</td><td>
Remove from Quick Access Toolbar</td></tr>
<tr>
<td>
AddtoQuickAccessToolbar</td><td>
Add to Quick Access Toolbar</td></tr>
<tr>
<td>
ShowAbovetheRibbon</td><td>
Show Above the Ribbon</td></tr>
<tr>
<td>
ShowBelowtheRibbon</td><td>
Show Below the Ribbon</td></tr>
<tr>
<td>
MoreCommands</td><td>
More Commands...</td></tr>
</table>

N> By default, the Ribbon control is localized in `en-US` culture.

For further information on – how to refer the required culture scripts into your application, refer [`here`](http://help.syncfusion.com/js/localization).

{% highlight html %}

    <div id="defaultRibbon"></div>
              <ul id="ribbonmenu">
                <li><a>FILE</a>
                 <ul>
                 <li><a>New</a></li>
                 </ul>
               </li>
            </ul>
          </div>
    <script>
	ej.Ribbon.Locale["es-ES"] = {
		CustomizeQuickAccess: "Agordu Rapida Aliro",
		RemovefromQuickAccessToolbar: "Forigu de Rapida Aliro Ilobreto",
		AddtoQuickAccessToolbar: "Aldoni al Rapida Aliro Ilobreto",
		ShowAbovetheRibbon: "Montru Super la Ribbona",
		ShowBelowtheRibbon: "Montru Sube la Ribbon",
		MoreCommands: "pli Komando"
	};
	$(function() {
		$("#defaultRibbon").ejRibbon({
			width: "600",
			locale: "es-ES",
			showQAT: true,
			applicationTab: {
				type: ej.Ribbon.applicationTabType.menu,
				menuItemID: "ribbonmenu",
				menuSettings: {
					openOnClick: false
				}
			},
			tabs: [{
				id: "home",
				text: "HOME",
				groups: [{
					text: "Clipboard",
					alignType: ej.Ribbon.alignType.columns,
					content: [{
						groups: [{
							id: "paste",
							text: "paste",
							toolTip: "Paste",
							quickAccessMode: ej.Ribbon.quickAccessMode.toolBar,
							splitButtonSettings: {
								contentType: ej.ContentType.ImageOnly,
								prefixIcon: "e-ribbon e-ribbonpaste",
								targetID: "pasteSplit",
								buttonMode: "dropdown",
								arrowPosition: ej.ArrowPosition.Bottom,
								click: "executeAction"
							}
						}],
						defaults: {
							type: ej.Ribbon.type.splitButton,
							width: 50,
							height: 70
						}
					}]
				}]
			}]
		});
	});
	</script>

{% endhighlight %}

![](/js/Ribbon/Localization_images/Localization_img1.png)