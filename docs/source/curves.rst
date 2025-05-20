Curve
===================================

************************************************************
2D Hilber Curve
************************************************************

Creates hilbert curve

.. image:: images/hilbc1.JPG
.. image:: images/hilbc2.JPG

Size
  Size of hilber curve

Order
  Order of hilber curve

Absolute Size
  Makes hilbert curve exactly match Size

Moore Curve / Cyclic
  Creates Moore curve that is cyclic

.. image:: images/hilbc3.JPG



************************************************************
3D Curve Fill
************************************************************

Fills curves with face in 3d

.. image:: images/3dcf.PNG

N-Gons/Triangles
  Fills with single n-gon face or triangulates it

.. image:: images/3dcf2.PNG



************************************************************
Adaptive Catenary Splines
************************************************************

Creates physically accurate rope sag effect that maintains its length from a splines with 2 points

.. image:: images/catn1.PNG
.. image:: images/catn2.gif

Splines Length
  Splines length per spline segment
  
Splines Resolution
  Resolution of the splines per spline segment

Axis Rotation
  Rotates spline around its axis



************************************************************
Advect Splines
************************************************************

Instances splines on points and advects/moves splines each step by vector

.. image:: images/advectsp.PNG
.. image:: images/advectsp1.PNG

Steps
  Steps of the splines
  
Direction
  Vector direction that splines moves each step



************************************************************
Align Curve Normal
************************************************************

Aligns curve normal to the Direction vector by tilting it

.. image:: images/curveal.png

Direction
  Direction that curve normals will be aligned
  
Tilt
  Tilts curve



************************************************************
Circle Outer/Inner Tangent Curve
************************************************************

Bevels curve segments in a way that connects circles inner/outer tangnets

.. image:: images/ciot.PNG
.. image:: images/ciot1.PNG

Resolution
  Resolution of the bevel

Radius 
  Radius of the bevel

Up Axis
  Axis of bevel

Flip Sides
  Flips bevel side

.. image:: images/ciot2.PNG
.. image:: images/ciot3.PNG



************************************************************
Curve Banking
************************************************************

Sets curve tilt to create road banking effect depending on curve curvature

.. image:: images/c_bank1.PNG
.. image:: images/c_bank.PNG

Banking
  Amount of banking curve tilt

Blur
  Blurs banking tilt for smoother results

Tilt
  Tilts whole curve



************************************************************
Curve Bisect
************************************************************

Cuts a curve along a custom plane

.. image:: images/cbisect.PNG

Place Position
  Position of cutting plane

Plane Normal
  Direction of cutting plane

Flip Direction
  Flips cutting plane direction



************************************************************
Curve Intersection
************************************************************

Creates point on curve segment where intersection is find

.. image:: images/cinter.JPG

**2D/3D**

- **2D:** Calculates intersection on Z axis
- **3D:** Calculates intersection in 3D space

.. image:: images/cinter1.JPG
.. image:: images/cinter2.JPG

3D Distance Threshold
  Distance Threshold between found intersection segments



************************************************************
Curve Mesh Boolean
************************************************************

Cuts curve using a mesh

.. image:: images/cmbool.PNG

**Diff/Inter/Slice**

- **Diff:** Difference boolean mode
- **Inter:**  Intersection boolean mode
- **Slice:**  Slice boolean mode

Intersecting points
  Outputs true boolean value on new points that been created from mesh boolean

.. warning::
    Singe curve segment can only be cut one time



************************************************************
Curve Offset
************************************************************

Evenly offsets curve from axis or normal

.. image:: images/curve_offset.PNG
.. image:: images/curve_offset2.PNG

Duplicate
  Duplicates input curves
  
Distance  
  Distance of the offset
  
Axis Rotation
  Rotation of the axis
  
Offset
  Offsets distance offset
  
Axis/Normal
  Uses axis vector or the curve normal
  
Axis
  Axis direction



************************************************************
Curve Point Angle
************************************************************

Calculates curve points angle from its neighbors points 

.. image:: images/c_p_a.PNG
.. image:: images/c_p_a2.PNG

Angle
  Angle output in radians from 0 to 3.14159



************************************************************
Decimate Curve
************************************************************

Removes curve points depending on curve curvature

.. image:: images/cdecim.PNG

Angle
  Cuve points greater then angle that points will be removed
  
Smooth
  Smooths curve to minimize the gaps

.. warning::
    Cyclic curves decimate results can be undesirable 



************************************************************
Even Curve to Mesh
************************************************************

Makes curve radius even

.. image:: images/even_curve1.PNG
.. image:: images/even_curve.PNG

Profile Curve
  Profile Curve
  
Fill Caps
  Fill Caps



************************************************************
Heart
************************************************************

Curve heart shape

.. image:: images/cheart.PNG



************************************************************
Loft Splines
************************************************************

Connects splines

.. image:: images/loft_splines.PNG
.. image:: images/loft_splines.jpeg

Bezier/Catmull/Poly
  Interpolation method
  
Resample Splines
  Resamples splines. **Tip:** Use it if splines has uneven controls points 
  
Resample Count
  Resamples spline points count
  
Subdivide
  Subdivides connection between splines
  
Cyclic Splines
  Connects input splines
  
Cyclic Loft
  Connected loft



************************************************************
Poly Arc
************************************************************

Creates circle arcs smootly connected from curve segments

.. image:: images/polyarc.PNG

Resolution
  Resolution of each segment arc
  
Auto Tangent
  Automaticaly creates tangent that first curve segment arc will follow

First Point Tangent
  Tangent direction that first curve segment arc will follow

.. image:: images/polyarc2.PNG
.. image:: images/polyarc3.PNG

Connect Segment
  Connects each arcs segments

Set Cyclic
  Connects first arc with the last arc

Arc/Poly
  Connection type 
  
.. warning::
    Node only works with single spline and spline can only have maximum of 40 segments. In Blender 4.0 works with unlimited curve segments



************************************************************
Splines Patch
************************************************************

Creates grid patch from 4 splines

.. image:: images/spatch.png
.. image:: images/spatch1.png

**Resample/Set Resolution**

- **Resample:**  Resamples input splines
- **Set Resolution:**  Set resolution for Bezier splines
  
U Resolution
  Sets grid resolution for rows
  
V Resolution
  Sets grid resolution for columns



************************************************************
Tubes to Splines
************************************************************

Converts mesh tubes to splines

.. image:: images/tts.PNG

Sort Index
  Choses edge index to compare direction
  
Epsilon
  Value to match direction

Delete Caps
  Deletes caps that has more than 4 faces

.. warning::
    Cylinder primitives or manually created cylinders might not work because of random indices



************************************************************
Twist Curve
************************************************************

Evenly offsets curve from axis or normal

.. image:: images/twist_curve.PNG
.. image:: images/twist_curve2.PNG

Spline Amount
  Duplicates splines
  
Factor/Lenth
  Uses splines factor or lenth paramater for the rotations
  
Thickness
  Distance of the offset from the curve
  
Rotation
  Amount of rotation



************************************************************
UV Curve to Mesh
************************************************************

Creates UV map attribute for curves

.. image:: images/uv_curve.jpeg

Profile Curve
  Profile Curve
  
Fill Caps
  Fill Caps
  
**Factor/Lenth**

- **Factor:** Scales UV map to curve parameter factor
- **Lenth:**  Scales UV map to curve lenth
 
UV Attribute
  Attribute name for storing UV attribute on mesh
  
Pack UV Islands
  Packs UV Islands
  
Margin
  Gap between UV islands
  
Rotate
  Rotates UV islands for better packing

