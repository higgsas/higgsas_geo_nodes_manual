Generators
===================================

************************************************************
2D Triangular Remesh
************************************************************

Remeshes 2d mesh using delaunay triangulation

.. image:: images/2dtriang.PNG

Density
  Density of triangles

Corner Angles
  Keeps corners sharp

Relax Iterations
  Relaxing triangles for more even spacing
  
.. warning::
    Input meshes has to be on the Z axis



************************************************************
Connect Points
************************************************************

Connects points with segment by distance

.. image:: images/c_points.PNG 
  
Distance
  Distance that points will be connected
  
Connect All
  Connects all points



************************************************************
Cube Recursive Subdivision
************************************************************

Recursively subdivides cubes with offset

.. image:: images/cuber1.PNG

W
  Controls subdivided quad movement 

Limit Distance
  Limits subdivided quad movement side to side
  
Random Orientation
  Randomize movement verticaly and horizontaly  
  
Seed
  Seed of random orientation
   
Scale
  Scale of the cubes
  
.. image:: images/cuber3.PNG
  
Selection
  Selects which cubes to subdivide 
  
.. image:: images/cuber2.PNG
    
.. warning::
    Cubes subdivision only wokrs correctly on geometry nodes Cube



************************************************************
Edge Bisect
************************************************************

Bisects edges from plane defined from position/direction

.. image:: images/edge_b.PNG

Position
  Position of intersection plane
  
Direction
  Direction of intersection plane
  
Flip Direction
  Flips intersection direction



************************************************************
Edge Offset
************************************************************

Evenly offsets, extrudes or dublicates selected edges

.. image:: images/edge_offset.jpeg

**Offset/Extrude/Dublicate**

- **Offset** Offsets edges
- **Extrude** Extrude edges  
- **Dublicate** Dublicates edges  
  
Distance
  Distance of the offset
  
Angle
  Rotates offset around the selected edge
  
Offset
  Offset of the offseted and original edges
  
Axis/Normal
  Direction that edges will be offseted
  
- **Axis** Uses Axis vector input for offset direction
- **Normal** Uses face normals directions

Axis
  Direction of the offset
  
Selection
  Selects what edges to offset



************************************************************
Inset Faces
************************************************************

Insets mesh faces

.. image:: images/inset_face.PNG

Offset
  Offset of the inset
  
Depth
  Push inseted faces from face normal
  
Reletive Offset
  Offsets inseted faces reletive to face area
  
Selection
  Selection of the face inset


************************************************************
Marching Squares Isolines
************************************************************

Creates edge lines on quad faces using gradient of the texture

.. image:: images/marching_squares.PNG
.. image:: images/marching_squares_img.png
.. image:: images/marching_squares1.png
.. image:: images/marching_squares2.png
.. image:: images/marching_squares3.PNG

Texture
  Texture 
  
Threshold
  Threshold
  
**Linier Interpolation**
  
- **On**  Smoothly interpolates values from texture
- **Off**  Places line on face edge midpoint

.. tip::
    Use **Attribute Smooth** node to smooth edges
    
    .. image:: images/marching_squares_tip.png
    
    .. image:: images/marching_squares_tip1.png
    
.. warning::
    Node only works on quad faces (faces that has 4 vertises)


************************************************************
Marching Squares Surface
************************************************************

smoothly cuts mesh using texture

.. image:: images/marchsurf.PNG
.. image:: images/marchsurf2.PNG
.. image:: images/marchsurf3.PNG

Texture
  Texture 
  
Threshold
  Threshold
  
**Linier Interpolation**
  
- **On**  Smoothly interpolates values from texture
- **Off**  Places line on face edge midpoint

.. image:: images/marchsurf4.PNG

.. warning::
    Node only works on quad faces (faces that has 4 vertises)



************************************************************
Marching Triangles Isolines
************************************************************

Creates edge lines on tris faces using gradient of the texture

.. image:: images/marching_triangles.PNG
.. image:: images/marching_triangles_s1.png

Texture
  Texture 
  
Threshold
  Threshold
  
**Linier Interpolation**
  
- **On**  Smoothly interpolates values from texture
- **Off**  Places line on face edge midpoint

.. tip::
    Use **Attribute Smooth** node to smooth edges
    
    .. image:: images/marching_squares_tip.png
    
    .. image:: images/marching_squares_tip1.png
    
.. warning::
    Node only works on tris faces (faces that has 3 vertises)



************************************************************
Maze Solver
************************************************************

Generates maze edge walls on the mesh using random walk with backtracing

.. image:: images/maze1.JPG
.. image:: images/maze2.JPG
  
Start Face
  Index of face from where random walk beginds
  
End Face
  Index of face that finds shortest path between start and end faces. Note this will not effect maze generation

Seed
  Seed of maze generation

Start End Path
  Curve path between start and end faces

All Paths
  All pahts of the maze

Edge Walls
  Edges selection of maze walls

Start Face
  Face selection of start face

End Face
  Face selection of end face

.. tip::
    Note that after maze generated you might not want to use **Start Face** as start of the maze, because it will give more easier path to the end, so use it as the end of the maze



************************************************************
Mesh Contours
************************************************************

Creates contour lines from mesh

.. image:: images/cont1.PNG

Slice Distance
  Distance between contour slices
  
Single Slice
  Creates just a single contour slice

.. image:: images/cont2.PNG

Plane Position
  Position of the contour slices
  
Plane Normal
  Direction of the contour slices



************************************************************
Mesh Face Divider
************************************************************

Divides mesh face horizontally and vertically / U or V

.. image:: images/mfd.PNG
.. image:: images/mfd2.PNG

U/V Ratio
  Ratio of more U or V divisions
  
Divide Propability
  Propability of face to be divided

Even Propability
  Makes division more even

Limit Distance
  Limits division distance from the center

Seed
  Seed of random divisions

Selection
  Selection of faces being divided

.. warning::
    Tris and n-gon faces will be ignored 



************************************************************
Mesh Face Recursive Subdivision
************************************************************

Subdivides quad faces with offset

.. image:: images/frs1.JPG
.. image:: images/frs2.JPG
.. image:: images/2drec.gif

Iterations
  How many times faces will be divided

W
  Controls subdivided quad movement 

Limit Distance
  Limits subdivided quad movement side to side

Smoothstep
  Creates more "sharp" movment
  
Loop Animation
  Will loops animation of selected frame range



************************************************************
Mesh to Ascii
************************************************************

Creates Ascii representation of geometry inside camera

.. image:: images/m_t_a.jpeg
.. image:: images/m_t_a.gif

Mesh
  Mesh that will be projected as Ascii

Camera
  Camera that Ascii will be projected from

Focal Lenth
  Camera focal lenth
  
Sensor Size
  Camera censor size
  
Scene Res X
  Scene X resoliution
   
Scene Res Y
  Scene Y resoliution
  
Grid Resoliution
  Resoliution of the Ascii grid
  
Grid offset
  Grid offset inside camera
  
Contrast Min
  Min contrast of the mesh normals dot product

Contrast Max
  Max contrast of the mesh normals dot product

Light Direction
  Gradient direction
  
Ascii
  Ascii characters that used for gradient values. Black/empty is space " " 



************************************************************
Mesh Topology Face Strips
************************************************************

Creates ID values for each face strips using face corner indices order.

.. image:: images/facestrip.JPG
.. image:: images/facestrip3.JPG
.. image:: images/facestrip6.JPG

Order
  Selects which face edge to use as direction

Guide Direction
  Uses direction vector to guide face strips

.. image:: images/facestrip4.JPG
.. image:: images/facestrip5.JPG
.. image:: images/facestrip7.JPG

Face Group ID
  Outputs unique id for each face strip

Boundary Edge
  Outputs edges that creates face strips boundaries

.. warning::
    Its only works on quad faces, triangles or n-gons will give bad results



************************************************************
Mesh Unfold
************************************************************

Unfolds mesh into face strips

.. image:: images/munfold.JPG

|unfold|

.. |unfold| raw:: html

    <blockquote class="twitter-tweet" data-media-max-width="560"><p lang="en" dir="ltr">Mesh unfold<a href="https://twitter.com/hashtag/geometrynodes?src=hash&amp;ref_src=twsrc%5Etfw">#geometrynodes</a> <a href="https://twitter.com/hashtag/b3d?src=hash&amp;ref_src=twsrc%5Etfw">#b3d</a> <a href="https://t.co/sZD9Ae7oGg">pic.twitter.com/sZD9Ae7oGg</a></p>&mdash; higgsas (@higgsasxyz) <a href="https://twitter.com/higgsasxyz/status/1828514096645386648?ref_src=twsrc%5Etfw">August 27, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Start Face
  Face selection that unfolding will begins. Can have multiple faces selected

.. image:: images/munfold3.JPG
.. image:: images/munfold4.JPG
.. image:: images/munfold5.JPG

**Angle/Flat**

- **Angle:** Rotates faces by custom angle defided by Unfold Amount
- **Flat:** Rotates faces by its edge angles making whole mesh flat

.. image:: images/munfold2.JPG

Unfold Amount
  Amount of how much face stris will rotate

Unfold Factor
  How much unfolding happens with using a falloff mask

Falloff Factor
  Adjusts falloff gradient

Randomize Unfolding
  By default it will use edge angles to determine which faces to split into strips. Randomize Unfolding will mix edge angles with random values

Seed
  Seed of Randomize Unfolding

Normalize Mask
  Ignores unfold factor and falloff factor making mask 0 to 1

Mask
  Creates mask that goes from start face to end face trip

.. image:: images/munfold6.JPG
.. image:: images/munfold7.JPG

Mask can also be used in shader editor to make curly parts transparent

.. image:: images/munfold8.JPG
.. image:: images/munfold9.JPG

.. warning::
    For dence mesh with many faces node can become slow, recomend to use Bake node for the animation



************************************************************
Solidify
************************************************************

Evenly solidifies mesh

.. image:: images/solidify.jpeg  
  
Even Thickness
  Evenly solidifies mesh
  
Thickness
  Thickness of solidify
  
Offset
  Offset of solidify
  
**All/TopSide/TopBottom**

- **All:** Outputs all mesh faces
- **TopSide:** Outputs Top and Side mesh faces
- **TopBottom:** Outputs Top and Bottom mesh faces

Individual
  Solidified individual faces
  
Selection
  Selection of the faces that will be solified

Top
  Selection of the top solified faces

Side
  Selection of the side solified faces

Bottom
  Selection of the bottom solified faces



************************************************************
Spheres Intersections
************************************************************

Instaces sphere meshes on points and deforms it to not intersect

.. image:: images/spinter.PNG  
.. image:: images/spinter1.PNG  
.. image:: images/spinter2.PNG  
.. image:: images/spinter3.PNG  

Sphere Mesh
  Mesh of spheres that will be deformed

Radius
  Controls radius of sphere on points

Relax Interations
  Relaxes mesh spheres

.. warning::
    Sphere Mesh must have radius of 1



************************************************************
Spin
************************************************************

Extrudes and spins mesh around the axis

.. image:: images/spin.PNG  

Angle
  Angle of the spin

Steps
  Amount of steps

Axis Push
  Push spin on the axis

Axis
  Axis of the push

Center
  Center of the spin

Merge
  Merges mesh when spins is 360

Merge Distance
  Distance of the mesh

UV Map
  Generates UV Map

Keep Faces
  Keeps Faces of the mesh

Shade Smooth
  Shades mesh smooth



************************************************************
Tessellate Align Orientation
************************************************************

Aligns components rotation to direction

.. image:: images/tesali.png

Direction
  Direction that compotent will be aligned
  
Flip Offset
  Offsets component oreantation by 90 degree 
  


************************************************************
Tessellate Mesh
************************************************************

Instances geometry (Component) on mesh faces and deforms to match face

.. image:: images/tessellate_mesh.PNG
.. image:: images/tessellate_mesh2.jpeg

Component
  Geometry that is being deformed to match mesh faces
  
**Constant/Reletive Scale**

- **Constant Scale:** Uniformly scales component
- **Reletive Scale:**  Scales component reletive to face area

Scale
  Scale factor
  
Offset
  Offsets component location from mesh face normal
  
Flip
  Rotates component 90 degrees 
  
- **0** = 0°   
- **1** = 90° 
- **2** = 180° 
- **3** = 270° 
  
Pick Component
  **ON:** Picks component from the instances list, similar how **Instance on Points/Pick Instace** node works   
  
.. image:: images/tessellate_mesh_pick.PNG

Component Index
  When **Pick Component** is On, Selects which component to use from the instaces list, similar how **Instance on Points/Instance Index** node works  
  
Merge
  Merges geometry by distance
  
Merge Distance
  Distance when geoemty gets merge
  
.. warning::
    For triangle and n-gon faces results can be undesirable
    
    .. image:: images/tessellate_mesh_warn.PNG



************************************************************
Tessellate Mesh Smooth
************************************************************

Instances geometry (Component) on mesh faces and deforms to match (Subdivision Surface) face

.. image:: images/tessellate_mesh_smooth.PNG
.. image:: images/tessellate_mesh_smooth2.PNG

Component
  Geometry that is being deformed to match mesh faces
  
Subdivisions
  Smoothly subdivides (Subdivision Surface) input mesh 
  
.. image:: images/tessellate_mesh_smooth_sub.PNG
  
**Constant/Reletive Scale**

- **Constant Scale:** Uniformly scales component
- **Reletive Scale:**  Scales component reletive to face area

Scale
  Scale factor
  
Offset
  Offsets component location from mesh face normal
  
Flip
  Rotates component 90 degrees 
  
- **0** = 0°   
- **1** = 90° 
- **2** = 180° 
- **3** = 270° 
  
Pick Component
  **ON:** Picks component from the instances list, similar how **Instance on Points/Pick Instace** node works   
  
.. image:: images/tessellate_mesh_pick.PNG

Component Index
  When **Pick Component** is On, Selects which component to use from the instaces list, similar how **Instance on Points/Instance Index** node works  
    
.. warning::
    Tris and n-gon faces will be ignored 



************************************************************
Triangle Mesh to Voronoi
************************************************************

Converts triangulated mesh to voronoi cells 

.. image:: images/triantovor.JPG
  
Limit Obtuse Triangles
  Limits obtuse triangles (triangles in which one of the interior angles measures more than 90° degrees) to avoid mesh intersections

.. image:: images/triantovor2.JPG
.. image:: images/triantovor3.JPG
.. image:: images/triantovor4.JPG

**Clamp/Use Average**

- **Clamp:** Clamps calculated circumcircle center if its lays outside of the triangle
- **Use Average:**  Uses triangle face center

Keep Boundaries
  Keeps boundaries of the mesh



************************************************************
Voxel Remesh
************************************************************

Remeshes mesh to surface voxels without voxels inside volume

.. image:: images/voxel_r1.PNG  
  
Voxel Size
  Size of a voxel
  
Exterior Band Width
  The maximum distance of the included voxels to the surface on the outside of the mesh

Interior Band Width
  The maximum distance of the included voxels to the surface on the inside of the mesh

Fill Volume
  The entire enclosed volume or otherwise only the voxels close to the surface will get a density greater than zero. This setting is only used when the mesh object is Manifold.
  
Transfer Attribute
  Transfer attribute from source mesh to a voxel

.. image:: images/voxel_r3.PNG  

Face UV Map
  Creates uv map for each face

.. image:: images/voxel_r2.PNG  










