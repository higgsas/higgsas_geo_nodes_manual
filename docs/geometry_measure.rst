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







  
  
