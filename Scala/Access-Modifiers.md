Private Members
A private member is visible only inside the class or object that contains the member definition.

Following is the example code snippet to explain Private member −

Example
class Outer {
   class Inner {
      private def f() { 
        println("f")
        }
      
      class InnerMost {
         f() // OK
      }
   }
   (new Inner).f() // Error: f is not accessible
}
In Scala, the access (new Inner). f() is illegal because f is declared private in Inner and the access is not from within class Inner.

Protected Members
A protected member is only accessible from subclasses of the class in which the member is defined.

Following is the example code snippet to explain protected member −

Example
package p {
   class Super {
      protected def f() { 
        println("f") 
        }
   }
   
   class Sub extends Super {
      f()
   }
   
   class Other {
      (new Super).f() // Error: f is not accessible
   }
}
The access to f in class Sub is OK because f is declared protected in ‘Super’ class and ‘Sub’ class is a subclass of Super. By contrast the access to f in ‘Other’ class is not permitted, because class ‘Other’ does not inherit from class ‘Super’.


Public Members
Unlike private and protected members, it is not required to specify Public keyword for Public members. There is no explicit modifier for public members. Such members can be accessed from anywhere.

Following is the example code snippet to explain public member −

Example
class Outer {
   class Inner {
      def f() { println("f") }
      
      class InnerMost {
         f() // OK
      }
   }
   (new Inner).f() // OK because now f() is public
}