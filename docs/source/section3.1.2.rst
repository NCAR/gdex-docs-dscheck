
.. _section3.1.2:

3.1.2 - Get Daemon Control
=================================


.. _GD:

Action Option -**GD** (-**GetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

retrieves daemon control records. With no :ref:`Info <section5>`-option
filters, only records owned by the current specialist are returned.

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
     - pad each column to a uniform width for readability.

:ref:`-FN <FN>` (-FieldNames) selects which daemon-control fields to retrieve as a
string of single-letter codes. When :ref:`-FN <FN>` is omitted, all fields are
returned.

Field codes for daemon control records:

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Code
     - :ref:`Info Option <section5>`
     - Description
   * - I
     - :ref:`-(DI|DaemonIndex) <DI>`
     - daemon control index
   * - C
     - :ref:`-(CM|Command) <CM>`
     - command name of a utility program
   * - H
     - :ref:`-(HN|Hostname) <HN>`
     - computer hostname
   * - M
     - :ref:`-(MH|MatchHost) <MH>`
     - flag controlling hostname match
   * - S
     - :ref:`-(SN|Specialist) <SN>`
     - DECS specialist this control applies to
   * - P
     - :ref:`-(PL|ProcessLimit) <PL>`
     - max concurrent processes for this control
   * - O
     - :ref:`-(PO|Priority) <PO>`
     - host priority within this control

:ref:`-SN <SN>`, :ref:`-CM <CM>`, and :ref:`-HN <HN>` accept the SQL-style '%' wildcard. Pass :ref:`-SN <SN>` ALL to
retrieve every specialist's records (or a specific other specialist by
login name).

Example - retrieve all daemon control records owned by you:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-GD <GD>`



| :ref:`Back to Top <section3.1.2>`
| :ref:`Back to Table of Contents <index>`
