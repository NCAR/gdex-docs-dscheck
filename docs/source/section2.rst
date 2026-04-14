
.. _section2:

2 - GENERAL DSCHECK USAGE
=================================

| **dscheck** [:ref:`Action Option <section3>`] [:ref:`Mode Options <section4>`] [:ref:`Info Options <section5>`]
|         or
| **dscheck** [:ref:`-(IF|InputFile) <IF>`] InputFileNames

Brackets [] indicate optional elements. A pipe '|' within parentheses, as in
(A|B), means either A or B may be used. Options fall into three categories:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - :ref:`Action options <section3>`
     - specify the task to execute
   * - :ref:`Mode options <section4>`
     - modify how an action behaves
   * - :ref:`Info options <section5>`
     - pass one or more values to the action

An option can be given in short or long form — for example, :ref:`-DS <DS>` or -Dataset.
Some options have alias names for convenience; for example, -UnLock is an alias
for :ref:`Mode option <section4>` :ref:`-UL <UL>` (-UnLockCheck). Option names are case-insensitive, but
values following :ref:`Info options <section5>` are case-sensitive.

Specify exactly one :ref:`Action option <section3>` per **dscheck** invocation. Based on the chosen
action, certain :ref:`Info options <section5>` are required, others are optional, and specific
:ref:`Mode options <section4>` may be used to alter the action's behavior.

All options except :ref:`-IF <IF>` (-InputFile) may be given either on the command line or
in input files. Input file names are provided via :ref:`-IF <IF>` and can only be specified
on the command line. See the :ref:`-IF <IF>` option description for details on how to format
options in input files. One or more input files may be combined with command-line
options. The option name :ref:`-IF <IF>` itself may be omitted when a single input file is
given on the command line and all other options are contained within that file.

When retrieving daemon or check information, :ref:`Info options <section5>` serve as query filters.
Four special characters can refine queries further — quote or escape them on the
command line to prevent shell interpretation:

.. list-table::
   :widths: auto
   :header-rows: 0

   * - '!'
     - exclude matches; must appear immediately after the option name
   * - '<'
     - less-than comparison on the following value
   * - '>'
     - greater-than comparison on the following value
   * - '<>'
     - range between the following two values

Combining '!' and '<' as "'!' '<' OptionValue" expresses a 'greater than or
equal to OptionValue' condition.

The description of an individual option is shown when **dscheck** is run as

| **dscheck** [Option] -(h|help) [Option]

A description is shown for the option placed either before or after -(h|help).
If no option is specified, or **dscheck** is run without arguments, the full
document is displayed via the UNIX utility 'more'. A hard copy of this document
can be printed from the saved file, dscheck.usg, under python package
rda_python_dscheck.



| :ref:`Back to Top <section2>`
| :ref:`Back to Table of Contents <index>`
