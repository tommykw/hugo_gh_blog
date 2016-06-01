+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-06-01T13:56:11+09:00"
menu = "main"
title = "Fragment IllegalStateException"

+++
Operation to FragmentManager must be in front of the Activity of the side onSaveInstanceState().
The following error will occur if you have an operation.

```
Can not perform this action after onSaveInstanceState()
```

The operation in onCreate, you need to stop the operation of Fragment in asynchronous.
