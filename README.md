# Constructor
Going to discuss all the constructor in c#
Constructor
-----------
<h1>1>A Constructor of a class must be same as class name </h1>
<h1>2>A Constructor can not be the abstract ,final, Synchronized.</h1>
<h1>3>A Constructor doesn't have any return type ,not even void.</h1>
<h1>4>A Constructor without access specifier is Private Constructor.</h1>
<h1>5>Access modifier can be used in constructor declaration to control its access.</h1>
<h1>6>if we don't create a constructor then compilar will create a default constructor.</h1>
<h1>7>A static constructor can not be parameterized constructor.</h1>
<h1>8>Within a class we can created only one constructor.</h1>
<h1><b>Types of Constructor in c#</b></h1>
1.Default Constructor: A constructor without parameter is called Default Constructor.
class Program
{
    public Program()
    {}
}
2. Parameterized Constructor : A constructor with parameter is called Parameterized Constructor.
class Program
{
    int a;
    public Program(int a)
     { 
        this.a=a;
        Console.WriteLine("parametrized constructor");
     }
}
3.Copy Constructor : It created an object by copying variables from another object.
class Program
{
    public int a;
    public Program()
    {
      a=Program.a;
    Console.WriteLine("Copy Constructor");
    }
}
4.Static Constructor : When a constructor is created using a static keyword, it will invoked only once from all of the instances of the class.
class Program
{
    static Program()
    {
    }

}
