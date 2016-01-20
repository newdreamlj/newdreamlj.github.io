---
layout: post
title:  Golang Handbook
---

#### Compile

	> 6g hello.go
	> 6l hello.6
	> ./6.out

#### Basic framework

	import "fmt"
	func main(){
		fmt.Println("Hello World!\n")
	}

#### Declaring Variables

	var i int
	var theta float32
	var explicitly, typed, pointers *complex128
	int_pointer := &i
	int_pointer2 := new(int)
	channel := make(chan interface{}) 


