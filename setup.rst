Setup
=====

This section shows how to set up your Dangerous Waters game so that you can join multiplayer events with the unit.

To follow these instructions you need to know the location of the game files. By default, Steam stores the Dangerous Waters game files under::

  Programs (x86)/Steam/steamapps/common/Dangerous Waters

Windows 8/10 Compatibility
--------------------------

Out of the box, Dangerous Waters crashes on current Windows versions.

`subsim.com <https://www.subsim.com/radioroom/showthread.php?t=223629>`_ provides a fix to this problem. The download link on this page contains a file ``d3d8.dll``. Copy it to your game folder.

Resolution
----------

By default, Dangerous Waters is set to an 800x600 resolution although 1250x1024 is the highest possible resolution. It is impossible to set the resolution in-game since the game crashes when you try.

Edit the file ``dangerouswaters.ini`` located in the game folder. In the ``[Graphics]`` section on line 27 find the entry ``.ModeID`` which defaults to ``1`` by default. Set it to ``3``.

LwAmi Mod
---------

LuftWolf and Amizaur (LwAmi)'s weapons and sensors realism mod increases the realism of Dangerous Waters.

Download the mod from `subguru.com <http://subguru.com/downloads.html>`_. The archive contains an executable ``LwAmi_308_Full.exe``. When you run it the installer asks for the location of the game files. After the installation finishes a dialog opens where you can select the mods to activate. You need only ``LwAmi_Mod``. All other components are cosmetic.

You can reopen the mod selection menu by running the executable ``JSGME.exe`` that the installer creates in the game directory.

Multiplayer with Hamachi
------------------------

To play Dangerous Waters in multiplayer, we use a Virtual Private Network (VPN). `Hamachi <https://vpn.net/>`_ allows to set up a VPN on Windows. Install Hamachi and create an account. Hamachi creates a virtual network adapter that allows access to a simulated Local Area Network (LAN). By default, Dangerous Waters uses the first network adapter it finds to host and find multiplayer sessions which is not the Hamachi network adapter.

Edit the file ``dangerouswaters.ini`` located in the game folder. In the ``[MultiPlayer]`` section on line 167 find the entry ``.AdapterName`` which defaults to ``"IPv4"``. Set it to ``"Hamachi - IPv4"``.

