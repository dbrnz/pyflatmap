=======
Details
=======

-------------
Specification
-------------

* Python based DSL. ``pyflatmap`` Python package:

.. code-block:: python

	import FlatMap, Layer, Component, Style, Geometry from PyFlatMap

FlatMaps
========

.. code-block:: python

	fm = FlatMap()

	# Maps are scalable
	fm.aspect_ratio = 1.0

	# How is background image scaled?
	# If no width/height then image determines them?

	fm.background = Background('xxx.svg')
	fm.background = Background('xxx.png')

Layers
------

.. code-block:: python

	# A map has layers, initially just the base layer (layer 0)
	# Layers are accessed by index

	fm.add_layer(Layer())
	fm.layer[n]   # n >= 0

	# Layer visibility, order, opacity
	# Can any Layer have a background image??

Components
==========

.. code-block:: python

	c = Component()
	c.style = Style()
	c.geometry = Geometry()

	# Do Components belong to a Layer or to the FlatMap??
	fm.add_component(c)
	fm.layer[1].add_component(c) # ??

	# Component hierarchy
	c1 = Component(children[Component(), Component()])
	c.add_child(c1)
	c.add_children([])


Connections
===========

.. code-block:: python

	Connection(c1, c2)


Diagrams
========

.. code-block:: python

	# A Diagram represents the visual representation of a FlatMap
	# A FlatMap may be displayed in different Diagrams

	d = Diagram()

	# Size (width, height) are part of displaying the map
	# In what units?
	#d.width, d.height # or d.size = (w, h)



--------
Creating
--------

* Editing tools
* Automatically via software


----------
Generation
----------

* Convert from DSL specification to JSON (+ CSS + JS)


-------
Viewing
-------

* Web app takes generated diagram and allows a user to interact with it.


--------
Creating
--------

Editing tools
=============

