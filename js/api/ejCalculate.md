---
layout: post
title: ejCalculate
documentation: ug
platform: js
metaname: 
metacontent: 
---

Custom engine to perfom calculation like excel sheet










#### $(element).ejCalculate<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;script&gt;
// Create calcEngine with grid data
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.core.js


* module:ej.calculate.js




### Methods








#### addCustomFunction<span class="signature">(FormulaName, FunctionName)</span>








Add the custom formuls with function in CalcEngine library

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
<td class="name"><code>FormulaName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the formula name</td>
</tr>
<tr>
<td class="name"><code>FunctionName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the custom function name to call</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### addNamedRange<span class="signature">(Name, cellRange)</span>








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
<td class="name"><code>Name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the namedRange's name</td>
</tr>
<tr>
<td class="name"><code>cellRange</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell range of NamedRange</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Grid"&gt;&lt;/div&gt; 
&lt;script&gt;
// Create Grid
$('#Grid').ejGrid({
    dataSource: window.gridData
});         
var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
var sheetID = calcObj.createSheetFamilyID();
calcObj.registerGridAsSheet("sheet1", $("#Grid").data("ejGrid"), sheetID);
calcObj.addNamedRange("FIRSTCELL","A1");
&lt;/script&gt;</code>
</pre>






#### adjustRangeArg<span class="signature">(Name)</span>








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
<td class="name"><code>Name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell range to adjust its range</td>
</tr>
</tbody>
</table>




##### Returns:

range


##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
var sheetID = calcObj.createSheetFamilyID();
calcObj.registerGridAsSheet("sheet1", $("#Grid").data("ejGrid"), sheetID);
calcObj.addNamedRange("FIRSTCELL","A1");
&lt;/script&gt;</code>
</pre>






#### clearFormulaDependentCells<span class="signature">(Cell)</span>








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
<td class="name"><code>Cell</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the changed cell address</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.clearFormulaDependentCells("A1");
&lt;/script&gt;</code>
</pre>






#### clearLibraryComputationException<span class="signature">()</span>








Call this method to clear whether an exception was raised during the computation of a library function.





##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.clearLibraryComputationException();
&lt;/script&gt;</code>
</pre>






#### colIndex<span class="signature">(Cell)</span>








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
<td class="name"><code>Cell</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the cell address</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.colIndex("A1");
&lt;/script&gt;</code>
</pre>






#### computedValue<span class="signature">(Formula)</span>








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
<td class="name"><code>Formula</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the parsed formula</td>
</tr>
</tbody>
</table>




##### Returns:

value of formula


##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.computedValue("&rsquo;n10n2a&rsquo;");
&lt;/script&gt;</code>
</pre>






#### computeFormula<span class="signature">(Formula)</span>








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
<td class="name"><code>Formula</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">pass the parsed formula</td>
</tr>
</tbody>
</table>




##### Returns:

value of formula


##### Example

<pre class="prettyprint">
<code>var calcObj = new CalcEngine($("#Grid").data("ejGrid"));
calcObj.computedValue("&rsquo;n10n2a&rsquo;");
&lt;/script&gt;</code>
</pre>



