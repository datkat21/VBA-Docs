---
title: CustomControl.Application property (Access)
keywords: vbaac10.chm11995
f1_keywords:
- vbaac10.chm11995
ms.prod: access
api_name:
- Access.CustomControl.Application
ms.assetid: 54b56ba5-f624-acc4-cab3-1e007a09a890
ms.date: 03/06/2019
ms.localizationpriority: medium
---


# CustomControl.Application property (Access)

You can use the **Application** property to access the active Microsoft Access **[Application](Access.Application.md)** object and its related properties. Read-only **Application** object.


## Syntax

_expression_.**Application**

_expression_ A variable that represents a **[CustomControl](Access.CustomControl.md)** object.


## Remarks

The **Application** property is set by Microsoft Access and is read-only in all views.

Each Microsoft Access object has an **Application** property that returns the current **Application** object. You can use this property to access any of the object's properties. For example, you could refer to the menu bar for the **Application** object from the current form by using the following syntax.

```vb
Me.Application.MenuBar 

```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]