
.. _section3.2.4:

3.2.4 - Unlock Check
=================================


.. _UL:

Action Option -**UL** (-**UnLockCheck**) (Alias: -**UnLock**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

unlocks check records whose commands
aborted abnormally during processing.

When a command is running, its process ID and hostname are saved in the
check record. If the process aborts abnormally, this lock information may
not be cleared properly. Use this action to remove the lock so the command
can be reprocessed or purged.

| **dscheck** -(UL|UnLockCheck)
|            :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

A check index is required to unlock a recorded command.



| :ref:`Back to Top <section3.2.4>`
| :ref:`Back to Table of Contents <index>`
