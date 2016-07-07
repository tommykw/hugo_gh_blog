+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-07-07T19:01:42+09:00"
menu = "main"
title = "Filename oneshot replacement"

+++
Filename replace command

```
find . -name "*-fs8*" | sed -e 's/\(\(.*\)-fs8\(.*\)\)/mv \1 \2\3/g' | sh
```
