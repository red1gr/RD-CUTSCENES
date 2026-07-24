# RD-CUTSCENES

[![GitHub Forks](https://img.shields.io/github/forks/red1gr/rd-cutscenes?style=for-the-badge)](https://github.com/red1gr/rd-cutscenes/network)
[![GitHub Issues](https://img.shields.io/github/issues/red1gr/rd-cutscenes?style=for-the-badge)](https://github.com/red1gr/rd-cutscenes/issues)
[![GitHub License](https://img.shields.io/github/license/red1gr/rd-cutscenes?style=for-the-badge)](LICENSE)

A CURATED COLLECTION OF GRAND THEFT AUTO V CUTSCENE NAMES.

THIS REPOSITORY PROVIDES A COMPREHENSIVE LIST OF GTA V CUTSCENE IDENTIFIERS FOR FIVEM, SCRIPTHOOKV, MODDING TOOLS, CINEMATIC EDITORS, AND OTHER DEVELOPMENT PROJECTS.

> ## WARNING
>
> THIS REPOSITORY CONTAINS **ONLY CUTSCENE NAMES**.
>
> NO SCRIPTS, GAME ASSETS, AUDIO, MODELS, OR ROCKSTAR GAMES FILES ARE INCLUDED.

---

## FEATURES

- HUNDREDS OF GTA V CUTSCENE NAMES
- EASY TO SEARCH
- ORGANIZED REFERENCE LIST
- USEFUL FOR CINEMATIC DEVELOPMENT
- COMPATIBLE WITH FIVEM, SCRIPTHOOKV, AND OTHER GTA V PROJECTS
- CONTINUOUSLY UPDATED

---

## EXAMPLE CUTSCENES

<p align="center">
    <img src="https://i.ytimg.com/vi/1X66xeFg5wE/maxresdefault.jpg" width="31%">
    <img src="https://i.ytimg.com/vi/mye8Sw3gsdQ/maxresdefault.jpg" width="31%">
    <img src="https://i.ytimg.com/vi/PpLrAefy9pM/maxresdefault.jpg" width="31%">
</p>

<p align="center">
<b>AH_1_INT</b> - <b>ABIGAIL_MCS_2</b> - <b>APA_FIN_CEL_APT3</b>
</p>

IMAGES ABOVE ARE PROVIDED AS VISUAL EXAMPLES ONLY AND ARE **NOT INCLUDED** IN THIS REPOSITORY.

---

## EXAMPLE CUTSCENE NAMES

```text
ABIGAIL_MCS_1_CONCAT
ABIGAIL_MCS_2
AC_IG_3_P3_B
AH_1_EXT_T6
AH_1_INT
AH_1_MCS_1
AH_2_EXT_ALT
APA_FIN_CEL_APT3
BARRY_1_MCS_1
BARRY_3A_MCS_2
BARRY_3B_MCS_1
BARRY_3C_MCS_3
CARSTEAL_1_GARDEN
CHINESE1
CHOP
DRF_1
EPS_4
FAM_5_MCS_6
FINALE_A
JEWEL_STORE_HEIST
MICHAEL_TOWN
...
```

MORE CUTSCENE NAMES WILL BE ADDED AS THEY ARE DISCOVERED.

---

## USAGE

THIS REPOSITORY CAN BE USED FOR:

- FIVEM RESOURCES
- SCRIPTHOOKV PROJECTS
- SINGLEPLAYER MODS
- CINEMATIC EDITORS
- ANIMATION TOOLS
- DEVELOPMENT UTILITIES
- DOCUMENTATION
- RESEARCH

---

## LUA EXAMPLE

```lua
-- PLAYS A CUTSCENE USING ITS INTERNAL GTA V NAME.
-- NAME: GTA V CUTSCENE IDENTIFIER.
-- DURATION: OPTIONAL DURATION IN MILLISECONDS.

function PlayCutsceneByName(name, duration)
    RequestCutscene(name, 8)

    local timeout = 0

    while not HasCutsceneLoaded() and timeout < 100 do
        Citizen.Wait(100)
        timeout = timeout + 1
    end

    if not HasCutsceneLoaded() then
        print(("FAILED TO LOAD CUTSCENE: %s"):format(name))
        return false
    end

    StartCutscene(0)

    print(("STARTED CUTSCENE: %s"):format(name))

    if duration then
        Citizen.Wait(duration)
        StopCutsceneImmediately()
    else
        while IsCutscenePlaying() do
            Citizen.Wait(100)
        end
    end

    RemoveCutscene()

    print(("FINISHED CUTSCENE: %s"):format(name))

    return true
end

-- EXAMPLE
PlayCutsceneByName("AH_1_INT")
```

---

## WHY THIS REPOSITORY?

GTA V CUTSCENE NAMES ARE OFTEN SCATTERED ACROSS FORUMS, OLD DOCUMENTATION, OR DECOMPILED FILES.

THIS PROJECT COLLECTS THEM INTO A SINGLE, EASY-TO-SEARCH REFERENCE FOR DEVELOPERS, MODDERS, AND THE GTA V COMMUNITY.

---

## CONTRIBUTING

WE WELCOME CONTRIBUTIONS.

IF YOU DISCOVER MISSING CUTSCENE NAMES, FIND INCORRECT ENTRIES, NOTICE DUPLICATES, OR WANT TO IMPROVE THE DOCUMENTATION, PLEASE OPEN AN ISSUE OR SUBMIT A PULL REQUEST.

---

## LICENSE

THIS PROJECT IS LICENSED UNDER THE **APACHE LICENSE 2.0**.

SEE THE [LICENSE](LICENSE) FILE FOR MORE INFORMATION.


## SUPPORT & CONTACT

- ISSUES:  [GITHUB ISSUES](https://github.com/red1gr/rd-weapons/issues)
- CONTACT: [SUPPORT CONTACT](mailto:mail@red1gr.dev) 

---

<p align="center">
MADE FOR THE GTA V MODDING COMMUNITY.
</p>

<p align="center">
    <img src="https://logos-world.net/wp-content/uploads/2021/02/GTA-5-Emblem.png" width="80" alt="GTA V Logo">
</p>
