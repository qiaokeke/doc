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
