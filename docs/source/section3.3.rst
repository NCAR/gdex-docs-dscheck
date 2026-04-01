
.. _section3.3:

3.3 - Check Process Actions
=================================

Delayed mode command executions recorded in GDEXDB are automatically started,
or restarted, by the common 'dscheck' daemon. Running commands can be interrupted
at any time and the child processed of the interrupted commands are also cleaned up.
The status of the current check records can be gathered and emailed to a specialist.

Here are the actions for process checks:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Process Check <section3.3.1>`
     - start a command from its information recorded in 'dscheck'
   * - :ref:`Interrupt Check <section3.3.2>`
     - interrupt a running command for given check record and clean the child processes
   * - :ref:`Email Check <section3.3.3>`
     - email a specialist for the status of the current check records

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.3.1
   section3.3.2
   section3.3.3



| :ref:`Back to Top <section3.3>`
| :ref:`Back to Table of Contents <index>`
