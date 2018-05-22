﻿---
Description: 'Called by CertDeleteCTLFromStore before deleting a CTL from the store.'
ms.assetid: '6cda772f-7e94-414d-99fc-a90451ac0ccf'
title: CertStoreProvDeleteCTL callback function
---

# CertStoreProvDeleteCTL callback function

The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](certdeletectlfromstore.md) before deleting a CTL from the store. This function determines whether a CTL can be deleted.

## Syntax


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## Parameters

<dl> <dt>

*hStoreProv* \[in\]
</dt> <dd>

**HCERTSTOREPROV** handle to a [*certificate store*](security.c_gly#-security-certificate-store-gly).

</dd> <dt>

*pCtlContext* \[in\]
</dt> <dd>

A pointer to a [**CTL\_CONTEXT**](ctl-context.md) structure.

</dd> <dt>

*dwFlags* \[in\]
</dt> <dd>

Any needed flag values.

</dd> </dl>

## Return value

Returns **TRUE** if a CTL can be deleted from the store.

## Requirements



|                                     |                                                      |
|-------------------------------------|------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>          |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/> |



 

 



