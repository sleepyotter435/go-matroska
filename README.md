# Golang implementation of Matroska and WebM media container formats

[![Build Status](https://travis-ci.org/pixelbender/go-matroska.svg)](https://travis-ci.org/pixelbender/go-matroska)
[![Coverage Status](https://coveralls.io/repos/github/pixelbender/go-matroska/badge.svg?branch=master)](https://coveralls.io/github/pixelbender/go-matroska?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/pixelbender/go-matroska)](https://goreportcard.com/report/github.com/pixelbender/go-matroska)
[![GoDoc](https://godoc.org/github.com/pixelbender/go-matroska?status.svg)](https://godoc.org/github.com/pixelbender/go-matroska)

## Installation

```sh
go get github.com/sleepyotter435/go-matroska/...
```

## Usage

```go
import (
    "os"
    "fmt"
    "github.com/sleepyotter435/go-matroska/matroska"
)

func main() {
    doc, err := matroska.Decode("example.mkv")
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(doc.Segment.Info[0].Duration)
}
```

## Specifications

- [Matroska Media Container - Specifications](https://matroska.org/technical/specs/index.html)
- [WebM Container - Guidelines](https://www.webmproject.org/docs/container/)
