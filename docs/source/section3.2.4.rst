
.. _section3.2.4:

3.2.4 - Unlock Check
=================================


.. _UL:

Action Option -**UL** (-**UnLockCheck**) (Alias: -**UnLock**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

clears stale lock information from
a check record.

When a check is being processed, the running process ID and hostname are
written into the check record. If the process aborts abnormally, that
lock may not be cleared. Unlocking a check allows it to be reprocessed
or purged.

| **dscheck** -(UL|UnLockCheck)
|            :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

:ref:`-CI <CI>` is required.



| :ref:`Back to Top <section3.2.4>`
| :ref:`Back to Table of Contents <index>`
