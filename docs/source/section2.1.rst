
.. _section2.1:

2.1 - Quick Start
=================================

Show the full document, paged through 'more':

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck

Show the description of a single option:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck -h :ref:`-AC <AC>`

List your own daemon control records:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-GD <GD>`

List your own active check records:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-GC <GC>`

Add a deferred run of a script on PBS:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-AC <AC>` -CM myscript.sh :ref:`-HN <HN>` PBS

Email yourself the status of all your active checks:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-EC <EC>`

Start the dscheck daemon (typical for the operator):

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-PC <PC>` -DM start



| :ref:`Back to Top <section2.1>`
| :ref:`Back to Table of Contents <index>`
