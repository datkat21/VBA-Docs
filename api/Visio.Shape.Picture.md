---
title: Shape.Picture property (Visio)
keywords: vis_sdr.chm11250765
f1_keywords:
- vis_sdr.chm11250765
ms.prod: visio
api_name:
- Visio.Shape.Picture
ms.assetid: 0ccd2df9-fd84-dee0-0d89-5b7115e418d6
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Shape.Picture property (Visio)

Returns a picture that represents an enhanced metafile (EMF) contained in a master, shape, selection, or page. Read-only.


## Syntax

_expression_. `Picture`

_expression_ A variable that represents a **[Shape](Visio.Shape.md)** object.


## Return value

IPictureDisp


## Remarks

The  **Picture** property returns only EMF files.

COM provides a standard implementation of a picture object that has the  **IPictureDisp** interface on top of the underlying system picture support. The **IPictureDisp** interface exposes a picture object's properties and is implemented in the **stdole** type library as a **StdPicture** object creatable within Microsoft Visual Basic. The **stdole** type library is automatically referenced from all Visual Basic for Applications (VBA) projects in Microsoft Visio.

Currently, only in-process solutions can use the  **Picture** property because the **IPictureDisp** interface cannot be marshaled.


### To get information about the StdPicture object that supports the IPictureDisp interface




1. In the  **Code** group on the [Developer](../visio/How-to/run-visio-in-developer-mode.md) tab, click **Visual Basic**.
    
2. On the  **View** menu, click **Object Browser**.
    
3. In the  **Project/Library** list, click **stdole**.
    
4. Under  **Classes**, examine the class named  **StdPicture**.
    
For details about the  **IPictureDisp** interface, see the Microsoft Platform SDK on MSDN, the Microsoft Developer Network.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]