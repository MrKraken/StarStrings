# MrKraken's String Replacements
### (English) Community Translated .ini for **Star Citizen [Build: sc-alpha-4.7.0_live_11518367]**

# Includes
- Contracts that award blueprints have the potential pool added to the end of the description
  - Not perfect, but if you want to *search* for contracts/blueprints instead [SCMDB by 🥑Krovax](https://scmdb.net/) can help
- Contracts that award BP's have `[BP]` in the title
  - `[BP]*` for contracts with shared text and only a specific one awards, which is stated in description
- Warning prefixes for illegal substances
- Componenet Type/Size/Grade prefixed to the name (eg.  )
- Hephaestanite (Raw) shortened to Heph (Raw)
- Hauling contract titles cleaned up and Direct underlined
- Reformatted the Mining guide journal entry to group ores by rarity
 - nb. I have not verified that the source journal entry is in any way accurate. It looks like it's still using 4.6 information....
- Type notation prefix for missiles (Thanks to WhisperDark in Discord for suggestion)
  - Eg. `Dominator II Missile` -> `[EM] Dominator II Missile`

If you want to use bits from different translation packs you've found, check out [BeltaKoda's web based tool](https://beltakoda.github.io/StarMeld/)

> With thanks to [SaltEMike](https://www.twitch.tv/saltemike) for the joking idea that I ran with... [Check out his video here](https://youtu.be/K5yBt55NljE)

>[!NOTE]
> Based once again on the wonderful Language Pack idea by [ExoAE](https://github.com/ExoAE/ScCompLangPack/tree/main).

> [!WARNING]
> You will need to maintain this file in order to keep strings up-to-date with each new build/patch that modifies strings. I have an automation setup to push new versions live but please keep in mind that I am UK based and PTU builds normally go up very late UK time, so there may be a few hours delay

# Known Constraints/Unfixable Problems
- Because of how some contracts share strings, there's some 'odd' looking behaviour that I've tried to show cleanly with `*` in titles marked with BP and then caveat text in the description. (I'm trying to keep this to an automated find/conditional replace operation so I don't need to manually maintain)
- Some contracts like Black Box recovery literally share the same assigned strings across mission givers
- Rayari "Need More Research Data" is a generic description/title re-used for many different contracts, most not awarding blueprints.
  - The title shows [BP] but I have added a caveat that it's for Yormandi Eyes Only
# Installation
1. Download the latest release on the right hand side
2. Extract the ZIP file.
3. If you already have a user.cfg file, do not overwrite it. Instead, open your existing user.cfg and add the following line at the end `g_language = english.`
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
- The ability to customise your localisation using the extracted global.ini file is intended/authorised by CIG to support community made translations until it is officially integrated
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
