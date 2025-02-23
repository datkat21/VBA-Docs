---
title: DistListItem.BeforeAttachmentWriteToTempFile event (Outlook)
ms.prod: outlook
api_name:
- Outlook.DistListItem.BeforeAttachmentWriteToTempFile
ms.assetid: 565c9c1d-cbab-1ac2-de79-3a15532c4f76
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# DistListItem.BeforeAttachmentWriteToTempFile event (Outlook)

Occurs before an attachment associated with an instance of the parent object is written to a temporary file.


## Syntax

_expression_. `BeforeAttachmentWriteToTempFile`( `_Attachment_` , `_Cancel_` )

_expression_ A variable that represents a [DistListItem](Outlook.DistListItem.md) object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Attachment_|Required| **[Attachment](Outlook.Attachment.md)**|The **Attachment** to be written.|
| _Cancel_|Required| **Boolean**|Set to  **True** to cancel the operation; otherwise, set to **False** to allow the **Attachment** to be written.|

## See also


[DistListItem Object](Outlook.DistListItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]