+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-08-29T23:53:03+09:00"
menu = "main"
title = "Nullpointer serializable"

+++
The following code is nullpointer exception.

```
private val userLumps by lazy {
    intent.getSerializableExtra(ARG_USER_LUMP) as ArrayList<UserLump>
}
private val adapter = OriginalAdapter(userLumps)
```

Error details
```
Caused by: java.lang.NullPointerException: Attempt to invoke virtual method 'java.io.Serializable android.content.Intent.getSerializableExtra(java.lang.String)' on a null object reference
```

It becomes null before it is initialized wit the lifecycle proble. No proble if set in onCreate.
