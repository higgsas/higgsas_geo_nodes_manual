Simulation
===================================

************************************************************
Reaction Diffusion Solver
************************************************************

Creater growing/mixing effect between two virtual chemicals 

.. image:: images/reactdiff1.PNG
.. image:: images/reactdiff.gif
.. image:: images/reactdiff2.PNG

Inside Reaction Diffusion Solver node group (tab to open)

.. image:: images/reactdiff3.PNG

A
  Chemical A value stored on the mesh (set to 1)

B
  Chemical B value stored on the mesh (set it to some random texture/noise that effect will growth from)

F
  Chemicals feed rate

K
  Chemicals kill rate






************************************************************
Surface Curl Noise
************************************************************

Creates direction vectors from a noise texture that curls on surface (follows in curl pattern) 

.. image:: images/surfacecurl1.PNG
.. image:: images/surfacecurl2.PNG

Surface Normal
  Normal directional vector from a surface that curl directional vectors will be aligned 

Vector Scale
  Scale of the direction vector 
  
Normalize Vector
  Normalizes direction vectors

4D Noise
  Adds time dimension to noise texture

W
  Time offset of noise
  
Noise Scale
  Scale of noise 

Noise Detail
  Detail of noise 

Noise Distortion
  Distortion of noise

Noise Offset
  Offsets noise texture

Epsilon
  Small value that offsets noise texture to sample noise from different directions to get directional vector (only change it if trying get curl noise on really small or really big sampling area)



************************************************************
Curl Noise 2D
************************************************************

Creates 2D direction vectors from a noise texture that curls (follows in curl pattern) 

.. image:: images/curl2dn.PNG
.. image:: images/curl2dn2.PNG

Vector Scale
  Scale of the direction vector 
  
Normalize Vector
  Normalizes direction vectors
  
Noise Scale
  Scale of noise 

Noise Detail
  Detail of noise 

Noise Distortion
  Distortion of noise

Noise Offset
  Offsets noise texture

Epsilon
  Small value that offsets noise texture to sample noise from different directions to get directional vector (only change it if trying get curl noise on really small or really big sampling area)



************************************************************
Curl Noise 3D
************************************************************

Creates 3D direction vectors from a noise texture that curls (follows in curl pattern) 

.. image:: images/curl3d1.PNG
.. image:: images/curl3d.PNG

Vector Scale
  Scale of the direction vector 
  
Normalize Vector
  Normalizes direction vectors

4D Noise
  Adds time dimension to noise texture

W
  Time offset of noise
  
Noise Scale
  Scale of noise 

Noise Detail
  Detail of noise 

Noise Distortion
  Distortion of noise

Noise Offset
  Offsets noise texture

Epsilon
  Small value that offsets noise texture to sample noise from different directions to get directional vector (only change it if trying get curl noise on really small or really big sampling area)







