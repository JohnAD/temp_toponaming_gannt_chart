# TopoNaming Phase 1 (step 2 of 4) - create MappedName class

> The toponaming algorithm would benefit from a type to easily store and manipulate the name serialized from the element mapping.

## description

Create MappedName.cs to store and manipulate the more-complex mapped-name used by elements (and the toponaming algorithm).

For context, see issue https://github.com/FreeCAD/FreeCAD/issues/8432

## notes

private data members are defined as follow in the branch:

```cpp
    QByteArray data; 
    QByteArray postfix; 
    bool raw;
```

where `data` could contain something like "Face2" which is either the parent (?? or the actual name if not postfix ??)
and `postfix` could contain something like ";:M2;FUS;:Hb4d:8,F" which is a "description" how we got here.

The methods of determining the contents of those fields is done in phase 2 in the ElementMap class; this class should be simpler.

I personally recommend using a more descriptive name than `data`, but those are private elements so the naming is not critical.

Most of the work already done in `src/App/MappedElement.*`

mostly, just extract this into a separate file and add unit tests to ensure that these core functions are very reliable.

