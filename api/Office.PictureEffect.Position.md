---
title: PictureEffect.Position property (Office)
ms.prod: office
api_name:
- Office.PictureEffect.Position
ms.assetid: 29c2d136-777f-5984-3018-3dae2721ed76
ms.date: 01/23/2019
ms.localizationpriority: medium
---


# PictureEffect.Position property (Office)

Specifies the position of a picture effect in a chain of composite effects. Read/write.


## Syntax

_expression_.**Position**

_expression_ An expression that returns a **[PictureEffect](Office.PictureEffect.md)** object.


## Remarks

Picture effects are processed as a chain composed of individual items that are applied in sequence to create the final composited image. An effects chain will allow an effect to be added to the chain, reordered, or removed from the chain.


## Example

The following code sets several **PictureEffect** fill properties on a shape in a Microsoft PowerPoint slide.


```vb
Sub PictureEffectSample() 
' Setup a slide with one picture shape. 
With ActivePresentation.Slides(1).Shapes(1).Fill.PictureEffects 
 
 ' Insert a 150% Saturation effect. 
 .Insert(msoEffectSaturation).EffectParameters(1).Value = 1.5 
 
 ' Insert Brightness/Contrast effect and set values to -50% Brightness and +25% Contrast. 
 Dim brightnessContrast As PictureEffect 
 Set brightnessContrast = .Insert(msoEffectBrightnessContrast) 
 brightnessContrast.EffectParameters(1).Value = -0.5 
 brightnessContrast.EffectParameters(2).Value = 0.25 
 
 ' Remove all Picture effects. 
 While .Count > 0 
 .Delete (1) 
 Wend 
 
End With 
End Sub
```


## See also

- [PictureEffect object members](overview/Library-Reference/pictureeffect-members-office.md)



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
