---
title: Windows Post-Install Script for Gaming
date: 2023-01-16 13:31:35
lastmod: 2024-01-07 22:20:12
categories: 
tags:
  - batch
aliases: 
share: true
---

# Windows Post-Install Script for Gaming

Core :

```
winget install --id=Valve.Steam -e
winget install --id=EpicGames.EpicGamesLauncher -e
```

Others :

```
winget install --id=ElectronicArts.EADesktop -e
winget install --id=Ubisoft.Connect -e
winget install --id=GOG.Galaxy -e
```

Nvidia specific :

```
winget install --id=TechPowerUp.NVCleanstall  -e
```

Logitech specific :

```
winget install --id=Logitech.GHUB  -e
```

MSI GL75 :

```
winget install --id=SteelSeries.GG  -e
```

![How to Fix a Slow Upload Speed with a Killer E2400 Gigabit Ethernet Controller](/images/How to Fix a Slow Upload Speed with a Killer E2400 Gigabit Ethernet Controller)
