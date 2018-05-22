---
title: SLIDER.disabledImage
description: The disabledImage attribute specifies or retrieves the image of the slider that is used when the slider control is disabled.
ms.assetid: '91b1c2e3-6c92-4baa-b1f3-e44707157f4b'
keywords: ["SLIDER.disabledImage Windows Media Player"]
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
---

# SLIDER.disabledImage

The **disabledImage** attribute specifies or retrieves the image of the slider that is used when the slider control is disabled.

``` syntax
        elementID.disabledImage
```

## Possible Values

This attribute is a read/write **String** containing the name of an image file.

## Remarks

The **disabledImage** is optional. If it is not provided, the **backgroundImage** is used for all disabled states. When a slider control is disabled, no foreground image is visible.

The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).

## Requirements



|                    |                                                      |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player version 7.0 or later<br/> |



## See also

<dl> <dt>

[**SLIDER Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

�

�




