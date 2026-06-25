
.. _section3:

3 - ACTION OPTIONS
=================================

An Action option selects what **dscheck** does. Action options take no
values, and exactly one Action option may be supplied per invocation.

Action options are grouped into four categories:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Daemon Control Actions <section3.1>`
     - create, modify, view, and delete daemon control records that govern how, where, and how concurrently commands run.
   * - :ref:`Check Actions <section3.2>`
     - add, view, delete, and unlock individual check records.
   * - :ref:`Check Process Actions <section3.3>`
     - start commands from check records, interrupt running commands, or email check status.
   * - :ref:`Daemon Host Connectivity <section3.4>`
     - verify that daemon hosts are reachable for a specialist.

A fifth, narrower action :ref:`-SO <SO>` (-SetOptions) builds batch options dynamically
and is documented in Section 3.5.

.. toctree::
   :maxdepth: 2
   :caption: Table of Contents

   section3.1
   section3.2
   section3.3
   section3.4
   section3.5

**Appendix A: List of Examples**

- :ref:`A.1. Action Option -GD (-GetDaemon) <3.1.2_e1>`
- :ref:`A.2. Action Option -AC (-AddCheck) <3.2.1_e2>`
- :ref:`A.3. Action Option -AC (-AddCheck) <3.2.1_e3>`
- :ref:`A.4. Action Option -AC (-AddCheck) <3.2.1_e4>`



| :ref:`Back to Top <section3>`
| :ref:`Back to Table of Contents <index>`
