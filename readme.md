# MrKraken's String Replacements
### (English) Community Translated .ini for **Star Citizen [Build: sc-alpha-4.10.0_ptu_12368639]**
##  ⚠️ You **need** to check for an update to this file every patch ⚠️
> [!CAUTION]
> Not officially endorsed or approved by CIG. Considered a 3rd party contribution: Use at your own discretion. Further information below.

> [!WARNING]
> I don't recommend using custom strings on PTU as each new build will likely add new strings, this will result in you seeing blank contracts & "missing" text. I try to update ASAP after a build but it's not always possible.
# Changes Included
### Contracts
- Contracts that award blueprints have the potential pool added to the end of the description
  - Not perfect, but if you want to *search* for contracts/blueprints instead [SCMDB by 🥑Krovax](https://scmdb.net/) can help
- Contracts that award BP's have `[BP]` in the title
  - `[BP]*` for contracts with shared text and only a specific one awards, which is stated in description
  - Also attempted to add some clarity to rank based contracts (like covalex hauling) due to issues with shared titles by adding the required rank name for the version of the contract that awards BP's
  - For the same reason, and for regional variations of pools awarded, there can be 2 lists showing.
    - I've attempted to display these as cleanly as possible, but with it being an automated process there's only so much I can do.
    - Certain contracts (Like Tactical Strike Groups) have 2 pools that award on completion
  - Contracts with component blueprints in their pool show Name (Type) eg. `SnowBlind (Cooler)`
  - Pools that only award at certain rep ranks should now *mostly* display what level they award at (it's complicated)
    - Eg. Covalex - only awards at Master rank, but all the ranks re-use the same string keys with formatting: `Covalex_HaulCargo_AToB_title=~mission(ReputationRank) Rank - Direct ~mission(CargoGradeToken) Cargo Haul`
- Hauling contract title overhaul
  - Direct now underlined
  - Extra 'wordyness' removed
  - To → From locations added (with thanks to WayfinderDrax for the idea)
- Contracts that award scenario progress (Eg. Return of Xenothreat) show how many points & if they are split
- Added reputation award amount to all contracts (title & description)
- Added asteroid RS values to scanning contract objectives
### Mining
- Hephaestanite (Raw) shortened to Heph (Raw)
- Mining UI text shortened to avoid crossover with values
- Any `item_commodities_raw_` entry that begins "Raw ..." will now be suffixed (Raw) instead
### Items
- Warning prefixes `[!]` for illegal substances
- Componenet Type/Size/Grade prefixed to the name
  - Eg. `Tundra` → `Mil/1/D Tundra`
- Type notation prefix for missiles (Thanks to WhisperDark in Discord for suggestion)
  - Eg. `Dominator II Missile` → `[EM] Dominator II Missile`
- Reduced verbosity of Pyro MultiTool attachment names (so they don't scroll when using customise)
  - Eg. `TruHold Tractor Beam Attachment` → `Tractorbeam`
### Journal
- Reformatted the Mining guide journal entry to group ores by rarity
  - nb. I do not verify that the source journal entry is in any way accurate.
- Added some QoL quick tips to the Refuelling Guide

If you want to use bits from different translation packs you've found, check out [BeltaKoda's web based tool](https://beltakoda.github.io/StarMeld/)

> With thanks to [SaltEMike](https://www.twitch.tv/saltemike) for the joking idea that I ran with... [Check out his video here](https://youtu.be/K5yBt55NljE)

>[!NOTE]
> Based once again on the wonderful Language Pack idea by [ExoAE](https://github.com/ExoAE/ScCompLangPack/tree/main).


# Known Constraints/Unfixable Problems
- Because of how some contracts share strings, there's some 'odd' looking behaviour that I've tried to show cleanly with `*` in titles marked with BP and then caveat text in the description. (I'm trying to keep this to an automated find/conditional replace operation so I don't need to manually maintain)
- Some contracts like Black Box recovery literally share the same assigned strings across mission givers
  - This may just be a quirk of the mission generator and how it's pulled out, a much more involved fix than just the string replacer
- Rayari "Need More Research Data" is a generic description/title re-used for many different contracts, most not awarding blueprints.
  - The title shows [BP] but I have added a caveat that it's for Yormandi Eyes Only
# Installation
1. Download the [latest release ](https://github.com/MrKraken/StarStrings/releases/tag/latest)on the right hand side
2. Extract the ZIP file.
3. If you already have a user.cfg file, do not overwrite it. Instead, open your existing user.cfg and add the following line at the end `g_language = english`
4. Copy the data folder and the (user.cfg) file into your game’s LIVE folder root.
5. Launch the game! 

```
StarCitizen/
└── LIVE/
    ├── user.cfg
    └── data/
        └── Localization/
            └── english/
                └── global.ini
```
> [!WARNING]
> This is done by find/replace operations based on extracted game data and it would be an almight task to manually check each contract personally, if you find any errors please let me know via the Issues tab. 

> [!IMPORTANT]
> **Made by the Community** - This is an unofficial Star Citizen fan project, not affiliated with the Cloud Imperium group of companies. All content in this repository not authored by its host or users are property of their respective owners.
- The ability to customise your localisation using the extracted global.ini file is intended/authorised by CIG to support community made translations until it is officially integrated. *As this is adding information to an existing, official language, they can ask me to cease distributing it at any time.*
    - *[Star Citizen: Community Localization Update](https://robertsspaceindustries.com/spectrum/community/SC/forum/1/thread/star-citizen-community-localization-update) 2023-10-11*
- Considered as third-party contributions, use at your own discretion
- [RSI Terms of Service](https://robertsspaceindustries.com/en/tos)
- [Translation & Fan Localization Statement](https://support.robertsspaceindustries.com/hc/en-us/articles/360006895793-Star-Citizen-Fankit-and-Fandom-FAQ#h_01JNKSPM7MRSB1WNBW6FGD2H98)

>[!NOTE]
> To sanity check & debug why some contracts had multiple pools when it looked like there shouldn't be, Claude was used to look over the files & parser, turns out there are regional variations in Pyro 🤷‍♂️


<div id="badges">
  <a href="https://www.youtube.com/@Mrkraken">
    <img src="https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="https://x.com/RealMrKraken">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
  <a href="https://ko-fi.com/realmrkraken"><img src="https://img.shields.io/badge/Ko--fi-F16061?logo=ko-fi&logoColor=white&style=for-the-badge"></a>
</div>
