
.. _section3.2.2:

3.2.2 - Get Check
=================================


.. _GC:

Action Option -**GC** (-**GetCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

retrieves check records from GDEXDB. With no filter,
returns active check records owned by the current specialist.

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

Available mode options:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`-(CS|CheckStatus) <CS>`
     - include detailed status: progress percentage for running commands and error messages for failed ones.
   * - :ref:`-(FO|FormatOutput) <FO>`
     - pad each column to a uniform width for readability.

:ref:`-FN <FN>` (-FieldNames) selects which fields to retrieve as a string of
single-letter codes. When :ref:`-FN <FN>` is omitted, the default field set is
"COVTUPFJDNW".

Field codes for check records:

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Code
     - :ref:`Info Option <section5>`
     - Description
   * - C
     - :ref:`-(CI|CheckIndex) <CI>`
     - check index
   * - O
     - :ref:`-(CM|Command) <CM>`
     - original command name
   * - V
     - :ref:`-(AV|ArgumentVector) <AV>`
     - argument string after the command (<= 100 chars)
   * - T
     - :ref:`-(DS|Dataset) <DS>`
     - dataset ID the command runs against
   * - A
     - :ref:`-(AN|ActionName) <AN>`
     - action name for the command
   * - U
     - :ref:`-(ST|Status) <ST>`
     - check status for the recorded command
   * - B
     - :ref:`-(DF|DownFlags) <DF>`
     - storage down flags: D-DRDATA, G-GLADE, O-ObjectStore
   * - P
     - :ref:`-(PQ|PBSQueue) <PQ>`
     - PBS batch queue name (e.g. gdex, htc)
   * - R
     - :ref:`-(PI|ParentIndex) <PI>`
     - parent check index this check waits on
   * - F
     - :ref:`-(FC|FileCount) <FC>`
     - number of files to be processed
   * - J
     - :ref:`-(DC|DoneCount) <DC>`
     - number of files already processed
   * - K
     - :ref:`-(TC|TryCount) <TC>`
     - number of times the command has run
   * - L
     - :ref:`-(MC|MaxCount) <MC>`
     - maximum number of tries allowed
   * - Z
     - :ref:`-(SZ|DataSize) <SZ>`
     - total bytes processed for the command
   * - D
     - :ref:`-(CD|CheckDate) <CD>`
     - date the command was first recorded
   * - Y
     - :ref:`-(CT|CheckTime) <CT>`
     - time the command was first recorded
   * - H
     - :ref:`-(HN|HostName) <HN>`
     - host(s) the command can or cannot run on
   * - N
     - :ref:`-(SN|Specialist) <SN>`
     - specialist who owns the check
   * - W
     - :ref:`-(WD|WorkDir) <WD>`
     - working directory for the command
   * - M
     - :ref:`-(MO|Modules) <MO>`
     - modules to load in the batch job script
   * - I
     - :ref:`-(EV|Environments) <EV>`
     - environment variables for the batch job
   * - Q
     - :ref:`-(QS|QsubOptions) <QS>`
     - additional qsub options
   * - X
     - :ref:`-(AX|ArgumentExtra) <AX>`
     - additional argument string beyond 100 chars
   * - E
     - :ref:`-(ER|ErrorMessage) <ER>`
     - error message from a failed command

Use :ref:`-CI <CI>` (-CheckIndex) to fetch specific records. To inspect another
specialist's records, supply :ref:`-SN <SN>` with the appropriate login name.



| :ref:`Back to Top <section3.2.2>`
| :ref:`Back to Table of Contents <index>`
