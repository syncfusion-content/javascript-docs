---
layout: post
title: Filtering in ComboBox widget for Syncfusion Essential JS
description: Describes about the filtering in ComboBox widget for Syncfusion Essential JS
platform: js
control: ComboBox
documentation: ug
keywords: ComboBox, combobox, Filtering, minimum filter character, filter type
---

# Filtering

The ComboBox has built-in support to filter data items when [allowFiltering](https://help.syncfusion.com/api/js/ejcombobox#members:allowfiltering) is enabled. The filter operation starts as soon as you start typing characters in the component.

To display filtered items in the popup, filter the required data and return it to the ComboBox via [updateData](https://help.syncfusion.com/api/js/ejcombobox#members:fields) method by using the [filtering](https://help.syncfusion.com/api/js/ejcombobox#events:filtering) event.

The following sample illustrates how to query the data source and pass the data to the ComboBox through the `updateData` method in `filtering` event.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">

    var sportsData = [
        { id: 'level1', game: 'American Football' }, { id: 'level2', game: 'Badminton' },
        { id: 'level3', game: 'Basketball' }, { id: 'level4', game: 'Cricket' },
        { id: 'level5', game: 'Football' }, { id: 'level6', game: 'Golf' },
        { id: 'level7', game: 'Hockey' }, { id: 'level8', game: 'Rugby' },
        { id: 'level9', game: 'Snooker' }, { id: 'level10', game: 'Tennis' }
        ];
    var query = new ej.Query().select(['game', 'id']);
    $(function () {
        $('#list').ejComboBox({
            dataSource: sportsData,
            query: query.take(5),
            fields: { text: 'game', value: 'id' },
            placeholder: 'Select a game',
            popupHeight: '230px',
            allowFiltering: true,
            filtering: function(e){
                var query = new ej.Query().select(['game', 'id']);
                query = (e.text !== '') ? query.where('game', 'startswith', e.text, true) : query;
                e.updateData(sportsData, query);
            }
        });
    });

</script>	
		
{% endhighlight %}

![](Filtering_images/Filtering_image1.png)

## Limit the Minimum Filter Character

When filtering the list items, you can set the limit for character count to raise remote request and fetch filtered data on the ComboBox. This can be done by manual validation within the filter event handler.

In the following example, the remote request does not fetch the search data until the search key contains three characters.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">

    var sportsData = [
        { id: 'level1', game: 'American Football' }, { id: 'level2', game: 'Badminton' },
        { id: 'level3', game: 'Basketball' }, { id: 'level4', game: 'Cricket' },
        { id: 'level5', game: 'Football' }, { id: 'level6', game: 'Golf' },
        { id: 'level7', game: 'Hockey' }, { id: 'level8', game: 'Rugby' },
        { id: 'level9', game: 'Snooker' }, { id: 'level10', game: 'Tennis' }
        ];
    var query = new ej.Query().select(['game', 'id']);
    $(function () {
        $('#list').ejComboBox({
            dataSource: sportsData,
            query: query.take(5),
            fields: { text: 'game', value: 'id' },
            placeholder: 'Select a game',
            popupHeight: '230px',
            allowFiltering: true,
            filtering: function(e){
                // load overall data when search key empty.
                if(e.text == '') e.updateData(sportsData);
                else{
                    // restrict the remote request until search key contains 3 characters.
                    if (e.text.length < 3) { return; }
                    var query = new ej.Query().select(['country', 'id']);

                    query = (e.text !== '') ? query.where('country', 'startswith', e.text, true) : query;
                    e.updateData(sportsData, query);
                }
            }
        });
    });

</script>	
		
{% endhighlight %}

![](Filtering_images/Filtering_image2.png)

## Change the Filter Type

While filtering, you can change the filter type to `contains`, `startsWith`, or `endsWith` for string type within the filter event handler.

In the following examples, data filtering is done with `endsWith` type.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">

    var sportsData = [
        { id: 'level1', game: 'American Football' }, { id: 'level2', game: 'Badminton' },
        { id: 'level3', game: 'Basketball' }, { id: 'level4', game: 'Cricket' },
        { id: 'level5', game: 'Football' }, { id: 'level6', game: 'Golf' },
        { id: 'level7', game: 'Hockey' }, { id: 'level8', game: 'Rugby' },
        { id: 'level9', game: 'Snooker' }, { id: 'level10', game: 'Tennis' }
        ];
    var query = new ej.Query().select(['game', 'id']);
    $(function () {
        $('#list').ejComboBox({
            dataSource: sportsData,
            query: query.take(5),
            fields: { text: 'game', value: 'id' },
            placeholder: 'Select a game',
            popupHeight: '230px',
            allowFiltering: true,
            filtering: function(e){
                // load overall data when search key empty.
                if(e.text == '') e.updateData(sportsData);
                else{
                    var query = new ej.Query().select(['country', 'id']);
                    query = (e.text !== '') ? query.where('country', 'endswith', e.text, true) : query;
                    e.updateData(sportsData, query);
                }
            }
        });
    });

</script>	
		
{% endhighlight %}

![](Filtering_images/Filtering_image3.png)

## Case Sensitive Filtering

Data items can be filtered either with or without case sensitivity using the DataManager. This can be done by passing the fourth optional parameter of the [where](https://help.syncfusion.com/api/js/ejquery#methods:where) clause.

The following example shows how to perform case-sensitive filter.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
<script type="text/javascript">

    var sportsData = [
        { id: 'level1', game: 'American Football' }, { id: 'level2', game: 'Badminton' },
        { id: 'level3', game: 'Basketball' }, { id: 'level4', game: 'Cricket' },
        { id: 'level5', game: 'Football' }, { id: 'level6', game: 'Golf' },
        { id: 'level7', game: 'Hockey' }, { id: 'level8', game: 'Rugby' },
        { id: 'level9', game: 'Snooker' }, { id: 'level10', game: 'Tennis' }
        ];
    var query = new ej.Query().select(['game', 'id']);
    $(function () {
        $('#list').ejComboBox({
            dataSource: sportsData,
            query: query.take(5),
            fields: { text: 'game', value: 'id' },
            placeholder: 'Select a game',
            popupHeight: '230px',
            allowFiltering: true,
            filtering: function(e){
                // load overall data when search key empty.
                if(e.text == '') e.updateData(sportsData);
                else{
                    var query = new ej.Query().select(['country', 'id']);
                    //enable the case sensitive filtering by passing false to 4th parameter.
                    query = (e.text !== '') ? query.where('country', 'startswith', e.text, false) : query;
                    e.updateData(sportsData, query);
                }
            }
        });
    });

</script>	
		
{% endhighlight %}

![](Filtering_images/Filtering_image4.png)