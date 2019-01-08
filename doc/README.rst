========
Flatmaps
========

--------
Overview
--------

Use concepts from geographical map viewers (Google Maps, Open Street Maps, etc) when viewing flatmaps:

* tiles
* layers
* zoom/pan
* select related
* etc.

Components
==========

* Map specification
* Map preparation/layout
* Map display

	- User interaction

See :ref:`SPECIFICATION:Details`

Connections
===========

* Between Components.
* Directed -- ``from`` a source ``to`` a target.
* Possible to route their paths, including bundling together those that run alongside each other (edge bundling).


Objects
=======

Properties
----------

* Size/area
* Shape
* Position
* Containment

Locating objects
----------------

* Geographical mapping systems have well defined coordinate systems and transformations between them.
* **We don't.**
* Containment and other topological relationships are important for placing objects on our maps.

Layers
------

* Hierarchy
* Base coordinates determined by base layer.

.. code-block:: xml

	<component id="l0">
		<component id="l1">
			<component id="c1"/>
			<component id="c2"/>
		</component>
		<component id="l2">
			<component id="c3"/>
			<component id="c4"/>
		</component>
		<component id="c5"/>
	</component>



Are ``layers`` just part of map presentation/viewing?? Do they represent semantic grouping??

-------------
Visualization
-------------

* `The visualizations transforming biology <https://www.nature.com/news/the-visualizations-transforming-biology-1.20201>`_


------------
Related Work
------------

NaviCell
========

* https://bmcsystbiol.biomedcentral.com/articles/10.1186/1752-0509-7-100.
* Uses Google Maps API to display tiles.
* Semantic zooming:

	- Provide a readable image of the visible part of the map at each zoom level (`Zomit: biological data visualization and browsing <https://academic.oup.com/bioinformatics/article/14/9/807/259557>`_).
	- Details vanish progressively when zooming out with individual objects or groups of objects replaced by representations more suitable for the current scale.
	- Four different zoom levels where each level is double the size of the preceding level:

		- Top-level
		- Pruned
		- Details hidden
		- Detailed


CellNetVis
==========

* https://www.biorxiv.org/content/biorxiv/early/2017/07/13/163410.full.pdf
* http://bioinfo03.ibi.unicamp.br/lnbio/IIS2/cellnetvis/index.html


NetyPyNE
========

* http://www.netpyne.org/


OpenLayers
==========

* https://openlayers.org
* https://openlayers.org/en/latest/examples/
* https://openlayersbook.github.io/


DE-9IM
======

* https://en.wikipedia.org/wiki/DE-9IM


Javascript libraries
====================

* `Cytoscape.js <http://js.cytoscape.org/>`_
* `JSTS <http://bjornharrtell.github.io/jsts/>`_
* `SVG.js <https://svgjs.com/docs/3.0/>`_
