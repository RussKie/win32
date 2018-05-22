---
title: RasAdminFreeBuffer function
description: The RasAdminFreeBuffer function frees memory that was allocated by RAS on behalf of the caller.
ms.assetid: '6dfbba22-3af1-4771-8c22-506996f30c6b'
keywords: ["RasAdminFreeBuffer function RAS"]
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
---

# RasAdminFreeBuffer function

\[This function is provided only for backward compatibility with Windows�NT Server 4.0. It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server�2003. Applications should use the [**MprAdminBufferFree**](mpradminbufferfree.md) function.\]

The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.

## Syntax


```C++
DWORD RasAdminFreeBuffer(
  _In_�PVOID Pointer
);
```



## Parameters

<dl> <dt>

*Pointer* \[in\]
</dt> <dd>

Pointer to the buffer to be freed.

</dd> </dl>

## Return value

If the function succeeds, the return value is ERROR\_SUCCESS.

If the function fails, the return value can be the following error code.



| Value                                                                                                    | Meaning                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**ERROR\_INVALID\_PARAMETER**</dt> </dl> | The *Pointer* parameter is invalid.<br/> |



�

There is no extended error information for this function; do not call [**GetLastError**](https://msdn.microsoft.com/library/windows/desktop/ms679360).

## Remarks

Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.

## Requirements



|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| End of client support<br/> | Windows�2000 Professional<br/>                                                   |
| End of server support<br/> | Windows�2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Library<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## See also

<dl> <dt>

[Remote Access Service (RAS) Overview](about-remote-access-service.md)
</dt> <dt>

[RAS Server Administration Functions](ras-server-administration-functions.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

�

�




