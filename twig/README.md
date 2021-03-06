Twig
====

[![Build Status](https://travis-ci.org/kaiaverkvist/stick.svg?branch=master)](https://travis-ci.org/kaiaverkvist/stick)
[![GoDoc](https://godoc.org/github.com/kaiaverkvist/stick/twig?status.svg)](https://godoc.org/github.com/kaiaverkvist/stick/twig)

Provides [Twig-compatibility](http://twig.sensiolabs.org/) for the stick
templating engine.


Overview
--------

This project is split over two main parts.

Package
[`github.com/kaiaverkvist/stick`](https://github.com/kaiaverkvist/stick)
is a Twig template parser and executor. It provides the core
functionality and offers many of the same extension points as Twig like
functions, filters, node visitors, etc.

Package
[`github.com/kaiaverkvist/stick/twig`](https://github.com/kaiaverkvist/stick/tree/master/twig)
contains extensions to provide the most Twig-like experience for
template writers. It aims to feature the same functions, filters, etc.
to be closely Twig-compatible.


Installation
------------

The `twig` package is intended to be used as a library. The recommended
way to install the library is using `go get`.

```bash
go get -u github.com/kaiaverkvist/stick/twig
```


Usage
-----

Execute a simple Twig template.

```go
package main

import (
	/stick/twig"
	/stick"
	"os"
)

func main() {
    env := twig.New(nil)
	env.Execute("Hello, {{ name }}!", os.Stdout, map[string]stick.Value{"name": "Tyler"})
}
```

See [godoc for more information](https://godoc.org/github.com/kaiaverkvist/stick/twig).

