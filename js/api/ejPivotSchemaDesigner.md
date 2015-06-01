---
layout: post
title: ejPivotSchemaDesigner
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Pivot Schema Designer control.





#### $(element).ejPivotSchemaDesigner<span class="signature">()</span>






##### Example
<pre class="prettyprint"><code> &lt;div id="PivotSchemaDesigner"&gt; &lt;/div&gt; 
 &lt;script&gt;// Create Pivot Schema Designer$("#PivotSchemaDesigner").ejPivotSchemaDesigner(...);   &lt;/script&gt;</code></pre>



### Requires


* module:jQuery

* module:ej.common.all

* module:ej.tools.js


### Members




#### cssClass<span class="type-signature type string">String</span>




Sets the CSS name for custom operation.


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> //To set the CSS name during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({cssClass: "gradient-lime"});   </code></pre><pre class="prettyprint"><code> //Get or set css class for initialization:
        // Gets the css name.                   $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "cssClass");                          // Sets the css class to PivotSchemaDesigner        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "cssClass",  "gradient-lime" );               </code></pre>



#### filters<span class="type-signature type array">Array</span>




Allows the user to set the filter list.


Default Value:



* new Array()




##### Examples
<pre class="prettyprint"><code> //To set the filter list during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({filterList: true});</code></pre><pre class="prettyprint"><code> //Get or set the filter list, after initialization:
        //Gets the filter list        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "filterList");
                                    //Sets the filter list        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "filterList","true");                 *               </code></pre>



#### height<span class="type-signature type string">String</span>




Sets the height for PivotSchemaDesigner.


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> //To set the height during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({height: "630px"});     </code></pre><pre class="prettyprint"><code> //Get or set height for initialization:
        // Gets the height.                     $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "height");                            // Sets the height to PivotSchemaDesigner        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "height",  "630px" );                 </code></pre>



#### pivotCalculations<span class="type-signature type array">Array</span>




Allows the user to set Pivot Calculation List.


Default Value:



* new Array()




##### Examples
<pre class="prettyprint"><code> //To set the pivot calculation cist during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: });</code></pre><pre class="prettyprint"><code> //Get or set the pivot calculation list, after initialization:
        //Gets the cell context state        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
                           //Sets the pivot calculation list value        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true");                        *               </code></pre>



#### pivotColumns<span class="type-signature type array">Array</span>




Allows the user to set the pivot column list.


Default Value:



* new Array()




##### Examples
<pre class="prettyprint"><code> //To set the pivot column list during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: true});</code></pre><pre class="prettyprint"><code> //Get or set the pivot column list, after initialization:
        //Gets the pivot column list        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
                           //Sets the pivot column list value        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true");                        *               </code></pre>



#### pivotControl<span class="type-signature type object">object</span>




Sets the pivot control bounds with the Pivot Schema Designer.


Default Value:



* null




##### Examples
<pre class="prettyprint"><code> //To set the pivot control during initialization  var control = $("#PivotSchemaDesigner").data("ejPivotSchemaDesigner");$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotControl: control});</code></pre><pre class="prettyprint"><code> //Get or set the pivot control, after initialization:
        //Gets the pivot control value        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotControl");
                          //Sets the pivot control        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotControl", control);                     *               </code></pre>



#### pivotRows<span class="type-signature type array">Array</span>




Allows the user to set the pivot row list.


Default Value:



* new Array()




##### Examples
<pre class="prettyprint"><code> //To set the pivot row list during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotRowList: true});</code></pre><pre class="prettyprint"><code> //Get or set the pivot row list, after initialization:
        //Gets the pivot row list        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotRowList");
                  //Sets the pivot row list        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotRowList","true");                       *               </code></pre>



#### pivotTableFields<span class="type-signature type array">Array</span>




Allows the user to Pivot Table Field List to Pivot Schema Designer.


Default Value:



* new Array()




##### Examples
<pre class="prettyprint"><code> //To set the Pivot Table Field List during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: });</code></pre><pre class="prettyprint"><code> //Get or set the Pivot Table Field List, after initialization:
        //Gets the virtual calling state        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
                   //Sets the Pivot Table Field List         $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true");                        *               </code></pre>



#### url<span class="type-signature type string">String</span>




Connects the service using the specified URL for any server updates. See url


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> //To set service url during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({url: "/wcf/PivotService.svc"});</code></pre><pre class="prettyprint"><code> //Get or set the size API, after initialization:
//Gets the url value  $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option","url");
   //Sets the url value $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option","url", "/wcf/PivotService.svc" ); </code></pre>



#### width<span class="type-signature type string">String</span>




Sets the width for PivotSchemaDesigner.


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> //To set the width during initialization  $("#PivotSchemaDesigner").ejPivotSchemaDesigner({width: "415px"});      </code></pre><pre class="prettyprint"><code> //Get or set width for initialization:
        // Gets the width.                      $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "width");                             // Sets the width to PivotSchemaDesigner        $("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "width",  "415px" );          </code></pre>


### Methods




#### doAjaxPost<span class="signature">()</span>




Perform an asynchronous HTTP (Ajax) request.



##### Example
<pre class="prettyprint"><code> &lt;div id="PivotSchemaDesigner"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create PivotSchemaDesigner$('#PivotSchemaDesigner').ejPivotSchemaDesigner({      url: "PivotGridService.svc",  });var gridObj = $("#PivotSchemaDesigner").data("ejPivotSchemaDesigner");gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);// Initiate an Ajax request.&lt;/script&gt;</code></pre>


