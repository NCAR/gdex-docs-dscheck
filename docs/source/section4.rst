
.. _section4:

4 - MODE OPTIONS
=================================

Mode options modify the behavior of an :ref:`Action option <section3>`. They take no values.
Each Mode option is meaningful only with specific actions; the relevant
action is noted with each one below.


.. _AW:

Mode Option -**AW** (-**AnyWhere**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-AC <AC>` (-AddCheck): leave the check's working
directory empty so the command may run from any location.


.. _BG:

Mode Option -**BG** (-**BackGround**) (Alias: -**b**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

run as a background process and suppress
all screen output and error messages.


.. _CP:

Mode Option -**CP** (-**CheckPending**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-PC <PC>` (-ProcessCheck): identify and kill
checks that have been pending too long.


.. _CS:

Mode Option -**CS** (-**CheckStatus**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-GC <GC>` (-GetCheck): include detailed status
for each check, including progress percentage for running commands and
error messages for failed ones.


.. _FI:

Mode Option -**FI** (-**ForceInterrrupt**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

required with :ref:`-IC <IC>` (-InterruptCheck) to actually
interrupt a check that is currently being processed; without it, dscheck
prints a warning instead of interrupting.


.. _FO:

Mode Option -**FO** (-**FormatOutput**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with Get-style actions (:ref:`-GD <GD>`, :ref:`-GC <GC>`): pad each
column to a uniform width computed from the data, for readability.


.. _LO:

Mode Option -**LO** (-**LogOn**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-PC <PC>` -DM start: enable
detailed daemon logging from startup. Detailed logging is off by default.


.. _MD:

Mode Option -**MD** (-**MyDataset**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

allows a specialist to access check information for
a dataset owned by a different specialist.


.. _NC:

Mode Option -**NC** (-**NoCommand**) (Alias: -**NoRemoteCommand**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-PC <PC>`: skip the
actual remote command execution (dry run).


.. _ND:

Mode Option -**ND** (-**NewDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

required with :ref:`-SD <SD>` (-SetDaemon) when the daemon
control index is 0, so that a new daemon control record is created.
This guard prevents creating records by accident.


.. _NT:

Mode Option -**NT** (-**NoTrim**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

skip stripping spaces and comments from input values
when reading input files; this speeds up parsing of large input files.


.. _WR:

Mode Option -**WR** (-**WithdsRqst**) (Alias: -**WithRequest**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode:

.. list-table::
   :widths: auto
   :header-rows: 1
 add `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ records due to be built or purged to check records before processing.


.. _WU:

Mode Option -**WU** (-**WithdsUpdt**) (Alias: -**WithUpdate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode:

.. list-table::
   :widths: auto
   :header-rows: 1
 add due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ update controls to check records before processing.



| :ref:`Back to Top <section4>`
| :ref:`Back to Table of Contents <index>`
