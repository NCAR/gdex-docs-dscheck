
.. _section5.2:

5.2 - Multi-Value Info Options
=================================

A multi-value Info option is used to pass multiple values for one Info option
into 'dscheck'. At lease one value must follow each multi-value option.


.. _AN:

Info Option -**AN** (-**ActionName**) (Alias: -**Action**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specifies an action name for given command
name recorded in check record.


.. _AV:

Info Option -**AV** (-**ArgumentVector**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space delimited argument vector string up to 100
characters. It is quoted with single quotes '' for a individual argument
containing spaces.


.. _AX:

Info Option -**AX** (-**ArgumenteXtra**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the space delimited argument vector string beyond 100
characters. This field is not empty only if the argument vector string is
longer than 100 characters.


.. _CC:

Info Option -**CC** (-**CarbonCopy**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

provides additional one or multiple email addresses on
command line to send Cc'd email notification of the check status. For
DECS specialist, login user names themselves are acceptable; otherwise full
email addresses are required for email domains other than 'ucar.edu'.


.. _CD:

Info Option -**CD** (-**CheckDate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the check date of the recorded command is first processed.


.. _CI:

Info Option -**CI** (-**CheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

check record indices for commands recorded in RDADB. A check
record is automatically purged if the command is finished.


.. _CM:

Info Option -**CM** (-**Command**) (Alias: -**CommandName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the command name recorded in check record.


.. _CT:

Info Option -**CT** (-**CheckTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the check time of the recorded command is first processed.


.. _DB:

Info Option -**DB** (-**Debug**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

turns on debug mode with specified information. This option
provides up to 3 values, they are Debug Level, debug log file path and debug
log file name. The debug level is mandatory for this option. It can be a
single integer value, for example, 1000 means to log debug messages for debug
levels 1 to 1000; or a range of values, for example, 200-1000 means to log
debug messages from debug levels 200 to 1000. The default debug file path is
'$DSSHOME}/dssdb/log' and the default debug file name is 'mydss.dbg'. Provides
the second and third values for this option to override the default ones
respectively.


.. _DC:

Info Option -**DC** (-**DoneCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files that are processed successfully already.


.. _DF:

Info Option -**DF** (-**DownFlags**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

storage system down flags. The current supported flags are:

.. list-table::
   :widths: auto
   :header-rows: 1
 H-HPSS, D-DRDATA, G-GLADE, O-ObjectStore. It can hold multiple flags, up to 5, for all down storage systems.


.. _DI:

Info Option -**DI** (-**DaemonIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

daemon control indices. A daemon control record retains
configuration information for how many processes on what host and its priority
can a command be started for specified specialist.


.. _DS:

Info Option -**DS** (-**Dataset**) (Aliases: -**Dsid**, -**DatasetID**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for dataset numbers, or called dataset IDs in form as [a-z]NNNNNN.


.. _ER:

Info Option -**ER** (-**ERrormessage**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

error message of a failed check command.


.. _EV:

Info Option -**EV** (-**Environments**) (Alias: -**Envs**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(Alias: -Envs), specifies environment variables, in form of
VarName=VarValue and separated by ',', needed to be set to execute a command as
a batch job. The environment varaibles will be set in the batch starting script.


.. _FC:

Info Option -**FC** (-**FileCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of files to be processed by a check command.


.. _HN:

Info Option -**HN** (-**HostName**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specify the host names the check can or cannot be processed on.


.. _IF:

Info Option -**IF** (-**InputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for input file names; one or multiple file names may be
given on command line. Input files are used to hold all valid options and
the associated values of Info options that need to be passed in for
execution of 'dscheck'.

In a input file, lines start with sign '#' are considered as comments;
Option Names can be given either short, long or alias names. :ref:`Action <section3>` and :ref:`Mode <section4>`
options are given in format of OptionName<!>. Single value Assignment is
given in format of OptionName<=>OptionValue. One option is given on each line.
Different setting sign of :ref:`Action <section3>` and :ref:`Mode options <section4>` can be provided by Info
option -AO (-ActOption, default to <!>); and different equal sign of single
value assignment can be provided by Info option :ref:`-ES <ES>`, (-EqualSign, default to
'<=>'). Multi-value assignments can be given in columns delimited with
separator specified per option -SP (-Separator, default to '<:>'). It starts
with a column title line for multi-value option names and the rest holds
values corresponding to each column titles. The value information stops at
the end of the file or when a new column name line or another single value
assignment appears. If the last column is a multi-line value field, an
additional separator must be appended for each line, including the column
title line to end lines properly.


.. _MC:

Info Option -**MC** (-**MaxCount**) (Aliases: -**MaximumCount**, -**MaxTryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum number of tries for a check command can be processed
if the command is failed.


.. _MH:

Info Option -**MH** (-**MatchHost**) (Alias: -**MatchHostname**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

flag to control hostname match.
'G' - general match, including emty hostname specified, or exclusive hostnames
given but the hostname is not in the list, and 'M' - match only the hostname
specified is identical to the current host.


.. _MO:

Info Option -**MO** (-**Modules**) (Alias: -**Mods**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(Alias: -Mods), specifies module names, separated by ',',
needed to be loaded to execute a command as a batch job. The modules will
be set in the batch starting script.


.. _PI:

Info Option -**PI** (-**ParentIndex**) (Alias: -**ParentCheckIndex**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specifies a parent check index for the current check to
wait on.


.. _PO:

Info Option -**PO** (-**Priority**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specifies the priority of a given host so that the host is
picked in such an order to start a 'dscheck' process.


.. _PL:

Info Option -**PL** (-**ProcessLimit**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specifies how many processes can be started for specified
command and specialist on a given host; Work for :ref:`Action <section3>` :ref:`-SO <SO>` (-SetOptions) to limit
how many concurrent cron processes.


.. _PQ:

Info Option -**PQ** (-**PBSQueue**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specifies PBS batch queue index the current check to submit to.


.. _QS:

Info Option -**QS** (-**QSubOptions**) (Alias: -**PBSOptions**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(Alias: -PBSOptions), specifies options to execute a command
as a batch job via qsub on PBS nodes. The qsub options must be quoted when prsented
on command line, such as, :ref:`-QS <QS>` '-l walltime=12:00:00'.


.. _SN:

Info Option -**SN** (-**Specialist**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the specialist who runs the original command. This Info
option is working with :ref:`Action <section3>` :ref:`-GC <GC>` (-GetCheck) only to view check information
of a specified specialist.


.. _ST:

Info Option -**ST** (-**Status**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

check command status for a check record. Include command
progress percentage if under process and error message for a failed command.


.. _SZ:

Info Option -**SZ** (-**DataSize**) (Aliases: -**Size**, -**ProcSize**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the total bytes of data is processed for the check record.


.. _TC:

Info Option -**TC** (-**TryCount**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the number of tries for a check command being processed. It
is up to the number of tries specified via info option :ref:`-MC <MC>`.


.. _WD:

Info Option -**WD** (-**WorkDir**) (Alias: -**WorkDirectory**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the working directory where the
the recorded command is started.



| :ref:`Back to Top <section5.2>`
| :ref:`Back to Table of Contents <index>`
