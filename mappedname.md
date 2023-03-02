# MappedName class

Used to store and manipulate the more-complex mapped-name used by elements (and the toponaming algorithm).

## details

private data members in the class:

```cpp
    QByteArray data;              // ideal name?
    QByteArray postfix;           // ideal name?
    bool raw;
```

where `data` could contain something like "Face2" which is either the parent (?? or the actual name if not postfix ??)
and `postfix` could contain something like ";:M2;FUS;:Hb4d:8,F" which is a "description" how we got here. 

Most of the work already done in `src/App/MappedElement.*`

mostly, just extract this into a separate file and add unit tests to ensure that these core functions are very reliable.

