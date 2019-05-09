---
title: Go array
category: Array, Slice & Map
order: 4
---
Array is a range of a particular type of data. It's a data structure used to store data of a particular type like integers, strings etc. Array is very popular in most programming languages.

Array can be defined as:
```
var variableName [size] dataType

```
For example, an array of five integers would be defined as:-

### Defining arrays

```go
 var numbers [3][4] int{[4]int{1, 2, 3, 4}, [4]int{ 2, 5, 6, 8}, [4]int{9, 3, 12, 1}}
```
Like other languages, array index starts from 0.

We can set an array values in go using its indices.

```go
numbers[0] = 20  // assign 20 as value of index 0 
numbers[1] = 40 // assign 40 as value of index 1
```
You can also define the values at creation

```go
 numbers := [4] int {20, 40, 60, 80, 100}
```
When the values defined are less than the size, the rest default to 0.
```go
numbers := [4] int {20, 40}

numbers[0] // value equals 20;
numbers[1] // value equals 40
numbers[2] // value equals 0
...
numbers[4] // value equals 0
```
You can replace 'size' with `...`, the size will be automatically calculated.
```go
var numbers = [...] int {20, 40, 60, 80, 100}
```
### Defining multi-dimensional array
Multi-dimensional array must define the number of elements and the size of each.

An array of 3 elements with a size 4 in each is defined as follows:
```go
    var numbers = [3][4]int{[4]int{1, 2, 3, 4}, [4]int{ 2, 5, 6, 8}, [4]int{9, 3, 12, 1}}

    numbers[1] //[2 5 6 8]
    
```

## Slice
We can think of slice as dynamic arrays whose size is not defined. It is an array without the size constraint.
```go
var slice = []int //
```
A slice -- just like its name can be a chunk from a bigger array.

To define a slice, you may specify `lowerIndex` where the slice should begin from and `upperIndex` where the slice should end.

```go
var slice = biggerArray[lowerIndex:upperIndex]

```

Let's play around a bit here.

```go
package main

import (
	"fmt"
)

func main() {
    var arrayNumber = [6]int{1, 2, 3, 4, 5, 6}  // an array of six elements
    // A slice with a lower index and a upper index
	firstSlice := arrayNumber[2:4]
	fmt.Println(firstSlice) // prints [3 4] 

// A slice with same lower index and upper index
	secondSlice := arrayNumber[0:0] //[]
	fmt.Println(secondSlice)

    //A slice with lower index  only
	thirdSlice := arrayNumber[4:]
	fmt.Println(thirdSlice) // prints  [5 6]

    // A slice with upper index only
	fourthSlice := arrayNumber[:4]
	fmt.Println(fourthSlice) //[//1 2 3 4]

    // A slice with neither lower nor upper index
	fifthSlice := arrayNumber[:]
	fmt.Println(fifthSlice) //[1 2 3 4 5 6]
}

```
## Map
Map is go built-in associative data types known as hashes or dicts in other languages. Unlike slice, map can have strings or integers as indices.
We define map in go as:
```go
var myMap = make(map[keyType][valueType])
```
```go
var fruits = make(map[string][string])
fruits["a"] = "apple"
fruits["b"] = "banana"

```
Map values can be defined using a `key:value` format
```go
fruits := map[string]string{"a":"Apple", "b":"Banana"}
```
