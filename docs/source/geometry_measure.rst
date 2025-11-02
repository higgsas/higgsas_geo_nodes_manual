Geometry Measure
===================================

.. image:: images/geomeasure.jpg

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
Fit Plane
************************************************************

Creates diretional normal vector given point cloud 

.. image:: images/fitp.JPG
.. image:: images/fitp2.JPG

Position
  Position of the points
  
Group ID
  Group if for points

.. image:: images/fitp3.JPG



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
Instances Bounding Box
************************************************************

Generates bounding box min max values for each instance in global coordinate space

.. image:: images/bboxinst.JPG


Min
  Min of bounding box

Max
  Max of bounding box



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
Line Plane Intersection
************************************************************

Calculates intersection points between lines and plane

.. image:: images/bisect.PNG

Line Point 1
  First point of the line

Line Point 2
  Second point of the line

Plane Position
  Position of intersection plane

Plane Normal
  Normal of intersection plane



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
Mesh Curvature
************************************************************

Calculates different types of mesh curvatures

Angle Unsigned

.. image:: images/curvat.JPG
  
Angle Signed

.. image:: images/curvat2.JPG

Gaussian Curvature

.. image:: images/curvat3.JPG

Mean Curvature

.. image:: images/curvat4.JPG



************************************************************
Mesh Fresnel
************************************************************

Calculates mesh fresnel from camera point of view

.. image:: images/mfrestnel.JPG
.. image:: images/mfrestnel2.JPG
  
Camera/Origin
  Uses Camera or Custom origin location for calculating direction 

Origin
  Location of hte origin

Bias
  Offset of the fresnel

Scale
  Intensity of the fresnel

Exponent
  Falloff of the fresnel



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
Mesh Tension
************************************************************

Creates Compression and Tension masks by comparing edge lenghts before and after mesh deformation

.. image:: images/tension.jpg
.. image:: images/tension3.jpg
.. image:: images/tension4.jpg
.. image:: images/mesh_tension1.png

Rest Position
  Position attribute that needs to be captured/stored before the mesh deformation happens. If using Armature use "rest_position" attribute by enabling it in properties/data tab

.. image:: images/tension2.jpg

Strength Tension
  Strength of the Tension mask

Strength Compression
  Strength of the compression mask
  
Bias Tension
  Offset of the tension values 
  
Bias Compression
  Offset of the compression values 

Clamp
  Clamps tension and compresions mask values between 0 and 1



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
Triangle Incircle
************************************************************

Calculate incircle from triangle

.. image:: images/incircle.PNG
.. image:: images/incircle2.PNG

Point 1
  Point 1 of triangle
  
Point 2
  Point 2 of triangle

Point 3
  Point 3 of triangle

Center
  Center of circle

Radius
  Radius of circle

Normal
  Normal direction of circle



************************************************************
UV Tangent
************************************************************

Creates directional vector from UV map on face domain

.. image:: images/uv_tangent.png

UV
  UV map input for direction calculation
  
U/V
  Choses UV map alightment axis to **U** or **V**



  
  
