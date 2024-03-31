# CfxLua (FiveM/RedM) Lua LLS Addon LuaRC Config

***Credits to [zfbx](https://github.com/zfbx) for the diagnostics.globals***

I was browsing the web for a Lua Language Server addon for FiveM, that would support NeoVim. I didn't come across a single one that supported it out of the gate. But i found overextended's [cfxlua-vscode](https://github.com/overextended/cfxlua-vscode/) plugin, reversed how it put the config together, and figured out how to setup Lua Language Server without their vscode plugin.

## Installation

1. Download and unzip [fivem-lls-addon](https://github.com/overextended/fivem-lls-addon/) somewhere easy to refrence.
2. Create a new file called `.luarc.json` in your main directory, I put mine in the same folder as `server.cfg`
3. Add the folowing lines to your `.luarc.json`
4) Update the `fivem-lls-addon` path's to correctly point to your unzipped folder from earlier.

```json
{
  "runtime.nonstandardSymbol": [
    "/**/",
    "`",
    "+=",
    "-=",
    "*=",
    "/=",
    "<<=",
    ">>=",
    "&=",
    "|=",
    "^="
  ],
  "runtime.plugin": "fivem-lls-addon\\plugin.lua",
  "workspace.checkThirdParty": false,
  "workspace.library": [
    "fivem-lls-addon\\library\\natives\\CFX-NATIVE",
    "fivem-lls-addon\\library\\natives\\GTAV",
    "fivem-lls-addon\\library\\runtime"
  ],
  "diagnostics.globals": [
    "vim",
    "qbx",
    "require",
    "math",
    "lib",
    "GetPlayerName",
    "provide",
    "CopyToClipboard",
    "GetCamMatrix",
    "NetworkDoesEntityExistWithNetworkId",
    "GetCurrentResourceName",
    "TriggerClientEvent",
    "TriggerEvent",
    "json",
    "Citizen",
    "GetPlayerIdentifiers",
    "exports",
    "AddEventHandler",
    "RegisterServerEvent",
    "GetPlayerPing",
    "DropPlayer",
    "CancelEvent",
    "IsPlayerAceAllowed",
    "GetConvarInt",
    "GetNumPlayerIndices",
    "PerformHttpRequest",
    "GetPlayerEP",
    "GetActivePlayers",
    "GetPlayerPed",
    "TriggerServerEvent",
    "RegisterNetEvent",
    "SetPedCoordsKeepVehicle",
    "SetEntityHeading",
    "PlayerPedId",
    "GetVehiclePedIsIn",
    "GetVehicleNumberPlateText",
    "SetVehicleFuelLevel",
    "TaskWarpPedIntoVehicle",
    "IsPedInAnyVehicle",
    "NetworkResurrectLocalPlayer",
    "SetPlayerInvincible",
    "ClearPedBloodDamage",
    "GetVehiclePedIsUsing",
    "GetBlipInfoIdIterator",
    "GetFirstBlipInfoId",
    "DoesBlipExist",
    "GetBlipInfoIdType",
    "GetNextBlipInfoId",
    "DoScreenFadeOut",
    "IsScreenFadedOut",
    "GetEntityHeading",
    "SetEntityCoordsNoOffset",
    "SetEntityRotation",
    "ToFloat",
    "SetBigmapActive",
    "GetActiveScreenResolution",
    "GetPlayerSprintStaminaRemaining",
    "GetPlayerUnderwaterTimeRemaining",
    "TriggerScreenblurFadeIn",
    "TriggerScreenblurFadeOut",
    "AddReplaceTexture",
    "SetMinimapClipType",
    "GetNorthRadarBlip",
    "SetGameplayCamRelativeHeading",
    "GetGroundZFor_3dCoord",
    "IsPedSittingInAnyVehicle",
    "GetPedInVehicleSeat",
    "SetVehicleOnGroundProperly",
    "DoScreenFadeIn",
    "GetPlayerFromServerId",
    "GetEntityCoords",
    "NetworkIsSessionStarted",
    "GetEntityHealth",
    "SetEntityHealth",
    "ShutdownLoadingScreenNui",
    "SetCanAttackFriendly",
    "NetworkSetFriendlyFireOption",
    "isLoggedIn",
    "SetTextFont",
    "SetTextProportional",
    "SetTextScale",
    "SetTextColour",
    "SetTextDropShadow",
    "SetTextEdge",
    "SetTextOutline",
    "SetTextEntry",
    "AddTextComponentString",
    "DrawText",
    "SetTextCentre",
    "SetDrawOrigin",
    "DrawRect",
    "ClearDrawOrigin",
    "RequestModel",
    "HasModelLoaded",
    "CreateVehicle",
    "NetworkGetNetworkIdFromEntity",
    "SetVehicleHasBeenOwnedByPlayer",
    "SetNetworkIdCanMigrate",
    "SetVehicleNeedsToBeHotwired",
    "SetVehRadioStation",
    "SetModelAsNoLongerNeeded",
    "SetEntityAsMissionEntity",
    "DeleteVehicle",
    "SendNUIMessage",
    "vector3",
    "RequestIpl",
    "CreateThread",
    "EnableInteriorProp",
    "DisableInteriorProp",
    "SetInteriorEntitySetColor",
    "RefreshInterior",
    "SetRadarAsExteriorThisFrame",
    "Wait",
    "SetRadarAsInteriorThisFrame",
    "vec",
    "GetInteriorAtCoordsWithType",
    "IsIplActive",
    "DoesEntityExist",
    "GetGamePool",
    "PlayerId",
    "GetVehicleColours",
    "GetVehicleExtraColours",
    "GetVehicleLivery",
    "GetVehicleMod",
    "GetEntityModel",
    "GetVehicleNumberPlateTextIndex",
    "GetVehicleDirtLevel",
    "GetVehicleWheelType",
    "GetVehicleWindowTint",
    "IsVehicleNeonLightEnabled",
    "GetVehicleNeonLightsColour",
    "IsToggleModOn",
    "GetVehicleTyreSmokeColor",
    "GetVehicleModVariation",
    "SetVehicleModKit",
    "SetVehicleNumberPlateText",
    "SetVehicleNumberPlateTextIndex",
    "SetVehicleDirtLevel",
    "SetVehicleColours",
    "SetVehicleExtraColours",
    "SetVehicleWheelType",
    "SetVehicleWindowTint",
    "SetVehicleNeonLightEnabled",
    "SetVehicleNeonLightsColour",
    "ToggleVehicleMod",
    "SetVehicleTyreSmokeColor",
    "SetVehicleMod",
    "GetPedDrawableVariation",
    "server_scripts",
    "shared_scripts",
    "description",
    "game",
    "ui_page",
    "files",
    "fx_version",
    "client_scripts",
    "GetGameTimer",
    "DeleteEntity",
    "IsControlJustPressed",
    "IsPedSwimming",
    "IsEntityPlayingAnim",
    "RemoveLoadingPrompt",
    "ClearPedTasks",
    "HasStreamedTextureDictLoaded",
    "RequestStreamedTextureDict",
    "DrawSprite",
    "SetStreamedTextureDictAsNoLongerNeeded",
    "GetEntityForwardVector",
    "GetWaterHeight",
    "CreatePed",
    "SetEntityAlpha",
    "IsEntityInWater",
    "CreateObject",
    "AttachEntityToEntity",
    "GetPedBoneIndex",
    "SetEntityInvincible",
    "SetBlockingOfNonTemporaryEvents",
    "AddBlipForCoord",
    "SetBlipSprite",
    "SetBlipScale",
    "SetBlipColour",
    "SetBlipAsShortRange",
    "BeginTextCommandSetBlipName",
    "EndTextCommandSetBlipName",
    "TaskTurnPedToFaceEntity",
    "RequestAnimDict",
    "HasAnimDictLoaded",
    "TaskPlayAnim",
    "IsScreenFadedIn",
    "TaskStartScenarioInPlace",
    "RemoveAnimDict",
    "IsModelValid",
    "SetLoadingPromptTextEntry",
    "AddTextComponentSubstringPlayerName",
    "ShowLoadingPrompt",
    "AddTextEntry",
    "DisplayHelpTextThisFrame",
    "BeginTextCommandDisplayHelp",
    "EndTextCommandDisplayHelp",
    "GetPlayerServerId",
    "RegisterCommand",
    "GetPedArmour",
    "GetEntityMaxHealth",
    "DisplayRadar",
    "IsThisModelABike",
    "veh",
    "IsRadarEnabled",
    "GetVehicleLightsState",
    "GetStreetNameAtCoord",
    "GetLabelText",
    "GetNameOfZone",
    "GetStreetNameFromHashKey",
    "GetEntitySpeed",
    "GetClockMinutes",
    "GetClockHours",
    "GetIsVehicleEngineRunning",
    "PlaySound",
    "calcHeading",
    "rangePercent",
    "lerp",
    "IsPedShooting",
    "IsPlayerFreeAiming",
    "GetSelectedPedWeapon",
    "ShakeGameplayCam",
    "SetFlash",
    "IsPedOnFoot",
    "IsPedRagdoll",
    "SetPedToRagdollWithFall",
    "EnableControlAction",
    "DisableAllControlActions",
    "DrawMarker",
    "IsControlJustReleased",
    "PlaceObjectOnGroundProperly",
    "SetNuiFocus",
    "GetCamCoord",
    "openDecorateUI",
    "closeDecorateUI",
    "SetCursorLocation",
    "DeleteObject",
    "RegisterNUICallback",
    "GetClosestObjectOfType",
    "FreezeEntityPosition",
    "GetEntityRotation",
    "GetCamRot",
    "SetEntityCompletelyDisableCollision",
    "SetEntityVisible",
    "SetEntityCollision",
    "EnableAllControlActions",
    "IsDisabledControlPressed",
    "IsControlPressed",
    "SetEntityCoords",
    "GetDisabledControlNormal",
    "SetCamRot",
    "SetCamCoord",
    "CreateCamWithParams",
    "RenderScriptCams",
    "SetCamActive",
    "DestroyCam",
    "DestroyAllCams",
    "GetEntityMatrix",
    "GetModelDimensions",
    "DrawLine",
    "GetScreenResolution",
    "SetRainFxIntensity",
    "SetWeatherTypePersist",
    "SetWeatherTypeNow",
    "SetWeatherTypeNowPersist",
    "NetworkOverrideClockTime",
    "SetBlipDisplay",
    "DrawScaleformMovieFullscreen",
    "SetTimecycleModifier",
    "SetTimecycleModifierStrength",
    "ClearTimecycleModifier",
    "RequestScaleformMovie",
    "HasScaleformMovieLoaded",
    "PushScaleformMovieFunction",
    "PushScaleformMovieFunctionParameterInt",
    "PopScaleformMovieFunctionVoid",
    "GetControlInstructionalButton",
    "AddTextComponentScaleform",
    "N_0xe83a3e3557a56640",
    "BeginTextCommandScaleformString",
    "EndTextCommandScaleformString",
    "disableViewCam",
    "SetTimeout",
    "RemoveBlip",
    "getOfflinePlayerData",
    "hasKey",
    "server_export",
    "shared_script",
    "version",
    "SaveResourceFile",
    "client_script",
    "server_script",
    "LoadResourceFile",
    "StopAnimTask",
    "StartScriptFire",
    "RemoveScriptFire",
    "GiveWeaponToPed",
    "TaskPlantBomb",
    "StartParticleFxLoopedOnEntity",
    "UseParticleFxAssetNextCall",
    "ClearAreaOfProjectiles",
    "RemoveParticleFxFromEntity",
    "SetParticleFxLoopedAlpha",
    "RemoveParticleFx",
    "AddExplosion",
    "RequestNamedPtfxAsset",
    "HasNamedPtfxAssetLoaded",
    "loadParticleDict",
    "loadAnimDict",
    "DetachEntity",
    "PlaySoundFrontend",
    "SetBlipAlpha",
    "IsEntityDead",
    "OpenMazeDoor",
    "generateBusinessAccount",
    "IsObjectNearPoint",
    "dependencies",
    "SetRainLevel",
    "vector4",
    "ClearPedSecondaryTask",
    "IsEntityAttachedToAnyPed",
    "SetTextComponentFormat",
    "DisplayHelpTextFromStringLabel",
    "NetworkIsPlayerActive",
    "author",
    "games",
    "ClearAreaOfEverything",
    "IsRecording",
    "StopRecordingAndSaveClip",
    "StartRecording",
    "UpdateOnscreenKeyboard",
    "DisplayOnscreenKeyboard",
    "GetOnscreenKeyboardResult",
    "this_is_a_map",
    "data_file",
    "GetInteriorAtCoords",
    "IsValidInterior",
    "file",
    "RemoveIpl",
    "lua54",
    "AddTextEntryByHash",
    "repository",
    "dependency",
    "IsPedFatallyInjured",
    "NetworkGetEntityKillerOfPlayer",
    "GetEntityType",
    "GetPedType",
    "GetDisplayNameFromVehicleModel",
    "source",
    "RconLog",
    "IsPlayerDead",
    "GetVehiclePedIsTryingToEnter",
    "GetSeatPedIsTryingToEnter",
    "VehToNet",
    "GetVehicleMaxNumberOfPassengers",
    "GetHostId",
    "GetPlayerLastMsg",
    "EnableEnhancedHostSupport",
    "resource_type",
    "TerraingridActivate",
    "ExecuteCommand",
    "GetRegisteredCommands",
    "IsAceAllowed",
    "GetNumResources",
    "GetResourceByFindIndex",
    "GetResourceState",
    "GetNumResourceMetadata",
    "GetResourceMetadata",
    "GetResourceKvpString",
    "RegisterKeyMapping",
    "SetTextChatEnabled",
    "SetResourceKvp",
    "IsPauseMenuActive",
    "rdr3_warning",
    "GetInvokingResource",
    "GetPlayers",
    "WasEventCanceled",
    "webpack_config",
    "spawnpoint",
    "vehicle_generator",
    "map",
    "CreateScriptVehicleGenerator",
    "GetHashKey",
    "SetScriptVehicleGenerator",
    "SetAllVehicleGeneratorsActive",
    "DeleteScriptVehicleGenerator",
    "GetConvar",
    "GetInstanceId",
    "SetMapName",
    "SetGameType",
    "StopResource",
    "RconPrint",
    "StartResource",
    "vector2",
    "env",
    "quat",
    "IsModelInCdimage",
    "IsEntityVisible",
    "SetPlayerControl",
    "ClearPedTasksImmediately",
    "NewLoadSceneStart",
    "IsNewLoadSceneActive",
    "GetNetworkTimer",
    "NetworkUpdateLoadScene",
    "SetRadarZoom",
    "SetMapZoomDataLevel",
    "DrawPoly",
    "GetPedBoneCoords",
    "RemoveEventHandler",
    "GetOffsetFromEntityInWorldCoords",
    "SetBlipCoords",
    "DisableControlAction",
    "IsDisabledControlJustPressed",
    "BlockWeaponWheelThisFrame",
    "GetGameplayCamRot",
    "postal_file",
    "url",
    "SetBlipRoute",
    "SetBlipRouteColour",
    "server_only",
    "GetBlipFromEntity",
    "NetworkIsPlayerTalking",
    "AddBlipForEntity",
    "GetBlipSprite",
    "GetVehicleClass",
    "GetVehicleNumberOfPassengers",
    "IsVehicleSeatFree",
    "ShowNumberOnBlip",
    "HideNumberOnBlip",
    "SetBlipRotation",
    "SetBlipNameToPlayerName",
    "StartShapeTestRay",
    "GetShapeTestResult",
    "GetGameplayCamCoord",
    "IsEntityAVehicle",
    "IsEntityAPed",
    "IsEntityAnObject",
    "NetworkSetInSpectatorMode",
    "SetPlayerModel",
    "SetPedRandomComponentVariation",
    "SetRunSprintMultiplierForPlayer",
    "SetSwimMultiplierForPlayer",
    "SetPedAmmo",
    "SetNotificationTextEntry",
    "DrawNotification",
    "GetVehicleEngineHealth",
    "GetVehicleBodyHealth",
    "PlaySoundFromEntity",
    "SetUserRadioControlEnabled",
    "SetLocalPlayerVisibleLocally",
    "SetEveryoneIgnorePlayer",
    "SetPoliceIgnorePlayer",
    "GetControlNormal",
    "ResetEntityAlpha",
    "IsVehicleOnAllWheels",
    "GetEntityHeightAboveGround",
    "IsPedFalling",
    "IsPedStopped",
    "Timestep",
    "SetPedIntoVehicle",
    "NetworkGetPlayerIndexFromPed",
    "GetPedSourceOfDeath",
    "SetCurrentPedWeapon",
    "IsControlReleased",
    "SetVehicleLivery",
    "SetVehicleEngineOn",
    "TaskGoStraightToCoord",
    "SetPedKeepTask",
    "TaskLookAtEntity",
    "SetEntityAsNoLongerNeeded",
    "GetPedLastDamageBone",
    "SetEntityMaxHealth",
    "SetPlayerSprint",
    "SetPlayerHealthRechargeMultiplier",
    "SetPlayerHealthRechargeLimit",
    "SetPedArmour",
    "HasPedBeenDamagedByWeapon",
    "AttachCamToPedBone",
    "SetCamFov",
    "CreateCam",
    "SetPedMoveRateOverride",
    "ApplyDamageToPed",
    "IsPedSprinting",
    "IsPedRunning",
    "DisablePlayerFiring",
    "SetPedToRagdoll",
    "ClearEntityLastDamageEntity",
    "HasAnimSetLoaded",
    "RequestAnimSet",
    "SetPedMovementClipset",
    "IsPedJumping",
    "GetUsingnightvision",
    "IsPedInAnyHeli",
    "GetUsingseethrough",
    "SetTextDropshadow",
    "GetObjectOffsetFromCoords",
    "RequestScaleformMovie_2",
    "IsEntityAtCoord",
    "SetNetworkIdExistsOnAllMachines",
    "NetworkSetNetworkIdDynamic",
    "RequestAmbientAudioBank",
    "LocalPlayer",
    "IsThisModelABicycle",
    "ResetPedMovementClipset",
    "GetEntityBoneIndexByName",
    "SetVehicleDoorOpen",
    "SetVehicleDoorShut",
    "GetVehicleDoorAngleRatio",
    "GetVehicleDoorLockStatus",
    "NetworkGetEntityIsNetworked",
    "StartShapeTestLosProbe",
    "SetPauseMenuActive",
    "IsPedAPlayer",
    "SetNuiFocusKeepInput",
    "SetEntityDrawOutline",
    "GetWorldPositionOfEntityBone",
    "DeletePed",
    "vec2",
    "vec3",
    "SetRadarBigmapEnabled",
    "SetMinimapComponentPosition",
    "chat_theme",
    "GetIsTaskActive",
    "HideHudComponentThisFrame",
    "DisplayAmmoThisFrame",
    "RemoveVehiclesFromGeneratorsInArea",
    "CancelCurrentPoliceReport",
    "DistantCopCarSirens",
    "SetCreateRandomCopsOnScenarios",
    "SetCreateRandomCopsNotOnScenarios",
    "SetCreateRandomCops",
    "SetGarbageTrucks",
    "SetAudioFlag",
    "StartAudioScene",
    "SetPedModelIsSuppressed",
    "SetPedDropsWeaponsWhenDead",
    "IsPedBeingStunned",
    "SetPedMinGroundTimeForStungun",
    "EnableDispatchService",
    "GetPlayerWantedLevel",
    "SetPlayerWantedLevel",
    "SetPlayerWantedLevelNow",
    "SetPlayerWantedLevelNoDrop",
    "IsPedArmed",
    "SetPedInfiniteAmmo",
    "SetVehicleModelIsSuppressed",
    "SetScenarioGroupEnabled",
    "SetScenarioTypeEnabled",
    "SetPedConfigFlag",
    "SetPedCurrentWeaponVisible",
    "IsPedInjured",
    "GetGameplayCamRelativePitch",
    "GetGameplayCamRelativeHeading",
    "Cos",
    "Sin",
    "GetRaycastResult",
    "Cast_3dRayPointToPoint",
    "IsPedDoingDriveby",
    "GetCurrentPedWeapon",
    "GetAmmoInClip",
    "GetFollowPedCamViewMode",
    "SetGameplayCamRelativePitch",
    "SetPedHelmet",
    "SetVehicleEngineHealth",
    "GetVehicleHandbrake",
    "GetVehicleSteeringAngle",
    "GetEntityVelocity",
    "SetEntityVelocity",
    "TaskPlayAnimAdvanced",
    "SetPedComponentVariation",
    "RemoveAllPickupsOfType",
    "IsPickupWithinRadius",
    "StartNetworkedParticleFxNonLoopedAtCoord",
    "SetDiscordRichPresenceAction",
    "SetRichPresence",
    "SetDiscordRichPresenceAssetSmallText",
    "SetDiscordRichPresenceAssetSmall",
    "SetDiscordRichPresenceAssetText",
    "SetDiscordRichPresenceAsset",
    "SetDiscordAppId",
    "SetScenarioPedDensityMultiplierThisFrame",
    "SetParkedVehicleDensityMultiplierThisFrame",
    "SetPedDensityMultiplierThisFrame",
    "SetVehicleDensityMultiplierThisFrame",
    "GetVehicleCurrentGear",
    "SetVehicleForwardSpeed",
    "SetPedWeaponMovementClipset",
    "SetPedStrafeClipset",
    "SetPedStealthMovement",
    "ResetPedWeaponMovementClipset",
    "ResetPedStrafeClipset",
    "SetPedMoveAnimsBlendOut",
    "RemoveAnimSet",
    "GetFollowVehicleCamViewMode",
    "GetPedTextureVariation",
    "RestorePlayerStamina",
    "StartScreenEffect",
    "StopScreenEffect",
    "SetRelationshipBetweenGroups",
    "PlayAmbientSpeech1",
    "AttachCamToEntity",
    "IsPedUsingScenario",
    "SetScaleformMovieAsNoLongerNeeded",
    "SetNightvision",
    "SetSeethrough",
    "HideHelpTextThisFrame",
    "HideHudAndRadarThisFrame",
    "GetCamFov",
    "IsPedDeadOrDying",
    "EndTextCommandPrint",
    "AddTextComponentSubstringWebsite",
    "BeginTextCommandPrint",
    "ClearPrints",
    "EndTextCommandThefeedPostTicker",
    "BeginTextCommandThefeedPost",
    "ThefeedNextPostBackgroundColor",
    "SetEntityCanBeDamaged",
    "SetPedCanRagdollFromPlayerImpact",
    "SetPedResetFlag",
    "TaskSynchronizedScene",
    "CreateSynchronizedScene",
    "GetAnimDuration",
    "NetworkStartSynchronisedScene",
    "NetworkAddPedToSynchronisedScene",
    "NetworkCreateSynchronisedScene",
    "GetSynchronizedScenePhase",
    "NetworkConvertSynchronisedSceneToSynchronizedScene",
    "HasAnimEventFired",
    "ThefeedSetAnimpostfxColor",
    "GetScriptTaskStatus",
    "GetAnimInitialOffsetRotation",
    "GetAnimInitialOffsetPosition",
    "GetWorldRotationOfEntityBone",
    "CreateObjectNoOffset",
    "Vdist2",
    "EndScaleformMovieMethod",
    "BeginScaleformMovieMethod",
    "ScaleformMovieMethodAddParamPlayerNameString",
    "ScaleformMovieMethodAddParamInt",
    "StopCurrentPlayingAmbientSpeech",
    "SetObjectTextureVariant",
    "SetPedDefaultComponentVariation",
    "SetPedPropIndex",
    "name",
    "GetSafeZoneSize",
    "BeginTextCommandDisplayText",
    "SetTextRightJustify",
    "SetTextWrap",
    "EndTextCommandDisplayText",
    "IsThisModelAHeli",
    "IsThisModelAPlane",
    "IsThisModelABoat",
    "IsEntityInAir",
    "IsThisModelACar",
    "IsMpGamerTagActive",
    "RemoveMpGamerTag",
    "CreateMpGamerTag",
    "SetMpGamerTagName",
    "HasEntityClearLosToEntity",
    "SetMpGamerTagVisibility",
    "IsPlayerTargettingEntity",
    "SetMpGamerTagAlpha",
    "SetMpGamerTagColour",
    "SetMpGamerTagWantedLevel",
    "SetMpGamerTagHealthBarColour",
    "IsDuplicityVersion",
    "server_exports",
    "ngx",
    "jit",
    "GetResourceKvpInt",
    "SetResourceKvpInt",
    "msgpack",
    "StartFindKvp",
    "FindKvp",
    "EndFindKvp",
    "provides",
    "GetRandomIntInRange",
    "RequestCollisionAtCoord",
    "RemoveAllPedWeapons",
    "ClearPlayerWantedLevel",
    "HasCollisionLoadedAroundEntity",
    "ShutdownLoadingScreen",
    "N_0x283978a15512b2fe",
    "GetTimeDifference",
    "resource_manifest_version",
    "SetPlayerRoutingBucket",
    "SetBlipFlashes",
    "SetVehicleUndriveable",
    "WashDecalsFromVehicle",
    "GetNumberOfPedPropDrawableVariations",
    "GetNumHeadOverlayValues",
    "GetNumberOfPedTextureVariations",
    "GetNumberOfPedPropTextureVariations",
    "GetPedPropIndex",
    "GetNumberOfPedDrawableVariations",
    "DoesCamExist",
    "SetPedHeadBlendData",
    "SetPedHairColor",
    "SetPedHeadOverlay",
    "SetPedHeadOverlayColor",
    "SetPedEyeColor",
    "SetPedFaceFeature",
    "ClearPedProp",
    "GetPedPaletteVariation",
    "GetPedPropTextureIndex",
    "GetLastInputMethod",
    "GetVehicleInteriorColour",
    "GetVehicleDashboardColour",
    "IsVehicleExtraTurnedOn",
    "SetVehiclePetrolTankHealth",
    "SetVehicleFixed",
    "GetModTextLabel",
    "GetVehicleHeadlightsColour",
    "GetNumVehicleMods",
    "SetVehicleDoorsShut",
    "SetVehicleHeadlightsColour",
    "SetVehicleLights",
    "SetVehicleDashboardColour",
    "SetVehicleInteriorColour",
    "SetVehicleExtra",
    "IsDisabledControlJustReleased",
    "World3dToScreen2d",
    "GetGameplayCamCoords",
    "GetVehicleLiveryCount",
    "DoesExtraExist",
    "SetVehicleDoorsLocked",
    "AddBlipForRadius",
    "SetPedMaxTimeUnderwater",
    "SetEnableScuba",
    "IsPedInAnyBoat",
    "SetNewWaypoint",
    "SmashVehicleWindow",
    "SetVehicleDoorBroken",
    "SetVehicleTyreBurst",
    "SetVehicleBodyHealth",
    "TaskLeaveVehicle",
    "NetworkRequestControlOfEntity",
    "IsPedInMeleeCombat",
    "NetworkRegisterEntityAsNetworked",
    "IsEntityAMissionEntity",
    "GiveWeaponComponentToPed",
    "RemoveWeaponComponentFromPed",
    "SetPtfxAssetNextCall",
    "StartParticleFxLoopedAtCoord",
    "ClearAreaOfObjects",
    "SetBlipShowCone",
    "SetParticleFxLoopedColour",
    "StopParticleFxLooped",
    "GetVehicleHandlingFloat",
    "SetVehicleHandlingFloat",
    "SetVehicleHandlingField",
    "SetVehicleSteeringScale",
    "SetVehicleHandbrake",
    "LoadInterior",
    "IsInteriorReady",
    "ObjToNet",
    "NetToObj",
    "DrawScaleformMovie",
    "GetClosestVehicle",
    "TaskSetBlockingOfNonTemporaryEvents",
    "SetPedFleeAttributes",
    "SetPedCombatAttributes",
    "SetPedSeeingRange",
    "SetPedHearingRange",
    "SetPedAlertness",
    "TaskWanderStandard",
    "SetPedAsNoLongerNeeded",
    "GetClosestPed",
    "GetPlayersLastVehicle",
    "SetFocusArea",
    "SetFocusEntity",
    "GetGameplayCamFov",
    "TaskRappelFromHeli",
    "PointCamAtEntity",
    "PushScaleformMovieFunctionParameterFloat",
    "SetVehicleSearchlight",
    "IsVehicleModel",
    "CastRayPointToPoint",
    "ShowHeadingIndicatorOnBlip",
    "IsVehicleTyreBurst",
    "Vdist",
    "PulseBlip",
    "PrepareAlarm",
    "StartAlarm",
    "StopAllAlarms",
    "SetTextJustification",
    "GetVehicleModelNumberOfSeats",
    "GetEntityAttachedTo",
    "IsEntityAttachedToEntity",
    "TaskVehicleTempAction",
    "HasEntityCollidedWithAnything",
    "PointCamAtCoord",
    "SetCamActiveWithInterp",
    "TaskEnterVehicle",
    "GetEntityPlayerIsFreeAimingAt",
    "TaskStandStill",
    "AddShockingEventAtPosition",
    "ClearAllBlipRoutes",
    "ClearAreaOfVehicles",
    "SetPedCombatAbility",
    "SetPedCombatMovement",
    "SetPedCombatRange",
    "SetPedAsCop",
    "TaskVehicleDriveWander",
    "IsVehicleStopped",
    "ApplyForceToEntity",
    "SetVehicleEnginePowerMultiplier",
    "SetVehicleEngineTorqueMultiplier",
    "SetEntityMaxSpeed",
    "SetVehicleBoostActive",
    "StartParticleFxLoopedOnEntityBone",
    "NetToVeh",
    "ClearAllPedProps",
    "SetVehicleTyreFixed",
    "GetVehicleTyresCanBurst",
    "GetVehicleNumberOfWheels",
    "GetVehicleOilLevel",
    "SetVehicleOilLevel",
    "GetControlValue",
    "GetEntitySpeedVector",
    "SetVehicleBrakeLights",
    "GetEntityRoll",
    "GetVehiclePetrolTankHealth",
    "GetAmmoInPedWeapon",
    "SetPlayerCanDoDriveBy",
    "SetAmmoInClip",
    "GetMaxAmmo",
    "AddAmmoToPed",
    "TaskReloadWeapon",
    "SetPedWeaponTintIndex",
    "SetWeatherTypeOverTime",
    "SetArtificialLightsState",
    "SetArtificialLightsStateAffectsVehicles",
    "ClearOverrideWeather",
    "ClearWeatherTypePersist",
    "SetForceVehicleTrails",
    "SetForcePedFootstepsTracks",
    "SetInteriorPropColor",
    "RemoveParticleFxInRange",
    "GetPedheadshotTxdString",
    "IsNamedRendertargetRegistered",
    "ReleaseNamedRendertarget",
    "UnregisterPedheadshot",
    "HasNamedScaleformMovieLoaded",
    "PushScaleformMovieMethodParameterInt",
    "PushScaleformMovieMethodParameterString",
    "PushScaleformMovieMethodParameterButtonName",
    "PushScaleformMovieMethodParameterFloat",
    "ScreenDrawPositionEnd",
    "SetTextRenderId",
    "ScreenDrawPositionBegin",
    "SetUiLayer",
    "N_0xc6372ecd45d73bcd",
    "GetDefaultScriptRendertargetRenderId",
    "N_0x2bc54a8188768488",
    "N_0xe6a9f00d4240b519",
    "SetEntityCollision_2",
    "IsInteriorPropEnabled",
    "RegisterNamedRendertarget",
    "IsNamedRendertargetLinked",
    "LinkNamedRendertarget",
    "GetNamedRendertargetRenderId",
    "N_0x77fe3402004cd1b0",
    "PushScaleformMovieMethodParameterBool",
    "N_0x32f34ff7f617643b",
    "RegisterPedheadshot",
    "IsPedheadshotReady",
    "GetGameBuildNumber",
    "GetPlayerEndpoint",
    "SetConvar",
    "StartNetworkedParticleFxLoopedOnEntityBone",
    "SetFacialIdleAnimOverride",
    "TaskStartScenarioAtPosition",
    "CreateDui",
    "CreateRuntimeTxd",
    "GetDuiHandle",
    "CreateRuntimeTextureFromDuiHandle",
    "NativeUI",
    "ClearFacialIdleAnimOverride",
    "StartShapeTestCapsule",
    "GetPlayerIdentifier",
    "DecorSetFloat",
    "GetVehicleFuelLevel",
    "DecorGetFloat",
    "FindFirstObject",
    "FindNextObject",
    "EndFindObject",
    "DecorExistOn",
    "IsVehicleEngineOn",
    "DecorRegister",
    "GetVehicleCurrentRpm",
    "HasPedGotWeapon",
    "N_0x4e096588b13ffeca",
    "RageUI",
    "IsHudHidden",
    "ResetScriptGfxAlign",
    "DrawFrontendAlert",
    "RMenu",
    "SetControlNormal",
    "IsVehicleSirenOn",
    "CopyVehicleDamages",
    "StopSound",
    "ReleaseSoundId",
    "SetVehicleIndicatorLights",
    "DisableVehicleImpactExplosionActivation",
    "GetSoundId",
    "SetVehicleSiren",
    "DeleteResourceKvp",
    "GetResourceKvpFloat",
    "UpdateApprovedTones",
    "compatible",
    "experimental",
    "debug_mode",
    "CreateRuntimeTextureFromImage",
    "GetEntityPhysicsHeading",
    "loadscreen",
    "IsVehiclePreviouslyOwnedByPlayer",
    "IsPedGettingIntoAVehicle",
    "GetVehiclePedIsEntering",
    "dot",
    "norm",
    "GetEntityPitch",
    "DecorSetBool",
    "DecorGetBool",
    "FindFirstVehicle",
    "FindNextVehicle",
    "EndFindVehicle",
    "MumbleClearVoiceTargetPlayers",
    "CreateAudioSubmix",
    "SetAudioSubmixEffectRadioFx",
    "SetAudioSubmixEffectParamInt",
    "AddAudioSubmixOutput",
    "SetAudioSubmixEffectParamFloat",
    "MumbleSetSubmixForServerId",
    "MumbleSetVolumeOverrideByServerId",
    "MumbleAddVoiceTargetPlayerByServerId",
    "MumbleSetAudioInputDistance",
    "MumbleAddVoiceTargetChannel",
    "NetworkSetVoiceChannel",
    "MumbleClearVoiceTargetChannels",
    "MumbleIsConnected",
    "MumbleSetServerAddress",
    "MumbleSetVoiceTarget",
    "MumbleClearVoiceTarget",
    "MumbleSetAudioOutputDistance",
    "MumbleSetAudioInputIntent",
    "MumbleCreateChannel",
    "SetConvarReplicated",
    "GetPlayerRoutingBucket",
    "convar_category",
    "GetVehicleInteriorColor",
    "GetVehicleXenonLightsColour",
    "SetVehicleInteriorColor",
    "SetVehicleXenonLightsColor",
    "GetWeaponClipSize",
    "IsPrincipalAceAllowed",
    "QBShared",
    "GetPedParachuteState",
    "GetWeapontypeGroup",
    "AddStateBagChangeHandler",
    "GetPlayerFromStateBagName",
    "SetWeaponAnimationOverride",
    "ClearPedDecorations",
    "promise",
    "GetNumHairColors",
    "GetPedHairRgbColor",
    "GetPedMakeupRgbColor",
    "GetNumMakeupColors",
    "GetPedHeadOverlayNum",
    "IsCamActive",
    "IsCamInterpolating",
    "CreateCameraWithParams",
    "OpenSequenceTask",
    "CloseSequenceTask",
    "ClearSequenceTask",
    "TaskPerformSequence",
    "SendNuiMessage",
    "joaat",
    "GetPedFaceFeature",
    "GetPedHeadOverlayData",
    "GetPedHairColor",
    "GetPedHairHighlightColor",
    "IsPedMale",
    "GetPedEyeColor",
    "GetPedHeadBlendData",
    "GetPedHeadOverlayCount",
    "GetPedHeadOverlay",
    "GetPedHeadOverlayTextureIndex",
    "GetPedHeadBlendTotal",
    "GetPedHeadBlendPaletteIndex",
    "GetPedHairHighlightColor",
    "GetPedPaletteVariation",
    "GetPedHeadOverlayColor",
    "AddPedDecorationFromHashes",
    "SetPedCanLosePropsOnDamage",
    "SetIkTarget",
    "IsPedRunningMeleeTask",
    "IsPedGoingIntoCover",
    "IsPedInCover",
    "IsPedReloading",
    "IsAimCamActive",
    "AddDoorToSystem",
    "DoorSystemSetDoorState",
    "DoorSystemSetAutomaticRate",
    "DoorSystemSetHoldOpen",
    "IsDoorOpen",
    "IsDoorClosed",
    "RequestScriptAudioBank",
    "PlaySoundFromCoord",
    "ReleaseNamedScriptAudioBank",
    "GetProfileSetting",
    "GetAspectRatio",
    "TaskTurnPedToFaceCoord",
    "StopEntityAnim",
    "RemoveDoorFromSystem",
    "GetResourcePath",
    "use_experimental_fxv2_oal",
    "GetIsDoorValid",
    "NetworkGetEntityFromNetworkId",
    "GetAllVehicles",
    "NetworkGetEntityOwner",
    "NetworkGetEntityFromNetworkId",
    "GetPlayerIdentifierByType",
    "SetPedCanRagdoll",
    "RefillAmmoInstantly",
    "CreateFakeMpGamerTag",
    "GetPlayerInvincible",
    "GetVehicleClutch",
    "GetVehicleEstimatedMaxSpeed",
    "GetVehicleEngineTemperature",
    "SetVehicleIsStolen",
    "SetVehicleIsWanted",
    "SetVehicleRadioEnabled",
    "ox_lib",
    "vec4",
    "vec3",
    "vec2",
    "vec1",
    "string",
    "vector3",
    "vector2",
    "vector1",
    "vector4",
    "vector5",
    "SetVehicleWheelHealth",
    "GetVehicleWheelHealth",
    "IsVehicleWindowIntact",
    "IsVehicleDoorDamaged",
    "ClearVehicleCustomPrimaryColour",
    "ClearVehicleCustomSecondaryColour",
    "SetVehicleModColor_1",
    "SetVehicleModColor_2",
    "SetVehicleCustomPrimaryColour",
    "SetVehicleCustomSecondaryColour",
    "GetVehicleModColor_1",
    "GetVehicleModColor_2",
    "GetVehicleCustomPrimaryColour",
    "GetVehicleCustomSecondaryColour",
    "GetVehicleWheelType",
    "GetVehicleMod",
    "GetVehicleModModifierValue",
    "GetVehicleModVariation",
    "GetNumVehicleMods",
    "GetNumVehicles",
    "GetNumVehicleDoors",
    "SetVehicleDashboardColour",
    "GetVehicleDashboardColour",
    "SetVehicleWheelSize",
    "RemoveVehicleWindow",
    "SetVehicleRoofLivery",
    "SetVehicleTyresCanBurst",
    "SetDriftTyresEnabled",
    "SetParticleFxLoopedAlpha",
    "SetParticleFxLoopedColour",
    "SetParticleFxNonLoopedAtCoord",
    "SetParticleFxLoopedEvolution",
    "SetParticleFxNonLoopedAlpha",
    "SetParticleFxNonLoopedColour",
    "SetParticleFxNonLoopedOnPedBone",
    "SetParticleFxNonLoopedOnEntity",
    "StartParticleFxNonLoopedOnPedBone",
    "StartParticleFxNonLoopedOnEntity",
    "StartParticleFxNonLoopedAtCoord",
    "SetVehicleWheelWidth",
    "SetVehicleDashboardColor",
    "GlobalState",
    "SetEntityRoutingBucket",
    "SetRoutingBucketEntityLockdownMode",
    "DoesPlayerExist"
  ]
}
```
