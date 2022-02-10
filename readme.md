minetest mod Simple Skins
=========================

Mod for skin appereance change of your player in a nice tab of your inventory

Information
------------

Simple Skins is a mod that's so easy to use you'll wonder why it hasn't been
done before... Just download and start to use it in your inventory.

Must be named `simple_skins` and uses SfInv or Inventory Plus mods,
and Unified Inventory if you use lasted original (master branch)
version when available to allow players to select a skin/texture from the list.

![screenshot.png](screenshot.png)

Original forum https://forum.minetest.net/viewtopic.php?id=9100

Technical Information
---------------------

This mod its more basic and minimalis, no preview and no download/upload, management,
it target is to be light for huge servers and be minimal for better performance.

Based on Zeg9's Skins mod originally from https://github.com/Zeg9/minetest-skins/ and
with some help from PilzAdam. Also implements some minimal features backported from SkinDB
like preview (disabled by default). The preview is autogenerated (2d), unless others mods.

#### Download

You can clone this repository in your minetest mods directory or in your game.

#### Depends

* default
* sfinv (optional, autodetected)
* player_api (newer version only)
* inventory_plus (optional, autodetected)
* unified_inventory (optional, autodetected)

#### Skin management

You can download a skin from skin database, set a new skin converted
from others boxel games or create it from scrat.

* **Download a mt-skin** It uses skins from Addi's **MT-Skin-DB**
skin database, currently at http://minetest.fensta.bplaced.net/
* **Download a mc-skind** Uses minecraft 1.7 skins, for 1.8+ will need newer 5.X mt,
and some images must crop it from 64x64 to 64x32.

To download a skin mt made or mc ones, just:
1. go to the web page skin, and download it, will get you a `png` file,
2. put into the textures directory and rename it accordingly e.g `character_2.png`
3. pop into the meta directory and make a new `character_2.txt` empty file
4. fill the txt file with as described in [Structure and formats](#structure-and-formats)

If you use the skindb download tool, that already generates all
the necessary files, with the requested names and formats. https://github.com/minetest-mods/skinsdb/tree/master/updater

#### Structure and formats

Each skin is made up of at least two files, a png file and a txt file,
the "png file" is placed in the `textures` directory and
the "txt file" in the `meta` directory.

the format of the txt file is:

. ```
name = "Skin Name",
author = "author that make the skin",
. ```

Change log:
-----------

Change log:

- 1.0 - Added skin_limit setting to limit skins loaded, sanitized skin description
- 0.9 - Added Unified Inventory support (thanks Opvolger)
- 0.8 - Added player model preview when viewing formspec (Minetest 5.4 dev only)
- 0.7 - Add some error checks, improve /setskin and tweak & tidy code
- 0.6 - Updated to use Minetest 0.4.16 functions
- 0.5 - Added compatibility with default sfinv inventory, disabled /skin command for now
- 0.4 - Added /skin command to set player skin, no longer dependent on Inventory+, also /setskin command for server admin to set custom skins for player.
- 0.3 - Now works with Minetest 0.4.10+
- 0.2 - Added 3D_Armor mod compatibility
- 0.1 - Added addi's changes to highlight selected skin on list (thanks)
- 0.0 - Initial release
