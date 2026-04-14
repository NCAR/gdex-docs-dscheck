
.. _section3.3.1:

3.3.1 - Process Check
=================================


.. _PC:

Action Option -**PC** (-**ProcessCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

starts commands from check records in daemon or
non-daemon mode. Check indices may be specified in non-daemon mode.

| **dscheck** -(PC|ProcessCheck) [:ref:`Mode Options <mode3.3.1>`]
|           [:ref:`-(CI|CheckIndex) <CI>` CheckIndices]
|           [:ref:`-(DM|DaemonMode) <DM>` (start|stop|logon|logoff)]
|           [:ref:`-(LH|LocalHost) <LH>` [LocalHostname]]
|           [:ref:`-(WI|WaitInterval) <WI>` WaitIntervalInSeconds]
|           [:ref:`-(MT|MaxrunTime) <MT>` MaximumRunTimeInSeconds]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

Available mode options:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(BG|BackGround) <BG>`
     - runs as a background process, suppressing screen output and errors
   * - :ref:`-(CP|CheckPending) <CP>`
     - checks and kills long-pending checks
   * - :ref:`-(LO|LogOn) <LO>`
     - enables detailed logging in daemon mode
   * - :ref:`-(NC|NoCommand) <NC>`
     - suppresses remote command execution
   * - :ref:`-(WU|WithdsUpdt) <WU>`
     - in non-daemon mode, adds check records for due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ actions configured in update control records
   * - :ref:`-(WR|WithdsRqst) <WR>`
     - in non-daemon mode, adds check records for `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ records due to be built or purged

In daemon mode, **dscheck** sleeps for two minutes (120 seconds by default,
or as configured via :ref:`-WI <WI>`) between processing cycles. On each wake-up, it
first adds due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ check records, then starts or restarts
commands from check records according to the host priorities set in daemon
controls.

In non-daemon mode, :ref:`Mode options <section4>` :ref:`-WU <WU>` and :ref:`-WR <WR>` must be present for due
`dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ actions to be added to check records. All current
check records (unless indices are specified) are then processed on machines
according to the daemon control configuration.



| :ref:`Back to Top <section3.3.1>`
| :ref:`Back to Table of Contents <index>`
