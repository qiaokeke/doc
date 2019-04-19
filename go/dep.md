## install
* https://golang.github.io/dep/docs/installation.html
## create a new project
* https://golang.github.io/dep/docs/new-project.html
```
$ mkdir -p $GOPATH/src/github.com/me/example
$ cd $GOPATH/src/github.com/me/example
$ dep init
$ ls
Gopkg.toml Gopkg.lock vendor/

$ dep ensure -add github.com/foo/bar github.com/baz/quux
```
## dep ensure
* https://golang.github.io/dep/docs/daily-dep.html
* To add a new dependency
* To update an existing dependency
* To catch up after importing a package for the first time in your project, or removing the last import of a package in your project
* To catch up to a change to a rule in Gopkg.toml
