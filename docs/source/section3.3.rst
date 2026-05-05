
.. _section3.3:

3.3 - Check Process Actions
=================================

The dscheck daemon starts and restarts deferred commands automatically.
Operators (and, in non-daemon mode, specialists) can also drive command
execution from the command line, interrupt running commands, and email
status summaries.

Available actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Process Check <section3.3.1>`
     - start commands from check records (daemon or non-daemon mode).
   * - :ref:`Interrupt Check <section3.3.2>`
     - stop a running command and recursively kill its process tree.
   * - :ref:`Email Check <section3.3.3>`
     - email a specialist the current status of one or more check records.

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.3.1
   section3.3.2
   section3.3.3



| :ref:`Back to Top <section3.3>`
| :ref:`Back to Table of Contents <index>`
