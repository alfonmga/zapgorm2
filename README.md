# zapgorm2

[![Go Reference](https://pkg.go.dev/badge/github.com/alfonmga/zapgorm2.svg)](https://pkg.go.dev/github.com/alfonmga/zapgorm2)

The initial source code is from [moul/zapgorm2](https://github.com/moul/zapgorm2). I made minor changes to make it work with my projects, like setting `IgnoreRecordNotFoundError` to `true`.

## Install

Via go get tool

```bash
$ go get -u github.com/alfonmga/zapgorm2
```

## Usage

```go
import "github.com/alfonmga/zapgorm2"

logger := zapgorm2.New(zap.L())
logger.SetAsDefault() // optional: configure gorm to use this zapgorm.Logger for callbacks
db, err = gorm.Open(sqlite.Open("./db.sqlite"), &gorm.Config{Logger: logger})
```
