
.. _section3.3.1:

3.3.1 - Process Check
=================================


.. _PC:

Action Option -**PC** (-**ProcessCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

drives command execution from check records, in
either daemon mode or non-daemon mode.

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
     - run as a background process; suppress screen output.
   * - :ref:`-(CP|CheckPending) <CP>`
     - identify and kill long-pending checks.
   * - :ref:`-(LO|LogOn) <LO>`
     - enable detailed logging in daemon mode.
   * - :ref:`-(NC|NoCommand) <NC>`
     - do not actually execute remote commands (dry run).
   * - :ref:`-(WU|WithdsUpdt) <WU>`
     - in non-daemon mode, add check records for due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ actions configured in update controls.
   * - :ref:`-(WR|WithdsRqst) <WR>`
     - in non-daemon mode, add check records for `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ records due to be built or purged.

Daemon mode (:ref:`-DM <DM>` start):

.. list-table::
   :widths: auto
   :header-rows: 1
 The daemon sleeps for :ref:`-WI <WI>` seconds (default 120) between cycles. Each cycle, it adds due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ check records, then starts or restarts checks on hosts chosen by daemon control priorities. :ref:`-DM <DM>` stop, :ref:`-DM <DM>` logon, and :ref:`-DM <DM>` logoff stop the daemon, enable detailed logging, and disable detailed logging respectively.

Non-daemon mode:

.. list-table::
   :widths: auto
   :header-rows: 1
 Without :ref:`-DM <DM>`, dscheck processes the current set of check records once. :ref:`-WU <WU>` and :ref:`-WR <WR>` must be set explicitly if you want due 'dsupdt'/'dsrqst' work to be added before processing. :ref:`-CI <CI>` restricts processing to specific check indices.



| :ref:`Back to Top <section3.3.1>`
| :ref:`Back to Table of Contents <index>`
