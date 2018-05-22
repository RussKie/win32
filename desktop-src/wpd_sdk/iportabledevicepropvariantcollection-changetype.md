---
Description: 'The ChangeType method converts all items in the collection to the specified VARTYPE.'
ms.assetid: 'b01b6205-c900-4b2e-810f-426e1e71a008'
title: 'IPortableDevicePropVariantCollection::ChangeType method'
---

# IPortableDevicePropVariantCollection::ChangeType method

The **ChangeType** method converts all items in the collection to the specified VARTYPE.

## Syntax


```C++
HRESULT ChangeType(
  [in]�const VARTYPE vt
);
```



## Parameters

<dl> <dt>

*vt* \[in\]
</dt> <dd>

Specifies the **VARTYPE** to which you want to convert all items in the collection. Example types include VT\_UI4 and VT\_UI8.

</dd> </dl>

## Return value

The method returns an **HRESULT**. Possible values include, but are not limited to, those in the following table.



| Return code                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl> | The method succeeded.<br/> |



�

## Remarks

If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.

## Requirements



|                    |                                                                                                    |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Library<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## See also

<dl> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> </dl>

�

�



