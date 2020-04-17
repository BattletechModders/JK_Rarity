Version 1.5.1.0

This was originally part of the JK_Variants mod, but I am going to break it out as a separate function, as I have received multiple requests to make it work with the other existing New 'Mech skins and mods.

IMPORTANT NOTE: 
BT1_4_MadlibsFix is no longer required - if you have an older version of this mod, please delete the "BT1_4_MadlibsFix" folder.

Also, I suggest you delete you Battletech/Mods/.modtek folder when you install this mod.


What does it do?
The idea behind this mod is to add Faction Rarity Tags to every 'Mech and Vee in the game, in JK_Variants and in other mods. These tags are then used in new LanceDef files that will call for a mix of tag values.

This makes the various 'Mech/Vee variants become more/less prevalent for the various factions. So, something like the Panther will appear more frequently for a Kurita lance, but that same Panther would be Rare elsewhere - so, instead an Urbie might appear for a similar Liao lance.


How do I install it?
This mod relies on BTML / ModTek - as long as you have those, you can download the attached "Encounters.zip", then unzip and drop all 3 mod folders into the Battletech/Mods/ folder.

This includes:
Z_JK_AppearanceDates - this folder includes tags for the appearance year of various 'Mechs and Vehicles.  This should prevent them from appearing prior to their cannon dates when active.
Z_Sab_JK_RarityTables - this folder includes the lancedefs & tags for vanilla, Flashpoint DLC, JK_Variants & then multiple subfolders for all the wonderful work done by BloodyDoves, GentlePayload, Colo/MattyXR, SolahmaJoe, Dialcaliper and Haree78

Note: in the Z_Sab_JK_RarityTables, there are multiple options for the JSON.  Currently there are only files in the base folder  (which cover 3025 rarity), 3039 folder and the userAdded folder (this includes various homebrew or non-standard named 'Mechs/Vees).  In time, the 3050 folder will also be populated.  When those folders are activated, they will overwrite the older tags (where appropriate), so the folders should be applied in the order the relative JSON shows.


Does it work with Vanilla?
Yes, it does, but with the limited choices in the pure vanilla mode, you will see a LOT of the same common 'Mechs for each faction. As more 'Mechs are added to the game, the field expands further allowing for more core game variety in the lances.


Does it work with other 'Mech/Vee mods?
As mentioned at the start, this was originally designed to work with the JK_Variants mod (which adds 75+ new 'Mech variants and 55+ new Vehicle variants to the existing chassis), but during the testing, there was interest expressed in expanding the viable candidates to things like the Bloody Doves' 'Mechs, SolahmaJoe's 'Mechs and Colo's work (), Dr Banzai's Helm Core Resurgence is on the horizon (many new variants using upgraded tech) and the 3025 Extended mod.

NOTE : I do not include any of these mods in the file, they must be downloaded individually. This mod will ONLY modify the Tags for the various MechDef_ files that it finds.

Adding in these extra mods will expand the potential pool that the LanceDefs draw from, giving each Faction an even more distinct feel.

The mods currently covered:
@bloodydoves : All 3025 era 'Mechs
@SolahmaJoe :  All 3025 era 'Mechs
@MattyXR / Colo :  All 3025 era 'Mechs
@GentlePayload :  All 3025 era 'Mechs
@DialCaliper : SLDF Royals
@Haree78 : 3025 Extended

That being said, since the current era is 3025-ish, some of the variants in the above mods are not era appropriate and receive a None tag across the board, essentially BLACKLISTING them from randomly appearing.


Does it make the game harder?
It will make certain achievements difficult, like gathering the Chassis Collection bonuses. It also changes the force disposition for the lances (based on faction availability), which may lead to facing 'tougher' or 'easier' adversaries based on the available models.


How does it work?
The Rarity of the 'Mechs/Vees (and all their variants) was determined by referencing the XOTL Rarity Tables that are used for the tabletop BT game. They are slightly adjusted to account for salvage from neighboring powers and occasionally adjusted to fill gaps in the available variants / chassis.  However, for the most part, the values are a close match.

The values range through :
Common - Prevalent model, all but guaranteed to see these. However, these are excluded as targets in the 'Solo' lances (usually used for the solo 'Mech you may have to kill).
Uncommon - For the purpose of this mod, these are usually called along with Common, though it is a possibility in the 'Solo' lance.
Rare - You will see these, but they will be limited to no more than half the lance typically.
Very Rare - These tend to show up in the full skull missions rather than the half levels.
Ext Rare - Right now these are restricted to potentially appearing in just the Solo lances.
None - This should prevent the model from appearing at all for the chosen Faction(s).
Hero - This is only called in special missions, as these are 1 off character / hero variants.

The LanceDef files will then look to make a lance that consists of a mix of those values by using a combination of Inclusion and Exclusion Tags that are then appended with the Opposing Force's Faction name.

For example, a 1/2 Skull Mission might call for a Mixed Light Battle Lance (Vees and 'Mechs)

Normally this would call:
2 Light Vehicles
1 Medium Vehicle
1 Light Mech (Tank)

By setting the Exclusions to exclude "Rare, Very Rare, Ext Rare and None " for the two lights, this will force the choices on the two lights to be Common/Uncommon for that faction.

Then by setting the Exclusions to exclude " Very Rare, Ext Rare and None " for the medium and 'Mech, it opens the choices to allow the Medium Vee & Light 'Mech to be Common/Uncommon/Rare for that faction with the Light 'Mech also having the Tank Tag.


I Don't Like MyFavoriteMech™ to be Very/Ext Rare or Unavailable - what can I do?
If you want to change the Rarity of a particular model (or models), you just navigate to the relevant mechdef_ file in this Mod's folders (not the original mod) and open it up, then change to a value you find more suitable.

You can use this to tweak things to your liking, to increase or decrease rarity levels if you aren't using all the variants out there.