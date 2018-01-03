---
title: Formula support with Spreadsheet widget for Syncfusion Essential JS
description: How to use formulas in Spreadsheet with cell references, named ranges etc.
platform: Js
control: Spreadsheet
documentation: Ug
api: /api/js/ejspreadsheet
---
# Formulas

Formulas are used for calculation of data in sheet. You can set formula for a `cell` in following ways,

1. Initial Load
2. Method
3. User Interface

### Initial Load

You can set formula for a cell by specifying [`value`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rows-cells-value "value") property in cell data binding. The following code example describes the above behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]  
                },
                {
                    cells: [{
                        value: 2
                    }]
                },
                {
                    cells: [{
                        value: "=SUM(A1,A2)"
                    }]
                }]
            }]
        });
    });
</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img1.png)

### Method

You can set formula for a cell using [`updateCellValue`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xledit-updatecellvalue "updateCellValue") method. The following code example describes the above behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                },
                {
                    cells: [{
                        value: 2
                    }]
                }]
            }],
            loadComplete: "loadComplete"
        });
    });

    function loadComplete() {
        this.XLEdit.updateCellValue({ rowIndex: 2, colIndex: 0 }, "=SUM(A1,A2)");
    }
</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img1.png)

### User Interface

You can set formula for a cell by edit and save a cell through user interface using `Editing` feature. The following code example and screenshot describes the above behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                },
                {
                    cells: [{
                        value: 2
                    }]
                }]
            }]
        });
    });
</script>

{% endhighlight %}

![](Formulas_images/Formula_img2.png)

The following output is displayed while saving edited cell with above code example.
![](Formulas_images/Formula_img1.png)

N> 1. The list of supported formulas can be find in following [`link`](https://help.syncfusion.com/js/calculate/supported-formulas/supported-formulas "link")
N> 2. Constant values, cell references, formulas and named ranges can be passed as argument to formulas
N> 3. Selection can be used to mention cell references within formula

## User Defined Functions

The list of formulas supported in Spreadsheet is sufficient for most of your calculations. If not, you can create and use your own function using user defined function option. You can add user defined function to Spreadsheet in following ways,

1. Initial Load

2. Method


### Initial Load

You can add your own function to Spreadsheet at initial load with [`customFormulas`](https://help.syncfusion.com/api/js/ejspreadsheet#members:customformulas "customFormulas") API. The following code example describes the above behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                    },
                    {
                    cells: [{
                        value: 2
                    }]
                    },                    
                    {
                    cells: [{
                        value: "=CUSTOMTOTAL(A1,A2,3)"
                    }]
                }]
            }],
            customFormulas: [{"formulaName":"CUSTOMTOTAL", "functionName":"customTotal"}]
        });
    });

    function customTotal(args) {
        var param1, param2, param3, value, excelObj = $('#Spreadsheet').data("ejSpreadsheet"),
        argument = excelObj.getValueFromFormulaArg(args);
        param1 = argument["arg1"];
        param2 = argument["arg2"];
        param3 = argument["arg3"];
        value = param1 * param2 + param3;
        return value;
    }

</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img5.png)

### Method

You can add your own function to Spreadsheet using [`addCustomFormula`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:addcustomformula "addCustomFormula") method. The following code example describes the above behavior,

You can also calculate formulas in the specified sheet by using[`calcNow`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xledit-calcnow "calcNow") method in Spreadsheet.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({                
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                    },
                    {
                    cells: [{
                        value: 2
                    }]
                }]                                       
            }],
            loadComplete: "loadComplete"
        });
    });

    function loadComplete() {
        this.addCustomFormula("CUSTOMTOTAL", "customTotal");
        this.XLEdit.updateCellValue({ rowIndex: 2, colIndex: 0 }, "=CUSTOMTOTAL(A1,A2,3)");
    }

    function customTotal(args) {
        var param1, param2, param3, value, excelObj = $('#Spreadsheet').data("ejSpreadsheet"),
        argument = excelObj.getValueFromFormulaArg(args);
        param1 = argument["arg1"];
        param2 = argument["arg2"];
        param3 = argument["arg3"];
        value = param1 * param2 + param3;
        return value;
    }
</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img5.png)

To remove user defined function from Spreadsheet use [`removeCustomFormula`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:removecustomformula "removeCustomFormula") method.

## Named Ranges

To understand the purpose of cell reference or table, you can define a meaningful name using named ranges support. By using names, you can make your formula much easier to understand and maintain. You can add named ranges to Spreadsheet in following ways,
    
1. Initial Load

2. Method

3. User Interface

### Initial Load

To add named ranges at initial load by using [`nameManager`](https://help.syncfusion.com/api/js/ejspreadsheet#members:namemanager "nameManager") API, and also you can specify the name and address of the range by using [`name`](https://help.syncfusion.com/api/js/ejspreadsheet#members:namemanager-name "name") and [`refersto`](https://help.syncfusion.com/api/js/ejspreadsheet#members:namemanager-refersto "refersto") API. The following code example describes the above behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({                               
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                    },
                    {
                    cells: [{
                        value: 2
                    }]
                    },
                    {
                    cells: [{
                        value: "=SUM(inputrange)"
                    }]
                }]                    
            }],
            nameManager: [{name: "inputrange", refersto: "=Sheet1!$A$1:$A$2"}]
        });
    });
</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img3.png)

### Method

You can add named range to Spreadsheet with [`addNamedRange`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addnamedrange "addNamedRange") method and it can be removed with [`removeNamedRange`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-removenamedrange "removeNamedRange") method. The following code example describes the [`addNamedRange`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addnamedrange "addNamedRange") behavior,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
    $(function () {
        $("#Spreadsheet").ejSpreadsheet({                                
            sheets: [{
                rows: [{
                    cells: [{
                        value: 1
                    }]
                    },
                    {
                    cells: [{
                        value: 2
                    }]
                }]
            }],
            loadComplete: "loadComplete"
        });
    });

    function loadComplete() {
        this.XLRibbon.addNamedRange("inputrange", "=Sheet1!$A$1:$A$2", "named range demo", this.getActiveSheetIndex());
        this.XLEdit.updateCellValue({rowIndex: 2, colIndex: 0}, "=SUM(inputrange)");            
    }
</script>

{% endhighlight %}

The following output is displayed as a result of the above code example.
![](Formulas_images/Formula_img3.png)

### User Interface

You can define name for range of cells through user interface using `Define Name` option in `OTHERS` tab. The following screenshot describes the above behavior,
![](Formulas_images/Formula_img4.png)

N> Defining name for cell reference or table will be accessible across all sheets.
N> Named Ranges will be displayed in Name Manger dialog box.

## Formula Bar

Formula bar is used to edit or enter cell data in much easier way. To enable formula bar set [`allowFormulaBar`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowformulabar "allowFormulaBar") as `true`.You have following formula bar options in Spreadsheet.

1) Hide Formula Bar

2) Show Formula Bar

3) Update Formula Bar

#### Hide Formula Bar
To hide the formula bar in Spreadsheet. Use  [`hideFormulaBar`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:hideformulabar "hideFormulaBar") method to hide formula bar via code.

#### Show Formula Bar
To show the formula bar in Spreadsheet. Use  [`showFormulaBar`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showformulabar "showFormulaBar") method to show formula bar via code.

#### Update Formula Bar
To Update the formula bar in Spreadsheet. Use  [`updateFormulaBar`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:updateformulabar "updateFormulaBar") method to Update formula bar via code.

## Auto Sum

To sum a row or column of numbers, select a cell next to the numbers you want to sum, click `AutoSum` on the `HOME` tab and press enter. To enable auto sum set [`allowAutoSum`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowautosum "allowAutoSum") API as `true`.
The auto sum options in ribbon is used to perform basic operations like sum, average, count, minimum, maximum etc.

You can also perform auto sum operations by using [`autoSum`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-autosum "autoSum")method.