
.. _section5.2:

5.2 - Multi-Value Info Options
=================================

A multi-value Info option accepts a list of one or more values. Supplying
zero values causes an error.


.. _AN:

Info Option -**AN** (-**ActionName**) (Alias: -**Action**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the action name associated with a given
command recorded in a check record.


.. _AV:

Info Option -**AV** (-**ArgumentVector**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space-delimited argument string following the
command, up to 100 characters. Quote individual arguments containing spaces
with single quotes.


.. _AX:

Info Option -**AX** (-**ArgumenteXtra**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space-delimited argument string beyond 100
characters. Non-empty only when the argument vector exceeds 100 characters.


.. _CC:

Info Option -**CC** (-**CarbonCopy**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

one or more additional email addresses for Cc'd
notification of check status. For DECS specialists, login names are
acceptable; for other domains, full email addresses are required.


.. _CD:

Info Option -**CD** (-**CheckDate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the date the recorded command was first processed.


.. _CI:

Info Option -**CI** (-**CheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the check record indices for commands recorded in GDEXDB.
A check record is automatically purged when the command finishes.


.. _CM:

Info Option -**CM** (-**Command**) (Alias: -**CommandName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the command name recorded in a check
record.


.. _CT:

Info Option -**CT** (-**CheckTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the time the recorded command was first processed.


.. _DB:

Info Option -**DB** (-**Debug**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

enables debug logging. Up to 3 values may be given: debug
level (required), log file path, and log file name. The level can be a
single integer (e.g., 1000 means levels 1 to 1000) or a range (e.g.,
200-1000). Defaults: log path '${DSSHOME}/dssdb/log', file name 'mydss.dbg'.


.. _DC:

Info Option -**DC** (-**DoneCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files successfully processed so far.


.. _DF:

Info Option -**DF** (-**DownFlags**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

storage system down flags. Supported values: D-DRDATA,
G-GLADE, O-ObjectStore. Up to 5 flags may be combined.


.. _DI:

Info Option -**DI** (-**DaemonIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

daemon control indices. A daemon control record holds
the configuration for how many processes of a given command a specialist may
run on a given host, and at what priority.


.. _DS:

Info Option -**DS** (-**Dataset**) (Aliases: -**Dsid**, -**DatasetID**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

dataset numbers (also called dataset IDs), in the format
[a-z]NNNNNN.


.. _ER:

Info Option -**ER** (-**ERrormessage**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the error message from a failed check command.


.. _EV:

Info Option -**EV** (-**Environments**) (Alias: -**Envs**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

environment variables required to
execute a command as a batch job, in the form VarName=VarValue and separated
by commas. These variables are set in the batch startup script.


.. _FC:

Info Option -**FC** (-**FileCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files to be processed by a check command.


.. _HN:

Info Option -**HN** (-**HostName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the host names on which the check can or cannot be
processed.


.. _IF:

Info Option -**IF** (-**InputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

one or more input file names provided on the command line.
Input files hold options and their values for a **dscheck** execution.

In an input file:

* Lines beginning with '#' are comments and are ignored.
* Option names may be given in short, long, or alias form.
* :ref:`Action <section3>`/Mode options: OptionName<!>  (marker changeable via -AO)
* Single-value assignments: OptionName<=>OptionValue, one per line (delimiter changeable via -ES; default '<=>')
* Multi-value (tabular) assignments: a title row followed by data rows, with columns separated by '<:>' (changeable via -DV).
* Tabular data ends at EOF or when a new title line or single-value assignment is encountered.
* If the last column contains multi-line text, append the separator to every row (including the title line).


.. _MC:

Info Option -**MC** (-**MaxCount**) (Aliases: -**MaximumCount**, -**MaxTryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum number of times a failed check command may be
retried.


.. _MH:

Info Option -**MH** (-**MatchHost**) (Alias: -**MatchHostname**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

controls how hostnames are
matched: 'G' (general match — includes empty hostname or exclusive hostname
lists where the current host is not listed) or 'M' (exact match — only
the specified hostname).


.. _MO:

Info Option -**MO** (-**Modules**) (Alias: -**Mods**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

module names, separated by commas, needed
to execute a command as a batch job. These modules are loaded in the batch
startup script.


.. _PI:

Info Option -**PI** (-**ParentIndex**) (Alias: -**ParentCheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the parent check index that the current check must wait
for before it can run.


.. _PO:

Info Option -**PO** (-**Priority**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the priority of a given host, determining the order in
which hosts are selected to start a **dscheck** process.


.. _PL:

Info Option -**PL** (-**ProcessLimit**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum number of concurrent processes that can be
started for a given command and specialist on a specified host. Also used with
:ref:`Action <section3>` :ref:`-SO <SO>` (-SetOptions) to limit concurrent cron processes.


.. _PQ:

Info Option -**PQ** (-**PBSQueue**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the PBS batch queue to which the current check is submitted.


.. _QS:

Info Option -**QS** (-**QSubOptions**) (Alias: -**PBSOptions**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

options passed to qsub when running
a command as a PBS batch job. Quote the value on the command line, e.g.,
:ref:`-QS <QS>` '-l walltime=12:00:00'.


.. _SN:

Info Option -**SN** (-**Specialist**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the specialist who ran the original command. Used with
:ref:`Action <section3>` :ref:`-GC <GC>` (-GetCheck) to view check records owned by a specific specialist.


.. _ST:

Info Option -**ST** (-**Status**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the check status for a recorded command, including progress
percentage for running commands and error messages for failed ones.


.. _SZ:

Info Option -**SZ** (-**DataSize**) (Aliases: -**Size**, -**ProcSize**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the total bytes of data processed for the check record.


.. _TC:

Info Option -**TC** (-**TryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of times the check command has been attempted,
up to the limit set via :ref:`-MC <MC>`.


.. _WD:

Info Option -**WD** (-**WorkDir**) (Alias: -**WorkDirectory**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the working directory from which
the recorded command is started.



| :ref:`Back to Top <section5.2>`
| :ref:`Back to Table of Contents <index>`
