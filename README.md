# Go Python Way to Scala while CPPing Java

Python one liners - First of all you are in for a ride!

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
## Implicit aid 
![](http://livingcivil.com/wp-content/uploads/2011/10/Story4.jpg)
```python
```

# References
1. _https://datasciencevademecum.wordpress.com/2016/01/28/6-points-to-compare-python-and-scala-for-data-science-using-apache-spark/_
2. _http://www.alessandrolacava.com/blog/scala-case-classes-in-depth/_
