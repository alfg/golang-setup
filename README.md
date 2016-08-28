# golang-setup

## Go Setup (for local development)
Please note: Go 1.4.x is required to build 1.5.x. This is because the Go compiler is written in Go as of 1.5.x. Previous versions' compilers were written in C, hence the instructions below to install 1.4 before 1.5.

* Install Go
* Install GVM
* Setup GVM/Go environment

```
gvm install go1.4.3
gvm use go1.4.3
gvm install go1.5.3
gvm use go1.5.3
```

GVM will automatically set your GOBIN and GOPATH environment variables.

## Go Project Setup (for local development)
Setting up Go for local development is a bit different than other languages. You will generally create a Go directory somewhere on your system and all projects, modules, binaries and packages will be stored here under a directory structure like below:

```
Go/
  src/ - Source files of projects, modules and packages will be installed here.
    github.com/
    aws
    ...
    golang.org/
    my-golang-project/
  bin/ - Binaries will compiled here.
  pkg/ - Platform specific binaries to be packaged here.
```

## Setup GOPATH project structure
```
cd ~/Source/Go
gvm pkgset use --local
```

Environment is activated and ready. Now you can install and run a Go project:
```
git clone my-golang-project src
go build my-golang-project && ./my-golang-project
```

## Go IDE Setup
* Follow the guides below to setup a decent Go IDE in VIM or Atom.
* https://github.com/fatih/vim-go
* https://github.com/farazdagi/vim-go-ide
* http://farazdagi.com/blog/2015/vim-as-golang-ide/
* https://atom.io/packages/go-plus
* https://github.com/joefitzgerald/go-plus
* https://github.com/nsf/gocode
