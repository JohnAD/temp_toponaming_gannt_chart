# TopoNaming Phase 1 (card 4 of 4) - ElementMap Header file

> The toponaming is more easily worked on if the descriptive elements of it are gathered in one place for easy reference.

## description

The goal here is to create a common place for the consts and other names that will be used by toponaming as a whole.

`ElementMap.h`

At first, this will be mainly the strings used for serialization of the MappedName's elements. As common point of reference are discovered related to the toponaming ElementMap algorithm, this will be a good place to place them.

Later, in phase 2, this header file will be used with the associated ElementMap.cpp class.

For context, see issue https://github.com/FreeCAD/FreeCAD/issues/8432

## notes

Go ahead and move the contents of src/Mod/Part/App/TopoShapeOpCode.h to here. Include the conditional directives.

For the following items, see ComplexGeoData.cpp, TopoShapeEx.cpp.

| postfix (elementMap key) | meaning       |
|----------------|---------------|
| `:H`           | tag (local)   |
| `:C`           | child element |
| `:X`           | external tag  |
| `:I`           | index         |
| `D`            | duplicate     |
| `:T`           | deprecated tag (uses decimal) |
| `:M`           | mod           |
| `:MG`            | modgen        |
| `:G`           | gen           |
| `:U`           | upper         |
| `:L`           | lower         |

(above edited based on RealThunder's feedback)

For example,

```cpp
const std::string &ComplexGeoData::tagPostfix() {
    static std::string postfix(elementMapPrefix() + ":H");
    return postfix;
}
```

in ComplexGeoData.cpp chould be moved here to simply be something like:

```cpp
const std::string POSTFIX_FOR_TAG = ";:H";
```

I recommend we also go ahead and move `elementMapPrefix()` to a const as it simply returns a semicolon (always).
