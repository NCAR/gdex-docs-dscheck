
.. _section3.2.1:

3.2.1 - Add Check
=================================


.. _AC:

Action Option -**AC** (-**AddCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds a check record for delayed command execution.

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

Available mode option:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(AW|AnyWhere) <AW>`
     - leaves the working directory empty in the check record so the command can be processed from any location

The command name is required. If not specified, the current specialist is
set as the owner of the check record and the current directory is used as
the working directory when the command runs later.

Pass additional PBS batch options via :ref:`-QS <QS>` (-QsubOptions). Use :ref:`-PI <PI>`
(-ParentIndex) to put the current command on hold until a parent check
finishes.

Commands with redirections or pipes are not supported for delayed mode.
Wrap complex commands in a simple shell script instead.


.. _3.2.1_e3:

**EXAMPLE 3. To list files containing 'test' in the current directory, capturing stdout to a log and displaying it on screen:**

| **dscheck** :ref:`-AC <AC>` :ref:`-CM <CM>` test1.sh :ref:`-HN <HN>` PBS

Content of shell script test1.sh:

.. code-block:: none

 (ls -l | grep test) | tee test1.out


.. _3.2.1_e4:

**EXAMPLE 4. To list files containing 'test', capturing stdout and stderr to separate log files:**

| **dscheck** :ref:`-AC <AC>` :ref:`-CM <CM>` test2.sh :ref:`-HN <HN>` PBS

Content of shell script test2.sh:

.. code-block:: none

 (ls -l | grep test) 1> test2.out 2>test2.err


.. _3.2.1_e5:

**EXAMPLE 5. To add command 'test3' to 'dscheck' for deferred execution on PBS:**

| **dscheck** :ref:`-AC <AC>` :ref:`-CM <CM>` test3 :ref:`-HN <HN>` PBS

The command 'test3' must be executable in the current working directory on
PBS machines.



| :ref:`Back to Top <section3.2.1>`
| :ref:`Back to Table of Contents <index>`
