
.. _section5.2:

5.2 - Multi-Value Info Options
=================================

A multi-value Info option accepts a list of one or more values. Supplying
zero values is an error.


.. _AN:

Info Option -**AN** (-**ActionName**) (Alias: -**Action**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the action name associated with
a command in a check record.


.. _AV:

Info Option -**AV** (-**ArgumentVector**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space-delimited argument string that
follows the command, up to 100 characters. Quote individual arguments
containing spaces with single quotes.


.. _AX:

Info Option -**AX** (-**ArgumenteXtra**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space-delimited argument string beyond 100
characters. Non-empty only when the argument vector exceeds 100
characters.


.. _CC:

Info Option -**CC** (-**CarbonCopy**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

additional email addresses for Cc'd notification
of check status. DECS specialists may be specified by login name; for
other domains, use full email addresses.


.. _CD:

Info Option -**CD** (-**CheckDate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the date a recorded command was first processed.


.. _CI:

Info Option -**CI** (-**CheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the indices of check records in GDEXDB. A check
record is moved to history once its command finishes.


.. _CM:

Info Option -**CM** (-**Command**) (Alias: -**CommandName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the command name in a check
record.


.. _CT:

Info Option -**CT** (-**CheckTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the time a recorded command was first processed.


.. _DB:

Info Option -**DB** (-**Debug**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

enable debug logging. Up to three values may be given:

.. list-table::
   :widths: auto
   :header-rows: 1
 the debug level (required), the log file path, and the log file name. The level is either a single integer (e.g. 1000 means levels 1 to 1000) or a range (e.g. 200-1000). Defaults: log path '${DSSHOME}/dssdb/log', file name 'mydss.dbg'.


.. _DC:

Info Option -**DC** (-**DoneCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files successfully processed so far.


.. _DF:

Info Option -**DF** (-**DownFlags**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

storage system down flags. Valid flags: D-DRDATA,
G-GLADE, O-ObjectStore. Up to five flags may be combined.


.. _DI:

Info Option -**DI** (-**DaemonIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

daemon control indices. A daemon control record
defines how many concurrent processes of a given command a specialist
may run on a given host, and at what priority.


.. _DS:

Info Option -**DS** (-**Dataset**) (Aliases: -**Dsid**, -**DatasetID**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

dataset numbers (also called dataset IDs). Format:

.. list-table::
   :widths: auto
   :header-rows: 1
 [a-z]NNNNNN.


.. _ER:

Info Option -**ER** (-**ERrormessage**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the error message from a failed check command.


.. _EV:

Info Option -**EV** (-**Environments**) (Alias: -**Envs**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

environment variables required
to run a command as a batch job, in the form VarName=VarValue, separated
by commas. The variables are set in the batch startup script.


.. _FC:

Info Option -**FC** (-**FileCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files to be processed by a check
command.


.. _HN:

Info Option -**HN** (-**HostName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

host names on which the check can or cannot be
processed.


.. _IF:

Info Option -**IF** (-**InputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

one or more input file names supplied on the command
line. An input file holds options and their values for a dscheck
invocation.

Input file format:

* Lines starting with '#' are comments and are ignored.
* Option names may appear in short, long, or alias form.
* :ref:`Action <section3>`/Mode markers:           OptionName<!> (marker overridable via :ref:`-AO <AO>`)
* Single-value assignments:      OptionName<=>OptionValue (one per line; '<=>' overridable via -ES)
* Multi-value tabular assignments: a title row followed by data rows, columns separated by '<:>' ('<:>' overridable via -DV).
* A tabular block ends at EOF, at the next title line, or at the next single-value assignment.
* If the last column of a tabular block contains multi-line text, append the column separator to every row, including the title row.


.. _MC:

Info Option -**MC** (-**MaxCount**) (Aliases: -**MaximumCount**, -**MaxTryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum number of times a failed check command
may be retried.


.. _MH:

Info Option -**MH** (-**MatchHost**) (Alias: -**MatchHostname**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

controls how hostnames are
matched. 'G' is a general match - it includes empty hostnames and
exclusive lists where the current host is not listed. 'M' is an exact
match against the specified hostname.


.. _MO:

Info Option -**MO** (-**Modules**) (Alias: -**Mods**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

comma-separated module names required
to run a command as a batch job. The modules are loaded in the batch
startup script.


.. _PI:

Info Option -**PI** (-**ParentIndex**) (Alias: -**ParentCheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the parent check index that the current check
must wait for before it can run.


.. _PO:

Info Option -**PO** (-**Priority**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the priority of a host within a daemon control,
determining the order in which hosts are tried when starting a check.


.. _PL:

Info Option -**PL** (-**ProcessLimit**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum number of concurrent processes
allowed for a given (command, specialist) on a given host. Also used
with :ref:`-SO <SO>` (-SetOptions) to bound concurrent cron processes.


.. _PQ:

Info Option -**PQ** (-**PBSQueue**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the PBS batch queue to which the current check is
submitted.


.. _QS:

Info Option -**QS** (-**QSubOptions**) (Alias: -**PBSOptions**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

options passed to qsub when
the command runs as a PBS batch job. Quote the value on the command
line, e.g. :ref:`-QS <QS>` '-l walltime=12:00:00'.


.. _SN:

Info Option -**SN** (-**Specialist**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the specialist who originally ran the command.
Used with :ref:`-GC <GC>` (-GetCheck) and :ref:`-GD <GD>` (-GetDaemon) to view records owned
by a particular specialist.


.. _ST:

Info Option -**ST** (-**Status**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the check status for a recorded command, including
progress percentage for running commands and error messages for failed
ones.


.. _SZ:

Info Option -**SZ** (-**DataSize**) (Aliases: -**Size**, -**ProcSize**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the total number of bytes processed for the check
record.


.. _TC:

Info Option -**TC** (-**TryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of times the check command has been
attempted, up to the limit set by :ref:`-MC <MC>`.


.. _WD:

Info Option -**WD** (-**WorkDir**) (Alias: -**WorkDirectory**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the working directory from
which the recorded command is started.



| :ref:`Back to Top <section5.2>`
| :ref:`Back to Table of Contents <index>`
