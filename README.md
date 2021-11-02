[![Session Ubuntu](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-ubuntu.yml/badge.svg)](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-ubuntu.yml) 
[![Session Mac](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-mac.yml/badge.svg)](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-mac.yml) 
[![Session Win](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-win.yml/badge.svg)](https://github.com/gridai-actions/gridai-session/actions/workflows/unittest-win.yml)

Run on Grid.ai and download artifacts on success.  

# Overview

This action performs the following:
- Run specified script
- Wait for success status
- Download artifacts


#

```
grid session | awk -F'│' '$3 ~ /.*running.*/ {print $2}' | while read s; do echo $s; done
grid session | awk -F'│' '$3 ~ /.*running.*/ {print $2}' | while read s; do echo $s; grid session delete $s; done

```