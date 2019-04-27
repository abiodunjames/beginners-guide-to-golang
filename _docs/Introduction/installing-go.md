---
title: Installing Go
category: Introduction
order: 2
---
### Install Go from Golang official binary
You can download Go from its binary for FreeBSD, Linux, macOS, and Windows operating systems from Golang [official download page](https://golang.org/dl/)
### Install Go on Mac OS using Home Brew

```
brew update
brew install golang-go
```
### Install Go on Linux  from APT Repository
You can install Go on Linux machine using APT. 

```
sudo apt-get update
sudo apt-get install golang
```
> Please be aware that APT repository does not always provide the recent or current up to date version of go. 


## Go workspace
Go uses one workspace to manage "Go" code called `$GOPATH` and this must be added to your path. `$GOPATH` is a directory that houses go code in a machine. From Go version 1.8, `$GOPATH` is not set it defaults to `$HOME/go` on Unix and `%USERPROFILE%/go` on Windows.

In Unix systems, you can set gopath like this.
```
export GOPATH=${HOME}/GoProject
```
There are 3 directories in `$GOPATH`

- `src` for go original source files with extension is .s, .c
- `pkg` for compiled files whose suffix is .a
- `bin` directory is where go executable files live

### $GOROOT

`$GOROOT` is the path where GO is installed on the machine. By default, the path on Unix is `/usr/local/go` and `C:\go` on Windows.

### Test your installation
 Execute  "go version" from command
 ``` 
 $ go version
  go version go1.12.4 darwin/amd64
 ```