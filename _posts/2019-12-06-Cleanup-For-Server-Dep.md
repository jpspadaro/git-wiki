---
published: true
---
# Cleanup for Server Deployment

> ***UNTESTED***

```
#/bin/bash

######################################
# predeploy.sh [identifier]
# Created 12-05-19
# Updates the bundle zip file (based on contents of the bundle directory and needed scripts), then moves it to the File Server.
######################################

# Quick cleanup...
rm /Volumes/File\ Server/bundle*

# Zip up the installers and scripts
zip bundle$1.zip Scripts/run.ps1 bundle/*

# Copy it to the Server Root
cp bundle$1.zip /Volumes/File\ Server
```
