+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-08-25T18:58:32+09:00"
menu = "main"
title = "Resolve error in AS"

+++
The following error occurred in the android studio.

```
Resolve Error

SDK location not found. Define location with sdk.dir in the local.properties files
or with an ANDROID_HOME environment variable.
```

I do the following in the corresponding you in my case.
```
1. Create local.properties
2. Add local.properties to sdk.dir=/Users/xxx/Downloads/android-sdk-macosx
3. set ANDROID_HOME=/Users/xxx/Downloads/android-sdk-macosx/sdk
4. export ANDROID_HOME=/Users/xxx/Downloads/android-sdk-macosx/sdk
5. ./gradlew
6. reinstall android studio
```

It works.
