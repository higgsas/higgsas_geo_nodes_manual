Installation
===================================





************************************************************
Adding node groups to the Assect Browser
************************************************************

Go to``Edit/Preferences/File Paths/Asset Libraries`` and add node group :guilabel:`.blend` file to the Path folder, and press :guilabel:`Safe Preferences`

.. image:: images/instal_asset1.PNG

Now node groups will accessible in :guilabel:`Asset Browser`

.. image:: images/instal_asset2.PNG

.. warning::
    Node groups are not searchable inside Geometry Nodes editor



************************************************************
Linking node groups to the Startup File
************************************************************

- Open :guilabel:`Blender`
- Go to ``File/Link``

.. image:: images/instal1.png

- Navigate to where node group file :guilabel:`.blend` is located and double click it

.. image:: images/instal2.png

- Double click :guilabel:`NodeTree` folder 

.. image:: images/instal3.png

- Select all nodes (ALT-A) and press :guilabel:`Link`

.. image:: images/instal4.png

Go to ``File/Defaults/Save Startup File`` and press :guilabel:`Save Startup File`

.. image:: images/instal5.png

Now the node groups will be linked to the startup file, so everytime you open :guilabel:`Blender` , node groups will be available and searchable inside Geomety Nodes editor.

.. warning::
    Existing :guilabel:`Blender` files won't have node groups linked, you will have to re-link it
