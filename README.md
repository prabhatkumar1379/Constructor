# Constructor

Constructor
<ul>
    <li>A Constructor of a class must be same as class name</li>
    <li>A Constructor cannot be abstract, final, synchronized.</li>
    <li>A Constructor doesn't have any return type, not even void.</li>
    <li>A Constructor without access specifier is Private Constructor.</li>
    <li>Access modifier can be used in constructor declaration to control its access.</li>
    <li>If we don't create a constructor then compiler will create a default constructor.</li>
    <li>A static constructor cannot be parameterized constructor.</li>
    <li>Within a class, we can create only one constructor. </li>
</ul>

 
<h3>What is Constructor?</h3>
<p dir="auto">
Constructor is a special method present under a class which is responsible for Initializing the data member(fields) of that class.
constructor method is Invoked automatically when we create the instance of class.
the name of a constructor method is the same name of the class and more over it's a non-value returning method.
Every class required a constructor in it. if we want to create the instance of that class or else,we can't create the instance of any class
</p>
<p dir="auto">
Note:while defing a class  it's the responsibility of developer to define a <b>constructor explicitly</b> under class,
and if we fail to do so. on behalf of developer an <b>implicit constructor</b> gets defined in those classes;

</p>
<h3>Example of an Implicit Constructor</h3>
<p>Consider the following class definition:</p>

<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>
class Test 
{
   int i = 10; 
   string s; 
   bool b;  // Fields
}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="curl --location --request POST 'http://localhost:8080/login' \
--data-urlencode 'email=test@gmail.com' \
--data-urlencode 'password=test'" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
  <p>After compilation, the above class will include an implicit constructor, as shown below:</p>
  
  <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>
class Test 
{
   int i = 10; 
   string s; 
   bool b;  // Fields
   
   public Test()  // Implicit Constructor
   {			
      i = 10; 
      s = null; 
      b = false;		
   }
}

</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="curl --location --request POST 'http://localhost:8080/login' \
--data-urlencode 'email=test@gmail.com' \
--data-urlencode 'password=test'" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
--------------------


<p>
    <b>Types of Constructor in c#</b></p>
<img src="https://www.simplilearn.com/ice9/free_resources_article_thumb/Constructor-in-C%23/Constructor-in-C%23-Types-img1.png" alt="Constructor-in-C#-Types-img1" width="900" height="563" class="blend-mode">

 1.Default Constructor: A constructor without parameter is called Default Constructor.

<img src="https://github.com/prabhatkumar1379/Constructor/blob/main/DefaultConstructor.png" alt="Constructor-in-C#-Types-img1" width="900" height="563" class="blend-mode">
<p dir="auto">

Default constructors can be defined either explicitly or will be defined implicitly provided there is no explicit constructor defined under that class, whereas implicit constructors will never be parameterized i.e., if a constructor is parameterized then it is very sure, that it is an explicit constructor.

Note: if Constructors of a class are parameterized then values to those parameters should be sent while creating instance of that class.
To test Parameterized Constructors, add a new class in our project naming it as “ParamConDemo.cs” and write the below code in it:

</p>

<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>
 {
  public ParamConDemo(int i)
  {
    Console.WriteLine($"Parameterized constructor is called: {i}"); 
  }
  static void Main()
  {
    ParamConDemo cd1 = new ParamConDemo(100);
    ParamConDemo cd2 = new ParamConDemo(200);
    ParamConDemo cd3 = new ParamConDemo(300);
    Console.ReadLine(); 
  }
}


</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="curl --location --request POST 'http://localhost:8080/login' \
--data-urlencode 'email=test@gmail.com' \
--data-urlencode 'password=test'" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>

 
 <p dir="auto">
  2.Parameterized Constructor : A constructor with parameter is called Parameterized Constructor.
 </p>p>
<b>3.Copy Constructor </b>: It created an object by copying variables from another object.
<p dir="auto">
The constructor takes a parameter of class type is called the copy constructor and this constructor is used to copy one object data into another object. The main purpose of the copy constructor is to initialize a new object (instance) with the values of an existing object (instance).

That means this constructor is used to copy the data of an existing object into a newly created object that’s why this constructor is called the copy constructor.
</p>

<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>class Program
{
    public int a;
    public Program()
    {
      a=Program.a;
    Console.WriteLine("Copy Constructor");
    }
}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w"   tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>

<b>4.Static Constructor </b>: When a constructor is created using a static keyword, it will invoked only once from all of the instances of the class.

<p dir="auto">
We can create a constructor as static and when a constructor is created as static, it will be invoked only once. There is no matter how many numbers of instances (objects) of the class are created but it is going too invoked only once and that is during the creation of the first instance (object) of the class.

The static constructor is used to initialize static fields of the class and we can also write some code inside the static constructor that needs to be executed only once.

Static data fields are created only once in a class even though we are created any number of objects.
</p>
<ul>
   
 <li>There can be only one static constructor in a class.</li>
 <li>The static constructor should be without any parameter.</li>
 <li>It can only access the static members of the class.</li>
 <li>There should not be any access modifier in the static constructor definition.</li>
 <li>If a class is static then we cannot create the object for the static class.</li>
 <li>Static constructor will be invoked only once i.e. at the time of first object creation of the class, from 2nd object creation onwards static constructor will not be called.</li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>class Program
{
    static Program()
    {
    }

}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w"   tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
