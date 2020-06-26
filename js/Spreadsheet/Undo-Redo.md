---
layout: post
title: Undo and Redo in JavaScript Spreadsheet widget | Syncfusion
description: You can learn here about undo and redo support in Syncfusion JavaScript Spreadsheet control and more details.
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
--- 

# Undo and Redo in JavaScript Spreadsheet

Spreadsheet provides the support to perform undo and redo operations. You can set [`allowUndoRedo`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowundoredo "allowUndoRedo") as true to enable undo redo feature. You can also use [`undoRedoStep`](https://help.syncfusion.com/api/js/ejspreadsheet#members:undoredostep "undoRedoStep") property to limit the undo redo action.

The following options are available in Spreadsheet undo redo.

* To perform undo action use [`undo`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:undo "undo") method.
* To perform redo action use [`redo`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:redo "redo") method.
* To update the undo redo collections use [`updateUndoRedoCollection`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:updateundoredocollection "updateUndoRedoCollection") method.
* To clear the undo redo collections use [`clearUndoRedo`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:clearundoredo "clearUndoRedo") method.


N> Default value of [`undoRedoStep`](https://help.syncfusion.com/api/js/ejspreadsheet#members:undoredostep "undoRedoStep") is 20. You can perform 20 undo or redo actions.


## Undo the last action

Undo reverses the last action you performed with Spreadsheet. You can do this by following ways.

* Use Undo button of HOME tab in ribbon.
* Use "Ctrl + Z" key.

## Redo the action

Redo reverses the last undo action you performed with Spreadsheet. You can do this by following ways.

* Use Redo button of HOME tab in ribbon.
* Use "Ctrl + Y" key.

