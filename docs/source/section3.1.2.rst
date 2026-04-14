
.. _section3.1.2:

3.1.2 - Get Daemon Control
=================================


.. _GD:

Action Option -**GD** (-**GetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

retrieves daemon control records for specified commands,
specialists, or hostnames. If no conditions are provided, only records owned
by the specialist running **dscheck** are returned.

| **dscheck** -(GD|GetDaemon) [:ref:`Mode Option <mode3.1.2>`]
|           [:ref:`-(FN|FieldNames) <FN>` FieldNameString]
|           [:ref:`-(DI|DaemonIndex) <DI>` controlIndices]
|           [:ref:`-(CM|Command) <CM>` UtilityProgramNames]
|           [:ref:`-(SN|Specialist) <SN>` DECSSpecialists]
|           [:ref:`-(HN|HostName) <HN>`  HostMachineName]
|           [:ref:`-(PL|ProcessLimit) <PL>` MaxNumberOfProcesses]
|           [:ref:`-(PO|Priority) <PO>` ProcessPriority]
|           [:ref:`-(OF|OutputFile) <OF>` OutputFileName]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

Available mode option:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(FO|FormatOutput) <FO>`
     - formats each column to a uniform fixed width

Use :ref:`-FN <FN>` (-FieldNames) to specify which daemon control fields to retrieve.
Defaults to all available fields when :ref:`-FN <FN>` is not provided.

Valid daemon control field names and their corresponding :ref:`Info options <section5>`:

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Names
     - :ref:`Info Options <section5>`
     - Descriptions
   * - I
     - :ref:`-(DI|DaemonIndex) <DI>`
     - daemon control index
   * - C
     - :ref:`-(CM|Command) <CM>`
     - command names of utility programs
   * - H
     - :ref:`-(HN|Hostname) <HN>`
     - computer hostname
   * - M
     - :ref:`-(MH|MatchHost) <MH>`
     - Flags to control hostname match
   * - S
     - :ref:`-(SN|Specialist) <SN>`
     - DECS specialist the daemon set for
   * - P
     - :ref:`-(PL|ProcessLimit) <PL>`
     - Max check count to be processed at the same times
   * - O
     - :ref:`-(PO|Priority) <PO>`
     - host priority a specified command to start on

Results can be filtered by specialist (:ref:`-SN <SN>`), and/or other conditions.
Options :ref:`-SN <SN>`, :ref:`-CM <CM>`, and :ref:`-HN <HN>` accept the '%' wildcard.

To view records owned by another specialist, provide their login name via
:ref:`-SN <SN>` (-Specialist). To view all control records, use :ref:`-SN <SN>` ALL.


.. _3.1.2_e2:

**EXAMPLE 2. To retrieve all daemon control records set for you:**

dscheck GD



| :ref:`Back to Top <section3.1.2>`
| :ref:`Back to Table of Contents <index>`
