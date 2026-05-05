
.. _section3.3.2:

3.3.2 - Interrupt Check
=================================


.. _IC:

Action Option -**IC** (-**InterruptCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

stops a running command and recursively kills
its child processes. The check's lock is released as part of the
interrupt.

| **dscheck** -(IC|InterruptCheck) [:ref:`Mode Option <mode3.3.2>`]
|            :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

Available mode option:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(FI|ForceInterrupt) <FI>`
     - required to interrupt a check that is currently being processed; without it dscheck only warns.

:ref:`-CI <CI>` is required.



| :ref:`Back to Top <section3.3.2>`
| :ref:`Back to Table of Contents <index>`
