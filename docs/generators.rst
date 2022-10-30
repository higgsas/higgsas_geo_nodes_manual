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
    Node only works on quad faces (face that has 4 vertises)



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
    Node only works on tris faces (face that has 3 vertises)



************************************************************
Tessellate Mesh
************************************************************

Creates edge lines on quad faces using gradient of the texture

.. image:: images/tessellate_mesh.PNG

Mesh 
  Mesh
  
Component
  as
  
**Constant/Reletive Scale**

- **Constant Scale:** Uniformly scales component
- **Reletive Scale:**  Scales component reletive to face area

Scale
  Scale factor
  
Offset
  Offsets component location on face
  
Flip
  Rotates component 90 degrees 
  
- **0** = 0°   
- **1** = 90° 
- **2** = 180° 
- **3** = 270° 
  
  
  
  
  
  
  
  
  
  
  
