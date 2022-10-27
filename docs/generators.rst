Generators
===================================

************************************************************
Marching Squares
************************************************************

Creates edge lines on faces using gradient of the texture

.. image:: images/marching_sqaures.PNG
.. image:: images/marching_sqaures1.png
.. image:: images/marching_sqaures2.png
.. image:: images/marching_sqaures3.PNG

Texture
  Texture 
  
Threshold
  Threshold
  
**Linier Interpolation**
  
- **On**  Smoothly interpolates values from texture
- **Off**  Places line on face edge midpoint

.. tip::
    Use **Attribute Smooth** node to smooth edges
    
    .. image:: images/marching_sqaures_tip.png
    
    .. image:: images/marching_sqaures_tip1.png
    
.. warning::
    Node only works quad faces (face has 4 vertises)

