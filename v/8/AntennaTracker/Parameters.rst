.. Dynamically generated list of documented parameters
.. This page was generated using Tools\/autotest\/param\_metadata\/param\_parse\.py

.. DO NOT EDIT


.. _parameters:

Complete Parameter List
=======================

This is a complete list of the parameters which can be set \(e\.g\. via the MAVLink protocol\) to control vehicle behaviour\. They are stored in persistent storage on the vehicle\.

This list is automatically generated from the latest ardupilot source code\, and so may contain parameters which are not yet in the stable released versions of the code\.




.. _parameters_AntennaTracker:

AntennaTracker Parameters
-------------------------


.. _FORMAT_VERSION:

FORMAT\_VERSION: Eeprom format version number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This value is incremented when changes are made to the eeprom format


.. _SYSID_THISMAV:

SYSID\_THISMAV: MAVLink system ID of this vehicle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Allows setting an individual system id for this vehicle to distinguish it from others on the same network


+---------+
| Range   |
+=========+
| 1 - 255 |
+---------+




.. _SYSID_MYGCS:

SYSID\_MYGCS: Ground station MAVLink system ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The identifier of the ground station in the MAVLink protocol\. Don\'t change this unless you also modify the ground station to match\.


+---------+
| Range   |
+=========+
| 1 - 255 |
+---------+




.. _SYSID_TARGET:

SYSID\_TARGET: Target vehicle\'s MAVLink system ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The identifier of the vehicle being tracked\. This should be zero \(to auto detect\) or be the same as the SYSID\_THISMAV parameter of the vehicle being tracked\.


+---------+
| Range   |
+=========+
| 1 - 255 |
+---------+




.. _YAW_SLEW_TIME:

YAW\_SLEW\_TIME: Time for yaw to slew through its full range
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls how rapidly the tracker will change the servo output for yaw\. It is set as the number of seconds to do a full rotation\. You can use this parameter to slow the trackers movements\, which may help with some types of trackers\. A value of zero will allow for unlimited servo movement per update\.


+-----------+--------+---------+
| Increment | Range  | Units   |
+===========+========+=========+
| 0.1       | 0 - 20 | seconds |
+-----------+--------+---------+




.. _PITCH_SLEW_TIME:

PITCH\_SLEW\_TIME: Time for pitch to slew through its full range
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls how rapidly the tracker will change the servo output for pitch\. It is set as the number of seconds to do a full range of pitch movement\. You can use this parameter to slow the trackers movements\, which may help with some types of trackers\. A value of zero will allow for unlimited servo movement per update\.


+-----------+--------+---------+
| Increment | Range  | Units   |
+===========+========+=========+
| 0.1       | 0 - 20 | seconds |
+-----------+--------+---------+




.. _MIN_REVERSE_TIME:

MIN\_REVERSE\_TIME: Minimum time to apply a yaw reversal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


When the tracker detects it has reached the limit of servo movement in yaw it will reverse and try moving to the other extreme of yaw\. This parameter controls the minimum time it should reverse for\. It is used to cope with trackers that have a significant lag in movement to ensure they do move all the way around\.


+-----------+--------+---------+
| Increment | Range  | Units   |
+===========+========+=========+
| 1         | 0 - 20 | seconds |
+-----------+--------+---------+




.. _START_LATITUDE:

START\_LATITUDE: Initial Latitude before GPS lock
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Combined with START\_LONGITUDE this parameter allows for an initial position of the tracker to be set\. This position will be used until the GPS gets lock\. It can also be used to run a stationary tracker with no GPS attached\.


+-----------+----------+---------+
| Increment | Range    | Units   |
+===========+==========+=========+
| 0.000001  | -90 - 90 | degrees |
+-----------+----------+---------+




.. _START_LONGITUDE:

START\_LONGITUDE: Initial Longitude before GPS lock
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Combined with START\_LATITUDE this parameter allows for an initial position of the tracker to be set\. This position will be used until the GPS gets lock\. It can also be used to run a stationary tracker with no GPS attached\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 0.000001  | -180 - 180 | degrees |
+-----------+------------+---------+




.. _STARTUP_DELAY:

STARTUP\_DELAY: Delay before first servo movement from trim
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This parameter can be used to force the servos to their trim value for a time on startup\. This can help with some servo types


+-----------+--------+---------+
| Increment | Range  | Units   |
+===========+========+=========+
| 0.1       | 0 - 10 | seconds |
+-----------+--------+---------+




.. _SERVO_PITCH_TYPE:

SERVO\_PITCH\_TYPE: Type of servo system being used for pitch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This allows selection of position servos or on\/off servos for pitch


+--------------------------------+
| Values                         |
+================================+
| +-------+--------------------+ |
| | Value | Meaning            | |
| +=======+====================+ |
| | 0     | Position           | |
| +-------+--------------------+ |
| | 1     | OnOff              | |
| +-------+--------------------+ |
| | 2     | ContinuousRotation | |
| +-------+--------------------+ |
|                                |
+--------------------------------+




.. _SERVO_YAW_TYPE:

SERVO\_YAW\_TYPE: Type of servo system being used for yaw
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This allows selection of position servos or on\/off servos for yaw


+--------------------------------+
| Values                         |
+================================+
| +-------+--------------------+ |
| | Value | Meaning            | |
| +=======+====================+ |
| | 0     | Position           | |
| +-------+--------------------+ |
| | 1     | OnOff              | |
| +-------+--------------------+ |
| | 2     | ContinuousRotation | |
| +-------+--------------------+ |
|                                |
+--------------------------------+




.. _ONOFF_YAW_RATE:

ONOFF\_YAW\_RATE: Yaw rate for on\/off servos
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Rate of change of yaw in degrees\/second for on\/off servos


+-----------+--------+--------------------+
| Increment | Range  | Units              |
+===========+========+====================+
| 0.1       | 0 - 50 | degrees per second |
+-----------+--------+--------------------+




.. _ONOFF_PITCH_RATE:

ONOFF\_PITCH\_RATE: Pitch rate for on\/off servos
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Rate of change of pitch in degrees\/second for on\/off servos


+-----------+--------+--------------------+
| Increment | Range  | Units              |
+===========+========+====================+
| 0.1       | 0 - 50 | degrees per second |
+-----------+--------+--------------------+




.. _ONOFF_YAW_MINT:

ONOFF\_YAW\_MINT: Yaw minimum movement time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Minimum amount of time in seconds to move in yaw


+-----------+-------+---------+
| Increment | Range | Units   |
+===========+=======+=========+
| 0.01      | 0 - 2 | seconds |
+-----------+-------+---------+




.. _ONOFF_PITCH_MINT:

ONOFF\_PITCH\_MINT: Pitch minimum movement time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Minimim amount of time in seconds to move in pitch


+-----------+-------+---------+
| Increment | Range | Units   |
+===========+=======+=========+
| 0.01      | 0 - 2 | seconds |
+-----------+-------+---------+




.. _YAW_TRIM:

YAW\_TRIM: Yaw trim
~~~~~~~~~~~~~~~~~~~


Amount of extra yaw to add when tracking\. This allows for small adjustments for an out of trim compass\.


+-----------+----------+---------+
| Increment | Range    | Units   |
+===========+==========+=========+
| 0.1       | -10 - 10 | degrees |
+-----------+----------+---------+




.. _PITCH_TRIM:

PITCH\_TRIM: Pitch trim
~~~~~~~~~~~~~~~~~~~~~~~


Amount of extra pitch to add when tracking\. This allows for small adjustments for a badly calibrated barometer\.


+-----------+----------+---------+
| Increment | Range    | Units   |
+===========+==========+=========+
| 0.1       | -10 - 10 | degrees |
+-----------+----------+---------+




.. _YAW_RANGE:

YAW\_RANGE: Yaw Angle Range
~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis total range of motion in degrees


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 0.1       | 0 - 360 | degrees |
+-----------+---------+---------+




.. _DISTANCE_MIN:

DISTANCE\_MIN: Distance minimum to target
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Tracker will track targets at least this distance away


+-----------+---------+--------+
| Increment | Range   | Units  |
+===========+=========+========+
| 1         | 0 - 100 | meters |
+-----------+---------+--------+




.. _ALT_SOURCE:

ALT\_SOURCE: Altitude Source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What provides altitude information for vehicle\. Vehicle only assumes tracker has same altitude as vehicle\'s home


+------------------------------+
| Values                       |
+==============================+
| +-------+------------------+ |
| | Value | Meaning          | |
| +=======+==================+ |
| | 0     | Barometer        | |
| +-------+------------------+ |
| | 1     | GPS              | |
| +-------+------------------+ |
| | 2     | GPS vehicle only | |
| +-------+------------------+ |
|                              |
+------------------------------+




.. _MAV_UPDATE_RATE:

MAV\_UPDATE\_RATE: Mavlink Update Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The rate at which Mavlink updates position and baro data


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 1 - 10 | hertz |
+-----------+--------+-------+




.. _PITCH_MIN:

PITCH\_MIN: Minimum Pitch Angle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The lowest angle the pitch can reach


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | -90 - 0 | degrees |
+-----------+---------+---------+




.. _PITCH_MAX:

PITCH\_MAX: Maximum Pitch Angle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The highest angle the pitch can reach


+-----------+--------+---------+
| Increment | Range  | Units   |
+===========+========+=========+
| 1         | 0 - 90 | degrees |
+-----------+--------+---------+




.. _LOG_BITMASK:

LOG\_BITMASK: Log bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~


4 byte bitmap of log types to enable


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | ATTITUDE | |
| +-----+----------+ |
| | 1   | GPS      | |
| +-----+----------+ |
| | 2   | RCIN     | |
| +-----+----------+ |
| | 3   | IMU      | |
| +-----+----------+ |
| | 4   | RCOUT    | |
| +-----+----------+ |
| | 5   | COMPASS  | |
| +-----+----------+ |
| | 6   | Battery  | |
| +-----+----------+ |
|                    |
+--------------------+




.. _PITCH2SRV_P:

PITCH2SRV\_P: Pitch axis controller P gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller P gain\.  Converts the difference between desired pitch angle and actual pitch angle into a pitch servo pwm change


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| 0.01      | 0.0 - 3.0 |
+-----------+-----------+




.. _PITCH2SRV_I:

PITCH2SRV\_I: Pitch axis controller I gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller I gain\.  Corrects long\-term difference in desired pitch angle vs actual pitch angle


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| 0.01      | 0.0 - 3.0 |
+-----------+-----------+




.. _PITCH2SRV_IMAX:

PITCH2SRV\_IMAX: Pitch axis controller I gain maximum
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller I gain maximum\.  Constrains the maximum pwm change that the I gain will output


+-----------+----------+-------------+
| Increment | Range    | Units       |
+===========+==========+=============+
| 10        | 0 - 4000 | decipercent |
+-----------+----------+-------------+




.. _PITCH2SRV_D:

PITCH2SRV\_D: Pitch axis controller D gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller D gain\.  Compensates for short\-term change in desired pitch angle vs actual pitch angle


+-----------+-------------+
| Increment | Range       |
+===========+=============+
| 0.001     | 0.001 - 0.1 |
+-----------+-------------+




.. _PITCH2SRV_FF:

PITCH2SRV\_FF: Pitch axis controller feed forward
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller feed forward


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 0.001     | 0 - 0.5 |
+-----------+---------+




.. _PITCH2SRV_FLTT:

PITCH2SRV\_FLTT: Pitch axis controller target frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller target frequency in Hz


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 1 - 50 | hertz |
+-----------+--------+-------+




.. _PITCH2SRV_FLTE:

PITCH2SRV\_FLTE: Pitch axis controller error frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller error frequency in Hz


+-----------+---------+-------+
| Increment | Range   | Units |
+===========+=========+=======+
| 1         | 1 - 100 | hertz |
+-----------+---------+-------+




.. _PITCH2SRV_FLTD:

PITCH2SRV\_FLTD: Pitch axis controller derivative frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Pitch axis controller derivative frequency in Hz


+-----------+---------+-------+
| Increment | Range   | Units |
+===========+=========+=======+
| 1         | 1 - 100 | hertz |
+-----------+---------+-------+




.. _PITCH2SRV_SMAX:

PITCH2SRV\_SMAX: Pitch slew rate limit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Sets an upper limit on the slew rate produced by the combined P and D gains\. If the amplitude of the control action produced by the rate feedback exceeds this value\, then the D\+P gain is reduced to respect the limit\. This limits the amplitude of high frequency oscillations caused by an excessive gain\. The limit should be set to no more than 25\% of the actuators maximum slew rate to allow for load effects\. Note\: The gain will not be reduced to less than 10\% of the nominal value\. A value of zero will disable this feature\.


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 0.5       | 0 - 200 |
+-----------+---------+




.. _YAW2SRV_P:

YAW2SRV\_P: Yaw axis controller P gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller P gain\.  Converts the difference between desired yaw angle \(heading\) and actual yaw angle into a yaw servo pwm change


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| 0.01      | 0.0 - 3.0 |
+-----------+-----------+




.. _YAW2SRV_I:

YAW2SRV\_I: Yaw axis controller I gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller I gain\.  Corrects long\-term difference in desired yaw angle \(heading\) vs actual yaw angle


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| 0.01      | 0.0 - 3.0 |
+-----------+-----------+




.. _YAW2SRV_IMAX:

YAW2SRV\_IMAX: Yaw axis controller I gain maximum
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller I gain maximum\.  Constrains the maximum pwm change that the I gain will output


+-----------+----------+-------------+
| Increment | Range    | Units       |
+===========+==========+=============+
| 10        | 0 - 4000 | decipercent |
+-----------+----------+-------------+




.. _YAW2SRV_D:

YAW2SRV\_D: Yaw axis controller D gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller D gain\.  Compensates for short\-term change in desired yaw angle \(heading\) vs actual yaw angle


+-----------+-------------+
| Increment | Range       |
+===========+=============+
| 0.001     | 0.001 - 0.1 |
+-----------+-------------+




.. _YAW2SRV_FF:

YAW2SRV\_FF: Yaw axis controller feed forward
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller feed forward


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 0.001     | 0 - 0.5 |
+-----------+---------+




.. _YAW2SRV_FLTT:

YAW2SRV\_FLTT: Yaw axis controller target frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller target frequency in Hz


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 1 - 50 | hertz |
+-----------+--------+-------+




.. _YAW2SRV_FLTE:

YAW2SRV\_FLTE: Yaw axis controller error frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller error frequency in Hz


+-----------+---------+-------+
| Increment | Range   | Units |
+===========+=========+=======+
| 1         | 1 - 100 | hertz |
+-----------+---------+-------+




.. _YAW2SRV_FLTD:

YAW2SRV\_FLTD: Yaw axis controller derivative frequency in Hz
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Yaw axis controller derivative frequency in Hz


+-----------+---------+-------+
| Increment | Range   | Units |
+===========+=========+=======+
| 1         | 1 - 100 | hertz |
+-----------+---------+-------+




.. _YAW2SRV_SMAX:

YAW2SRV\_SMAX: Yaw slew rate limit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Sets an upper limit on the slew rate produced by the combined P and D gains\. If the amplitude of the control action produced by the rate feedback exceeds this value\, then the D\+P gain is reduced to respect the limit\. This limits the amplitude of high frequency oscillations caused by an excessive gain\. The limit should be set to no more than 25\% of the actuators maximum slew rate to allow for load effects\. Note\: The gain will not be reduced to less than 10\% of the nominal value\. A value of zero will disable this feature\.


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 0.5       | 0 - 200 |
+-----------+---------+




.. _CMD_TOTAL:

CMD\_TOTAL: Number of loaded mission items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set to 1 if HOME location has been loaded by the ground station\. Do not change this manually\.


+---------+
| Range   |
+=========+
| 1 - 255 |
+---------+




.. _GCS_PID_MASK:

GCS\_PID\_MASK: GCS PID tuning mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

bitmask of PIDs to send MAVLink PID\_TUNING messages for


+-------------------+---------------------+
| Bitmask           | Values              |
+===================+=====================+
| +-----+---------+ | +-------+---------+ |
| | Bit | Meaning | | | Value | Meaning | |
| +=====+=========+ | +=======+=========+ |
| | 0   | Pitch   | | | 0     | None    | |
| +-----+---------+ | +-------+---------+ |
| | 1   | Yaw     | | | 1     | Pitch   | |
| +-----+---------+ | +-------+---------+ |
|                   | | 2     | Yaw     | |
|                   | +-------+---------+ |
|                   |                     |
+-------------------+---------------------+




.. _SCAN_SPEED_YAW:

SCAN\_SPEED\_YAW: Speed at which to rotate the yaw axis in scan mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls how rapidly the tracker will move the servos in SCAN mode


+-----------+---------+--------------------+
| Increment | Range   | Units              |
+===========+=========+====================+
| 1         | 0 - 100 | degrees per second |
+-----------+---------+--------------------+




.. _SCAN_SPEED_PIT:

SCAN\_SPEED\_PIT: Speed at which to rotate pitch axis in scan mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls how rapidly the tracker will move the servos in SCAN mode


+-----------+---------+--------------------+
| Increment | Range   | Units              |
+===========+=========+====================+
| 1         | 0 - 100 | degrees per second |
+-----------+---------+--------------------+




.. _INITIAL_MODE:

INITIAL\_MODE: Mode tracker will switch into after initialization
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\:MANUAL\, 1\:STOP\, 2\:SCAN\, 10\:AUTO


.. _SAFE_DISARM_PWM:

SAFE\_DISARM\_PWM: PWM that will be output when disarmed or in stop mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\:zero pwm\, 1\:trim pwm


.. _AUTO_OPTIONS:

AUTO\_OPTIONS: Auto mode options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


1\: Scan for unknown target


+-----------------------------------+--------------------------------------------------+
| Bitmask                           | Values                                           |
+===================================+==================================================+
| +-----+-------------------------+ | +-------+--------------------------------------+ |
| | Bit | Meaning                 | | | Value | Meaning                              | |
| +=====+=========================+ | +=======+======================================+ |
| | 0   | Scan for unknown target | | | 0     | None                                 | |
| +-----+-------------------------+ | +-------+--------------------------------------+ |
|                                   | | 1     | Scan for unknown target in auto mode | |
|                                   | +-------+--------------------------------------+ |
|                                   |                                                  |
+-----------------------------------+--------------------------------------------------+





.. _parameters_AHRS_:

AHRS\_ Parameters
-----------------


.. _AHRS_GPS_GAIN:

AHRS\_GPS\_GAIN: AHRS GPS gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls how much to use the GPS to correct the attitude\. This should never be set to zero for a plane as it would result in the plane losing control in turns\. For a plane please use the default value of 1\.0\.


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| .01       | 0.0 - 1.0 |
+-----------+-----------+




.. _AHRS_GPS_USE:

AHRS\_GPS\_USE: AHRS use GPS for DCM navigation and position\-down
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls whether to use dead\-reckoning or GPS based navigation\. If set to 0 then the GPS won\'t be used for navigation\, and only dead reckoning will be used\. A value of zero should never be used for normal flight\. Currently this affects only the DCM\-based AHRS\: the EKF uses GPS according to its own parameters\. A value of 2 means to use GPS for height as well as position \- both in DCM estimation and when determining altitude\-above\-home\.


+-------------------------------------------------+
| Values                                          |
+=================================================+
| +-------+-------------------------------------+ |
| | Value | Meaning                             | |
| +=======+=====================================+ |
| | 0     | Disabled                            | |
| +-------+-------------------------------------+ |
| | 1     | Use GPS for DCM position            | |
| +-------+-------------------------------------+ |
| | 2     | Use GPS for DCM position and height | |
| +-------+-------------------------------------+ |
|                                                 |
+-------------------------------------------------+




.. _AHRS_YAW_P:

AHRS\_YAW\_P: Yaw P
~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls the weight the compass or GPS has on the heading\. A higher value means the heading will track the yaw source \(GPS or compass\) more rapidly\.


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| .01       | 0.1 - 0.4 |
+-----------+-----------+




.. _AHRS_RP_P:

AHRS\_RP\_P: AHRS RP\_P
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls how fast the accelerometers correct the attitude


+-----------+-----------+
| Increment | Range     |
+===========+===========+
| .01       | 0.1 - 0.4 |
+-----------+-----------+




.. _AHRS_WIND_MAX:

AHRS\_WIND\_MAX: Maximum wind
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the maximum allowable difference between ground speed and airspeed\. This allows the plane to cope with a failing airspeed sensor\. A value of zero means to use the airspeed as is\. See ARSPD\_OPTIONS and ARSPD\_MAX\_WIND to disable airspeed sensors\.


+-----------+---------+-------------------+
| Increment | Range   | Units             |
+===========+=========+===================+
| 1         | 0 - 127 | meters per second |
+-----------+---------+-------------------+




.. _AHRS_TRIM_X:

AHRS\_TRIM\_X: AHRS Trim Roll
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Compensates for the roll angle difference between the control board and the frame\. Positive values make the vehicle roll right\.


+-----------+-------------------+---------+
| Increment | Range             | Units   |
+===========+===================+=========+
| 0.01      | -0.1745 - +0.1745 | radians |
+-----------+-------------------+---------+




.. _AHRS_TRIM_Y:

AHRS\_TRIM\_Y: AHRS Trim Pitch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Compensates for the pitch angle difference between the control board and the frame\. Positive values make the vehicle pitch up\/back\.


+-----------+-------------------+---------+
| Increment | Range             | Units   |
+===========+===================+=========+
| 0.01      | -0.1745 - +0.1745 | radians |
+-----------+-------------------+---------+




.. _AHRS_TRIM_Z:

AHRS\_TRIM\_Z: AHRS Trim Yaw
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Not Used


+-----------+-------------------+---------+
| Increment | Range             | Units   |
+===========+===================+=========+
| 0.01      | -0.1745 - +0.1745 | radians |
+-----------+-------------------+---------+




.. _AHRS_ORIENTATION:

AHRS\_ORIENTATION: Board Orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overall board orientation relative to the standard orientation for the board type\. This rotates the IMU and compass readings to allow the board to be oriented in your vehicle at any 90 or 45 degree angle\. The label for each option is specified in the order of rotations for that orientation\. This option takes affect on next boot\. After changing you will need to re\-level your vehicle\.


+----------------------------------+
| Values                           |
+==================================+
| +-------+----------------------+ |
| | Value | Meaning              | |
| +=======+======================+ |
| | 0     | None                 | |
| +-------+----------------------+ |
| | 1     | Yaw45                | |
| +-------+----------------------+ |
| | 2     | Yaw90                | |
| +-------+----------------------+ |
| | 3     | Yaw135               | |
| +-------+----------------------+ |
| | 4     | Yaw180               | |
| +-------+----------------------+ |
| | 5     | Yaw225               | |
| +-------+----------------------+ |
| | 6     | Yaw270               | |
| +-------+----------------------+ |
| | 7     | Yaw315               | |
| +-------+----------------------+ |
| | 8     | Roll180              | |
| +-------+----------------------+ |
| | 9     | Yaw45Roll180         | |
| +-------+----------------------+ |
| | 10    | Yaw90Roll180         | |
| +-------+----------------------+ |
| | 11    | Yaw135Roll180        | |
| +-------+----------------------+ |
| | 12    | Pitch180             | |
| +-------+----------------------+ |
| | 13    | Yaw225Roll180        | |
| +-------+----------------------+ |
| | 14    | Yaw270Roll180        | |
| +-------+----------------------+ |
| | 15    | Yaw315Roll180        | |
| +-------+----------------------+ |
| | 16    | Roll90               | |
| +-------+----------------------+ |
| | 17    | Yaw45Roll90          | |
| +-------+----------------------+ |
| | 18    | Yaw90Roll90          | |
| +-------+----------------------+ |
| | 19    | Yaw135Roll90         | |
| +-------+----------------------+ |
| | 20    | Roll270              | |
| +-------+----------------------+ |
| | 21    | Yaw45Roll270         | |
| +-------+----------------------+ |
| | 22    | Yaw90Roll270         | |
| +-------+----------------------+ |
| | 23    | Yaw135Roll270        | |
| +-------+----------------------+ |
| | 24    | Pitch90              | |
| +-------+----------------------+ |
| | 25    | Pitch270             | |
| +-------+----------------------+ |
| | 26    | Yaw90Pitch180        | |
| +-------+----------------------+ |
| | 27    | Yaw270Pitch180       | |
| +-------+----------------------+ |
| | 28    | Pitch90Roll90        | |
| +-------+----------------------+ |
| | 29    | Pitch90Roll180       | |
| +-------+----------------------+ |
| | 30    | Pitch90Roll270       | |
| +-------+----------------------+ |
| | 31    | Pitch180Roll90       | |
| +-------+----------------------+ |
| | 32    | Pitch180Roll270      | |
| +-------+----------------------+ |
| | 33    | Pitch270Roll90       | |
| +-------+----------------------+ |
| | 34    | Pitch270Roll180      | |
| +-------+----------------------+ |
| | 35    | Pitch270Roll270      | |
| +-------+----------------------+ |
| | 36    | Yaw90Pitch180Roll90  | |
| +-------+----------------------+ |
| | 37    | Yaw270Roll90         | |
| +-------+----------------------+ |
| | 38    | Yaw293Pitch68Roll180 | |
| +-------+----------------------+ |
| | 39    | Pitch315             | |
| +-------+----------------------+ |
| | 40    | Pitch315Roll90       | |
| +-------+----------------------+ |
| | 42    | Roll45               | |
| +-------+----------------------+ |
| | 43    | Roll315              | |
| +-------+----------------------+ |
| | 100   | Custom               | |
| +-------+----------------------+ |
|                                  |
+----------------------------------+




.. _AHRS_COMP_BETA:

AHRS\_COMP\_BETA: AHRS Velocity Complementary Filter Beta Coefficient
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls the time constant for the cross\-over frequency used to fuse AHRS \(airspeed and heading\) and GPS data to estimate ground velocity\. Time constant is 0\.1\/beta\. A larger time constant will use GPS data less and a small time constant will use air data less\.


+-----------+-------------+
| Increment | Range       |
+===========+=============+
| .01       | 0.001 - 0.5 |
+-----------+-------------+




.. _AHRS_GPS_MINSATS:

AHRS\_GPS\_MINSATS: AHRS GPS Minimum satellites
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Minimum number of satellites visible to use GPS for velocity based corrections attitude correction\. This defaults to 6\, which is about the point at which the velocity numbers from a GPS become too unreliable for accurate correction of the accelerometers\.


+-----------+--------+
| Increment | Range  |
+===========+========+
| 1         | 0 - 10 |
+-----------+--------+




.. _AHRS_EKF_TYPE:

AHRS\_EKF\_TYPE: Use NavEKF Kalman filter for attitude and position estimation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls which NavEKF Kalman filter version is used for attitude and position estimation


+--------------------------+
| Values                   |
+==========================+
| +-------+--------------+ |
| | Value | Meaning      | |
| +=======+==============+ |
| | 0     | Disabled     | |
| +-------+--------------+ |
| | 2     | Enable EKF2  | |
| +-------+--------------+ |
| | 3     | Enable EKF3  | |
| +-------+--------------+ |
| | 11    | ExternalAHRS | |
| +-------+--------------+ |
|                          |
+--------------------------+




.. _AHRS_CUSTOM_ROLL:

AHRS\_CUSTOM\_ROLL: Board orientation roll offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Autopilot mounting position roll offset\. Positive values \= roll right\, negative values \= roll left\. This parameter is only used when AHRS\_ORIENTATION is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+




.. _AHRS_CUSTOM_PIT:

AHRS\_CUSTOM\_PIT: Board orientation pitch offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Autopilot mounting position pitch offset\. Positive values \= pitch up\, negative values \= pitch down\. This parameter is only used when AHRS\_ORIENTATION is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+




.. _AHRS_CUSTOM_YAW:

AHRS\_CUSTOM\_YAW: Board orientation yaw offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Autopilot mounting position yaw offset\. Positive values \= yaw right\, negative values \= yaw left\. This parameter is only used when AHRS\_ORIENTATION is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+





.. _parameters_BARO:

BARO Parameters
---------------


.. _BARO1_GND_PRESS:

BARO1\_GND\_PRESS: Ground Pressure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

calibrated ground pressure in Pascals


+-----------+----------+--------+----------+
| Increment | ReadOnly | Units  | Volatile |
+===========+==========+========+==========+
| 1         | True     | pascal | True     |
+-----------+----------+--------+----------+




.. _BARO_GND_TEMP:

BARO\_GND\_TEMP: ground temperature
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

User provided ambient ground temperature in degrees Celsius\. This is used to improve the calculation of the altitude the vehicle is at\. This parameter is not persistent and will be reset to 0 every time the vehicle is rebooted\. A value of 0 means use the internal measurement ambient temperature\.


+-----------+-----------------+----------+
| Increment | Units           | Volatile |
+===========+=================+==========+
| 1         | degrees Celsius | True     |
+-----------+-----------------+----------+




.. _BARO_ALT_OFFSET:

BARO\_ALT\_OFFSET: altitude offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

altitude offset in meters added to barometric altitude\. This is used to allow for automatic adjustment of the base barometric altitude by a ground station equipped with a barometer\. The value is added to the barometric altitude read by the aircraft\. It is automatically reset to 0 when the barometer is calibrated on each reboot or when a preflight calibration is performed\.


+-----------+--------+
| Increment | Units  |
+===========+========+
| 0.1       | meters |
+-----------+--------+




.. _BARO_PRIMARY:

BARO\_PRIMARY: Primary barometer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This selects which barometer will be the primary if multiple barometers are found


+-----------------------+
| Values                |
+=======================+
| +-------+-----------+ |
| | Value | Meaning   | |
| +=======+===========+ |
| | 0     | FirstBaro | |
| +-------+-----------+ |
| | 1     | 2ndBaro   | |
| +-------+-----------+ |
| | 2     | 3rdBaro   | |
| +-------+-----------+ |
|                       |
+-----------------------+




.. _BARO_EXT_BUS:

BARO\_EXT\_BUS: External baro bus
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This selects the bus number for looking for an I2C barometer\. When set to \-1 it will probe all external i2c buses based on the GND\_PROBE\_EXT parameter\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | -1    | Disabled | |
| +-------+----------+ |
| | 0     | Bus0     | |
| +-------+----------+ |
| | 1     | Bus1     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BARO_SPEC_GRAV:

BARO\_SPEC\_GRAV: Specific Gravity \(For water depth measurement\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the specific gravity of the fluid when flying an underwater ROV\.


+------------------------+
| Values                 |
+========================+
| +-------+------------+ |
| | Value | Meaning    | |
| +=======+============+ |
| | 1.0   | Freshwater | |
| +-------+------------+ |
| | 1.024 | Saltwater  | |
| +-------+------------+ |
|                        |
+------------------------+




.. _BARO2_GND_PRESS:

BARO2\_GND\_PRESS: Ground Pressure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

calibrated ground pressure in Pascals


+-----------+----------+--------+----------+
| Increment | ReadOnly | Units  | Volatile |
+===========+==========+========+==========+
| 1         | True     | pascal | True     |
+-----------+----------+--------+----------+




.. _BARO3_GND_PRESS:

BARO3\_GND\_PRESS: Absolute Pressure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

calibrated ground pressure in Pascals


+-----------+----------+--------+----------+
| Increment | ReadOnly | Units  | Volatile |
+===========+==========+========+==========+
| 1         | True     | pascal | True     |
+-----------+----------+--------+----------+




.. _BARO_FLTR_RNG:

BARO\_FLTR\_RNG: Range in which sample is accepted
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the range around the average value that new samples must be within to be accepted\. This can help reduce the impact of noise on sensors that are on long I2C cables\. The value is a percentage from the average value\. A value of zero disables this filter\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 100 | percent |
+-----------+---------+---------+




.. _BARO_PROBE_EXT:

BARO\_PROBE\_EXT: External barometers to probe
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets which types of external i2c barometer to look for\. It is a bitmask of barometer types\. The I2C buses to probe is based on GND\_EXT\_BUS\. If BARO\_EXT\_BUS is \-1 then it will probe all external buses\, otherwise it will probe just the bus number given in GND\_EXT\_BUS\.


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | BMP085  | |
| +-----+---------+ |
| | 1   | BMP280  | |
| +-----+---------+ |
| | 2   | MS5611  | |
| +-----+---------+ |
| | 3   | MS5607  | |
| +-----+---------+ |
| | 4   | MS5637  | |
| +-----+---------+ |
| | 5   | FBM320  | |
| +-----+---------+ |
| | 6   | DPS280  | |
| +-----+---------+ |
| | 7   | LPS25H  | |
| +-----+---------+ |
| | 8   | Keller  | |
| +-----+---------+ |
| | 9   | MS5837  | |
| +-----+---------+ |
| | 10  | BMP388  | |
| +-----+---------+ |
| | 11  | SPL06   | |
| +-----+---------+ |
| | 12  | MSP     | |
| +-----+---------+ |
|                   |
+-------------------+




.. _BARO1_DEVID:

BARO1\_DEVID: Baro ID
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Barometer sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _BARO2_DEVID:

BARO2\_DEVID: Baro ID2
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Barometer2 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _BARO3_DEVID:

BARO3\_DEVID: Baro ID3
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Barometer3 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+





.. _parameters_BARO1_WCF_:

BARO1\_WCF\_ Parameters
-----------------------


.. _BARO1_WCF_ENABLE:

BARO1\_WCF\_ENABLE: Wind coefficient enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This enables the use of wind coefficients for barometer compensation


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




.. _BARO1_WCF_FWD:

BARO1\_WCF\_FWD: Pressure error coefficient in positive X direction \(forward\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the X body axis\. If the baro height estimate rises during forwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO1_WCF_BCK:

BARO1\_WCF\_BCK: Pressure error coefficient in negative X direction \(backwards\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the X body axis\. If the baro height estimate rises during backwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO1_WCF_RGT:

BARO1\_WCF\_RGT: Pressure error coefficient in positive Y direction \(right\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the right\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO1_WCF_LFT:

BARO1\_WCF\_LFT: Pressure error coefficient in negative Y direction \(left\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the left\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+





.. _parameters_BARO2_WCF_:

BARO2\_WCF\_ Parameters
-----------------------


.. _BARO2_WCF_ENABLE:

BARO2\_WCF\_ENABLE: Wind coefficient enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This enables the use of wind coefficients for barometer compensation


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




.. _BARO2_WCF_FWD:

BARO2\_WCF\_FWD: Pressure error coefficient in positive X direction \(forward\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the X body axis\. If the baro height estimate rises during forwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO2_WCF_BCK:

BARO2\_WCF\_BCK: Pressure error coefficient in negative X direction \(backwards\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the X body axis\. If the baro height estimate rises during backwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO2_WCF_RGT:

BARO2\_WCF\_RGT: Pressure error coefficient in positive Y direction \(right\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the right\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO2_WCF_LFT:

BARO2\_WCF\_LFT: Pressure error coefficient in negative Y direction \(left\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the left\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+





.. _parameters_BARO3_WCF_:

BARO3\_WCF\_ Parameters
-----------------------


.. _BARO3_WCF_ENABLE:

BARO3\_WCF\_ENABLE: Wind coefficient enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This enables the use of wind coefficients for barometer compensation


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




.. _BARO3_WCF_FWD:

BARO3\_WCF\_FWD: Pressure error coefficient in positive X direction \(forward\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the X body axis\. If the baro height estimate rises during forwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO3_WCF_BCK:

BARO3\_WCF\_BCK: Pressure error coefficient in negative X direction \(backwards\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the X body axis\. If the baro height estimate rises during backwards flight\, then this will be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO3_WCF_RGT:

BARO3\_WCF\_RGT: Pressure error coefficient in positive Y direction \(right\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a positive wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the right\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+




.. _BARO3_WCF_LFT:

BARO3\_WCF\_LFT: Pressure error coefficient in negative Y direction \(left\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the ratio of static pressure error to dynamic pressure generated by a negative wind relative velocity along the Y body axis\. If the baro height estimate rises during sideways flight to the left\, then this should be a negative number\. Multirotors can use this feature only if using EKF3 and if the EK3\_BCOEF\_X and EK3\_BCOEF\_Y parameters have been tuned\.


+-----------+------------+
| Increment | Range      |
+===========+============+
| 0.05      | -1.0 - 1.0 |
+-----------+------------+





.. _parameters_BATT2_:

BATT2\_ Parameters
------------------


.. _BATT2_MONITOR:

BATT2\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT2_CAPACITY:

BATT2\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT2_SERIAL_NUM:

BATT2\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT2_LOW_TIMER:

BATT2\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT2_FS_VOLTSRC:

BATT2\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT2_LOW_VOLT:

BATT2\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT2\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT2\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT2_LOW_MAH:

BATT2\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT2\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT2_CRT_VOLT:

BATT2\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT2\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT2\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT2_CRT_MAH:

BATT2\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT2\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT2_FS_LOW_ACT:

BATT2\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT2_FS_CRT_ACT:

BATT2\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT2_ARM_VOLT:

BATT2\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT2_ARM_MAH:

BATT2\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT2\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT2_OPTIONS:

BATT2\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT2_CELL_DT_V:

BATT2\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT2_CELL_COUNT:

BATT2\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT2_VOLT_PIN:

BATT2\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT2_CURR_PIN:

BATT2\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT2_VOLT_MULT:

BATT2\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT2\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT2_AMP_PERVLT:

BATT2\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT2_AMP_OFFSET:

BATT2\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT2_VLT_OFFSET:

BATT2\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT2_I2C_BUS:

BATT2\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT2_I2C_ADDR:

BATT2\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT2_SUM_MASK:

BATT2\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT3_:

BATT3\_ Parameters
------------------


.. _BATT3_MONITOR:

BATT3\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT3_CAPACITY:

BATT3\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT3_SERIAL_NUM:

BATT3\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT3_LOW_TIMER:

BATT3\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT3_FS_VOLTSRC:

BATT3\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT3_LOW_VOLT:

BATT3\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT3\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT3\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT3_LOW_MAH:

BATT3\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT3\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT3_CRT_VOLT:

BATT3\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT3\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT3\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT3_CRT_MAH:

BATT3\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT3\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT3_FS_LOW_ACT:

BATT3\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT3_FS_CRT_ACT:

BATT3\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT3_ARM_VOLT:

BATT3\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT3_ARM_MAH:

BATT3\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT3\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT3_OPTIONS:

BATT3\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT3_CELL_DT_V:

BATT3\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT3_CELL_COUNT:

BATT3\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT3_VOLT_PIN:

BATT3\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT3_CURR_PIN:

BATT3\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT3_VOLT_MULT:

BATT3\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT3\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT3_AMP_PERVLT:

BATT3\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT3_AMP_OFFSET:

BATT3\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT3_VLT_OFFSET:

BATT3\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT3_I2C_BUS:

BATT3\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT3_I2C_ADDR:

BATT3\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT3_SUM_MASK:

BATT3\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT4_:

BATT4\_ Parameters
------------------


.. _BATT4_MONITOR:

BATT4\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT4_CAPACITY:

BATT4\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT4_SERIAL_NUM:

BATT4\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT4_LOW_TIMER:

BATT4\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT4_FS_VOLTSRC:

BATT4\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT4_LOW_VOLT:

BATT4\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT4\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT4\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT4_LOW_MAH:

BATT4\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT4\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT4_CRT_VOLT:

BATT4\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT4\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT4\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT4_CRT_MAH:

BATT4\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT4\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT4_FS_LOW_ACT:

BATT4\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT4_FS_CRT_ACT:

BATT4\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT4_ARM_VOLT:

BATT4\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT4_ARM_MAH:

BATT4\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT4\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT4_OPTIONS:

BATT4\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT4_CELL_DT_V:

BATT4\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT4_CELL_COUNT:

BATT4\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT4_VOLT_PIN:

BATT4\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT4_CURR_PIN:

BATT4\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT4_VOLT_MULT:

BATT4\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT4\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT4_AMP_PERVLT:

BATT4\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT4_AMP_OFFSET:

BATT4\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT4_VLT_OFFSET:

BATT4\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT4_I2C_BUS:

BATT4\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT4_I2C_ADDR:

BATT4\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT4_SUM_MASK:

BATT4\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT5_:

BATT5\_ Parameters
------------------


.. _BATT5_MONITOR:

BATT5\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT5_CAPACITY:

BATT5\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT5_SERIAL_NUM:

BATT5\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT5_LOW_TIMER:

BATT5\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT5_FS_VOLTSRC:

BATT5\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT5_LOW_VOLT:

BATT5\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT5\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT5\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT5_LOW_MAH:

BATT5\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT5\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT5_CRT_VOLT:

BATT5\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT5\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT5\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT5_CRT_MAH:

BATT5\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT5\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT5_FS_LOW_ACT:

BATT5\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT5_FS_CRT_ACT:

BATT5\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT5_ARM_VOLT:

BATT5\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT5_ARM_MAH:

BATT5\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT5\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT5_OPTIONS:

BATT5\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT5_CELL_DT_V:

BATT5\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT5_CELL_COUNT:

BATT5\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT5_VOLT_PIN:

BATT5\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT5_CURR_PIN:

BATT5\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT5_VOLT_MULT:

BATT5\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT5\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT5_AMP_PERVLT:

BATT5\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT5_AMP_OFFSET:

BATT5\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT5_VLT_OFFSET:

BATT5\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT5_I2C_BUS:

BATT5\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT5_I2C_ADDR:

BATT5\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT5_SUM_MASK:

BATT5\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT6_:

BATT6\_ Parameters
------------------


.. _BATT6_MONITOR:

BATT6\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT6_CAPACITY:

BATT6\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT6_SERIAL_NUM:

BATT6\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT6_LOW_TIMER:

BATT6\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT6_FS_VOLTSRC:

BATT6\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT6_LOW_VOLT:

BATT6\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT6\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT6\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT6_LOW_MAH:

BATT6\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT6\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT6_CRT_VOLT:

BATT6\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT6\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT6\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT6_CRT_MAH:

BATT6\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT6\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT6_FS_LOW_ACT:

BATT6\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT6_FS_CRT_ACT:

BATT6\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT6_ARM_VOLT:

BATT6\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT6_ARM_MAH:

BATT6\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT6\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT6_OPTIONS:

BATT6\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT6_CELL_DT_V:

BATT6\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT6_CELL_COUNT:

BATT6\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT6_VOLT_PIN:

BATT6\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT6_CURR_PIN:

BATT6\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT6_VOLT_MULT:

BATT6\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT6\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT6_AMP_PERVLT:

BATT6\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT6_AMP_OFFSET:

BATT6\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT6_VLT_OFFSET:

BATT6\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT6_I2C_BUS:

BATT6\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT6_I2C_ADDR:

BATT6\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT6_SUM_MASK:

BATT6\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT7_:

BATT7\_ Parameters
------------------


.. _BATT7_MONITOR:

BATT7\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT7_CAPACITY:

BATT7\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT7_SERIAL_NUM:

BATT7\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT7_LOW_TIMER:

BATT7\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT7_FS_VOLTSRC:

BATT7\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT7_LOW_VOLT:

BATT7\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT7\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT7\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT7_LOW_MAH:

BATT7\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT7\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT7_CRT_VOLT:

BATT7\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT7\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT7\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT7_CRT_MAH:

BATT7\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT7\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT7_FS_LOW_ACT:

BATT7\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT7_FS_CRT_ACT:

BATT7\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT7_ARM_VOLT:

BATT7\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT7_ARM_MAH:

BATT7\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT7\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT7_OPTIONS:

BATT7\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT7_CELL_DT_V:

BATT7\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT7_CELL_COUNT:

BATT7\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT7_VOLT_PIN:

BATT7\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT7_CURR_PIN:

BATT7\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT7_VOLT_MULT:

BATT7\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT7\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT7_AMP_PERVLT:

BATT7\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT7_AMP_OFFSET:

BATT7\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT7_VLT_OFFSET:

BATT7\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT7_I2C_BUS:

BATT7\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT7_I2C_ADDR:

BATT7\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT7_SUM_MASK:

BATT7\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT8_:

BATT8\_ Parameters
------------------


.. _BATT8_MONITOR:

BATT8\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT8_CAPACITY:

BATT8\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT8_SERIAL_NUM:

BATT8\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT8_LOW_TIMER:

BATT8\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT8_FS_VOLTSRC:

BATT8\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT8_LOW_VOLT:

BATT8\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT8\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT8\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT8_LOW_MAH:

BATT8\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT8\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT8_CRT_VOLT:

BATT8\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT8\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT8\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT8_CRT_MAH:

BATT8\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT8\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT8_FS_LOW_ACT:

BATT8\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT8_FS_CRT_ACT:

BATT8\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT8_ARM_VOLT:

BATT8\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT8_ARM_MAH:

BATT8\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT8\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT8_OPTIONS:

BATT8\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT8_CELL_DT_V:

BATT8\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT8_CELL_COUNT:

BATT8\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT8_VOLT_PIN:

BATT8\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT8_CURR_PIN:

BATT8\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT8_VOLT_MULT:

BATT8\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT8\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT8_AMP_PERVLT:

BATT8\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT8_AMP_OFFSET:

BATT8\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT8_VLT_OFFSET:

BATT8\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT8_I2C_BUS:

BATT8\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT8_I2C_ADDR:

BATT8\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT8_SUM_MASK:

BATT8\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT9_:

BATT9\_ Parameters
------------------


.. _BATT9_MONITOR:

BATT9\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT9_CAPACITY:

BATT9\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT9_SERIAL_NUM:

BATT9\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT9_LOW_TIMER:

BATT9\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT9_FS_VOLTSRC:

BATT9\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT9_LOW_VOLT:

BATT9\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT9\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT9\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT9_LOW_MAH:

BATT9\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT9\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT9_CRT_VOLT:

BATT9\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT9\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT9\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT9_CRT_MAH:

BATT9\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT9\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT9_FS_LOW_ACT:

BATT9\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT9_FS_CRT_ACT:

BATT9\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT9_ARM_VOLT:

BATT9\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT9_ARM_MAH:

BATT9\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT9\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT9_OPTIONS:

BATT9\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT9_CELL_DT_V:

BATT9\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT9_CELL_COUNT:

BATT9\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT9_VOLT_PIN:

BATT9\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT9_CURR_PIN:

BATT9\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT9_VOLT_MULT:

BATT9\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT9\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT9_AMP_PERVLT:

BATT9\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT9_AMP_OFFSET:

BATT9\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT9_VLT_OFFSET:

BATT9\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT9_I2C_BUS:

BATT9\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT9_I2C_ADDR:

BATT9\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT9_SUM_MASK:

BATT9\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BATT_:

BATT\_ Parameters
-----------------


.. _BATT_MONITOR:

BATT\_MONITOR: Battery monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Controls enabling monitoring of the battery\'s voltage and current


+----------------------------------------+
| Values                                 |
+========================================+
| +-------+----------------------------+ |
| | Value | Meaning                    | |
| +=======+============================+ |
| | 0     | Disabled                   | |
| +-------+----------------------------+ |
| | 3     | Analog Voltage Only        | |
| +-------+----------------------------+ |
| | 4     | Analog Voltage and Current | |
| +-------+----------------------------+ |
| | 5     | Solo                       | |
| +-------+----------------------------+ |
| | 6     | Bebop                      | |
| +-------+----------------------------+ |
| | 7     | SMBus-Generic              | |
| +-------+----------------------------+ |
| | 8     | UAVCAN-BatteryInfo         | |
| +-------+----------------------------+ |
| | 9     | ESC                        | |
| +-------+----------------------------+ |
| | 10    | SumOfFollowing             | |
| +-------+----------------------------+ |
| | 11    | FuelFlow                   | |
| +-------+----------------------------+ |
| | 12    | FuelLevelPWM               | |
| +-------+----------------------------+ |
| | 13    | SMBUS-SUI3                 | |
| +-------+----------------------------+ |
| | 14    | SMBUS-SUI6                 | |
| +-------+----------------------------+ |
| | 15    | NeoDesign                  | |
| +-------+----------------------------+ |
| | 16    | SMBus-Maxell               | |
| +-------+----------------------------+ |
| | 17    | Generator-Elec             | |
| +-------+----------------------------+ |
| | 18    | Generator-Fuel             | |
| +-------+----------------------------+ |
| | 19    | Rotoye                     | |
| +-------+----------------------------+ |
| | 20    | MPPT                       | |
| +-------+----------------------------+ |
| | 21    | INA2XX                     | |
| +-------+----------------------------+ |
| | 22    | LTC2946                    | |
| +-------+----------------------------+ |
| | 23    | Torqeedo                   | |
| +-------+----------------------------+ |
|                                        |
+----------------------------------------+




.. _BATT_CAPACITY:

BATT\_CAPACITY: Battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Capacity of the battery in mAh when full


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT_SERIAL_NUM:

BATT\_SERIAL\_NUM: Battery serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery serial number\, automatically filled in for SMBus batteries\, otherwise will be \-1\. With UAVCAN it is the battery\_id\.


.. _BATT_LOW_TIMER:

BATT\_LOW\_TIMER: Low voltage timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the timeout in seconds before a low voltage event will be triggered\. For aircraft with low C batteries it may be necessary to raise this in order to cope with low voltage on long takeoffs\. A value of zero disables low voltage errors\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 120 | seconds |
+-----------+---------+---------+




.. _BATT_FS_VOLTSRC:

BATT\_FS\_VOLTSRC: Failsafe voltage source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage type used for detection of low voltage event


+-------------------------------------+
| Values                              |
+=====================================+
| +-------+-------------------------+ |
| | Value | Meaning                 | |
| +=======+=========================+ |
| | 0     | Raw Voltage             | |
| +-------+-------------------------+ |
| | 1     | Sag Compensated Voltage | |
| +-------+-------------------------+ |
|                                     |
+-------------------------------------+




.. _BATT_LOW_VOLT:

BATT\_LOW\_VOLT: Low battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a low battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT\_FS\_LOW\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT_LOW_MAH:

BATT\_LOW\_MAH: Low battery capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the low battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT\_FS\_LOW\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT_CRT_VOLT:

BATT\_CRT\_VOLT: Critical battery voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery voltage that triggers a critical battery failsafe\. Set to 0 to disable\. If the battery voltage drops below this voltage continuously for more then the period specified by the BATT\_LOW\_TIMER parameter then the vehicle will perform the failsafe specified by the BATT\_FS\_CRT\_ACT parameter\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT_CRT_MAH:

BATT\_CRT\_MAH: Battery critical capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Battery capacity at which the critical battery failsafe is triggered\. Set to 0 to disable battery remaining failsafe\. If the battery capacity drops below this level the vehicle will perform the failsafe specified by the BATT\_\_FS\_CRT\_ACT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT_FS_LOW_ACT:

BATT\_FS\_LOW\_ACT: Low battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a low battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT_FS_CRT_ACT:

BATT\_FS\_CRT\_ACT: Critical battery failsafe action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


What action the vehicle should perform if it hits a critical battery failsafe


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | None    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BATT_ARM_VOLT:

BATT\_ARM\_VOLT: Required arming voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery voltage level which is required to arm the aircraft\. Set to 0 to allow arming at any voltage\.


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.1       | volt  |
+-----------+-------+




.. _BATT_ARM_MAH:

BATT\_ARM\_MAH: Required arming remaining capacity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Battery capacity remaining which is required to arm the aircraft\. Set to 0 to allow arming at any capacity\. Note that execept for smart batteries rebooting the vehicle will always reset the remaining capacity estimate\, which can lead to this check not providing sufficent protection\, it is recommended to always use this in conjunction with the BATT\_\_ARM\_VOLT parameter\.


+-----------+------------------+
| Increment | Units            |
+===========+==================+
| 50        | milliampere hour |
+-----------+------------------+




.. _BATT_OPTIONS:

BATT\_OPTIONS: Battery monitor options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the battery monitor


+--------------------------------------------------+
| Bitmask                                          |
+==================================================+
| +-----+----------------------------------------+ |
| | Bit | Meaning                                | |
| +=====+========================================+ |
| | 0   | Ignore UAVCAN SoC                      | |
| +-----+----------------------------------------+ |
| | 1   | MPPT reports input voltage and current | |
| +-----+----------------------------------------+ |
| | 2   | MPPT Powered off when disarmed         | |
| +-----+----------------------------------------+ |
| | 3   | MPPT Powered on when armed             | |
| +-----+----------------------------------------+ |
| | 4   | MPPT Powered off at boot               | |
| +-----+----------------------------------------+ |
| | 5   | MPPT Powered on at boot                | |
| +-----+----------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT_CELL_DT_V:

BATT\_CELL\_DT\_V: Battery cell max voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum cell voltage for cell count detection


+-----------+-------+
| Increment | Units |
+===========+=======+
| 0.01      | volt  |
+-----------+-------+




.. _BATT_CELL_COUNT:

BATT\_CELL\_COUNT: Battery cell count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Overrides cell count autodetection if not \-1


+-----------+
| Increment |
+===========+
| 1         |
+-----------+




.. _BATT_VOLT_PIN:

BATT\_VOLT\_PIN: Battery Voltage sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for voltage monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 2     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 5     | Navigator                            | |
| +-------+--------------------------------------+ |
| | 13    | Pixhawk2_PM2/CubeOrange_PM2          | |
| +-------+--------------------------------------+ |
| | 14    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 16    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 100   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT_CURR_PIN:

BATT\_CURR\_PIN: Battery Current sensing pin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Sets the analog input pin that should be used for current monitoring\.


+--------------------------------------------------+
| Values                                           |
+==================================================+
| +-------+--------------------------------------+ |
| | Value | Meaning                              | |
| +=======+======================================+ |
| | -1    | Disabled                             | |
| +-------+--------------------------------------+ |
| | 3     | Pixhawk/Pixracer/Navio2/Pixhawk2_PM1 | |
| +-------+--------------------------------------+ |
| | 4     | CubeOrange_PM2/Navigator             | |
| +-------+--------------------------------------+ |
| | 14    | Pixhawk2_PM2                         | |
| +-------+--------------------------------------+ |
| | 15    | CubeOrange                           | |
| +-------+--------------------------------------+ |
| | 17    | Durandal                             | |
| +-------+--------------------------------------+ |
| | 101   | PX4-v1                               | |
| +-------+--------------------------------------+ |
|                                                  |
+--------------------------------------------------+




.. _BATT_VOLT_MULT:

BATT\_VOLT\_MULT: Voltage Multiplier
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to convert the voltage of the voltage sensing pin \(BATT\_VOLT\_PIN\) to the actual battery\'s voltage \(pin\_voltage \* VOLT\_MULT\)\. For the 3DR Power brick with a Pixhawk\, this should be set to 10\.1\. For the Pixhawk with the 3DR 4in1 ESC this should be 12\.02\. For the PX using the PX4IO power supply this should be set to 1\.


.. _BATT_AMP_PERVLT:

BATT\_AMP\_PERVLT: Amps per volt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of amps that a 1V reading on the current sensor corresponds to\. With a Pixhawk using the 3DR Power brick this should be set to 17\. For the Pixhawk with the 3DR 4in1 ESC this should be 17\.


+-----------------+
| Units           |
+=================+
| ampere per volt |
+-----------------+




.. _BATT_AMP_OFFSET:

BATT\_AMP\_OFFSET: AMP offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Voltage offset at zero current on current sensor


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT_VLT_OFFSET:

BATT\_VLT\_OFFSET: Volage offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Voltage offset on voltage pin\. This allows for an offset due to a diode\. This voltage is subtracted before the scaling is applied


+-------+
| Units |
+=======+
| volt  |
+-------+




.. _BATT_I2C_BUS:

BATT\_I2C\_BUS: Battery monitor I2C bus number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C bus number


+-------+
| Range |
+=======+
| 0 - 3 |
+-------+




.. _BATT_I2C_ADDR:

BATT\_I2C\_ADDR: Battery monitor I2C address
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Battery monitor I2C address


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _BATT_SUM_MASK:

BATT\_SUM\_MASK: Battery Sum mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


0\: sum of remaining battery monitors\, If none 0 sum of specified monitors\. Current will be summed and voltages averaged\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | monitor 1 | |
| +-----+-----------+ |
| | 1   | monitor 2 | |
| +-----+-----------+ |
| | 2   | monitor 3 | |
| +-----+-----------+ |
| | 3   | monitor 4 | |
| +-----+-----------+ |
| | 4   | monitor 5 | |
| +-----+-----------+ |
| | 5   | monitor 6 | |
| +-----+-----------+ |
| | 6   | monitor 7 | |
| +-----+-----------+ |
| | 7   | monitor 8 | |
| +-----+-----------+ |
| | 8   | monitor 9 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_BRD_:

BRD\_ Parameters
----------------


.. _BRD_SER1_RTSCTS:

BRD\_SER1\_RTSCTS: Serial 1 flow control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable flow control on serial 1 \(telemetry 1\)\. You must have the RTS and CTS pins connected to your radio\. The standard DF13 6 pin connector for a 3DR radio does have those pins connected\. If this is set to 2 then flow control will be auto\-detected by checking for the output buffer filling on startup\. Note that the PX4v1 does not have hardware flow control pins on this port\, so you should leave this disabled\.


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
| | 2     | Auto     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SER2_RTSCTS:

BRD\_SER2\_RTSCTS: Serial 2 flow control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable flow control on serial 2 \(telemetry 2\)\. You must have the RTS and CTS pins connected to your radio\. The standard DF13 6 pin connector for a 3DR radio does have those pins connected\. If this is set to 2 then flow control will be auto\-detected by checking for the output buffer filling on startup\.


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
| | 2     | Auto     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SER3_RTSCTS:

BRD\_SER3\_RTSCTS: Serial 3 flow control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable flow control on serial 3\. You must have the RTS and CTS pins connected to your radio\. The standard DF13 6 pin connector for a 3DR radio does have those pins connected\. If this is set to 2 then flow control will be auto\-detected by checking for the output buffer filling on startup\.


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
| | 2     | Auto     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SER4_RTSCTS:

BRD\_SER4\_RTSCTS: Serial 4 flow control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable flow control on serial 4\. You must have the RTS and CTS pins connected to your radio\. The standard DF13 6 pin connector for a 3DR radio does have those pins connected\. If this is set to 2 then flow control will be auto\-detected by checking for the output buffer filling on startup\.


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
| | 2     | Auto     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SER5_RTSCTS:

BRD\_SER5\_RTSCTS: Serial 5 flow control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable flow control on serial 5\. You must have the RTS and CTS pins connected to your radio\. The standard DF13 6 pin connector for a 3DR radio does have those pins connected\. If this is set to 2 then flow control will be auto\-detected by checking for the output buffer filling on startup\.


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
| | 2     | Auto     | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SAFETYENABLE:

BRD\_SAFETYENABLE: Enable use of safety arming switch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

This controls the default state of the safety switch at startup\. When set to 1 the safety switch will start in the safe state \(flashing\) at boot\. When set to zero the safety switch will start in the unsafe state \(solid\) at startup\. Note that if a safety switch is fitted the user can still control the safety state after startup using the switch\. The safety state can also be controlled in software using a MAVLink message\.


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




.. _BRD_SBUS_OUT:

BRD\_SBUS\_OUT:  SBUS output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This sets the SBUS output frame rate in Hz


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | 50Hz     | |
| +-------+----------+ |
| | 2     | 75Hz     | |
| +-------+----------+ |
| | 3     | 100Hz    | |
| +-------+----------+ |
| | 4     | 150Hz    | |
| +-------+----------+ |
| | 5     | 200Hz    | |
| +-------+----------+ |
| | 6     | 250Hz    | |
| +-------+----------+ |
| | 7     | 300Hz    | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_SERIAL_NUM:

BRD\_SERIAL\_NUM: User\-defined serial number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


User\-defined serial number of this vehicle\, it can be any arbitrary number you want and has no effect on the autopilot


+----------------+
| Range          |
+================+
| -32768 - 32767 |
+----------------+




.. _BRD_SAFETY_MASK:

BRD\_SAFETY\_MASK: Outputs which ignore the safety switch state
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

A bitmask which controls what outputs can move while the safety switch has not been pressed


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Output1  | |
| +-----+----------+ |
| | 1   | Output2  | |
| +-----+----------+ |
| | 2   | Output3  | |
| +-----+----------+ |
| | 3   | Output4  | |
| +-----+----------+ |
| | 4   | Output5  | |
| +-----+----------+ |
| | 5   | Output6  | |
| +-----+----------+ |
| | 6   | Output7  | |
| +-----+----------+ |
| | 7   | Output8  | |
| +-----+----------+ |
| | 8   | Output9  | |
| +-----+----------+ |
| | 9   | Output10 | |
| +-----+----------+ |
| | 10  | Output11 | |
| +-----+----------+ |
| | 11  | Output12 | |
| +-----+----------+ |
| | 12  | Output13 | |
| +-----+----------+ |
| | 13  | Output14 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _BRD_HEAT_TARG:

BRD\_HEAT\_TARG: Board heater temperature target
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Board heater target temperature for boards with controllable heating units\. DO NOT SET to \-1 on the Cube\. Set to \-1 to disable the heater\, please reboot after setting to \-1\.


+---------+-----------------+
| Range   | Units           |
+=========+=================+
| -1 - 80 | degrees Celsius |
+---------+-----------------+




.. _BRD_TYPE:

BRD\_TYPE: Board type
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This allows selection of a PX4 or VRBRAIN board type\. If set to zero then the board type is auto\-detected \(PX4\)


+----------------------------+
| Values                     |
+============================+
| +-------+----------------+ |
| | Value | Meaning        | |
| +=======+================+ |
| | 0     | AUTO           | |
| +-------+----------------+ |
| | 1     | PX4V1          | |
| +-------+----------------+ |
| | 2     | Pixhawk        | |
| +-------+----------------+ |
| | 3     | Cube/Pixhawk2  | |
| +-------+----------------+ |
| | 4     | Pixracer       | |
| +-------+----------------+ |
| | 5     | PixhawkMini    | |
| +-------+----------------+ |
| | 6     | Pixhawk2Slim   | |
| +-------+----------------+ |
| | 13    | Intel Aero FC  | |
| +-------+----------------+ |
| | 14    | Pixhawk Pro    | |
| +-------+----------------+ |
| | 20    | AUAV2.1        | |
| +-------+----------------+ |
| | 21    | PCNC1          | |
| +-------+----------------+ |
| | 22    | MINDPXV2       | |
| +-------+----------------+ |
| | 23    | SP01           | |
| +-------+----------------+ |
| | 24    | CUAVv5/FMUV5   | |
| +-------+----------------+ |
| | 30    | VRX BRAIN51    | |
| +-------+----------------+ |
| | 32    | VRX BRAIN52    | |
| +-------+----------------+ |
| | 33    | VRX BRAIN52E   | |
| +-------+----------------+ |
| | 34    | VRX UBRAIN51   | |
| +-------+----------------+ |
| | 35    | VRX UBRAIN52   | |
| +-------+----------------+ |
| | 36    | VRX CORE10     | |
| +-------+----------------+ |
| | 38    | VRX BRAIN54    | |
| +-------+----------------+ |
| | 39    | PX4 FMUV6      | |
| +-------+----------------+ |
| | 100   | PX4 OLDDRIVERS | |
| +-------+----------------+ |
|                            |
+----------------------------+




.. _BRD_IO_ENABLE:

BRD\_IO\_ENABLE: Enable IO co\-processor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This allows for the IO co\-processor on FMUv1 and FMUv2 to be disabled


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




.. _BRD_SAFETYOPTION:

BRD\_SAFETYOPTION: Options for safety button behavior
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls the activation of the safety button\. It allows you to control if the safety button can be used for safety enable and\/or disable\, and whether the button is only active when disarmed


+-----------------------------------------------------+
| Bitmask                                             |
+=====================================================+
| +-----+-------------------------------------------+ |
| | Bit | Meaning                                   | |
| +=====+===========================================+ |
| | 0   | ActiveForSafetyEnable                     | |
| +-----+-------------------------------------------+ |
| | 1   | ActiveForSafetyDisable                    | |
| +-----+-------------------------------------------+ |
| | 2   | ActiveWhenArmed                           | |
| +-----+-------------------------------------------+ |
| | 3   | Force safety on when the aircraft disarms | |
| +-----+-------------------------------------------+ |
|                                                     |
+-----------------------------------------------------+




.. _BRD_VBUS_MIN:

BRD\_VBUS\_MIN: Autopilot board voltage requirement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Minimum voltage on the autopilot power rail to allow the aircraft to arm\. 0 to disable the check\.


+-----------+-----------+-------+
| Increment | Range     | Units |
+===========+===========+=======+
| 0.1       | 4.0 - 5.5 | volt  |
+-----------+-----------+-------+




.. _BRD_VSERVO_MIN:

BRD\_VSERVO\_MIN: Servo voltage requirement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Minimum voltage on the servo rail to allow the aircraft to arm\. 0 to disable the check\.


+-----------+------------+-------+
| Increment | Range      | Units |
+===========+============+=======+
| 0.1       | 3.3 - 12.0 | volt  |
+-----------+------------+-------+




.. _BRD_SD_SLOWDOWN:

BRD\_SD\_SLOWDOWN: microSD slowdown
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is a scaling factor to slow down microSD operation\. It can be used on flight board and microSD card combinations where full speed is not reliable\. For normal full speed operation a value of 0 should be used\.


+-----------+--------+
| Increment | Range  |
+===========+========+
| 1         | 0 - 32 |
+-----------+--------+




.. _BRD_PWM_VOLT_SEL:

BRD\_PWM\_VOLT\_SEL: Set PWM Out Voltage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the voltage max for PWM output pulses\. 0 for 3\.3V and 1 for 5V output\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | 3.3V    | |
| +-------+---------+ |
| | 1     | 5V      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BRD_OPTIONS:

BRD\_OPTIONS: Board options
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Board specific option flags


+---------------------------------------------+
| Bitmask                                     |
+=============================================+
| +-----+-----------------------------------+ |
| | Bit | Meaning                           | |
| +=====+===================================+ |
| | 0   | Enable hardware watchdog          | |
| +-----+-----------------------------------+ |
| | 1   | Disable MAVftp                    | |
| +-----+-----------------------------------+ |
| | 2   | Enable set of internal parameters | |
| +-----+-----------------------------------+ |
|                                             |
+---------------------------------------------+




.. _BRD_BOOT_DELAY:

BRD\_BOOT\_DELAY: Boot delay
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This adds a delay in milliseconds to boot to ensure peripherals initialise fully


+-----------+--------------+
| Range     | Units        |
+===========+==============+
| 0 - 10000 | milliseconds |
+-----------+--------------+




.. _BRD_HEAT_P:

BRD\_HEAT\_P: Board Heater P gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Board Heater P gain


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 1         | 1 - 500 |
+-----------+---------+




.. _BRD_HEAT_I:

BRD\_HEAT\_I: Board Heater I gain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Board Heater integrator gain


+-----------+-------+
| Increment | Range |
+===========+=======+
| 0.1       | 0 - 1 |
+-----------+-------+




.. _BRD_HEAT_IMAX:

BRD\_HEAT\_IMAX: Board Heater IMAX
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Board Heater integrator maximum


+-----------+---------+
| Increment | Range   |
+===========+=========+
| 1         | 0 - 100 |
+-----------+---------+




.. _BRD_ALT_CONFIG:

BRD\_ALT\_CONFIG: Alternative HW config
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Select an alternative hardware configuration\. A value of zero selects the default configuration for this board\. Other values are board specific\. Please see the documentation for your board for details on any alternative configuration values that may be available\.


+-----------+--------+
| Increment | Range  |
+===========+========+
| 1         | 0 - 10 |
+-----------+--------+




.. _BRD_HEAT_LOWMGN:

BRD\_HEAT\_LOWMGN: Board heater temp lower margin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Arming check will fail if temp is lower than this margin below BRD\_HEAT\_TARG\. 0 disables the low temperature check


+--------+-----------------+
| Range  | Units           |
+========+=================+
| 0 - 20 | degrees Celsius |
+--------+-----------------+





.. _parameters_BRD_RADIO:

BRD\_RADIO Parameters
---------------------


.. _BRD_RADIO_TYPE:

BRD\_RADIO\_TYPE: Set type of direct attached radio
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This enables support for direct attached radio receivers


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | None     | |
| +-------+----------+ |
| | 1     | CYRF6936 | |
| +-------+----------+ |
| | 2     | CC2500   | |
| +-------+----------+ |
| | 3     | BK2425   | |
| +-------+----------+ |
|                      |
+----------------------+




.. _BRD_RADIO_PROT:

BRD\_RADIO\_PROT: protocol
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Select air protocol


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Auto    | |
| +-------+---------+ |
| | 1     | DSM2    | |
| +-------+---------+ |
| | 2     | DSMX    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BRD_RADIO_DEBUG:

BRD\_RADIO\_DEBUG: debug level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

radio debug level


+-------+
| Range |
+=======+
| 0 - 4 |
+-------+




.. _BRD_RADIO_DISCRC:

BRD\_RADIO\_DISCRC: disable receive CRC
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

disable receive CRC \(for debug\)


+-------------------------+
| Values                  |
+=========================+
| +-------+-------------+ |
| | Value | Meaning     | |
| +=======+=============+ |
| | 0     | NotDisabled | |
| +-------+-------------+ |
| | 1     | Disabled    | |
| +-------+-------------+ |
|                         |
+-------------------------+




.. _BRD_RADIO_SIGCH:

BRD\_RADIO\_SIGCH: RSSI signal strength
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Channel to show receive RSSI signal strength\, or zero for disabled


+--------+
| Range  |
+========+
| 0 - 16 |
+--------+




.. _BRD_RADIO_PPSCH:

BRD\_RADIO\_PPSCH: Packet rate channel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Channel to show received packet\-per\-second rate\, or zero for disabled


+--------+
| Range  |
+========+
| 0 - 16 |
+--------+




.. _BRD_RADIO_TELEM:

BRD\_RADIO\_TELEM: Enable telemetry
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

If this is non\-zero then telemetry packets will be sent over DSM


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




.. _BRD_RADIO_TXPOW:

BRD\_RADIO\_TXPOW: Telemetry Transmit power
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set telemetry transmit power\. This is the power level \(from 1 to 8\) for telemetry packets sent from the RX to the TX


+-------+
| Range |
+=======+
| 1 - 8 |
+-------+




.. _BRD_RADIO_FCCTST:

BRD\_RADIO\_FCCTST: Put radio into FCC test mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

If this is enabled then the radio will continuously transmit as required for FCC testing\. The transmit channel is set by the value of the parameter\. The radio will not work for RC input while this is enabled


+--------------------------+
| Values                   |
+==========================+
| +-------+--------------+ |
| | Value | Meaning      | |
| +=======+==============+ |
| | 0     | Disabled     | |
| +-------+--------------+ |
| | 1     | MinChannel   | |
| +-------+--------------+ |
| | 2     | MidChannel   | |
| +-------+--------------+ |
| | 3     | MaxChannel   | |
| +-------+--------------+ |
| | 4     | MinChannelCW | |
| +-------+--------------+ |
| | 5     | MidChannelCW | |
| +-------+--------------+ |
| | 6     | MaxChannelCW | |
| +-------+--------------+ |
|                          |
+--------------------------+




.. _BRD_RADIO_STKMD:

BRD\_RADIO\_STKMD: Stick input mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This selects between different stick input modes\. The default is mode2\, which has throttle on the left stick and pitch on the right stick\. You can instead set mode1\, which has throttle on the right stick and pitch on the left stick\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | Mode1   | |
| +-------+---------+ |
| | 2     | Mode2   | |
| +-------+---------+ |
|                     |
+---------------------+




.. _BRD_RADIO_TESTCH:

BRD\_RADIO\_TESTCH: Set radio to factory test channel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the radio to a fixed test channel for factory testing\. Using a fixed channel avoids the need for binding in factory testing\.


+-----------------------+
| Values                |
+=======================+
| +-------+-----------+ |
| | Value | Meaning   | |
| +=======+===========+ |
| | 0     | Disabled  | |
| +-------+-----------+ |
| | 1     | TestChan1 | |
| +-------+-----------+ |
| | 2     | TestChan2 | |
| +-------+-----------+ |
| | 3     | TestChan3 | |
| +-------+-----------+ |
| | 4     | TestChan4 | |
| +-------+-----------+ |
| | 5     | TestChan5 | |
| +-------+-----------+ |
| | 6     | TestChan6 | |
| +-------+-----------+ |
| | 7     | TestChan7 | |
| +-------+-----------+ |
| | 8     | TestChan8 | |
| +-------+-----------+ |
|                       |
+-----------------------+




.. _BRD_RADIO_TSIGCH:

BRD\_RADIO\_TSIGCH: RSSI value channel for telemetry data on transmitter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Channel to show telemetry RSSI value as received by TX


+--------+
| Range  |
+========+
| 0 - 16 |
+--------+




.. _BRD_RADIO_TPPSCH:

BRD\_RADIO\_TPPSCH: Telemetry PPS channel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Channel to show telemetry packets\-per\-second value\, as received at TX


+--------+
| Range  |
+========+
| 0 - 16 |
+--------+




.. _BRD_RADIO_TXMAX:

BRD\_RADIO\_TXMAX: Transmitter transmit power
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set transmitter maximum transmit power \(from 1 to 8\)


+-------+
| Range |
+=======+
| 1 - 8 |
+-------+




.. _BRD_RADIO_BZOFS:

BRD\_RADIO\_BZOFS: Transmitter buzzer adjustment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set transmitter buzzer note adjustment \(adjust frequency up\)


+--------+
| Range  |
+========+
| 0 - 40 |
+--------+




.. _BRD_RADIO_ABTIME:

BRD\_RADIO\_ABTIME: Auto\-bind time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

When non\-zero this sets the time with no transmitter packets before we start looking for auto\-bind packets\.


+---------+
| Range   |
+=========+
| 0 - 120 |
+---------+




.. _BRD_RADIO_ABLVL:

BRD\_RADIO\_ABLVL: Auto\-bind level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the minimum RSSI of an auto\-bind packet for it to be accepted\. This should be set so that auto\-bind will only happen at short range to minimise the change of an auto\-bind happening accidentially


+--------+
| Range  |
+========+
| 0 - 31 |
+--------+





.. _parameters_BRD_RTC:

BRD\_RTC Parameters
-------------------


.. _BRD_RTC_TYPES:

BRD\_RTC\_TYPES: Allowed sources of RTC time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Specifies which sources of UTC time will be accepted


+-------------------------------+
| Bitmask                       |
+===============================+
| +-----+---------------------+ |
| | Bit | Meaning             | |
| +=====+=====================+ |
| | 0   | GPS                 | |
| +-----+---------------------+ |
| | 1   | MAVLINK_SYSTEM_TIME | |
| +-----+---------------------+ |
| | 2   | HW                  | |
| +-----+---------------------+ |
|                               |
+-------------------------------+




.. _BRD_RTC_TZ_MIN:

BRD\_RTC\_TZ\_MIN: Timezone offset from UTC
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Adds offset in \+\- minutes from UTC to calculate local time


+-------------+
| Range       |
+=============+
| -720 - +840 |
+-------------+





.. _parameters_CAM_RC_:

CAM\_RC\_ Parameters
--------------------


.. _CAM_RC_TYPE:

CAM\_RC\_TYPE: RunCam device type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


RunCam deviee type used to determine OSD menu structure and shutter options\.


+-------------------------------------------------+
| Values                                          |
+=================================================+
| +-------+-------------------------------------+ |
| | Value | Meaning                             | |
| +=======+=====================================+ |
| | 0     | Disabled                            | |
| +-------+-------------------------------------+ |
| | 1     | RunCam Split Micro/RunCam with UART | |
| +-------+-------------------------------------+ |
| | 2     | RunCam Split                        | |
| +-------+-------------------------------------+ |
| | 3     | RunCam Split4 4k                    | |
| +-------+-------------------------------------+ |
| | 4     | RunCam Hybrid                       | |
| +-------+-------------------------------------+ |
|                                                 |
+-------------------------------------------------+




.. _CAM_RC_FEATURES:

CAM\_RC\_FEATURES: RunCam features available
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The available features of the attached RunCam device\. If 0 then the RunCam device will be queried for the features it supports\, otherwise this setting is used\.


+---------------------------+
| Bitmask                   |
+===========================+
| +-----+-----------------+ |
| | Bit | Meaning         | |
| +=====+=================+ |
| | 0   | Power Button    | |
| +-----+-----------------+ |
| | 1   | WiFi Button     | |
| +-----+-----------------+ |
| | 2   | Change Mode     | |
| +-----+-----------------+ |
| | 3   | 5-Key OSD       | |
| +-----+-----------------+ |
| | 4   | Settings Access | |
| +-----+-----------------+ |
| | 5   | DisplayPort     | |
| +-----+-----------------+ |
| | 6   | Start Recording | |
| +-----+-----------------+ |
| | 7   | Stop Recording  | |
| +-----+-----------------+ |
|                           |
+---------------------------+




.. _CAM_RC_BT_DELAY:

CAM\_RC\_BT\_DELAY: RunCam boot delay before allowing updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Time it takes for the RunCam to become fully ready in ms\. If this is too short then commands can get out of sync\.


.. _CAM_RC_BTN_DELAY:

CAM\_RC\_BTN\_DELAY: RunCam button delay before allowing further button presses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Time it takes for the a RunCam button press to be actived in ms\. If this is too short then commands can get out of sync\.


.. _CAM_RC_MDE_DELAY:

CAM\_RC\_MDE\_DELAY: RunCam mode delay before allowing further button presses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Time it takes for the a RunCam mode button press to be actived in ms\. If a mode change first requires a video recording change then double this value is used\. If this is too short then commands can get out of sync\.


.. _CAM_RC_CONTROL:

CAM\_RC\_CONTROL: RunCam control option
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Specifies the allowed actions required to enter the OSD menu


+---------------------------------+
| Bitmask                         |
+=================================+
| +-----+-----------------------+ |
| | Bit | Meaning               | |
| +=====+=======================+ |
| | 0   | Stick yaw right       | |
| +-----+-----------------------+ |
| | 1   | Stick roll right      | |
| +-----+-----------------------+ |
| | 2   | 3-position switch     | |
| +-----+-----------------------+ |
| | 3   | 2-position switch     | |
| +-----+-----------------------+ |
| | 4   | Autorecording enabled | |
| +-----+-----------------------+ |
|                                 |
+---------------------------------+





.. _parameters_CAN_:

CAN\_ Parameters
----------------


.. _CAN_LOGLEVEL:

CAN\_LOGLEVEL: Loglevel
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Loglevel for recording initialisation and debug information from CAN Interface


+-------+-----------------------------------+
| Range | Values                            |
+=======+===================================+
| 0 - 4 | +-------+-----------------------+ |
|       | | Value | Meaning               | |
|       | +=======+=======================+ |
|       | | 0     | Log None              | |
|       | +-------+-----------------------+ |
|       | | 1     | Log Error             | |
|       | +-------+-----------------------+ |
|       | | 2     | Log Warning and below | |
|       | +-------+-----------------------+ |
|       | | 3     | Log Info and below    | |
|       | +-------+-----------------------+ |
|       | | 4     | Log Everything        | |
|       | +-------+-----------------------+ |
|       |                                   |
+-------+-----------------------------------+





.. _parameters_CAN_D1_:

CAN\_D1\_ Parameters
--------------------


.. _CAN_D1_PROTOCOL:

CAN\_D1\_PROTOCOL: Enable use of specific protocol over virtual driver
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enabling this option starts selected protocol that will use this virtual driver


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | UAVCAN        | |
| +-------+---------------+ |
| | 3     | ToshibaCAN    | |
| +-------+---------------+ |
| | 4     | PiccoloCAN    | |
| +-------+---------------+ |
| | 5     | CANTester     | |
| +-------+---------------+ |
| | 6     | EFI_NWPMU     | |
| +-------+---------------+ |
| | 7     | USD1          | |
| +-------+---------------+ |
| | 8     | KDECAN        | |
| +-------+---------------+ |
| | 9     | PacketDigital | |
| +-------+---------------+ |
| | 10    | Scripting     | |
| +-------+---------------+ |
| | 11    | Benewake      | |
| +-------+---------------+ |
|                           |
+---------------------------+





.. _parameters_CAN_D1_KDE_:

CAN\_D1\_KDE\_ Parameters
-------------------------


.. _CAN_D1_KDE_NPOLE:

CAN\_D1\_KDE\_NPOLE: Number of motor poles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Sets the number of motor poles to calculate the correct RPM value



.. _parameters_CAN_D1_PC_:

CAN\_D1\_PC\_ Parameters
------------------------


.. _CAN_D1_PC_ESC_BM:

CAN\_D1\_PC\_ESC\_BM: ESC channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which ESC \(motor\) channels are to be transmitted over Piccolo CAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D1_PC_ESC_RT:

CAN\_D1\_PC\_ESC\_RT: ESC output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of ESC command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+




.. _CAN_D1_PC_SRV_BM:

CAN\_D1\_PC\_SRV\_BM: Servo channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which servo channels are to be transmitted over Piccolo CAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
| | 15  | Servo 16 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D1_PC_SRV_RT:

CAN\_D1\_PC\_SRV\_RT: Servo command output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of servo command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+





.. _parameters_CAN_D1_TST_:

CAN\_D1\_TST\_ Parameters
-------------------------


.. _CAN_D1_TST_ID:

CAN\_D1\_TST\_ID: CAN Test Index
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Index of Test that needs to be run recursively\, this value gets reset to 0 at boot\.


+-------+----------------------------------+
| Range | Values                           |
+=======+==================================+
| 0 - 4 | +-------+----------------------+ |
|       | | Value | Meaning              | |
|       | +=======+======================+ |
|       | | 0     | TEST_NONE            | |
|       | +-------+----------------------+ |
|       | | 1     | TEST_LOOPBACK        | |
|       | +-------+----------------------+ |
|       | | 2     | TEST_BUSOFF_RECOVERY | |
|       | +-------+----------------------+ |
|       | | 3     | TEST_UAVCAN_DNA      | |
|       | +-------+----------------------+ |
|       | | 4     | TEST_TOSHIBA_CAN     | |
|       | +-------+----------------------+ |
|       | | 5     | TEST_KDE_CAN         | |
|       | +-------+----------------------+ |
|       | | 6     | TEST_UAVCAN_ESC      | |
|       | +-------+----------------------+ |
|       |                                  |
+-------+----------------------------------+




.. _CAN_D1_TST_LPR8:

CAN\_D1\_TST\_LPR8: CANTester LoopRate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Looprate of Test methods


+--------------+
| Units        |
+==============+
| microseconds |
+--------------+





.. _parameters_CAN_D1_UC_:

CAN\_D1\_UC\_ Parameters
------------------------


.. _CAN_D1_UC_NODE:

CAN\_D1\_UC\_NODE: UAVCAN node that is used for this network
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

UAVCAN node should be set implicitly


+---------+
| Range   |
+=========+
| 1 - 250 |
+---------+




.. _CAN_D1_UC_SRV_BM:

CAN\_D1\_UC\_SRV\_BM: RC Out channels to be transmitted as servo over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a servo command over UAVCAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D1_UC_ESC_BM:

CAN\_D1\_UC\_ESC\_BM: RC Out channels to be transmitted as ESC over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a ESC command over UAVCAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D1_UC_SRV_RT:

CAN\_D1\_UC\_SRV\_RT: Servo output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for servo outputs


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+




.. _CAN_D1_UC_OPTION:

CAN\_D1\_UC\_OPTION: UAVCAN options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Option flags


+----------------------------------+
| Bitmask                          |
+==================================+
| +-----+------------------------+ |
| | Bit | Meaning                | |
| +=====+========================+ |
| | 0   | ClearDNADatabase       | |
| +-----+------------------------+ |
| | 1   | IgnoreDNANodeConflicts | |
| +-----+------------------------+ |
|                                  |
+----------------------------------+




.. _CAN_D1_UC_NTF_RT:

CAN\_D1\_UC\_NTF\_RT: Notify State rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for Notify State Message


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+





.. _parameters_CAN_D2_:

CAN\_D2\_ Parameters
--------------------


.. _CAN_D2_PROTOCOL:

CAN\_D2\_PROTOCOL: Enable use of specific protocol over virtual driver
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enabling this option starts selected protocol that will use this virtual driver


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | UAVCAN        | |
| +-------+---------------+ |
| | 3     | ToshibaCAN    | |
| +-------+---------------+ |
| | 4     | PiccoloCAN    | |
| +-------+---------------+ |
| | 5     | CANTester     | |
| +-------+---------------+ |
| | 6     | EFI_NWPMU     | |
| +-------+---------------+ |
| | 7     | USD1          | |
| +-------+---------------+ |
| | 8     | KDECAN        | |
| +-------+---------------+ |
| | 9     | PacketDigital | |
| +-------+---------------+ |
| | 10    | Scripting     | |
| +-------+---------------+ |
| | 11    | Benewake      | |
| +-------+---------------+ |
|                           |
+---------------------------+





.. _parameters_CAN_D2_KDE_:

CAN\_D2\_KDE\_ Parameters
-------------------------


.. _CAN_D2_KDE_NPOLE:

CAN\_D2\_KDE\_NPOLE: Number of motor poles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Sets the number of motor poles to calculate the correct RPM value



.. _parameters_CAN_D2_PC_:

CAN\_D2\_PC\_ Parameters
------------------------


.. _CAN_D2_PC_ESC_BM:

CAN\_D2\_PC\_ESC\_BM: ESC channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which ESC \(motor\) channels are to be transmitted over Piccolo CAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D2_PC_ESC_RT:

CAN\_D2\_PC\_ESC\_RT: ESC output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of ESC command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+




.. _CAN_D2_PC_SRV_BM:

CAN\_D2\_PC\_SRV\_BM: Servo channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which servo channels are to be transmitted over Piccolo CAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
| | 15  | Servo 16 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D2_PC_SRV_RT:

CAN\_D2\_PC\_SRV\_RT: Servo command output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of servo command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+





.. _parameters_CAN_D2_TST_:

CAN\_D2\_TST\_ Parameters
-------------------------


.. _CAN_D2_TST_ID:

CAN\_D2\_TST\_ID: CAN Test Index
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Index of Test that needs to be run recursively\, this value gets reset to 0 at boot\.


+-------+----------------------------------+
| Range | Values                           |
+=======+==================================+
| 0 - 4 | +-------+----------------------+ |
|       | | Value | Meaning              | |
|       | +=======+======================+ |
|       | | 0     | TEST_NONE            | |
|       | +-------+----------------------+ |
|       | | 1     | TEST_LOOPBACK        | |
|       | +-------+----------------------+ |
|       | | 2     | TEST_BUSOFF_RECOVERY | |
|       | +-------+----------------------+ |
|       | | 3     | TEST_UAVCAN_DNA      | |
|       | +-------+----------------------+ |
|       | | 4     | TEST_TOSHIBA_CAN     | |
|       | +-------+----------------------+ |
|       | | 5     | TEST_KDE_CAN         | |
|       | +-------+----------------------+ |
|       | | 6     | TEST_UAVCAN_ESC      | |
|       | +-------+----------------------+ |
|       |                                  |
+-------+----------------------------------+




.. _CAN_D2_TST_LPR8:

CAN\_D2\_TST\_LPR8: CANTester LoopRate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Looprate of Test methods


+--------------+
| Units        |
+==============+
| microseconds |
+--------------+





.. _parameters_CAN_D2_UC_:

CAN\_D2\_UC\_ Parameters
------------------------


.. _CAN_D2_UC_NODE:

CAN\_D2\_UC\_NODE: UAVCAN node that is used for this network
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

UAVCAN node should be set implicitly


+---------+
| Range   |
+=========+
| 1 - 250 |
+---------+




.. _CAN_D2_UC_SRV_BM:

CAN\_D2\_UC\_SRV\_BM: RC Out channels to be transmitted as servo over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a servo command over UAVCAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D2_UC_ESC_BM:

CAN\_D2\_UC\_ESC\_BM: RC Out channels to be transmitted as ESC over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a ESC command over UAVCAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D2_UC_SRV_RT:

CAN\_D2\_UC\_SRV\_RT: Servo output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for servo outputs


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+




.. _CAN_D2_UC_OPTION:

CAN\_D2\_UC\_OPTION: UAVCAN options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Option flags


+----------------------------------+
| Bitmask                          |
+==================================+
| +-----+------------------------+ |
| | Bit | Meaning                | |
| +=====+========================+ |
| | 0   | ClearDNADatabase       | |
| +-----+------------------------+ |
| | 1   | IgnoreDNANodeConflicts | |
| +-----+------------------------+ |
|                                  |
+----------------------------------+




.. _CAN_D2_UC_NTF_RT:

CAN\_D2\_UC\_NTF\_RT: Notify State rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for Notify State Message


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+





.. _parameters_CAN_D3_:

CAN\_D3\_ Parameters
--------------------


.. _CAN_D3_PROTOCOL:

CAN\_D3\_PROTOCOL: Enable use of specific protocol over virtual driver
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enabling this option starts selected protocol that will use this virtual driver


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | UAVCAN        | |
| +-------+---------------+ |
| | 3     | ToshibaCAN    | |
| +-------+---------------+ |
| | 4     | PiccoloCAN    | |
| +-------+---------------+ |
| | 5     | CANTester     | |
| +-------+---------------+ |
| | 6     | EFI_NWPMU     | |
| +-------+---------------+ |
| | 7     | USD1          | |
| +-------+---------------+ |
| | 8     | KDECAN        | |
| +-------+---------------+ |
| | 9     | PacketDigital | |
| +-------+---------------+ |
| | 10    | Scripting     | |
| +-------+---------------+ |
| | 11    | Benewake      | |
| +-------+---------------+ |
|                           |
+---------------------------+





.. _parameters_CAN_D3_KDE_:

CAN\_D3\_KDE\_ Parameters
-------------------------


.. _CAN_D3_KDE_NPOLE:

CAN\_D3\_KDE\_NPOLE: Number of motor poles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Sets the number of motor poles to calculate the correct RPM value



.. _parameters_CAN_D3_PC_:

CAN\_D3\_PC\_ Parameters
------------------------


.. _CAN_D3_PC_ESC_BM:

CAN\_D3\_PC\_ESC\_BM: ESC channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which ESC \(motor\) channels are to be transmitted over Piccolo CAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D3_PC_ESC_RT:

CAN\_D3\_PC\_ESC\_RT: ESC output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of ESC command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+




.. _CAN_D3_PC_SRV_BM:

CAN\_D3\_PC\_SRV\_BM: Servo channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask defining which servo channels are to be transmitted over Piccolo CAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
| | 15  | Servo 16 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D3_PC_SRV_RT:

CAN\_D3\_PC\_SRV\_RT: Servo command output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Output rate of servo command messages


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 500 | hertz |
+---------+-------+





.. _parameters_CAN_D3_TST_:

CAN\_D3\_TST\_ Parameters
-------------------------


.. _CAN_D3_TST_ID:

CAN\_D3\_TST\_ID: CAN Test Index
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Index of Test that needs to be run recursively\, this value gets reset to 0 at boot\.


+-------+----------------------------------+
| Range | Values                           |
+=======+==================================+
| 0 - 4 | +-------+----------------------+ |
|       | | Value | Meaning              | |
|       | +=======+======================+ |
|       | | 0     | TEST_NONE            | |
|       | +-------+----------------------+ |
|       | | 1     | TEST_LOOPBACK        | |
|       | +-------+----------------------+ |
|       | | 2     | TEST_BUSOFF_RECOVERY | |
|       | +-------+----------------------+ |
|       | | 3     | TEST_UAVCAN_DNA      | |
|       | +-------+----------------------+ |
|       | | 4     | TEST_TOSHIBA_CAN     | |
|       | +-------+----------------------+ |
|       | | 5     | TEST_KDE_CAN         | |
|       | +-------+----------------------+ |
|       | | 6     | TEST_UAVCAN_ESC      | |
|       | +-------+----------------------+ |
|       |                                  |
+-------+----------------------------------+




.. _CAN_D3_TST_LPR8:

CAN\_D3\_TST\_LPR8: CANTester LoopRate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Selects the Looprate of Test methods


+--------------+
| Units        |
+==============+
| microseconds |
+--------------+





.. _parameters_CAN_D3_UC_:

CAN\_D3\_UC\_ Parameters
------------------------


.. _CAN_D3_UC_NODE:

CAN\_D3\_UC\_NODE: UAVCAN node that is used for this network
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

UAVCAN node should be set implicitly


+---------+
| Range   |
+=========+
| 1 - 250 |
+---------+




.. _CAN_D3_UC_SRV_BM:

CAN\_D3\_UC\_SRV\_BM: RC Out channels to be transmitted as servo over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a servo command over UAVCAN


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
|                    |
+--------------------+




.. _CAN_D3_UC_ESC_BM:

CAN\_D3\_UC\_ESC\_BM: RC Out channels to be transmitted as ESC over UAVCAN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask with one set for channel to be transmitted as a ESC command over UAVCAN


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | ESC 1   | |
| +-----+---------+ |
| | 1   | ESC 2   | |
| +-----+---------+ |
| | 2   | ESC 3   | |
| +-----+---------+ |
| | 3   | ESC 4   | |
| +-----+---------+ |
| | 4   | ESC 5   | |
| +-----+---------+ |
| | 5   | ESC 6   | |
| +-----+---------+ |
| | 6   | ESC 7   | |
| +-----+---------+ |
| | 7   | ESC 8   | |
| +-----+---------+ |
| | 8   | ESC 9   | |
| +-----+---------+ |
| | 9   | ESC 10  | |
| +-----+---------+ |
| | 10  | ESC 11  | |
| +-----+---------+ |
| | 11  | ESC 12  | |
| +-----+---------+ |
| | 12  | ESC 13  | |
| +-----+---------+ |
| | 13  | ESC 14  | |
| +-----+---------+ |
| | 14  | ESC 15  | |
| +-----+---------+ |
| | 15  | ESC 16  | |
| +-----+---------+ |
|                   |
+-------------------+




.. _CAN_D3_UC_SRV_RT:

CAN\_D3\_UC\_SRV\_RT: Servo output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for servo outputs


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+




.. _CAN_D3_UC_OPTION:

CAN\_D3\_UC\_OPTION: UAVCAN options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Option flags


+----------------------------------+
| Bitmask                          |
+==================================+
| +-----+------------------------+ |
| | Bit | Meaning                | |
| +=====+========================+ |
| | 0   | ClearDNADatabase       | |
| +-----+------------------------+ |
| | 1   | IgnoreDNANodeConflicts | |
| +-----+------------------------+ |
|                                  |
+----------------------------------+




.. _CAN_D3_UC_NTF_RT:

CAN\_D3\_UC\_NTF\_RT: Notify State rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum transmit rate for Notify State Message


+---------+-------+
| Range   | Units |
+=========+=======+
| 1 - 200 | hertz |
+---------+-------+





.. _parameters_CAN_P1_:

CAN\_P1\_ Parameters
--------------------


.. _CAN_P1_DRIVER:

CAN\_P1\_DRIVER: Index of virtual driver to be used with physical CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Enabling this option enables use of CAN buses\.


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | First driver  | |
| +-------+---------------+ |
| | 2     | Second driver | |
| +-------+---------------+ |
| | 3     | Third driver  | |
| +-------+---------------+ |
|                           |
+---------------------------+




.. _CAN_P1_BITRATE:

CAN\_P1\_BITRATE: Bitrate of CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bit rate can be set up to from 10000 to 1000000


+-----------------+
| Range           |
+=================+
| 10000 - 1000000 |
+-----------------+





.. _parameters_CAN_P2_:

CAN\_P2\_ Parameters
--------------------


.. _CAN_P2_DRIVER:

CAN\_P2\_DRIVER: Index of virtual driver to be used with physical CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Enabling this option enables use of CAN buses\.


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | First driver  | |
| +-------+---------------+ |
| | 2     | Second driver | |
| +-------+---------------+ |
| | 3     | Third driver  | |
| +-------+---------------+ |
|                           |
+---------------------------+




.. _CAN_P2_BITRATE:

CAN\_P2\_BITRATE: Bitrate of CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bit rate can be set up to from 10000 to 1000000


+-----------------+
| Range           |
+=================+
| 10000 - 1000000 |
+-----------------+





.. _parameters_CAN_P3_:

CAN\_P3\_ Parameters
--------------------


.. _CAN_P3_DRIVER:

CAN\_P3\_DRIVER: Index of virtual driver to be used with physical CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Enabling this option enables use of CAN buses\.


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Disabled      | |
| +-------+---------------+ |
| | 1     | First driver  | |
| +-------+---------------+ |
| | 2     | Second driver | |
| +-------+---------------+ |
| | 3     | Third driver  | |
| +-------+---------------+ |
|                           |
+---------------------------+




.. _CAN_P3_BITRATE:

CAN\_P3\_BITRATE: Bitrate of CAN interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bit rate can be set up to from 10000 to 1000000


+-----------------+
| Range           |
+=================+
| 10000 - 1000000 |
+-----------------+





.. _parameters_CAN_SLCAN_:

CAN\_SLCAN\_ Parameters
-----------------------


.. _CAN_SLCAN_CPORT:

CAN\_SLCAN\_CPORT: SLCAN Route
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

CAN Interface ID to be routed to SLCAN\, 0 means no routing


+------------------------------+
| Values                       |
+==============================+
| +-------+------------------+ |
| | Value | Meaning          | |
| +=======+==================+ |
| | 0     | Disabled         | |
| +-------+------------------+ |
| | 1     | First interface  | |
| +-------+------------------+ |
| | 2     | Second interface | |
| +-------+------------------+ |
|                              |
+------------------------------+




.. _CAN_SLCAN_SERNUM:

CAN\_SLCAN\_SERNUM: SLCAN Serial Port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Serial Port ID to be used for temporary SLCAN iface\, \-1 means no temporary serial\. This parameter is automatically reset on reboot or on timeout\. See CAN\_SLCAN\_TIMOUT for timeout details


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | -1    | Disabled | |
| +-------+----------+ |
| | 0     | Serial0  | |
| +-------+----------+ |
| | 1     | Serial1  | |
| +-------+----------+ |
| | 2     | Serial2  | |
| +-------+----------+ |
| | 3     | Serial3  | |
| +-------+----------+ |
| | 4     | Serial4  | |
| +-------+----------+ |
| | 5     | Serial5  | |
| +-------+----------+ |
| | 6     | Serial6  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _CAN_SLCAN_TIMOUT:

CAN\_SLCAN\_TIMOUT: SLCAN Timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Duration of inactivity after which SLCAN is switched back to original driver in seconds\.


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+




.. _CAN_SLCAN_SDELAY:

CAN\_SLCAN\_SDELAY: SLCAN Start Delay
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Duration after which slcan starts after setting SERNUM in seconds\.


+---------+
| Range   |
+=========+
| 0 - 127 |
+---------+





.. _parameters_COMPASS_:

COMPASS\_ Parameters
--------------------


.. _COMPASS_OFS_X:

COMPASS\_OFS\_X: Compass offsets in milligauss on the X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to the compass x\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS_Y:

COMPASS\_OFS\_Y: Compass offsets in milligauss on the Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to the compass y\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS_Z:

COMPASS\_OFS\_Z: Compass offsets in milligauss on the Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to the compass z\-axis values to compensate for metal in the frame


+-----------+------------+------------+
| Increment | Range      | Units      |
+===========+============+============+
| 1         | -400 - 400 | milligauss |
+-----------+------------+------------+




.. _COMPASS_DEC:

COMPASS\_DEC: Compass declination
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


An angle to compensate between the true north and magnetic north


+-----------+----------------+---------+
| Increment | Range          | Units   |
+===========+================+=========+
| 0.01      | -3.142 - 3.142 | radians |
+-----------+----------------+---------+




.. _COMPASS_LEARN:

COMPASS\_LEARN: Learn compass offsets automatically
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable or disable the automatic learning of compass offsets\. You can enable learning either using a compass\-only method that is suitable only for fixed wing aircraft or using the offsets learnt by the active EKF state estimator\. If this option is enabled then the learnt offsets are saved when you disarm the vehicle\. If InFlight learning is enabled then the compass with automatically start learning once a flight starts \(must be armed\)\. While InFlight learning is running you cannot use position control modes\.


+-------------------------------+
| Values                        |
+===============================+
| +-------+-------------------+ |
| | Value | Meaning           | |
| +=======+===================+ |
| | 0     | Disabled          | |
| +-------+-------------------+ |
| | 1     | Internal-Learning | |
| +-------+-------------------+ |
| | 2     | EKF-Learning      | |
| +-------+-------------------+ |
| | 3     | InFlight-Learning | |
| +-------+-------------------+ |
|                               |
+-------------------------------+




.. _COMPASS_USE:

COMPASS\_USE: Use compass for yaw
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable or disable the use of the compass \(instead of the GPS\) for determining heading


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




.. _COMPASS_AUTODEC:

COMPASS\_AUTODEC: Auto Declination
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable or disable the automatic calculation of the declination based on gps location


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




.. _COMPASS_MOTCT:

COMPASS\_MOTCT: Motor interference compensation type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set motor interference compensation type to disabled\, throttle or current\.  Do not change manually\.


+-------------+--------------------------+
| Calibration | Values                   |
+=============+==========================+
| 1           | +-------+--------------+ |
|             | | Value | Meaning      | |
|             | +=======+==============+ |
|             | | 0     | Disabled     | |
|             | +-------+--------------+ |
|             | | 1     | Use Throttle | |
|             | +-------+--------------+ |
|             | | 2     | Use Current  | |
|             | +-------+--------------+ |
|             |                          |
+-------------+--------------------------+




.. _COMPASS_MOT_X:

COMPASS\_MOT\_X: Motor interference compensation for body frame X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to the compass\'s x\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT_Y:

COMPASS\_MOT\_Y: Motor interference compensation for body frame Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to the compass\'s y\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT_Z:

COMPASS\_MOT\_Z: Motor interference compensation for body frame Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to the compass\'s z\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-----------+--------------+-----------------------+
| Increment | Range        | Units                 |
+===========+==============+=======================+
| 1         | -1000 - 1000 | milligauss per ampere |
+-----------+--------------+-----------------------+




.. _COMPASS_ORIENT:

COMPASS\_ORIENT: Compass orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The orientation of the first external compass relative to the vehicle frame\. This value will be ignored unless this compass is set as an external compass\. When set correctly in the northern hemisphere\, pointing the nose and right side down should increase the MagX and MagY values respectively\. Rolling the vehicle upside down should decrease the MagZ value\. For southern hemisphere\, switch increase and decrease\. NOTE\: For internal compasses\, AHRS\_ORIENT is used\. The label for each option is specified in the order of rotations for that orientation\.


+----------------------------------+
| Values                           |
+==================================+
| +-------+----------------------+ |
| | Value | Meaning              | |
| +=======+======================+ |
| | 0     | None                 | |
| +-------+----------------------+ |
| | 1     | Yaw45                | |
| +-------+----------------------+ |
| | 2     | Yaw90                | |
| +-------+----------------------+ |
| | 3     | Yaw135               | |
| +-------+----------------------+ |
| | 4     | Yaw180               | |
| +-------+----------------------+ |
| | 5     | Yaw225               | |
| +-------+----------------------+ |
| | 6     | Yaw270               | |
| +-------+----------------------+ |
| | 7     | Yaw315               | |
| +-------+----------------------+ |
| | 8     | Roll180              | |
| +-------+----------------------+ |
| | 9     | Yaw45Roll180         | |
| +-------+----------------------+ |
| | 10    | Yaw90Roll180         | |
| +-------+----------------------+ |
| | 11    | Yaw135Roll180        | |
| +-------+----------------------+ |
| | 12    | Pitch180             | |
| +-------+----------------------+ |
| | 13    | Yaw225Roll180        | |
| +-------+----------------------+ |
| | 14    | Yaw270Roll180        | |
| +-------+----------------------+ |
| | 15    | Yaw315Roll180        | |
| +-------+----------------------+ |
| | 16    | Roll90               | |
| +-------+----------------------+ |
| | 17    | Yaw45Roll90          | |
| +-------+----------------------+ |
| | 18    | Yaw90Roll90          | |
| +-------+----------------------+ |
| | 19    | Yaw135Roll90         | |
| +-------+----------------------+ |
| | 20    | Roll270              | |
| +-------+----------------------+ |
| | 21    | Yaw45Roll270         | |
| +-------+----------------------+ |
| | 22    | Yaw90Roll270         | |
| +-------+----------------------+ |
| | 23    | Yaw135Roll270        | |
| +-------+----------------------+ |
| | 24    | Pitch90              | |
| +-------+----------------------+ |
| | 25    | Pitch270             | |
| +-------+----------------------+ |
| | 26    | Yaw90Pitch180        | |
| +-------+----------------------+ |
| | 27    | Yaw270Pitch180       | |
| +-------+----------------------+ |
| | 28    | Pitch90Roll90        | |
| +-------+----------------------+ |
| | 29    | Pitch90Roll180       | |
| +-------+----------------------+ |
| | 30    | Pitch90Roll270       | |
| +-------+----------------------+ |
| | 31    | Pitch180Roll90       | |
| +-------+----------------------+ |
| | 32    | Pitch180Roll270      | |
| +-------+----------------------+ |
| | 33    | Pitch270Roll90       | |
| +-------+----------------------+ |
| | 34    | Pitch270Roll180      | |
| +-------+----------------------+ |
| | 35    | Pitch270Roll270      | |
| +-------+----------------------+ |
| | 36    | Yaw90Pitch180Roll90  | |
| +-------+----------------------+ |
| | 37    | Yaw270Roll90         | |
| +-------+----------------------+ |
| | 38    | Yaw293Pitch68Roll180 | |
| +-------+----------------------+ |
| | 39    | Pitch315             | |
| +-------+----------------------+ |
| | 40    | Pitch315Roll90       | |
| +-------+----------------------+ |
| | 42    | Roll45               | |
| +-------+----------------------+ |
| | 43    | Roll315              | |
| +-------+----------------------+ |
| | 100   | Custom               | |
| +-------+----------------------+ |
|                                  |
+----------------------------------+




.. _COMPASS_EXTERNAL:

COMPASS\_EXTERNAL: Compass is attached via an external cable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Configure compass so it is attached externally\. This is auto\-detected on most boards\. Set to 1 if the compass is externally connected\. When externally connected the COMPASS\_ORIENT option operates independently of the AHRS\_ORIENTATION board orientation option\. If set to 0 or 1 then auto\-detection by bus connection can override the value\. If set to 2 then auto\-detection will be disabled\.


+----------------------------+
| Values                     |
+============================+
| +-------+----------------+ |
| | Value | Meaning        | |
| +=======+================+ |
| | 0     | Internal       | |
| +-------+----------------+ |
| | 1     | External       | |
| +-------+----------------+ |
| | 2     | ForcedExternal | |
| +-------+----------------+ |
|                            |
+----------------------------+




.. _COMPASS_OFS2_X:

COMPASS\_OFS2\_X: Compass2 offsets in milligauss on the X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass2\'s x\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS2_Y:

COMPASS\_OFS2\_Y: Compass2 offsets in milligauss on the Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass2\'s y\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS2_Z:

COMPASS\_OFS2\_Z: Compass2 offsets in milligauss on the Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass2\'s z\-axis values to compensate for metal in the frame


+-----------+------------+------------+
| Increment | Range      | Units      |
+===========+============+============+
| 1         | -400 - 400 | milligauss |
+-----------+------------+------------+




.. _COMPASS_MOT2_X:

COMPASS\_MOT2\_X: Motor interference compensation to compass2 for body frame X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass2\'s x\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT2_Y:

COMPASS\_MOT2\_Y: Motor interference compensation to compass2 for body frame Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass2\'s y\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT2_Z:

COMPASS\_MOT2\_Z: Motor interference compensation to compass2 for body frame Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass2\'s z\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-----------+--------------+-----------------------+
| Increment | Range        | Units                 |
+===========+==============+=======================+
| 1         | -1000 - 1000 | milligauss per ampere |
+-----------+--------------+-----------------------+




.. _COMPASS_OFS3_X:

COMPASS\_OFS3\_X: Compass3 offsets in milligauss on the X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass3\'s x\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS3_Y:

COMPASS\_OFS3\_Y: Compass3 offsets in milligauss on the Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass3\'s y\-axis values to compensate for metal in the frame


+-------------+-----------+------------+------------+
| Calibration | Increment | Range      | Units      |
+=============+===========+============+============+
| 1           | 1         | -400 - 400 | milligauss |
+-------------+-----------+------------+------------+




.. _COMPASS_OFS3_Z:

COMPASS\_OFS3\_Z: Compass3 offsets in milligauss on the Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Offset to be added to compass3\'s z\-axis values to compensate for metal in the frame


+-----------+------------+------------+
| Increment | Range      | Units      |
+===========+============+============+
| 1         | -400 - 400 | milligauss |
+-----------+------------+------------+




.. _COMPASS_MOT3_X:

COMPASS\_MOT3\_X: Motor interference compensation to compass3 for body frame X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass3\'s x\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT3_Y:

COMPASS\_MOT3\_Y: Motor interference compensation to compass3 for body frame Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass3\'s y\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-------------+-----------+--------------+-----------------------+
| Calibration | Increment | Range        | Units                 |
+=============+===========+==============+=======================+
| 1           | 1         | -1000 - 1000 | milligauss per ampere |
+-------------+-----------+--------------+-----------------------+




.. _COMPASS_MOT3_Z:

COMPASS\_MOT3\_Z: Motor interference compensation to compass3 for body frame Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Multiplied by the current throttle and added to compass3\'s z\-axis values to compensate for motor interference \(Offset per Amp or at Full Throttle\)


+-----------+--------------+-----------------------+
| Increment | Range        | Units                 |
+===========+==============+=======================+
| 1         | -1000 - 1000 | milligauss per ampere |
+-----------+--------------+-----------------------+




.. _COMPASS_DEV_ID:

COMPASS\_DEV\_ID: Compass device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compass device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID2:

COMPASS\_DEV\_ID2: Compass2 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Second compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID3:

COMPASS\_DEV\_ID3: Compass3 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Third compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_USE2:

COMPASS\_USE2: Compass2 used for yaw
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable or disable the secondary compass for determining heading\.


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




.. _COMPASS_ORIENT2:

COMPASS\_ORIENT2: Compass2 orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The orientation of a second external compass relative to the vehicle frame\. This value will be ignored unless this compass is set as an external compass\. When set correctly in the northern hemisphere\, pointing the nose and right side down should increase the MagX and MagY values respectively\. Rolling the vehicle upside down should decrease the MagZ value\. For southern hemisphere\, switch increase and decrease\. NOTE\: For internal compasses\, AHRS\_ORIENT is used\.


+----------------------------------+
| Values                           |
+==================================+
| +-------+----------------------+ |
| | Value | Meaning              | |
| +=======+======================+ |
| | 0     | None                 | |
| +-------+----------------------+ |
| | 1     | Yaw45                | |
| +-------+----------------------+ |
| | 2     | Yaw90                | |
| +-------+----------------------+ |
| | 3     | Yaw135               | |
| +-------+----------------------+ |
| | 4     | Yaw180               | |
| +-------+----------------------+ |
| | 5     | Yaw225               | |
| +-------+----------------------+ |
| | 6     | Yaw270               | |
| +-------+----------------------+ |
| | 7     | Yaw315               | |
| +-------+----------------------+ |
| | 8     | Roll180              | |
| +-------+----------------------+ |
| | 9     | Roll180Yaw45         | |
| +-------+----------------------+ |
| | 10    | Roll180Yaw90         | |
| +-------+----------------------+ |
| | 11    | Roll180Yaw135        | |
| +-------+----------------------+ |
| | 12    | Pitch180             | |
| +-------+----------------------+ |
| | 13    | Roll180Yaw225        | |
| +-------+----------------------+ |
| | 14    | Roll180Yaw270        | |
| +-------+----------------------+ |
| | 15    | Roll180Yaw315        | |
| +-------+----------------------+ |
| | 16    | Roll90               | |
| +-------+----------------------+ |
| | 17    | Roll90Yaw45          | |
| +-------+----------------------+ |
| | 18    | Roll90Yaw90          | |
| +-------+----------------------+ |
| | 19    | Roll90Yaw135         | |
| +-------+----------------------+ |
| | 20    | Roll270              | |
| +-------+----------------------+ |
| | 21    | Roll270Yaw45         | |
| +-------+----------------------+ |
| | 22    | Roll270Yaw90         | |
| +-------+----------------------+ |
| | 23    | Roll270Yaw135        | |
| +-------+----------------------+ |
| | 24    | Pitch90              | |
| +-------+----------------------+ |
| | 25    | Pitch270             | |
| +-------+----------------------+ |
| | 26    | Pitch180Yaw90        | |
| +-------+----------------------+ |
| | 27    | Pitch180Yaw270       | |
| +-------+----------------------+ |
| | 28    | Roll90Pitch90        | |
| +-------+----------------------+ |
| | 29    | Roll180Pitch90       | |
| +-------+----------------------+ |
| | 30    | Roll270Pitch90       | |
| +-------+----------------------+ |
| | 31    | Roll90Pitch180       | |
| +-------+----------------------+ |
| | 32    | Roll270Pitch180      | |
| +-------+----------------------+ |
| | 33    | Roll90Pitch270       | |
| +-------+----------------------+ |
| | 34    | Roll180Pitch270      | |
| +-------+----------------------+ |
| | 35    | Roll270Pitch270      | |
| +-------+----------------------+ |
| | 36    | Roll90Pitch180Yaw90  | |
| +-------+----------------------+ |
| | 37    | Roll90Yaw270         | |
| +-------+----------------------+ |
| | 38    | Yaw293Pitch68Roll180 | |
| +-------+----------------------+ |
| | 39    | Pitch315             | |
| +-------+----------------------+ |
| | 40    | Roll90Pitch315       | |
| +-------+----------------------+ |
| | 42    | Roll45               | |
| +-------+----------------------+ |
| | 43    | Roll315              | |
| +-------+----------------------+ |
| | 100   | Custom               | |
| +-------+----------------------+ |
|                                  |
+----------------------------------+




.. _COMPASS_EXTERN2:

COMPASS\_EXTERN2: Compass2 is attached via an external cable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Configure second compass so it is attached externally\. This is auto\-detected on most boards\. If set to 0 or 1 then auto\-detection by bus connection can override the value\. If set to 2 then auto\-detection will be disabled\.


+----------------------------+
| Values                     |
+============================+
| +-------+----------------+ |
| | Value | Meaning        | |
| +=======+================+ |
| | 0     | Internal       | |
| +-------+----------------+ |
| | 1     | External       | |
| +-------+----------------+ |
| | 2     | ForcedExternal | |
| +-------+----------------+ |
|                            |
+----------------------------+




.. _COMPASS_USE3:

COMPASS\_USE3: Compass3 used for yaw
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable or disable the tertiary compass for determining heading\.


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




.. _COMPASS_ORIENT3:

COMPASS\_ORIENT3: Compass3 orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The orientation of a third external compass relative to the vehicle frame\. This value will be ignored unless this compass is set as an external compass\. When set correctly in the northern hemisphere\, pointing the nose and right side down should increase the MagX and MagY values respectively\. Rolling the vehicle upside down should decrease the MagZ value\. For southern hemisphere\, switch increase and decrease\. NOTE\: For internal compasses\, AHRS\_ORIENT is used\.


+----------------------------------+
| Values                           |
+==================================+
| +-------+----------------------+ |
| | Value | Meaning              | |
| +=======+======================+ |
| | 0     | None                 | |
| +-------+----------------------+ |
| | 1     | Yaw45                | |
| +-------+----------------------+ |
| | 2     | Yaw90                | |
| +-------+----------------------+ |
| | 3     | Yaw135               | |
| +-------+----------------------+ |
| | 4     | Yaw180               | |
| +-------+----------------------+ |
| | 5     | Yaw225               | |
| +-------+----------------------+ |
| | 6     | Yaw270               | |
| +-------+----------------------+ |
| | 7     | Yaw315               | |
| +-------+----------------------+ |
| | 8     | Roll180              | |
| +-------+----------------------+ |
| | 9     | Roll180Yaw45         | |
| +-------+----------------------+ |
| | 10    | Roll180Yaw90         | |
| +-------+----------------------+ |
| | 11    | Roll180Yaw135        | |
| +-------+----------------------+ |
| | 12    | Pitch180             | |
| +-------+----------------------+ |
| | 13    | Roll180Yaw225        | |
| +-------+----------------------+ |
| | 14    | Roll180Yaw270        | |
| +-------+----------------------+ |
| | 15    | Roll180Yaw315        | |
| +-------+----------------------+ |
| | 16    | Roll90               | |
| +-------+----------------------+ |
| | 17    | Roll90Yaw45          | |
| +-------+----------------------+ |
| | 18    | Roll90Yaw90          | |
| +-------+----------------------+ |
| | 19    | Roll90Yaw135         | |
| +-------+----------------------+ |
| | 20    | Roll270              | |
| +-------+----------------------+ |
| | 21    | Roll270Yaw45         | |
| +-------+----------------------+ |
| | 22    | Roll270Yaw90         | |
| +-------+----------------------+ |
| | 23    | Roll270Yaw135        | |
| +-------+----------------------+ |
| | 24    | Pitch90              | |
| +-------+----------------------+ |
| | 25    | Pitch270             | |
| +-------+----------------------+ |
| | 26    | Pitch180Yaw90        | |
| +-------+----------------------+ |
| | 27    | Pitch180Yaw270       | |
| +-------+----------------------+ |
| | 28    | Roll90Pitch90        | |
| +-------+----------------------+ |
| | 29    | Roll180Pitch90       | |
| +-------+----------------------+ |
| | 30    | Roll270Pitch90       | |
| +-------+----------------------+ |
| | 31    | Roll90Pitch180       | |
| +-------+----------------------+ |
| | 32    | Roll270Pitch180      | |
| +-------+----------------------+ |
| | 33    | Roll90Pitch270       | |
| +-------+----------------------+ |
| | 34    | Roll180Pitch270      | |
| +-------+----------------------+ |
| | 35    | Roll270Pitch270      | |
| +-------+----------------------+ |
| | 36    | Roll90Pitch180Yaw90  | |
| +-------+----------------------+ |
| | 37    | Roll90Yaw270         | |
| +-------+----------------------+ |
| | 38    | Yaw293Pitch68Roll180 | |
| +-------+----------------------+ |
| | 39    | Pitch315             | |
| +-------+----------------------+ |
| | 40    | Roll90Pitch315       | |
| +-------+----------------------+ |
| | 42    | Roll45               | |
| +-------+----------------------+ |
| | 43    | Roll315              | |
| +-------+----------------------+ |
| | 100   | Custom               | |
| +-------+----------------------+ |
|                                  |
+----------------------------------+




.. _COMPASS_EXTERN3:

COMPASS\_EXTERN3: Compass3 is attached via an external cable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Configure third compass so it is attached externally\. This is auto\-detected on most boards\. If set to 0 or 1 then auto\-detection by bus connection can override the value\. If set to 2 then auto\-detection will be disabled\.


+----------------------------+
| Values                     |
+============================+
| +-------+----------------+ |
| | Value | Meaning        | |
| +=======+================+ |
| | 0     | Internal       | |
| +-------+----------------+ |
| | 1     | External       | |
| +-------+----------------+ |
| | 2     | ForcedExternal | |
| +-------+----------------+ |
|                            |
+----------------------------+




.. _COMPASS_DIA_X:

COMPASS\_DIA\_X: Compass soft\-iron diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_X in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA_Y:

COMPASS\_DIA\_Y: Compass soft\-iron diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Y in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA_Z:

COMPASS\_DIA\_Z: Compass soft\-iron diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Z in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_ODI_X:

COMPASS\_ODI\_X: Compass soft\-iron off\-diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_X in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI_Y:

COMPASS\_ODI\_Y: Compass soft\-iron off\-diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Y in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI_Z:

COMPASS\_ODI\_Z: Compass soft\-iron off\-diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Z in the compass soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_DIA2_X:

COMPASS\_DIA2\_X: Compass2 soft\-iron diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_X in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA2_Y:

COMPASS\_DIA2\_Y: Compass2 soft\-iron diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Y in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA2_Z:

COMPASS\_DIA2\_Z: Compass2 soft\-iron diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Z in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_ODI2_X:

COMPASS\_ODI2\_X: Compass2 soft\-iron off\-diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_X in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI2_Y:

COMPASS\_ODI2\_Y: Compass2 soft\-iron off\-diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Y in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI2_Z:

COMPASS\_ODI2\_Z: Compass2 soft\-iron off\-diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Z in the compass2 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_DIA3_X:

COMPASS\_DIA3\_X: Compass3 soft\-iron diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_X in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA3_Y:

COMPASS\_DIA3\_Y: Compass3 soft\-iron diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Y in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_DIA3_Z:

COMPASS\_DIA3\_Z: Compass3 soft\-iron diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

DIA\_Z in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_ODI3_X:

COMPASS\_ODI3\_X: Compass3 soft\-iron off\-diagonal X component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_X in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI3_Y:

COMPASS\_ODI3\_Y: Compass3 soft\-iron off\-diagonal Y component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Y in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _COMPASS_ODI3_Z:

COMPASS\_ODI3\_Z: Compass3 soft\-iron off\-diagonal Z component
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

ODI\_Z in the compass3 soft\-iron calibration matrix\: \[\[DIA\_X\, ODI\_X\, ODI\_Y\]\, \[ODI\_X\, DIA\_Y\, ODI\_Z\]\, \[ODI\_Y\, ODI\_Z\, DIA\_Z\]\]


.. _COMPASS_CAL_FIT:

COMPASS\_CAL\_FIT: Compass calibration fitness
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls the fitness level required for a successful compass calibration\. A lower value makes for a stricter fit \(less likely to pass\)\. This is the value used for the primary magnetometer\. Other magnetometers get double the value\.


+-----------+--------+-------------------------+
| Increment | Range  | Values                  |
+===========+========+=========================+
| 0.1       | 4 - 32 | +-------+-------------+ |
|           |        | | Value | Meaning     | |
|           |        | +=======+=============+ |
|           |        | | 4     | Very Strict | |
|           |        | +-------+-------------+ |
|           |        | | 8     | Strict      | |
|           |        | +-------+-------------+ |
|           |        | | 16    | Default     | |
|           |        | +-------+-------------+ |
|           |        | | 32    | Relaxed     | |
|           |        | +-------+-------------+ |
|           |        |                         |
+-----------+--------+-------------------------+




.. _COMPASS_OFFS_MAX:

COMPASS\_OFFS\_MAX: Compass maximum offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the maximum allowed compass offset in calibration and arming checks


+-----------+------------+
| Increment | Range      |
+===========+============+
| 1         | 500 - 3000 |
+-----------+------------+




.. _COMPASS_TYPEMASK:

COMPASS\_TYPEMASK: Compass disable driver type mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is a bitmask of driver types to disable\. If a driver type is set in this mask then that driver will not try to find a sensor at startup


+------------------------+
| Bitmask                |
+========================+
| +-----+--------------+ |
| | Bit | Meaning      | |
| +=====+==============+ |
| | 0   | HMC5883      | |
| +-----+--------------+ |
| | 1   | LSM303D      | |
| +-----+--------------+ |
| | 2   | AK8963       | |
| +-----+--------------+ |
| | 3   | BMM150       | |
| +-----+--------------+ |
| | 4   | LSM9DS1      | |
| +-----+--------------+ |
| | 5   | LIS3MDL      | |
| +-----+--------------+ |
| | 6   | AK09916      | |
| +-----+--------------+ |
| | 7   | IST8310      | |
| +-----+--------------+ |
| | 8   | ICM20948     | |
| +-----+--------------+ |
| | 9   | MMC3416      | |
| +-----+--------------+ |
| | 11  | UAVCAN       | |
| +-----+--------------+ |
| | 12  | QMC5883      | |
| +-----+--------------+ |
| | 14  | MAG3110      | |
| +-----+--------------+ |
| | 15  | IST8308      | |
| +-----+--------------+ |
| | 16  | RM3100       | |
| +-----+--------------+ |
| | 17  | MSP          | |
| +-----+--------------+ |
| | 18  | ExternalAHRS | |
| +-----+--------------+ |
|                        |
+------------------------+




.. _COMPASS_FLTR_RNG:

COMPASS\_FLTR\_RNG: Range in which sample is accepted
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the range around the average value that new samples must be within to be accepted\. This can help reduce the impact of noise on sensors that are on long I2C cables\. The value is a percentage from the average value\. A value of zero disables this filter\.


+-----------+---------+---------+
| Increment | Range   | Units   |
+===========+=========+=========+
| 1         | 0 - 100 | percent |
+-----------+---------+---------+




.. _COMPASS_AUTO_ROT:

COMPASS\_AUTO\_ROT: Automatically check orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


When enabled this will automatically check the orientation of compasses on successful completion of compass calibration\. If set to 2 then external compasses will have their orientation automatically corrected\.


+----------------------------------------------------------------+
| Values                                                         |
+================================================================+
| +-------+----------------------------------------------------+ |
| | Value | Meaning                                            | |
| +=======+====================================================+ |
| | 0     | Disabled                                           | |
| +-------+----------------------------------------------------+ |
| | 1     | CheckOnly                                          | |
| +-------+----------------------------------------------------+ |
| | 2     | CheckAndFix                                        | |
| +-------+----------------------------------------------------+ |
| | 3     | use same tolerance to auto rotate 45 deg rotations | |
| +-------+----------------------------------------------------+ |
|                                                                |
+----------------------------------------------------------------+




.. _COMPASS_PRIO1_ID:

COMPASS\_PRIO1\_ID: Compass device id with 1st order priority
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass device id with 1st order priority\, set automatically if 0\. Reboot required after change\.


.. _COMPASS_PRIO2_ID:

COMPASS\_PRIO2\_ID: Compass device id with 2nd order priority
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass device id with 2nd order priority\, set automatically if 0\. Reboot required after change\.


.. _COMPASS_PRIO3_ID:

COMPASS\_PRIO3\_ID: Compass device id with 3rd order priority
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass device id with 3rd order priority\, set automatically if 0\. Reboot required after change\.


.. _COMPASS_ENABLE:

COMPASS\_ENABLE: Enable Compass
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Setting this to Enabled\(1\) will enable the compass\. Setting this to Disabled\(0\) will disable the compass\. Note that this is separate from COMPASS\_USE\. This will enable the low level senor\, and will enable logging of magnetometer data\. To use the compass for navigation you must also set COMPASS\_USE to 1\.


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




.. _COMPASS_SCALE:

COMPASS\_SCALE: Compass1 scale factor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Scaling factor for first compass to compensate for sensor scaling errors\. If this is 0 then no scaling is done


+---------+
| Range   |
+=========+
| 0 - 1.3 |
+---------+




.. _COMPASS_SCALE2:

COMPASS\_SCALE2: Compass2 scale factor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Scaling factor for 2nd compass to compensate for sensor scaling errors\. If this is 0 then no scaling is done


+---------+
| Range   |
+=========+
| 0 - 1.3 |
+---------+




.. _COMPASS_SCALE3:

COMPASS\_SCALE3: Compass3 scale factor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Scaling factor for 3rd compass to compensate for sensor scaling errors\. If this is 0 then no scaling is done


+---------+
| Range   |
+=========+
| 0 - 1.3 |
+---------+




.. _COMPASS_OPTIONS:

COMPASS\_OPTIONS: Compass options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets options to change the behaviour of the compass


+-------------------------+
| Bitmask                 |
+=========================+
| +-----+---------------+ |
| | Bit | Meaning       | |
| +=====+===============+ |
| | 0   | CalRequireGPS | |
| +-----+---------------+ |
|                         |
+-------------------------+




.. _COMPASS_DEV_ID4:

COMPASS\_DEV\_ID4: Compass4 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra 4th compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID5:

COMPASS\_DEV\_ID5: Compass5 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra 5th compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID6:

COMPASS\_DEV\_ID6: Compass6 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra 6th compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID7:

COMPASS\_DEV\_ID7: Compass7 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra 7th compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_DEV_ID8:

COMPASS\_DEV\_ID8: Compass8 device id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra 8th compass\'s device id\.  Automatically detected\, do not set manually


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _COMPASS_CUS_ROLL:

COMPASS\_CUS\_ROLL: Custom orientation roll offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass mounting position roll offset\. Positive values \= roll right\, negative values \= roll left\. This parameter is only used when COMPASS\_ORIENT\/2\/3 is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+




.. _COMPASS_CUS_PIT:

COMPASS\_CUS\_PIT: Custom orientation pitch offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass mounting position pitch offset\. Positive values \= pitch up\, negative values \= pitch down\. This parameter is only used when COMPASS\_ORIENT\/2\/3 is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+




.. _COMPASS_CUS_YAW:

COMPASS\_CUS\_YAW: Custom orientation yaw offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Compass mounting position yaw offset\. Positive values \= yaw right\, negative values \= yaw left\. This parameter is only used when COMPASS\_ORIENT\/2\/3 is set to CUSTOM\.


+-----------+------------+---------+
| Increment | Range      | Units   |
+===========+============+=========+
| 1         | -180 - 180 | degrees |
+-----------+------------+---------+





.. _parameters_COMPASS_PMOT:

COMPASS\_PMOT Parameters
------------------------


.. _COMPASS_PMOT_EN:

COMPASS\_PMOT\_EN: per\-motor compass correction enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This enables per\-motor compass corrections


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




.. _COMPASS_PMOT_EXP:

COMPASS\_PMOT\_EXP: per\-motor exponential correction
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the exponential correction for the power output of the motor for per\-motor compass correction


+-----------+-------+
| Increment | Range |
+===========+=======+
| 0.01      | 0 - 2 |
+-----------+-------+




.. _COMPASS_PMOT1_X:

COMPASS\_PMOT1\_X: Compass per\-motor1 X
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for X axis of motor1


.. _COMPASS_PMOT1_Y:

COMPASS\_PMOT1\_Y: Compass per\-motor1 Y
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Y axis of motor1


.. _COMPASS_PMOT1_Z:

COMPASS\_PMOT1\_Z: Compass per\-motor1 Z
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Z axis of motor1


.. _COMPASS_PMOT2_X:

COMPASS\_PMOT2\_X: Compass per\-motor2 X
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for X axis of motor2


.. _COMPASS_PMOT2_Y:

COMPASS\_PMOT2\_Y: Compass per\-motor2 Y
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Y axis of motor2


.. _COMPASS_PMOT2_Z:

COMPASS\_PMOT2\_Z: Compass per\-motor2 Z
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Z axis of motor2


.. _COMPASS_PMOT3_X:

COMPASS\_PMOT3\_X: Compass per\-motor3 X
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for X axis of motor3


.. _COMPASS_PMOT3_Y:

COMPASS\_PMOT3\_Y: Compass per\-motor3 Y
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Y axis of motor3


.. _COMPASS_PMOT3_Z:

COMPASS\_PMOT3\_Z: Compass per\-motor3 Z
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Z axis of motor3


.. _COMPASS_PMOT4_X:

COMPASS\_PMOT4\_X: Compass per\-motor4 X
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for X axis of motor4


.. _COMPASS_PMOT4_Y:

COMPASS\_PMOT4\_Y: Compass per\-motor4 Y
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Y axis of motor4


.. _COMPASS_PMOT4_Z:

COMPASS\_PMOT4\_Z: Compass per\-motor4 Z
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Compensation for Z axis of motor4



.. _parameters_EAHRS:

EAHRS Parameters
----------------


.. _EAHRS_TYPE:

EAHRS\_TYPE: AHRS type
~~~~~~~~~~~~~~~~~~~~~~


Type of AHRS device


+-----------------------+
| Values                |
+=======================+
| +-------+-----------+ |
| | Value | Meaning   | |
| +=======+===========+ |
| | 0     | None      | |
| +-------+-----------+ |
| | 1     | VectorNav | |
| +-------+-----------+ |
| | 2     | LORD      | |
| +-------+-----------+ |
|                       |
+-----------------------+




.. _EAHRS_RATE:

EAHRS\_RATE: AHRS data rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~


Requested rate for AHRS device


+-------+
| Units |
+=======+
| hertz |
+-------+





.. _parameters_EFI:

EFI Parameters
--------------


.. _EFI_TYPE:

EFI\_TYPE: EFI communication type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

What method of communication is used for EFI \#1


+-----------------------+
| Values                |
+=======================+
| +-------+-----------+ |
| | Value | Meaning   | |
| +=======+===========+ |
| | 0     | None      | |
| +-------+-----------+ |
| | 1     | Serial-MS | |
| +-------+-----------+ |
| | 2     | NWPMU     | |
| +-------+-----------+ |
|                       |
+-----------------------+




.. _EFI_COEF1:

EFI\_COEF1: EFI Calibration Coefficient 1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to calibrate fuel flow for MS protocol \(Slope\)


+-------+
| Range |
+=======+
| 0 - 1 |
+-------+




.. _EFI_COEF2:

EFI\_COEF2: EFI Calibration Coefficient 2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Used to calibrate fuel flow for MS protocol \(Offset\)


+--------+
| Range  |
+========+
| 0 - 10 |
+--------+





.. _parameters_FFT_:

FFT\_ Parameters
----------------


.. _FFT_ENABLE:

FFT\_ENABLE: Enable
~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable Gyro FFT analyser


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




.. _FFT_MINHZ:

FFT\_MINHZ: Minimum Frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Lower bound of FFT frequency detection in Hz\. On larger vehicles the minimum motor frequency is likely to be significantly lower than for smaller vehicles\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 20 - 400 | hertz |
+----------+-------+




.. _FFT_MAXHZ:

FFT\_MAXHZ: Maximum Frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Upper bound of FFT frequency detection in Hz\. On smaller vehicles the maximum motor frequency is likely to be significantly higher than for larger vehicles\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 20 - 495 | hertz |
+----------+-------+




.. _FFT_SAMPLE_MODE:

FFT\_SAMPLE\_MODE: Sample Mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Sampling mode \(and therefore rate\)\. 0\: Gyro rate sampling\, 1\: Fast loop rate sampling\, 2\: Fast loop rate \/ 2 sampling\, 3\: Fast loop rate \/ 3 sampling\. Takes effect on reboot\.


+-------+
| Range |
+=======+
| 0 - 4 |
+-------+




.. _FFT_WINDOW_SIZE:

FFT\_WINDOW\_SIZE: FFT window size
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Size of window to be used in FFT calculations\. Takes effect on reboot\. Must be a power of 2 and between 32 and 512\. Larger windows give greater frequency resolution but poorer time resolution\, consume more CPU time and may not be appropriate for all vehicles\. Time and frequency resolution are given by the sample\-rate \/ window\-size\. Windows of 256 are only really recommended for F7 class boards\, windows of 512 or more H7 class\.


+-----------+
| Range     |
+===========+
| 32 - 1024 |
+-----------+




.. _FFT_WINDOW_OLAP:

FFT\_WINDOW\_OLAP: FFT window overlap
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Percentage of window to be overlapped before another frame is process\. Takes effect on reboot\. A good default is 50\% overlap\. Higher overlap results in more processed frames but not necessarily more temporal resolution\. Lower overlap results in lost information at the frame edges\.


+---------+
| Range   |
+=========+
| 0 - 0.9 |
+---------+




.. _FFT_FREQ_HOVER:

FFT\_FREQ\_HOVER: FFT learned hover frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The learned hover noise frequency


+---------+
| Range   |
+=========+
| 0 - 250 |
+---------+




.. _FFT_THR_REF:

FFT\_THR\_REF: FFT learned thrust reference
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

FFT learned thrust reference for the hover frequency and FFT minimum frequency\.


+------------+
| Range      |
+============+
| 0.01 - 0.9 |
+------------+




.. _FFT_SNR_REF:

FFT\_SNR\_REF: FFT SNR reference threshold
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

FFT SNR reference threshold in dB at which a signal is determined to be present\.


+-------------+
| Range       |
+=============+
| 0.0 - 100.0 |
+-------------+




.. _FFT_ATT_REF:

FFT\_ATT\_REF: FFT attenuation for bandwidth calculation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

FFT attenuation level in dB for bandwidth calculation and peak detection\. The bandwidth is calculated by comparing peak power output with the attenuated version\. The default of 15 has shown to be a good compromise in both simulations and real flight\.


+---------+
| Range   |
+=========+
| 0 - 100 |
+---------+




.. _FFT_BW_HOVER:

FFT\_BW\_HOVER: FFT learned bandwidth at hover
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

FFT learned bandwidth at hover for the attenuation frequencies\.


+---------+
| Range   |
+=========+
| 0 - 200 |
+---------+




.. _FFT_HMNC_FIT:

FFT\_HMNC\_FIT: FFT harmonic fit frequency threshold
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

FFT harmonic fit frequency threshold percentage at which a signal of the appropriate frequency is determined to be the harmonic of another\. Signals that have a harmonic relationship that varies at most by this percentage are considered harmonics of each other for the purpose of selecting the harmonic notch frequency\. If a match is found then the lower frequency harmonic is always used as the basis for the dynamic harmonic notch\. A value of zero completely disables harmonic matching\.


+---------+
| Range   |
+=========+
| 0 - 100 |
+---------+




.. _FFT_HMNC_PEAK:

FFT\_HMNC\_PEAK: FFT harmonic peak target
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The FFT harmonic peak target that should be returned by FTN1\.PkAvg\. The resulting value will be used by the harmonic notch if configured to track the FFT frequency\. By default the appropriate peak is auto\-detected based on the harmonic fit between peaks and the energy\-weighted average frequency on roll on pitch is used\. Setting this to 1 will always target the highest energy peak\. Setting this to 2 will target the highest energy peak that is lower in frequency than the highest energy peak\. Setting this to 3 will target the highest energy peak that is higher in frequency than the highest energy peak\. Setting this to 4 will target the highest energy peak on the roll axis only and only the roll frequency will be used \(some vehicles have a much more pronounced peak on roll\)\. Setting this to 5 will target the highest energy peak on the pitch axis only and only the pitch frequency will be used \(some vehicles have a much more pronounced peak on roll\)\.


+--------------------------------------+
| Values                               |
+======================================+
| +-------+--------------------------+ |
| | Value | Meaning                  | |
| +=======+==========================+ |
| | 0     | Auto                     | |
| +-------+--------------------------+ |
| | 1     | Center Frequency         | |
| +-------+--------------------------+ |
| | 2     | Lower-Shoulder Frequency | |
| +-------+--------------------------+ |
| | 3     | Upper-Shoulder Frequency | |
| +-------+--------------------------+ |
| | 4     | Roll-Axis                | |
| +-------+--------------------------+ |
| | 5     | Pitch-Axis               | |
| +-------+--------------------------+ |
|                                      |
+--------------------------------------+





.. _parameters_FRSKY_:

FRSKY\_ Parameters
------------------


.. _FRSKY_UPLINK_ID:

FRSKY\_UPLINK\_ID: Uplink sensor id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Change the uplink sensor id \(SPort only\)


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | -1    | Disable | |
| +-------+---------+ |
| | 7     | 7       | |
| +-------+---------+ |
| | 8     | 8       | |
| +-------+---------+ |
| | 9     | 9       | |
| +-------+---------+ |
| | 10    | 10      | |
| +-------+---------+ |
| | 11    | 11      | |
| +-------+---------+ |
| | 12    | 12      | |
| +-------+---------+ |
| | 13    | 13      | |
| +-------+---------+ |
| | 14    | 14      | |
| +-------+---------+ |
| | 15    | 15      | |
| +-------+---------+ |
| | 16    | 16      | |
| +-------+---------+ |
| | 17    | 17      | |
| +-------+---------+ |
| | 18    | 18      | |
| +-------+---------+ |
| | 19    | 19      | |
| +-------+---------+ |
| | 20    | 20      | |
| +-------+---------+ |
| | 21    | 21      | |
| +-------+---------+ |
| | 22    | 22      | |
| +-------+---------+ |
| | 23    | 23      | |
| +-------+---------+ |
| | 24    | 24      | |
| +-------+---------+ |
| | 25    | 25      | |
| +-------+---------+ |
| | 26    | 26      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _FRSKY_DNLINK1_ID:

FRSKY\_DNLINK1\_ID: First downlink sensor id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Change the first extra downlink sensor id \(SPort only\)


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | -1    | Disable | |
| +-------+---------+ |
| | 7     | 7       | |
| +-------+---------+ |
| | 8     | 8       | |
| +-------+---------+ |
| | 9     | 9       | |
| +-------+---------+ |
| | 10    | 10      | |
| +-------+---------+ |
| | 11    | 11      | |
| +-------+---------+ |
| | 12    | 12      | |
| +-------+---------+ |
| | 13    | 13      | |
| +-------+---------+ |
| | 14    | 14      | |
| +-------+---------+ |
| | 15    | 15      | |
| +-------+---------+ |
| | 16    | 16      | |
| +-------+---------+ |
| | 17    | 17      | |
| +-------+---------+ |
| | 18    | 18      | |
| +-------+---------+ |
| | 19    | 19      | |
| +-------+---------+ |
| | 20    | 20      | |
| +-------+---------+ |
| | 21    | 21      | |
| +-------+---------+ |
| | 22    | 22      | |
| +-------+---------+ |
| | 23    | 23      | |
| +-------+---------+ |
| | 24    | 24      | |
| +-------+---------+ |
| | 25    | 25      | |
| +-------+---------+ |
| | 26    | 26      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _FRSKY_DNLINK2_ID:

FRSKY\_DNLINK2\_ID: Second downlink sensor id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Change the second extra downlink sensor id \(SPort only\)


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | -1    | Disable | |
| +-------+---------+ |
| | 7     | 7       | |
| +-------+---------+ |
| | 8     | 8       | |
| +-------+---------+ |
| | 9     | 9       | |
| +-------+---------+ |
| | 10    | 10      | |
| +-------+---------+ |
| | 11    | 11      | |
| +-------+---------+ |
| | 12    | 12      | |
| +-------+---------+ |
| | 13    | 13      | |
| +-------+---------+ |
| | 14    | 14      | |
| +-------+---------+ |
| | 15    | 15      | |
| +-------+---------+ |
| | 16    | 16      | |
| +-------+---------+ |
| | 17    | 17      | |
| +-------+---------+ |
| | 18    | 18      | |
| +-------+---------+ |
| | 19    | 19      | |
| +-------+---------+ |
| | 20    | 20      | |
| +-------+---------+ |
| | 21    | 21      | |
| +-------+---------+ |
| | 22    | 22      | |
| +-------+---------+ |
| | 23    | 23      | |
| +-------+---------+ |
| | 24    | 24      | |
| +-------+---------+ |
| | 25    | 25      | |
| +-------+---------+ |
| | 26    | 26      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _FRSKY_DNLINK_ID:

FRSKY\_DNLINK\_ID: Default downlink sensor id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Change the default downlink sensor id \(SPort only\)


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | -1    | Disable | |
| +-------+---------+ |
| | 7     | 7       | |
| +-------+---------+ |
| | 8     | 8       | |
| +-------+---------+ |
| | 9     | 9       | |
| +-------+---------+ |
| | 10    | 10      | |
| +-------+---------+ |
| | 11    | 11      | |
| +-------+---------+ |
| | 12    | 12      | |
| +-------+---------+ |
| | 13    | 13      | |
| +-------+---------+ |
| | 14    | 14      | |
| +-------+---------+ |
| | 15    | 15      | |
| +-------+---------+ |
| | 16    | 16      | |
| +-------+---------+ |
| | 17    | 17      | |
| +-------+---------+ |
| | 18    | 18      | |
| +-------+---------+ |
| | 19    | 19      | |
| +-------+---------+ |
| | 20    | 20      | |
| +-------+---------+ |
| | 21    | 21      | |
| +-------+---------+ |
| | 22    | 22      | |
| +-------+---------+ |
| | 23    | 23      | |
| +-------+---------+ |
| | 24    | 24      | |
| +-------+---------+ |
| | 25    | 25      | |
| +-------+---------+ |
| | 26    | 26      | |
| +-------+---------+ |
| | 27    | 27      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _FRSKY_OPTIONS:

FRSKY\_OPTIONS: FRSky Telemetry Options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


A bitmask to set some FRSky Telemetry specific options


+----------------------------------------+
| Bitmask                                |
+========================================+
| +-----+------------------------------+ |
| | Bit | Meaning                      | |
| +=====+==============================+ |
| | 0   | EnableAirspeedAndGroundspeed | |
| +-----+------------------------------+ |
|                                        |
+----------------------------------------+





.. _parameters_GEN_:

GEN\_ Parameters
----------------


.. _GEN_TYPE:

GEN\_TYPE: Generator type
~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Generator type


+------------------------------------+
| Values                             |
+====================================+
| +-------+------------------------+ |
| | Value | Meaning                | |
| +=======+========================+ |
| | 0     | Disabled               | |
| +-------+------------------------+ |
| | 1     | IE 650w 800w Fuel Cell | |
| +-------+------------------------+ |
| | 2     | IE 2.4kW Fuel Cell     | |
| +-------+------------------------+ |
| | 3     | Richenpower            | |
| +-------+------------------------+ |
|                                    |
+------------------------------------+





.. _parameters_GPS:

GPS Parameters
--------------


.. _GPS_TYPE:

GPS\_TYPE: 1st GPS type
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

GPS type of 1st GPS


+-----------------------------------------+
| Values                                  |
+=========================================+
| +-------+-----------------------------+ |
| | Value | Meaning                     | |
| +=======+=============================+ |
| | 0     | None                        | |
| +-------+-----------------------------+ |
| | 1     | AUTO                        | |
| +-------+-----------------------------+ |
| | 2     | uBlox                       | |
| +-------+-----------------------------+ |
| | 5     | NMEA                        | |
| +-------+-----------------------------+ |
| | 6     | SiRF                        | |
| +-------+-----------------------------+ |
| | 7     | HIL                         | |
| +-------+-----------------------------+ |
| | 8     | SwiftNav                    | |
| +-------+-----------------------------+ |
| | 9     | UAVCAN                      | |
| +-------+-----------------------------+ |
| | 10    | SBF                         | |
| +-------+-----------------------------+ |
| | 11    | GSOF                        | |
| +-------+-----------------------------+ |
| | 13    | ERB                         | |
| +-------+-----------------------------+ |
| | 14    | MAV                         | |
| +-------+-----------------------------+ |
| | 15    | NOVA                        | |
| +-------+-----------------------------+ |
| | 16    | HemisphereNMEA              | |
| +-------+-----------------------------+ |
| | 17    | uBlox-MovingBaseline-Base   | |
| +-------+-----------------------------+ |
| | 18    | uBlox-MovingBaseline-Rover  | |
| +-------+-----------------------------+ |
| | 19    | MSP                         | |
| +-------+-----------------------------+ |
| | 20    | AllyStar                    | |
| +-------+-----------------------------+ |
| | 21    | ExternalAHRS                | |
| +-------+-----------------------------+ |
| | 22    | UAVCAN-MovingBaseline-Base  | |
| +-------+-----------------------------+ |
| | 23    | UAVCAN-MovingBaseline-Rover | |
| +-------+-----------------------------+ |
|                                         |
+-----------------------------------------+




.. _GPS_TYPE2:

GPS\_TYPE2: 2nd GPS type
~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

GPS type of 2nd GPS


+-----------------------------------------+
| Values                                  |
+=========================================+
| +-------+-----------------------------+ |
| | Value | Meaning                     | |
| +=======+=============================+ |
| | 0     | None                        | |
| +-------+-----------------------------+ |
| | 1     | AUTO                        | |
| +-------+-----------------------------+ |
| | 2     | uBlox                       | |
| +-------+-----------------------------+ |
| | 5     | NMEA                        | |
| +-------+-----------------------------+ |
| | 6     | SiRF                        | |
| +-------+-----------------------------+ |
| | 7     | HIL                         | |
| +-------+-----------------------------+ |
| | 8     | SwiftNav                    | |
| +-------+-----------------------------+ |
| | 9     | UAVCAN                      | |
| +-------+-----------------------------+ |
| | 10    | SBF                         | |
| +-------+-----------------------------+ |
| | 11    | GSOF                        | |
| +-------+-----------------------------+ |
| | 13    | ERB                         | |
| +-------+-----------------------------+ |
| | 14    | MAV                         | |
| +-------+-----------------------------+ |
| | 15    | NOVA                        | |
| +-------+-----------------------------+ |
| | 16    | HemisphereNMEA              | |
| +-------+-----------------------------+ |
| | 17    | uBlox-MovingBaseline-Base   | |
| +-------+-----------------------------+ |
| | 18    | uBlox-MovingBaseline-Rover  | |
| +-------+-----------------------------+ |
| | 19    | MSP                         | |
| +-------+-----------------------------+ |
| | 20    | AllyStar                    | |
| +-------+-----------------------------+ |
| | 21    | ExternalAHRS                | |
| +-------+-----------------------------+ |
| | 22    | UAVCAN-MovingBaseline-Base  | |
| +-------+-----------------------------+ |
| | 23    | UAVCAN-MovingBaseline-Rover | |
| +-------+-----------------------------+ |
|                                         |
+-----------------------------------------+




.. _GPS_NAVFILTER:

GPS\_NAVFILTER: Navigation filter setting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Navigation filter engine setting


+------------------------+
| Values                 |
+========================+
| +-------+------------+ |
| | Value | Meaning    | |
| +=======+============+ |
| | 0     | Portable   | |
| +-------+------------+ |
| | 2     | Stationary | |
| +-------+------------+ |
| | 3     | Pedestrian | |
| +-------+------------+ |
| | 4     | Automotive | |
| +-------+------------+ |
| | 5     | Sea        | |
| +-------+------------+ |
| | 6     | Airborne1G | |
| +-------+------------+ |
| | 7     | Airborne2G | |
| +-------+------------+ |
| | 8     | Airborne4G | |
| +-------+------------+ |
|                        |
+------------------------+




.. _GPS_AUTO_SWITCH:

GPS\_AUTO\_SWITCH: Automatic Switchover Setting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Automatic switchover to GPS reporting best lock\, 1\:UseBest selects the GPS with highest status\, if both are equal the GPS with highest satellite count is used 4\:Use primary if 3D fix or better\, will revert to \'UseBest\' behaviour if 3D fix is lost on primary


+---------------------------------------------+
| Values                                      |
+=============================================+
| +-------+---------------------------------+ |
| | Value | Meaning                         | |
| +=======+=================================+ |
| | 0     | Use primary                     | |
| +-------+---------------------------------+ |
| | 1     | UseBest                         | |
| +-------+---------------------------------+ |
| | 2     | Blend                           | |
| +-------+---------------------------------+ |
| | 4     | Use primary if 3D fix or better | |
| +-------+---------------------------------+ |
|                                             |
+---------------------------------------------+




.. _GPS_MIN_DGPS:

GPS\_MIN\_DGPS: Minimum Lock Type Accepted for DGPS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Sets the minimum type of differential GPS corrections required before allowing to switch into DGPS mode\.


+------------------------+
| Values                 |
+========================+
| +-------+------------+ |
| | Value | Meaning    | |
| +=======+============+ |
| | 0     | Any        | |
| +-------+------------+ |
| | 50    | FloatRTK   | |
| +-------+------------+ |
| | 100   | IntegerRTK | |
| +-------+------------+ |
|                        |
+------------------------+




.. _GPS_SBAS_MODE:

GPS\_SBAS\_MODE: SBAS Mode
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the SBAS \(satellite based augmentation system\) mode if available on this GPS\. If set to 2 then the SBAS mode is not changed in the GPS\. Otherwise the GPS will be reconfigured to enable\/disable SBAS\. Disabling SBAS may be worthwhile in some parts of the world where an SBAS signal is available but the baseline is too long to be useful\.


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
| | 2     | NoChange | |
| +-------+----------+ |
|                      |
+----------------------+




.. _GPS_MIN_ELEV:

GPS\_MIN\_ELEV: Minimum elevation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the minimum elevation of satellites above the horizon for them to be used for navigation\. Setting this to \-100 leaves the minimum elevation set to the GPS modules default\.


+-----------+---------+
| Range     | Units   |
+===========+=========+
| -100 - 90 | degrees |
+-----------+---------+




.. _GPS_INJECT_TO:

GPS\_INJECT\_TO: Destination for GPS\_INJECT\_DATA MAVLink packets
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The GGS can send raw serial packets to inject data to multiple GPSes\.


+-------------------------------+
| Values                        |
+===============================+
| +-------+-------------------+ |
| | Value | Meaning           | |
| +=======+===================+ |
| | 0     | send to first GPS | |
| +-------+-------------------+ |
| | 1     | send to 2nd GPS   | |
| +-------+-------------------+ |
| | 127   | send to all       | |
| +-------+-------------------+ |
|                               |
+-------------------------------+




.. _GPS_SBP_LOGMASK:

GPS\_SBP\_LOGMASK: Swift Binary Protocol Logging Mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Masked with the SBP msg\_type field to determine whether SBR1\/SBR2 data is logged


+------------------------------------+
| Values                             |
+====================================+
| +-------+------------------------+ |
| | Value | Meaning                | |
| +=======+========================+ |
| | 0     | None (0x0000)          | |
| +-------+------------------------+ |
| | -1    | All (0xFFFF)           | |
| +-------+------------------------+ |
| | -256  | External only (0xFF00) | |
| +-------+------------------------+ |
|                                    |
+------------------------------------+




.. _GPS_RAW_DATA:

GPS\_RAW\_DATA: Raw data logging
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Handles logging raw data\; on uBlox chips that support raw data this will log RXM messages into logger\; on Septentrio this will log on the equipment\'s SD card and when set to 2\, the autopilot will try to stop logging after disarming and restart after arming


+------------------------------------------------------+
| Values                                               |
+======================================================+
| +-------+------------------------------------------+ |
| | Value | Meaning                                  | |
| +=======+==========================================+ |
| | 0     | Ignore                                   | |
| +-------+------------------------------------------+ |
| | 1     | Always log                               | |
| +-------+------------------------------------------+ |
| | 2     | Stop logging when disarmed (SBF only)    | |
| +-------+------------------------------------------+ |
| | 5     | Only log every five samples (uBlox only) | |
| +-------+------------------------------------------+ |
|                                                      |
+------------------------------------------------------+




.. _GPS_GNSS_MODE:

GPS\_GNSS\_MODE: GNSS system configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask for what GNSS system to use on the first GPS \(all unchecked or zero to leave GPS as configured\)


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | GPS     | |
| +-----+---------+ |
| | 1   | SBAS    | |
| +-----+---------+ |
| | 2   | Galileo | |
| +-----+---------+ |
| | 3   | Beidou  | |
| +-----+---------+ |
| | 4   | IMES    | |
| +-----+---------+ |
| | 5   | QZSS    | |
| +-----+---------+ |
| | 6   | GLONASS | |
| +-----+---------+ |
|                   |
+-------------------+




.. _GPS_SAVE_CFG:

GPS\_SAVE\_CFG: Save GPS configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Determines whether the configuration for this GPS should be written to non\-volatile memory on the GPS\. Currently working for UBlox 6 series and above\.


+-----------------------------------+
| Values                            |
+===================================+
| +-------+-----------------------+ |
| | Value | Meaning               | |
| +=======+=======================+ |
| | 0     | Do not save config    | |
| +-------+-----------------------+ |
| | 1     | Save config           | |
| +-------+-----------------------+ |
| | 2     | Save only when needed | |
| +-------+-----------------------+ |
|                                   |
+-----------------------------------+




.. _GPS_GNSS_MODE2:

GPS\_GNSS\_MODE2: GNSS system configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask for what GNSS system to use on the second GPS \(all unchecked or zero to leave GPS as configured\)


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | GPS     | |
| +-----+---------+ |
| | 1   | SBAS    | |
| +-----+---------+ |
| | 2   | Galileo | |
| +-----+---------+ |
| | 3   | Beidou  | |
| +-----+---------+ |
| | 4   | IMES    | |
| +-----+---------+ |
| | 5   | QZSS    | |
| +-----+---------+ |
| | 6   | GLONASS | |
| +-----+---------+ |
|                   |
+-------------------+




.. _GPS_AUTO_CONFIG:

GPS\_AUTO\_CONFIG: Automatic GPS configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls if the autopilot should automatically configure the GPS based on the parameters and default settings


+------------------------------------------------------------------+
| Values                                                           |
+==================================================================+
| +-------+------------------------------------------------------+ |
| | Value | Meaning                                              | |
| +=======+======================================================+ |
| | 0     | Disables automatic configuration                     | |
| +-------+------------------------------------------------------+ |
| | 1     | Enable automatic configuration for Serial GPSes only | |
| +-------+------------------------------------------------------+ |
| | 2     | Enable automatic configuration for UAVCAN as well    | |
| +-------+------------------------------------------------------+ |
|                                                                  |
+------------------------------------------------------------------+




.. _GPS_RATE_MS:

GPS\_RATE\_MS: GPS update rate in milliseconds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls how often the GPS should provide a position update\. Lowering below 5Hz\(default\) is not allowed\. Raising the rate above 5Hz usually provides little benefit and for some GPS \(eg Ublox M9N\) can severely impact performance\.


+----------+--------------+---------------------+
| Range    | Units        | Values              |
+==========+==============+=====================+
| 50 - 200 | milliseconds | +-------+---------+ |
|          |              | | Value | Meaning | |
|          |              | +=======+=========+ |
|          |              | | 100   | 10Hz    | |
|          |              | +-------+---------+ |
|          |              | | 125   | 8Hz     | |
|          |              | +-------+---------+ |
|          |              | | 200   | 5Hz     | |
|          |              | +-------+---------+ |
|          |              |                     |
+----------+--------------+---------------------+




.. _GPS_RATE_MS2:

GPS\_RATE\_MS2: GPS 2 update rate in milliseconds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls how often the GPS should provide a position update\. Lowering below 5Hz\(default\) is not allowed\. Raising the rate above 5Hz usually provides little benefit and for some GPS \(eg Ublox M9N\) can severely impact performance\.


+----------+--------------+---------------------+
| Range    | Units        | Values              |
+==========+==============+=====================+
| 50 - 200 | milliseconds | +-------+---------+ |
|          |              | | Value | Meaning | |
|          |              | +=======+=========+ |
|          |              | | 100   | 10Hz    | |
|          |              | +-------+---------+ |
|          |              | | 125   | 8Hz     | |
|          |              | +-------+---------+ |
|          |              | | 200   | 5Hz     | |
|          |              | +-------+---------+ |
|          |              |                     |
+----------+--------------+---------------------+




.. _GPS_POS1_X:

GPS\_POS1\_X: Antenna X position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the first GPS antenna in body frame\. Positive X is forward of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_POS1_Y:

GPS\_POS1\_Y: Antenna Y position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the first GPS antenna in body frame\. Positive Y is to the right of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_POS1_Z:

GPS\_POS1\_Z: Antenna Z position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the first GPS antenna in body frame\. Positive Z is down from the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_POS2_X:

GPS\_POS2\_X: Antenna X position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the second GPS antenna in body frame\. Positive X is forward of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_POS2_Y:

GPS\_POS2\_Y: Antenna Y position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the second GPS antenna in body frame\. Positive Y is to the right of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_POS2_Z:

GPS\_POS2\_Z: Antenna Z position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the second GPS antenna in body frame\. Positive Z is down from the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_DELAY_MS:

GPS\_DELAY\_MS: GPS delay in milliseconds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Controls the amount of GPS  measurement delay that the autopilot compensates for\. Set to zero to use the default delay for the detected GPS type\.


+---------+--------------+
| Range   | Units        |
+=========+==============+
| 0 - 250 | milliseconds |
+---------+--------------+




.. _GPS_DELAY_MS2:

GPS\_DELAY\_MS2: GPS 2 delay in milliseconds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Controls the amount of GPS  measurement delay that the autopilot compensates for\. Set to zero to use the default delay for the detected GPS type\.


+---------+--------------+
| Range   | Units        |
+=========+==============+
| 0 - 250 | milliseconds |
+---------+--------------+




.. _GPS_BLEND_MASK:

GPS\_BLEND\_MASK: Multi GPS Blending Mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Determines which of the accuracy measures Horizontal position\, Vertical Position and Speed are used to calculate the weighting on each GPS receiver when soft switching has been selected by setting GPS\_AUTO\_SWITCH to 2\(Blend\)


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Horiz Pos | |
| +-----+-----------+ |
| | 1   | Vert Pos  | |
| +-----+-----------+ |
| | 2   | Speed     | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _GPS_BLEND_TC:

GPS\_BLEND\_TC: Blending time constant
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls the slowest time constant applied to the calculation of GPS position and height offsets used to adjust different GPS receivers for steady state position differences\.


+------------+---------+
| Range      | Units   |
+============+=========+
| 5.0 - 30.0 | seconds |
+------------+---------+




.. _GPS_DRV_OPTIONS:

GPS\_DRV\_OPTIONS: driver options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Additional backend specific options


+----------------------------------------------------------------+
| Bitmask                                                        |
+================================================================+
| +-----+------------------------------------------------------+ |
| | Bit | Meaning                                              | |
| +=====+======================================================+ |
| | 0   | Use UART2 for moving baseline on ublox               | |
| +-----+------------------------------------------------------+ |
| | 1   | Use base station for GPS yaw on SBF                  | |
| +-----+------------------------------------------------------+ |
| | 2   | Use baudrate 115200                                  | |
| +-----+------------------------------------------------------+ |
| | 3   | Use dedicated CAN port b/w GPSes for moving baseline | |
| +-----+------------------------------------------------------+ |
|                                                                |
+----------------------------------------------------------------+




.. _GPS_COM_PORT:

GPS\_COM\_PORT: GPS physical COM port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

The physical COM port on the connected device\, currently only applies to SBF GPS


+-----------+--------+
| Increment | Range  |
+===========+========+
| 1         | 0 - 10 |
+-----------+--------+




.. _GPS_COM_PORT2:

GPS\_COM\_PORT2: GPS physical COM port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

The physical COM port on the connected device\, currently only applies to SBF GPS


+-----------+--------+
| Increment | Range  |
+===========+========+
| 1         | 0 - 10 |
+-----------+--------+




.. _GPS_PRIMARY:

GPS\_PRIMARY: Primary GPS
~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This GPS will be used when GPS\_AUTO\_SWITCH is 0 and used preferentially with GPS\_AUTO\_SWITCH \= 4\.


+-----------+-----------------------+
| Increment | Values                |
+===========+=======================+
| 1         | +-------+-----------+ |
|           | | Value | Meaning   | |
|           | +=======+===========+ |
|           | | 0     | FirstGPS  | |
|           | +-------+-----------+ |
|           | | 1     | SecondGPS | |
|           | +-------+-----------+ |
|           |                       |
+-----------+-----------------------+




.. _GPS_CAN_NODEID1:

GPS\_CAN\_NODEID1: GPS Node ID 1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

GPS Node id for discovered first\.


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _GPS_CAN_NODEID2:

GPS\_CAN\_NODEID2: GPS Node ID 2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

GPS Node id for discovered second\.


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _GPS1_CAN_OVRIDE:

GPS1\_CAN\_OVRIDE: First UAVCAN GPS NODE ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

GPS Node id for first GPS\. If 0 the gps will be automatically selected on first come basis\.


.. _GPS2_CAN_OVRIDE:

GPS2\_CAN\_OVRIDE: Second UAVCAN GPS NODE ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

GPS Node id for second GPS\. If 0 the gps will be automatically selected on first come basis\.



.. _parameters_GPS_MB1_:

GPS\_MB1\_ Parameters
---------------------


.. _GPS_MB1_TYPE:

GPS\_MB1\_TYPE: Moving base type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Controls the type of moving base used if using moving base\.


+------------------------------------------------+
| Values                                         |
+================================================+
| +-------+------------------------------------+ |
| | Value | Meaning                            | |
| +=======+====================================+ |
| | 0     | Relative to alternate GPS instance | |
| +-------+------------------------------------+ |
| | 1     | RelativeToCustomBase               | |
| +-------+------------------------------------+ |
|                                                |
+------------------------------------------------+




.. _GPS_MB1_OFS_X:

GPS\_MB1\_OFS\_X: Base antenna X position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the base GPS antenna in body frame\. Positive X is forward of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_MB1_OFS_Y:

GPS\_MB1\_OFS\_Y: Base antenna Y position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the base GPS antenna in body frame\. Positive Y is to the right of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_MB1_OFS_Z:

GPS\_MB1\_OFS\_Z: Base antenna Z position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the base GPS antenna in body frame\. Positive Z is down from the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+





.. _parameters_GPS_MB2_:

GPS\_MB2\_ Parameters
---------------------


.. _GPS_MB2_TYPE:

GPS\_MB2\_TYPE: Moving base type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Controls the type of moving base used if using moving base\.


+------------------------------------------------+
| Values                                         |
+================================================+
| +-------+------------------------------------+ |
| | Value | Meaning                            | |
| +=======+====================================+ |
| | 0     | Relative to alternate GPS instance | |
| +-------+------------------------------------+ |
| | 1     | RelativeToCustomBase               | |
| +-------+------------------------------------+ |
|                                                |
+------------------------------------------------+




.. _GPS_MB2_OFS_X:

GPS\_MB2\_OFS\_X: Base antenna X position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the base GPS antenna in body frame\. Positive X is forward of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_MB2_OFS_Y:

GPS\_MB2\_OFS\_Y: Base antenna Y position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the base GPS antenna in body frame\. Positive Y is to the right of the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _GPS_MB2_OFS_Z:

GPS\_MB2\_OFS\_Z: Base antenna Z position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the base GPS antenna in body frame\. Positive Z is down from the origin\. Use antenna phase centroid location if provided by the manufacturer\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+





.. _parameters_INS_:

INS\_ Parameters
----------------


.. _INS_GYROFFS_X:

INS\_GYROFFS\_X: Gyro offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro sensor offsets of X axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYROFFS_Y:

INS\_GYROFFS\_Y: Gyro offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro sensor offsets of Y axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYROFFS_Z:

INS\_GYROFFS\_Z: Gyro offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro sensor offsets of Z axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR2OFFS_X:

INS\_GYR2OFFS\_X: Gyro2 offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro2 sensor offsets of X axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR2OFFS_Y:

INS\_GYR2OFFS\_Y: Gyro2 offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro2 sensor offsets of Y axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR2OFFS_Z:

INS\_GYR2OFFS\_Z: Gyro2 offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro2 sensor offsets of Z axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR3OFFS_X:

INS\_GYR3OFFS\_X: Gyro3 offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro3 sensor offsets of X axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR3OFFS_Y:

INS\_GYR3OFFS\_Y: Gyro3 offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro3 sensor offsets of Y axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_GYR3OFFS_Z:

INS\_GYR3OFFS\_Z: Gyro3 offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro3 sensor offsets of Z axis\. This is setup on each boot during gyro calibrations


+-------------+--------------------+
| Calibration | Units              |
+=============+====================+
| 1           | radians per second |
+-------------+--------------------+




.. _INS_ACCSCAL_X:

INS\_ACCSCAL\_X: Accelerometer scaling of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer scaling of X axis\.  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACCSCAL_Y:

INS\_ACCSCAL\_Y: Accelerometer scaling of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer scaling of Y axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACCSCAL_Z:

INS\_ACCSCAL\_Z: Accelerometer scaling of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer scaling of Z axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACCOFFS_X:

INS\_ACCOFFS\_X: Accelerometer offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer offsets of X axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACCOFFS_Y:

INS\_ACCOFFS\_Y: Accelerometer offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer offsets of Y axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACCOFFS_Z:

INS\_ACCOFFS\_Z: Accelerometer offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer offsets of Z axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC2SCAL_X:

INS\_ACC2SCAL\_X: Accelerometer2 scaling of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 scaling of X axis\.  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC2SCAL_Y:

INS\_ACC2SCAL\_Y: Accelerometer2 scaling of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 scaling of Y axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC2SCAL_Z:

INS\_ACC2SCAL\_Z: Accelerometer2 scaling of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 scaling of Z axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC2OFFS_X:

INS\_ACC2OFFS\_X: Accelerometer2 offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 offsets of X axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC2OFFS_Y:

INS\_ACC2OFFS\_Y: Accelerometer2 offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 offsets of Y axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC2OFFS_Z:

INS\_ACC2OFFS\_Z: Accelerometer2 offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 offsets of Z axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC3SCAL_X:

INS\_ACC3SCAL\_X: Accelerometer3 scaling of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 scaling of X axis\.  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC3SCAL_Y:

INS\_ACC3SCAL\_Y: Accelerometer3 scaling of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 scaling of Y axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC3SCAL_Z:

INS\_ACC3SCAL\_Z: Accelerometer3 scaling of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 scaling of Z axis  Calculated during acceleration calibration routine


+-------------+-----------+
| Calibration | Range     |
+=============+===========+
| 1           | 0.8 - 1.2 |
+-------------+-----------+




.. _INS_ACC3OFFS_X:

INS\_ACC3OFFS\_X: Accelerometer3 offsets of X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 offsets of X axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC3OFFS_Y:

INS\_ACC3OFFS\_Y: Accelerometer3 offsets of Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 offsets of Y axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_ACC3OFFS_Z:

INS\_ACC3OFFS\_Z: Accelerometer3 offsets of Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 offsets of Z axis\. This is setup using the acceleration calibration or level operations


+-------------+------------+--------------------------+
| Calibration | Range      | Units                    |
+=============+============+==========================+
| 1           | -3.5 - 3.5 | meters per square second |
+-------------+------------+--------------------------+




.. _INS_GYRO_FILTER:

INS\_GYRO\_FILTER: Gyro filter cutoff frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Filter cutoff frequency for gyroscopes\. This can be set to a lower value to try to cope with very high vibration levels in aircraft\. A value of zero means no filtering \(not recommended\!\)


+---------+-------+
| Range   | Units |
+=========+=======+
| 0 - 256 | hertz |
+---------+-------+




.. _INS_ACCEL_FILTER:

INS\_ACCEL\_FILTER: Accel filter cutoff frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Filter cutoff frequency for accelerometers\. This can be set to a lower value to try to cope with very high vibration levels in aircraft\. A value of zero means no filtering \(not recommended\!\)


+---------+-------+
| Range   | Units |
+=========+=======+
| 0 - 256 | hertz |
+---------+-------+




.. _INS_USE:

INS\_USE: Use first IMU for attitude\, velocity and position estimates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Use first IMU for attitude\, velocity and position estimates


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




.. _INS_USE2:

INS\_USE2: Use second IMU for attitude\, velocity and position estimates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Use second IMU for attitude\, velocity and position estimates


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




.. _INS_USE3:

INS\_USE3: Use third IMU for attitude\, velocity and position estimates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Use third IMU for attitude\, velocity and position estimates


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




.. _INS_STILL_THRESH:

INS\_STILL\_THRESH: Stillness threshold for detecting if we are moving
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Threshold to tolerate vibration to determine if vehicle is motionless\. This depends on the frame type and if there is a constant vibration due to motors before launch or after landing\. Total motionless is about 0\.05\. Suggested values\: Planes\/rover use 0\.1\, multirotors use 1\, tradHeli uses 5


+-----------+
| Range     |
+===========+
| 0.05 - 50 |
+-----------+




.. _INS_GYR_CAL:

INS\_GYR\_CAL: Gyro Calibration scheme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Conrols when automatic gyro calibration is performed


+---------------------------+
| Values                    |
+===========================+
| +-------+---------------+ |
| | Value | Meaning       | |
| +=======+===============+ |
| | 0     | Never         | |
| +-------+---------------+ |
| | 1     | Start-up only | |
| +-------+---------------+ |
|                           |
+---------------------------+




.. _INS_TRIM_OPTION:

INS\_TRIM\_OPTION: Accel cal trim option
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Specifies how the accel cal routine determines the trims


+--------------------------------------------------------------------+
| Values                                                             |
+====================================================================+
| +-------+--------------------------------------------------------+ |
| | Value | Meaning                                                | |
| +=======+========================================================+ |
| | 0     | Don't adjust the trims                                 | |
| +-------+--------------------------------------------------------+ |
| | 1     | Assume first orientation was level                     | |
| +-------+--------------------------------------------------------+ |
| | 2     | Assume ACC_BODYFIX is perfectly aligned to the vehicle | |
| +-------+--------------------------------------------------------+ |
|                                                                    |
+--------------------------------------------------------------------+




.. _INS_ACC_BODYFIX:

INS\_ACC\_BODYFIX: Body\-fixed accelerometer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The body\-fixed accelerometer to be used for trim calculation


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | IMU 1   | |
| +-------+---------+ |
| | 2     | IMU 2   | |
| +-------+---------+ |
| | 3     | IMU 3   | |
| +-------+---------+ |
|                     |
+---------------------+




.. _INS_POS1_X:

INS\_POS1\_X: IMU accelerometer X position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the first IMU Accelerometer in body frame\. Positive X is forward of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS1_Y:

INS\_POS1\_Y: IMU accelerometer Y position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the first IMU accelerometer in body frame\. Positive Y is to the right of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS1_Z:

INS\_POS1\_Z: IMU accelerometer Z position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the first IMU accelerometer in body frame\. Positive Z is down from the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS2_X:

INS\_POS2\_X: IMU accelerometer X position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the second IMU accelerometer in body frame\. Positive X is forward of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS2_Y:

INS\_POS2\_Y: IMU accelerometer Y position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the second IMU accelerometer in body frame\. Positive Y is to the right of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS2_Z:

INS\_POS2\_Z: IMU accelerometer Z position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the second IMU accelerometer in body frame\. Positive Z is down from the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS3_X:

INS\_POS3\_X: IMU accelerometer X position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the third IMU accelerometer in body frame\. Positive X is forward of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+----------+--------+
| Range    | Units  |
+==========+========+
| -10 - 10 | meters |
+----------+--------+




.. _INS_POS3_Y:

INS\_POS3\_Y: IMU accelerometer Y position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the third IMU accelerometer in body frame\. Positive Y is to the right of the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_POS3_Z:

INS\_POS3\_Z: IMU accelerometer Z position
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the third IMU accelerometer in body frame\. Positive Z is down from the origin\. Attention\: The IMU should be located as close to the vehicle c\.g\. as practical so that the value of this parameter is minimised\. Failure to do so can result in noisy navigation velocity measurements due to vibration and IMU gyro noise\. If the IMU cannot be moved and velocity noise is a problem\, a location closer to the IMU can be used as the body frame origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _INS_GYR_ID:

INS\_GYR\_ID: Gyro ID
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_GYR2_ID:

INS\_GYR2\_ID: Gyro2 ID
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro2 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_GYR3_ID:

INS\_GYR3\_ID: Gyro3 ID
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Gyro3 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_ACC_ID:

INS\_ACC\_ID: Accelerometer ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_ACC2_ID:

INS\_ACC2\_ID: Accelerometer2 ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer2 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_ACC3_ID:

INS\_ACC3\_ID: Accelerometer3 ID
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Accelerometer3 sensor ID\, taking into account its type\, bus and instance


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _INS_FAST_SAMPLE:

INS\_FAST\_SAMPLE: Fast sampling mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Mask of IMUs to enable fast sampling on\, if available


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | FirstIMU  | |
| +-----+-----------+ |
| | 1   | SecondIMU | |
| +-----+-----------+ |
| | 2   | ThirdIMU  | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _INS_ENABLE_MASK:

INS\_ENABLE\_MASK: IMU enable mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask of IMUs to enable\. It can be used to prevent startup of specific detected IMUs


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | FirstIMU  | |
| +-----+-----------+ |
| | 1   | SecondIMU | |
| +-----+-----------+ |
| | 2   | ThirdIMU  | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _INS_GYRO_RATE:

INS\_GYRO\_RATE: Gyro rate for IMUs with Fast Sampling enabled
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Gyro rate for IMUs with fast sampling enabled\. The gyro rate is the sample rate at which the IMU filters operate and needs to be at least double the maximum filter frequency\. If the sensor does not support the selected rate the next highest supported rate will be used\. For IMUs which do not support fast sampling this setting is ignored and the default gyro rate of 1Khz is used\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | 1kHz    | |
| +-------+---------+ |
| | 1     | 2kHz    | |
| +-------+---------+ |
| | 2     | 4kHz    | |
| +-------+---------+ |
| | 3     | 8kHz    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _INS_ACC1_CALTEMP:

INS\_ACC1\_CALTEMP: Calibration temperature for 1st accelerometer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 1st accelerometer was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_GYR1_CALTEMP:

INS\_GYR1\_CALTEMP: Calibration temperature for 1st gyroscope
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 1st gyroscope was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_ACC2_CALTEMP:

INS\_ACC2\_CALTEMP: Calibration temperature for 2nd accelerometer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 2nd accelerometer was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_GYR2_CALTEMP:

INS\_GYR2\_CALTEMP: Calibration temperature for 2nd gyroscope
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 2nd gyroscope was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_ACC3_CALTEMP:

INS\_ACC3\_CALTEMP: Calibration temperature for 3rd accelerometer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 3rd accelerometer was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_GYR3_CALTEMP:

INS\_GYR3\_CALTEMP: Calibration temperature for 3rd gyroscope
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Temperature that the 3rd gyroscope was calibrated at


+-------------+-----------------+
| Calibration | Units           |
+=============+=================+
| 1           | degrees Celsius |
+-------------+-----------------+




.. _INS_TCAL_OPTIONS:

INS\_TCAL\_OPTIONS: Options for temperature calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This enables optional temperature calibration features\. Setting PersistParams will save the accelerometer and temperature calibration parameters in the bootloader sector on the next update of the bootloader\.


+-------------------------+
| Bitmask                 |
+=========================+
| +-----+---------------+ |
| | Bit | Meaning       | |
| +=====+===============+ |
| | 0   | PersistParams | |
| +-----+---------------+ |
|                         |
+-------------------------+





.. _parameters_INS_HNTCH_:

INS\_HNTCH\_ Parameters
-----------------------


.. _INS_HNTCH_ENABLE:

INS\_HNTCH\_ENABLE: Harmonic Notch Filter enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Harmonic Notch Filter enable


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




.. _INS_HNTCH_FREQ:

INS\_HNTCH\_FREQ: Harmonic Notch Filter base frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Harmonic Notch Filter base center frequency in Hz\. This should be set at most half the backend gyro rate \(which is typically 1Khz\)\. For helicopters using RPM sensor to dynamically set the notch frequency\, use this parameter to provide a lower limit to the dynamic notch filter\.  Recommend setting it to half the operating rotor speed in Hz\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 10 - 495 | hertz |
+----------+-------+




.. _INS_HNTCH_BW:

INS\_HNTCH\_BW: Harmonic Notch Filter bandwidth
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Harmonic Notch Filter bandwidth in Hz\. This is typically set to half the base frequency\. The ratio of base frequency to bandwidth determines the notch quality factor and is fixed across harmonics\.


+---------+-------+
| Range   | Units |
+=========+=======+
| 5 - 250 | hertz |
+---------+-------+




.. _INS_HNTCH_ATT:

INS\_HNTCH\_ATT: Harmonic Notch Filter attenuation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Harmonic Notch Filter attenuation in dB\. Values greater than 40dB will typically produce a hard notch rather than a modest attenuation of motor noise\.


+--------+---------+
| Range  | Units   |
+========+=========+
| 5 - 50 | decibel |
+--------+---------+




.. _INS_HNTCH_HMNCS:

INS\_HNTCH\_HMNCS: Harmonic Notch Filter harmonics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Bitmask of harmonic frequencies to apply Harmonic Notch Filter to\. This option takes effect on the next reboot\. A maximum of 3 harmonics can be used at any one time\.


+------------------------+
| Bitmask                |
+========================+
| +-----+--------------+ |
| | Bit | Meaning      | |
| +=====+==============+ |
| | 0   | 1st harmonic | |
| +-----+--------------+ |
| | 1   | 2nd harmonic | |
| +-----+--------------+ |
| | 2   | 3rd harmonic | |
| +-----+--------------+ |
| | 3   | 4th hamronic | |
| +-----+--------------+ |
| | 4   | 5th harmonic | |
| +-----+--------------+ |
| | 5   | 6th harmonic | |
| +-----+--------------+ |
| | 6   | 7th harmonic | |
| +-----+--------------+ |
| | 7   | 8th harmonic | |
| +-----+--------------+ |
|                        |
+------------------------+




.. _INS_HNTCH_REF:

INS\_HNTCH\_REF: Harmonic Notch Filter reference value
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

A reference value of zero disables dynamic updates on the Harmonic Notch Filter and a positive value enables dynamic updates on the Harmonic Notch Filter\.  For throttle\-based scaling\, this parameter is the reference value associated with the specified frequency to facilitate frequency scaling of the Harmonic Notch Filter\. For RPM and ESC telemetry based tracking\, this parameter is set to 1 to enable the Harmonic Notch Filter using the RPM sensor or ESC telemetry set to measure rotor speed\.  The sensor data is converted to Hz automatically for use in the Harmonic Notch Filter\.  This reference value may also be used to scale the sensor data\, if required\.  For example\, rpm sensor data is required to measure heli motor RPM\. Therefore the reference value can be used to scale the RPM sensor to the rotor RPM\.


+-----------+
| Range     |
+===========+
| 0.0 - 1.0 |
+-----------+




.. _INS_HNTCH_MODE:

INS\_HNTCH\_MODE: Harmonic Notch Filter dynamic frequency tracking mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Harmonic Notch Filter dynamic frequency tracking mode\. Dynamic updates can be throttle\, RPM sensor\, ESC telemetry or dynamic FFT based\. Throttle\-based updates should only be used with multicopters\.


+-------+---------------------------+
| Range | Values                    |
+=======+===========================+
| 0 - 4 | +-------+---------------+ |
|       | | Value | Meaning       | |
|       | +=======+===============+ |
|       | | 0     | Disabled      | |
|       | +-------+---------------+ |
|       | | 1     | Throttle      | |
|       | +-------+---------------+ |
|       | | 2     | RPM Sensor    | |
|       | +-------+---------------+ |
|       | | 3     | ESC Telemetry | |
|       | +-------+---------------+ |
|       | | 4     | Dynamic FFT   | |
|       | +-------+---------------+ |
|       |                           |
+-------+---------------------------+




.. _INS_HNTCH_OPTS:

INS\_HNTCH\_OPTS: Harmonic Notch Filter options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Harmonic Notch Filter options\. Double\-notches can provide deeper attenuation across a wider bandwidth than single notches and are suitable for larger aircraft\. Dynamic harmonics attaches a harmonic notch to each detected noise frequency instead of simply being multiples of the base frequency\, in the case of FFT it will attach notches to each of three detected noise peaks\, in the case of ESC it will attach notches to each of four motor RPM values\. Loop rate update changes the notch center frequency at the scheduler loop rate rather than at the default of 200Hz\.


+-------------------------------+
| Bitmask                       |
+===============================+
| +-----+---------------------+ |
| | Bit | Meaning             | |
| +=====+=====================+ |
| | 0   | Double notch        | |
| +-----+---------------------+ |
| | 1   | Dynamic harmonic    | |
| +-----+---------------------+ |
| | 2   | Update at loop rate | |
| +-----+---------------------+ |
|                               |
+-------------------------------+





.. _parameters_INS_LOG_:

INS\_LOG\_ Parameters
---------------------


.. _INS_LOG_BAT_CNT:

INS\_LOG\_BAT\_CNT: sample count per batch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Number of samples to take when logging streams of IMU sensor readings\.  Will be rounded down to a multiple of 32\. This option takes effect on the next reboot\.


+-----------+
| Increment |
+===========+
| 32        |
+-----------+




.. _INS_LOG_BAT_MASK:

INS\_LOG\_BAT\_MASK: Sensor Bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Bitmap of which IMUs to log batch data for\. This option takes effect on the next reboot\.


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | IMU1    | |
| +-----+---------+ |
| | 1   | IMU2    | |
| +-----+---------+ |
| | 2   | IMU3    | |
| +-----+---------+ |
|                   |
+-------------------+




.. _INS_LOG_BAT_OPT:

INS\_LOG\_BAT\_OPT: Batch Logging Options Mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Options for the BatchSampler\. Post\-filter and sensor\-rate logging cannot be used at the same time\.


+-----------------------------------------------------------------------+
| Bitmask                                                               |
+=======================================================================+
| +-----+-------------------------------------------------------------+ |
| | Bit | Meaning                                                     | |
| +=====+=============================================================+ |
| | 0   | Sensor-Rate Logging (sample at full sensor rate seen by AP) | |
| +-----+-------------------------------------------------------------+ |
| | 1   | Sample post-filtering                                       | |
| +-----+-------------------------------------------------------------+ |
|                                                                       |
+-----------------------------------------------------------------------+




.. _INS_LOG_BAT_LGIN:

INS\_LOG\_BAT\_LGIN: logging interval
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Interval between pushing samples to the AP\_Logger log


+-----------+--------------+
| Increment | Units        |
+===========+==============+
| 10        | milliseconds |
+-----------+--------------+




.. _INS_LOG_BAT_LGCT:

INS\_LOG\_BAT\_LGCT: logging count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of samples to push to count every INS\_LOG\_BAT\_LGIN


+-----------+
| Increment |
+===========+
| 1         |
+-----------+





.. _parameters_INS_NOTCH_:

INS\_NOTCH\_ Parameters
-----------------------


.. _INS_NOTCH_ENABLE:

INS\_NOTCH\_ENABLE: Enable
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable notch filter


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




.. _INS_NOTCH_ATT:

INS\_NOTCH\_ATT: Attenuation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Notch attenuation in dB


+--------+---------+
| Range  | Units   |
+========+=========+
| 5 - 30 | decibel |
+--------+---------+




.. _INS_NOTCH_FREQ:

INS\_NOTCH\_FREQ: Frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Notch center frequency in Hz


+----------+-------+
| Range    | Units |
+==========+=======+
| 10 - 400 | hertz |
+----------+-------+




.. _INS_NOTCH_BW:

INS\_NOTCH\_BW: Bandwidth
~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Notch bandwidth in Hz


+---------+-------+
| Range   | Units |
+=========+=======+
| 5 - 100 | hertz |
+---------+-------+





.. _parameters_INS_TCAL1_:

INS\_TCAL1\_ Parameters
-----------------------


.. _INS_TCAL1_ENABLE:

INS\_TCAL1\_ENABLE: Enable temperature calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable the use of temperature calibration parameters for this IMU\. For automatic learning set to 2 and also set the INS\_TCALn\_TMAX to the target temperature\, then reboot


+------------------------------+
| Values                       |
+==============================+
| +-------+------------------+ |
| | Value | Meaning          | |
| +=======+==================+ |
| | 0     | Disabled         | |
| +-------+------------------+ |
| | 1     | Enabled          | |
| +-------+------------------+ |
| | 2     | LearnCalibration | |
| +-------+------------------+ |
|                              |
+------------------------------+




.. _INS_TCAL1_TMIN:

INS\_TCAL1\_TMIN: Temperature calibration min
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The minimum temperature that the calibration is valid for


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL1_TMAX:

INS\_TCAL1\_TMAX: Temperature calibration max
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The maximum temperature that the calibration is valid for\. This must be at least 10 degrees above TMIN for calibration


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL1_ACC1_X:

INS\_TCAL1\_ACC1\_X: Accelerometer 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC1_Y:

INS\_TCAL1\_ACC1\_Y: Accelerometer 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC1_Z:

INS\_TCAL1\_ACC1\_Z: Accelerometer 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC2_X:

INS\_TCAL1\_ACC2\_X: Accelerometer 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC2_Y:

INS\_TCAL1\_ACC2\_Y: Accelerometer 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC2_Z:

INS\_TCAL1\_ACC2\_Z: Accelerometer 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC3_X:

INS\_TCAL1\_ACC3\_X: Accelerometer 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC3_Y:

INS\_TCAL1\_ACC3\_Y: Accelerometer 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_ACC3_Z:

INS\_TCAL1\_ACC3\_Z: Accelerometer 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR1_X:

INS\_TCAL1\_GYR1\_X: Gyroscope 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR1_Y:

INS\_TCAL1\_GYR1\_Y: Gyroscope 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR1_Z:

INS\_TCAL1\_GYR1\_Z: Gyroscope 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR2_X:

INS\_TCAL1\_GYR2\_X: Gyroscope 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR2_Y:

INS\_TCAL1\_GYR2\_Y: Gyroscope 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR2_Z:

INS\_TCAL1\_GYR2\_Z: Gyroscope 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR3_X:

INS\_TCAL1\_GYR3\_X: Gyroscope 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR3_Y:

INS\_TCAL1\_GYR3\_Y: Gyroscope 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL1_GYR3_Z:

INS\_TCAL1\_GYR3\_Z: Gyroscope 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+





.. _parameters_INS_TCAL2_:

INS\_TCAL2\_ Parameters
-----------------------


.. _INS_TCAL2_ENABLE:

INS\_TCAL2\_ENABLE: Enable temperature calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable the use of temperature calibration parameters for this IMU\. For automatic learning set to 2 and also set the INS\_TCALn\_TMAX to the target temperature\, then reboot


+------------------------------+
| Values                       |
+==============================+
| +-------+------------------+ |
| | Value | Meaning          | |
| +=======+==================+ |
| | 0     | Disabled         | |
| +-------+------------------+ |
| | 1     | Enabled          | |
| +-------+------------------+ |
| | 2     | LearnCalibration | |
| +-------+------------------+ |
|                              |
+------------------------------+




.. _INS_TCAL2_TMIN:

INS\_TCAL2\_TMIN: Temperature calibration min
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The minimum temperature that the calibration is valid for


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL2_TMAX:

INS\_TCAL2\_TMAX: Temperature calibration max
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The maximum temperature that the calibration is valid for\. This must be at least 10 degrees above TMIN for calibration


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL2_ACC1_X:

INS\_TCAL2\_ACC1\_X: Accelerometer 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC1_Y:

INS\_TCAL2\_ACC1\_Y: Accelerometer 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC1_Z:

INS\_TCAL2\_ACC1\_Z: Accelerometer 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC2_X:

INS\_TCAL2\_ACC2\_X: Accelerometer 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC2_Y:

INS\_TCAL2\_ACC2\_Y: Accelerometer 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC2_Z:

INS\_TCAL2\_ACC2\_Z: Accelerometer 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC3_X:

INS\_TCAL2\_ACC3\_X: Accelerometer 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC3_Y:

INS\_TCAL2\_ACC3\_Y: Accelerometer 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_ACC3_Z:

INS\_TCAL2\_ACC3\_Z: Accelerometer 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR1_X:

INS\_TCAL2\_GYR1\_X: Gyroscope 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR1_Y:

INS\_TCAL2\_GYR1\_Y: Gyroscope 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR1_Z:

INS\_TCAL2\_GYR1\_Z: Gyroscope 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR2_X:

INS\_TCAL2\_GYR2\_X: Gyroscope 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR2_Y:

INS\_TCAL2\_GYR2\_Y: Gyroscope 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR2_Z:

INS\_TCAL2\_GYR2\_Z: Gyroscope 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR3_X:

INS\_TCAL2\_GYR3\_X: Gyroscope 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR3_Y:

INS\_TCAL2\_GYR3\_Y: Gyroscope 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL2_GYR3_Z:

INS\_TCAL2\_GYR3\_Z: Gyroscope 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+





.. _parameters_INS_TCAL3_:

INS\_TCAL3\_ Parameters
-----------------------


.. _INS_TCAL3_ENABLE:

INS\_TCAL3\_ENABLE: Enable temperature calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Enable the use of temperature calibration parameters for this IMU\. For automatic learning set to 2 and also set the INS\_TCALn\_TMAX to the target temperature\, then reboot


+------------------------------+
| Values                       |
+==============================+
| +-------+------------------+ |
| | Value | Meaning          | |
| +=======+==================+ |
| | 0     | Disabled         | |
| +-------+------------------+ |
| | 1     | Enabled          | |
| +-------+------------------+ |
| | 2     | LearnCalibration | |
| +-------+------------------+ |
|                              |
+------------------------------+




.. _INS_TCAL3_TMIN:

INS\_TCAL3\_TMIN: Temperature calibration min
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The minimum temperature that the calibration is valid for


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL3_TMAX:

INS\_TCAL3\_TMAX: Temperature calibration max
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The maximum temperature that the calibration is valid for\. This must be at least 10 degrees above TMIN for calibration


+-------------+----------+-----------------+
| Calibration | Range    | Units           |
+=============+==========+=================+
| 1           | -70 - 80 | degrees Celsius |
+-------------+----------+-----------------+




.. _INS_TCAL3_ACC1_X:

INS\_TCAL3\_ACC1\_X: Accelerometer 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC1_Y:

INS\_TCAL3\_ACC1\_Y: Accelerometer 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC1_Z:

INS\_TCAL3\_ACC1\_Z: Accelerometer 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC2_X:

INS\_TCAL3\_ACC2\_X: Accelerometer 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC2_Y:

INS\_TCAL3\_ACC2\_Y: Accelerometer 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC2_Z:

INS\_TCAL3\_ACC2\_Z: Accelerometer 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC3_X:

INS\_TCAL3\_ACC3\_X: Accelerometer 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC3_Y:

INS\_TCAL3\_ACC3\_Y: Accelerometer 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_ACC3_Z:

INS\_TCAL3\_ACC3\_Z: Accelerometer 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR1_X:

INS\_TCAL3\_GYR1\_X: Gyroscope 1st order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR1_Y:

INS\_TCAL3\_GYR1\_Y: Gyroscope 1st order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR1_Z:

INS\_TCAL3\_GYR1\_Z: Gyroscope 1st order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 1st order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR2_X:

INS\_TCAL3\_GYR2\_X: Gyroscope 2nd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR2_Y:

INS\_TCAL3\_GYR2\_Y: Gyroscope 2nd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR2_Z:

INS\_TCAL3\_GYR2\_Z: Gyroscope 2nd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 2nd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR3_X:

INS\_TCAL3\_GYR3\_X: Gyroscope 3rd order temperature coefficient X axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR3_Y:

INS\_TCAL3\_GYR3\_Y: Gyroscope 3rd order temperature coefficient Y axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+




.. _INS_TCAL3_GYR3_Z:

INS\_TCAL3\_GYR3\_Z: Gyroscope 3rd order temperature coefficient Z axis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This is the 3rd order temperature coefficient from a temperature calibration


+-------------+
| Calibration |
+=============+
| 1           |
+-------------+





.. _parameters_LOG:

LOG Parameters
--------------


.. _LOG_BACKEND_TYPE:

LOG\_BACKEND\_TYPE: AP\_Logger Backend Storage type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Bitmap of what Logger backend types to enable\. Block\-based logging is available on SITL and boards with dataflash chips\. Multiple backends can be selected\.


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | File    | |
| +-----+---------+ |
| | 1   | MAVLink | |
| +-----+---------+ |
| | 2   | Block   | |
| +-----+---------+ |
|                   |
+-------------------+




.. _LOG_FILE_BUFSIZE:

LOG\_FILE\_BUFSIZE: Maximum AP\_Logger File and Block Backend buffer size \(in kilobytes\)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The File and Block backends use a buffer to store data before writing to the block device\.  Raising this value may reduce \"gaps\" in your SD card logging\.  This buffer size may be reduced depending on available memory\.  PixHawk requires at least 4 kilobytes\.  Maximum value available here is 64 kilobytes\.


.. _LOG_DISARMED:

LOG\_DISARMED: Enable logging while disarmed
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


If LOG\_DISARMED is set to 1 then logging will be enabled while disarmed\. This can make for very large logfiles but can help a lot when tracking down startup issues


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




.. _LOG_REPLAY:

LOG\_REPLAY: Enable logging of information needed for Replay
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


If LOG\_REPLAY is set to 1 then the EKF2 state estimator will log detailed information needed for diagnosing problems with the Kalman filter\. It is suggested that you also raise LOG\_FILE\_BUFSIZE to give more buffer space for logging and use a high quality microSD card to ensure no sensor data is lost


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




.. _LOG_FILE_DSRMROT:

LOG\_FILE\_DSRMROT: Stop logging to current file on disarm
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


When set\, the current log file is closed when the vehicle is disarmed\.  If LOG\_DISARMED is set then a fresh log will be opened\. Applies to the File and Block logging backends\.


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




.. _LOG_MAV_BUFSIZE:

LOG\_MAV\_BUFSIZE: Maximum AP\_Logger MAVLink Backend buffer size
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Maximum amount of memory to allocate to AP\_Logger\-over\-mavlink


+-----------+
| Units     |
+===========+
| kilobytes |
+-----------+




.. _LOG_FILE_TIMEOUT:

LOG\_FILE\_TIMEOUT: Timeout before giving up on file writes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This controls the amount of time before failing writes to a log file cause the file to be closed and logging stopped\.


+---------+
| Units   |
+=========+
| seconds |
+---------+




.. _LOG_FILE_MB_FREE:

LOG\_FILE\_MB\_FREE: Old logs on the SD card will be deleted to maintain this amount of free space
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Set this such that the free space is larger than your largest typical flight log


+-----------+----------+
| Range     | Units    |
+===========+==========+
| 10 - 1000 | megabyte |
+-----------+----------+




.. _LOG_FILE_RATEMAX:

LOG\_FILE\_RATEMAX: Maximum logging rate for file backend
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the maximum rate that streaming log messages will be logged to the file backend\. A value of zero means


+----------+-------+
| Range    | Units |
+==========+=======+
| 0 - 1000 | hertz |
+----------+-------+




.. _LOG_MAV_RATEMAX:

LOG\_MAV\_RATEMAX: Maximum logging rate for mavlink backend
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the maximum rate that streaming log messages will be logged to the mavlink backend\. A value of zero means


+----------+-------+
| Range    | Units |
+==========+=======+
| 0 - 1000 | hertz |
+----------+-------+




.. _LOG_BLK_RATEMAX:

LOG\_BLK\_RATEMAX: Maximum logging rate for block backend
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the maximum rate that streaming log messages will be logged to the mavlink backend\. A value of zero means


+----------+-------+
| Range    | Units |
+==========+=======+
| 0 - 1000 | hertz |
+----------+-------+





.. _parameters_MSP:

MSP Parameters
--------------


.. _MSP_OSD_NCELLS:

MSP\_OSD\_NCELLS: Cell count override
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Used for average cell voltage calculation


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Auto    | |
| +-------+---------+ |
| | 1     | 1       | |
| +-------+---------+ |
| | 2     | 2       | |
| +-------+---------+ |
| | 3     | 3       | |
| +-------+---------+ |
| | 4     | 4       | |
| +-------+---------+ |
| | 5     | 5       | |
| +-------+---------+ |
| | 6     | 6       | |
| +-------+---------+ |
| | 7     | 7       | |
| +-------+---------+ |
| | 8     | 8       | |
| +-------+---------+ |
| | 9     | 9       | |
| +-------+---------+ |
| | 10    | 10      | |
| +-------+---------+ |
| | 11    | 11      | |
| +-------+---------+ |
| | 12    | 12      | |
| +-------+---------+ |
| | 13    | 13      | |
| +-------+---------+ |
| | 14    | 14      | |
| +-------+---------+ |
|                     |
+---------------------+




.. _MSP_OPTIONS:

MSP\_OPTIONS: MSP OSD Options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


A bitmask to set some MSP specific options


+---------------------------------+
| Bitmask                         |
+=================================+
| +-----+-----------------------+ |
| | Bit | Meaning               | |
| +=====+=======================+ |
| | 0   | EnableTelemetryMode   | |
| +-----+-----------------------+ |
| | 1   | DisableDJIWorkarounds | |
| +-----+-----------------------+ |
| | 2   | EnableBTFLFonts       | |
| +-----+-----------------------+ |
|                                 |
+---------------------------------+





.. _parameters_NTF_:

NTF\_ Parameters
----------------


.. _NTF_LED_BRIGHT:

NTF\_LED\_BRIGHT: LED Brightness
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Select the RGB LED brightness level\. When USB is connected brightness will never be higher than low regardless of the setting\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Off     | |
| +-------+---------+ |
| | 1     | Low     | |
| +-------+---------+ |
| | 2     | Medium  | |
| +-------+---------+ |
| | 3     | High    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _NTF_BUZZ_TYPES:

NTF\_BUZZ\_TYPES: Buzzer Driver Types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls what types of Buzzer will be enabled


+---------------------------+
| Bitmask                   |
+===========================+
| +-----+-----------------+ |
| | Bit | Meaning         | |
| +=====+=================+ |
| | 0   | Built-in buzzer | |
| +-----+-----------------+ |
| | 1   | DShot           | |
| +-----+-----------------+ |
| | 2   | UAVCAN          | |
| +-----+-----------------+ |
|                           |
+---------------------------+




.. _NTF_LED_OVERRIDE:

NTF\_LED\_OVERRIDE: Specifies colour source for the RGBLed
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Specifies the source for the colours and brightness for the LED\.  OutbackChallenge conforms to the MedicalExpress \(https\:\/\/uavchallenge\.org\/medical\-express\/\) rules\, essentially \"Green\" is disarmed \(safe\-to\-approach\)\, \"Red\" is armed \(not safe\-to\-approach\)\. Traffic light is a simplified color set\, red when armed\, yellow when the safety switch is not surpressing outputs \(but disarmed\)\, and green when outputs are surpressed and disarmed\, the LED will blink faster if disarmed and failing arming checks\.


+-----------------------------------------+
| Values                                  |
+=========================================+
| +-------+-----------------------------+ |
| | Value | Meaning                     | |
| +=======+=============================+ |
| | 0     | Standard                    | |
| +-------+-----------------------------+ |
| | 1     | MAVLink/Scripting/AP_Periph | |
| +-------+-----------------------------+ |
| | 2     | OutbackChallenge            | |
| +-------+-----------------------------+ |
| | 3     | TrafficLight                | |
| +-------+-----------------------------+ |
|                                         |
+-----------------------------------------+




.. _NTF_DISPLAY_TYPE:

NTF\_DISPLAY\_TYPE: Type of on\-board I2C display
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets up the type of on\-board I2C display\. Disabled by default\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Disable | |
| +-------+---------+ |
| | 1     | ssd1306 | |
| +-------+---------+ |
| | 2     | sh1106  | |
| +-------+---------+ |
| | 10    | SITL    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _NTF_OREO_THEME:

NTF\_OREO\_THEME: OreoLED Theme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable\/Disable Solo Oreo LED driver\, 0 to disable\, 1 for Aircraft theme\, 2 for Rover theme


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
| | 1     | Aircraft | |
| +-------+----------+ |
| | 2     | Rover    | |
| +-------+----------+ |
|                      |
+----------------------+




.. _NTF_BUZZ_PIN:

NTF\_BUZZ\_PIN: Buzzer pin
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enables to connect active buzzer to arbitrary pin\. Requires 3\-pin buzzer or additional MOSFET\!


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Disabled | |
| +-------+----------+ |
|                      |
+----------------------+




.. _NTF_LED_TYPES:

NTF\_LED\_TYPES: LED Driver Types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Controls what types of LEDs will be enabled


+-------------------------------+
| Bitmask                       |
+===============================+
| +-----+---------------------+ |
| | Bit | Meaning             | |
| +=====+=====================+ |
| | 0   | Built-in LED        | |
| +-----+---------------------+ |
| | 1   | Internal ToshibaLED | |
| +-----+---------------------+ |
| | 2   | External ToshibaLED | |
| +-----+---------------------+ |
| | 3   | External PCA9685    | |
| +-----+---------------------+ |
| | 4   | Oreo LED            | |
| +-----+---------------------+ |
| | 5   | UAVCAN              | |
| +-----+---------------------+ |
| | 6   | NCP5623 External    | |
| +-----+---------------------+ |
| | 7   | NCP5623 Internal    | |
| +-----+---------------------+ |
| | 8   | NeoPixel            | |
| +-----+---------------------+ |
| | 9   | ProfiLED            | |
| +-----+---------------------+ |
| | 10  | Scripting           | |
| +-----+---------------------+ |
| | 11  | DShot               | |
| +-----+---------------------+ |
| | 12  | ProfiLED_SPI        | |
| +-----+---------------------+ |
|                               |
+-------------------------------+




.. _NTF_BUZZ_ON_LVL:

NTF\_BUZZ\_ON\_LVL: Buzzer\-on pin logic level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Specifies pin level that indicates buzzer should play


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | LowIsOn  | |
| +-------+----------+ |
| | 1     | HighIsOn | |
| +-------+----------+ |
|                      |
+----------------------+




.. _NTF_BUZZ_VOLUME:

NTF\_BUZZ\_VOLUME: Buzzer volume
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Control the volume of the buzzer


+---------+---------+
| Range   | Units   |
+=========+=========+
| 0 - 100 | percent |
+---------+---------+




.. _NTF_LED_LEN:

NTF\_LED\_LEN: Serial LED String Length
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

The number of Serial LED\'s to use for notifications \(NeoPixel\'s and ProfiLED\)


+--------+
| Range  |
+========+
| 1 - 32 |
+--------+





.. _parameters_RC:

RC Parameters
-------------


.. _RC_OVERRIDE_TIME:

RC\_OVERRIDE\_TIME: RC override timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Timeout after which RC overrides will no longer be used\, and RC input will resume\, 0 will disable RC overrides\, \-1 will never timeout\, and continue using overrides until they are disabled


+-------------+---------+
| Range       | Units   |
+=============+=========+
| 0.0 - 120.0 | seconds |
+-------------+---------+




.. _RC_OPTIONS:

RC\_OPTIONS: RC options
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC input options


+------------------------------------------------------------------------------+
| Bitmask                                                                      |
+==============================================================================+
| +-----+--------------------------------------------------------------------+ |
| | Bit | Meaning                                                            | |
| +=====+====================================================================+ |
| | 0   | Ignore RC Receiver                                                 | |
| +-----+--------------------------------------------------------------------+ |
| | 1   | Ignore MAVLink Overrides                                           | |
| +-----+--------------------------------------------------------------------+ |
| | 2   | Ignore Receiver Failsafe bit but allow other RC failsafes if setup | |
| +-----+--------------------------------------------------------------------+ |
| | 3   | FPort Pad                                                          | |
| +-----+--------------------------------------------------------------------+ |
| | 4   | Log RC input bytes                                                 | |
| +-----+--------------------------------------------------------------------+ |
| | 5   | Arming check throttle for 0 input                                  | |
| +-----+--------------------------------------------------------------------+ |
| | 6   | Skip the arming check for neutral Roll/Pitch/Yaw sticks            | |
| +-----+--------------------------------------------------------------------+ |
| | 7   | Allow Switch reverse                                               | |
| +-----+--------------------------------------------------------------------+ |
| | 8   | Use passthrough for CRSF telemetry                                 | |
| +-----+--------------------------------------------------------------------+ |
| | 9   | Suppress CRSF mode/rate message for ELRS systems                   | |
| +-----+--------------------------------------------------------------------+ |
| | 10  | Enable multiple receiver support                                   | |
| +-----+--------------------------------------------------------------------+ |
|                                                                              |
+------------------------------------------------------------------------------+




.. _RC_PROTOCOLS:

RC\_PROTOCOLS: RC protocols enabled
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Bitmask of enabled RC protocols\. Allows narrowing the protocol detection to only specific types of RC receivers which can avoid issues with incorrect detection\. Set to 1 to enable all protocols\.


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | All      | |
| +-----+----------+ |
| | 1   | PPM      | |
| +-----+----------+ |
| | 2   | IBUS     | |
| +-----+----------+ |
| | 3   | SBUS     | |
| +-----+----------+ |
| | 4   | SBUS_NI  | |
| +-----+----------+ |
| | 5   | DSM      | |
| +-----+----------+ |
| | 6   | SUMD     | |
| +-----+----------+ |
| | 7   | SRXL     | |
| +-----+----------+ |
| | 8   | SRXL2    | |
| +-----+----------+ |
| | 9   | CRSF     | |
| +-----+----------+ |
| | 10  | ST24     | |
| +-----+----------+ |
| | 11  | FPORT    | |
| +-----+----------+ |
| | 12  | FPORT2   | |
| +-----+----------+ |
| | 13  | FastSBUS | |
| +-----+----------+ |
|                    |
+--------------------+





.. _parameters_RC10_:

RC10\_ Parameters
-----------------


.. _RC10_MIN:

RC10\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC10_TRIM:

RC10\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC10_MAX:

RC10\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC10_REVERSED:

RC10\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC10_DZ:

RC10\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC11_:

RC11\_ Parameters
-----------------


.. _RC11_MIN:

RC11\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC11_TRIM:

RC11\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC11_MAX:

RC11\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC11_REVERSED:

RC11\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC11_DZ:

RC11\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC12_:

RC12\_ Parameters
-----------------


.. _RC12_MIN:

RC12\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC12_TRIM:

RC12\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC12_MAX:

RC12\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC12_REVERSED:

RC12\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC12_DZ:

RC12\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC13_:

RC13\_ Parameters
-----------------


.. _RC13_MIN:

RC13\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC13_TRIM:

RC13\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC13_MAX:

RC13\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC13_REVERSED:

RC13\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC13_DZ:

RC13\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC14_:

RC14\_ Parameters
-----------------


.. _RC14_MIN:

RC14\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC14_TRIM:

RC14\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC14_MAX:

RC14\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC14_REVERSED:

RC14\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC14_DZ:

RC14\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC15_:

RC15\_ Parameters
-----------------


.. _RC15_MIN:

RC15\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC15_TRIM:

RC15\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC15_MAX:

RC15\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC15_REVERSED:

RC15\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC15_DZ:

RC15\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC16_:

RC16\_ Parameters
-----------------


.. _RC16_MIN:

RC16\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC16_TRIM:

RC16\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC16_MAX:

RC16\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC16_REVERSED:

RC16\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC16_DZ:

RC16\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC1_:

RC1\_ Parameters
----------------


.. _RC1_MIN:

RC1\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC1_TRIM:

RC1\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC1_MAX:

RC1\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC1_REVERSED:

RC1\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC1_DZ:

RC1\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC2_:

RC2\_ Parameters
----------------


.. _RC2_MIN:

RC2\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC2_TRIM:

RC2\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC2_MAX:

RC2\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC2_REVERSED:

RC2\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC2_DZ:

RC2\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC3_:

RC3\_ Parameters
----------------


.. _RC3_MIN:

RC3\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC3_TRIM:

RC3\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC3_MAX:

RC3\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC3_REVERSED:

RC3\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC3_DZ:

RC3\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC4_:

RC4\_ Parameters
----------------


.. _RC4_MIN:

RC4\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC4_TRIM:

RC4\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC4_MAX:

RC4\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC4_REVERSED:

RC4\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC4_DZ:

RC4\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC5_:

RC5\_ Parameters
----------------


.. _RC5_MIN:

RC5\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC5_TRIM:

RC5\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC5_MAX:

RC5\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC5_REVERSED:

RC5\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC5_DZ:

RC5\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC6_:

RC6\_ Parameters
----------------


.. _RC6_MIN:

RC6\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC6_TRIM:

RC6\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC6_MAX:

RC6\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC6_REVERSED:

RC6\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC6_DZ:

RC6\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC7_:

RC7\_ Parameters
----------------


.. _RC7_MIN:

RC7\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC7_TRIM:

RC7\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC7_MAX:

RC7\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC7_REVERSED:

RC7\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC7_DZ:

RC7\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC8_:

RC8\_ Parameters
----------------


.. _RC8_MIN:

RC8\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC8_TRIM:

RC8\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC8_MAX:

RC8\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC8_REVERSED:

RC8\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC8_DZ:

RC8\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_RC9_:

RC9\_ Parameters
----------------


.. _RC9_MIN:

RC9\_MIN: RC min PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC9_TRIM:

RC9\_TRIM: RC trim PWM
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC trim \(neutral\) PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC9_MAX:

RC9\_MAX: RC max PWM
~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _RC9_REVERSED:

RC9\_REVERSED: RC reversed
~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Reverse channel input\. Set to 0 for normal operation\. Set to 1 to reverse this input channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _RC9_DZ:

RC9\_DZ: RC dead\-zone
~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

PWM dead zone in microseconds around trim or bottom


+---------+---------------------+
| Range   | Units               |
+=========+=====================+
| 0 - 200 | PWM in microseconds |
+---------+---------------------+





.. _parameters_SCHED_:

SCHED\_ Parameters
------------------


.. _SCHED_DEBUG:

SCHED\_DEBUG: Scheduler debug level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Set to non\-zero to enable scheduler debug messages\. When set to show \"Slips\" the scheduler will display a message whenever a scheduled task is delayed due to too much CPU load\. When set to ShowOverruns the scheduled will display a message whenever a task takes longer than the limit promised in the task table\.


+--------------------------+
| Values                   |
+==========================+
| +-------+--------------+ |
| | Value | Meaning      | |
| +=======+==============+ |
| | 0     | Disabled     | |
| +-------+--------------+ |
| | 2     | ShowSlips    | |
| +-------+--------------+ |
| | 3     | ShowOverruns | |
| +-------+--------------+ |
|                          |
+--------------------------+




.. _SCHED_LOOP_RATE:

SCHED\_LOOP\_RATE: Scheduling main loop rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This controls the rate of the main control loop in Hz\. This should only be changed by developers\. This only takes effect on restart\. Values over 400 are considered highly experimental\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 50    | 50Hz    | |
| +-------+---------+ |
| | 100   | 100Hz   | |
| +-------+---------+ |
| | 200   | 200Hz   | |
| +-------+---------+ |
| | 250   | 250Hz   | |
| +-------+---------+ |
| | 300   | 300Hz   | |
| +-------+---------+ |
| | 400   | 400Hz   | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SCHED_OPTIONS:

SCHED\_OPTIONS: Scheduling options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This controls optional aspects of the scheduler\.


+-------------------------------------+
| Bitmask                             |
+=====================================+
| +-----+---------------------------+ |
| | Bit | Meaning                   | |
| +=====+===========================+ |
| | 0   | Enable per-task perf info | |
| +-----+---------------------------+ |
|                                     |
+-------------------------------------+





.. _parameters_SCR_:

SCR\_ Parameters
----------------


.. _SCR_ENABLE:

SCR\_ENABLE: Enable Scripting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Controls if scripting is enabled


+-------------------------+
| Values                  |
+=========================+
| +-------+-------------+ |
| | Value | Meaning     | |
| +=======+=============+ |
| | 0     | None        | |
| +-------+-------------+ |
| | 1     | Lua Scripts | |
| +-------+-------------+ |
|                         |
+-------------------------+




.. _SCR_VM_I_COUNT:

SCR\_VM\_I\_COUNT: Scripting Virtual Machine Instruction Count
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

The number virtual machine instructions that can be run before considering a script to have taken an excessive amount of time


+-----------+----------------+
| Increment | Range          |
+===========+================+
| 10000     | 1000 - 1000000 |
+-----------+----------------+




.. _SCR_HEAP_SIZE:

SCR\_HEAP\_SIZE: Scripting Heap Size
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Amount of memory available for scripting


+-----------+----------------+
| Increment | Range          |
+===========+================+
| 1024      | 1024 - 1048576 |
+-----------+----------------+




.. _SCR_DEBUG_OPTS:

SCR\_DEBUG\_OPTS: Scripting Debug Level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Debugging options


+-----------------------------------------------------------------+
| Bitmask                                                         |
+=================================================================+
| +-----+-------------------------------------------------------+ |
| | Bit | Meaning                                               | |
| +=====+=======================================================+ |
| | 0   | No Scripts to run message if all scripts have stopped | |
| +-----+-------------------------------------------------------+ |
| | 1   | Runtime messages for memory usage and execution time  | |
| +-----+-------------------------------------------------------+ |
| | 2   | Suppress logging scripts to dataflash                 | |
| +-----+-------------------------------------------------------+ |
| | 3   | log runtime memory usage and execution time           | |
| +-----+-------------------------------------------------------+ |
|                                                                 |
+-----------------------------------------------------------------+




.. _SCR_USER1:

SCR\_USER1: Scripting User Parameter1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_USER2:

SCR\_USER2: Scripting User Parameter2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_USER3:

SCR\_USER3: Scripting User Parameter3
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_USER4:

SCR\_USER4: Scripting User Parameter4
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_USER5:

SCR\_USER5: Scripting User Parameter5
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_USER6:

SCR\_USER6: Scripting User Parameter6
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


General purpose user variable input for scripts


.. _SCR_DIR_DISABLE:

SCR\_DIR\_DISABLE: Directory disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This will stop scripts being loaded from the given locations


+-----------------------+
| Bitmask               |
+=======================+
| +-----+-------------+ |
| | Bit | Meaning     | |
| +=====+=============+ |
| | 0   | ROMFS       | |
| +-----+-------------+ |
| | 1   | APM/scripts | |
| +-----+-------------+ |
|                       |
+-----------------------+





.. _parameters_SERIAL:

SERIAL Parameters
-----------------


.. _SERIAL0_BAUD:

SERIAL0\_BAUD: Serial0 baud rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used on the USB console\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL0_PROTOCOL:

SERIAL0\_PROTOCOL: Console protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol to use on the console\. 


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 1     | MAVlink1 | |
| +-------+----------+ |
| | 2     | MAVLink2 | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERIAL1_PROTOCOL:

SERIAL1\_PROTOCOL: Telem1 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol to use on the Telem1 port\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL1_BAUD:

SERIAL1\_BAUD: Telem1 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used on the Telem1 port\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL2_PROTOCOL:

SERIAL2\_PROTOCOL: Telemetry 2 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol to use on the Telem2 port\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL2_BAUD:

SERIAL2\_BAUD: Telemetry 2 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate of the Telem2 port\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL3_PROTOCOL:

SERIAL3\_PROTOCOL: Serial 3 \(GPS\) protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial 3 \(GPS\) should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL3_BAUD:

SERIAL3\_BAUD: Serial 3 \(GPS\) Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for the Serial 3 \(GPS\)\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL4_PROTOCOL:

SERIAL4\_PROTOCOL: Serial4 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial4 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL4_BAUD:

SERIAL4\_BAUD: Serial 4 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial4\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL5_PROTOCOL:

SERIAL5\_PROTOCOL: Serial5 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial5 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL5_BAUD:

SERIAL5\_BAUD: Serial 5 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial5\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL6_PROTOCOL:

SERIAL6\_PROTOCOL: Serial6 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial6 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL6_BAUD:

SERIAL6\_BAUD: Serial 6 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial6\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL1_OPTIONS:

SERIAL1\_OPTIONS: Telem1 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\. The Swap option allows the RX and TX pins to be swapped on STM32F7 based boards\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL2_OPTIONS:

SERIAL2\_OPTIONS: Telem2 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL3_OPTIONS:

SERIAL3\_OPTIONS: Serial3 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL4_OPTIONS:

SERIAL4\_OPTIONS: Serial4 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL5_OPTIONS:

SERIAL5\_OPTIONS: Serial5 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL6_OPTIONS:

SERIAL6\_OPTIONS: Serial6 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL_PASS1:

SERIAL\_PASS1: Serial passthru first port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets one side of pass\-through between two serial ports\. Once both sides are set then all data received on either port will be passed to the other port


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | -1    | Disabled | |
| +-------+----------+ |
| | 0     | Serial0  | |
| +-------+----------+ |
| | 1     | Serial1  | |
| +-------+----------+ |
| | 2     | Serial2  | |
| +-------+----------+ |
| | 3     | Serial3  | |
| +-------+----------+ |
| | 4     | Serial4  | |
| +-------+----------+ |
| | 5     | Serial5  | |
| +-------+----------+ |
| | 6     | Serial6  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERIAL_PASS2:

SERIAL\_PASS2: Serial passthru second port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets one side of pass\-through between two serial ports\. Once both sides are set then all data received on either port will be passed to the other port


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | -1    | Disabled | |
| +-------+----------+ |
| | 0     | Serial0  | |
| +-------+----------+ |
| | 1     | Serial1  | |
| +-------+----------+ |
| | 2     | Serial2  | |
| +-------+----------+ |
| | 3     | Serial3  | |
| +-------+----------+ |
| | 4     | Serial4  | |
| +-------+----------+ |
| | 5     | Serial5  | |
| +-------+----------+ |
| | 6     | Serial6  | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERIAL_PASSTIMO:

SERIAL\_PASSTIMO: Serial passthru timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets a timeout for serial pass\-through in seconds\. When the pass\-through is enabled by setting the SERIAL\_PASS1 and SERIAL\_PASS2 parameters then it remains in effect until no data comes from the first port for SERIAL\_PASSTIMO seconds\. This allows the port to revent to its normal usage \(such as MAVLink connection to a GCS\) when it is no longer needed\. A value of 0 means no timeout\.


+---------+---------+
| Range   | Units   |
+=========+=========+
| 0 - 120 | seconds |
+---------+---------+




.. _SERIAL7_PROTOCOL:

SERIAL7\_PROTOCOL: Serial7 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial7 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL7_BAUD:

SERIAL7\_BAUD: Serial 7 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial7\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL7_OPTIONS:

SERIAL7\_OPTIONS: Serial7 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL8_PROTOCOL:

SERIAL8\_PROTOCOL: Serial8 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial8 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL8_BAUD:

SERIAL8\_BAUD: Serial 8 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial8\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL8_OPTIONS:

SERIAL8\_OPTIONS: Serial8 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+




.. _SERIAL9_PROTOCOL:

SERIAL9\_PROTOCOL: Serial9 protocol selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Control what protocol Serial9 port should be used for\. Note that the Frsky options require external converter hardware\. See the wiki for details\.


+----------------------------------------------+
| Values                                       |
+==============================================+
| +-------+----------------------------------+ |
| | Value | Meaning                          | |
| +=======+==================================+ |
| | -1    | None                             | |
| +-------+----------------------------------+ |
| | 1     | MAVLink1                         | |
| +-------+----------------------------------+ |
| | 2     | MAVLink2                         | |
| +-------+----------------------------------+ |
| | 3     | Frsky D                          | |
| +-------+----------------------------------+ |
| | 4     | Frsky SPort                      | |
| +-------+----------------------------------+ |
| | 5     | GPS                              | |
| +-------+----------------------------------+ |
| | 7     | Alexmos Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 8     | SToRM32 Gimbal Serial            | |
| +-------+----------------------------------+ |
| | 9     | Rangefinder                      | |
| +-------+----------------------------------+ |
| | 10    | FrSky SPort Passthrough (OpenTX) | |
| +-------+----------------------------------+ |
| | 11    | Lidar360                         | |
| +-------+----------------------------------+ |
| | 13    | Beacon                           | |
| +-------+----------------------------------+ |
| | 14    | Volz servo out                   | |
| +-------+----------------------------------+ |
| | 15    | SBus servo out                   | |
| +-------+----------------------------------+ |
| | 16    | ESC Telemetry                    | |
| +-------+----------------------------------+ |
| | 17    | Devo Telemetry                   | |
| +-------+----------------------------------+ |
| | 18    | OpticalFlow                      | |
| +-------+----------------------------------+ |
| | 19    | RobotisServo                     | |
| +-------+----------------------------------+ |
| | 20    | NMEA Output                      | |
| +-------+----------------------------------+ |
| | 21    | WindVane                         | |
| +-------+----------------------------------+ |
| | 22    | SLCAN                            | |
| +-------+----------------------------------+ |
| | 23    | RCIN                             | |
| +-------+----------------------------------+ |
| | 24    | MegaSquirt EFI                   | |
| +-------+----------------------------------+ |
| | 25    | LTM                              | |
| +-------+----------------------------------+ |
| | 26    | RunCam                           | |
| +-------+----------------------------------+ |
| | 27    | HottTelem                        | |
| +-------+----------------------------------+ |
| | 28    | Scripting                        | |
| +-------+----------------------------------+ |
| | 29    | Crossfire VTX                    | |
| +-------+----------------------------------+ |
| | 30    | Generator                        | |
| +-------+----------------------------------+ |
| | 31    | Winch                            | |
| +-------+----------------------------------+ |
| | 32    | MSP                              | |
| +-------+----------------------------------+ |
| | 33    | DJI FPV                          | |
| +-------+----------------------------------+ |
| | 34    | AirSpeed                         | |
| +-------+----------------------------------+ |
| | 35    | ADSB                             | |
| +-------+----------------------------------+ |
| | 36    | AHRS                             | |
| +-------+----------------------------------+ |
| | 37    | SmartAudio                       | |
| +-------+----------------------------------+ |
| | 38    | FETtecOneWire                    | |
| +-------+----------------------------------+ |
| | 39    | Torqeedo                         | |
| +-------+----------------------------------+ |
| | 40    | AIS                              | |
| +-------+----------------------------------+ |
|                                              |
+----------------------------------------------+




.. _SERIAL9_BAUD:

SERIAL9\_BAUD: Serial 9 Baud Rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


The baud rate used for Serial8\. Most stm32\-based boards can support rates of up to 1500\. If you setup a rate you cannot support and then can\'t connect to your board you should load a firmware from a different vehicle type\. That will reset all your parameters to defaults\.


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 1     | 1200    | |
| +-------+---------+ |
| | 2     | 2400    | |
| +-------+---------+ |
| | 4     | 4800    | |
| +-------+---------+ |
| | 9     | 9600    | |
| +-------+---------+ |
| | 19    | 19200   | |
| +-------+---------+ |
| | 38    | 38400   | |
| +-------+---------+ |
| | 57    | 57600   | |
| +-------+---------+ |
| | 111   | 111100  | |
| +-------+---------+ |
| | 115   | 115200  | |
| +-------+---------+ |
| | 230   | 230400  | |
| +-------+---------+ |
| | 256   | 256000  | |
| +-------+---------+ |
| | 460   | 460800  | |
| +-------+---------+ |
| | 500   | 500000  | |
| +-------+---------+ |
| | 921   | 921600  | |
| +-------+---------+ |
| | 1500  | 1500000 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERIAL9_OPTIONS:

SERIAL9\_OPTIONS: Serial9 options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Control over UART options\. The InvertRX option controls invert of the receive pin\. The InvertTX option controls invert of the transmit pin\. The HalfDuplex option controls half\-duplex \(onewire\) mode\, where both transmit and receive is done on the transmit wire\.


+-----------------------------------------+
| Bitmask                                 |
+=========================================+
| +-----+-------------------------------+ |
| | Bit | Meaning                       | |
| +=====+===============================+ |
| | 0   | InvertRX                      | |
| +-----+-------------------------------+ |
| | 1   | InvertTX                      | |
| +-----+-------------------------------+ |
| | 2   | HalfDuplex                    | |
| +-----+-------------------------------+ |
| | 3   | Swap                          | |
| +-----+-------------------------------+ |
| | 4   | RX_PullDown                   | |
| +-----+-------------------------------+ |
| | 5   | RX_PullUp                     | |
| +-----+-------------------------------+ |
| | 6   | TX_PullDown                   | |
| +-----+-------------------------------+ |
| | 7   | TX_PullUp                     | |
| +-----+-------------------------------+ |
| | 8   | RX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 9   | TX_NoDMA                      | |
| +-----+-------------------------------+ |
| | 10  | Don't forward mavlink to/from | |
| +-----+-------------------------------+ |
| | 11  | DisableFIFO                   | |
| +-----+-------------------------------+ |
|                                         |
+-----------------------------------------+





.. _parameters_SERVO:

SERVO Parameters
----------------


.. _SERVO_RATE:

SERVO\_RATE: Servo default output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the default output rate in Hz for all outputs\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 25 - 400 | hertz |
+----------+-------+




.. _SERVO_DSHOT_RATE:

SERVO\_DSHOT\_RATE: Servo DShot output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the DShot output rate for all outputs as a multiple of the loop rate\. 0 sets the output rate to be fixed at 1Khz for low loop rates\. This value should never be set below 500Hz\.


+---------------------------------+
| Values                          |
+=================================+
| +-------+---------------------+ |
| | Value | Meaning             | |
| +=======+=====================+ |
| | 0     | 1Khz                | |
| +-------+---------------------+ |
| | 1     | loop-rate           | |
| +-------+---------------------+ |
| | 2     | double loop-rate    | |
| +-------+---------------------+ |
| | 3     | triple loop-rate    | |
| +-------+---------------------+ |
| | 4     | quadruple loop rate | |
| +-------+---------------------+ |
|                                 |
+---------------------------------+




.. _SERVO_DSHOT_ESC:

SERVO\_DSHOT\_ESC: Servo DShot ESC type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the DShot ESC type for all outputs\. The ESC type affects the range of DShot commands available\. None means that no dshot commands will be executed\.


+------------------------------------+
| Values                             |
+====================================+
| +-------+------------------------+ |
| | Value | Meaning                | |
| +=======+========================+ |
| | 0     | None                   | |
| +-------+------------------------+ |
| | 1     | BLHeli32/BLHeli_S/Kiss | |
| +-------+------------------------+ |
|                                    |
+------------------------------------+




.. _SERVO_GPIO_MASK:

SERVO\_GPIO\_MASK: Servo GPIO mask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

This sets a bitmask of outputs which will be available as GPIOs\. Any auxillary output with either the function set to \-1 or with the corresponding bit set in this mask will be available for use as a GPIO pin


+--------------------+
| Bitmask            |
+====================+
| +-----+----------+ |
| | Bit | Meaning  | |
| +=====+==========+ |
| | 0   | Servo 1  | |
| +-----+----------+ |
| | 1   | Servo 2  | |
| +-----+----------+ |
| | 2   | Servo 3  | |
| +-----+----------+ |
| | 3   | Servo 4  | |
| +-----+----------+ |
| | 4   | Servo 5  | |
| +-----+----------+ |
| | 5   | Servo 6  | |
| +-----+----------+ |
| | 6   | Servo 7  | |
| +-----+----------+ |
| | 7   | Servo 8  | |
| +-----+----------+ |
| | 8   | Servo 9  | |
| +-----+----------+ |
| | 9   | Servo 10 | |
| +-----+----------+ |
| | 10  | Servo 11 | |
| +-----+----------+ |
| | 11  | Servo 12 | |
| +-----+----------+ |
| | 12  | Servo 13 | |
| +-----+----------+ |
| | 13  | Servo 14 | |
| +-----+----------+ |
| | 14  | Servo 15 | |
| +-----+----------+ |
| | 15  | Servo 16 | |
| +-----+----------+ |
|                    |
+--------------------+





.. _parameters_SERVO10_:

SERVO10\_ Parameters
--------------------


.. _SERVO10_MIN:

SERVO10\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO10_MAX:

SERVO10\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO10_TRIM:

SERVO10\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO10_REVERSED:

SERVO10\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO10_FUNCTION:

SERVO10\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO11_:

SERVO11\_ Parameters
--------------------


.. _SERVO11_MIN:

SERVO11\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO11_MAX:

SERVO11\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO11_TRIM:

SERVO11\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO11_REVERSED:

SERVO11\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO11_FUNCTION:

SERVO11\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO12_:

SERVO12\_ Parameters
--------------------


.. _SERVO12_MIN:

SERVO12\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO12_MAX:

SERVO12\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO12_TRIM:

SERVO12\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO12_REVERSED:

SERVO12\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO12_FUNCTION:

SERVO12\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO13_:

SERVO13\_ Parameters
--------------------


.. _SERVO13_MIN:

SERVO13\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO13_MAX:

SERVO13\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO13_TRIM:

SERVO13\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO13_REVERSED:

SERVO13\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO13_FUNCTION:

SERVO13\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO14_:

SERVO14\_ Parameters
--------------------


.. _SERVO14_MIN:

SERVO14\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO14_MAX:

SERVO14\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO14_TRIM:

SERVO14\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO14_REVERSED:

SERVO14\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO14_FUNCTION:

SERVO14\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO15_:

SERVO15\_ Parameters
--------------------


.. _SERVO15_MIN:

SERVO15\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO15_MAX:

SERVO15\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO15_TRIM:

SERVO15\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO15_REVERSED:

SERVO15\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO15_FUNCTION:

SERVO15\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO16_:

SERVO16\_ Parameters
--------------------


.. _SERVO16_MIN:

SERVO16\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO16_MAX:

SERVO16\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO16_TRIM:

SERVO16\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO16_REVERSED:

SERVO16\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO16_FUNCTION:

SERVO16\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO1_:

SERVO1\_ Parameters
-------------------


.. _SERVO1_MIN:

SERVO1\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO1_MAX:

SERVO1\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO1_TRIM:

SERVO1\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO1_REVERSED:

SERVO1\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO1_FUNCTION:

SERVO1\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO2_:

SERVO2\_ Parameters
-------------------


.. _SERVO2_MIN:

SERVO2\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO2_MAX:

SERVO2\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO2_TRIM:

SERVO2\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO2_REVERSED:

SERVO2\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO2_FUNCTION:

SERVO2\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO3_:

SERVO3\_ Parameters
-------------------


.. _SERVO3_MIN:

SERVO3\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO3_MAX:

SERVO3\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO3_TRIM:

SERVO3\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO3_REVERSED:

SERVO3\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO3_FUNCTION:

SERVO3\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO4_:

SERVO4\_ Parameters
-------------------


.. _SERVO4_MIN:

SERVO4\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO4_MAX:

SERVO4\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO4_TRIM:

SERVO4\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO4_REVERSED:

SERVO4\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO4_FUNCTION:

SERVO4\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO5_:

SERVO5\_ Parameters
-------------------


.. _SERVO5_MIN:

SERVO5\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO5_MAX:

SERVO5\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO5_TRIM:

SERVO5\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO5_REVERSED:

SERVO5\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO5_FUNCTION:

SERVO5\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO6_:

SERVO6\_ Parameters
-------------------


.. _SERVO6_MIN:

SERVO6\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO6_MAX:

SERVO6\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO6_TRIM:

SERVO6\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO6_REVERSED:

SERVO6\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO6_FUNCTION:

SERVO6\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO7_:

SERVO7\_ Parameters
-------------------


.. _SERVO7_MIN:

SERVO7\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO7_MAX:

SERVO7\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO7_TRIM:

SERVO7\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO7_REVERSED:

SERVO7\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO7_FUNCTION:

SERVO7\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO8_:

SERVO8\_ Parameters
-------------------


.. _SERVO8_MIN:

SERVO8\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO8_MAX:

SERVO8\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO8_TRIM:

SERVO8\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO8_REVERSED:

SERVO8\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO8_FUNCTION:

SERVO8\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO9_:

SERVO9\_ Parameters
-------------------


.. _SERVO9_MIN:

SERVO9\_MIN: Minimum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


minimum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 500 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO9_MAX:

SERVO9\_MAX: Maximum PWM
~~~~~~~~~~~~~~~~~~~~~~~~


maximum PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO9_TRIM:

SERVO9\_TRIM: Trim PWM
~~~~~~~~~~~~~~~~~~~~~~


Trim PWM pulse width in microseconds\. Typically 1000 is lower limit\, 1500 is neutral and 2000 is upper limit\.


+-----------+------------+---------------------+
| Increment | Range      | Units               |
+===========+============+=====================+
| 1         | 800 - 2200 | PWM in microseconds |
+-----------+------------+---------------------+




.. _SERVO9_REVERSED:

SERVO9\_REVERSED: Servo reverse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Reverse servo operation\. Set to 0 for normal operation\. Set to 1 to reverse this output channel\.


+----------------------+
| Values               |
+======================+
| +-------+----------+ |
| | Value | Meaning  | |
| +=======+==========+ |
| | 0     | Normal   | |
| +-------+----------+ |
| | 1     | Reversed | |
| +-------+----------+ |
|                      |
+----------------------+




.. _SERVO9_FUNCTION:

SERVO9\_FUNCTION: Servo output function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Function assigned to this servo\. Setting this to Disabled\(0\) will setup this output for control by auto missions or MAVLink servo set commands\. any other value will enable the corresponding function


+---------------------------------------+
| Values                                |
+=======================================+
| +-------+---------------------------+ |
| | Value | Meaning                   | |
| +=======+===========================+ |
| | -1    | GPIO                      | |
| +-------+---------------------------+ |
| | 0     | Disabled                  | |
| +-------+---------------------------+ |
| | 1     | RCPassThru                | |
| +-------+---------------------------+ |
| | 2     | Flap                      | |
| +-------+---------------------------+ |
| | 3     | FlapAuto                  | |
| +-------+---------------------------+ |
| | 4     | Aileron                   | |
| +-------+---------------------------+ |
| | 6     | MountPan                  | |
| +-------+---------------------------+ |
| | 7     | MountTilt                 | |
| +-------+---------------------------+ |
| | 8     | MountRoll                 | |
| +-------+---------------------------+ |
| | 9     | MountOpen                 | |
| +-------+---------------------------+ |
| | 10    | CameraTrigger             | |
| +-------+---------------------------+ |
| | 12    | Mount2Pan                 | |
| +-------+---------------------------+ |
| | 13    | Mount2Tilt                | |
| +-------+---------------------------+ |
| | 14    | Mount2Roll                | |
| +-------+---------------------------+ |
| | 15    | Mount2Open                | |
| +-------+---------------------------+ |
| | 16    | DifferentialSpoilerLeft1  | |
| +-------+---------------------------+ |
| | 17    | DifferentialSpoilerRight1 | |
| +-------+---------------------------+ |
| | 19    | Elevator                  | |
| +-------+---------------------------+ |
| | 21    | Rudder                    | |
| +-------+---------------------------+ |
| | 22    | SprayerPump               | |
| +-------+---------------------------+ |
| | 23    | SprayerSpinner            | |
| +-------+---------------------------+ |
| | 24    | FlaperonLeft              | |
| +-------+---------------------------+ |
| | 25    | FlaperonRight             | |
| +-------+---------------------------+ |
| | 26    | GroundSteering            | |
| +-------+---------------------------+ |
| | 27    | Parachute                 | |
| +-------+---------------------------+ |
| | 28    | Gripper                   | |
| +-------+---------------------------+ |
| | 29    | LandingGear               | |
| +-------+---------------------------+ |
| | 30    | EngineRunEnable           | |
| +-------+---------------------------+ |
| | 31    | HeliRSC                   | |
| +-------+---------------------------+ |
| | 32    | HeliTailRSC               | |
| +-------+---------------------------+ |
| | 33    | Motor1                    | |
| +-------+---------------------------+ |
| | 34    | Motor2                    | |
| +-------+---------------------------+ |
| | 35    | Motor3                    | |
| +-------+---------------------------+ |
| | 36    | Motor4                    | |
| +-------+---------------------------+ |
| | 37    | Motor5                    | |
| +-------+---------------------------+ |
| | 38    | Motor6                    | |
| +-------+---------------------------+ |
| | 39    | Motor7                    | |
| +-------+---------------------------+ |
| | 40    | Motor8                    | |
| +-------+---------------------------+ |
| | 41    | TiltMotorsFront           | |
| +-------+---------------------------+ |
| | 45    | TiltMotorsRear            | |
| +-------+---------------------------+ |
| | 46    | TiltMotorRearLeft         | |
| +-------+---------------------------+ |
| | 47    | TiltMotorRearRight        | |
| +-------+---------------------------+ |
| | 51    | RCIN1                     | |
| +-------+---------------------------+ |
| | 52    | RCIN2                     | |
| +-------+---------------------------+ |
| | 53    | RCIN3                     | |
| +-------+---------------------------+ |
| | 54    | RCIN4                     | |
| +-------+---------------------------+ |
| | 55    | RCIN5                     | |
| +-------+---------------------------+ |
| | 56    | RCIN6                     | |
| +-------+---------------------------+ |
| | 57    | RCIN7                     | |
| +-------+---------------------------+ |
| | 58    | RCIN8                     | |
| +-------+---------------------------+ |
| | 59    | RCIN9                     | |
| +-------+---------------------------+ |
| | 60    | RCIN10                    | |
| +-------+---------------------------+ |
| | 61    | RCIN11                    | |
| +-------+---------------------------+ |
| | 62    | RCIN12                    | |
| +-------+---------------------------+ |
| | 63    | RCIN13                    | |
| +-------+---------------------------+ |
| | 64    | RCIN14                    | |
| +-------+---------------------------+ |
| | 65    | RCIN15                    | |
| +-------+---------------------------+ |
| | 66    | RCIN16                    | |
| +-------+---------------------------+ |
| | 67    | Ignition                  | |
| +-------+---------------------------+ |
| | 69    | Starter                   | |
| +-------+---------------------------+ |
| | 70    | Throttle                  | |
| +-------+---------------------------+ |
| | 71    | TrackerYaw                | |
| +-------+---------------------------+ |
| | 72    | TrackerPitch              | |
| +-------+---------------------------+ |
| | 73    | ThrottleLeft              | |
| +-------+---------------------------+ |
| | 74    | ThrottleRight             | |
| +-------+---------------------------+ |
| | 75    | TiltMotorFrontLeft        | |
| +-------+---------------------------+ |
| | 76    | TiltMotorFrontRight       | |
| +-------+---------------------------+ |
| | 77    | ElevonLeft                | |
| +-------+---------------------------+ |
| | 78    | ElevonRight               | |
| +-------+---------------------------+ |
| | 79    | VTailLeft                 | |
| +-------+---------------------------+ |
| | 80    | VTailRight                | |
| +-------+---------------------------+ |
| | 81    | BoostThrottle             | |
| +-------+---------------------------+ |
| | 82    | Motor9                    | |
| +-------+---------------------------+ |
| | 83    | Motor10                   | |
| +-------+---------------------------+ |
| | 84    | Motor11                   | |
| +-------+---------------------------+ |
| | 85    | Motor12                   | |
| +-------+---------------------------+ |
| | 86    | DifferentialSpoilerLeft2  | |
| +-------+---------------------------+ |
| | 87    | DifferentialSpoilerRight2 | |
| +-------+---------------------------+ |
| | 88    | Winch                     | |
| +-------+---------------------------+ |
| | 89    | Main Sail                 | |
| +-------+---------------------------+ |
| | 90    | CameraISO                 | |
| +-------+---------------------------+ |
| | 91    | CameraAperture            | |
| +-------+---------------------------+ |
| | 92    | CameraFocus               | |
| +-------+---------------------------+ |
| | 93    | CameraShutterSpeed        | |
| +-------+---------------------------+ |
| | 94    | Script1                   | |
| +-------+---------------------------+ |
| | 95    | Script2                   | |
| +-------+---------------------------+ |
| | 96    | Script3                   | |
| +-------+---------------------------+ |
| | 97    | Script4                   | |
| +-------+---------------------------+ |
| | 98    | Script5                   | |
| +-------+---------------------------+ |
| | 99    | Script6                   | |
| +-------+---------------------------+ |
| | 100   | Script7                   | |
| +-------+---------------------------+ |
| | 101   | Script8                   | |
| +-------+---------------------------+ |
| | 102   | Script9                   | |
| +-------+---------------------------+ |
| | 103   | Script10                  | |
| +-------+---------------------------+ |
| | 104   | Script11                  | |
| +-------+---------------------------+ |
| | 105   | Script12                  | |
| +-------+---------------------------+ |
| | 106   | Script13                  | |
| +-------+---------------------------+ |
| | 107   | Script14                  | |
| +-------+---------------------------+ |
| | 108   | Script15                  | |
| +-------+---------------------------+ |
| | 109   | Script16                  | |
| +-------+---------------------------+ |
| | 120   | NeoPixel1                 | |
| +-------+---------------------------+ |
| | 121   | NeoPixel2                 | |
| +-------+---------------------------+ |
| | 122   | NeoPixel3                 | |
| +-------+---------------------------+ |
| | 123   | NeoPixel4                 | |
| +-------+---------------------------+ |
| | 124   | RateRoll                  | |
| +-------+---------------------------+ |
| | 125   | RatePitch                 | |
| +-------+---------------------------+ |
| | 126   | RateThrust                | |
| +-------+---------------------------+ |
| | 127   | RateYaw                   | |
| +-------+---------------------------+ |
| | 128   | WingSailElevator          | |
| +-------+---------------------------+ |
| | 129   | ProfiLED1                 | |
| +-------+---------------------------+ |
| | 130   | ProfiLED2                 | |
| +-------+---------------------------+ |
| | 131   | ProfiLED3                 | |
| +-------+---------------------------+ |
| | 132   | ProfiLEDClock             | |
| +-------+---------------------------+ |
| | 133   | Winch Clutch              | |
| +-------+---------------------------+ |
| | 134   | SERVOn_MIN                | |
| +-------+---------------------------+ |
| | 135   | SERVOn_TRIM               | |
| +-------+---------------------------+ |
| | 136   | SERVOn_MAX                | |
| +-------+---------------------------+ |
| | 137   | SailMastRotation          | |
| +-------+---------------------------+ |
|                                       |
+---------------------------------------+





.. _parameters_SERVO_BLH_:

SERVO\_BLH\_ Parameters
-----------------------


.. _SERVO_BLH_MASK:

SERVO\_BLH\_MASK: BLHeli Channel Bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Enable of BLHeli pass\-thru servo protocol support to specific channels\. This mask is in addition to motors enabled using SERVO\_BLH\_AUTO \(if any\)


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Channel1  | |
| +-----+-----------+ |
| | 1   | Channel2  | |
| +-----+-----------+ |
| | 2   | Channel3  | |
| +-----+-----------+ |
| | 3   | Channel4  | |
| +-----+-----------+ |
| | 4   | Channel5  | |
| +-----+-----------+ |
| | 5   | Channel6  | |
| +-----+-----------+ |
| | 6   | Channel7  | |
| +-----+-----------+ |
| | 7   | Channel8  | |
| +-----+-----------+ |
| | 8   | Channel9  | |
| +-----+-----------+ |
| | 9   | Channel10 | |
| +-----+-----------+ |
| | 10  | Channel11 | |
| +-----+-----------+ |
| | 11  | Channel12 | |
| +-----+-----------+ |
| | 12  | Channel13 | |
| +-----+-----------+ |
| | 13  | Channel14 | |
| +-----+-----------+ |
| | 14  | Channel15 | |
| +-----+-----------+ |
| | 15  | Channel16 | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _SERVO_BLH_AUTO:

SERVO\_BLH\_AUTO: BLHeli pass\-thru auto\-enable for multicopter motors
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


If set to 1 this auto\-enables BLHeli pass\-thru support for all multicopter motors


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




.. _SERVO_BLH_TEST:

SERVO\_BLH\_TEST: BLHeli internal interface test
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Setting SERVO\_BLH\_TEST to a motor number enables an internal test of the BLHeli ESC protocol to the corresponding ESC\. The debug output is displayed on the USB console\.


+------------------------+
| Values                 |
+========================+
| +-------+------------+ |
| | Value | Meaning    | |
| +=======+============+ |
| | 0     | Disabled   | |
| +-------+------------+ |
| | 1     | TestMotor1 | |
| +-------+------------+ |
| | 2     | TestMotor2 | |
| +-------+------------+ |
| | 3     | TestMotor3 | |
| +-------+------------+ |
| | 4     | TestMotor4 | |
| +-------+------------+ |
| | 5     | TestMotor5 | |
| +-------+------------+ |
| | 6     | TestMotor6 | |
| +-------+------------+ |
| | 7     | TestMotor7 | |
| +-------+------------+ |
| | 8     | TestMotor8 | |
| +-------+------------+ |
|                        |
+------------------------+




.. _SERVO_BLH_TMOUT:

SERVO\_BLH\_TMOUT: BLHeli protocol timeout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the inactivity timeout for the BLHeli protocol in seconds\. If no packets are received in this time normal MAVLink operations are resumed\. A value of 0 means no timeout


+---------+---------+
| Range   | Units   |
+=========+=========+
| 0 - 300 | seconds |
+---------+---------+




.. _SERVO_BLH_TRATE:

SERVO\_BLH\_TRATE: BLHeli telemetry rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This sets the rate in Hz for requesting telemetry from ESCs\. It is the rate per ESC\. Setting to zero disables telemetry requests


+---------+-------+
| Range   | Units |
+=========+=======+
| 0 - 500 | hertz |
+---------+-------+




.. _SERVO_BLH_DEBUG:

SERVO\_BLH\_DEBUG: BLHeli debug level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


When set to 1 this enabled verbose debugging output over MAVLink when the blheli protocol is active\. This can be used to diagnose failures\.


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




.. _SERVO_BLH_OTYPE:

SERVO\_BLH\_OTYPE: BLHeli output type override
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

When set to a non\-zero value this overrides the output type for the output channels given by SERVO\_BLH\_MASK\. This can be used to enable DShot on outputs that are not part of the multicopter motors group\.


+------------------------+
| Values                 |
+========================+
| +-------+------------+ |
| | Value | Meaning    | |
| +=======+============+ |
| | 0     | None       | |
| +-------+------------+ |
| | 1     | OneShot    | |
| +-------+------------+ |
| | 2     | OneShot125 | |
| +-------+------------+ |
| | 3     | Brushed    | |
| +-------+------------+ |
| | 4     | DShot150   | |
| +-------+------------+ |
| | 5     | DShot300   | |
| +-------+------------+ |
| | 6     | DShot600   | |
| +-------+------------+ |
| | 7     | DShot1200  | |
| +-------+------------+ |
|                        |
+------------------------+




.. _SERVO_BLH_PORT:

SERVO\_BLH\_PORT: Control port
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the serial port to use for blheli pass\-thru


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Console | |
| +-------+---------+ |
| | 1     | Serial1 | |
| +-------+---------+ |
| | 2     | Serial2 | |
| +-------+---------+ |
| | 3     | Serial3 | |
| +-------+---------+ |
| | 4     | Serial4 | |
| +-------+---------+ |
| | 5     | Serial5 | |
| +-------+---------+ |
|                     |
+---------------------+




.. _SERVO_BLH_POLES:

SERVO\_BLH\_POLES: BLHeli Motor Poles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This allows calculation of true RPM from ESC\'s eRPM\. The default is 14\.


+---------+
| Range   |
+=========+
| 1 - 127 |
+---------+




.. _SERVO_BLH_3DMASK:

SERVO\_BLH\_3DMASK: BLHeli bitmask of 3D channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Mask of channels which are dynamically reversible\. This is used to configure ESCs in \'3D\' mode\, allowing for the motor to spin in either direction


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Channel1  | |
| +-----+-----------+ |
| | 1   | Channel2  | |
| +-----+-----------+ |
| | 2   | Channel3  | |
| +-----+-----------+ |
| | 3   | Channel4  | |
| +-----+-----------+ |
| | 4   | Channel5  | |
| +-----+-----------+ |
| | 5   | Channel6  | |
| +-----+-----------+ |
| | 6   | Channel7  | |
| +-----+-----------+ |
| | 7   | Channel8  | |
| +-----+-----------+ |
| | 8   | Channel9  | |
| +-----+-----------+ |
| | 9   | Channel10 | |
| +-----+-----------+ |
| | 10  | Channel11 | |
| +-----+-----------+ |
| | 11  | Channel12 | |
| +-----+-----------+ |
| | 12  | Channel13 | |
| +-----+-----------+ |
| | 13  | Channel14 | |
| +-----+-----------+ |
| | 14  | Channel15 | |
| +-----+-----------+ |
| | 15  | Channel16 | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _SERVO_BLH_BDMASK:

SERVO\_BLH\_BDMASK: BLHeli bitmask of bi\-directional dshot channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Mask of channels which support bi\-directional dshot\. This is used for ESCs which have firmware that supports bi\-directional dshot allowing fast rpm telemetry values to be returned for the harmonic notch\.


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Channel1  | |
| +-----+-----------+ |
| | 1   | Channel2  | |
| +-----+-----------+ |
| | 2   | Channel3  | |
| +-----+-----------+ |
| | 3   | Channel4  | |
| +-----+-----------+ |
| | 4   | Channel5  | |
| +-----+-----------+ |
| | 5   | Channel6  | |
| +-----+-----------+ |
| | 6   | Channel7  | |
| +-----+-----------+ |
| | 7   | Channel8  | |
| +-----+-----------+ |
| | 8   | Channel9  | |
| +-----+-----------+ |
| | 9   | Channel10 | |
| +-----+-----------+ |
| | 10  | Channel11 | |
| +-----+-----------+ |
| | 11  | Channel12 | |
| +-----+-----------+ |
| | 12  | Channel13 | |
| +-----+-----------+ |
| | 13  | Channel14 | |
| +-----+-----------+ |
| | 14  | Channel15 | |
| +-----+-----------+ |
| | 15  | Channel16 | |
| +-----+-----------+ |
|                     |
+---------------------+




.. _SERVO_BLH_RVMASK:

SERVO\_BLH\_RVMASK: BLHeli bitmask of reversed channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Mask of channels which are reversed\. This is used to configure ESCs in reversed mode


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Channel1  | |
| +-----+-----------+ |
| | 1   | Channel2  | |
| +-----+-----------+ |
| | 2   | Channel3  | |
| +-----+-----------+ |
| | 3   | Channel4  | |
| +-----+-----------+ |
| | 4   | Channel5  | |
| +-----+-----------+ |
| | 5   | Channel6  | |
| +-----+-----------+ |
| | 6   | Channel7  | |
| +-----+-----------+ |
| | 7   | Channel8  | |
| +-----+-----------+ |
| | 8   | Channel9  | |
| +-----+-----------+ |
| | 9   | Channel10 | |
| +-----+-----------+ |
| | 10  | Channel11 | |
| +-----+-----------+ |
| | 11  | Channel12 | |
| +-----+-----------+ |
| | 12  | Channel13 | |
| +-----+-----------+ |
| | 13  | Channel14 | |
| +-----+-----------+ |
| | 14  | Channel15 | |
| +-----+-----------+ |
| | 15  | Channel16 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_SERVO_FTW_:

SERVO\_FTW\_ Parameters
-----------------------


.. _SERVO_FTW_MASK:

SERVO\_FTW\_MASK: Servo channel output bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: Reboot required after change*

Servo channel mask specifying FETtec ESC output\.


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | SERVO1  | |
| +-----+---------+ |
| | 1   | SERVO2  | |
| +-----+---------+ |
| | 2   | SERVO3  | |
| +-----+---------+ |
| | 3   | SERVO4  | |
| +-----+---------+ |
| | 4   | SERVO5  | |
| +-----+---------+ |
| | 5   | SERVO6  | |
| +-----+---------+ |
| | 6   | SERVO7  | |
| +-----+---------+ |
| | 7   | SERVO8  | |
| +-----+---------+ |
| | 8   | SERVO9  | |
| +-----+---------+ |
| | 9   | SERVO10 | |
| +-----+---------+ |
| | 10  | SERVO11 | |
| +-----+---------+ |
| | 11  | SERVO12 | |
| +-----+---------+ |
|                   |
+-------------------+




.. _SERVO_FTW_RVMASK:

SERVO\_FTW\_RVMASK: Servo channel reverse rotation bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Servo channel mask to reverse rotation of FETtec ESC outputs\.


+-------------------+
| Bitmask           |
+===================+
| +-----+---------+ |
| | Bit | Meaning | |
| +=====+=========+ |
| | 0   | SERVO1  | |
| +-----+---------+ |
| | 1   | SERVO2  | |
| +-----+---------+ |
| | 2   | SERVO3  | |
| +-----+---------+ |
| | 3   | SERVO4  | |
| +-----+---------+ |
| | 4   | SERVO5  | |
| +-----+---------+ |
| | 5   | SERVO6  | |
| +-----+---------+ |
| | 6   | SERVO7  | |
| +-----+---------+ |
| | 7   | SERVO8  | |
| +-----+---------+ |
| | 8   | SERVO9  | |
| +-----+---------+ |
| | 9   | SERVO10 | |
| +-----+---------+ |
| | 10  | SERVO11 | |
| +-----+---------+ |
| | 11  | SERVO12 | |
| +-----+---------+ |
|                   |
+-------------------+




.. _SERVO_FTW_POLES:

SERVO\_FTW\_POLES: Nr\. electrical poles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Number of motor electrical poles


+--------+
| Range  |
+========+
| 2 - 50 |
+--------+





.. _parameters_SERVO_ROB_:

SERVO\_ROB\_ Parameters
-----------------------


.. _SERVO_ROB_POSMIN:

SERVO\_ROB\_POSMIN: Robotis servo position min
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Position minimum at servo min value\. This should be within the position control range of the servos\, normally 0 to 4095


+----------+
| Range    |
+==========+
| 0 - 4095 |
+----------+




.. _SERVO_ROB_POSMAX:

SERVO\_ROB\_POSMAX: Robotis servo position max
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Position maximum at servo max value\. This should be within the position control range of the servos\, normally 0 to 4095


+----------+
| Range    |
+==========+
| 0 - 4095 |
+----------+





.. _parameters_SERVO_SBUS_:

SERVO\_SBUS\_ Parameters
------------------------


.. _SERVO_SBUS_RATE:

SERVO\_SBUS\_RATE: SBUS default output rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

This sets the SBUS output frame rate in Hz\.


+----------+-------+
| Range    | Units |
+==========+=======+
| 25 - 250 | hertz |
+----------+-------+





.. _parameters_SERVO_VOLZ_:

SERVO\_VOLZ\_ Parameters
------------------------


.. _SERVO_VOLZ_MASK:

SERVO\_VOLZ\_MASK: Channel Bitmask
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Enable of volz servo protocol to specific channels


+---------------------+
| Bitmask             |
+=====================+
| +-----+-----------+ |
| | Bit | Meaning   | |
| +=====+===========+ |
| | 0   | Channel1  | |
| +-----+-----------+ |
| | 1   | Channel2  | |
| +-----+-----------+ |
| | 2   | Channel3  | |
| +-----+-----------+ |
| | 3   | Channel4  | |
| +-----+-----------+ |
| | 4   | Channel5  | |
| +-----+-----------+ |
| | 5   | Channel6  | |
| +-----+-----------+ |
| | 6   | Channel7  | |
| +-----+-----------+ |
| | 7   | Channel8  | |
| +-----+-----------+ |
| | 8   | Channel9  | |
| +-----+-----------+ |
| | 9   | Channel10 | |
| +-----+-----------+ |
| | 10  | Channel11 | |
| +-----+-----------+ |
| | 11  | Channel12 | |
| +-----+-----------+ |
| | 12  | Channel13 | |
| +-----+-----------+ |
| | 13  | Channel14 | |
| +-----+-----------+ |
| | 14  | Channel15 | |
| +-----+-----------+ |
| | 15  | Channel16 | |
| +-----+-----------+ |
|                     |
+---------------------+





.. _parameters_SR0_:

SR0\_ Parameters
----------------


.. _SR0_RAW_SENS:

SR0\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_EXT_STAT:

SR0\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_RC_CHAN:

SR0\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_RAW_CTRL:

SR0\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_POSITION:

SR0\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_EXTRA1:

SR0\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_EXTRA2:

SR0\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_EXTRA3:

SR0\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR0_PARAMS:

SR0\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR1_:

SR1\_ Parameters
----------------


.. _SR1_RAW_SENS:

SR1\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_EXT_STAT:

SR1\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_RC_CHAN:

SR1\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_RAW_CTRL:

SR1\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_POSITION:

SR1\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_EXTRA1:

SR1\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_EXTRA2:

SR1\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_EXTRA3:

SR1\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR1_PARAMS:

SR1\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR2_:

SR2\_ Parameters
----------------


.. _SR2_RAW_SENS:

SR2\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_EXT_STAT:

SR2\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_RC_CHAN:

SR2\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_RAW_CTRL:

SR2\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_POSITION:

SR2\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_EXTRA1:

SR2\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_EXTRA2:

SR2\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_EXTRA3:

SR2\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR2_PARAMS:

SR2\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR3_:

SR3\_ Parameters
----------------


.. _SR3_RAW_SENS:

SR3\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_EXT_STAT:

SR3\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_RC_CHAN:

SR3\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_RAW_CTRL:

SR3\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_POSITION:

SR3\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_EXTRA1:

SR3\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_EXTRA2:

SR3\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_EXTRA3:

SR3\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR3_PARAMS:

SR3\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR4_:

SR4\_ Parameters
----------------


.. _SR4_RAW_SENS:

SR4\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_EXT_STAT:

SR4\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_RC_CHAN:

SR4\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_RAW_CTRL:

SR4\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_POSITION:

SR4\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_EXTRA1:

SR4\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_EXTRA2:

SR4\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_EXTRA3:

SR4\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR4_PARAMS:

SR4\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR5_:

SR5\_ Parameters
----------------


.. _SR5_RAW_SENS:

SR5\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_EXT_STAT:

SR5\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_RC_CHAN:

SR5\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_RAW_CTRL:

SR5\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_POSITION:

SR5\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_EXTRA1:

SR5\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_EXTRA2:

SR5\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_EXTRA3:

SR5\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR5_PARAMS:

SR5\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_SR6_:

SR6\_ Parameters
----------------


.. _SR6_RAW_SENS:

SR6\_RAW\_SENS: Raw sensor stream rate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw sensor stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_EXT_STAT:

SR6\_EXT\_STAT: Extended status stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extended status stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_RC_CHAN:

SR6\_RC\_CHAN: RC Channel stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

RC Channel stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_RAW_CTRL:

SR6\_RAW\_CTRL: Raw Control stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Raw Control stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_POSITION:

SR6\_POSITION: Position stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Position stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_EXTRA1:

SR6\_EXTRA1: Extra data type 1 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 1 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_EXTRA2:

SR6\_EXTRA2: Extra data type 2 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 2 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_EXTRA3:

SR6\_EXTRA3: Extra data type 3 stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Extra data type 3 stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+




.. _SR6_PARAMS:

SR6\_PARAMS: Parameter stream rate to ground station
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Parameter stream rate to ground station


+-----------+--------+-------+
| Increment | Range  | Units |
+===========+========+=======+
| 1         | 0 - 50 | hertz |
+-----------+--------+-------+





.. _parameters_STAT:

STAT Parameters
---------------


.. _STAT_BOOTCNT:

STAT\_BOOTCNT: Boot Count
~~~~~~~~~~~~~~~~~~~~~~~~~


Number of times board has been booted


+----------+
| ReadOnly |
+==========+
| True     |
+----------+




.. _STAT_FLTTIME:

STAT\_FLTTIME: Total FlightTime
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Total FlightTime \(seconds\)


+----------+---------+
| ReadOnly | Units   |
+==========+=========+
| True     | seconds |
+----------+---------+




.. _STAT_RUNTIME:

STAT\_RUNTIME: Total RunTime
~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Total time autopilot has run


+----------+---------+
| ReadOnly | Units   |
+==========+=========+
| True     | seconds |
+----------+---------+




.. _STAT_RESET:

STAT\_RESET: Statistics Reset Time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Seconds since January 1st 2016 \(Unix epoch\+1451606400\) since statistics reset \(set to 0 to reset statistics\)


+----------+---------+
| ReadOnly | Units   |
+==========+=========+
| True     | seconds |
+----------+---------+





.. _parameters_VISO:

VISO Parameters
---------------


.. _VISO_TYPE:

VISO\_TYPE: Visual odometry camera connection type
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*
| *Note: Reboot required after change*

Visual odometry camera connection type


+-----------------------+
| Values                |
+=======================+
| +-------+-----------+ |
| | Value | Meaning   | |
| +=======+===========+ |
| | 0     | None      | |
| +-------+-----------+ |
| | 1     | MAVLink   | |
| +-------+-----------+ |
| | 2     | IntelT265 | |
| +-------+-----------+ |
|                       |
+-----------------------+




.. _VISO_POS_X:

VISO\_POS\_X: Visual odometry camera X position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

X position of the camera in body frame\. Positive X is forward of the origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _VISO_POS_Y:

VISO\_POS\_Y: Visual odometry camera Y position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Y position of the camera in body frame\. Positive Y is to the right of the origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _VISO_POS_Z:

VISO\_POS\_Z: Visual odometry camera Z position offset
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Z position of the camera in body frame\. Positive Z is down from the origin\.


+-----------+--------+--------+
| Increment | Range  | Units  |
+===========+========+========+
| 0.01      | -5 - 5 | meters |
+-----------+--------+--------+




.. _VISO_ORIENT:

VISO\_ORIENT: Visual odometery camera orientation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometery camera orientation


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Forward | |
| +-------+---------+ |
| | 2     | Right   | |
| +-------+---------+ |
| | 4     | Back    | |
| +-------+---------+ |
| | 6     | Left    | |
| +-------+---------+ |
| | 24    | Up      | |
| +-------+---------+ |
| | 25    | Down    | |
| +-------+---------+ |
|                     |
+---------------------+




.. _VISO_SCALE:

VISO\_SCALE: Visual odometry scaling factor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometry scaling factor applied to position estimates from sensor


.. _VISO_DELAY_MS:

VISO\_DELAY\_MS: Visual odometry sensor delay
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometry sensor delay relative to inertial measurements


+---------+--------------+
| Range   | Units        |
+=========+==============+
| 0 - 250 | milliseconds |
+---------+--------------+




.. _VISO_VEL_M_NSE:

VISO\_VEL\_M\_NSE: Visual odometry velocity measurement noise
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometry velocity measurement noise in m\/s


+------------+-------------------+
| Range      | Units             |
+============+===================+
| 0.05 - 5.0 | meters per second |
+------------+-------------------+




.. _VISO_POS_M_NSE:

VISO\_POS\_M\_NSE: Visual odometry position measurement noise
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometry position measurement noise minimum \(meters\)\. This value will be used if the sensor provides a lower noise value \(or no noise value\)


+------------+--------+
| Range      | Units  |
+============+========+
| 0.1 - 10.0 | meters |
+------------+--------+




.. _VISO_YAW_M_NSE:

VISO\_YAW\_M\_NSE: Visual odometry yaw measurement noise
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Visual odometry yaw measurement noise minimum \(radians\)\, This value will be used if the sensor provides a lower noise value \(or no noise value\)


+------------+---------+
| Range      | Units   |
+============+=========+
| 0.05 - 1.0 | radians |
+------------+---------+





.. _parameters_VTX_:

VTX\_ Parameters
----------------


.. _VTX_ENABLE:

VTX\_ENABLE: Is the Video Transmitter enabled or not
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Toggles the Video Transmitter on and off


+---------------------+
| Values              |
+=====================+
| +-------+---------+ |
| | Value | Meaning | |
| +=======+=========+ |
| | 0     | Disable | |
| +-------+---------+ |
| | 1     | Enable  | |
| +-------+---------+ |
|                     |
+---------------------+




.. _VTX_POWER:

VTX\_POWER: Video Transmitter Power Level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Video Transmitter Power Level\. Different VTXs support different power levels\, the power level chosen will be rounded down to the nearest supported power level


+----------+
| Range    |
+==========+
| 1 - 1000 |
+----------+




.. _VTX_CHANNEL:

VTX\_CHANNEL: Video Transmitter Channel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Video Transmitter Channel


+-------+
| Range |
+=======+
| 0 - 7 |
+-------+




.. _VTX_BAND:

VTX\_BAND: Video Transmitter Band
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Video Transmitter Band


+--------------------------+
| Values                   |
+==========================+
| +-------+--------------+ |
| | Value | Meaning      | |
| +=======+==============+ |
| | 0     | Band A       | |
| +-------+--------------+ |
| | 1     | Band B       | |
| +-------+--------------+ |
| | 2     | Band E       | |
| +-------+--------------+ |
| | 3     | Airwave      | |
| +-------+--------------+ |
| | 4     | RaceBand     | |
| +-------+--------------+ |
| | 5     | Low RaceBand | |
| +-------+--------------+ |
|                          |
+--------------------------+




.. _VTX_FREQ:

VTX\_FREQ: Video Transmitter Frequency
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Video Transmitter Frequency\. The frequency is derived from the setting of BAND and CHANNEL


+-------------+----------+
| Range       | ReadOnly |
+=============+==========+
| 5000 - 6000 | True     |
+-------------+----------+




.. _VTX_OPTIONS:

VTX\_OPTIONS: Video Transmitter Options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| *Note: This parameter is for advanced users*

Video Transmitter Options\. Pitmode puts the VTX in a low power state\. Unlocked enables certain restricted frequencies and power levels\. Do not enable the Unlocked option unless you have appropriate permissions in your jurisdiction to transmit at high power levels\.


+---------------------------------------------+
| Bitmask                                     |
+=============================================+
| +-----+-----------------------------------+ |
| | Bit | Meaning                           | |
| +=====+===================================+ |
| | 0   | Pitmode                           | |
| +-----+-----------------------------------+ |
| | 1   | Pitmode until armed               | |
| +-----+-----------------------------------+ |
| | 2   | Pitmode when disarmed             | |
| +-----+-----------------------------------+ |
| | 3   | Unlocked                          | |
| +-----+-----------------------------------+ |
| | 4   | Add leading zero byte to requests | |
| +-----+-----------------------------------+ |
|                                             |
+---------------------------------------------+




.. _VTX_MAX_POWER:

VTX\_MAX\_POWER: Video Transmitter Max Power Level
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Video Transmitter Maximum Power Level\. Different VTXs support different power levels\, this prevents the power aux switch from requesting too high a power level\. The switch supports 6 power levels and the selected power will be a subdivision between 0 and this setting\.


+-----------+
| Range     |
+===========+
| 25 - 1000 |
+-----------+



