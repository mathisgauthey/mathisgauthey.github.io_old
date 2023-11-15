---
title: How to Automatically Back-up All Your Github Repo and Archive Them
date: 2023-11-14 15:29:00
lastmod: 2023-11-15 10:44:28
categories:
  - guide
tags:
  - script
  - bash
  - github
  - archive
aliases: 
share: true
---

# How to Automatically Back-up All Your Github Repo and Archive Them

## Goals

1. Clone all our repositories.
2. Archive them to their respective `folderName.zip`
3. Delete the repository folders

## Requirements

- Linux, git-bash on windows, well basically you need to be able to run bash script.
- [Github CLI](https://github.com/cli/cli#installation) → Access to the repo list and clone using https login.
- [parallel](https://www.gnu.org/software/parallel/) → Parallelize code to reduce execution time.
- [[p7zip [Wiki ubuntu-fr]|p7zip]] → Archive the cloned repository.

## The Script

You'll just need to input your account username in line `2` of the script.

You can find it here :`https://github.com/USER`

The script will clone and archive the repositories in the `current folder`.

```bash
# Cloning all the repositories from a profile
gh repo list USER --limit 1000 --json nameWithOwner --jq '.[].nameWithOwner' | \
   parallel -j16 gh repo clone

# Function to archive and remove subfolders
archive_and_remove() {
  local subfolder="$1"
  local subfolder_name="${subfolder%/}"

  # Archive the subfolder to its own ZIP file
  7z a -tzip "${subfolder_name}.zip" "$subfolder_name"

  # Remove the original subfolder
  rm -rf "$subfolder_name"
}

# Export the function to make it available to parallel
export -f archive_and_remove

# Use find to get a list of subfolders and pipe it to parallel
find . -maxdepth 1 -type d -exec basename {} \; | \
  parallel -j16 archive_and_remove
```
