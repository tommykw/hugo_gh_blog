+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-07-07T19:04:03+09:00"
menu = "main"
title = "Filename oneshot removement"

+++
Filename remove command

```
ls -al *.png | grep -v "fs8" | awk '{print "rm ",$10}' | sh
```
