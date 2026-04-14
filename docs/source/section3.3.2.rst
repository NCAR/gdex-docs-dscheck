
.. _section3.3.2:

3.3.2 - Interrupt Check
=================================


.. _IC:

Action Option -**IC** (-**InterruptCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

interrupts checks whose commands are currently
running and recursively kills all child processes. Locks are released when
the check is interrupted.

| **dscheck** -(IC|InterruptCheck) [:ref:`Mode Option <mode3.3.2>`]
|            :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

Available mode option:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(FI|ForceInterrupt) <FI>`
     - required to interrupt a check that is currently being processed

A check index is required to interrupt its command.



| :ref:`Back to Top <section3.3.2>`
| :ref:`Back to Table of Contents <index>`
