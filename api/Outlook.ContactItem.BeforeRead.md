---
title: ContactItem.BeforeRead event (Outlook)
ms.prod: outlook
api_name:
- Outlook.ContactItem.BeforeRead
ms.assetid: cebd1e59-b3a4-3c9d-5ed1-ff95c2c3d1ed
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# ContactItem.BeforeRead event (Outlook)

Occurs before Microsoft Outlook begins to read the properties for the item.


## Syntax

_expression_. `BeforeRead`

_expression_ A variable that represents a [ContactItem](Outlook.ContactItem.md) object.


## Remarks

The **BeforeRead** event occurs before the **[Read](Outlook.ContactItem.Read.md)** event. Unlike other events with the Before prefix, this event is not cancelable. To determine when the item is unloaded from memory, use the **[Unload](Outlook.ContactItem.Unload.md)** event.

The **BeforeRead** event corresponds to the Exchange Client Extensions (ECE) event **IExchExtMessageEvents::OnRead**.

Only the following members of the item object can be accessed in the  **BeforeRead** event:


-  **[Class](Outlook.ContactItem.Class.md)**
    
-  **[MessageClass](Outlook.ContactItem.MessageClass.md)**
    
-  **MAPIOBJECT**
    
The **MAPIOBJECT** property is a hidden property in the Outlook object model. This property provides access to the underlying MAPI **[IMessage](https://msdn.microsoft.com/library/cc842097%28office.14%29.aspx)** object, and can be invoked only via the **[IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)** interface. The property is accessible to programs written in languages such as C or C++ that support **IUnknown**. **MAPIOBJECT** is not available through the **[IDispatch](https://msdn.microsoft.com/library/ms221608.aspx)** interface. Development languages such as Visual Basic for Applications (VBA), Visual C#, and Visual Basic support the **IDispatch** interface and not **IUnknown**, and therefore, they cannot access **MAPIOBJECT**. If other properties or methods of the parent item are accessed in this event, Outlook raises an error.

If the implementer accesses the underlying  **IMessage** object and changes properties on that object, Outlook will render that item reflecting the changes to the **IMessage** object. The implementer does not have to call **[SaveChanges](https://msdn.microsoft.com/library/cc842181%28office.14%29.aspx)** on the **IMessage** object to cause the changes to be reflected in Outlook.

Implementers must release the object obtained from the  **MAPIOBJECT** property in the event before the event completes. Attempting to use that object outside the context of the event is unsupported and will lead to unpredictable behavior.


## See also


[ContactItem Object](Outlook.ContactItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]