# TopoNaming Phase 1 - create IndexedName class

This is a class that is used to save the name of an element. It will later by used by the `MappedElement` class which will be used by the `ElementMap` class.

It stores the "short name" of the element, such as "Face1".

------

Instead of a simple string, it is a string/integer combination. The string is the "type" of element. The integer is an number on it's suffix. So, instead of storing "face3", this class stores "face" and 3.

The purpose of this change is to "simplify" the renaming/numbering of faces/etc. For example, it provides a `+=` operator to increment the number part.

The `toString()` function resolves the class back into a simple string.

suggested private data members in the class:

```cpp
    const char* ;
    int;
```

most of the work has been done already in the branch at `src/App/MappedElement.h`

mostly, just extract this into a separate file and add good unit tests to ensure that these core functions are very reliable.
