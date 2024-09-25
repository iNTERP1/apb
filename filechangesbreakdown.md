File changes breakdown
In case you wish to undo some of my changes but keep others, open the relevant .ini file with your text editor of choice. There are other tiny misc optimizations/changes that will not impact your experience so I've skipped those.

The top will always be the vanilla game values and the bottom will be my edit as found in the ready-to-use files.

APB Reloaded\APBGame\Config\DefaultEngine.ini
Black Login Screen
Map=APBLoginLevel.apb
LocalMap=APBLoginLevel.apb
changed to
Map=UIDistrict_DistrictSelect.apb
LocalMap=UIDistrict_DistrictSelect.apb

Disabled Bounty Notifications (left side of the screen)
+GlobalDataStoreClasses="APBUserInterface.cUIDataStore_HUD_Ceremony"
changed to
;+GlobalDataStoreClasses="APBUserInterface.cUIDataStore_HUD_Ceremony"

Disabled Dirty Money (top left under pledged contact)
+GlobalDataStoreClasses="APBUserInterface.cUIDataStore_HUD_OpenWorld"
changed to
;+GlobalDataStoreClasses="APBUserInterface.cUIDataStore_HUD_OpenWorld"

APB Reloaded\Engine\Config\BaseEngine.ini
FPS
MinSmoothedFrameRate=22
MaxSmoothedFrameRate=100
MaxClientFrameRate=128
changed to
;bSmoothFrameRate=TRUE
;MinSmoothedFrameRate=22
MaxSmoothedFrameRate=128
MaxClientFrameRate=0

Disabled Texture Streaming (DTS)
bUseTextureStreaming=True
bUseLightingTextureStreaming=True
changed to
bUseTextureStreaming=False
bUseLightingTextureStreaming=False

Garbage Collection (GC/Stutter Fix)
TimeBetweenPurgingPendingKillObjects=60
changed to
TimeBetweenPurgingPendingKillObjects=0

Bloom
DefaultPostProcessName=APBPostEffectMaterials.APBPostEffect_Process
changed to
;DefaultPostProcessName=APBPostEffectMaterials.APBPostEffect_Process

APB Reloaded\APBGame\Config\DefaultGame.ini
Disable Muzzle Flash
m_bEnableMuzzleFlash=true
m_bEnableMagazineCasings=true
changed to
m_bEnableMuzzleFlash=false
m_bEnableMagazineCasings=false

Ragdolls
NPC/Civilian Ragdolls
m_cfg_fMinNPCRagdollDisplayTime=60.0
m_cfg_fMaxNPCRagdollDisplayTime=120.0
m_cfg_nMaxNumberOfNPCRagdolls=30
m_cfg_nHardMaxNumberOfNPCRagdolls=45
m_cfg_fMinNPCRagdollDespawnDelay=10.0
changed to
m_cfg_fMinNPCRagdollDisplayTime=0.0
m_cfg_fMaxNPCRagdollDisplayTime=0.0
m_cfg_nMaxNumberOfNPCRagdolls=0
m_cfg_nHardMaxNumberOfNPCRagdolls=0
m_cfg_fMinNPCRagdollDespawnDelay=0

Player Ragdolls
m_nMaxDeadRagDollPawns=8
m_bDeathAnimations=true
changed to
m_nMaxDeadRagDollPawns=0
m_bDeathAnimations=false
