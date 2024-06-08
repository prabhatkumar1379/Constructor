# Constructor
Going to discuss all the constructor in c#
Constructor
-----------
<p>1>A Constructor of a class must be same as class name </p>
<p>2>A Constructor can not be the abstract ,final, Synchronized.</p>
<p>3>A Constructor doesn't have any return type ,not even void.</p>
<p>4>A Constructor without access specifier is Private Constructor.</p>
<p>5>Access modifier can be used in constructor declaration to control its access.</p>
<p>6>if we don't create a constructor then compilar will create a default constructor.</p>
<p>7>A static constructor can not be parameterized constructor.</p>
<p>8>Within a class we can created only one constructor.</p>
<p><b>Types of Constructor in c#</b></p>
 1.Default Constructor: A constructor without parameter is called Default Constructor.
class Program
{
    public Program()
    {}
} 
<img src="https://www.simplilearn.com/ice9/free_resources_article_thumb/Constructor-in-C%23/Constructor-in-C%23-Types-img1.png" alt="Constructor-in-C#-Types-img1" width="900" height="563" class="blend-mode">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/amitshekhariitbhu/go-backend-clean-architecture/blob/main/assets/go-backend-arch-diagram.png?raw=true"><img src="https://github.com/amitshekhariitbhu/go-backend-clean-architecture/raw/main/assets/go-backend-arch-diagram.png?raw=true" alt="Go Backend Clean Architecture Diagram" style="max-width: 100%;"></a>
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
