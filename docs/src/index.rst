.. ops_vis documentation master file, created by
   sphinx-quickstart on Sat Aug 22 13:35:16 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to ``ops_vis``'s documentation!
=======================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   plot_model
   plot_defo
   plot_mode_shape
   section_force_diagram_2d
   section_force_diagram_3d
   plot_stress_2d
   plot_extruded_model_rect_section_3d
   anim_defo
   anim_mode
   plot_fiber_section
   fib_sec_list_to_cmds
   quad_sig_out_per_node
   examples


The ``ops_vis`` postprocessing and plotting module is meant to be used
with Opensees Python (OpenSeesPy). First read the
`OpenSeesPy documentation <https://openseespydoc.readthedocs.io>`_
before geting started with ``ops_vis``.

This module can be mainly useful for students when learning the
fundamentals of structural analysis (interpolated deformation of frame
structures (static images or animations), section force distribution
of frame structures, stress distribution in triangle, quadrilateral 2d
elements, orientation of frame members in 3d space, fibers of a cross
section, static and animated eigenvalue mode shapes etc.). This way,
we can lower the bar in teaching and learning OpenSees at earlier
years of civil engineering studies. However the visualization features
for OpenSees can also be helpful for research studies.

Note that OpenSeesPy contains another plotting module called
``Get_Rendering``, however ``ops_vis`` is an alternative with some
distinct features, which for example allow us to plot:

- interpolated deformation of frame structures,
- stresses of triangular and (four, eight and nine-node) quadrilateral
  2d elements (calculation of Huber-Mieses-Hencky equivalent stress,
  principal stresses),
- fibers of cross-sections,
- models with extruded cross sections
- animation of mode shapes.

To use ``ops_vis`` in OpenSees Python
scripts, your ``.py`` file should start as follows: ::

	import openseespy.opensees as ops
	import ops_vis as opsv
	import matplotlib.pyplot as plt

	# ... your OpenSeesPy model and analysis commands ...
	opsv.plot_model()
	opsv.plot_defo()

The main commands related to various aspects of OpenSees model
visualization are as follows:

#. :doc:`plot_model`
#. :doc:`plot_defo`
#. :doc:`plot_mode_shape`
#. :doc:`section_force_diagram_2d`
#. :doc:`section_force_diagram_3d`
#. :doc:`plot_stress_2d`
#. :doc:`plot_extruded_model_rect_section_3d`
#. :doc:`anim_defo`
#. :doc:`anim_mode`
#. :doc:`plot_fiber_section`

Helper functions include:

#. :doc:`fib_sec_list_to_cmds`
#. :doc:`quad_sig_out_per_node`

For examples go to: :doc:`examples`.

Notes:

- matplotlib's ``plt.axis('equal')`` does not work for 3d plots
  therefore right angles are not guaranteed to be 90 degrees on the
  plots

- ``plot_fiber_section`` is inspired by Matlab ``plotSection.zip``
  written by D. Vamvatsikos available at
  http://users.ntua.gr/divamva/software.html
