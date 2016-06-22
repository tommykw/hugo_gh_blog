+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-06-23T07:36:13+09:00"
menu = "main"
title = "Rx.Single timer"

+++
The timer processing introduce the following two of Pattern in Rx.Single.

Repeat until OnError
```
callSingle().toObservable()
    .subscribeOn(Schedulers.io())
    .observeOn(AndroidSchedulers.mainThread())
    .repeatWhen { it.flatMap({ Observable.timer(50, TimeUnit.SECONDS)}) }
    .subscribe({
        doStuff()
    })
```

Repeat until OnSuccess
```
callSingle().toObservable()
    .subscribeOn(Schedulers.io())
    .observeOn(AndroidSchedulers.mainThread())
    .retryWhen { it.flatMap({ Observable.timer(50, TimeUnit.SECONDS)}) }
    .subscribe({
        doStuff()
    })
```

There is a need to convert once from Single to Observable
