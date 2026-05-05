
.. _section3.5:

3.5 - Set Batch Options Dynamically
=================================


.. _SO:

Action Option -**SO** (-**SetOptions**) (Alias: -**SetBatchOptions**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

evaluates batch options
whose values begin with '!' so that PBS options can be assembled
dynamically (for example, by resolving environment- or workload-derived
values at submission time).

| **dscheck** -(SO|SetOptions)
|           [:ref:`-(HN|HostName) <HN>` HostNames]
|           [:ref:`-(PL|ProcessLimit) <PL>` MaxNumberOfProcesses]
|           [:ref:`-(MO|Modules) <MO>`  ModuleList]
|           [:ref:`-(EV|Environments) <EV>`  EnvironmentPairList]
|           [:ref:`-(QS|QsubOptions) <QS>`  PBSBatchOptions]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]



| :ref:`Back to Top <section3.5>`
| :ref:`Back to Table of Contents <index>`
