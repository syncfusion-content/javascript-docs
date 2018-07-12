---
layout: post
title: Joining Tables with Syncfusion Web Report Designer
description: How to join table with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Joining Tables

The joining of tables is required when more than one table is used in data design. 

You can use join icon in the tools pane to invoke join operation for joining more than one tables. The join icon will be in disabled state, if there is only one table found dropped in table design view like below:

![](Joiner-Images/Query-JoinerDisable.png)

The join icon will get enabled once the second table found dropped in table design like below:

![](Joiner-Images/Joiner-Enable.png)

## Adding a join condition

If the subsequent table being dropped, has any of its column as foreign key in any of the already dropped tables, the joining will take place automatically. Else, it will prompt the join editor like below to let you define the keys (columns) to join between this table and any one of the already dropped tables.

![](Joiner-Images/Query-JoinerPrompt.png)

* **LeftTable** - The `LeftTable` illustrates the list of table dropped already.

* **RightTable** - The `RightTable` illustrates the table which you have dropped recently and that requires to set up a relation with any of the previously dropped tables. 

The fields of the specific table will be listed in the drop-down list below to that.

![](Joiner-Images/Fields-List.png)

You can add multiple join condition for single table relation by clicking `Add Field` button.

![](Joiner-Images/Multiple-Relation.png)

### Join Types

The join type compares operator and relational operator to make relationship between the two tables.

**Types** of joins - Inner Join, Left Outer, Right Outer and Full Outer.

![](Joiner-Images/Join-Type.png)

**Inner Join**

`INNER JOIN` will return the records from two or more tables, while records are matching in both the tables. 

An inner join of Table1 and Table2 gives the result of Table1 intersect Table2.

For example, consider the below two tables.

Table1

| `Supplier_Id` | `Supplier_Name` |
|---------------|-----------------|
| 100           | James           |
| 101           | John            |
| 102           | Robert          |
| 103           | Michael         |

Table2

| `Order_Id` | `Supplier_Id` | `Order_Date` |
|------------|---------------|--------------|
| 20125      | 100           | 09/21/2017   |
| 20126      | 101           | 09/22/2017   |
| 20127      | 104           | 09/23/2017   |

If we join (INNER JOIN) Table1 and Table2 based on Supplier_Id column and equals (=) as comparison operator, then the result will be like below.  

| `Supplier_Id` | `Supplier_Name` | `Order_Id` | `Supplier_Id(Table2)` | `Order_Date` |
|---------------|-----------------|------------|-----------------------|--------------|
| 100           | James           | 20125      | 100                   | 09/21/2017   |
| 101           | John            | 20126      | 101                   | 09/22/2017   |

**Left outer join**

`LEFT OUTER JOIN` will return all record from the left table and the matched records from the right table. The result is NULL from the right table, if there is no match.

For example, consider the below two tables.

Table1

| `Supplier_Id` | `Supplier_Name` |
|---------------|-----------------|
| 100           | James           |
| 101           | John            |
| 102           | Robert          |
| 103           | Michael         |

Table2

| `Order_Id` | `Supplier_Id` | `Order_Date` |
|------------|---------------|--------------|
| 20125      | 100           | 09/21/2017   |
| 20126      | 101           | 09/22/2017   |
| 20127      | 104           | 09/23/2017   |

If we join (LEFT OUTER JOIN) Table1 and Table2 based on Supplier_Id column and equals (=) as comparison operator, then the result will be like below. 

| `Supplier_Id` | `Supplier_Name`  | `Order_Id` | `Supplier_Id(Table2)` | `Order_Date` |
|---------------|------------------|------------|-----------------------|--------------|
| 100           | James            | 20125      | 100                   | 09/21/2017   |
| 101           | John             | 20126      | 101                   | 09/22/2017   |
| 102           | Robert           |            |                       |              |
| 103           | Michael          |            |                       |              |

**Right outer join**

Right outer join preserves the unmatched rows from the second (right) table, joining them with a NULL in the shape of the first (left) table.

For example, consider the below two tables.

Table1

|   OrderID    |   CustomerID   |   EmployeeID  |   OrderDate   |   ShipperID   |
|--------------|----------------|---------------|---------------|---------------|
|   10308      |   2            |   7           |   1996-09-18  |   3           |
|   10309      |   37           |   3           |   1996-09-19  |   1           |
|   10310      |   77           |   8           |   1996-09-20  |   2           |


Table2

| `EmployeeID`  |	`LastName`  |	`FirstName` |	`BirthDate` |	`Photo`     |
|---------------|---------------|---------------|---------------|---------------|
|   1           |   Davolio     |	Nancy       |	12/8/1968   |	EmpID1.png  |
|   2	        |   Fuller  	|   Andrew	    |   2/19/1952   |	EmpID2.png  |
|   3	        |   Leverling   |	Janet       |	8/30/1963   |	EmpID3.png  |

If we join (RIGHT OUTER) Table1 and Table2 based on EmployeeID column and equals (=) as comparison operator, then the result will be like below.

| `EmployeeID`  |	`LastName`  |	`FirstName` |	`OrderID`   |	`EmployeeID`|   OrderDate   |   ShipperID   |
|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
|   1           |   Davolio     |	Nancy       |	12/8/1968   |	            |               |               |
|   2	        |   Fuller  	|   Andrew	    |   2/19/1952   |	            |               |               |
|   3	        |   Leverling   |	Janet       |	8/30/1963   |	3           |   1996-09-19  |   2           |

**Full outer join**

The FULL OUTER JOIN keyword return all records when there is a match in either left (table1) or right (table2) table records.

For example, consider the below two tables.

Table1

|   CustomerID	|   Name    |	ContactName     |	  City      |	PostalCode  |	Country |
|---------------|-----------|-------------------|---------------|---------------|-----------|
|   1           |   Alfreds | 	Maria 	        |    Berlin	    |   12209	    |   Germany |
|   2           |   Ana     |  	Ana Trujillo    |	México D.F. | 	05021       |   Mexico  |
|   3           |   Antonio |  Antonio Moreno   |	México D.F.	|   05023	    |   Mexico  |

Table2

|   OrderID    |   CustomerID   |   EmployeeID  |   OrderDate   |   ShipperID   |
|--------------|----------------|---------------|---------------|---------------|
|   10308      |   2            |   7           |   1996-09-18  |   3           |
|   10309      |   37           |   3           |   1996-09-19  |   1           |
|   10310      |   77           |   8           |   1996-09-20  |   2           |

The FULL OUTER JOIN keyword returns all the rows from the left table (table1), and all the rows from the right table (table2).


|   CustomerID	|   Name    |	ContactName     |	  City      |	PostalCode  |	Country |   OrderID |
|---------------|-----------|-------------------|---------------|---------------|-----------|-----------|
|   1           |   Alfreds | 	Maria 	        |    Berlin	    |   12209	    |   Germany |           |
|   2           |   Ana     |  	Ana Trujillo    |	México D.F. | 	05021       |   Mexico  |	10308   |
|   3           |   Antonio |  Antonio Moreno   |	México D.F.	|   05023	    |   Mexico  |   10365   |
|               |           |                   |               |               |           |   10382   |
|               |           |                   |               |               |           |   10351   |

### Join Condition

To compare the values of the two columns (one from each table) between tables, any of the operator list shown in the below image can be used.

![](Joiner-Images/Operator-List.png)

![](Joiner-Images/Join-Tables.png)

### Edit a join condition

* Update an existing join condition by clicking the `Edit` icon in the respective field.

  ![](Joiner-Images/Edit-Join.png)

* Clicking on the icon will enable the respective join fields.

* Click `Ok` button to save the join relationship.

### Removing a join condition

Remove a join condition by clicking the close icon placed at left of the respective join condition.

![](Joiner-Images/delete-Join.png)