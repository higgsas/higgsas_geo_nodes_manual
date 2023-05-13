SDF Nodes
===================================

SDF - Signed distance fields creates 3d volume surface that can be definded using mathematical functions

************************************************************
SDF to Mesh
************************************************************

Converts SDF volume to mesh

.. image:: images/sdftomesh.PNG

SDF
  SDF field that mesh will be created
  
Voxel Size
  Density of the mesh created. Lower values = dense mesh
  
Min Bounds
  Position in 3d space that volume will be calculated
  
Max Bounds
  Position in 3d space that volume will be calculated
  
Bounds Padding
  Extends voxels from the bounds
  
Shade Smooth
  Shades mesh smooth
  
Show Bounds
  Shows bounds visualisation that volume will be calculated
  
  
  
************************************************************
SDF Boolean
************************************************************

Creates boolean operation between 2 SDFs volumes

.. image:: images/sdfb1.PNG
.. image:: images/sdfb2.PNG
.. image:: images/sdfb3.PNG

**Uni / Dif / Int**

- **Uni** Union operation
- **Dif** Difference operation
- **Int** Intersection operation
  
SDF 1
  First SDF input
  
SDF 2
  Second SDF input
  
Blend
  Smoothly blends boolean operation between 2 SDFs
  
.. image:: images/sdfb4.PNG

Color Mask
  Crates mask between 2 SDFs
  
.. image:: images/sdfb5.PNG
.. image:: images/sdfb6.PNG
  

************************************************************
Mesh to SDF
************************************************************

.. image:: images/sdftm.PNG

Converts mesh to SDF volume

Iso
  Volume offset from mesh surface to inside/outside
  
.. image:: images/sdftm2.PNG
.. image:: images/sdftm3.PNG

Fill Volume
  Fills SDF volume
  
.. image:: images/sdftm5.PNG

  






















