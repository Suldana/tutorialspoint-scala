Variable Declaration
mutable variable: is a variable that can change value.

Following is the syntax to define a variable using var keyword

Syntax:
var myVar : String = "Foo"

immutable variable: is a variable that cannot be changed.

Following is the syntax to define a variable using val keyword

Syntax:
val myVal : String = "Foo"

Variable Data Types
The type of a variable is specified after the variable name and before equals sign. You can define any type of Scala variable by mentioning its data type as follows −

Syntax
val or val VariableName : DataType = [Initial Value]

Syntax:
var myVar :Int;
val myVal :String;

Variable Type Inference:
When you assign an initial value to a variable, the Scala compiler can figure out the type of the variable based on the value assigned to it. This is called variable type inference. 

Syntax
var myVar = 10;
val myVal = "Hello, Scala!";

Multiple assignments
Syntax
val (myVar1: Int, myVar2: String) = Pair(40, "Foo")

And the type inference gets it right −

Syntax
val (myVar1, myVar2) = Pair(40, "Foo")

Example
object Demo {
   def main(args: Array[String]) {
      var myVar :Int = 10;
      val myVal :String = "Hello Scala with datatype declaration.";
      var myVar1 = 20;
      val myVal1 = "Hello Scala new without datatype declaration.";
      
      println(myVar); println(myVal); println(myVar1); 
      println(myVal1);
   }
}