---
title: Go array
category: Array, Slice & Map
order: 1
---
Array is a range of a particular type of data, a data structure used to store data of a particular type like integers, strings etc. Array is very popular in all programming languages.

Array can be defined in go as:
```
var variableName [size] dataType

```
For example, an array of five integers would be defined as:-

### Defining arrays

```go
 var numbers [3][4] int{[4]int{1, 2, 3, 4}, [4]int{ 2, 5, 6, 8}, [4]int{9, 3, 12, 1}}
```
Like other languages, Go array index starts from 0.

We can set array values in go using indices.

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