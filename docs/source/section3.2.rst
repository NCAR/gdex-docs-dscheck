
.. _section3.2:

3.2 - Check Actions
=================================

Delayed mode command executions for due actions of `dsupdt <https://gdex-docs-dsupdt.readthedocs.io/en/latest/index.html>`_ and `dsrqst <https://gdex-docs-dsrqst.readthedocs.io/en/latest/index.html>`_ are
recorded automatically, while other commands, including `dsarch <https://gdex-docs-dsarch.readthedocs.io/en/latest/index.html>`_ and specialist-
defined ones, can be manually added into 'dscheck'. Command information can be
added, viewed and manipulated via 'dscheck' actions:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Add Check <section3.2.1>`
     - Add a new check record for a specified command
   * - :ref:`Get Check <section3.2.2>`
     - get the command information recorded in check records
   * - :ref:`Delete Check <section3.2.3>`
     - delete check records for no need of processing the commands
   * - :ref:`Unlock Check <section3.2.4>`
     - unlock check records in case that its recorded command is aborted without cleaning the lock

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
