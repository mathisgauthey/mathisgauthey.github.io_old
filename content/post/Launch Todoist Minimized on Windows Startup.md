---
title: Launch Todoist Minimized on Windows Startup
date: 2023-11-23 18:41:00
lastmod: 2024-01-08 09:43:02
categories:
  - guide
tags: 
aliases: 
share: true
---

# Launch Todoist Minimized on Windows Startup

```ahk
Run, %localappdata%\Programs\todoist\Todoist.exe
WinWait, ahk_exe Todoist.exe
WinClose, ahk_exe Todoist.exe
```
