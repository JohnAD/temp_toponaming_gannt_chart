1. (Prepare)

   * IndexedName

     see `indexedname.md`

   * MappedName

     see `mappedname.md`

   * MappedElement

     see `mappedelement.md` The previous two items must be completed first.

   * ElementMap.h

     see `elementmap-h.md`

   Are there any other clean libraries we could write to help with the following steps?

2. (Implement)

   * Add the members to the ComplexGeoData.cpp class. They are not actually used yet.
     Nor are they set unless called by hand via Python console.

   * Basics and members added to ComplexGeoData.cpp/.h; Add visibility in Selection View of current name

   * ElementMap.cpp (importing RealThunder algo)

     see elementmap-cpp.md
     
   * Support user-defined element-name mapping override (add to Algo)

3. (Integrate)

   * Adjustments to Sketcher workbench

   * Adjustments to Part workbench

   * Adjustments to ComplexGeoDataPy

4. (Enable)

   * Adjustments to Save / Restore processes

   * Adjustments to Sketcher workbench

   * Adjustments to Part workbench

5. (Optimize)

   * consider MappedName hashing

   * consider IndexedName int:string map cache per-project or system-wide.
