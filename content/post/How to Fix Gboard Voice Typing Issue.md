---
title: How to Fix Gboard Voice Typing Issue
date: 2023-12-01 14:03:00
lastmod: 2023-12-01 14:14:51
categories:
  - guide
tags:
  - android
  - voice-typing
aliases: 
share: true
---

# How to Fix Gboard Voice Typing Issue

## Introduction

If you ever had issues with voice typing on Gboard like starting voice input and speaking but nothing writes down. But sometimes it works and you don't understand why.

But why does it happen ? Well, it turns out it only happens to people using :

- At least two languages on their keyboard.
- Have `Multilingual typing` options activated in their keyboards.

## Fix

Without any more talking, the ultimate fix for me was to make sure that :

> My first keyboard language on Gboard was the same as my Android display language.

That's it. Now it detects my voice correctly, in English or French. But I can't start typing in one language and switch midway through, I need to actually type on the voice recording once again.

**Always try force stopping Gboard, then clearing its cache, then rebooting your phone after each method.**

## Other Possible Fixes

One could also try :

- Deactivate `multilingual typing`, and manually switch to the right language before activating voice input.
- Deactivating the second language on your Gboard.
- Some users reported going inside `Voice typing` options and unticking `Faster voice typing` helped. It helped on reboot but started happening again on my end.
- Some user reported uninstalling the Google Assistant app on your phone if you have a Google Pixel phone, as it is already bundled in your phone.

Sources :

- [gBoard voice typing not working properly | XDA Forums](https://xdaforums.com/t/gboard-voice-typing-not-working-properly.4572165/)
- [Question - Gboard's Assistant voice typing is jacked | XDA Forums](https://xdaforums.com/t/gboards-assistant-voice-typing-is-jacked.4520341/)
