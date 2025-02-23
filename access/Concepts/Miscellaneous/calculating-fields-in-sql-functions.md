---
title: Calculating fields in SQL functions
ms.prod: access
ms.assetid: 441af335-469d-5d70-bd90-5309717cb941
ms.date: 10/12/2018
ms.localizationpriority: medium
---


# Calculating fields in SQL functions

**Applies to:** Access 2013 | Access 2016

You can use the string expression argument in an SQL aggregate function to perform a calculation on values in a field. For example, you could calculate a percentage (such as a surcharge or sales tax) by multiplying a field value by a fraction.

The following table provides examples of calculations on fields from the Orders and Order Details tables in the Northwind.mdb database.


|**Calculation**|**Example**|
|:-----|:-----|
|Add a number to a field| `Freight + 5`|
|Subtract a number from a field| `Freight - 5`|
|Multiply a field by a number| `UnitPrice * 2`|
|Divide a field by a number| `Freight / 2`|
|Add one field to another| `UnitsInStock + UnitsOnOrder`|
|Subtract one field from another| `ReorderLevel - UnitsInStock`|

The following example calculates the average discount amount of all orders in the Northwind.mdb database. It multiplies the values in the UnitPrice and Discount fields to determine the discount amount of each order and then calculates the average. You can use this expression in an SQL statement in Visual Basic code:

<br/>

```sql
SELECT Avg(UnitPrice * Discount) AS [Average Discount] FROM [Order Details];
```

## See also

- [Access for developers forum](https://social.msdn.microsoft.com/Forums/office/home?forum=accessdev)
- [Access help on support.office.com](https://support.office.com/search/results?query=Access)
- [Access help on answers.microsoft.com](https://answers.microsoft.com/)
- [Access forums on UtterAccess](https://www.utteraccess.com/forum/index.php?act=idx)
- [Access developer and VBA programming help center (FMS)](https://www.fmsinc.com/MicrosoftAccess/developer/)
- [Access posts on StackOverflow](https://stackoverflow.com/questions/tagged/ms-access)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]