Generators
===================================

************************************************************
Marching Squares
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
Marching Triangles
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
Tessellate Align Orientation
************************************************************

Aligns components rotation to direction

.. image:: images/tesali.png

Direction
  Direction that compotent will be aligned
  
Flip Offset
  Offsets component oreantation by 90 degree 
  

************************************************************
2D Recursive Subdivision
************************************************************

Subdivides quad faces with offset

.. image:: images/2drec.PNG
.. image:: images/2drec2.PNG
.. image:: images/2drec3.PNG
.. image:: images/2drec.gif

W
  Controls subdivided quad movement 

Limit Distance
  Limits subdivided quad movement side to side
  
Random Orientation
  Randomize movement verticaly and horizontaly  
  
Seed
  Seed of random orientation
  
Rotation
  Rotation
  
Scale
  Scale
  
Selection
  Selects which faces to subdivide 
    
.. warning::
    Subdivision only wokrs on non-deformed quad faces



************************************************************
UV Deform
************************************************************

Projects geometry to target mesh UV map

.. image:: images/uvdefrom.PNG
.. image:: images/uvdefrom2.PNG


Target Mesh
  Mesh that geometry will be project on

Depth
  Scale of projected geometry along target mesh normals
  
Offset
  Offset of projected geometry along target mesh normals
  
Delete Nonvalind
  Deletes geometry that are outside the trarget mesh UV Map
  
Rotation
  Rotation of goemetry
  
Translation 
  Translation of goemetry

Scale
  Scale of geometry
  
  

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
2D Curl Noise
************************************************************

Creates curl noise curves

.. image:: images/2d_curl.jpeg   
  
Iterations
  More iteration longer curl curves. Max iterations 400
  
Step
  Size between each iteration in curve
  
Scale
  Noise scale
  
Detail
  Noise detail
  
Offset
  Noise offset
  
Normalize Step
  Makes each step size even
  
.. warning::
    Node become really slow after alot of iterations, you can "bake it" by converting curves to mesh and applying modifier  
  
  
  
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
Array
************************************************************

Creates array of the geometry

.. image:: images/array.PNG

Count
  Amount that geometry will duplicated
  
**Constant Offset**

- **Off:** Offsets geometry from its bonding box
- **On:** Offsets geometry from its center

Translation
  Offsets array
  
Rotation
  Rotates geometry



************************************************************
Circular Array
************************************************************

Creates array of the geometry on a circle

.. image:: images/c_array.PNG

Count
  Amount that geometry will duplicated on a circle
  
Radius
  Radius of the circle
  
Circle Rotation
  Rotates circle
  
Rotation
  Rotates geometry orientation
  
Scale
  Scale of the geometry
  
Pick Instance
  Picks instaces from the instances list or collection

.. image:: images/array_p.PNG

Instance Index
  Index of the instances list
  
  
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
Image to Ascii
************************************************************

Creates Ascii from image

.. image:: images/i_t_ac.jpeg

Image
  Image input
  
Resoliution
  Grid resolution of Ascii
  
Img Res X
  Input image X resolution

Img Res Y
  Input image Y resolution

Contrast Min
  Min contrast of the image values

Contrast Max
  Max contrast of the image values

Ascii
  Ascii characters that used for gradient values. Black/empty is space " " 
  
Frame
  Frame of the image input
  
Color Attribute
  Creates color attribute from image colors









