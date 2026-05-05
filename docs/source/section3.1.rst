
.. _section3.1:

3.1 - Daemon Control Actions
=================================

A daemon control record answers three questions for the dscheck daemon:

* Whose checks?  (specialist login)
* For which command?  (utility program name, or 'ALL')
* On which host, at what concurrency, at what priority? (hostname, ProcessLimit, Priority)

Daemon controls are read by the daemon on every cycle, so changes take
effect without restarting the daemon. A specialist with no daemon control
records will have no checks started automatically.

Available actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Set Daemon Control <section3.1.1>`
     - create or modify daemon control records.
   * - :ref:`Get Daemon Control <section3.1.2>`
     - retrieve existing daemon control records.
   * - :ref:`Delete Daemon Control <section3.1.3>`
     - remove daemon control records by index.

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.1.1
   section3.1.2
   section3.1.3



| :ref:`Back to Top <section3.1>`
| :ref:`Back to Table of Contents <index>`
