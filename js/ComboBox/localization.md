---
layout: post
title: Localization with ComboBox widget for Syncfusion Essential JS
description: Describes about the localization in ComboBox widget for Syncfusion Essential JS.
platform: js
control: ComboBox
documentation: ug
keywords: ComboBox, ComboBox, Localization
---

# Localization

The Localization library allows you to localize static text content of the [noRecordsTemplate](https://help.syncfusion.com/api/js/ejcombobox#members:norecordstemplate) and [actionFailureTemplate](https://help.syncfusion.com/api/js/ejcombobox#members:actionfailuretemplate) &nbsp;properties according to the culture currently assigned to the ComboBox.

| Locale key | en-US (default)  |
|------|------|-------------|
| noRecordsTemplate |  No records found |
| actionFailureTemplate | The request failed |

## Loading Translations

In the following sample, French culture is set to the ComboBox and no data is loaded. Hence, the `noRecordsTemplate` property displays its text in French culture initially, and if the sample is run offline, the `actionFailureTemplate` property displays its text appropriately.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">
        ej.ComboBox.Locale["fr-BE"] = {
        'noRecordsTemplate': "Aucun enregistrement trouvé",
        'actionFailureTemplate': "Modèle d'échec d'action"
    };
    // DataManager creation
    var dataManger = ej.DataManager({
        url: window.baseurl + "Wcf/Northwind.svc/", crossDomain: true
    });
    // Query creation
    var query = ej.Query()
            .from("Customers").take(0);
    $(function () {
        $('#list').ejComboBox({
            dataSource: dataManger,
            placeholder: 'Select a customer',
            fields: { text: "CustomerID",value: "CustomerID" },
            placeholder: "Select a customer",
            query: query,
            width: "100%"
        });
    });

</script>		
		
{% endhighlight %}

![](localization_images/localization_image1.png)