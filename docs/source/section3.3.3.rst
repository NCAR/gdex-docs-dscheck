
.. _section3.3.3:

3.3.3 - Email Check
=================================


.. _EC:

Action Option -**EC** (-**EmailCheck**) :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

sends an email to a specialist with the current status
of all their check records, unless more specific conditions are provided.

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

Any error messages recorded in the check record are included in the email.



| :ref:`Back to Top <section3.3.3>`
| :ref:`Back to Table of Contents <index>`
