---
id: q7fsg8qiq6rovg1z8176pg1
title: Rclone
desc: ''
updated: 1673946900151
created: 1673946897658
---

# Initialising

`sudo apt-get install curl`  

`curl https://rclone.org/install.sh | sudo bash`

## Backing up to Google Drive

### Start RClone

`rclone config`

### Make a new remote

`n`

### Name it something you can remember(you'll use this in near future)

`gdrive`

### Choose Google Drive

`15` (prolly)


## Google Setup

### Google Application Client ID - [RClone Docs](https://rclone.org/drive/#making-your-own-client-id)

### Google Application Secret 

### Scope of Access

`1`

### Folder ID

https://drive.google.com/drive/u/3/folders/XXXX 

Folder ID is **XXXX**

### Service Account
` press enter - blank `

(If you're on a headless machine, in auto config Choose NO)


## Command to Execute after the Remote Setup is done

DRY RUN
`rclone copy "/srv/airtime/stor/imported/1" "gdrive-server:FolderNameYouChoose" --dry-run --progress -V --transfers 40 --checkers 10 --contimeout 60s --timeout 300s --retries 3 --low-level-retries 10`

Final
`rclone copy "/srv/airtime/stor/imported/1" "gdrive-server:MainBackup" --progress --verbose --transfers 40 --checkers 10 --contimeout 60s --timeout 300s --retries 3 --low-level-retries 10`
