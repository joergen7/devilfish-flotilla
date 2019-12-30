Sub Standoff
============

In this tutorial you take your first steps in using the mission editor. You place two opposing submarines, give them tactics, and define winning conditions for both sides.

Select a Region
---------------

First, the mission editor prompts you to pick a region on the world map. Pick a region in the Atlantic by right-clicking. The editor faces you with a dialog where you can choose between a single mission and a campaign mission. Leave single mission selected and confirm.

.. note::

  After selecting a region the editor shows four panels. On the left is a map chart. Below it, on the bottom left, is a status bar describing the state of the editor. On the right is the scenario browser listing all items in the mission. Below it, on the bottom right, are five buttons for placing a submarine, a surface ship, a trigger, a land-based prop, or a script.

Place Two Subs
--------------

Next, place two submarines on the map chart. Click on the place submarine button and on a location on the map chart. A submarine icon appears on the map chart. The mission editor automatically selects the new submarine and shows the property editor instead of the scenario browser on the right panel. Edit the submarine's properties as follows:

================= ======================
Key               Value
================= ======================
Side              Side 0
Country           United States
Class Designation Los Angeles (688i) SSN
Name              Albany SSN753
================= ======================

Place a second sub with the following properties:

================= ==============
Key               Value
================= ==============
Side              Side 1
Country           Russia
Class Designation Project 971A K
Name              Gepard-M K335
================= ==============

The distance between the two subs should be about 10 nm.

Tactic: Random Box
------------------

Every platform needs a tactic. The random box tactic makes a platform pick random destinations inside a rectangular region, searching for contacts. Give both submarines a random box tactic. Make sure each sub starts inside the random box of the other.

Let both submarines travel at the same speed and depth.

=========== =====
Key         Value
=========== =====
Speed (kts) 5
Depth (ft)  600
=========== =====

Next, we set the Albany to target the Gepard and vice versa. For the Albany, set target mode and platform as follows:

=============== ======
Key             Value
=============== ======
Target Mode     Attack
Target Platform K 335
=============== ======

Conversely, for the Gepard, set target mode and platform as follows:

=============== =======
Key             Value
=============== =======
Target Mode     Attack
Target Platform SSN 753
=============== =======

Last, on page 2 of each platform's property list, set it as a controllable platform.

Attached Goal Triggers
----------------------

Next, we define when the scenario concludes successfully for each controllable platform.

First, we need to express that the Albany wins when it kills the Gepard. Right-click on the Gepard and select ``Add Attached Trigger``. Place the trigger somewhere on the map chart. Now, set the trigger properties as follows:

=================== ===============
Key                 Value
=================== ===============
Apply Trigger To    SSN 753
Trigger Name        T01
Trigger Type        Goal Trigger
Trigger Activation  Kill
Trigger Description Kill the Gepard
Critical            yes
=================== ===============

Next, on page 4 of the property list, define what messages to generate when the trigger fires:

=============== ================================
Key             Value
=============== ================================
Type            Report
To              Ownship / Accomplishing Platform
Text            You killed the Gepard
=============== ================================

.. note::

  The ``Report`` communication type allows a message to appear in a submarine's message box, without the submarine having to establish a link connection.

Last, on page 5 of the property list set the text that appears in the mission status report for both the unfulfilled and fulfilled goal:

===================== ================================
Key                   Value
===================== ================================
Goal Complete Message 
===================== ================================

Mission Brief
-------------