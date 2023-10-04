Folder Structure
================

DCS lives in three locations:

- the *setup folder* relative to the Steam library folder ``...\steamapps\common\DCSWorld``
- the *work folder* relative to the user folder ``...\Saved Games\DCS``
- the *Tacview folder* relative to the user folder ``...\Documents\Tacview``

Setup and Work Folder
---------------------

.. Warning::

   The setup folder should never be altered. To install a skin, kneeboard, or mod alter only the work folder.

================ ===========
Folder           Description
================ ===========
API
Bazar
bin
bin-mt
Config
CoreMods         alternative modification folder
Data
DemoMods         alternative modification folder
Doc
dxgui
FUI
JConfHtml
I10n
Kneeboard        custom kneeboard images
Liveries         custom livery textures
LuaSocket
MissionEditor
Mods             modification folder
Mods\\aircraft   aircraft (like Bronco or A4-E Skyhawk)
Mods\\campaigns  campaigns comprised of missions
Mods\\characters
Mods\\services   utilities (like SRS)
Mods\\tech       buildings, vehicles, and ships
Mods\\terrains   maps
Scripts          Lua scripts that make up DCS's scripting environment including the initialization script ``MissionScripting.lua`` but also scripts for extensions (like Tacview or Volanta)
Sounds.edc
WebGUI
================ ===========

Tacview Folder
--------------

This folder holds the Tacview recordings in ``.acmi`` format.
