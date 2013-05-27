## Overview

Mirror of: https://code.google.com/p/vitess/source/browse/go/cache/

Package name is changed to lrucache from cache to match the project name.

## Usage

    package main
    
    import (
        "fmt"
        "github.com/aniljava/lrucache"
    )
    
    func main() {
        cache := lrucache.NewLRUCache(200)
    
        key := "foo"
        value := []byte("BAR")
    
        cache.Set(key, lrucache.ByteValue(value))
     
        data, _ := cache.Get(key)
        fmt.Println(data.(lrucache.ByteValue))
    }