---
title: CD3DX12\_RANGE\_UINT64 structure
description: A helper structure to enable easy initialization of a D3D12\_RANGE\_UINT64 structure.
ms.assetid: '789A2C46-B7D4-462E-9C10-69FD63D27491'
keywords: ["CD3DX12_RANGE_UINT64 structure"]
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
---

# CD3DX12\_RANGE\_UINT64 structure

A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](d3d12-range-uint64.md) structure.

## Syntax


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &amp;o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
   ��������������������operator const D3D12_RANGE_UINT64&amp;() const;
};
```



## Members

<dl> <dt>

**CD3DX12\_RANGE\_UINT64()**
</dt> <dd>

Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.

</dd> <dt>

**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**
</dt> <dd>

Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](d3d12-range-uint64.md) structure.

</dd> <dt>

**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**
</dt> <dd>

Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.

</dd> <dt>

**operator const D3D12\_RANGE\_UINT64&() const**
</dt> <dd>

Implicit conversion to a D3D12\_RANGE\_UINT64 structure. Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.

</dd> </dl>

## Requirements



|                   |                                                                                     |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## See also

<dl> <dt>

[Helper Structures for D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12\_RANGE\_UINT64**](d3d12-range-uint64.md)
</dt> </dl>

�

�




