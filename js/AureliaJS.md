---
layout: post
title: Getting Started with Aurelia Syncfusion Bridge
description: How to use Essential js Aurelia.
platform: js
control: Introduction
documentation: ug
---

# Aurelia Syncfusion Bridge

Aurelia-Syncfusion-Bridge includes wrappers for Syncfusion-JavaScript widget’s, which act as the interface for both [Aurelia](http://aurelia.io/) frameworks and Syncfusion JavaScript widgets. This bridge is a structured, configurable collection of JavaScript classes which wrap Syncfusion JavaScript controls, presenting them in the form of Aurelia components.

The Syncfusion Aurelia components are named with prefix `ej` to avoid conflicting with other library component and offers the following features.

* Properties
* Two-way binding
* Event binding
* Templates
 
N> Those who are wish to directly getting started with Syncfusion Aurelia components navigate to [here](#getting-started).

## Properties

All the properties of Syncfusion JavaScript widget are defined as attributes for particular Aurelia component, so you can easily set value to widget properties, simply by prefixing property name with `e-` in component markup.

The `allowPaging` property of `ejGrid` widget can be defined as like the below code example.

{% highlight html %}

<ej-grid e-data-source.bind="gridData" e-allow-paging="true"></ej-grid>

{% endhighlight %}

N> The `gridData` will be loaded from Aurelia view-model.

## Two-way binding

Two-way binding observes the property in model and updates the UI automatically. The Syncfusion Aurelia component supports two-way binding for all the interactive properties. For ex., `value` property in input components, `dataSource` in Grids etc.

The `dataSource` property of `ejGrid` widget can be defined as two-way bindable property like the below code example.

{% highlight html %}

<ej-grid e-data-source.two-way="gridData" e-allow-paging="true"></ej-grid>

{% endhighlight %}

The below table depicts the properties of all the Syncfusion widgets that supports two-way data binding.

| **Control** | **Supported properties** |
| --- | --- |
| ejAccordion | - |
| ejAutoComplete | value <br/> selectedValueByKey |
| ejBarcode | - |
| ejBulletGraph | - |
| ejButton | - |
| ejChart | xZoomFactor <br/> yZoomFactor <br/> xZoomPosition <br/> yZoomPosition |
| ejCheckBox | Checked |
| ejCircularGauge | value <br/> minimum <br/> maximum |
| ejColorPicker | value <br/> opacityValue |
| ejDatePicker | value |
| ejDateTimePicker | value |
| ejDiagram | - |
| ejDialog | - |
| ejDigitalGauge | value |
| ejDropDownList | value |
| ejFileExplorer | - |
| ejGantt | dataSource <br/> selectedRowIndex |
| ejGrid | dataSource |
| ejGroupButton |   |
| ejKanban | dataSource |
| ejLinearGauge | value <br/> minimum <br/> maximum |
| ejListBox | value |
| ejListView | dataSource <br/> selectedItemIndex |
| ejMap | baseMapIndex <br/> enablePan <br/> enableResize <br/> enableAnimation |
| ejMaskEdit | value |
| ejMenu | - |
| ejNavigationDrawer | - |
| ejPdfViewer | - |
| ejPivotChart | - |
| ejPivotGauge | - |
| ejPivotGrid | - |
| ejPivotSchemaDesigner | - |
| ejProgressBar | - |
| ejRadialMenu | - |
| ejRadialSlider | - |
| ejRadioButton | - |
| ejRangeNavigator | - |
| ejRating | value |
| ejReportViewer | - |
| ejRibbon | - |
| ejRotator | - |
| ejRTE | value |
| ejSchedule | currentView <br/> currentDate |
| ejScroller | scrollLeft <br/> scrollTop |
| ejSlider | value |
| ejSparkline | - |
| ejSplitButton | - |
| ejSplitter | - |
| ejSpreadsheet | - |
| ejSymbolPalette | - |
| ejTab | selectedItemIndex |
| ejTagCloud | - |
| ejTile | - |
| ejTimePicker | value |
| ejToggleButton | - |
| ejToolbar | - |
| ejTooltip | - |
| ejTreeGrid | dataSource <br/> selectedRowIndex |
| ejTreeMap | dataSource <br/> weightValuePath |
| ejTreeView | - |
| ejUploadbox | -  |

## Event binding

Events can be bound to the components using the concern event name attribute with prefix `e-on-`.

The `recordClick` event of `ejGrid` widget can be bound to Aurelia component as like below code example.

{% highlight html %}

<ej-grid e-data-source.two-way="gridData" e-allow-paging="true" 
        e-on-record-click.delegate="recordClick($event.detail)">
</ej-grid>

{% endhighlight %}

## Templates

Aurelia framework’s template engine and syntaxes can be used within all template supported Syncfusion Aurelia components.

The `ejGrid` widget’s column template can be rendered as like the below code example.

{% highlight html %}

<ej-grid e-data-source.two-way="gridData" e-allow-paging=true 
        e-on-record-click.delegate="recordClick($event.detail)">
   <ej-column e-field="EmployeeImage" e-header-text="Employee Image"
     <ej-template>
         <div><img src="images/grid/Employees/${EmployeeID}.png" /> </div>
     </ej-template>
   </ej-column>
   <ej-column e-field="EmployeeID" e-header-text="Employee ID"></ej-column>
   <ej-column e-field="FirstName" e-header-text="First Name"></ej-column>
   <ej-column e-field="LastName" e-header-text="Last Name"></ej-column>
</ej-grid>

{% endhighlight %}

## Getting started

We are going to club all the above code examples in this section to render `ejGrid` widget. For quick start, we already configured a template project in GitHub repository [syncfusion-template-repository](https://github.com/aurelia-ui-toolkits/syncfusion-template-repository). Run the below set of commands to clone the repository and install the required packages for Syncfusion Aurelia application.

{% highlight html %}

> git clone "https://github.com/aurelia-ui-toolkits/syncfusion-template-repository"
> cd syncfusion-template-repository
> npm install
> jspm install

{% endhighlight %}

The below steps describes to create Syncfusion Aurelia Grid component.

* Create `grid` folder inside `src/samples/` location.
* Create `grid.html` file inside `src/samples/grid` folder and use the below code example to render the Grid component.

{% highlight html %}

<template>
  <div>
    <ej-grid e-data-source.two-way="gridData" e-allow-paging=true e-allow-sorting=true 
            e-on-record-click.delegate="recordClick($event.detail)">
      <ej-column e-field="OrderID" e-header-text="Order ID" e-text-align="right"></ej-column>
      <ej-column e-field="CustomerID" e-header-text="Customer ID"></ej-column>
     <ej-column e-field="EmployeeID" e-header-text="Employee ID" e-text-align="right"></ej-column>
     <ej-column e-field="Freight" e-header-text="Freight" e-format="{0:C}" e-text-align="right"></ej-column>
     <ej-column e-field="OrderDate" e-header-text="Order Date" e-format="{0:MM/dd/yyyy}" e-text-align="right"></ej-column>
   </ej-grid>
  </div>
</template>

{% endhighlight %}

* Create `grid.js` file with the below code snippet inside `src/samples/grid` folder.

{% highlight javascript %}

export class Grid {
  constructor() {
    this.gridData = [{
      OrderID: 10248, CustomerID: 'VINET', EmployeeID: 5, 
      OrderDate: new Date(8364186e5), Freight: 32.38
    },
    {
      OrderID: 10249, CustomerID: 'TOMSP', EmployeeID: 6, 
      OrderDate: new Date(836505e6), Freight: 11.61
    },
    {
      OrderID: 10250, CustomerID: 'HANAR', EmployeeID: 4, 
      OrderDate: new Date(8367642e5), Freight: 65.83
    },
    {
      OrderID: 10251, CustomerID: 'VICTE', EmployeeID: 3, 
      OrderDate: new Date(8367642e5), Freight: 41.34
    },
    {
      OrderID: 10252, CustomerID: 'SUPRD', EmployeeID: 4, 
      OrderDate: new Date(8368506e5), Freight: 51.3
    }];
  }

  recordClick(e) {
     //handle event here
  }
}

{% endhighlight %}

* Now, we are going to configure the navigation for created Grid sample in `src/app.js` file.

{% highlight javascript %}

export class App {
 configureRouter(config, router) {
  config.title = 'Aurelia Syncfusion';
  config.map([
   { route: ['', 'welcome'], name: 'welcome', moduleId: 'welcome',                              
                nav: true, title: 'Welcome' },
   { route: 'child-router',  name: 'child-router', moduleId: 'child-router',                         
                nav: true, title: 'Child Router' },
   { route: 'button',        name: 'button', moduleId: 'samples/button/button',                
                nav: true, title: 'Button' },
   { route: 'grid',        name: 'grid',       moduleId: 'samples/grid/grid',                
                nav: true, title: 'Grid' }
 ]);
 this.router = router;
 }
}

{% endhighlight %}

* To run the application, execute the following command.

{% highlight javascript %}

gulp watch

{% endhighlight %}

* Browse to [`http://localhost:9000`](http://localhost:9000)  to see the application. You can make changes in the code found under `src` folder and the browser should auto-refresh itself while you save files. The Grid component is rendered as like the below screenshot.

![](/js/Aurelia_images/skeleton_navigation.png)

# Catalog application

We have developed Catalog application for Aurelia-Syncfusion-Bridge [demo](http://aurelia-ui-toolkits.github.io/demo-syncfusion/) which is fully built on Aurelia framework.