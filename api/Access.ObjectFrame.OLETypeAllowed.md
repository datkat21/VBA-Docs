---
title: ObjectFrame.OLETypeAllowed property (Access)
keywords: vbaac10.chm11572
f1_keywords:
- vbaac10.chm11572
ms.prod: access
api_name:
- Access.ObjectFrame.OLETypeAllowed
ms.assetid: ca669834-9bce-057c-dfb7-c8411b26bdd1
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# ObjectFrame.OLETypeAllowed property (Access)

You can use the **OLETypeAllowed** property to specify the type of OLE object that a control can contain. Read/write **Byte**.


## Syntax

_expression_.**OLETypeAllowed** 

_expression_ A variable that represents an **[ObjectFrame](Access.ObjectFrame.md)** object.


## Remarks

The **OLETypeAllowed** property uses the following settings.

|Setting|Constant|Description|
|:-----|:-----|:-----|
|Linked|**acOLELinked**|The control can contain only a linked object.|
|Embedded|**acOLEEmbedded**|The control can contain only an embedded object.|
|Either|**acOLEEither**|(Default) The control can contain either a linked or an embedded object.|

> [!NOTE] 
> For unbound object frames and charts, you can't change the **OLETypeAllowed** setting after an object is created. For bound object frames, you can change the setting after the object is created. Changing the **OLETypeAllowed** property setting only affects new objects that you add to the control.

To determine the type of OLE object a control already contains, you can use the **OLEType** property.


## Example

The following example creates a linked OLE object by using an unbound object frame named **OLE1**, and sizes the control to display the object's entire contents when the user chooses a command button.

```vb
Sub Command1_Click 
 OLE1.Class = "Excel.Sheet" ' Set class name. 
 ' Specify type of object. 
 OLE1.OLETypeAllowed = acOLELinked 
 ' Specify source file. 
 OLE1.SourceDoc = "C:\Excel\Oletext.xls" 
 ' Specify data to create link to. 
 OLE1.SourceItem = "R1C1:R5C5" 
 ' Create linked object. 
 OLE1.Action = acOLECreateLink 
 ' Adjust control size. 
 OLE1.SizeMode = acOLESizeZoom 
End Sub
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]