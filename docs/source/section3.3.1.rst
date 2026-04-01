
.. _section3.3.1:

3.3.1 - Process Check
=================================


.. _PC:

Action Option -**PC** (-**ProcessCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

starts process commands in check records in daemon or
non-daemon modes. Check indices can be specified if in non-daemon mode.

| **dscheck** -(PC|ProcessCheck) [:ref:`Mode Options <mode3.3.1>`]
|           [:ref:`-(CI|CheckIndex) <CI>` CheckIndices]
|           [:ref:`-(DM|DaemonMode) <DM>` (start|stop|logon|logoff)]
|           [:ref:`-(LH|LocalHost) <LH>` [LocalHostname]]
|           [:ref:`-(WI|WaitInterval) <WI>` WaitIntervalInSeconds]
|           [:ref:`-(MT|MaxrunTime) <MT>` MaximumRunTimeInSeconds]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

.. _mode3.3.1:

:ref:`Mode options <section4>` that can be specified for processing check Action:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(BG|BackGround) <BG>`
     - background process to turn off screen display for both standard outputs and errors
   * - :ref:`-(CP|CheckPending) <CP>`
     - Check and kill long pending checks
   * - :ref:`-(LO|LogOn) <LO>`
     - log detail for daemon mode
   * - :ref:`-(NC|NoCommand) <NC>`
     - does not issue remote commands if this :ref:`Mode option <section4>` is present
   * - :ref:`-(WU|WithdsUpdt) <WU>`
     - in non-daemon mode, add check records for due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ actions configured in update control records
   * - :ref:`-(WR|WithdsRqst) <WR>`
     - in non-daemon mode, add check records for `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ records due to be built or purged

In daemon mode, 'dscheck' sleeps two minutes (120 seconds as default), unless
provided  differently per option :ref:`-WI <WI>` (-WaitInterval), between processing check
records. Every time it wakes up, 'dscheck' first tries to add the due update
controls for command `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and add requests due to be built or purged for
command `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_, and then starts, or restarts, commands recorded in check
records on a computer according the priorities configured in the daemon controls.

In non-daemon mode, :ref:`Mode options <section4>` :ref:`-WU <WU>` and :ref:`-WR <WR>` must be present for due actions
of `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ to be added to check records. All current standing
check records, unless check indices are specified, are processed on machines
according to the configured information in daemon controls.



| :ref:`Back to Top <section3.3.1>`
| :ref:`Back to Table of Contents <index>`
