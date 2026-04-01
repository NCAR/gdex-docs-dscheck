
.. _section3.3.2:

3.3.2 - Interrupt Check
=================================


.. _IC:

Action Option -**IC** (-**InterruptCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

interrupts checks whose commands are currently running
and also kills recursively all the child processes running under those
commands. Locks are cleaned too when the checks are interrupted.

| **dscheck** -(IC|InterruptCheck) [:ref:`Mode Option <mode3.3.2>`]
|            :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

.. _mode3.3.2:

:ref:`Mode option <section4>` that can be specified for this action:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(FI|ForceInterrupt) <FI>`
     - it must be present for this action to interrupt a check that is under processing.

It is mandatory to provide a check index to interrupt its command.



| :ref:`Back to Top <section3.3.2>`
| :ref:`Back to Table of Contents <index>`
