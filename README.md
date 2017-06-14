# Go Python Way to Scala while CPPing Java[script] and Designing Patterns

Python one liners - First of all you are in for a ride!

## Index

```golang
type SomeName struct {
}

func (SomeName*sm) SomeMethodName() {
}

func main() {
    var someVariable int = 0;
}
```

```scala
object SomeName {
/*
*/
//
    def main(args: Array[String]){
          val someVariable: Int = 0; // Immtable variable
          var someOtherVariable:Int = 0; // Mutable Variable
          println(args)
    }
}
```
Alright the aim is to taste the scala sugar.
```scala
object someName extends App {
    val someVariable: Integer = 0;
    println(args)
}
```

Interesting thing one can see about over here is a typed tuple `val (myVar1: Int, myVar2: String) = Pair(40, "Foo")`, this Pair reminds me of the pair from cpp `pair<int,int> someName;`.

```python
class someName:
    def __init__(self,someArgument):
        self.someVariable=someArgument
    
    def someMethod(self):
        pass
```


```scala
class someName(val someArgument: Int) {
    val someVariable: Int = someArgument
    
    def someMethod(){
    }
}
```
## Love Python Generators .. Oh yeah you will love this
```python
# Generator
```
```scala
Source
```
## Lambda Functions
```python
someName=lambda x:  x
```
```scala
val someName = (x:Int) => { x}:Int
```
## Just functions
```golang
func someName(a Int) Int {
}
```
```scala
def someName(a:int): Int {
}
```
## function variables
```golang
var f func(int) int
f = func(i int) int {
    if i == 0 {
        return 1
    }
    return i * f(i-1)
}
```

```scala
def someName(a:int): Int {
}
val someOtherName: (Int, Int) => Int = someName
```
> In scala everything is a function.

### if else - Sugar :candy:

```python
someVariableName=1 if 1 else 0
```
```scala
val someConstantVariableName:Int=  1 if ( true) else 0
```

## Functional Looping

## Accumulative computation on Iterables with _Folding_
```python3.4
from itertools import accumulate
from operator import add

print accumulate([1,2,3,4,5], add)
```
if you think that is just cool. We can do functionally on scala. Whoa! [4][5]
```scala
List([1,2,3,4,5]).fold(0) { (z,i) => z+i }
List([1,2,3,4,5]).foldLeft(0) { (z,i) => z+i }
List([1,2,3,4,5]).foldRight(0) { (z,i) => z+i }
```
## I _Promise_ you a :high_brightness: _Future_

```javascript
new Promise(function(resolve, reject) {
    resolve("hi")
}).then( function( result ) {
}, function( error ) {
});
```
May be scala will change the name to "Promises" too who knows. [3]
```scala
val f = Future {
}
```
## Implicit aid 
![](http://livingcivil.com/wp-content/uploads/2011/10/Story4.jpg)
```python
```
```scala
```
### Implicit Value for a type
```scala
implicit val a:Int = 5;
def someFunctionName(){a:int}={
println(a)
}
println(implicitly(Int))
```
## Partial Functions
### Starting with Default parameters
```python
def someFunctionName(one, two=None):
    pass
```
```scala
def someFunctionName(one:Int, two:Int=0)={
}
```
### Now there there
```scala
def someFunction(a:Int){b:Int}= (a%b==0)
List(4,5,6).map(someFunction(30))
```
# References
1. _https://datasciencevademecum.wordpress.com/2016/01/28/6-points-to-compare-python-and-scala-for-data-science-using-apache-spark/_
2. _http://www.alessandrolacava.com/blog/scala-case-classes-in-depth/_
3. _https://developers.google.com/web/fundamentals/getting-started/primers/promises_
4. _https://coderwall.com/p/4l73-a/scala-fold-foldleft-and-foldright_
5. _https://oldfashionedsoftware.com/2009/07/30/lots-and-lots-of-foldleft-examples/_
