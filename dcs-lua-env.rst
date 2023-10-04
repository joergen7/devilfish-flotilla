Lua Scripting Environment
=========================

Entry Point
-----------

The entry point of the Lua scripting environment is given in the file ``Scripts\MissionScripting.lua`` in the setup folder. It performs the following tasks:

- it loads the file ``Scripts\ScriptingSystem.lua``
- it removes the modules ``os``, ``io``, and ``lfs`` from the scope
- it removes the functions ``require`` and ``loadlib`` and the table ``package`` from the scope

``Scripts\ScriptingSystem.lua``, in turn, performs the following tasks:

- it loads the files ``Scripts\Common\LuaClass.lua`` and ``Scripts\Database\db_countries.lua``
- it defines the classes ``Object``, ``SceneryObject``, ``StaticObject``, ``Unit``, ``Weapon``, ``Airbase``, ``Group``, ``Controller``, ``Spot``, and ``Warehouse``

``Scripts\Common\LuaClass.lua`` defines a Lua-based object-oriented infrastructure. In particular it defines the function ``class`` which is used to define classes like ``Object`` or ``SceneryObject``.

``Scripts\Database\db_countries.lua`` performs the following tasks:

- it defines the table(string, number) ``coalition`` with the entries NEUTRAL = 0, RED = 1, and BLUE = 2
- it defines the strings ``db_path`` and ``troopsPath``
- it defines the object ``country`` with the methods ``next``, ``add``, and ``get``


Add Script File via Editor
--------------------------

To add an external script via the mission editor a once-type trigger can be used. However, there are two methods that differ in the frequency the content of the external script file is loaded.

For both methods, perform the following steps:

- open the triggers window
- add a trigger
- type: once
- event: no event

do-script-file
^^^^^^^^^^^^^^

- add an action to the trigger
- action: do script file
- file: [external script]

.. note::
   The do-script-file method does not update the content of the external script on server start. Instead, the content of the script is cached until the trigger changes.

Use this method to load a script that does not change often, e.g., Mist or Moose.

   
do-script
^^^^^^^^^

- add an action to the trigger
- action: do script
- text:

.. code-block:: lua

   assert( loadfile( "[external script]" ))()

Use this method to load a script that changes often, e.g., a mission-related script.
