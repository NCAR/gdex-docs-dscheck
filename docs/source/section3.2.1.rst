
.. _section3.2.1:

3.2.1 - Add Check
=================================


.. _AC:

Action Option -**AC** (-**AddCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds check information for a delayed mode command execution.

| **dscheck** -(AC|AddCheck) [:ref:`Mode Option <mode3.2.1>`]
|            :ref:`-(CM|Command) <CM>` CommandNames
|           [:ref:`-(AV|ArgumentVector) <AV>` ArgumentVectorString]
|           [:ref:`-(SN|Specialist) <SN>` SpecialistNames]
|           [:ref:`-(HN|HostName) <HN>` HostNames]
|           [:ref:`-(DS|Dataset) <DS>` DatasetIDs]
|           [:ref:`-(AN|ActionName) <AN>` ActionNames]
|           [:ref:`-(PI|ParentIndex) <PI>` ParentCheckIndex]
|           [:ref:`-(PQ|PBSQueue) <PQ>`  PBSBatchQueue]
|           [:ref:`-(WD|WorkDir) <WD>` WorkingDirectory]
|           [:ref:`-(MC|MaxCount) <MC>` MaxTryCount]
|           [:ref:`-(MO|Modules) <MO>`  ModuleList]
|           [:ref:`-(EV|Environments) <EV>`  EnvironmentPairList]
|           [:ref:`-(QS|QsubOptions) <QS>`  PBSBatchOptions]
|           [:ref:`-(OF|OutputFile) <OF>` OutputFileName]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

.. _mode3.2.1:

:ref:`Mode option <section4>` that can be specified for adding check control Action:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(AW|AnyWhere) <AW>`
     - sets Working directory empty in check record to start processing the check anywhere.

Command name is mandatory for adding a new check for delayed mode execution.
Unless they are specified, the current specialist who adds the command is defaulted
as the owner of the added check record, and the current path is defaulted as the
working directory when the command is executed later.

Specified addtional PBS batch options via :ref:`Info option <section5>` :ref:`-QS <QS>` (-QSubOptions) to add a check;
and specify a parent check index to put the current command on hold until the parent
check is finished.

Commands containing redirections and pipes are not supported for delayed mode.
A simple shell script can be used to wrap a complicated command.


.. _3.2.1_e3:

**EXAMPLE 3. To list file names in the current directory with name containing 'test' by catching the standard output into a log and display it on screen:**

dsheck AC :ref:`-CM <CM>` test1.sh :ref:`-HN <HN>` PBS

Content of shell script test1.sh:

.. code-block:: none

 (ls -l | grep test) | tee test1.out


.. _3.2.1_e4:

**EXAMPLE 4. To list file names in the current directory with name containing 'test' by catching the standard output and error into separate log files:**

dsheck AC :ref:`-CM <CM>` test2.sh :ref:`-HN <HN>` PBS

Content of shell script test2.sh:

.. code-block:: none

 (ls -l | grep test) 1> test2.out 2>test2.err


.. _3.2.1_e5:

**EXAMPLE 5. To add testing command 'test3' into 'dscheck' for delayed mode execution on PBS:**

dsheck AC :ref:`-CM <CM>` test3 :ref:`-HN <HN>` PBS

The command 'test3' must be executable at the current working directory on PBS machines.



| :ref:`Back to Top <section3.2.1>`
| :ref:`Back to Table of Contents <index>`
