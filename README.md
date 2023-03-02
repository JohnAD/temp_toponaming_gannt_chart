General pattern (make this a linear flowchart-like thing)


1. Create the supporting functions needed by element naming and the algorithm.

   This stage does not yet change the behavior of FreeCAD.

   These are simply libraries with good unit testing to ensure they are accurate when used later.

   * IndexedName

     see indexedname.md

   * MappedName

     see mappedname.md

   * ElementMap.h

     see elementmap-h.md

   Are there any other clean libraries we could write to help with the following steps?

2. Create the naming-of-elements algorithm.

   Create the ElementMap class.

   This stage does not yet change the behavior of FreeCAD

   Using the previous libraries, import the general algorithm that will _eventually_ be called by ComplexGeoData.cpp to have the more advanced naming.

   Using unit tests, verify that the naming is very predictable and reliable.

   * ElementMap.cpp

     see elementmap-cpp.md

3. Add the naming.

   Add the naming, but do not use it yet.

   Add the members to the ComplexGeoData.cpp class. While the member values are set, they are not actually used.

   Add support for visibility in the Selection View.

   This stage will slow down FreeCAD and will make the naming visible on an element when selected.

   * Basics and members added to ComplexGeoData.cpp/.h

   * Adjustments to Part workbench

   * Adjustments to Sketcher workbench

   * Adjustments to ComplexGeoDataPy

4. Use it.

   Use the toponaming so that the model is more resilient to upstream object changes.

   This is the big step.

   * Adjustments to Save / Restore processes

   * Adjustments to Part workbench

   * Adjustments to Sketcher workbench

5. Optimize.

   Selectively add optimizations to speed FreeCAD up again. 

   This could include: 

     * MappedName hashing

     * IndexedName int:string map cache per-project or system-wide.

   What is actually done is TBD after step 4 is finished
