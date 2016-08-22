+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-08-23T00:25:42+09:00"
menu = "main"
title = "Fragment on fragment"

+++
Implementation of the fragmnet on fragment.

```
val transaction = fragmentManager.beginTransaction()
transaction.setTransition(FragmentTransaction.TRANSIT_FRAGMENT_OPEN)
transaction.replace(R.id.placeholder, fragment).addToBackStack(null).commit()
```
