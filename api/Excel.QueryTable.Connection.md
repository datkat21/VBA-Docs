---
title: QueryTable.Connection property (Excel)
keywords: vbaxl10.chm518087
f1_keywords:
- vbaxl10.chm518087
ms.prod: excel
api_name:
- Excel.QueryTable.Connection
ms.assetid: a576c5d2-113c-cbd0-1ad2-aa46591944de
ms.date: 05/03/2019
ms.localizationpriority: medium
---


# QueryTable.Connection property (Excel)

Returns or sets a string that contains one of the following: 

- OLE DB settings that enable Microsoft Excel to connect to an OLE DB data source
- ODBC settings that enable Excel to connect to an ODBC data source
- A URL that enables Excel to connect to a web data source
- The path to and file name of a text file
- The path to and file name of a file that specifies a database or web query 

Read/write **Variant**.

## Syntax

_expression_.**Connection**

_expression_ An expression that returns a **[QueryTable](Excel.QueryTable.md)** object.


## Remarks

Setting the **Connection** property doesn't immediately initiate the connection to the data source. You must use the **[Refresh](Excel.QueryTable.Refresh.md)** method to make the connection and retrieve the data.

For more information about the connection string syntax, see the **[Add](Excel.QueryTables.Add.md)** method of the **QueryTables** collection.

Alternatively, you may choose to access a data source directly by using the Microsoft ActiveX Data Objects (ADO) library instead.

If you import data by using the user interface, data from a web query or a text query is imported as a **QueryTable** object, while all other external data is imported as a **[ListObject](Excel.ListObject.md)** object.

If you import data by using the object model, data from a web query or a text query must be imported as a **QueryTable**, while all other external data can be imported as either a **ListObject** or a **QueryTable**.

You can use the **[QueryTable](Excel.ListObject.QueryTable.md)** property of the **ListObject** to access the **Connection** property.


## Example

This example supplies new ODBC connection information for the first query table on the first worksheet.

```vb
Worksheets(1).QueryTables(1) _ 
 .Connection:="ODBC;DSN=96SalesData;UID=Rep21;PWD=NUyHwYQI;"
```

<br/>

This example specifies a text file.

```vb
Worksheets(1).QueryTables(1) _ 
 Connection := "TEXT;C:\My Documents\19980331.txt"
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
