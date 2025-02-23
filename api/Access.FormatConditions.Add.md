---
title: FormatConditions.Add method (Access)
keywords: vbaac10.chm10071
f1_keywords:
- vbaac10.chm10071
ms.prod: access
api_name:
- Access.FormatConditions.Add
ms.assetid: 6066d3ee-7e47-b090-ea64-ccf95e4ecc89
ms.date: 03/20/2019
ms.localizationpriority: medium
---


# FormatConditions.Add method (Access)

You can use the **Add** method to add a conditional format as a **[FormatCondition](Access.FormatCondition.md)** object to the **FormatConditions** collection of a combo box or text box control.


## Syntax

_expression_.**Add** (_Type_, _Operator_, _Expression1_, _Expression2_)

_expression_ A variable that represents a **[FormatConditions](Access.FormatConditions.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Type_|Required|**[AcFormatConditionType](Access.AcFormatConditionType.md)**|An **AcFormatConditionType** constant that specifies the type of format condition to be added.|
| _Operator_|Optional|**[AcFormatConditionOperator](Access.AcFormatConditionOperator.md)**|An **AcFormatConditionOperator** constant that specifies the operator. If the _Type_ argument is **acExpression**, the _Operator_ argument is ignored. If you leave this argument blank, the default constant (**acBetween**) is assumed.|
| _Expression1_|Optional|**Variant**|A value or expression associated with the first part of the conditional format. Can be a constant or a string value.|
| _Expression2_|Optional|**Variant**|A value or expression associated with the second part of the conditional format when the  _Operator_ argument is **acBetween** or **acNotBetween** (otherwise, this argument is ignored). Can be a constant or a string value.|

## Return value

FormatCondition


## Remarks

You can use the **Delete** method of the **FormatConditions** collection to delete an existing **FormatConditions** collection from a combo box or text box control.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]