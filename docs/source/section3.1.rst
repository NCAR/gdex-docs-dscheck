
.. _section3.1:

3.1 - Daemon Control Actions
=================================

A daemon control record configures how many concurrent processes of a given
command a specialist may run on a specified host, and the priority order in
which hosts are selected. The centralized daemon reads these records
periodically, so specialists can update daemon control values at any time
without restarting the daemon.

Daemon control records are managed with the following actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Set Daemon Control <section3.1.1>`
     - create or modify daemon control records for specified specialists, commands, and hostnames
   * - :ref:`Get Daemon Control <section3.1.2>`
     - retrieve existing daemon control information
   * - :ref:`Delete Daemon Control <section3.1.3>`
     - remove one or more daemon control records

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.1.1
   section3.1.2
   section3.1.3

**Appendix A: List of Examples**

- :ref:`A.1. Action Option -SD (-SetDaemon) <3.1.1_e1>`
- :ref:`A.2. Action Option -GD (-GetDaemon) <3.1.2_e2>`



| :ref:`Back to Top <section3.1>`
| :ref:`Back to Table of Contents <index>`
