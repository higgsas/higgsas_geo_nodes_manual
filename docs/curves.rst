Curves
===================================

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


************************************************************
3D Curve Fill
************************************************************

Fills curves with face in 3d

.. image:: images/3dcf.PNG

N-Gons/Triangles
  Fills with single n-gon face or triangulates it

.. image:: images/3dcf2.PNG


************************************************************
Curve Bisect
************************************************************

Cut a curbe along a custom plane

.. image:: images/cbisect.PNG

Place Position
  Position of cutting plane

Plane Normal
  Direction of cutting plane

Flip Direction
  Flips cutting plane direction



************************************************************
Curve Point Angle
************************************************************

Calculates curve points angle from its neighbors points 

.. image:: images/c_p_a.PNG
.. image:: images/c_p_a2.PNG

Angle
  Angle output in radians from 0 to 3.14159
  
  

************************************************************
Align Curve Normal
************************************************************

Aligns curve normal to the Direction vector by tilting it

.. image:: images/curveal.png

Direction
  Direction that curve normals will be aligned
  
Tilt
  Tilts curve






