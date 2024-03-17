Distribution
===================================

************************************************************
3D Points Grid
************************************************************

Distributes points in 3d grid

.. image:: images/3d_p_g.PNG

Size
  Size of the grid
  
Points X
  Amount of points in X axis
  
Points Y
  Amount of points in Y axis  
  
Points Z
  Amount of points in Z axis  
  
Radius
  Radius of the points



************************************************************
Array
************************************************************

Creates array of the geometry

.. image:: images/array.PNG

Count
  Amount that geometry will duplicated
  
**Constant Offset**

- **Off:** Offsets geometry from its bonding box
- **On:** Offsets geometry from its center

Translation
  Offsets array
  
Rotation
  Rotates geometry



************************************************************
Circle Packing
************************************************************

Creates circle packing by removing points that inside the radius each interation. The more points you have the better circle packing will be, aim it around 50k/100k points

.. image:: images/cipack.PNG
.. image:: images/cipack1.PNG

Iterations
  Iterations of the circle packing. If you have a lot of points or min/max radius set to low values increase Iterations
  
Min Radius
  Min radius of the circle
  
Max Radius
  Max radius of the circle

**Random/Max Radius**

- **Random** Each interation sets circle radius to random value, and will clamp it with existing circles that it won't overlap. It will give more randomized circles, but with bigger gaps
- **Max Radius** Each interation sets circle radius to max radius to the closest existing circle. It will tighter gaps between circles but with more uniform circles

**Random/Index Order**

- **Random** Selects each point randomly. Will result in more randomized circles with bigger gaps
- **Index Order** Selects each point by its index. Will result in more tighter packing. Note that points indices depending on how points was created

.. image:: images/cipack4.PNG
.. image:: images/cipack5.PNG

Seed
  Seed of setting random radius between min and max to circles

Fit in Mesh
  Fits circles inside the mesh that won't go past boundary

Mesh
  Mesh for boundary

**2D Boundary/3D Surface**

- **2D Boundary** Makes circles radius equal boundary edge

.. image:: images/cipack2.PNG
.. image:: images/cipack3.PNG

- **3D Surface** Makes circles/sphere radius equal to surface boundary

.. image:: images/cipack6.PNG
.. image:: images/cipack7.PNG

Packing using noise or the texture

.. image:: images/cipack8.PNG



************************************************************
Circular Array
************************************************************

Creates array of the geometry on a circle

.. image:: images/c_array.PNG

Count
  Amount that geometry will duplicated on a circle
  
Radius
  Radius of the circle
  
Circle Rotation
  Rotates circle
  
Rotation
  Rotates geometry orientation
  
Scale
  Scale of the geometry
  
Pick Instance
  Picks instaces from the instances list or collection

.. image:: images/array_p.PNG

Instance Index
  Index of the instances list
  


************************************************************
Distribute Points in Volume
************************************************************

Distributes points inside mesh volume

.. image:: images/dist_p_i_v.PNG

Density
  Amount of points inside volume
  
Radius
  Radius of the points
  
Seed
  Seed of the random distribution



************************************************************
Distribute Points on Edges
************************************************************

Distributes Points on mesh edges

.. image:: images/d_p_o_e.PNG

Count
  Amount of points
  
Radius
  Radius of the points
  
Seed
  Seed of the random distribution
  
Selection
  Selection of the edges that points will be distributed



************************************************************
Homogeneous Disk
************************************************************

Evenly distributes points on to disk

.. image:: images/h_d.PNG
.. image:: images/h_d_2.PNG

Distance
  Distance between distributed points
  
Radius
  Radius of the disk
  
Scale
  Scale of the points gap
  
Pole Distance
  Increases gap on the disk pole
  
.. image:: images/h_d_p_d.PNG

Rotation
  Rotation
  
Scale
  Points gap distance



************************************************************
Homogeneous Sphere
************************************************************

Evenly distributes points on to sphere

.. image:: images/h_s.PNG
.. image:: images/h_s_2.PNG

Distance
  Distance between distributed points
  
Radius
  Radius of the sphere
  
Scale
  Scale of the points gap
  
Poles Distance
  Increases gap on the sphere poles
  
.. image:: images/h_s_p_d.PNG

Rotation
  Rotation
  
Scale
  Points gap distance



************************************************************
Phyllotaxis Disk
************************************************************

Distributes points in phyllotaxy arrangement

.. image:: images/phy_d.PNG

Count
  Count of points
  
Radius
  Radius of the disk
  
Angle
  Angle of spiral 
  
Even Spacing
  Space points evenly
  
.. image:: images/phy_d2.PNG
  
Even Pole
  Offsets first point for more even distribution
  
Points Radius
  Radius of the points



************************************************************
Phyllotaxis Profile Surface
************************************************************

Distributes points in phyllotaxys arrangement on the surface from the profile curve

.. image:: images/phyprof.JPG

Petal Area
  Density of phyllotaxys distribution
  
Step Size
  Step size for choosing which petal point are valid for the ddistribution. Smaller value more accurate results
  
Axis
  Axis of the distribution
  
Center
  Center of the distribution



************************************************************
Phyllotaxis Sphere
************************************************************

Distributes points in phyllotaxy arrangement on sphere

.. image:: images/phy_s.PNG

Count
  Count of points
  
Radius
  Radius of the disk
  
Angle
  Angle of spiral 
  
Even Pole
  Offsets first point for more even distribution
  
U Parameter
  Cuts sphere along U coordinate
  
.. image:: images/phy_s2.PNG

Points Radius
  Radius of the points



************************************************************
Random Points
************************************************************

Randomly distributes points

.. image:: images/random_points.PNG

Spherical
  **On:** Random points will be distributed into sphere  
  
.. image:: images/random_points_s.PNG

Count
  Count of points
  
Size
  Size of the points distrubution
  
Radius
  Radius of the point
  
Seed
  Seed of the random distribution



************************************************************
Volume Points Grid
************************************************************

Distributes points inside mesh volume in grid pattern

.. image:: images/v_p_g.PNG

Density
  Amount of points inside volume
  
World Space
  **On:** Points dstribution stays at world coordinates if mesh moving
  