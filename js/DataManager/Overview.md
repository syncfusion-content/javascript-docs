---
layout: post
title: Overview
description: overview 
platform: js
control: DataManager
documentation: ug
---

# Overview  

**DataManager** helps in managing relational data in **JavaScript**. Its rich features make querying data sources easier. **JavaScript** **OData** **Client** fully supports **oData** queries that are enabled in **Web API** & **WCF** data services.

**DataManager** supports different type of data binding, such as:

1. JSON

2. Web Services

3. OData

Basically, all services that have **JSON** acts as a transport.

##Key Features

Some important features of the **DataManager** for **JavaScript** are:

1. **DataManager** - Communicates with data source and returns the desired result based on the Query provided.

2. **JavaScript Query** – **DataManager** have APIs for generating JavaScript data query with ease.

3. **CRUD in individual requests and Batch** – **CRUD** operations are fully supported. The options are enabled to commit the data as a single or multiple requests.

4. **Adaptors** – **Adaptors** are specific dataSource type aware interfaces that are used by **DataManager** to communicate with DataSource. Three adaptors are created. They are, ODataAdaptor, JsonAdaptor and UrlAdaptor

5. **Model binding** – Simple model binding is made using **DataManager**. You can directly bind Query result to **HTML** element.

