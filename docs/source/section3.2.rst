
.. _section3.2:

3.2 - Check Actions
=================================

Delayed command executions for due `dsupdt <https://gdex-docs-dsupdt.readthedocs.io>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io>`_ actions are recorded
automatically. Other commands — including `dsarch <https://gdex-docs-dsarch.readthedocs.io>`_ and specialist-defined ones
— can be added to **dscheck** manually. The following actions manage check records:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Add Check <section3.2.1>`
     - add a new check record for a deferred command
   * - :ref:`Get Check <section3.2.2>`
     - retrieve command information from check records
   * - :ref:`Delete Check <section3.2.3>`
     - delete check records for commands that no longer need processing
   * - :ref:`Unlock Check <section3.2.4>`
     - unlock a check record whose command aborted without releasing the lock

.. toctree::
   :maxdepth: 1
   :caption: Table of Contents

   section3.2.1
   section3.2.2
   section3.2.3
   section3.2.4

**Appendix A: List of Examples**

- :ref:`A.3. Action Option -AC (-AddCheck) <3.2.1_e3>`
- :ref:`A.4. Action Option -AC (-AddCheck) <3.2.1_e4>`
- :ref:`A.5. Action Option -AC (-AddCheck) <3.2.1_e5>`



| :ref:`Back to Top <section3.2>`
| :ref:`Back to Table of Contents <index>`
