---
layout: post
title: Properties, Methods and Events of ejCalculate Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom engine to perform calculation like excel sheet
$(element).ejCalculate<span class="signature">()</span>
Example
{:.example}


{% highlight html %}
 
<script>
// Create calcEngine with grid data
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core.js


* module:ej.calculate.js




## Methods








### addCustomFunction<span class="signature">(FormulaName, FunctionName)</span>
{:#methods:addcustomfunction}








Add the custom formulas with function in CalcEngine library

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
FormulaName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the formula name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
FunctionName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the custom function name to call</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Grid"></div> 
<script>
// Create Grid
$('#Grid').ejGrid({
    dataSource: window.gridData
});         
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
var sheetID = calcObj.createSheetFamilyID();
calcObj.registerGridAsSheet("sheet1", $("#Grid").data("ejGrid"), sheetID);
calcObj.addCustomFunction("ADD", "customAdd");
   customAdd = function (argsList) {
   var splitArgs = argsList.split(calcObj.getParseArgumentSeparator())
      var result = 0;
      for (var i in splitArgs) {
          var s1 = calcObj.getValueFromArg(splitArgs[i]);
          result = Number(result) + Number(s1);
      }
      return result;
   }
</script>{% endhighlight %}







### addNamedRange<span class="signature">(Name, cellRange)</span>
{:#methods:addnamedrange}








Adds a named range to the NamedRanges collection

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
Name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the namedRange's name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellRange{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell range of NamedRange</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Grid"></div> 
<script>
// Create Grid
$('#Grid').ejGrid({
    dataSource: window.gridData
});         
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
var sheetID = calcObj.createSheetFamilyID();
calcObj.registerGridAsSheet("sheet1", $("#Grid").data("ejGrid"), sheetID);
calcObj.addNamedRange("FIRSTCELL","A1");
</script>{% endhighlight %}







### adjustRangeArg<span class="signature">(Name)</span>
{:#methods:adjustrangearg}








Accepts a possible parsed formula and returns the calculated value without quotes.

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
Name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell range to adjust its range</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

string


Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
var sheetID = calcObj.createSheetFamilyID();
calcObj.registerGridAsSheet("sheet1", $("#Grid").data("ejGrid"), sheetID);
calcObj.addNamedRange("FIRSTCELL","A1");
</script>{% endhighlight %}







### clearFormulaDependentCells<span class="signature">(Cell)</span>
{:#methods:clearformuladependentcells}








When a formula cell changes, call this method to clear it from its dependent cells.

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
Cell{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the changed cell address</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.clearFormulaDependentCells("A1");
</script>{% endhighlight %}







### clearLibraryComputationException<span class="signature">()</span>
{:#methods:clearlibrarycomputationexception}








Call this method to clear whether an exception was raised during the computation of a library function.





Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.clearLibraryComputationException();
</script>{% endhighlight %}







### colIndex<span class="signature">(Cell)</span>
{:#methods:colindex}








Get the column index from a cell reference passed in.

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
Cell{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell address</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.colIndex("A1");
</script>{% endhighlight %}







### computedValue<span class="signature">(Formula)</span>
{:#methods:computedvalue}








Evaluates a parsed formula.

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
Formula{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the parsed formula</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

string


Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.computedValue("&rsquo;n10n2a&rsquo;");
</script>{% endhighlight %}







### computeFormula<span class="signature">(Formula)</span>
{:#methods:computeformula}








Evaluates a parsed formula.

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
Formula{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the parsed formula</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

string


Example
{:.example}


{% highlight html %}
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.computedValue("&rsquo;n10n2a&rsquo;");
</script>{% endhighlight %}




