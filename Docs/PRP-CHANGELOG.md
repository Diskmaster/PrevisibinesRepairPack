This document superceeds the old bugtracker document and is intended to more significantly document the bugfixes provided by the PRP project and review the accumulated fixes since and what they do at a glance.

Last known major release for PRP: 74
Last known major release for UFO4P: 2.1.7

Previsibines Repair Pack Changelog - All entries are noted by FormID where applicable.

00001

-- All new records have to be here for the process to work as expected.

00002
- BillboardTallCherryBomb2Scholt01 [MSWP:001C33DD]
-- As reported by DoubleYou, the material reference in the material swap has a spelling error that cannot be fixed without a precombine rebuild, and PRP accounts for this.

00003
- PRP_PicketFenceB_PW_GateOpen01_PretoPost [MSWP:XX000800]
- [REFR:000981EC] (places PicketFenceB_PW_GateOpen01 [STAT:00125C69] in GRUP Cell Temporary Children of WestEverettEstatesExt [CELL:0000DAE8] (in Commonwealth "Commonwealth" [WRLD:0000003C] at 3,10) in Precombined\0000DAE8_1F475F65_OC.nif)
- Textures\SetDressing\Fences\PaintedWoodWhiteDirty01_d,n,s.dds
- Materials\SetDressing\Fences\PaintedWoodWhiteDirty01.BGSM
-- Marvesly reported a picket fence piece that had an odd texture choice compared to it's brethren, and we discovered that it didn't have a postwar texture swap. Thundra654 created one on our behalf and the matswap has been applied to the gate in West Everett Estates as that's the only reference requiring the swap.

00004
- [REFR:000C980B] (places MetalBaseA1x1CorWin01Full01 [SCOL:000FB099] in GRUP Cell Temporary Children of CambridgeMassChemical01 "Mass Chemical" [CELL:000A3AD4] in Precombined\000A3AD4_136F4A76_OC.nif)
- [REFR:000C98E6] (places MetalBaseA1x1CorWin01Full01 [SCOL:000FB099] in GRUP Cell Temporary Children of CambridgeMassChemical01 "Mass Chemical" [CELL:000A3AD4] in Precombined\000A3AD4_32488570_OC.nif)
- PRP_CambridgeSCOL_BluetoRed [MSWP:XX000800]
-- Two referenced building block meshes in Cambridge's Mass Chemical interior had a strange blue colorant that looked out of place that can't be fixed without the correct material swap. The swap had to be created explicitly as it didn't exist in the game, but the material file is used in other swaps of this nature.

00005
- 001D0AE3 ExtRubble_Plain_Sm_Mid05
- 001D0B36 ExtRubble_Plain_Sm_Mid05
- 001D0B46 ExtRubble_Plain_Med_High02
- xx004C52 PRP_ExtRubblePlaintoDebrisGroundNoAlpha
-- Originally, a trio of rubble was discovered to have holes in them that weren't supposed to be there, and we thought that they had the wrong material file (AFK32322) but then later on, the realization that the material file was also assigned to other meshes (AFK32590) (AFK32691) so a new material swap needed to be made to get around the issue as the correct no alpha mat is already in the game, just not hooked up to a matswap.

00006 
- xx004C53 PRP_CarCoupe01_Static_Swap_GlassFix
- xx004C54 PRP_CarCoupe02_Static_Swap_GlassFix
- xx004C55 PRP_CarCoupe03_Static_Swap_GlassFix
- xx004C56 PRP_CarCoupe04_Static_Swap_GlassFix
- xx004C57 PRP_CarCoupe05_Static_Swap_GlassFix
- xx004C58 PRP_VertibirdUnderwaterFix
- xx004C59 PRP_CarUnderwaterFix
- 
-- Implementation of the changes from the (Underwater Glass Fix)[https://www.nexusmods.com/fallout4/mods/58671] mod, though adjustments were made to account for precombined material swaps, as the original mod didn't think to setup individual static entries for the swaps and had to be remade accordingly.

00007
- xx004C5A BillboardPRP_CollectionIdent
           Materials\SetDressing\Signage\BillboardSignPRP.BGSM
-- Intended to allow for replacement of the nearest billboard to the Vault 111 entrance for collection users to better identify installs with.

- xx004C5B PRP_CompatQuests
           Scripts\PRP\DisableObjectIfModExists.pex
		   Scripts\Source\User\PRP\DisableObjectIfModExists.psc
-- A Story Manager Branch Node needed to setup the Creation Club specific detections and dynamic disables implemented to handle them. Also include the compiled script itself and source.

00008
- xxxxxxx PRPUtilityCell
  xxxxxxx PRP_HeavyFlamerCustomizationEnable etc
-- Setup for the dynamic ref disables for CC detection and include the actually disabled refs as needed.

00009
00010
-- Reserved slots.

00011
-- CroupManor01 (2 Duplicate Refs)

00012
-- PrewarVault111 (2 Duplicate Refs, Adapt (Vault 111 Floor Fix)[https://www.nexusmods.com/fallout4/mods/28167] 's changes, but actually apply them to the actual references to fix z-fighting)

00013
-- Malden Drainage (1 Duplicate Ref)

00014
-- DLC04BottlingPlant01 (284 Duplicate Refs)

00015
-- DLC04BottlingPlant01 (Correct z-pos for a set of debris to fix z-fighting and also adjust the position of a wall chunk to better fit.

00016
-- CambridgeMassChemical01 (Fix the chimney block's bad placement and exclude an IndustrialMachine07 reference that wasn't occluding well. I need to go back and recheck this one.)

00017
-- Switchboard (1 Duplicate Ref)

00018
-- DLC03VimPopFactory01 (2 Duplicate Refs, moved a wall and bookshelf to stop it clobbering a nearby door.

00019
-- CharlestownHouse01 (1 Duplicate Ref)

00020
-- BeaconHillApartments (3 Duplicate Refs)

00021
-- BADTFL01 (5 Duplicate Refs)

00022
-- BeantownBrewery01 (4 Duplicate Refs, one of which is a BlackWireSpline01, UFO4P could pick up this fix)

00023
-- MassStateHouse01 (70 Duplicate Refs)

00024
-- ConcordFactory (1 Duplicate Ref)

00025
-- ConcordSpeakeasy (5 Duplicate Refs)

00026
-- BostonPublicLibrary01 (3 Duplicate Refs)

00027
-- RelayTowerInt15A (1 Duplicate Ref)

00028
-- ShawHighSchool01 (5 Duplicate Refs)

00029
-- DLC03NucleusCommandCenter01 (5 Duplicate Refs)

00030
-- LaytonTowers01 (2 Duplicate Refs, adjust a trio of stairs to make Umbra play nice)

00031
-- LaytonTowers01 (001bed90, 0015d9b8: Wrong overhead lamp type used, was clipping through the ceiling or floating free in the air, imported from UFO4P)

00032
-- DLC01Lair01 (295 Duplicate Refs)

00033
-- MassFusion02 (1 Duplicate Ref)

00034
-- DLC03Vault118 (A pair of cameras needed to be flipped around on their Z axis to resolve a visual bug. Imported from UFO4P, bug 25794)

00035
-- DLC03Vault118 (5 Duplicate Refs)

00036
-- DLC03PineCrestCavern01 (1 Duplicate Ref)

00037 (Dumbass, you named the plugin wrong, fix it)
-- ParsonsState01 (3 Duplicate Refs)

00038
-- Financial13 (1 Duplicate Ref)

00039
-- DLC01FortHagenSatelliteArray01 (7 Refs marked XLRT, all crates, to get around occlusion generation issues in that interior)

00040
-- InstituteConcourse (2 Duplicate Refs)

00041
-- CollegeSquare01 (4 Duplicate Refs)

00042
-- FensStreetSewer01 (9 Duplicate Refs, 1 Ref move to cover up a hole)

00043
-- DLC04NukaWorldPowerPlant01 (11 Duplicate Refs, 1 Ref moved to fix z-fighting)

00044
-- DLC04WWMineCart01 (3 Duplicate Refs)

00045
-- ConcordCivicAccess01 (1 Duplicate Ref)

00046
-- PickmanGallery01 (7 Duplicate Refs)

00047
-- SaugusIronworks01 (7 Duplicate Refs)

00048
-- BostonPublicLibrary02 (5 Duplicate Refs, two ref moves)

00049
-- DLC04BradbertonsOffice01 (3 Duplicate Refs)

00050
-- FortStrong01 (1 Duplicate Ref)

00051
-- ArcjetSystems01 (9 Duplicate Refs, 1 Adjustment to fix z-fighting)

00052
-- DLC03FarHarborLastPlank (5 Duplicate Refs)

00053 needs layer assign past this point
-- DLC03EagleCoveTannery01 (2 Duplicate Refs)

00054 
-- Vault114 (4 Duplicate Refs, 4 Adjustments for umbra and z-fighting)

00055
-- DLC03BeaverCreekLanes01 (2 Duplicate Refs)

00056
-- RevereBeachStation01 (11 Duplicate Refs)

00057
-- Financial06 (2 Duplicate Refs)

00058
-- DLC04HubPackLair (1 Duplicate Ref)

00059
-- TheBigDig01 (15 Duplicate Refs)

00060
-- GoodneighborTheThirdRail (2 Duplicate Refs)

00061
-- SuperDuperMart01 (1 Duplicate Ref)

00062
-- SentinelSite01 (2 Duplicate Refs)

00063
-- FederalRationStockpile01 (5 Duplicate Refs, 3 Refs to fix seams, and a ref to fix z-fighting)

00064
-- FaneuilHall01 (3 Duplicate Refs, 2 refs needed moved to fix previs issues)

00065
-- FortHagen01 (3 Duplicate Refs)

00066
-- DmndSecurity01 (2 Refs needed excluded for previs fixes, one table moved and fix the correct matswap in the ceiling)

00067
-- EastBostonPrep01 (5 Duplicate Refs)

00068
-- PrydwenHull01 (7 Duplicate Refs)

00069 REVIEW ACTI CHANGE
-- DLC04GZVaultTec01 (9 Duplicate Refs, one moved railway activator for reasons I don't remember)

00070
-- TheCastle01 (2 Duplicate Refs)

00071
-- ArcjetSystems02 (1 Duplicate Ref)

00072
-- Wattz01 (3 Duplicate Refs)

00073, 00074 (update UFO4P number 73 -> 74)
-- GoodneighborBobbisPlace (1 Duplicate Ref, 2 reference moves as per UFO4P Bug 20310)

00075
-- FraternalPost11501 (6 Duplicate refs, 1 Persistent ref move that otherwise clobbers a picture frame?)

00076
-- DLC03FringeCoveDocks01 (REVIEW)

00077
-- DLC04TransitCenter01 (1 Duplicate Ref)

00078
-- PrydwenHull03 (1 Duplicate Ref)

00079
-- CambridgeKendallHospital01 (11 Duplicate Refs)

00080
-- WarehouseIndustrialMachines (2 Duplicate Refs)

00081
-- CambridgePD01 (1 Duplicate Ref)

00082
-- MiltonGeneral01 (10 Duplicate Refs)

00083
-- DLC04GZNukaGalaxy (21 Duplicate Refs)

00084
-- ConcordMuseum01 (18 Duplicate Refs, 3 Stair block moves to fix a tiny hole that lets you see into the void)

00085
-- GoodneighborOldStateHouse (2 Duplicate Refs)

00086
-- REObject02Interior (1 Duplicate Ref)

00087
-- GNN01 (6 Duplicate Refs)

00088
-- HubrisComics01 (6 Duplicate Refs)

00089
-- WaldenPond01

00090
-- PoseidonEnergy01 (10 Duplicate Refs)

00091
-- PoseidonEnergy02 (3 Duplicate Refs)

00092
-- AndrewStation01 (5 Duplicate Refs, 2 Refs that need grounded to the floor)

00093
-- zLexingtonGarage (1 Duplicate Ref)

00094
-- zUnusedSubwayTerminalShowcase (3 Duplicate Refs)

00095
-- DLC04SafariWelcomeCenter (5 Duplicate Refs)

00096 REVIEW
-- zVitalePumphouse (5 Ref moves, inherited from UFO4P bug 20283)

00097
-- DLC04HubFizztopMountainInterior01 (2 Duplicate Refs)

00098
-- GoodneighborTheMemoryDen (1 Duplicate Ref, 1 Ref moved to fix z-fighting)

00099
-- HestersRobotics01 (1 Duplicate Ref)

00100
-- DmndOutfieldShengsHouse01 (2 Duplicate Refs)

00101
-- MedfordMemorial01 (8 Duplicate Refs, 4 Refs got moved to fix z-fighting and placement issues)

00102
-- Vault81 (fill me in, I did stuff here related to the suit CC changes)

00103
-- UFOCrashSite01 (1 Duplicate Ref)

00104
-- Theater16PearwoodResidences01 (4 Duplicate Refs, 2 Previs Fixes)

00105
-- Waterfront02 (2 Duplicate ref)

00106
-- EsplanadeChurch01 (1 Duplicate Ref)

00107 UPSTREAM NEW RECORD
-- MassFusion01 (14 Duplicate Refs, 1 Z-fighting Fix, 1 New ref that needs upstreamed)

00108
-- InstituteAdvSystems (1 Duplicate Ref)

00109
-- Vault81Secret (fill me in, more work was done here)

00110
-- CambridgePolymerLabs01 (5 Duplicate Refs, 4 Bookcases moved to address wall z-fighting)

00111
-- InstituteReactor (1 Duplicate Ref)

00112 REVIEW
-- USSConstitution01 (1 Duplicate Ref, 1 ref move to resolve a previs issue)

00113
-- InstituteTunnel01 (6 Duplicate Refs, 1 position fix and a scaling change to address bad pipe placement)

00114
-- GwinnettBrewery01 (6 Duplicate Refs)

00115
-- DLC04SafariReptileHouse (1 Duplicate Ref)

00116 A trio of SCOLs were excluded previously in response to strangeness in the cell, needs reviewed.
-- Vault11402 (1 Duplicate Ref)

00117
-- DLC04HubOperatorLair01

00118
-- zLexingtonApartments (1 Duplicate Ref, 9 Ref Adjustments to tighten up placement seams)

00119
-- DLC04BottlingPlant02 (1 Duplicate Ref)

00120
-- SandyCovesHome01 (2 Duplicate Refs)

00121
-- MahkraFishpacking01 (1 Duplicate Ref)

00122 A metric fuckton of work (342 records) that needs to be recorded in more detail.
-- Vault75

00123
-- DLC04GZTheater01 (2 Duplicate Refs)

00124
-- DmndArturosHouse01 (1 Duplicate Ref)

00125
-- FourLeafFishpacking01 (4 Duplicate Refs, and moved a Barnacle)

00126
-- RailroadHQ01 (4 Duplicate Refs)

00127
-- TrinityChurch01 (1 Duplicate Ref)

00128
-- BostonCommon02 (1 Duplicate Ref)

00129
-- GlowingSeaPOIDB06Int (5 Duplicate Refs, one Duplicate Activator)

00130
-- CambridgeEastCITRaiderCamp01 (1 Duplicate Ref)

00131
-- TheaterMassBayMedicalCenter02 (1 Duplicate Ref)

00132
-- SouthBoston25 (3 Duplicate Refs)

00133
-- GeneralAtomicsGalleria01 (4 Duplicate Refs)

00134
-- zUnusuedGrenades (1 Duplicate Ref)

00135
-- TheaterMassBayMedicalCenter01 (2 Duplicate Refs)

00136
-- DLC03NucleusSubInterior01 (10 Duplicate Refs)

00137
-- BackStreetApparel01 (2 Duplicate Refs, 2 corrected refs to fix debris z-fighting)

00138
-- Waterfront12 (2 Duplicate Refs)

00139
-- Financial28 (1 Duplicate Ref, 5 corrected refs to fix z-fighting, including one UFO4P placement fix)

00140
-- InstituteOldRobotics01 (1 Duplicate Ref)

00141
-- zUnusedFinancial23 (2 Duplicate Refs)

00142
-- GwinnettBrewery02 (Moved a pair of barnacles)

00143
-- Financial14 (1 Duplicate Ref)

00144
-- DmndCitySurplus01New (1 Duplicate Ref)

00145
-- ShamrockTaphouse01 (1 Duplicate Ref)

00146
-- FensBank01 (1 Duplicate Ref)

00147
-- FortHagen02 (2 Duplicate Refs, 1 New Ref (HitDebrisPileCeiling03, copied to 00001 plugin)

00148
-- UniversityPoint01 (3 Duplicate Refs, 1 ref adjusted for z-fighting?)

00149
-- zInstituteRotunda (5 Duplicate Refs)

00150
-- WarrenTheater01 (1 Duplicate Ref)

00151
-- DLC04Gauntlet01 (5 Duplicate Refs)

00152
-- InstituteFEVlab (2 Duplicate Refs)

00153 CHECKPOINT - Blk7 SubBlk0 - 342CB
-- RelayTowerInt12 (NEW ROOM MARKER?! Was I drunk?)