SDF Nodes
===================================

SDF - Signed distance fields creates 3d volume surface that can be definded using mathematical functions

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



************************************************************
SDF Boolean
************************************************************

Creates boolean operation between 2 SDFs volumes

**Union / Difference / Intersection / Slice / Xor**

**Union**

.. image:: images/sdfun.JPG

**Differnce**

.. image:: images/sdfdif.JPG

**Interection**

.. image:: images/sdfint.JPG

**Slice**

.. image:: images/sdfsli.JPG

**Xor**

.. image:: images/sdfxor.JPG
  
SDF 1
  First SDF input
  
SDF 2
  Second SDF input
  
Blend
  Smoothly blends boolean operation between 2 SDFs
  
.. image:: images/sdfb4.PNG

Slice / Xor Blend

  Smoothly blends boolean operation between 2 SDFs when using Slice and Xor options

Color Mask
  Crates mask between 2 SDFs
  
.. image:: images/sdfb5.PNG
.. image:: images/sdfb6.PNG
  

  


************************************************************
SDF Capsule
************************************************************

.. image:: images/sdfcap.JPG



************************************************************
SDF Cube
************************************************************

.. image:: images/sdfcube.JPG



************************************************************
SDF Cylinder
************************************************************

.. image:: images/sdfcyl.JPG



************************************************************
SDF Gyroid
************************************************************

.. image:: images/sdfgy.JPG



************************************************************
SDF Heart
************************************************************

.. image:: images/sdfheart.PNG



************************************************************
SDF Polygon
************************************************************

.. image:: images/sdfpo.JPG



************************************************************
SDF Round Cone
************************************************************

.. image:: images/sdfrc.JPG



************************************************************
SDF Schwarz P
************************************************************

.. image:: images/sdfsw.JPG



************************************************************
SDF Sphere
************************************************************

.. image:: images/sdfsp.PNG



************************************************************
SDF to Mesh
************************************************************

Converts SDF volume to mesh

.. image:: images/sdfbool.JPG

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
SDF Torus
************************************************************

.. image:: images/sdftor.PNG



************************************************************
SDF Volume Points Fracture
************************************************************

Fractures mesh volume from points

.. image:: images/svpf.PNG

Voxel Size
  Size of the voxel

Smoothing
  Creates smoother/beveled fracture edges

Gap
  Gap between cells

Noise Distortion
  Distorts fracture cells using noise texture











