# manusoft-refcountedptr
Simple shared smart pointer implementation with ULONG refence count

The reference counted pointer is a template class that wraps a typed
data member along with a reference count. Just include the header in
your C++ project:

#include "RefCountedPtr.h"

The following classes are implemented:
- RefCounterBase
    => non-template base class containing reference count
- RefCounter<T>
    => wraps a T along with a reference count
- RefCountedPtr<T, R>
    => wraps a T* and associated reference count
- LockedPtr<T, R>
    => Non-counted pointer to T that can be cast to RefCountedPtr<T, R>
- RefCountedPtrAsIUnknown<R>
    => implements IUnknown for a RefCountedPtr
