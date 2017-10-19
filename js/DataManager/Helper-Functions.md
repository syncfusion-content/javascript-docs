---
layout: post
title: Helper-Functions
description: helper functions
platform: js
control: DataManager
documentation: ug
api: /api/js/ejdatamanager
---

# Helper Functions

**ej.parseJSON**

This method is used to parse the string to **JSON**. 

**ej.parseTable**

This method is used to parse the **HTML** element into the **JSON** Array and is used commonly in element binding using **DataManager**.

**ej.getGuid**

This method returns the globally unique identifier and it generates unique identifier with the prefix provided as parameter.

**ej.merge**

The ej.merge is used to merge two arrays and the result is merged in the first array. 

**ej.support**

The ej.support property contains a collection of properties representing different browser features or bugs. The property are as follows.

1. cors – represents the cross browser support.

2. enableLocalizedSort – enables the localized sort operation.

3. stableSort – enables stable sort operation.

4. outerHTML – represents the outerHTML support.

**ej.swap**

This method is used to swap the position of element in an array. It accepts three arguments such as input array and two swap positions.

**ej.serverTimezoneOffset**

This property is used to set the time-zone offset from UTC, in hours.