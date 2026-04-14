
.. _section4:

4 - MODE OPTIONS
=================================

Mode options modify the behavior of :ref:`Action options <section3>`. They are all optional and
take no values.


.. _AW:

Mode Option -**AW** (-**AnyWhere**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

used with :ref:`Action <section3>` :ref:`-AC <AC>` (-AddCheck), leaves the working
directory empty in the check record so the command can run from any location.


.. _BG:

Mode Option -**BG** (-**BackGround**) (Alias: -**b**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

runs as a background process, suppressing
all screen output and error messages.


.. _CP:

Mode Option -**CP** (-**CheckPending**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

when used with :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck), checks and
kills long-pending checks.


.. _CS:

Mode Option -**CS** (-**CheckStatus**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

displays detailed status information for recorded
commands, including progress percentage for running commands and error
messages for failed ones.


.. _FI:

Mode Option -**FI** (-**ForceInterrrupt**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

required to interrupt a check that is currently being
processed; without it, a warning message is displayed instead.


.. _FO:

Mode Option -**FO** (-**FormatOutput**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

formats column output for GET actions. A uniform width,
evaluated dynamically, is applied to all values of a given field.


.. _LO:

Mode Option -**LO** (-**LogOn**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

enables detailed logging when **dscheck**
starts in daemon mode. Detailed logging is off by default.


.. _MD:

Mode Option -**MD** (-**MyDataset**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

allows a specialist to access check information for a
dataset owned by another specialist.


.. _NC:

Mode Option -**NC** (-**NoCommand**) (Alias: -**NoRemoteCommand**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

suppresses remote command
execution when used with :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck).


.. _ND:

Mode Option -**ND** (-**NewDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

required to add a new daemon control record when :ref:`Action <section3>`
:ref:`-SD <SD>` (-SetDaemon) is run with a daemon control index of 0. This flag prevents
daemon control records from being added unintentionally.


.. _NT:

Mode Option -**NT** (-**NoTrim**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

skips stripping spaces and comments from input values to
speed up reading of input files.


.. _WR:

Mode Option -**WR** (-**WithdsRqst**) (Alias: -**WithRequest**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ records due to be built or purged to check
records, for use with :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode.


.. _WU:

Mode Option -**WU** (-**WithdsUpdt**) (Alias: -**WithUpdate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ update controls to check records, for
use with :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode.



| :ref:`Back to Top <section4>`
| :ref:`Back to Table of Contents <index>`
