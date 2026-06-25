
.. _section2.1:

2.1 - Quick Start
=================================

Show the full document, paged through 'more':

.. code-block:: none

   dscheck

Show the description of a single option:

.. code-block:: none

   dscheck -h -AC

List your own daemon control records:

.. code-block:: none

   dscheck -GD

List your own active check records:

.. code-block:: none

   dscheck -GC

Add a deferred run of a script on PBS:

.. code-block:: none

   dscheck -AC -CM myscript.sh -HN PBS

Email yourself the status of all your active checks:

.. code-block:: none

   dscheck -EC

Start the dscheck driver as a long-running daemon (typical for the operator):

.. code-block:: none

   dscheck -PC -DM start

Or run the dscheck driver from crontab every minute (lightweight alternative):

.. code-block:: none

   * * * * * dscheck -PC



| :ref:`Back to Top <section2.1>`
| :ref:`Back to Table of Contents <index>`
