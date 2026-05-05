
.. _section3.1.1:

3.1.1 - Set Daemon Control
=================================


.. _SD:

Action Option -**SD** (-**SetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

creates or modifies daemon control records in GDEXDB
for given specialist login names, commands, and hostnames. One or many
records can be set per invocation.

| **dscheck** -(SD|SetDaemon) [:ref:`Mode Option <mode3.1.1>`]
|           [:ref:`-(DI|DaemonIndex) <DI>` controlIndices]
|           [:ref:`-(CM|Command) <CM>`  UtilityProgramNames]
|           [:ref:`-(SN|Specialist) <SN>` DECSSpecialists]
|           [:ref:`-(HN|HostName) <HN>`  HostMachineNames]
|           [:ref:`-(MH|MatchHost) <MH>`  FlagToMatchHostname]
|           [:ref:`-(PL|ProcessLimit) <PL>` MaxNumberOfProcesses],
|           [:ref:`-(PO|Priority) <PO>` HostListOrder]

Available mode option:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(ND|NewDaemon) <ND>`
     - add a new daemon control record (required when the daemon index is 0).

An existing record matching the (specialist, command, hostname) triple
is updated in place. To create a new record, supply daemon index 0 and
the :ref:`-ND <ND>` mode option; this guards against creating records by accident.
The (specialist, command, hostname) triple must be unique.

Special hostnames and commands:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - HN = PBS
     - submit the command to the PBS batch system.
   * - CM = ALL
     - apply to any command not otherwise configured for this specialist.



| :ref:`Back to Top <section3.1.1>`
| :ref:`Back to Table of Contents <index>`
