+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-04-06T08:08:07+09:00"
menu = "main"
title = "Stack hello world"

+++
Stack is famous for Haskell package manager. 
As a web developer I am used to clear tutorial that I can understand and learn.
Let's make a sample app.


## Installing Stack
Install on OSX through homebrew
```
$ brew update
$ brew install haskell-stack
```

## Creating a new app
```
$ stack new hello-world
```
Stack has some templates you can use your app. 

## Installing GHC
Run this in your app.
```
$ stack setup
```

## Building an Executable
You can build with stack build
```
$ stack buuild
```

## Run the app
Runt the app. This is cool.
```
$ stack exec hello-world-exe
SomeFunc
```
