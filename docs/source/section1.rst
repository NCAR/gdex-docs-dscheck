
.. _section1:

1 - INTRODUCTION
=================================

**dscheck** is a utility for adding, removing, viewing, and processing recorded
commands of other utility programs in the Research Data Archive Management System
(GDEXMS). Utility programs `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_, `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_, and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ support delayed
execution (also called batch processing): when a command is deferred, its
information and the directory from which it was invoked are saved to GDEXDB as
a check record. Specialist-defined commands can also be deferred by adding them
to **dscheck** control via :ref:`Action <section3>` :ref:`-AC <AC>` (-AddCheck).

Check records are processed automatically by a centralized **dscheck** daemon,
though they can also be processed manually from the command line. While a
recorded command is running, its check record is locked in GDEXDB to prevent
duplicate executions. Once a command finishes, its check record is automatically
moved to check history.

When a recorded command fails due to a system, storage, or database error, the
check record is normally purged with status 'E' (error). However, if the utility
program supports check-reprocessing — as `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_ does — the record is retained
in GDEXDB until the command succeeds or the maximum retry limit is reached.
`dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ and `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ handle their own failure recovery and do not require
check-reprocessing.

Completed check records are retained in GDEXDB as history and can be viewed via
the utility program **viewcheckusage**.

**dscheck** supports the following major functions:

* Set daemon control records for individual specialists to configure how many concurrent processes of a specified command can run on a given host, and the host priorities that determine which host is selected for processing a check. Without daemon control information, recorded commands will not start automatically
* Add a check record for delayed execution of any specialist-defined command
* View utility command information currently saved in GDEXDB
* Email the current status of a specified command or list of commands, including any error messages, to a specialist
* Delete recorded command information when a command is no longer needed
* Unlock a check record when lock information was not cleaned up properly after a command failure
* Interrupt a running command and recursively kill all associated child processes
* Add due `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ and `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ actions into dscheck records
* Process commands recorded in GDEXDB, including ones that previously failed

The specialist who submits a command under **dscheck** control remains its
exclusive owner in GDEXDB, preventing the command from being processed or
deleted accidentally by other specialists.

The following sections describe general **dscheck** usage first, then :ref:`Action <section3>`
options in detail, followed by :ref:`Mode <section4>` and :ref:`Info options <section5>`.



| :ref:`Back to Top <section1>`
| :ref:`Back to Table of Contents <index>`
