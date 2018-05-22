---
Description: 'This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.'
ms.assetid: 'cb935c26-2dc9-4ab3-810d-b63f1018a62a'
title: DLL Functions
---

# DLL Functions

This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.

A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.

-   [*DllMain*](https://msdn.microsoft.com/library/windows/desktop/ms682583): The DLL entry point. The name *DllMain* is a placeholder for the library-defined function name. The DirectShow implementation uses the name **DllEntryPoint**. For more information, see the Platform SDK.
-   [**DllGetClassObject**](https://msdn.microsoft.com/library/windows/desktop/ms680760): Creates a class factory instance. Described in the previous sections.
-   [**DllCanUnloadNow**](https://msdn.microsoft.com/library/windows/desktop/ms690368): Queries whether the DLL can safely be unloaded.
-   [**DllRegisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms682162): Creates registry entries for the DLL.
-   [**DllUnregisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms691457): Removes registry entries for the DLL.

Of these, the first three are implemented by DirectShow. If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function. For more information on when the system calls the DLL entry-point function, see [*DllMain*](https://msdn.microsoft.com/library/windows/desktop/ms682583).

You must implement [**DllRegisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms682162) and [**DllUnregisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms691457), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work. Your component can simply wrap this function, as shown in the following example:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



However, within [**DllRegisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms682162) and [**DllUnregisterServer**](https://msdn.microsoft.com/library/windows/desktop/ms691457) you can customize the registration process as needed. If your DLL contains a filter, you might need to do some additional work. For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).

In your module-definition (.def) file, export all the DLL functions except for the entry-point function. The following is an example .def file:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



You can register the DLL using the Regsvr32.exe utility.

## Related topics

<dl> <dt>

[How to Create a DirectShow Filter DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 


