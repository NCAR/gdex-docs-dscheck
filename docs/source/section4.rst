
.. _section4:

4 - MODE OPTIONS
=================================

Use proper Mode options to modify behaviors of :ref:`Action options <section3>`. Mode options
are all optional. No value is allowed to be passed in following any Mode option.


.. _AW:

Mode Option -**AW** (-**AnyWhere**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

for :ref:`Action <section3>` :ref:`-AC <AC>` (-AddCheck), sets Working directory empty in
check record to start processing the check anywhere.


.. _BG:

Mode Option -**BG** (-**BackGround**) (Alias: -**b**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

background process. When it is present,
screen display is turned off for both standard output and errors.


.. _CP:

Mode Option -**CP** (-**CheckPending**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

if present for :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck), checks and kills
long pending checks.


.. _CS:

Mode Option -**CS** (-**CheckStatus**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

if present, displays detailed status information of the
recorded commands, including progress percentage for a running command and
error message for a failed command.


.. _FI:

Mode Option -**FI** (-**ForceInterrrupt**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

if present, force interrupts a check that is still under
processing; otherwise a warning message will display.


.. _FO:

Mode Option -**FO** (-**FormatOutput**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

if present, formats column output results for get
actions. A same width, evaluated dynamically, is applied for all values of a
given field.


.. _LO:

Mode Option -**LO** (-**LogOn**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

turns detail logging on when **dscheck** starts
in Daemon mode. The detail logging is off as default if this Mode option is
not present.


.. _MD:

Mode Option -**MD** (-**MyDataset**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

allows a specialist to manipulate check information of
a given dataset listed for another specialist.


.. _NC:

Mode Option -**NC** (-**NoCommand**) (Alias: -**NoRemoteCommand**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

does not issue remote commands if
this Mode option is present for action :ref:`-PC <PC>` (-ProcessCheck).


.. _ND:

Mode Option -**ND** (-**NewDaemon**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a new daemon control can only be added when this Mode option is
present and daemon control index is given as 0 when :ref:`Action <section3>` :ref:`-SD <SD>` (-SetDaemon) of
**dscheck** is executed. This Mode option blocks mistakes of adding daemon control
records unintentionally.


.. _NT:

Mode Option -**NT** (-**NoTrim**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

skips trimming of spaces and comments from input values to
speed up reading input file(s).


.. _WR:

Mode Option -**WR** (-**WithdsRqst**) (Alias: -**WithRequest**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds requests due to be built or purged of command `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_
for **dscheck** :ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode.


.. _WU:

Mode Option -**WU** (-**WithdsUpdt**) (Alias: -**WithUpdate**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

adds due update controls of command `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ for **dscheck**
:ref:`Action <section3>` :ref:`-PC <PC>` (-ProcessCheck) in non-daemon mode.



| :ref:`Back to Top <section4>`
| :ref:`Back to Table of Contents <index>`
