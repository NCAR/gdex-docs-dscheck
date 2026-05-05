
.. _section1:

1 - INTRODUCTION
=================================

**dscheck** is the command-line interface to the centralized batch-processing
system for the GDEX Research Data Archive Management System (GDEXMS). It lets
DECS specialists schedule, monitor, control, and clean up deferred (delayed)
executions of utility programs such as `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_, `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_, and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_, as
well as any specialist-defined command.

The mental model has three layers:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - 1. A check record
     - a row in GDEXDB that captures one deferred command: its name, arguments, owner, working directory, target host, retry policy, and current status.
   * - 2. A daemon control
     - a row in GDEXDB that tells the centralized **dscheck** daemon how many concurrent processes of a given command a given specialist may run on a given host, and at what host priority.
   * - 3. The dscheck daemon
     - a long-running process that wakes on a fixed interval, adds due 'dsupdt'/'dsrqst' check records, and starts (or restarts) commands from check records on hosts chosen according to daemon control configuration.

Typical lifecycle of a deferred command:

.. code-block:: none

     added  --->  pending  --->  running  --->  finished (purged to history)     
                        \             \                                          
                         \             +--->  failed (E)            [purged]     
                          \                \                                     
                           +-->  retried (if reprocessing supported, e.g. dsarch)

A check record is locked while its command runs so the same command is never
started twice. When the command finishes successfully, or fails terminally,
the check record is moved to check history. History records can be reviewed
with the utility **viewcheckusage**.

Failure handling depends on the calling utility. `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_ supports
check-reprocessing: failed checks remain in GDEXDB until the command
succeeds or its maximum retry count is reached. `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ and `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ have
their own recovery paths and do not rely on dscheck retries; for them, an
errored check is purged with status 'E'.

A check is owned exclusively by the specialist who submitted it. Other
specialists cannot accidentally process or delete it.

What **dscheck** can do:

* Configure daemon controls per (specialist, command, host) so that the daemon knows where, how many at a time, and in what host order to run commands. Without daemon controls, recorded commands are not started automatically.
* Add a check record to schedule a deferred run of any specialist-defined command.
* Inspect daemon controls and check records currently in GDEXDB.
* Email the current status of one or more checks (including any error messages) to a specialist.
* Remove check records that are no longer needed.
* Unlock a check whose lock was left behind after an abnormal termination.
* Interrupt a running check and recursively kill all of its child processes.
* Add due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ work to dscheck records.
* Process checks (start them on the configured hosts) in daemon mode or on demand.
* Verify daemon-host connectivity for a specialist.

The remainder of this document is organized as follows. Section 2 covers
general usage and conventions. Section 3 describes :ref:`Action options <section3>` grouped
by what they manipulate (daemon controls, check records, check processing,
host connectivity, batch options). Section 4 lists :ref:`Mode options <section4>` that modify
how an action behaves. Section 5 lists Information options that pass values
into an action.



| :ref:`Back to Top <section1>`
| :ref:`Back to Table of Contents <index>`
