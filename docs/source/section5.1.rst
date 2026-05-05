
.. _section5.1:

5.1 - Single-Value Info Options
=================================

A single-value Info option accepts exactly one value. Supplying zero or
multiple values is an error.


.. _DM:

Info Option -**DM** (-**DaemonMode**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the daemon mode for :ref:`-PC <PC>` (-ProcessCheck). Valid
values are start, stop, logon, and logoff: start the daemon, stop the
daemon, enable detailed logging, or disable detailed logging.


.. _DV:

Info Option -**DV** (-**Divider**) (Aliases: -**Delimiter**, -**Separater**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the column delimiter
used by multi-value tabular assignments in input files. Defaults to '<:>'.


.. _ES:

Info Option -**ES** (-**EqualSign**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the token that assigns a value to an option in input
files. Defaults to '<=>'.


.. _FN:

Info Option -**FN** (-**FieldNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a string of single-letter field codes selecting
which fields to retrieve. Used with :ref:`-GC <GC>` (-GetCheck) and :ref:`-GD <GD>` (-GetDaemon);
see Sections 3.1.2 and 3.2.2 for the code tables.


.. _LH:

Info Option -**LH** (-**LocalHost**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the local hostname on which to process checks for
:ref:`-PC <PC>` (-ProcessCheck). Defaults to the current hostname. Pass PBS to
process batch jobs.


.. _MT:

Info Option -**MT** (-**MaxrunTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum daemon run time. Defaults to 0
(unlimited). Examples: 5000 means 5000 seconds; 1D means one day
(86400 seconds).


.. _OF:

Info Option -**OF** (-**OutputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

redirect output to a file instead of the screen.


.. _ON:

Info Option -**ON** (-**OrderNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a string of single-letter field codes that
controls the sort order of :ref:`-GC <GC>` (-GetCheck) output.


.. _AO:

Info Option -**AO** (-**ActOption**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the token that marks :ref:`Action <section3>` and :ref:`Mode options <section4>` in
input files. Defaults to '<!>'.


.. _WI:

Info Option -**WI** (-**WaitInterval**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the time the dscheck daemon sleeps between
cycles. Defaults to 120 seconds (2 minutes).



| :ref:`Back to Top <section5.1>`
| :ref:`Back to Table of Contents <index>`
