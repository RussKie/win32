﻿---
Description: 'Gets an array of BOOL values.'
ms.assetid: '4a5e2f48-fa82-47dc-a388-02a8679585d2'
title: 'ID3DXBaseEffect::GetBoolArray method'
---

# ID3DXBaseEffect::GetBoolArray method

Gets an array of BOOL values.

## Syntax


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## Parameters

<dl> <dt>

*hParameter* \[in\]
</dt> <dd>

Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Unique identifier. See [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pB* \[out\]
</dt> <dd>

Type: **[**BOOL**](winprog.windows_data_types)\***

Returns an array of Boolean values.

</dd> <dt>

*Count* \[in\]
</dt> <dd>

Type: **[**UINT**](winprog.windows_data_types)**

Number of Boolean values in the array.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK. If the method fails, the return value can be D3DERR\_INVALIDCALL.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetBoolArray**](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 



