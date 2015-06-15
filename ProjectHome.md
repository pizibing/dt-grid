# Introduction #

The DT-Grid is a data structure for representing and simulating high resolution level set surfaces.
The memory usage is proportional to the size of the narrow band as opposed to the volume of the simulation domain,
and in addition the DT-Grid performs relatively fast due to cache coherency.
The DT-Grid and derivative work have been used in many applications ranging from surface processing to fluid simulation.
Furthermore the DT-Grid has been used in movie production, e.g. to create fluid effects for Pirates of the Caribbean III.

# License #

The core library including the DT-Grid data structure is released under the New BSD license, whereas the remaining tools are released under GPL V2 due to a dependency on third party libraries that come with GPL V2.
In case you use the DT-Grid data structure to produce results for a publication, a citation of the main DT-Grid reference is highly appreciated:

"Dynamic Tubular Grid: An Efficient Data Structure and Algorithms for High Resolution Level Sets", Michael B. Nielsen and Ken Museth, Journal of Scientific Computing 26(3), March 2006, Pages 261-299.

# Features #

This DT-Grid package currently contains the following features:

DT-Grid narrow band data structure (New BSD license)
  * Support for iterators
  * Support for random and neighbor access
  * Support for narrow band dilation and rebuild
  * Support for first order one-sided, second order central and WENO finite difference schemes
  * Support for CSG operations
  * Support for open (ie unenclosed) level set volumes
    * Extration of open level set subvolumes from larger closed or open level set volumes
    * Random and neighbor access, csg and localized level set operations on open level set volumes
    * Insertion of open level set volumes back into the original level set volume
  * Support for augmented level sets
    * Additional fields such as texture coordinates, normals etc.

Tool for conversion of closed .obj and .ply mesh files to DT-Grids (GPL V2 license)

Tool for conversion of DT-Grids to .ply mesh files (GPL V2 license)

Simulation Tools (New BSD license)
  * Level set motion in the normal direction
    * Mean curvature flow
    * Volume conserving mean curvature flow
    * Shape metamorphosis
  * Level set advection in an externally generated velocity field
    * Enright Test

Test program that illustrates the following features (New BSD license)
  * Iterating over the narrow band
  * Iterating a stencil over the narrow band
  * Random and neighbor access (on open and closed level sets)
  * CSG operations (on open and closed level sets)
  * Computing the closest point on a surface
  * Level set computations (on open and closed level sets)
  * Localized level set computations on subsets of the level set narrow band (open level sets)
  * Rebuilding the narrow band (on augmented, open and closed level sets)


# References #

For more detail see for example the following papers and technical sketches:

Nielsen, M.B., Museth, K.: Dynamic Tubular Grid: An Efficient Data Structure and Algorithms for High Resolution Level Sets. Journal of Scientific Computing, Volume 26, Number 3, March 2006. Pages 261-299.

Houston, B., Nielsen, M.B., Batty, C., Nilsson, O., Museth, K.: Hierarchical RLE Level Set: A Compact and Versatile Deformable Surface Representation. ACM Transactions on Graphics, Volume 25, Number 1, January 2006. Pages 151-175.

Nielsen, M.B., Nilsson, O., Söderström, A., Museth, K.: Out-Of-Core and Compressed Level Set Simulations, ACM Transactions on Graphics 26(4), October 2007 (Presented at SIGGRAPH 2008, Partial Differential Equations paper session).

Nemitz, O., Nielsen, M. B., Rumpf, M., Whitaker, R.: Finite Element Methods on Very Large, Dynamic Tubular Grid Encoded Implicit Surfaces, SIAM Journal of Scientific Computing, Vol. 31, No. 3. pp. 2258-2281, 2009.

Nemitz, O., Nielsen, M. B., Rumpf, M., Whitaker, R.: Narrow Band Methods for PDEs on Very Large Implicit Surfaces. In Vision, Modeling and Visualization Proceedings, pages 171-180, November 2007.

Nielsen, M.B., Nilsson, O., Söderström, A., Museth, K.: Virtually Infinite Resolution Deformable Surfaces. In Proc. SIGGRAPH 2006 Sketches and Applications, August 2006.

Houston, B., Nielsen, M.B., Batty, C., Nilsson, O., Museth, K.: Gigantic Deformable Surfaces. In Proc. SIGGRAPH 2005 Sketches and Applications, August 2005.

Nielsen, M.B., Museth, K.: An Optimized, Grid Independent, Narrow Band Data Structure. In Proc. SIGRAD 2004 Sketches and Applications, November 2004.

Nielsen, M.B.: Efficient and High Resolution Level Set Simulations - Data Structures, Algorithms and Applications, PhD Dissertation, Aarhus University, December 2006.

Museth, K., Clive, M., Bin Zafar, N.: Blobtacular: surfacing particle system in "Pirates of the Caribbean 3". In Proc. SIGGRAPH 2007 Sketches and Applications, August 2007.