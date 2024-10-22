This document superceeds the old bugtracker document and is intended to more significantly document the bugfixes provided by the PRP project and review the accumulated fixes since and what they do at a glance.

Last known major release for PRP: 74
Last known major release for UFO4P: 2.1.7

Previsibines Repair Pack Changelog - All entries are noted by FormID where applicable. Any entry with a ! Prefacing it does not currently have a subpage as of yet or imagery.

00001 001C33DD BillboardTallCherryBomb2Scholt01
- As reported by DoubleYou, the material reference in the material swap has a spelling error that cannot be fixed without a precombine rebuild, and PRP accounts for this.
-- PluginFix BeforeImage AfterImage

00002 000981EC PicketFenceB_PW_GateOpen01
      xx004C50 PRP_PicketFenceB_PW_GateOpen01_PretoPost
	           Textures\SetDressing\Fences\PaintedWoodWhiteDirty01_d,n,s.dds
			   Materials\SetDressing\Fences\PaintedWoodWhiteDirty01.BGSM
- Marvesly reported a picket fence piece that had an odd texture choice compared to it's brethren, and we discovered that it didn't have a postwar texture swap. Thundra654 created one on our behalf and the matswap has been applied to the gate in West Everett Estates as that's the only reference requiring the swap.
-- PluginFix BeforeImage AfterImage

00003 