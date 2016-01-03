---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Calculate
documentation: ug
---

# Getting Started

This section explains how to create an application with CalcEngine support in JavaScript. The following screenshot shows the formula support of CalcEngine for JavaScript. For example: “=SUM(A1:A8)”.

![](/js/Calculate/Getting-Started_images/Getting-Started_img1.png)

## Configuring Calculate in JavaScript

This section encompasses the details on how you can configure the **calculate** in your application for formula calculation manually.

**Add Scripts and Styles**

Add the script files and CSS files in the title tag of the default.html page.

N>  Keep the following order while adding the scripts and styles.



{% highlight html %}
  
<link href="http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" />
<script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"> </script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js" type="text/javascript"> </script>
<script src=" http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js" type="text/javascript"></script>

{% endhighlight %}

**Add Control in HTML page**

1. Add the following code example inside the **&lt;body&gt;** tag in the default.html page.

   ~~~

	<!-- ... -->
	<head>
	<body>
		<div id="Grid"></div>
		</body>
	<!-- ... -->
	<script type="text/javascript">
			$(function () {

				var calcObj = new CalcEngine($("#Grid"));
				calcObj.setUseDependencies(true);
				calcObj.registerGridAsSheet("Sheet1", $("#Grid"), "0");
	</script>
	</head>
	<!-- ... -->

   ~~~
   {:.prettyprint}



2. Add the following code example in button click to compute the formula. Clicking on **CalcEngine** computes the required data from the grid and returns the result.

   ~~~

	 $("input:button").ejButton({
						click: function (args) {
							if (document.activeElement.value == "Compute") {
								try
								{
									var value = calcObj.parseAndComputeFormula($("#formulaTxt").val());
									document.getElementById("result").innerHTML = value;
								}
								catch(ex)
								{
									alert(ex.message);
								}
							}
							else if (document.activeElement.value == "OK") {
								$("#Grid").data("ejGrid")._triggerConfirm(args);
							}
							else if (document.activeElement.value == "Cancel") {
								$("#Grid").data("ejGrid")._triggerConfirm(args);
							}
						}
					});


   ~~~
   {:.prettyprint}

3. The following function must be included in the HTML file. These methods only act as intermediate to transfer the data between **CalcEngine** and the **Grid.**



   **GetValueFromRowCol**

   Get the value of cell based on the excel like rowIndex and colIndex.

   ~~~

	 calcObj.getValueRowCol = function (sheetID,row, col) {
					   //return the data based on row and column index
					}

   ~~~
   {:.prettyprint}




   **SetValueFromRowCol**

   Set the computed value of cell based on the excel like rowIndex and colIndex when formula is applied in cell.

   ~~~

   calcObj.setValueRowCol = function (sheetID, value, row, col) {

            //set the value to grid cell
        }

   ~~~
   {:.prettyprint}



