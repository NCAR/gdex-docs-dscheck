
.. _section3.2.1:

3.2.1 - Add Check
=================================


.. _AC:

Action Option -**AC** (-**AddCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds a check record so that a command runs later,
driven by the dscheck daemon (or by an explicit :ref:`-PC <PC>` invocation).

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
     - leave the working directory empty in the check record so the command may run from any location.

Defaults:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - Owner
     - the specialist running **dscheck**.
   * - Working directory
     - the current directory at the time of :ref:`-AC <AC>`.
   * - Host
     - none specified; daemon control governs placement.

Use :ref:`-PI <PI>` (-ParentIndex) to make the new check wait for an existing parent
check to finish before it can run. Use :ref:`-QS <QS>` to pass options through to
qsub when the command will run as a PBS batch job.

Limitations:

* Shell redirections and pipes (>, >>, |, <) are not supported in the deferred command line. Wrap such commands in a shell script and add the script.

Examples:

.. list-table::
   :widths: auto
   :header-rows: 1
 List files containing 'test' in the current directory, capture stdout to a log, and also display it on screen:

| **dscheck** :ref:`-AC <AC>` -CM test1.sh :ref:`-HN <HN>` PBS

<<Content of shell script test1.sh>>
(ls -l | grep test) | tee test1.out

List files containing 'test', capturing stdout and stderr to separate
log files:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-AC <AC>` -CM test2.sh :ref:`-HN <HN>` PBS

<<Content of shell script test2.sh>>
(ls -l | grep test) 1> test2.out 2>test2.err

Add the executable 'test3' for deferred execution on PBS:

.. list-table::
   :widths: auto
   :header-rows: 1
 dscheck :ref:`-AC <AC>` -CM test3 :ref:`-HN <HN>` PBS

The command 'test3' must be executable from the working directory on
the PBS machine.



| :ref:`Back to Top <section3.2.1>`
| :ref:`Back to Table of Contents <index>`
