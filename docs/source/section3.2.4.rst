
.. _section3.2.4:

3.2.4 - Unlock Check
=================================


.. _UL:

Action Option -**UL** (-**UnLockCheck**) (Alias: -**UnLock**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(Alias: -UnLock), unlocks check records that their
commands aborted abnormally during processes.

Process ID and computer hostname are saved in a check record when the recorded
command is running. If the process aborts abnormally, the PID and hostname may
sometimes be not cleaned properly. Use this action to clean up the locking
information to allow the command to be reprocessed or purged.

| **dscheck** -(:ref:`-UL <UL>`|UnLockCheck)
|             :ref:`-(CI|CheckIndex) <CI>` CheckIndices
|            [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

It is mandatory to provide a check index to remove lock on a recorded command.



| :ref:`Back to Top <section3.2.4>`
| :ref:`Back to Table of Contents <index>`
