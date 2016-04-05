+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-04-06T08:08:07+09:00"
menu = "main"
title = "Stack hello world"

+++
Stack is famous for Haskell package manager. 
As a web developer I am used to clear tutorial that I can understand.

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

## Installing GHC
```
$ stack setup
```

## Building an Executable
```
$ stack buuild
```

## Run the app
```
$ stack exec hello-world-exe
SomeFunc
```
