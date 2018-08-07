# Functions

- [Function examples](../todd-mcleod/06-functions)
- [Variadic](https://golang.org/ref/spec#Passing_arguments_to_..._parameters)


### Go functions

#### fmt.Sprint
```
// from package fmt: Sprint
// concatenate with space
fmt.Sprint('Santiago', 'Laparra')
```

#### append
```
// append: add an element to a slice
aSlice := {0, 1}
anotherSlice := append(aSlice, 2)

```

#### len: length of a slice
```
aVar := {1, 2}
fmt.Print(len(aVar)) // 2
```
[* length & capacity tour](https://tour.golang.org/moretypes/11)


#### make
```
var s []byte

//create a slice len 5 cap 5
s = make([]byte, 5, 5)

// s == []byte{0, 0, 0, 0, 0}
```
[* from golang blog](https://blog.golang.org/go-slices-usage-and-internals)