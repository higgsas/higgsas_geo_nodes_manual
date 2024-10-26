Image
===================================

************************************************************
Image Box Mapping  
************************************************************

Map image on mesh using box mapping method 

.. image:: images/box_map.png

Image
  Input of the image that will be box mapped on the mesh
  
Blend
  Blends between seams

.. image:: images/box_map2.png

Translation
  Translation of box mapping
  
Rotation
  Rotation of box mapping
  
Scale
  Scale of box mapping



************************************************************
Image Dithering
************************************************************

Converts image gray scale values to single black and white values

.. image:: images/imgdit.JPG
.. image:: images/imgdit6.JPG

Image
  Image input
  
Resoliution Scale
  Grid resolution scale from image pixels
  
Floyd-Steinberg

.. image:: images/imgdit.JPG

Sierra

.. image:: images/imgdit2.JPG

Ordered 2x2

.. image:: images/imgdit3.JPG

Ordered 4x4

.. image:: images/imgdit4.JPG

Ordered 8x8

.. image:: images/imgdit5.JPG

Average/Lightness/Saturation/Hue/Red/Blue/Green
  Converts image color to specified channel

Gamma Correction
  Gamma corrects image values

Contrast Min
  Min contrast control of the image

Contrast Max
  Max contrast control of the image

Brightness Min
  Min brightness control of the image

Brightness Max
  Min brightness control of the image

Frame
  Current frame of image/video

.. tip::
    To correctly render the image:
    
    - Set camera to Orthographic mode 
    - Set scene resolution that matches image. Node outputs image Width and Height to help set scene resoliution 
    - Use Cycles render endgine with sample of 1 to get most accurate results. Samples above 1 will create blury pixels 
    
    .. image:: images/imgsort4.JPG



************************************************************
Image Pixel Sorting
************************************************************

Sorts image pixel values on rows or columns

.. image:: images/imgsort.JPG
.. image:: images/imgsort2.JPG

Image
  Image input
  
Resoliution Scale
  Grid resolution scale from image pixels
  
Vertical/Horizontal
  Sorts pixels values in vertical strips or horizontal

Frame
  Current frame of image/video

Threshold - Lightness/Saturation/Hue/Red/Blue/Green
  Image grey scale channels that will be used by Treshhold

.. image:: images/imgsort3.JPG

Threshold
  Threshold selection where pixel sorting will happen

Invert Threshold
  Inverts threshold selection

Sorting - Lightness/Saturation/Hue/Red/Blue/Green
  Image grey scale channels that will be used for sorting pixels

Invert Sorting
  Invers sorting values

Randomize
  Randomly splits veritcal or horizontal sorting groups

.. image:: images/imgsort5.JPG
.. image:: images/imgsort6.JPG
  
Seed
  Seed of randomize

.. tip::
    To correctly render the image:
    
    - Set camera to Orthographic mode 
    - Set scene resolution that matches image. Node outputs image Width and Height to help set scene resoliution 
    - Use Cycles render endgine with sample of 1 to get most accurate results. Samples above 1 will create blury pixels 
    
    .. image:: images/imgsort4.JPG



************************************************************
Image to Ascii
************************************************************

Creates Ascii from image

.. image:: images/i_t_ac.jpeg

Image
  Image input
  
Resoliution
  Grid resolution of Ascii
  
Img Res X
  Input image X resolution

Img Res Y
  Input image Y resolution

Contrast Min
  Min contrast of the image values

Contrast Max
  Max contrast of the image values

Ascii
  Ascii characters that used for gradient values. Black/empty is space " " 
  
Frame
  Frame of the image input
  
Color Attribute
  Creates color attribute from image colors

.. tip::
    If you want to change font, you can by opening the node group (TAB key) and changing font in String to Curves node
    

