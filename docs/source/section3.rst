
.. _section3:

3 - ACTION OPTIONS
=================================

Action options are used to specify what task 'dscheck' executes. No values
are allowed to follow Action options. Multiple Action options provided
simultaneously are blocked.

Based on the information being manipulated, the actions are divided into three
categories:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Daemon Control Actions <section3.1>`
     - create, delete, modify and view daemon control information in GDEXDB, of specified specialist, command and hostname
   * - :ref:`Check Actions <section3.2>`
     - add, delete, unlock and view check information of the active individual checks
   * - :ref:`Check Process Actions <section3.3>`
     - process checks by starting commands on remote hosts as configured in daemon controls and purge checks by recording the commands and their execution information into check history; interrupt the current executing commands by killing the current process and its all children; and email status of current checks
   * - :ref:`Daemon Host Connectivity <section3.4>`
     - check connectivity of daemon hosts for specialists

.. toctree::
   :maxdepth: 2
   :caption: Table of Contents

   section3.1
   section3.2
   section3.3
   section3.4
   section3.5

**Appendix A: List of Examples**

- :ref:`A.1. Action Option -SD (-SetDaemon) <3.1.1_e1>`
- :ref:`A.2. Action Option -GD (-GetDaemon) <3.1.2_e2>`
- :ref:`A.3. Action Option -AC (-AddCheck) <3.2.1_e3>`
- :ref:`A.4. Action Option -AC (-AddCheck) <3.2.1_e4>`
- :ref:`A.5. Action Option -AC (-AddCheck) <3.2.1_e5>`



| :ref:`Back to Top <section3>`
| :ref:`Back to Table of Contents <index>`
