
.. _section3.3:

3.3 - Check Process Actions
=================================

Deferred commands recorded in GDEXDB are started (or restarted) automatically
by the centralized **dscheck** daemon. Running commands can be interrupted at any
time, and all child processes of the interrupted command are also cleaned up.
The current check status can be gathered and emailed to a specialist.

Available actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Process Check <section3.3.1>`
     - start a command from its check record, in daemon or non-daemon mode
   * - :ref:`Interrupt Check <section3.3.2>`
     - interrupt a running command for a given check record and kill all its child processes
   * - :ref:`Email Check <section3.3.3>`
     - email a specialist the current status of their check records

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.3.1
   section3.3.2
   section3.3.3



| :ref:`Back to Top <section3.3>`
| :ref:`Back to Table of Contents <index>`
