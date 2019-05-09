---
title: Declaring Constants in Go
category: Go Basics
order: 2
---

Constants are variables whose value cannot be changed once it's declared. Applications often contain attributes that dont change. For example, database name, mathematical constant like pie etc. They are better defined as constant.

Declaring constant in Go is simillar to Javascript

```go
const database = "mydatabase"
```
Constants can also be declared in one group. If you have multiple constant to define, this is often the best way to go.

```go
const (
  host = "https://example.com",
  database = "go-app",
  ipAddress = "127.0.0.1"
)
```