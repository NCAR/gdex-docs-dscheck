
.. _section3.2.2:

3.2.2 - Get Check
=================================


.. _GC:

Action Option -**GC** (-**GetCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

gets check information recorded in GDEXDB.

| **dscheck** -(GC|GetCheck) [:ref:`Mode Options <mode3.2.2>`]
|           [:ref:`-(FN|FieldNames) <FN>` FieldNameString]
|           [:ref:`-(CI|CheckIndex) <CI>` CheckIndices]
|           [:ref:`-(ON|OrderNames) <ON>` OrderNameString]
|           [:ref:`-(CM|Command) <CM>` CommandNames]
|           [:ref:`-(AV|ArgumentVector) <AV>` ArgumentVectorString]
|           [:ref:`-(SN|Specialist) <SN>` SpecialistNames]
|           [:ref:`-(DS|Dataset) <DS>` DatasetIDs]
|           [:ref:`-(AN|ActionName) <AN>` ActionNames]
|           [:ref:`-(CD|CheckDate) <CD>` CommandDate]
|           [:ref:`-(CT|CheckTime) <CT>` CommandTime]
|           [:ref:`-(WD|WorkDir) <WD>` WorkingDirectory]
|           [:ref:`-(PQ|PBSQueue) <PQ>`  PBSBatchQueue]
|           [:ref:`-(OF|OutputFile) <OF>` OutputFileName]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

.. _mode3.2.2:

:ref:`Mode options <section4>` that can be specified for getting check Action:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(CS|CheckStatus) <CS>`
     - check and show detail information on check status
   * - :ref:`-(FO|FormatOutput) <FO>`
     - format the column output with a fix width for all values of a given field

Use :ref:`Info option <section5>` :ref:`-FN <FN>` (-FieldNames) to specify what check fields to retrieve.
It defaults to "COVTUPFJDNW" if :ref:`-FN <FN>` is not given.

Valid check field names and their corresponding :ref:`Info options <section5>`:

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Names
     - :ref:`Info Options <section5>`
     - Descriptions
   * - C
     - :ref:`-(CI|CheckIndex) <CI>`
     - check index
   * - O
     - :ref:`-(CM|Command) <CM>`
     - original command name
   * - V
     - :ref:`-(AV|ArgumentVector) <AV>`
     - argument line following command, up to 100 chars
   * - T
     - :ref:`-(DS|Dataset) <DS>`
     - dataset ID, the original command run against
   * - A
     - :ref:`-(AN|ActionName) <AN>`
     - action name for a given command
   * - U
     - :ref:`-(ST|Status) <ST>`
     - check status for a recorded command
   * - B
     - :ref:`-(DF|DownFlags) <DF>`
     - Storage system down flags: D-DRDATA,G-GLADE,O-ObjectStore
   * - P
     - :ref:`-(PQ|PBSQueue) <PQ>`
     - PBS batch queue name: gdex or htc
   * - R
     - :ref:`-(PI|ParentIndex) <PI>`
     - parent check index the current one to wait on
   * - F
     - :ref:`-(FC|FileCount) <FC>`
     - number of files need to be processed
   * - J
     - :ref:`-(DC|DoneCount) <DC>`
     - number of files are processed already
   * - K
     - :ref:`-(TC|TryCount) <TC>`
     - number of tries the command is executed
   * - L
     - :ref:`-(MC|MaxCount) <MC>`
     - upper limit for number of command tries
   * - Z
     - :ref:`-(SZ|DataSize) <SZ>`
     - total bytes of data processed for the command
   * - D
     - :ref:`-(CD|CheckDate) <CD>`
     - date the command is initially recorded
   * - Y
     - :ref:`-(CT|CheckTime) <CT>`
     - time the command is initially recorded
   * - H
     - :ref:`-(HN|HostName) <HN>`
     - host names the command can or cannot run on
   * - N
     - :ref:`-(SN|Specialist) <SN>`
     - specialist login name who starts the command
   * - W
     - :ref:`-(WD|WorkDir) <WD>`
     - working directory where the command is started
   * - M
     - :ref:`-(MO|Modules) <MO>`
     - include modules to load to batch job script
   * - I
     - :ref:`-(EV|Environments) <EV>`
     - include environment variables to load to batch job script
   * - Q
     - :ref:`-(QS|QsubOptions) <QS>`
     - additional PBS batch options for qsub
   * - X
     - :ref:`-(AX|ArgumentExtra) <AX>`
     - additional argument line beyond 100 characters
   * - E
     - :ref:`-(ER|ErrorMessage) <ER>`
     - error message from failed command

Check information can be retrieved for specified check index per option
:ref:`-CI <CI>` (-CheckIndex). Without any condition, the check records owned by the
current specialist are retrieved.



| :ref:`Back to Top <section3.2.2>`
| :ref:`Back to Table of Contents <index>`
