# mtrand

## Introdution

*mtrand* based on *Mersenne Twister* algorithm. The *Mersenne Twister* is a strong pseudo-random number generator. Strong PRNG has a long period (how many values it generates before repeating itself) and a statistically uniform distribution of values (bits 0 and 1 are equally likely to appear regardless of previous values). A version of the Mersenne Twister available in many programming languages, *MT19937*, has an impressive period of *2^19937-1*.

## Installation

```
go get "github.com/wmentor/mtrand"
```

## Usage

```go
package main

import (

  "fmt"
  "time"

  "github.com/wmentor/mtrand"
)

func main() {

  gen := mtrand.New()
  gen.Seed(time.Now().UnixNano())


  for i := 0 ; i < 1000 ; i++ {

    // get int64 value
    // or you can call gen.Uint64 to get uint64
    fmt.Println(gen.Int63())
  }
}
```
