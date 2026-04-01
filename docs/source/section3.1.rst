
.. _section3.1:

3.1 - Daemon Control Actions
=================================

A daemon control record for a command, a specialist and a hostname is used to
configure how many concurrent processes the specified command can be executed
for the specialist on specified hostname, and the priority the the hostname is
picked to start the command. A running centralized daemon reads this record
periodically in case the configuration is changed while the daemon is still
running, so that specialists can reset the values in daemon control records to
change the behave of dscheck daemon dynamically without shutting the daemon down.

Daemon control information can be created, modified and viewed via Actions
included in this section:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Set Daemon Control <section3.1.1>`
     - create and modify daemon control information for specified specialists, commands and hostnames
   * - :ref:`Get Daemon Control <section3.1.2>`
     - retrieve information of existing daemon controls
   * - :ref:`Delete Daemon Control <section3.1.3>`
     - delete one or multiple daemon control records

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
