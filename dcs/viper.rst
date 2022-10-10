F-16C Viper
===========

Engine Start
------------

.. NOTE::
   Unlike other airframes the Viper needs no ground power to spool up.

EXT LIGHTING
  - set FLASH STEADY switch to STEADY
  - set WING/TAIL switch to BRT
   
FUEL
  - ensure ENGINE FEED knob is set to NORM

ELEC
  - set MAIN PWR switch to MAIN PWR
  
ENG & JET START
  - set JFS switch to START 2
  - wait for the green JFS RUN light to go on and the RPM to reach 25%

Throttle
  - switch to IDLE position (``rshift-home`` by default)
  - make sure the FTIT does not exceed 900°C
  - wait for the RPM to reach 65%, the FTIT to settle at 400°C, and the oil pressure to settle at 27 psi

Front Panel
  - turn SAI Cage knob until the artificial horizon is uncaged and calibrated

.. HINT::
   You can switch the trottle from IDLE back to the OFF position by pressing ``rshift-end``.

.. HINT::
   You can get rid of the ELEC SYS warning on the caution pannel by pressing the CAUTION RESET button in the ELEC panel.


System Start
------------

AVIONICS POWER
  - set MMC switch to MMC
  - set ST STA switch to ST STA
  - set MFD switch to MFD
  - set UFC switch to UFC
  - set GPS switch to GPS
  - set DL switch to DL
  - set INS knob to NORM
  - set MIDS LVT to ON

SNSR PWR
  - set FCR switch to FCR
  - set RDR ALT switch to STBY

.. HINT::
   If the HUD hasn't come on automatically, turn up the ICP HUD symbology intensity knob.

IFF
  - set IFF MASTER knob to STBY
  - ensure C&I knob is set to UFC

THREAT WARNING AUX
  - enable RWR indicator control POWER button

CMDS
  - set RWR 555 switch to ON
  - set JMR source switch to ON
  - set CH expendable category switch to ON
  - set FL expendable category switch to ON
  - ensure PROGRAM knob is set to 1
  - set MODE knob to MAN

AVIONICS POWER
  - wait until the DED shows a flashing RDY in the INS line
  - set INS knob to NAV

EXT LIGHTING
  - set FLASH STEADY switch to FLASH


Taxi
----

- TAXI LANDING LIGHTS switch to TAXI
- enable nose wheel steering

"Kutaisi traffic, Uzi 9-1, taxi runway 07."

- taxi

Take Off
--------

"Kutaisi control, Uzi 9-1, take off runway 07."

IFF
  - set IFF MASTER knob to NORM

SNSR PWR
  - set RDR ALT switch to RDR ALT

EXT LIGHTING
  - set ANTI-COLL knob to OFF

- close canopy (``lctl-C`` by default)
- set canopy handle (yellow spider) to DOWN
- set ejection safety lever to ARMED

- ensure speed brake is retracted
- go full throttle
- deactivate nose wheel steering
- lift off
- retract landing gear
- set TAXI LANDING LIGHTS switch to OFF

Land
----

"Kutaisi control, Uzi 9-1, coming in runway 07."

- extract landing gear
- set TAXI LANDING LIGHTS switch to LANDING

"Kutaisi control, Uzi 9-1, on finals."

- land

EXT LIGHTING
  - set ANTI-COLL knob to 1

"Kutaisi control, Uzi 9-1, runway 07 clear."


Light Discipline
----------------
In a hostile environment we turn off all lights. Otherwise, whenever we operate the plane we turn on the navigation lights. When the plane stands still, we set the navigation lights to steady. When the plane moves in any way, we set the navigation lights to flashing. Whenever we operate the plane on the ground, we turn on the anti-collision lights. Only while taxiing we turn on the taxi lights. Only while landing we turn on the landing lights.

========= ========= ============ ========= ===================
procedure anti-coll flash steady wing/tail landing taxi lights
========= ========= ============ ========= ===================
park      1                      OFF       OFF
hold      1         STEADY       BRT       OFF
taxi      1         FLASH        BRT       TAXI
takeoff   OFF       FLASH        BRT       TAXI
combat    OFF                    OFF       OFF
land      OFF       FLASH        BRT       LAND
========= ========= ============ ========= ===================

.. image:: img/light_discipline.png
   :width: 602
   :height: 801
   :alt: light discipline state graph


Radio
-----

.. CAUTION::
   Make sure the C&I knob on the IFF panel is set to UFC.

- press COM 1 (COM 2) on the ICP

This brings up the UHF (VHF) page on the DED.

- in the scratch pad enter the frequency using the number buttons on the ICP
- press ICP Enter button

TACAN
-----

.. CAUTION::
   Make sure the MIDS LVT knob is set to ON.

- press 1 on the ICP to bring up the T-ILS page
- press ICP DCS SEQ until the DED reads TCN T/R
- press ICP Data Control Switch DOWN to select the TACAN channel
- press ICP Enter button
- press the Mode button on the HSI until it reads TCN

Air-to-Air Refueling
--------------------

- enter the TACAN receiver of the fuel plane
- enter the radio frequency of the fuel plane
- call "Intent to refuel"
- once under the fuel plane, call "Ready precontact"
- fly steady under the fuel plane
- the fuel plane calls you "You're taking fuel"
- the fuel plane calls you "Transfer complete"

Navigation
----------

Instrument Landing System
-------------------------


Radar Warning Receiver
----------------------

Glossary
--------

ACM
  Air Combat Mode. FCR main mode for ranges within 10nm.

ADI
  Attitude Direction Indicator. Artificial horizon.

CRM
  Combined Radar Mode. FCR main mode for ranges beyond 10nm.

DED
  Data Entry Display. Part of the UFC.

FCR
  Fire Control Radar. FCR has two main modes: CRM and ACM.

FTIT
  Fan Turbine Inlet Temperature.

HMCS
  Helmet Mounted Cueing System.

HSI
  Horizontal Situation Indicator.

HUD
  Heads-Up Display. Part of the UFC.

ICP
  Integrated Control Panel. Part of the UFC.

ILS
  Instrument Landing System.

MFD
  Multi-Function Display.

PFLD
  Pilot Fault List Display.

RPM
  Rotations Per Minute.

RWR
  Radar Warning Receiver.

RWS
  Range-While-Search. Radar mode of operation under CRM.

SAM
  Situational Awareness Mode.
  
SOI
  Sensor Of Interest.

STT
  Single Target Track.

TWS
  Track-While-Scan. Radar mode of operation under CRM.
  
UFC
  Up-Front Control. The UFC comprises the ICP, DED, and HUD.

