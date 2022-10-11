Light Discipline
================

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

