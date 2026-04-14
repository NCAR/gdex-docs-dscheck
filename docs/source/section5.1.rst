
.. _section5.1:

5.1 - Single-Value Info Options
=================================

A single-value Info option accepts exactly one value. Providing no value or
more than one causes an error.


.. _DM:

Info Option -**DM** (-**DaemonMode**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

passes a daemon mode value — start, stop, logon, or
logoff — to :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) to start, stop, enable, or disable
detailed logging, respectively.


.. _DV:

Info Option -**DV** (-**Divider**) (Aliases: -**Delimiter**, -**Separater**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the column delimiter for
multi-value Info options in input files. Defaults to '<:>'.


.. _ES:

Info Option -**ES** (-**EqualSign**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the token used to assign a value to an option in input
files. Defaults to '<=>'.


.. _FN:

Info Option -**FN** (-**FieldNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a string of single-letter field codes selecting which
fields to retrieve for check information via :ref:`Action <section3>` :ref:`-GC <GC>` (-GetCheck).


.. _LH:

Info Option -**LH** (-**LocalHost**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the local hostname on which to process checks for :ref:`Action <section3>`
:ref:`-PC <PC>` (-ProcessCheck). Defaults to the current hostname. Specify PBS to process
batch jobs.


.. _MT:

Info Option -**MT** (-**MaxrunTime**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the maximum run time for daemon mode. Defaults to 0
(unlimited). For example, 5000 means 5000 seconds, and 1D means 1 day
(86400 seconds).


.. _OF:

Info Option -**OF** (-**OutputFile**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

redirects output to a file instead of the screen.


.. _ON:

Info Option -**ON** (-**OrderNames**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a string of single-letter field codes controlling the
sort order of results from :ref:`Action <section3>` :ref:`-GC <GC>` (-GetCheck).


.. _AO:

Info Option -**AO** (-**ActOption**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the token that marks :ref:`Action <section3>` and :ref:`Mode options <section4>` in input
files. Defaults to '<!>'.


.. _WI:

Info Option -**WI** (-**WaitInterval**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the time the **dscheck** daemon sleeps between processing
cycles. Defaults to 2 minutes (120 seconds).



| :ref:`Back to Top <section5.1>`
| :ref:`Back to Table of Contents <index>`
