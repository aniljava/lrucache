## Overview

Mirror of: https://code.google.com/p/vitess/source/browse/go/cache/

Package name is changed to lrucache from cache to match the project name.

## Usage

package main

    import (
        "fmt"
        "github.com/aniljava/lrucache"
    )
    
    type Value []byte
    
    func (value Value) Size() int {
        return len(value)
    }
    
    func main() {
        c := lrucache.NewLRUCache(2)
        c.Set("One", Value("Two"))
    
        fmt.Println(c.Get("One"))
    }
