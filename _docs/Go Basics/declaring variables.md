---
title: Declaring Variables in Go
category: Go Basics
order: 1
---
### Variable declaration 

There are many ways to declare variable in Go and one of my favourites is this:

```go
var surname string
```
Three things are needed to declare variables in the example above.
`var` keyword, followed by variable's name `surname` and type.


You can also declare multiple variables at once.
```go
 var firstname, middlename, lastname string
```
When you define a variable without initialising its value, zero is automatically assigned to it.

```go
var age int  //0
```
Untialize boolean types default to false.
```go
var active boolean  //false
```

What about initialing  variables with values?

 ```go
var firstname strig = "Peter"
 ```

You can declare multiple variables and initialize their values in one line.

```go
var variable1, variable2, variable3 = value1, value2, value3
```
You can also declare variables without specifying the type.

```go
var surname = "Peter"
```
Why cant we remove `var` as well? Well, you can with "Go" *short assignment*.

```go
firstname, middlename, lastname :="Peter", "Olabisi", "Abolade"
```
Variable declared using Go's short assignment must be used inside a function. They cannot be global. Please take note.

If you're a JavaScript developer, you would remember `_` in  ES6 destructuring assignment. It's used to skip values you do not need. It works the same way in Go. You can skip any variable you don't want with `_`

```go
var _,year =  1990, 2000 //year = 2000

```
One of the cool things in Go is that all declared variables must be used. You can't keep dead variables in your code. Go compiler will scream at you if you do.

###Defining Variables in Group

You can declare variables or constants in group

```go
var (
  counter int,
  name string,
  age int8
)
```

For constants,

```go
const (
  counter = 1,
  database = "go-app"
)
```

You can also import packages in group

```go
import (
  "fmt",
  "os",
  "errors"
)
```

### Variable Visibility

A variable is public if its first letter is capitalized. Private variables  begin with a small case.

```go
var Name string  //public variable
var age string // private variable
const Os = "mac" // public variable
```

This same rule applies to go functions. Functions that begin with capital letter are public and can be exported