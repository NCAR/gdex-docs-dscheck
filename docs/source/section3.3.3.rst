
.. _section3.3.3:

3.3.3 - Email Check
=================================


.. _EC:

Action Option -**EC** (-**EmailCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

sends an email to a specialist for the current status of all check
records owned by the specialist, unless more specific conditions are provided.

| **dscheck** -(EC|EmailCheck)
|           [:ref:`-(CI|CheckIndex) <CI>` CheckIndices]
|           [:ref:`-(CM|Command) <CM>` CommandNames]
|           [:ref:`-(AV|ArgumentVector) <AV>` ArgumentVectorStrings]
|           [:ref:`-(SN|Specialist) <SN>` SpecialistNames]
|           [:ref:`-(DS|Dataset) <DS>` DatasetNames]
|           [:ref:`-(CD|CheckDate) <CD>` CommandDate]
|           [:ref:`-(CT|CheckTime) <CT>` CommandTime]
|           [:ref:`-(WD|WorkDir) <WD>` WorkingDirectory]
|           [:ref:`-(CC|CarbonCopy) <CC>` Cc'dEmailAddresses]
|           [:ref:`-(DB|Debug) <DB>` DebugModeInfo]

Command error messages are included too if any error messages are recorded in
the check record.



| :ref:`Back to Top <section3.3.3>`
| :ref:`Back to Table of Contents <index>`
