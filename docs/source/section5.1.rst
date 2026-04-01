
.. _section5.1:

5.1 - Single-Value Info Options
=================================

A single-value Info option is used to pass one value into this application.
One value, and one only, must follow a single-value option; otherwise an
error message is displayed if no value or more than one value passed in.


.. _DM:

Info Option -**DM** (-**DaemonMode**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

passes daemon mode values, start, stop, logon or logoff
to 'dscheck' :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) to start, to stop, to log detail or
not to log detail, correspondingly.


.. _DV:

Info Option -**DV** (-**Divider**) (Aliases: -**Delimiter**, -**Separater**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

delimiter for separating
columns of multi-value Info options in input files. It is default to '<:>'.


.. _ES:

Info Option -**ES** (-**EqualSign**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for an equal sign of assigning one value to either a
single-value option or multi-value option in input files. It is defaulted
to '<=>'.


.. _FN:

Info Option -**FN** (-**FieldNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for a string of single letter field names. Values of
the selected fields are retrieved for check information per actions :ref:`-GC <GC>`
(-GetCheck).


.. _LH:

Info Option -**LH** (-**LocalHost**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specify a local hostname to processes checks on the host for
action :ref:`-PC <PC>`(-ProcessCheck). It defaults to '' to use the local host name. Specify
PBS to process batch jobs.


.. _MT:

Info Option -**MT** (-**MaxrunTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

specify the maxmum run time for deamon mode. It defaults to 0
for unlimit time. For examples, 5000 means seconds, and 1D means 1 day for 86400
seconds.


.. _OF:

Info Option -**OF** (-**OutputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

leads an output file name into which the output result
of this application is dumped. If this option is not given, the result is
displayed as standard output.


.. _ON:

Info Option -**ON** (-**OrderNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for a string of single letter field names use to order
the results of getting check information via action :ref:`-GC <GC>` (-GetCheck).


.. _AO:

Info Option -**AO** (-**ActOption**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for setting :ref:`Action <section3>` and :ref:`Mode options <section4>` in input files. It is
default to '<!>'.


.. _WI:

Info Option -**WI** (-**WaitInterval**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

defaults to 2 minutes (120 seconds). It is used as a time
intervals for the 'dscheck' daemon to sleep between processing check records.



| :ref:`Back to Top <section5.1>`
| :ref:`Back to Table of Contents <index>`
