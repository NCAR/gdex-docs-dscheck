
.. _section3.1.1:

3.1.1 - Set Daemon Control
=================================


.. _SD:

Action Option -**SD** (-**SetDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

creates and modifies daemon control information into
GDEXDB for given specialist login names, commands, and hostnames of computers on
which the check commands are processed. One or multiple records can be set each
time.

| **dscheck** -(SD|SetDaemon) [:ref:`Mode Option <mode3.1.1>`]
|           [:ref:`-(DI|DaemonIndex) <DI>` controlIndices]
|           [:ref:`-(CM|Command) <CM>`  UtilityProgramNames]
|           [:ref:`-(SN|Specialist) <SN>` DECSSpecialists]
|           [:ref:`-(HN|HostName) <HN>`  HostMachineNames]
|           [:ref:`-(MH|MatchHost) <MH>`  FlagToMatchHostname]
|           [:ref:`-(PL|ProcessLimit) <PL>` MaxNumberOfProcesses],
|           [:ref:`-(PO|Priority) <PO>` HostListOrder]

.. _mode3.1.1:

:ref:`Mode option <section4>` that can be specified for this action include:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(ND|NewDaemon) <ND>`
     - sets a new daemon control record into GDEXDB

If information of a daemon control exists already in GDEXDB for a given specialist,
a command and a hostname, the daemon control record is modified; otherwise, a new
daemon control record is added if daemon index is 0 and :ref:`Mode option <section4>` :ref:`-ND <ND>` (-NewDaemon)
is present. Combination of specialist login name, command name and hostname of
computer must be unique for each daemon control record.

Specify host name 'PBS' for putting the command in the PBS batch control system. If
a specified command name is not found in the daemon control, the general 'dscheck'
configuration for command name 'ALL' is used.


.. _3.1.1_e1:

**EXAMPLE 1. Set daemon control information for schuster, all commands on PBS hosts, for maximum 4 checks can be processed at the same time with priority 1, the smaller the number the higher the priority is, via input file daemon.ctl:**

| **dscheck** :ref:`-SD <SD>` :ref:`-ND <ND>` :ref:`-IF <IF>` daemon.ctl

Content of input file daemon.ctl:

.. code-block:: none

 DaemonIndex<:>Specialist<:>Command<:>Hostname<:>ProcessLimit<:>Priority<:>
 0<:>schuster<:>ALL<:>PBS<:>4<:>1<:>



| :ref:`Back to Top <section3.1.1>`
| :ref:`Back to Table of Contents <index>`
