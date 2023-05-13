Geometry Measure
===================================

************************************************************
Mesh Measure
************************************************************

Calculates mesh total Volume, Area, Volume Center of Mass, Area Center of Mass

.. image:: images/mesh_measure.png

Volume
  Volume of the mesh
  
Area
  Area of the mesh
  
Volume Center of Mass
  Position of Volume Center of Mass

Area Center of Mass
  Position of Area Center of Mass
  
  

************************************************************
Mesh Island Measure
************************************************************

Calculates Area, Center, Area Center of Mass for each mesh island

.. image:: images/m_i_m.png

Area
  Area of the mesh
  
Center
  Position from average vertex locations

Area Center of Mass
  Position of Area Center of Mass
  
  
  
************************************************************
Mesh Ambient Occlusion
************************************************************

Calculates mesh ambient occlusion

.. image:: images/ao1.PNG
  
Rays Samples
  Amount of rays for sampling
  
Rays Angle
  Angle that rays direction will be randomly rotated. Bigger angle will give more accurate results but with more noise

Seed
  Random seed of the rays random direction
  
Blur Iterations
  Smooth ambient occlusion map
  
External Mesh
  Uses external mesh that rays will hit from main mesh to calculate ambient occlusion map
  
.. image:: images/ao2.PNG
  
Attribute
  Name of the thickness value attribute on point domain 
  
.. warning::
    Node can be really slow depending on mesh density and rays samples. You can "bake it" by applying geometry nodes modifier and the "ao" attribute will be stored on the mesh
    
    
    
************************************************************
Mesh Thickness
************************************************************

Calculates mesh thickness 

.. image:: images/mesh_thick.jpeg
  
Rays Samples
  Amount of rays for sampling
  
Rays Angle
  Angle that rays direction will be randomly rotated. Bigger angle will give more accurate results but with more noise

Seed
  Random seed of the rays random direction
  
Normalize
  Fits values between 0 to 1
  
Attribute
  Name of the thickness value attribute on point domain 
  
.. warning::
    Node can be really slow depending on mesh density and rays samples. You can "bake it" by applying geometry nodes modifier and the "thickness" attribute will be stored on the mesh
  
  
 
************************************************************
Mesh Tension
************************************************************

Creates Compression and Tension mask by comparing Face Area before and after mesh deformation

.. image:: images/mesh_tension.png
.. image:: images/mesh_tension1.png

Original Geometry
  Geometry before deformation happens
  
Strength
  Strength of the Tension / Compresion values
  
Bias
  Offset of the Tension / Compresion values 
  
Tension
  Output values of the tension map

Compresion
  Output values of the compresion map

 

************************************************************
Face Tangent
************************************************************

Creates Direction Vector that points from Face center to its edge

.. image:: images/face_tangent.png
.. image:: images/face_tangent2.png

Order
  Selects to which face edge vector points
  
Aligh to Direction
  Choses direction that are closest to the **Direction** input

.. image:: images/face_tangent_a.png

Direction
  Direction
  
Corner Tangent
  Creates Direction Vector that points from Face center to its vertex

.. image:: images/face_tangent_c.png


************************************************************
UV Tangent
************************************************************

Creates directional vector from UV map on face domain

.. image:: images/uv_tangent.png

UV
  UV map input for direction calculation
  
U/V
  Choses UV map alightment axis to **U** or **V**



************************************************************
Gradient Direction
************************************************************

Creates directional vector from gradient 

.. image:: images/grad_dir.jpeg
.. image:: images/grad_dir2.PNG
.. image:: images/grad_dir.PNG

Gradient
  Gradient float input
  
Solenoidal
  Divergence-free vector field



************************************************************
Face Vertex Poistion
************************************************************

Gives face vertex position on face domain

.. image:: images/f_v_p.png
.. image:: images/f_v_p1.png
.. image:: images/f_v_p2.png  

Position 1
  Position 1 of the face corner

Position 2
  Position 2 of the face corner

Position 3
  Position 3 of the face corner

Position 4
  Position 4 of the face corner



************************************************************
Line Line Intersection
************************************************************

Calculates intersection point between 2 lines on the Z axis

.. image:: images/lines_int.PNG

Line 1 Point 1
  First point of the line

Line 1 Point 2
  Second point of the line

Line 2 Point 1
  First point of the line

Line 2 Point 2
  Second point of the line



************************************************************
Line Line Intersection
************************************************************

Calculates intersection point between 2 lines on the Z axis

.. image:: images/bisect.PNG

Line Point 1
  First point of the line

Line Point 2
  Second point of the line

Plane Position
  Position of intersection plane

Plane Normal
  Normal of intersection plane



  
  
