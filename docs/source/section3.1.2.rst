
.. _section3.1.2:

3.1.2 - Get Daemon Control
=================================


.. _GD:

Action Option -**GD** (-**GetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

retrieves daemon control information for given commands,
specialists or hostnames. Daemon control information of specified specialists
are retrieved if the specialist login names are provided. Without specified
condition, only the daemon control records set for the specialist who runs
**dscheck** are retrieved.

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

.. _mode3.1.2:

:ref:`Mode option <section4>` that can be specified for getting check control Action:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(FO|FormatOutput) <FO>`
     - format the column output with a fix width for all values of a given field

Use :ref:`Info option <section5>` :ref:`-FN <FN>` (-FieldNames) to specify what daemon control fields to be
retrieved. It defaults to all available fields if option :ref:`-FN <FN>` is not provided.

Valid field names of daemon controls and their corresponding :ref:`Info <section5>` option
names:

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

Daemon control information can be retrieved for specified specialist per option
:ref:`-SN <SN>` (-Specialist), and/or other conditions. :ref:`Info option <section5>` :ref:`-SN <SN>`, :ref:`-CM <CM>` and :ref:`-HN <HN>` accept
wildcard input of '%' for matching any number of characters.

If daemon control index is not given, **dscheck** gathers only the daemon control
records owned by the specialist who executes this getting daemon control Action.
To view daemon control records owned by another specialist, you need specify :ref:`Info <section5>`
option :ref:`-SN <SN>` (-Specialist). To view all control records, you simply provide option
:ref:`-SN <SN>` with value of 'ALL'.


.. _3.1.2_e2:

**EXAMPLE 2. To get all daemon control information currently set for you:**

dscheck GD



| :ref:`Back to Top <section3.1.2>`
| :ref:`Back to Table of Contents <index>`
