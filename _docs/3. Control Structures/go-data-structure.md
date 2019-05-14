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

### Numeric Types

Are sets of integer or floating-point values. Go has the following built-in numeric types. 

| Type       | Description                                                  |
| ---------- | ------------------------------------------------------------ |
| uint8      | The set of all unsigned  8-bit integers (0 to 255)           |
| uint16     | The set of all unsigned 16-bit integers (0 to 65535)         |
| uint32     | The set of all unsigned 32-bit integers (0 to 4294967295)    |
| uint64     | The set of all unsigned 64-bit integers (0 to 18446744073709551615) |
| Int8       | The set of all signed  8-bit integers (-128 to 127)          |
| Int16      | The set of all signed 16-bit integers (-32768 to 32767)      |
| Int32      | The set of all signed 32-bit integers (-2147483648 to 2147483647) |
| Int64      | The set of all signed 64-bit integers (-9223372036854775808 to 9223372036854775807) |
| float32    | The set of all IEEE-754 32-bit floating-point numbers        |
| Float64    | The set of all IEEE-754 64-bit floating-point numbers        |
| Complex64  | The set of all complex numbers with float32 real and imaginary parts |
| Complex128 | The set of all complex numbers with float64 real and imaginary parts |
| Byte       | Alias for uint8                                              |
| Rune       | Alias for int32                                              |
| uint       | Either 32 or 64 bits                                         |
| Int        | Same size as uint                                            |
| uintptr    | An unsigned integer large enough to store the uninterpreted bits of a pointer value |
|            |                                                              |

### Error Types

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



