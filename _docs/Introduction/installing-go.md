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
brew install go
```
### Install Go on Linux  from APT Repository
You can install Go on Linux machine using APT

```
sudo apt-get update
sudo apt-get install golang
```
## Go workspace
### $GOPATH

`$GOPATH` is a directory that houses go code in a machine. From Go version 1.8, if this path is not set it defaults to `$HOME/go` on Unix and `%USERPROFILE%/go` on Windows.

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

