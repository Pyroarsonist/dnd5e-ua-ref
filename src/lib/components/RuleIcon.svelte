<script lang="ts">
	export let icon: string;
	export let size: string = 'big';

	const classMap = { big: 'h-14 w-14', small: 'h-8 w-8' };
	const className = classMap[size] ?? classMap?.big;

	const icons = {
		'acid': IconGameIconsAcid,
		'acrobatic': IconGameIconsAcrobatic,
		'anatomy': IconGameIconsAnatomy,
		'angel-outfit': IconGameIconsAngelOutfit,
		'anvil-impact': IconGameIconsAnvilImpact,
		'anvil': IconGameIconsAnvil,
		'archer': IconGameIconsArcher,
		'archery-target': IconGameIconsArcheryTarget,
		'arm-sling': IconGameIconsArmSling,
		'armor-downgrade': IconGameIconsArmorDowngrade,
		'armor-upgrade': IconGameIconsArmorUpgrade,
		'axe-swing': IconGameIconsAxeSwing,
		'backstab': IconGameIconsBackstab,
		'ball-glow': IconGameIconsBallGlow,
		'bandage-roll': IconGameIconsBandageRoll,
		'bed': IconGameIconsBed,
		'beer-stein': IconGameIconsBeerStein,
		'bleeding-eye': IconGameIconsBleedingEye,
		'bleeding-heart': IconGameIconsBleedingHeart,
		'blindfold': IconGameIconsBlindfold,
		'blood': IconGameIconsBlood,
		'boar': IconGameIconsBoar,
		'body-balance': IconGameIconsBodyBalance,
		'bolt-spell-cast': IconGameIconsBoltSpellCast,
		'bone-knife': IconGameIconsBoneKnife,
		'bookmark': IconGameIconsBookmark,
		'boots': IconGameIconsBoots,
		'bow-arrow': IconGameIconsBowArrow,
		'brain': IconGameIconsBrain,
		'breastplate': IconGameIconsBreastplate,
		'broken-axe': IconGameIconsBrokenAxe,
		'broken-shield': IconGameIconsBrokenShield,
		'broken-tablet': IconGameIconsBrokenTablet,
		'camp-cooking-pot': IconGameIconsCampCookingPot,
		'campfire': IconGameIconsCampfire,
		'cavalry': IconGameIconsCavalry,
		'cave-entrance': IconGameIconsCaveEntrance,
		'caveman': IconGameIconsCaveman,
		'coma': IconGameIconsComa,
		'compass': IconGameIconsCompass,
		'conversation': IconGameIconsConversation,
		'convince': IconGameIconsConvince,
		'cooking-pot': IconGameIconsCookingPot,
		'cow': IconGameIconsCow,
		'cracked-shield': IconGameIconsCrackedShield,
		'crafting': IconGameIconsCrafting,
		'crossbow': IconGameIconsCrossbow,
		'crossed-sabres': IconGameIconsCrossedSabres,
		'crossed-swords': IconGameIconsCrossedSwords,
		'dead-eye': IconGameIconsDeadEye,
		'dead-head': IconGameIconsDeadHead,
		'decapitation': IconGameIconsDecapitation,
		'despair': IconGameIconsDespair,
		'diablo-skull': IconGameIconsDiabloSkull,
		'dice-twenty-faces-one': IconGameIconsDiceTwentyFacesOne,
		'dice-twenty-faces-twenty': IconGameIconsDiceTwentyFacesTwenty,
		'discussion': IconGameIconsDiscussion,
		'disintegrate': IconGameIconsDisintegrate,
		'dodging': IconGameIconsDodging,
		'domino-mask': IconGameIconsDominoMask,
		'dragon-head': IconGameIconsDragonHead,
		'drama-masks': IconGameIconsDramaMasks,
		'drowning': IconGameIconsDrowning,
		'dungeon-gate': IconGameIconsDungeonGate,
		'dwarf-face': IconGameIconsDwarfFace,
		'embrassed-energy': IconGameIconsEmbrassedEnergy,
		'empty-hourglass': IconGameIconsEmptyHourglass,
		'engagement-ring': IconGameIconsEngagementRing,
		'extra-lucid': IconGameIconsExtraLucid,
		'eye-shield': IconGameIconsEyeShield,
		'eyelashes': IconGameIconsEyelashes,
		'fairy': IconGameIconsFairy,
		'falling': IconGameIconsFalling,
		'feather': IconGameIconsFeather,
		'fireball': IconGameIconsFireball,
		'flame': IconGameIconsFlame,
		'flower-pot': IconGameIconsFlowerPot,
		'flying-shuriken': IconGameIconsFlyingShuriken,
		'folded-paper': IconGameIconsFoldedPaper,
		'footprint': IconGameIconsFootprint,
		'fossil': IconGameIconsFossil,
		'goblin-head': IconGameIconsGoblinHead,
		'grab': IconGameIconsGrab,
		'guitar': IconGameIconsGuitar,
		'halberd': IconGameIconsHalberd,
		'hammer-nails': IconGameIconsHammerNails,
		'hand-saw': IconGameIconsHandSaw,
		'hand': IconGameIconsHand,
		'harpoon-trident': IconGameIconsHarpoonTrident,
		'health-capsule': IconGameIconsHealthCapsule,
		'health-normal': IconGameIconsHealthNormal,
		'hearing-disabled': IconGameIconsHearingDisabled,
		'heart-bottle': IconGameIconsHeartBottle,
		'heart-shield': IconGameIconsHeartShield,
		'heavy-arrow': IconGameIconsHeavyArrow,
		'hiking': IconGameIconsHiking,
		'holy-grail': IconGameIconsHolyGrail,
		'holy-symbol': IconGameIconsHolySymbol,
		'hood': IconGameIconsHood,
		'hooded-assassin': IconGameIconsHoodedAssassin,
		'hooded-figure': IconGameIconsHoodedFigure,
		'ice-bolt': IconGameIconsIceBolt,
		'ice-spell-cast': IconGameIconsIceSpellCast,
		'id-card': IconGameIconsIdCard,
		'ifrit': IconGameIconsIfrit,
		'imp': IconGameIconsImp,
		'imprisoned': IconGameIconsImprisoned,
		'internal-injury': IconGameIconsInternalInjury,
		'invisible': IconGameIconsInvisible,
		'journey': IconGameIconsJourney,
		'juggler': IconGameIconsJuggler,
		'jump-across': IconGameIconsJumpAcross,
		'knapsack': IconGameIconsKnapsack,
		'knockout': IconGameIconsKnockout,
		'koala': IconGameIconsKoala,
		'leapfrog': IconGameIconsLeapfrog,
		'leather-vest': IconGameIconsLeatherVest,
		'letter-bomb': IconGameIconsLetterBomb,
		'lift': IconGameIconsLift,
		'lightning-bow': IconGameIconsLightningBow,
		'lightning-slashes': IconGameIconsLightningSlashes,
		'lightning-trio': IconGameIconsLightningTrio,
		'lockpicks': IconGameIconsLockpicks,
		'magic-hat': IconGameIconsMagicHat,
		'magic-lamp': IconGameIconsMagicLamp,
		'magic-swirl': IconGameIconsMagicSwirl,
		'magnifying-glass': IconGameIconsMagnifyingGlass,
		'manacles': IconGameIconsManacles,
		'master-of-arms': IconGameIconsMasterOfArms,
		'meal': IconGameIconsMeal,
		'meat-cleaver': IconGameIconsMeatCleaver,
		'minions': IconGameIconsMinions,
		'mountain-climbing': IconGameIconsMountainClimbing,
		'move': IconGameIconsMove,
		'riposte': IconGameIconsRiposte,
		'extra-time': IconGameIconsExtraTime,
		'slap': IconGameIconsSlap,
		'silenced': IconGameIconsSilenced,
		'world': IconGameIconsWorld,
		'broad-dagger': IconGameIconsBroadDagger,
		'skills': IconGameIconsSkills,
		'switch-weapon': IconGameIconsSwitchWeapon,
		'spell-book': IconGameIconsSpellBook,
		'minotaur': IconGameIconsMinotaur,
		'talk': IconGameIconsTalk,
		'stairs': IconGameIconsStairs,
		'night-vision': IconGameIconsNightVision,
		'nun-face': IconGameIconsNunFace,
		'octogonal-eye': IconGameIconsOctogonalEye,
		'ogre': IconGameIconsOgre,
		'old-wagon': IconGameIconsOldWagon,
		'one-eyed': IconGameIconsOneEyed,
		'open-book': IconGameIconsOpenBook,
		'orc-head': IconGameIconsOrcHead,
		'paint-brush': IconGameIconsPaintBrush,
		'painted-pottery': IconGameIconsPaintedPottery,
		'path-distance': IconGameIconsPathDistance,
		'person': IconGameIconsPerson,
		'perspective-dice-five': IconGameIconsPerspectiveDiceFive,
		'perspective-dice-four': IconGameIconsPerspectiveDiceFour,
		'perspective-dice-one': IconGameIconsPerspectiveDiceOne,
		'perspective-dice-six-faces-five': IconGameIconsPerspectiveDiceSixFacesFive,
		'perspective-dice-six-faces-four': IconGameIconsPerspectiveDiceSixFacesFour,
		'perspective-dice-six-faces-one': IconGameIconsPerspectiveDiceSixFacesOne,
		'perspective-dice-six-faces-random': IconGameIconsPerspectiveDiceSixFacesRandom,
		'perspective-dice-six-faces-six': IconGameIconsPerspectiveDiceSixFacesSix,
		'perspective-dice-six-faces-three': IconGameIconsPerspectiveDiceSixFacesThree,
		'perspective-dice-six-faces-two': IconGameIconsPerspectiveDiceSixFacesTwo,
		'perspective-dice-six': IconGameIconsPerspectiveDiceSix,
		'perspective-dice-three': IconGameIconsPerspectiveDiceThree,
		'perspective-dice-two': IconGameIconsPerspectiveDiceTwo,
		'pierced-body': IconGameIconsPiercedBody,
		'plasma-bolt': IconGameIconsPlasmaBolt,
		'poison-bottle': IconGameIconsPoisonBottle,
		'poison-gas': IconGameIconsPoisonGas,
		'poison': IconGameIconsPoison,
		'pool-dive': IconGameIconsPoolDive,
		'potion-ball': IconGameIconsPotionBall,
		'progression': IconGameIconsProgression,
		'psychic-waves': IconGameIconsPsychicWaves,
		'pull': IconGameIconsPull,
		'push': IconGameIconsPush,
		'quake-stomp': IconGameIconsQuakeStomp,
		'rally-the-troops': IconGameIconsRallyTheTroops,
		'relic-blade': IconGameIconsRelicBlade,
		'ring-box': IconGameIconsRingBox,
		'robber': IconGameIconsRobber,
		'rock-golem': IconGameIconsRockGolem,
		'rolling-dices': IconGameIconsRollingDices,
		'round-shield': IconGameIconsRoundShield,
		'run': IconGameIconsRun,
		'rune-stone': IconGameIconsRuneStone,
		'saber-and-pistol': IconGameIconsSaberAndPistol,
		'saber-slash': IconGameIconsSaberSlash,
		'sands-of-time': IconGameIconsSandsOfTime,
		'screaming': IconGameIconsScreaming,
		'scroll-quill': IconGameIconsScrollQuill,
		'semi-closed-eye': IconGameIconsSemiClosedEye,
		'shaking-hands': IconGameIconsShakingHands,
		'shard-sword': IconGameIconsShardSword,
		'sharp-axe': IconGameIconsSharpAxe,
		'sharp-smile': IconGameIconsSharpSmile,
		'shield': IconGameIconsShield,
		'shining-sword': IconGameIconsShiningSword,
		'shotgun': IconGameIconsShotgun,
		'sleepy': IconGameIconsSleepy,
		'smart': IconGameIconsSmart,
		'smitten': IconGameIconsSmitten,
		'snatch': IconGameIconsSnatch,
		'sonic-screech': IconGameIconsSonicScreech,
		'spell-book': IconGameIconsSpellBook,
		'spiked-armor': IconGameIconsSpikedArmor,
		'spoted-flower': IconGameIconsSpotedFlower,
		'sprint': IconGameIconsSprint,
		'squid-head': IconGameIconsSquidHead,
		'star-pupil': IconGameIconsStarPupil,
		'stone-axe': IconGameIconsStoneAxe,
		'stone-crafting': IconGameIconsStoneCrafting,
		'stone-pile': IconGameIconsStonePile,
		'stone-sphere': IconGameIconsStoneSphere,
		'strong': IconGameIconsStrong,
		'sunbeams': IconGameIconsSunbeams,
		'sundial': IconGameIconsSundial,
		'sunken-eye': IconGameIconsSunkenEye,
		'surprised': IconGameIconsSurprised,
		'sword-hilt': IconGameIconsSwordHilt,
		'sword-wound': IconGameIconsSwordWound,
		'telepathy': IconGameIconsTelepathy,
		'third-eye': IconGameIconsThirdEye,
		'tinker': IconGameIconsTinker,
		'tired-eye': IconGameIconsTiredEye,
		'tombstone': IconGameIconsTombstone,
		'torch': IconGameIconsTorch,
		'treasure-map': IconGameIconsTreasureMap,
		'ultrasound': IconGameIconsUltrasound,
		'wax-seal': IconGameIconsWaxSeal,
		'wine-glass': IconGameIconsWineGlass,
		'wizard-face': IconGameIconsWizardFace,
		'wizard-staff': IconGameIconsWizardStaff,
		'woman-elf-face': IconGameIconsWomanElfFace,
		'wood-club': IconGameIconsWoodClub,
		'wool': IconGameIconsWool,
		'worried-eyes': IconGameIconsWorriedEyes,
		'yin-yang': IconGameIconsYinYang
	};
</script>

<svelte:component this={icons[icon]} class="{className} p-1" />
