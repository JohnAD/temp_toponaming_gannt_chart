# TopoNaming Phase 1 (step 3 of 4) - create MappedElement class

> The toponaming algorithm would benefit from a type to easily store and manipulate element naming as a whole.

## description

Create teh MappedElement.cpp class that is used to save the name parts of an element. Steps 1 and 2 must be complete first.

For context, see issue https://github.com/FreeCAD/FreeCAD/issues/8432

## notes

It contains the current IndexedName and the generated MappedName.

most of the work has been done already in the branch at `src/App/MappedElement.h`.

The comparator `ElementNameComp` and the classes `HistoryItem` and `MappedChildElements` will be added elsewhere in phase 2 when ElementMap code is built out.

mostly, just extract this into a separate file and add good unit tests to ensure that these core functions are very reliable.
