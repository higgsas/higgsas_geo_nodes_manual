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

.. image:: images/reactshow.png

T
  Time scale of the simulation (going above 1.5 simulation will become unstable)

Scale
  Scale of the grouth pattern

.. image:: images/diffsale.png


************************************************************
Image Points Stippling
************************************************************

Recreates image using point/dots for the gradiant shading using weighted voronoi technique 

.. image:: images/stipp1.JPG
.. image:: images/stipp2.JPG
.. image:: images/stipp3.JPG

**Setting up the solver**

- First open image of your choice 
- Connect **Initial Distribution View** to the **Group Output** or a viewer node
- Adjust **Min Brightness** and **Max Brightness** to best match gradient of the image 

.. image:: images/stippa1.JPG

- **Min Points Amount** and **Max Points Amount** controls density of points for bright and dark portions of the image. For the best results adjust **Min Points Amount** to get small amount of points in bright areas while keeping image contrast, can leave it to the default. **Max Points Amount** can be decreased if you have too many points in dark areas, preferably leave it default of 1

.. image:: images/stippa2.JPG
.. image:: images/stippa3.JPG

- **Min Distance** controls density in the dark areas, lower values will results in more points in dark areas. Be carefull not to set value too low, resulting in way too many points that will slow simulation significantly. For decent results aim total point count somewhere between 10k / 30k

- **Points Count** initial points count that points will be deleted using image brightness values. Preferably leave it to the default and only increase it if in some areas points are too sparse

**Simulation**

- After adjusted Initial Distribution settings, connect **Points Stippling Simulation** to the Group Output and rund the simulation

.. image:: images/stipps1.JPG
.. image:: images/stipps2.JPG

- Usually it will take about 50 frames to get stippling effect
- Instancing spheres on to points with small radius

.. image:: images/stipps3.JPG

- **Sharpness/Softness** controls the gradient of the points distribution, negatives values will results in sharper gradient cut off, positives values results in softer gradient. Preferably use the values in between 0 and 1

.. image:: images/stipps4.JPG
.. image:: images/stipps5.JPG
.. image:: images/stipps6.JPG

- **Sharpness Scale** controls gradient difference between bright and dark ares. If set **Sharpness Scale** to 0, points in bright ares will not apear. Leave it default value 0.01 

.. image:: images/stipps7.JPG

- **Grid Resolution** used to calculate weighted voronoi coordinates for points directions to move. For better quality of points distribution, grid resolution can be increased. Make sure keep keep it around 1200 / 2000, higher grid number will make simulation significantly slower

- **Color** attribute can be use for controlling points scale from image texture for better effect

.. image:: images/stipps8.JPG

- Stippling effect can be inverted by inverting **Min Brightness** and **Max Brightness** values

.. image:: images/stipps9.JPG

- To apply the simulation, apply geo nodes modifier with realized circle instances, or convert points to vertices by using **Points to Vertices** nodes and apply the geo nodes modifier

.. tip::
    You can use fill curve trick to convert points to triangular mesh 
    
    .. image:: images/stipps10.JPG


************************************************************
Triangle Mesh Circle Packing
************************************************************

Relaxes triangulated mesh to fit tangent circles using simulation


.. image:: images/tmeshc.PNG
.. image:: images/tmeshc1.PNG

Time Steps
  Number of simulation steps per frame

Relax Strenght 
  The amount of relaxation per step. Going above 1 can create unstable simulation. Value bellow 1 will slow down the simulation for more stable relaxations, but it slower convergence to packed circles. Preferably leave at 1
  




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







