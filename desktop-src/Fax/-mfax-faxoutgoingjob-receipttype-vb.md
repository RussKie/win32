﻿---
Description: 'The ReceiptType property is a value that specifies the type of delivery receipt to deliver when the fax message reaches a final state. The receipt type can be Simple Mail Transport Protocol (SMTP) mail, a message box, or no receipt.'
ms.assetid: '7b88efe4-d5cb-4b5e-a7e7-f13da53f144a'
title: 'FaxOutgoingJob.ReceiptType property'
---

# FaxOutgoingJob.ReceiptType property

The **ReceiptType** property is a value that specifies the type of delivery receipt to deliver when the fax message reaches a final state. The receipt type can be Simple Mail Transport Protocol (SMTP) mail, a message box, or no receipt.

This property is read-only.

## Syntax


```VB
Property ReceiptType As Integer
```



## Property value

A value from the [**FAX\_RECEIPT\_TYPE\_ENUM**](-mfax-fax-receipt-type-enum.md) enumeration that specifies a receipt type.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>FaxComex.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Fxscomex.dll</dt> </dl> |



## See also

<dl> <dt>

[Visual Basic Example](-mfax-managing-outgoing-jobs.md)
</dt> <dt>

[**FaxOutgoingJob**](-mfax-faxoutgoingjob.md)
</dt> <dt>

[**IFaxOutgoingJob**](-mfax-faxoutgoingjob-cpp.md)
</dt> </dl>

 

 



