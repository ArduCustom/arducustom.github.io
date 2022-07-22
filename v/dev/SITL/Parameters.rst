.. Dynamically generated list of documented parameters
.. This page was generated using Tools\/autotest\/param\_metadata\/param\_parse\.py

.. DO NOT EDIT


.. _parameters:

SITL Parameter List
===================

SITL parameters



.. _parameters_SIM_:

SIM\_ Parameters
----------------


.. _SIM_BARO_RND:

SIM\_BARO\_RND: Baro Noise
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Amount of \(evenly\-distributed\) noise injected into the 1st baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_BARO_GLITCH:

SIM\_BARO\_GLITCH: Baro Glitch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Glitch for 1st baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_BAR2_RND:

SIM\_BAR2\_RND: Baro2 Noise
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Amount of \(evenly\-distributed\) noise injected into the 2nd baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_BAR2_GLITCH:

SIM\_BAR2\_GLITCH: Baro2 Glitch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Glitch for 2nd baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_BAR3_RND:

SIM\_BAR3\_RND: Baro3 Noise
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Amount of \(evenly\-distributed\) noise injected into the 3rd baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_BAR3_GLITCH:

SIM\_BAR3\_GLITCH: Baro3 Glitch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Glitch for 2nd baro


+--------+
| Units  |
+========+
| meters |
+--------+




.. _SIM_SAIL_TYPE:

SIM\_SAIL\_TYPE: Sailboat simulation sail type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: mainsail with sheet\, 1\: directly actuated wing


.. _SIM_JSON_MASTER:

SIM\_JSON\_MASTER: JSON master instance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


the instance number to  take servos from


.. _SIM_OH_MASK:

SIM\_OH\_MASK: SIM\-on\_hardware Output Enable Mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


channels which are passed through to actual hardware when running on actual hardware



.. _parameters_SIM_GRPE_:

SIM\_GRPE\_ Parameters
----------------------


.. _SIM_GRPE_ENABLE:

SIM\_GRPE\_ENABLE: Gripper servo Sim enable\/disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Allows you to enable \(1\) or disable \(0\) the gripper servo simulation


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | Enabled  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SIM_GRPE_PIN:

SIM\_GRPE\_PIN: Gripper emp pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The pin number that the gripper emp is connected to\. \(start at 1\)


+---------+
| Range   |
+=========+
| 0 to 15 |
+---------+





.. _parameters_SIM_GRPS_:

SIM\_GRPS\_ Parameters
----------------------


.. _SIM_GRPS_ENABLE:

SIM\_GRPS\_ENABLE: Gripper servo Sim enable\/disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Allows you to enable \(1\) or disable \(0\) the gripper servo simulation


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | Enabled  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SIM_GRPS_PIN:

SIM\_GRPS\_PIN: Gripper servo pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The pin number that the gripper servo is connected to\. \(start at 1\)


+---------+
| Range   |
+=========+
| 0 to 15 |
+---------+




.. _SIM_GRPS_GRAB:

SIM\_GRPS\_GRAB: Gripper Grab PWM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM value in microseconds sent to Gripper to initiate grabbing the cargo


+--------------+---------------------+
| Range        | Units               |
+==============+=====================+
| 1000 to 2000 | PWM in microseconds |
+--------------+---------------------+




.. _SIM_GRPS_RELEASE:

SIM\_GRPS\_RELEASE: Gripper Release PWM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM value in microseconds sent to Gripper to release the cargo


+--------------+---------------------+
| Range        | Units               |
+==============+=====================+
| 1000 to 2000 | PWM in microseconds |
+--------------+---------------------+




.. _SIM_GRPS_REVERSE:

SIM\_GRPS\_REVERSE: Gripper close direction
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse the closing direction\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Normal  | |
| +-------+---------+ |
| | 1     | Reverse | |
| +-------+---------+ |
|                     |
+---------------------+





.. _parameters_SIM_PLD_:

SIM\_PLD\_ Parameters
---------------------


.. _SIM_PLD_ENABLE:

SIM\_PLD\_ENABLE: Preland device Sim enable\/disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Allows you to enable \(1\) or disable \(0\) the Preland simulation


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | Enabled  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SIM_PLD_LAT:

SIM\_PLD\_LAT: Precland device origin\'s latitude
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device origin\'s latitude


+-----------+-----------+---------+
| Increment | Range     | Units   |
+===========+===========+=========+
| 0.000001  | -90 to 90 | degrees |
+-----------+-----------+---------+




.. _SIM_PLD_LON:

SIM\_PLD\_LON: Precland device origin\'s longitude
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device origin\'s longitude


+-----------+-------------+---------+
| Increment | Range       | Units   |
+===========+=============+=========+
| 0.000001  | -180 to 180 | degrees |
+-----------+-------------+---------+




.. _SIM_PLD_HEIGHT:

SIM\_PLD\_HEIGHT: Precland device origin\'s height above sealevel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device origin\'s height above sealevel assume a 2x2m square as station base


+-----------+------------+-------------+
| Increment | Range      | Units       |
+===========+============+=============+
| 1         | 0 to 10000 | centimeters |
+-----------+------------+-------------+




.. _SIM_PLD_YAW:

SIM\_PLD\_YAW: Precland device systems rotation from north
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device systems rotation from north


+-----------+--------------+---------+
| Increment | Range        | Units   |
+===========+==============+=========+
| 1         | -180 to +180 | degrees |
+-----------+--------------+---------+




.. _SIM_PLD_RATE:

SIM\_PLD\_RATE: Precland device update rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device rate\. e\.g led patter refresh rate\, RF message rate\, etc\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 0 to 200 | hertz |
+----------+-------+




.. _SIM_PLD_TYPE:

SIM\_PLD\_TYPE: Precland device radiance type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device radiance type\: it can be a cylinder\, a cone\, or a sphere\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | cylinder | |
| +-------+----------+ |
| | 1     | cone     | |
| +-------+----------+ |
| | 2     | sphere   | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SIM_PLD_ALT_LIMIT:

SIM\_PLD\_ALT\_LIMIT: Precland device alt range
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device maximum range altitude


+----------+--------+
| Range    | Units  |
+==========+========+
| 0 to 100 | meters |
+----------+--------+




.. _SIM_PLD_DIST_LIMIT:

SIM\_PLD\_DIST\_LIMIT: Precland device lateral range
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device maximum lateral range


+----------+--------+
| Range    | Units  |
+==========+========+
| 5 to 100 | meters |
+----------+--------+




.. _SIM_PLD_ORIENT:

SIM\_PLD\_ORIENT: Precland device orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Precland device orientation vector


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Front   | |
| +-------+---------+ |
| | 4     | Back    | |
| +-------+---------+ |
| | 24    | Up      | |
| +-------+---------+ |
|                     |
+---------------------+





.. _parameters_SIM_SPR_:

SIM\_SPR\_ Parameters
---------------------


.. _SIM_SPR_ENABLE:

SIM\_SPR\_ENABLE: Sprayer Sim enable\/disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Allows you to enable \(1\) or disable \(0\) the Sprayer simulation


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | Enabled  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SIM_SPR_PUMP:

SIM\_SPR\_PUMP: Sprayer pump pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The pin number that the Sprayer pump is connected to\. \(start at 1\)


+---------+
| Range   |
+=========+
| 0 to 15 |
+---------+




.. _SIM_SPR_SPIN:

SIM\_SPR\_SPIN: Sprayer spinner servo pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The pin number that the Sprayer spinner servo is connected to\. \(start at 1\)


+---------+
| Range   |
+=========+
| 0 to 15 |
+---------+



