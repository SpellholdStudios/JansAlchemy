---------------------------------------------------------------------------------

Jan's Book of Brewing is a magical tome that will allow Jan to create potions
following specific recipes. Includes 8 new potions, cutscenes and scripts.
No editing is required, just import the iap and load your game with Jan,
he will have his tome and be ready to rock.


=================================================================================


Here are some descriptions and guidelines for using this package.
First, it was set for Jan automatic use, which means you dont need to use cluaconsole, edit, visit a shop or whatever, just load your game and if you have Jan around he should be set to use the scripts and will create his book (havent tested if he had his inventory full, so... avoid it if you can).
Second, as stated in the book, each brewing requires an exact amount of ingredients (being either gems -misc-, scrolls -scrl- and/or other potions -potn-. If you have a different amount of those in Jan's inventory, you'll see him screwing up the recipe. Of course more gold wont ruin it, only less gold than necessary will. Haven't tested with extra ingredients in containers.
Third, many potions are really powerful, but if you play without cheating, you'll see that acquiring the ingredients may be hard sometimes, which should balance it out somewhat, unless you start the game stocking up on ingredients.
Note: use the book in the quickslot to begin brewing, it has 3 charges per day.

Here's some precise effects of each potion:
Note: each potion should warn you when their effects expired; any potion may be used by anyone, though the effects may not be useful for everyone.

POTX01 - Potion of Battlefield lust
2 extra attacks/round
2 bonus in attack speed
4 THAC0 bonus
Protection from OPCode (THAC0 bonus)
Duration: 900

POTX02 - Mage's Draught
Spell Restore 1 of lvl 1
Spell Restore 1 of lvl 2
Spell Restore 1 of lvl 3
Spell Restore 1 of lvl 4
Spell Restore 1 of lvl 5

POTX03 - Assassin's Gift
2x backstab bonus
THAC0 set to base 0
Protection from OPCode (Backstab bonus)
Duration: 900

POTX04 - Potion of Ogre Power
Maximum damage per hit
Duration: 900

POTX05 - Potion of Mind Shield
Protection from OPCode #5   (Charm specific creature)
Protection from OPCode #76  (Feeblemindness)
Protection from OPCode #128 (Confusion/Rigid Thinking/Fear)
Protection from OPCode #24  (Horror) (Dur:600)
Protection from OPCode #45  (Stun)
Protection from OPCode #210 (Stun 90HP)
Protection from OPCode #39  (Unconsciousness)
Protection from OPCode #217 (Unconsciousness 20HP)
Protection from OPCode #19  (Intelligence Bonus)
Protection from OPCode #106 (Fail Morale)
Protection from OPCode #175 (Hold Creature Type)
Duration: 900 (except horror)

POTX06 - Magic Ward
5 bonus on all Saves
Duration: 7200 (ONE_DAY)

POTX07 - Gatekeeper
Protection from OPCode (211 is Imprisonment)
Protection from OPCode (213 is Maze)
Duration: 300

POTX08 - Heal
Current HP set to 100%



VERSION HISTORY

Version 8.1.0 (August 30, 2020)
- Added Italian translation (by ilot).

Version 8.0.0 (June 8, 2020)
- Added alchemy.ini metadata file to support AL|EN's "Project Infinity".
- Renamed Setup-Alchemy.tp2 -> alchemy.tp2 to support AL|EN's "Project Infinity".
- Replaced `AUTHOR` keyword with `SUPPORT`.
- Fixed "infer_charsets" variable name in `HANDLE_CHARSETS` function.
- Added `REQUIRE_PREDICATE` conditions to avoid installing the mod in inaccurate games.
- Added component `DESIGNATED` number and "jan_alchemy" `LABEL`.
- Added native EET compatibility.
- alchem1.baf: replaced `CreateItem` action with `GiveItemCreate` and added `DestroyGold` action. Fixed Potion of Mind Shield recipe (2 Potions of Clarity - was 1 - and 2 000 gp - was 1 000).
- Spl files: removed hard-coded spell descriptions.
- Jan's Book of Brewing spell (jalchem.spl): replaced wrong description spell with a more accurate one (was "Spell Immunity" spell description!).
- Potions updates:
	- itm files: hard-coded item unidentified names and descriptions to avoid writing them in installation process.
	- Fixed item descriptions: added missing restriction flags.
	- Fixed wrong Dispel/Resistance effects values : 3 Dispel/Bypass resistance (were 0 Natural/Nonmagical).
	- Fixed wrong duration effects values.
	- Assassin's Gift (potx03.itm):
		- Added missing Ranger and Monk restriction flags.
	- Potion of Mind Shield (potx05.itm):
		- Added missing opcode #142 (Display portrait icon): 52 (Mind Shield).
		- Added missing opcodes for a full Immunity to Confusion effects: op#267 (protection from string = 14782 Confused - 14791 Rigid Thinking), op#169 (Immunity Special Effect Icon = 2 Rigid Thinking, 47 Chaos), op#296 Protection from Specific Animation (SPCONFUS).
		- Added missing opcodes for a full Immunity to Fear effects: op#296 (Protection from Specific Animation = CDHORROR), op#240 (Remove Special Effect Icon = 36 Panic), op#106 (Morale break = 1), op#161 (Remove fear), op#23 (Reset moral), op#101 (Protection: from Opcode = 23 Reset), Added op#321 (Remove effects by resource) for EE games (a7!in13b, spwi205, spin105).
		- Added DS value (67 BUFF_PRO_EFFECTS and 106 RESIST_FEAR) for EE games (op#328).
		- Added missing opcodes for a full Immunity to Charm effects: op#296 Protection from Specific Animation (SPNWCHRM), op#267 (protection from string = 8364 Dominated - 14780 Dire charmed - 1476 14672 Charmed).
		- Added missing opcodes for a full Immunity to Hold effects: op#296 (Protection from Specific Animation = SPFLAYER, SPMINDAT), op#101 (Protection: from Opcode = 109 Paralyze, 185 Hold Creature III), op#169 (Prevent portrait icon: 13 Held), op#267 (protection from string = 14102 17404 8823 1473 915 384 340 Held).
		- Added missing opcodes for a full Immunity to Stun effects: op#169 (Immunity Special Effect Icon = 55 Stun), op#267 (protection from string = 1280 Stunned - 14013 Stun).
		- Added missing opcodes for a full Immunity to Sleep effects: op#169 (Immunity Special Effect Icon = 14 Sleep 130 Unconscious), op#267 (protection from string = 14001 Sleep - 20438 Unconscious).
		- Added missing opcodes for a full Immunity to Feeblemindedness effects: op#169 (Immunity Special Effect Icon = 48 Feebleminded).
	- Gatekeeper (potx07.itm):
		- Fixed wrong duration effects values (300 - was 360).
	- Heal (potx08.itm):
		- Removed Wizard Slayer restriction flag.
- Updated tra files for compatibility with GW_UPDATE_ITM_DESCRIPTION_TO_EE WeiDU function requirements which automatically removes usability restrictions for EE games.
- Added German WeiDU prompts.
- Updated translations (Gwendolyne and Austin).
- Updated and renamed readme file to "alchemy-readme.txt", then moved it into new "readme" folder.
- Removed useless "backup" folder.
- Reorganized mod architecture tree: created or renamed folders to sort files according to their types.
- Lower cased files.
- Included Linux and Mac Os X versions in the same package (thanks AL|EN's Infinity Auto Packager tool!).
- Added archive libiconv-1.9.2-1-src.7z with iconv licence info.
- Uploaded mod to official Spellhold Studios GitHub mirror account.

Version 7 (November 7, 2018)
- Added native BG2EE compatibility by Deratiseur.
- jan.baf: included BWP Fixpack Lollorian's Jan Tome causing magical stuckiness fix ( http://www.shsforums.net/topic/50921-jan-jansen-magic-weapon-in-use/#entry578836 ).
- Updated WeiDU installer to v246.

Version 6 (May 28, 2010)
- Fixed Russian translation.
- Updated WeiDU installer to v218.

Version 5 (25 May 2010)
- Added Russian translation by Austin & AERIE.ru Team.
- Moved Setup-Alchemy.tp2 into top mod folder.
- Updated WeiDU installer to v217.

Version 4 (December 14, 2009)
- Added French translation by SkipCool.
- Updated WeiDU installer to v212.

Version 3 (October 25, 2009)
- Added German translation by Jarl.
- Changed to `README` command.
- Updated WeiDU installer to v211.

Version 2 (April 5, 2009)
- Fixed `COMPILE` command.
- Added `VERSION` flag.
- Updated WeiDU installer to v210.

Version 1 (February 04, 2009)
- WeiDU conversion by Badgert.
- Original files provided by Bill Keegan.
