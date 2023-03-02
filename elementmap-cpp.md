# ElementMap.cpp (and more to ElementMap.h)

This class much of the embodies the postfix support ElementMap in `src/App/ComplexGeoData.cpp`

It is a serialized sorted mapping of items which generatively describe the element and it's history.

The unit testing should mock up a variety of scenarios that would be seen in
real-world projects and assert expected strings. This is critical as future changes
to the class should be as consistent and non-breaking as possible.

This step DOES NOT add the `elementMap`/`_elementMap` members seen in the the ComplexGeoData class.
