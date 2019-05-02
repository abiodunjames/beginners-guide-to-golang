---
title: Go Data Structures
category: Go Basics
order: 3

---

In this page, we'll talk about  go data structures.

* Boolean type
* String type
* Numeric type

### Boolean type

To define a variable of boolean type, we'll follow go's way of defining variables described earlier.

```go
var active bool = true
var inactive bool = false
```

You can also define a variable of boolean type without initializing value

```go
var inactive bool  //defaults to false
```

You can not convert an int (for example `1` or `0`) to a boolean type.

### String type

Strings are represented by double quotes `"` or a   back tick `   and uses UTF-8 character set.  You can define a variable of string type this way :- 

```go
	var name string //no value
	var emptystring string = "" //blank string
	firstname, lastname := "Abolade", "Graham" 
  var name string = "Abolade Graham"
```

Combining strings in go similar to an old way of combining strings in javascript prior to ES6.
You can combine strings with `+` sign.

```go
var firstname string = "Abolade"
var lastname string = "Graham"
fullname := firstname + lastname //Abolade Graham
```

Back tick is useful for constructing multi line strings. 

```go
 multiline := `Line 1
 							 Line 2
							 Line 3`
```

` Back tick does not escape any values in strings. You simply get what you put in there.

### Numeric Type

Go has the following built-in numeric types, `int8`, `uint8` (`byte`), `int16`, `uint16`, `int32` (`rune`), `uint32`, `int64`, `uint64`, `int`, `uint`, `uintptr`, `float32`, `float64`, `complex64`, `complex128`.

### Error Type

Go does not have try and catch block for exceptions like in other languages but it does have  `error` type for defining error messages.

```go
import (
	"errors"
	"fmt"
)

var err error
err = errors.New("This is an error")
fmt.Print(err)
```

Or

```go
import (
	"errors"
	"fmt"
)
err := errors.New("This is an error")
fmt.Print(err)
```



