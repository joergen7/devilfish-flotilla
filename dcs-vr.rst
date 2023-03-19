Setting up VR in DCS
====================

In this short guide I explain how I get reasonable performance in DCS using a Meta Quest 2.

Enable ASW
----------


Quest Link
----------

Quest Link is the program that connects the VR headset with the PC. Herein it is important that the VR headset connects to the PC via the USB cable. You can also connect via wifi but this connection will result in terrible stuttering.

- in the Meta Quest interface open Settings
- select the Quest Link tab
- make sure the Quest Link switch is enabled
- press Launch Quest Link
- make sure Use Air Link is disabled
- press Launch

Start DCS in Multi-Threaded VR Mode
-----------------------------------

There are two scenarios: (i) you are a Steam user and (ii) you use the stand-alone distribution of DCS.

Steam
^^^^^

- open your Steam library
- right-click on DCS World Steam Edition [openbeta]
- select Properties...
- select the General tab
- Under Launch Options select ``Play MT Preview`` from the dropdown menu
- enter ``--force_enable_VR`` in the text field

Anytime you start DCS it will be in both VR and multi-threaded mode.

Stand-Alone
^^^^^^^^^^^

- open the ``DCSWorld`` folder in the file explorer
- navigate to the folder ``bin-mt``
- right-click ``DCS.exe`` and select Create shortcut
- right-click the newly created shortcut and alter the Target entry to read::
  
    "C:\...\DCSWorld\bin-mt\DCS.exe" --force_enable_VR

- move the shortcut to your desktop or preferred location


Graphics Settings
^^^^^^^^^^^^^^^^^

.. list-table:: Graphics Settings
   :widths: 25 25
   :header-rows: 1
				 
   * - Name
     - Setting
   * - Textures
     - Medium
   * - Terrain Textures
     - Low
   * - Civ. Traffic
     - OFF
   * - Water
     - Medium
   * - Visib Range
     - Medium
   * - Heat Blurr
     - OFF
   * - Shadows
     - Flat Only
   * - Blur Flat Shadows
     - OFF
   * - Secondary Shadows
     - OFF
   * - Resolution
     - 1280x768
   * - Monitors
     - 1 Screen
   * - Res. of Cockpit Displays
     - 512
   * - MSAA
     - OFF
   * - Depth of Field
     - OFF
