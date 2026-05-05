
.. _section3.2:

3.2 - Check Actions
=================================

Check records are created automatically by the dscheck daemon for due
`dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ actions. Other commands - including `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_ calls
and any specialist-defined script - are added manually with :ref:`-AC <AC>`.

Available actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Add Check <section3.2.1>`
     - add a check record for a deferred command.
   * - :ref:`Get Check <section3.2.2>`
     - retrieve check records and field values.
   * - :ref:`Delete Check <section3.2.3>`
     - delete check records that should no longer run.
   * - :ref:`Unlock Check <section3.2.4>`
     - clear leftover lock information after an abnormal exit.

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.2.1
   section3.2.2
   section3.2.3
   section3.2.4



| :ref:`Back to Top <section3.2>`
| :ref:`Back to Table of Contents <index>`
