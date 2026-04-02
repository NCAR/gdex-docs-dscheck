
.. _section2:

2 - GENERAL DSCHECK USAGE
=================================

| **dscheck** [:ref:`Action Option <section3>`] [:ref:`Mode Options <section4>`] [:ref:`Info Options <section5>`]
|        or
| **dscheck** [:ref:`-(IF|InputFile) <IF>`] InputFileNames

Quotes [] indicate optional. A pipeline '|' in parentheses as in format (A|B)
means either A or B can be used. The options applied to **dscheck** are divided
into three categories, :ref:`Action <section3>`, :ref:`Mode <section4>`, and Information (:ref:`Info <section5>` for short) options.
:ref:`Action options <section3>` are used to specify what task this utility program is to execute,
:ref:`Mode options <section4>` are used to modify behaviors of the actions, and the :ref:`Info <section5>` options
are used to pass information, one or multiple values, to run **dscheck**. An option
can be given in form of either short name or long name, :ref:`-DS <DS>` or -Dataset for
example. Some options have alias names for convenience; -UnLock, for example,
is an alias option name for :ref:`Mode option <section4>` :ref:`-UL <UL>` (-UnLockCheck). Option names can be
given in either upper or lower cases, while the values following :ref:`Info <section5>` options
are case sensitive.

Specify one of the :ref:`Action options <section3>` each time to execute **dscheck**. Based on what
:ref:`Action <section3>` is chosen, some of the :ref:`Info options <section5>` are mandatory and others are optional
and certain :ref:`Mode options <section4>` can be applied to alter the behaviors of the :ref:`Action <section3>`.

All options, except :ref:`Info option <section5>` :ref:`-IF <IF>` (-InputFile), can be given either on command
line or in input files. Input file names are presented per :ref:`Info option <section5>` :ref:`-IF <IF>` and
can only be provided on command line. Refer to the description of :ref:`Info option <section5>` :ref:`-IF <IF>`
(-InputFile) for details on how to present options in input files.  One or multiple
input files, combined with options on command line, are allowed to run **dscheck**.
The option name, :ref:`-IF <IF>` (-InputFile), itself can be omitted if a single input file is
given on command line and all other option information are provided inside the
input file.

When information of daemons and checks are retrieved, :ref:`Info options <section5>` are used to
specify conditions for querying information from GDEXDB. Some special signs can be
used to further confine the information with special and complicated conditions;
they are '!', '<', '>' and '<>'.  These special signs, if provided on command
line,  must be quoted or escaped to avoid being interpreted by the Unix shell.
The '!', or \!, means exclusion to the following value(s) and it must be the
first item following an :ref:`Info option <section5>` name, while '<' or '>' mean greater or less
than the following value and '<>' means between the following two values.
Combine '!' and '<', as syntax "'!' '<' OptionValue", to make a condition of
'larger than or equal to OptionValue'.

Description of an individual option is displayed if **dscheck** is issued on
command line as

| **dscheck** [Option] -(h|help) [Option]

A description is displayed for an option given either before or after -(h|help).
If no option is specified or **dscheck** is issued by itself, this whole document
is displayed via UNIX utility 'more'. A hard copy of this help document can be
printed from the saved file, dscheck.usg, under python package rda_python_dscheck.



| :ref:`Back to Top <section2>`
| :ref:`Back to Table of Contents <index>`
