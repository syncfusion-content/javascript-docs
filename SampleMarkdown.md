---
layout: post
title: Code Snippet
documentation: ug
platform: js
---

#Code Snippet

# `C#`

## C# With highlight

{% highlight c#  %}



public class WordCountMapper : MapperBase
{
	public override void Map(string inputLine, MapperContext context)
	{
		try
		{
			string[] words = inputLine.Split(' ');
			foreach (string word in words)
			
				context.EmitKeyValue(word, "1");
				
		}
		catch (ArgumentException ex)
		{
			return;
		}
	}
}
{% endhighlight %} 

{% highlight c#  %}
public class WordCountMapper : MapperBase
{
	public override void Map(string inputLine, MapperContext context)
	{
		try
		{
			string[] words = inputLine.Split(' ');
			foreach (string word in words)
			
				context.EmitKeyValue(word, "1");
				
		}
		catch (ArgumentException ex)
		{
			return;
		}
	}
}
{% endhighlight %} 

#HTML Code

##HTML with highlight

{% highlight html  %}
<!DOCTYPE html>

		<html>

			<head>

				<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

				<!-- style sheet for default theme(flat azure) -->

					<link href="<http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css>" rel="stylesheet" />

				<!--scripts-->
			
					<script src=" http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js "></script>

					<script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>

					<script src=" http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js "></script>

					<script src="<http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js>"> </script>

			</head>

			<body>

				<!-- add datepicker element here --->

			</body>

		</html>
{% endhighlight %} 

#JavaScript 

##JavaScript with Highlight

{% highlight js %}
var minDatepicker,maxDatepicker;

var curdate = new Date();// mentions the current date.

// Set the return date to60 days from the current date.

var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 60);
$(function () {

	// declaration

	$("#startDate").ejDatePicker({

		value: curdate, // the current date is used as the default value

		minDate: curdate,// Default date is set to mindate.
		
		maxDate: rangeDate, // 60 –days of interval from min date.

		select: "selectedStartDate"//select event functionality.

	});

	$("\#endDate").ejDatePicker({

		value: curdate, // the current date is used as the default value

		minDate: curdate, // Default date as mindate.

		maxDate: rangeDate, // 60 –days of interval from min date.

		select: " selectedEndDate"//select event functionality.

	});

});

function selectedStartDate (sender) {

	var selDate = new Date(sender.value); // mentions the selected date.

	minDatepicker = \$("\#endDate").data("ejDatePicker");// creating DatePicker object

	minDatepicker.setModel({ "minDate": selDate });// setting minDate property through setModel of DatePicker object.

}
function selectedEndDate(sender) {

	var selDate = new Date(sender.value);

	maxDatepicker = \$("\#startDate").data("ejDatePicker");// creating DatePicker object

	maxDatepicker.setModel({ "maxDate": selDate });// setting maxDate property through setModel of DatePicker object.
}
{% endhighlight %}


#CSS

##CSS With Highlight
{% highlight css %}
.tdclass
{
	width: 300px;
	font-weight: bold;
}
.innerdp
{
	.tdclass
	{
		width: 300px;
		font-weight: bold;
	}

	display: inline-block;
}
{% endhighlight %}
	
#Image

## Normal image With out caption 

![Alt text](/images/jekyll.png "Testing Image Title")

##Image with Caption 

{% include image.html url="/images/jekyll.png" Caption="Image using separate HTML" %}

#Tables


|Table Header|thead|
|:---:|---:|
|Table Content \n |tr|
|Table Content|tr|
|Table Content|tr|


| Feature                                         | IE  | Firefox | Chrome | Safari      | Opera |  Works w/o JavaScript
| ---                                             | --- | ---     | ---    | ---         | ---   |  ---
| Styled upload button                            | ✓   | ✓       | ✓      | ✓           | ✓     |  ✓|
| Styled upload button                            | ✓   | ✓       | ✓      | ✓           | ✓     |  ✓

|Table Header|thead
|---|---
|Table Content|tr'\'td
|Table Content|tr
|Table Content|tr




|             |          Grouping           ||
First Header  | Second Header | Third Header |
 ------------ | :-----------: | -----------: |
Content       |          *Long Cell*        
Content       |   **Cell**    |         Cell |





