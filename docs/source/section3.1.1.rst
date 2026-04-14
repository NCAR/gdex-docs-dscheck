
.. _section3.1.1:

3.1.1 - Set Daemon Control
=================================


.. _SD:

Action Option -**SD** (-**SetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

creates or modifies daemon control records in GDEXDB for
given specialist login names, commands, and hostnames. One or more records
can be set per execution.

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
     - adds a new daemon control record to GDEXDB

If a daemon control record already exists in GDEXDB for the given specialist,
command, and hostname, the record is updated. A new record is created when the
daemon index is 0 and :ref:`Mode option <section4>` :ref:`-ND <ND>` (-NewDaemon) is present. The combination
of specialist login name, command name, and hostname must be unique for each
daemon control record.

Specify hostname 'PBS' to submit the command to the PBS batch control system.
If the specified command name is not found in the daemon control, the general
'ALL' configuration is used.


.. _3.1.1_e1:

**EXAMPLE 1. To set daemon control for schuster on PBS hosts for all commands, allowing up to 4 concurrent checks at priority 1 (lower number = higher priority), using input file daemon.ctl:**

| **dscheck** :ref:`-SD <SD>` :ref:`-ND <ND>` :ref:`-IF <IF>` daemon.ctl

Content of input file daemon.ctl:

.. code-block:: none

 DaemonIndex<:>Specialist<:>Command<:>Hostname<:>ProcessLimit<:>Priority<:>
 0<:>schuster<:>ALL<:>PBS<:>4<:>1<:>



| :ref:`Back to Top <section3.1.1>`
| :ref:`Back to Table of Contents <index>`
