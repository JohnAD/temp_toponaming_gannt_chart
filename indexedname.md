# TopoNaming Phase 1 (step 1 of 4) - create IndexedName class

> The toponaming algorithm would benefit from a type to easily store and manipulate the short reference names of the elements.

## description

Create an IndexedName.cpp class that is used to save the name of an element. It will later by used by the `MappedElement` class which will be used by the `ElementMap` class.

One benefit of this change is to "simplify" the renaming/numbering of faces/etc. For example, it provides a `+=` operator to increment the number part.

It stores the "short name" of the element, such as "Face1".

For context, see issue https://github.com/FreeCAD/FreeCAD/issues/8432

## notes

Instead of a simple string, it is a string/integer combination. The string is the "type" of element. The integer is an number on it's suffix. So, instead of storing "face3", this class stores "face" and 3.

The `toString()` function resolves the class back into a simple string.

suggested private data members in the class:

```cpp
    const char* ;
    int;
```

most of the work has been done already in the branch at `src/App/MappedElement.h`

mostly, just extract this into a separate file and add good unit tests to ensure that these core functions are very reliable.
