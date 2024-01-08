---
title: Windows Post-Install Script for Gaming
date: 2023-01-16 13:31:35
lastmod: 2024-01-08 09:24:53
categories:
  - 
tags:
  - batch
aliases: 
share: true
---

# Windows Post-Install Script for Gaming

## Sources

Source : [Browse the winget repository - winstall](https://winstall.app/)

## Scrips

### Core Game Launchers

```
winget install --id=Valve.Steam -e
winget install --id=EpicGames.EpicGamesLauncher -e
```

### Other Stuff

```
winget install --id=GOG.Galaxy -e
winget install --id=ElectronicArts.EADesktop -e
winget install --id=Ubisoft.Connect -e
```

### Nvidia Specific

```
winget install --id=TechPowerUp.NVCleanstall  -e
```

Only check :

- Check `Disable Installer Telemetry & Advertising`
- Check `Perform a Clean Installation`

### Mouses

#### Logitech Specific

```
winget install --id=Logitech.GHUB  -e
```

#### Razer Specific

```
winget install --id=RazerInc.RazerInstaller -e 
```

### MSI GL75 Specifics

```
winget install --id=SteelSeries.GG  -e
```

- [How to Fix a Slow Upload Speed with a Killer E2400 Gigabit Ethernet Controller]({{< ref "How to Fix a Slow Upload Speed with a Killer E2400 Gigabit Ethernet Controller" >}})
