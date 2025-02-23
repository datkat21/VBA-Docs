---
title: Report.Parent property (Access)
keywords: vbaac10.chm13779
f1_keywords:
- vbaac10.chm13779
ms.prod: access
api_name:
- Access.Report.Parent
ms.assetid: 8ad25142-21e4-f0ae-d1c6-621dee5edc69
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# Report.Parent property (Access)

Returns the parent object for the specified object. Read-only.


## Syntax

_expression_.**Parent**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

You can use the **Parent** property to determine which form or report is currently the parent when you have a subform or subreport that has been inserted in multiple forms or reports.

For example, you might insert an **OrderDetails** subform into both a form and a report. The following example uses the **Parent** property to refer to the **OrderID** field, which is present on the main form and report. You can enter this expression in a bound control on the subform.

```vb
=Parent!OrderID
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]