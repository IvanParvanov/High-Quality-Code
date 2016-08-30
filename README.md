# High-Quality-Code
## Any fool can write code that a computer can understand. Good programmers write code that humans can understand.  
# Keys to being an effective programmer:
  - Maximizing the portion of a program that you can **safely ignore**
    - While working on any one section of code
  - Most practices discussed later propose ways to achieve this important goal
  
Best conventions for writing high quality code

# What is High-Quality Programming Code?
- **High-quality programming code:**
  - Easy to read and understand
    - Easy to modify and maintain
  - Correct behavior in all cases
    - Well tested
  - Well architectured and designed
  - Well documented
    - Self-documenting code
  - Well formatted   

# Software Quality
- **External quality**
  - Does the software behave correctly?
  - Are the produced results correct?
  - Does the software run fast?
  - Is the software UI easy-to-use?v
  - Is the code secure enough?
- **Internal quality**
  - Is the code easy to read and understand?
  - Is the code well structured?
  - Is the code easy to modify?  

- **High-quality programming code**:
  - Strong cohesion at all levels: modules, classes, methods, etc.
    - Single unit is responsible for single task
  - Loose coupling between modules, classes, methods, etc.
    - Units are independent one of another
  - Good formatting
  - Good names for classes, methods, variables, etc.
  - Self-documenting code style
   
# Code Conventions
- **Code conventions** are formal guidelines about the style of the source code:
  - Code formatting conventions
    - Indentation, whitespace, etc.
  - Naming conventions
    - **PascalCase** or **camelCase**, prefixes, suffixes, etc.
  - Best practices
    - Classes, interfaces, enumerations, structures, inheritance, exceptions, properties, events, constructors, fields, operators, etc.  

- Microsoft has official **C#** code conventions
  - Design Guidelines for Developing Class Libraries: http://msdn.microsoft.com/en-us/library/ms229042.aspx
- Semi-official **JavaScript** code conventions
  - http://javascript.crockford.com/code.html, http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
- Large organization follow strict conventions
  - Code conventions can vary in different teams
- High-quality code goes **beyond code conventions**
  - Software quality is a way of thinking!

# Managing Complexity
- **Managing complexity** has central role in software development
  - Minimize the amount of complexity that anyone’s brain has to deal with at a certain time
- Architecture and design challenges
  - Design modules and classes to reduce complexity
- Code construction challenges
  - Apply good software construction practices: classes, methods, variables, naming, statements, error handling, formatting, comments, etc.
   
# Key Characteristics of HQC
- **Correct behavior**
  - Conforming to the requirements
  - Stable, no hangs, no crashes
  - Bug free – works as expected
  - Correct response to incorrect usage
- **Readable** – easy to read
- **Understandable** – self-documenting
- **Maintainable** – easy to modify when required  
- Good **identifiers' names**

  - Good names for variables, constants, methods, parameters, classes, structures, fields, properties, interfaces, structures, enumerations, namespaces,
- High-quality **classes**, interfaces and class hierarchies
  - Good abstraction and encapsulation
  - Simplicity, reusability, minimal complexity
  - Strong cohesion, loose coupling

- High-quality **methods**
  - Reduced complexity, improved readability
  - Good method names and parameter names
  - Strong cohesion, loose coupling
- **Variables**, **data**, **expressions** and **constants**
  - Minimal variable scope, span, live time
  - Simple expressions
  - Correctly used constants
  - Correctly organized data  

- Correctly used **control structures**
  - Simple statements
  - Simple conditional statements and simple conditions
  - Well organized loops without deep nesting
- Good code **formatting**
  - Reflecting the logical structure of the program
  - Good formatting of classes, methods, blocks, whitespace, long lines, alignment, etc.  

- High-quality **documentation** and comments
  - Effective comments
  - Self-documenting code
- **Defensive programming** and exceptions
  - Ubiquitous use of defensive programming
  - Well organized exception handling
- Code tuning and **optimization**
  - Quality code instead of good performance
  - Code performance when required  

- Following the corporate **code conventions**
  - Formatting and style, naming, etc.
  - Domain-specific best practices
- Well **tested** and **reviewed**
  - Testable code
  - Well designed **unit tests**
    - Tests for all scenarios
    - High code coverage
  - Passed code reviews and inspections  

# Code Formatting
## Why do we need it? How can white spaces and parenthesis help us?

```cs
	public   const    string                    FILE_NAME
	="example.bin"  ;  static void Main   (             ){
	FileStream   fs=     new FileStream(FILE_NAME,FileMode
	.   CreateNew)   // Create the writer      for data  .
	;BinaryWriter w=new BinaryWriter     (    fs      );// Write data to                               Test.data.
	for(  int i=0;i<11;i++){w.Write((int)i);}w   .Close();
	fs   .   Close  (  ) // Create the reader    for data.
	;fs=new FileStream(FILE_NAME,FileMode.            Open
	,  FileAccess.Read)     ;BinaryReader                r
	= new BinaryReader(fs);  // Read data from  Test.data.
	 for (int i = 0; i < 11; i++){ Console      .WriteLine
	(r.ReadInt32                                       ())
	;}r       .    Close   (   );  fs .  Close  (  )  ;  }

```

- Good formatting goals
  - To improve code readability
  - To improve code maintainability
- Fundamental principle of code formatting:
  - Any (consistent) formatting style that follows the above principle is good
  - Good formatting don’t affect speed, memory use or other aspects of the program 
  
## Formatting Blocks in C#
- Put **{** and **}** alone on a line under the corresponding parent block
- Indent the block contents by a single [Tab]
  - Visual Studio will replace the [Tab] with 4 spaces
- _Example_:

```cs
if (some condition)
{
    // Block contents indented by a single [Tab]
    // VS will replace the [Tab] with 4 spaces
}
```

## Formatting Blocks in JS
- Put **{** at the end of the block and **}** alone on a line under the corresponding parent block
- Indent the block contents by a single [Tab]
  - [tab] or spaces depends on the team style
- _Example_:

```cs
if (some condition) {
    // Block contents indented by a single [Tab]
    // Choosing between [tab] and spaces depends
    //  on project formatting style
}
```

## Why are Brackets <br /> Obligatory?
```cs
x = 3+4 * 2+7;
```
```cs
x = (3 + 4) * (2 + 7);
```

# Methods
## Empty Lines between Methods
- Use empty line for separation between methods:

```cs
public class Factorial
{
  private static ulong CalcFactorial(uint num)
  {
    	if (num == 0) return 1;
    	else return num * CalcFactorial(num - 1);
  }

  static void Main()
  {
    	ulong factorial = CalcFactorial(5);
			Console.WriteLine(factorial);
  }
}
```

## Methods Indentation
- Methods should be indented with a single [Tab] from the class body
- Methods body should be indented with a single [Tab] as well

```cs
public class Indentation_Example_
{
    private int Zero()
    {
        return 0;
    }
}
```

## Brackets in Methods Declaration
- Brackets in the method declaration should be formatted as follows:

```cs
private static ulong CalcFactorial(uint num)
```

- Don't  use spaces between the brackets:

```cs
private static ulong CalcFactorial ( uint num )
private static ulong CalcFactorial (uint num)
```

- The same applies for **if**-conditions and **for**-loops:

```cs
if (condition) { … }

for (int i = 0; i < 10; i++) { … }
```

## Separating Parameters
- Separate method parameters by comma followed by a space
  - Don't put space before the comma
  - Correct examples:
```cs
private void RegisterUser(string username, string password);
RegisterUser("academy", "s3cr3t!p@ssw0rd");
```

  - Incorrect examples:
```cs
private void RegisterUser(string username,string password)
private void RegisterUser(string username ,string password)
private void RegisterUser(string username , string password)
```


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
## Empty Lines
- Use an empty line to separate logically related sequences of lines:

```cs
private List<Report> PrepareReports()
{
    List<Report> reports = new List<Report>();

    // Create incomes reports
    Report incomesSalesReport = PrepareIncomesSalesReport();
    Report incomesSupportReport = PrepareIncomesSupportReport();
    reports.Add(incomesSalesReport, incomesSupportReport);

    // Create expenses reports
    Report expensesPayrollReport = PrepareExpensesPayrollReport();
    Report expensesMarketingReport = PrepareExpensesMarketingReport();
    reports.Add(expensesPayrollReport, expensesMarketingReport);

    return reports;
}
```
# Formatting Types
- Formatting classes / structures / interfaces / enumerations
  - Indent the class body with a single [Tab]
  - Use the following order of definitions:
    - Constants, delegates, inner types, fields, constructors, properties, methods
    - Static members, public members, protected members,  internal members, private members
  - The above order of definitions is not the only possible correct one

# Formatting Types  <br /> – _Example in C#_

```cs
public class Dog
{
    // Static variables
    public const string SPECIES = "Canis Lupus Familiaris";

		// Instance variables
    private int age;

		// Constructors
    public Dog(string name, int age)
    {
        this.Name = name;
        this.Аge = age;
    }
    
		// Properties
    public string Name { get; set; }

    // Methods
    public void Breath()
    {
        // TODO: breathing process
    }

    public void Bark()
    {
        Console.WriteLine("wow-wow");
    }
}
```

# Formatting Conditional Statements and Loops
- Formatting conditional statements and loops
  - Always use **{ }** block after **if** / **for** / **while**, even when a single operator follows
  - Indent the block body after **if** / **for** / **while**
  - Always put a new line after a **if** / **for** / **while** block!
  - Always put the **{** on the next line (in C#)
  - Always put the **{** on the same line (in JavaScript)
  - Never indent with more than one [Tab]

## Conditional Statements and Loops Formatting <br/> – _Examples in C#_

- Correct examples:
```cs
for (int i = 0; i < 10; i++)
{
    Console.WriteLine("i={0}", i);
}
```

- Incorrect examples:

```cs
for (int i = 0; i < 10; i++)
  Console.WriteLine("i={0}", i);

for (int i = 0; i < 10; i++) Console.WriteLine("i={0}", i);

for (int i = 0; i < 10;) {
    Console.WriteLine("i={0}", i);  i++; Console.WriteLine();
}
```

## Using Empty Lines
- Empty lines are used to separate logically unrelated parts of the source code
  - Don't put empty lines when not needed!

```cs
public static void PrintList(List<int> ints)
{
    Console.Write("{ ");
    foreach (int item in ints)
    {
        Console.Write(item);
        Console.Write(" ");
    }

    Console.WriteLine("}");
}

static void Main()
{
    // …
```   

# Misplaced Empty Lines – _Example_

```cs
for (int i = 0; i < 10;)
{
    Console.WriteLine("i={0}", i);  





		i++;


		Console.WriteLine();
}
```

## Breaking Long Lines
- Break long lines after punctuation
- Indent the second line by single [Tab]
- Do not additionally indent the third line
- _Examples_:

```cs
if (matrix[x, y] == 0 || matrix[x-1, y] == 0 ||
    matrix[x+1, y] == 0 || matrix[x, y-1] == 0 ||
    matrix[x, y+1] == 0)
{ …

public void GetAllAbstractPaintings()
{
	   var paintings = this.Database.Paintings.All()
		 .Where(x => x.PaintingStyle == PaintingStyleType.Abstract)
		 .OrderBy(x => x.Price)
		 .ThenBy(x => x.DateCreated)
		 .Select(x => x.OriginalPaintingPath)
		 .ToList();
}
```  

## Incorrect ways to break long lines (in C#_)

```cs
if (matrix[x, y] == 0 || matrix[x-1, y] ==
  0 || matrix[x+1, y] == 0 || matrix[x,
  y-1] == 0 || matrix[x, y+1] == 0)
{ …
```

```cs
if (matrix[x, y] == 0 || matrix[x-1, y] == 0 ||
      matrix[x+1, y] == 0 || matrix[x, y-1] == 0 ||
      matrix[x, y+1] == 0)
{ …
```

```cs
DictionaryEntry<K, V> newEntry
  = new DictionaryEntry<K, V>(oldEntry
  .Key, oldEntry.Value);
```

## Breaking Long Lines <br/> in C# and JavaScript
- In C# use single [Tab] after breaking a long line:

```cs
if (matrix[x, y] == 0 || matrix[x-1, y] == 0 ||
    matrix[x+1, y] == 0 || matrix[x, y-1] == 0 ||
    matrix[x, y+1] == 0)
{
    matrix[x, y] == 1;
}
```

- In JavaScript use double [Tab] in the carried long lines:

```cs
if (matrix[x, y] == 0 || matrix[x-1, y] == 0 ||
       matrix[x+1, y] == 0 || matrix[x, y-1] == 0 ||
       matrix[x, y+1] == 0) {
    matrix[x, y] == 1;
}
```

# Alignments
- All types of alignments are considered harmful
  - Alignments are hard-to-maintain!
  - Modifying one line of code shouldn’t require modifying several others
- Incorrect examples:  

```cs
public void NotCool()
{
	var student          = new Student("Ivan", "Kolev", 21);
	var studentGrades    = new List<int>() { 2, 3, 4, 5, 6 };
	var school           = new SMG("Kopernik");
	var studenstInSchool = new List<Student>();
}

```

# Code Documentation and Comments in the Program
## Revealing the Secrets of Self-Documenting Code

## What is Project Documentation?
- Consists of documents and information
  - Both inside the source-code and outside
- **External documentation**
  - At a higher level compared to the code
  - Problem definition, requirements, architecture, design, project plans, test plans. etc.
- **Internal documentation**
  - Lower-level – explains a class,method or a piece of code
  
## Programming Style
- Main contributor to code-level documentation
  - The program structure
  - Straight-forward, easy-to-read and easily understandable code
  - Good naming approach
  - Clear layout and formatting
  - Clear abstractions
  - Minimized complexity
  - Loose coupling and strong cohesion

## Bad Comments – _Example_
```cs
public static List<int> FindPrimes(int start, int end)
{
    // Create new list of integers
    List<int> primesList = new List<int>();
    // Perform a loop from start to end
    for (int num = start; num <= end; num++)
    {
        // Declare boolean variable, initially true
        bool prime = true;
        // Perform loop from 2 to sqrt(num)
        for (int div = 2; div <= Math.Sqrt(num); div++)
        {
            // Check if div divides num with no remainder
            if (num % div == 0)
            {
                // We found a divider -> the number is not prime
                prime = false;
                // Exit from the loop
                break;
            }
            // Continue with the next loop value
  }

  // Check if the number is prime
  if (prime)
  {
      // Add the number to the list of primes
      primesList.Add(num);
  }
}

// Return the list of primes
return primesList;
}


```

## Self-Documenting Code – _Example_

```cs
public static List<int> FindPrimes(int start, int end)
{
  List<int> primesList = new List<int>();
  for (int num = start; num <= end; num++)
  {
    bool isPrime = IsPrime(num);
    if (isPrime)
    {
      primesList.Add(num);
    }
  }
  return primesList;
}
```

Good code does not need comments. It is self-explaining.

```cs
private static bool IsPrime(int num)
{
  bool isPrime = true;
  int maxDivider = Math.Sqrt(num);
  for (int div = 2; div <= maxDivider; div++)
  {
    if (num % div == 0)
    {
      // We found a divider -> the number is not prime
      isPrime = false;
      break;
    }
  }
  return isPrime;
}
```
Good methods have good name and are easy to read and understand.
This comment explain non-obvious details. It does not repeat the code.

## Bad Programming Style – _Example_
```cs
for (i = 1; i <= num; i++)
{
    meetsCriteria[i] = true;
}
for (i = 2; i <= num / 2; i++)
{
    j = i + i;
while (j <= num)
{
        meetsCriteria[j] = false;
        j = j + i;
    }
}
for (i = 1; i <= num; i++)
{
    if (meetsCriteria[i])
    {
        Console.WriteLine(i + " meets criteria.");
    }
}
```

Uninformative variable names. Crude layout.

## Good Programming Style – _Example_

```cs
for (primeCandidate = 1; primeCandidate <= num; primeCandidate++)
{
    isPrime[primeCandidate] = true;
}

for (int factor = 2; factor < (num / 2); factor++)
{
    int factorableNumber = factor + factor;
    while (factorableNumber <= num)
    {
        isPrime[factorableNumber] = false;
        factorableNumber = factorableNumber + factor;
    }
}

for (primeCandidate = 1; primeCandidate <= num; primeCandidate++)
{
    if (isPrime[primeCandidate])
    {
        Console.WriteLine(primeCandidate + " is prime.");
    }
}
```

## Self-Documenting Code
- Code that relies on **good programming style**
  - To carry major part of the information intended for the documentation
- Self-documenting code fundamental principles

```
The best documentation is the code itself.
```

```
Make the code self-explainable
and self-documenting, easy to read and understand.
```

```
Do not document bad code, rewrite it!
```

## Self-Documenting Code Checklist
- **Classes**
  - Does the class’s interface present a consistent abstraction?
  - Does the class’s interface make obvious how you should use the class?
  - Is the class well named, and does its name describe its purpose?
  - Can you treat the class as a black box?
  - Do you reuse instead of repeating code?

- **Methods**
  - Does each routine’s name describe exactly what the method does?
  - Does each method perform one well-defined task with minimal dependencies?
  - 
- **Data Names**
  - Are type names descriptive enough to help document data declarations?
  - Are variables used only for the purpose for which they’re named?
  - Does naming conventions distinguish among type names, enumerated types,  named constants, local variables, class variables, and global variables?
  
- **Others**
  - Are data types simple so that they minimize complexity?
  - Are related statements grouped together?
   
# "Everything the Compiler Needs to Know is in the Code!"

## Effective Comments
- Effective comments **do not repeat the code**
  - They explain it at a higher level and reveal non-obvious details
- The best software documentation is the source code itself – keep it clean and readable!
- **Self-documenting code** is self-explainable and does not need comments
  - Simple design, small well named methods, strong cohesion and loose coupling, simple logic, good variable names, good formatting, …

# Effective Comments – Mistakes
- Misleading comments

```cs
// write out the sums 1..n for all n from 1 to num   
current = 1;
previous = 0;
sum = 1;   
for (int i = 0; i < num; i++)
{   
   Console.WriteLine( "Sum = " + sum );   
   sum = current + previous;   
   previous = current;   
   current = sum;
}

```

Can you guess that sum is equal to the ith Fibonacci number?

- Comments repeating the code:

```cs
// set product to "base"
product = base;

// loop from 2 to "num"
for ( int i = 2; i <= num; i++ )
{
   // multiply "base" by "product"  
   product = product * base;
}
Console.WriteLine( "Product = " + product );
```

- Poor coding style:

```cs
// compute the square root of Num using
// the Newton-Raphson approximation
r = num / 2;
while (abs(r - (num/r)) > TOLERANCE)
{
   r = 0.5 * (r + (num/r) );
}
Console.WriteLine( "r = " + r );
```

- Do not comment bad code, rewrite it 
 
# Key Points for Effective Comments
- Use commenting styles that don’t break down or discourage modification

```cs
//  Variable            Meaning
//  --------            -------
//  xPos .............. X coordinate position (in meters)
//  yPos .............. Y coordinate position (in meters)
//  zPos .............. Z coordinate position (in meters)
//  radius ............ The radius of the sphere where the
                        battle ship is located (in meters)
//  distance .......... The distance from the start position
                        (in meters)
```

- The above comments are **unmaintainable**

- Comment the code intent, not implementation details

```cs
// Scan char by char to find the command-word terminator ($)
done = false;
maxLen = inputString.Length;
i = 0;
while (!done && (i < maxLen))
{
  if (inputString[i] == '$')
  {
    done = true;
  }
  else
  {
    i++;
  }
}
```

- Focus your documentation efforts on the code

```cs
// Find the command-word terminator
foundTheTerminator = false;
maxCommandLength = inputString.Length();
testCharPosition = 0;
while (!foundTheTerminator &&
    (testCharPosition < maxCommandLength))
{
  if (inputString[testCharPosition] == COMMAND_WORD_TERMINATOR)
  {
    foundTheTerminator = true;
    terminatorPosition = testCharPosition;
  }
  else
  {
    testCharPosition = testCharPosition + 1;
  }
}
```

Better code &rarr; less comments

- Focus paragraph comments on the **why** rather than the **how**

```cs
// Establish a new account
if (accountType == AccountType.NewAccount)
{
   …
}
```

- Use comments to prepare the reader for what is to follow
- Avoid abbreviations

- Comment anything that gets around an error or an undocumented feature
  - E.g. **//** **This** **is** **workaround** **for** **bug** **#3712**
- Justify violations of good programming style
- Don’t comment tricky code – rewrite it
- Use built-in features for commenting
  - XML comments in C#
  - JavaDoc in Java, …

## General Guidelines for Higher Level Documentation
- Describe the design approach to the class
- Describe limitations, usage assumptions, and so on
- Comment the class interface (public methods / properties / events / constructors)
- Don’t document implementation details in the class interface
- Describe the purpose and contents of each file
- Give the file a name related to its contents

## <a id="xml-docs"></a>C# XML Documentation
- In C# you can document the code by XML tags in special comments
  - Directly in the source code
- For example:

```cs
/// <summary>
/// This class performs an important function.
/// </summary>
public class MyClass { }
```

- The XML doc comments are not **metadata**
  - Not included in the compiled assembly and not accessible through reflection

## XML Documentation Tags
- **&lt;summary>**
  - A summary of the class / method / object
- **&lt;param>**

    `<param name="name">description</param>`
  - Describes one of the parameters for a method
- **&lt;returns>**
  - A description of the returned value
- **&lt;remarks>**
  - Additional information (remarks)

- **&lt;c>** and **&lt;code>**
  - Gives you a way to indicate code
- **&lt;see>** and **&lt;seealso>** and cref
  - Code reference `<seealso cref="TestClass.Main"/>`
- **&lt;exception>**

    `<exception cref="type">description</exception>`
  - Lets you specify which exceptions can be thrown
- All tags: http://msdn.microsoft.com/en-us/library/5ast78ax.aspx

## XML Documentation Example

```cs
/// <summary>
/// The GetZero method. Always returns zero.
/// </summary>
/// <example>  
/// This sample shows how to call the <see cref="GetZero"/> method.
/// <code>
/// class TestClass  
/// {
///     static int Main()  
///     {
///         return GetZero();
///     }
/// }
/// </code>
/// </example>
public static int GetZero()
{
    return 0;
}
```

## C# XML Documentation
- Visual Studio will use the XML documentation for autocomplete
  - Automatically, just use XML docs
- Compiling the XML documentation:
  - Compile with **/doc** the to extract the XML doc into an external XML file
  - Use Sandcastle or other tool to generate CHM / PDF / HTML / other MSDN-style documentation
    - _Example_: http://www.ewoodruff.us/shfbdocs/

# Correct Use of Variables, Data, Expressions and Constants
## Correctly Organizing Data and Expressions

## Initially Assigned <br/> Variables in C&num;
- Static variables
- Instance variables of class instances
- Instance variables of initially assigned struct variables
- Array elements
- Value parameters
- Reference parameters
- Variables declared in a `catch` clause or a `foreach` statement

## Initially Unassigned <br/> Variables in C&num;
- Instance variables of initially unassigned struct variables
- Output parameters
  - Including the `this` variable of struct instance constructors
- Local variables
  - Except those declared in a `catch` clause or a `foreach` statement

## Guidelines for Initializing Variables
- When the problems can happen?
  - The variable has never been assigned a value
  - The value in the variable is outdated
  - Part of the variable has been assigned a value and a part has not
    - E.g. **Student** class has initialized name, but faculty number is left unassigned
- Developing effective techniques for avoiding initialization problems can save a lot of time

## Variable Initialization
- Initialize all variables before their first usage
  - Local variables should be manually initialized
  - Declare and define each variable close to where it is used
  - This C# code will result in compiler error:

```cs
int value;
Console.WriteLine(value);
```
  - We can initialize the variable at its declaration:

```cs
int value = 0;
Console.WriteLine(value);
```

- Pay special attention to **counters** and **accumulators**
  - A common error is forgetting to reset a counter or an accumulator

```cs
int sum = 0;
for (int i = 0; i < array.GetLength(0); i++)
{
  for (int j = 0; j < array.GetLength(1); j++)
  {
    sum = sum + array[i, j];
  }
  Console.WriteLine(
    "The sum of the elements in row {0} is {1}", sum);
}
```

- Check the need for reinitialization
  - Make sure that the initialization statement is inside the part of the code that’s repeated
- Check input parameters for validity
  - Before you assign input values to anything, make sure the values are reasonable

```cs
int input;
bool validInput =
  int.TryParse(Console.ReadLine(), out input);
if (validInput)
{
  …
}
```

## Partially Initialized Objects
- Ensure objects cannot get into partially initialized state
  - Make all fields private and require valid values for all mandatory fields in all constructors
  - _Example_: **Student** object is invalid unless it has **Name** and **FacultyNumber**

```cs
class Student
{
  private string name, facultyNumber;
  public Student(string name, string facultyNumber)
  { … }
}
```

## Variables – Other Suggestions
- Don't define **unused variables**
  - Compilers usually issues warnings
- Don't use variables with **hidden purpose**
  - Incorrect example:

```cs
int mode = 1;
…
if (mode == 1) …; // Read
if (mode == 2) …; // Write
if (mode == 3) …; // Read and write
```

  - Use enumeration instead:

```cs
enum ResourceAccessMode { Read, Write, ReadWrite }
```

## Returning Result from a Method
- Always assign the result of a method in some variable before returning it. Benefits:
  - Improved code **readability**
    - The returned value has self-documenting name
  - Simplified debugging
  - Example:

```cs
int salary = days * hoursPerDay * ratePerHour;
return salary;
```

  - Incorrect example:

```cs
return days * hoursPerDay * ratePerHour;
```

The intent of the formula is obvious
We can put a breakpoint at this line and check if the result is correct

# Scope, Lifetime, Span

## Scope of Variables
- **Scope** – a way of thinking about a variable’s celebrity status
  - How **famous** is the variable?
  - Global (static), member variable, local
  - Most famous variables can be used anywhere, less famous variables are much more restricted
  - The scope is often combined with **visibility**
- In C# and Java, a variable can also be visible to a package or a namespace

## Visibility of Variables
- Variables' **visibility** is explicitly set restriction regarding the access to the variable
  - `public, protected, internal, private`
- Always try to reduce maximally the variables scope and visibility
  - This reduces potential coupling
  - Avoid public fields (exception: `readonly` / `const` in C# / `static` `final` in Java)
  - Access all fields through `properties / methods`

## Exceeded Scope – _Example_

```cs
public class Globals
{
   public static int state = 0;
}
public class ConsolePrinter
{
   public static void PrintSomething()
   {
      if (Globals.state == 0)
      {
         Console.WriteLine("Hello.");
       }
      else
      {
         Console.WriteLine("Good bye.");
      }
   }
}
```

## Span of Variables
- Variable **span**
  - The of lines of code (LOC) between variable usages
  - **Average span** can be calculated for all usages
  - Variable span should be kept as low as possible
  - Define variables at their first usage, not earlier
  - Initialize variables as late as possible
  - Try to keep together lines using the same variable

`Always define and initialize variables just before their first use!`

## Variable Live Time
- Variable **live time**
  - The number of lines of code (LOC) between the first and the last variable usage in a block
  - Live time should be kept as low as possible
- The same rules apply as for minimizing span:
  - Define variables at their first usage
  - Initialize variables just before their first use
  - Try to keep together lines using the same variable

## Unneeded Large Variable Span and Live Time
## Keep Variables LiveAs Short a Time

- Advantages of short time and short span
  - Gives you an accurate picture of your code
  - Reduces the chance of initialization errors
  - Makes your code more readable

## Best Practices
- Initialize variables used in a loop immediately before the loop
- Don’t assign a value to a variable until just before the value is used
  - Never follow the old C / Pascal style of declaring variables in the beginning of each method
- Begin with the most restricted visibility
  - Expand the visibility only when necessary
- Group related statements together

## Group RelatedStatements – _Example_

```cs
void SummarizeData(…)
{
  …
  GetOldData(oldData, numOldData);
  GetNewData(newData, numNewData);
  totalOldData = Sum(oldData, numOldData);
  totalNewData = Sum(newData, numNewData);
  PrintOldDataSummary(oldData, totalOldData);
  PrintNewDataSummary(newData, totalNewData);
  SaveOldDataSummary(totalOldData, numOldData);
  SaveNewDataSummary(totalNewData, numNewData);
  …
}
```
- Six variables for just this short fragment
You have to keep track of **oldData**, **newData**, **numOldData**, **numNewData**, **totalOldData** and **totalNewData**

## Better Grouping– _Example_
- Easier to understand, right?

```cs
void SummarizeDaily( … )
{
  GetOldData(oldData, numOldData);
  totalOldData = Sum(oldData, numOldData);
  PrintOldDataSummary(oldData, totalOldData);
  SaveOldDataSummary(totalOldData, numOldData);
  …
  GetNewData(newData, numNewData);
  totalNewData = Sum(newData, numNewData);
  PrintNewDataSummary(newData, totalNewData);
  SaveNewDataSummary(totalNewData, numNewData);
  …
}
```

The two blocks are each shorter and  individually contain fewer variables

## Single Purpose
- Variables should have **single purpose**
  - Never use a single variable for multiple purposes!
  - Economizing memory is not an excuse
- Can you choose a good name for variable that is used for several purposes?
  - _Example_: variable used to count students or to keep the average of their grades
  - Proposed name: `studentsCountOrAvgGrade`
 
## Variables Naming
- The name should describe the object clearly and accurately, which the variable represents
  - Bad names: **r18pq, __hip, rcfd, val1, val2**
  - Good names: **account**, **blockSize**, **customerDiscount**
- Address the problem, which the variable solves – "what" instead of "how"
  - Good names: **employeeSalary**, **employees**
  - Bad names: **myArray, customerFile, customerHashTable**
  - 
## Poor and Good Variable Names
```cs
x = x - xx;
xxx = aretha + SalesTax(aretha);
x = x + LateFee(x1, x) + xxx;
x = x + Interest(x1, x);
```

- What do x1, xx, and xxx mean?
- What does aretha mean ?

```cs
balance = balance - lastPayment;
monthlyTotal = NewPurchases + SalesTax(newPurchases);
balance = balance + LateFee(customerID, balance) +
  monthlyTotal;
balance = balance + Interest(customerID, balance);
```

## Naming Considerations
- Naming depends on the scope and visibility
  - Bigger scope, visibility, longer lifetime &rarr;longer and more descriptive name:

```cs
protected Account[] mCustomerAccounts;
```

  - Variables with smaller scope and shorter lifetime can be shorter:

```cs
for (int i=0; i<customers.Length; i++) { … }
```

- The enclosing type gives a context for naming:

```cs
class Account { Name: string { get; set; } }
// not AccountName
```

## Optimum Name Length
- Somewhere between the lengths of x and maximumNumberOfPointsInModernOlympics
- Optimal length – 10 to 16 symbols     
  - Too long

```cs
numberOfPeopleOfTheBulgarianOlympicTeamFor2012
```
  - Too short

```cs
а, n, z
```

  - Just right

```cs
numTeamMembers, teamMembersCount
```

## Naming Specific Data Types
- Naming counters

```cs
UsersCount, RolesCount, FilesCount
```

- Naming variables for state

```cs
ThreadState, TransactionState
```

- Naming temporary variables
  - Bad examples:

```cs
a, aa, tmpvar1, tmpvar2
```

  - Good examples:

```cs
index, value, count
```

- Name Boolean variables with names implying "Yes / No" answers

```cs
canRead, available, isOpen, valid
```

- Booleans variables should bring "truth" in their name
  - Bad examples:

```cs
notReady, cannotRead, noMoreData
```
  - Good examples:

```cs
isReady, canRead, hasMoreData
```

- Naming enumeration types
  - Use build in enumeration types (**Enum**)

```cs
Color.Red, Color.Yellow, Color.Blue
```

  - Or use appropriate prefixes (e.g. in JS / PHP)

```cs
colorRed, colorBlue, colorYellow
```

- Naming constants – use capital letters

```cs
MAX_FORM_WIDTH, BUFFER_SIZE
```

- C# constants should be in PascalCase:

```cs
Int32.MaxValue, String.Empty, InvariantCulture
```

## Naming Convention
- Some programmers resist to followstandards and conventions
  - But why?
- Conventions benefits
  - Transfer knowledge across projects
  - Helps to learn code more quickly on a new project
  - Avoid calling the same thing by two different names

- When should we use a naming convention?
  - Multiple developers are working on the same project
  - The source code is reviewed by other programmers
  - The project is large
  - The project will be long-lived
- You always benefit from having some kind of naming convention!

## Language-Specific Conventions
- C# and Java / JavaScript conventions
  - **i** and **j** are integer indexes
  - Constants are in **ALL_CAPS** separated by underscores (sometimes **PascalCase** in C#)
  - Method names use uppercase in C# and lowercase in JS for the first word
  - The underscore **_** is not used within names
    - Except for names in all caps

## Standard Prefixes
- Hungarian notation – not used
- Semantic prefixes (ex. **btnSave**)
  - Better use **buttonSave**
- Do not miss letters to make name shorter
- Abbreviate names in consistent way throughout the code
- Create names, which can be pronounced(not like btnDfltSvRzlts)
- Avoid combinations, which form another word or different meaning (ex. preFixStore)

## Kinds of Names to Avoid
- Document short names in the code
- Remember, names are designed for the people, who will read the code
  - Not for those who write it
- Avoid variables with similar names, but different purpose

```cs
UserStatus / UserCurrentStatus
```

- Avoid names, that sounds similar

```cs
decree / degree / digRee
```

- Avoid digits in names

- Avoid words, which can be easily mistaken
  - E.g. adsl, adcl, adctl, atcl
- Avoid using non-English words
- Avoid using standard types and keywords in the variable names
  - E.g. int, class, void, return
- Do not use names, which has nothing common with variables content
- Avoid names, that contains hard-readable symbols / syllables, e.g. Csikszentmihalyi

## Avoid Complex Expressions
- Never use complex expressions in the code!
  - Incorrect example:

```cs
for (int i=0; i<xCoords.length; i++) {
  for (int j=0; j<yCoords.length; j++) {
    matrix[i][j] =
      matrix[xCoords[findMax(i)+1]][yCoords[findMin(j)-1]] *
      matrix[yCoords[findMax(j)+1]][xCoords[findMin(i)-1]];
  }
}
```  
- Complex expressions are evil because:
  - Make code hard to read and understand, hard to debug, hard to modify and hard to maintain
What shall we do if we get at this line **IndexOutOfRangeException**?
There are 10 potential sources of **IndexOutOfRangeException** in this expre

## Simplifying Complex Expressions

```cs
for (int i = 0; i < xCoords.length; i++)
{
  for (int j = 0; j < yCoords.length; j++)
  {
    int maxStartIndex = findMax(i) + 1;
    int minStartIndex = findMin(i) - 1;
    int minXcoord = xCoords[minStartIndex];
    int maxXcoord = xCoords[maxStartIndex];
    int minYcoord = yCoords[minStartIndex];
    int maxYcoord = yCoords[maxStartIndex];
    int newValue =
      matrix[maxXcoord][minYcoord] *
      matrix[maxYcoord][minXcoord];
    matrix[i][j] = newValue;
  }
}
```

## Avoid Magic Numbers and Strings
- What is **magic number** or **value**?
  - Magic numbers / values are all literals different than `0, 1, -1, null` and `""` (empty string)
- Avoid using magic numbers / values
  - They are **hard to maintain**
    - In case of change, you need to modify all occurrences of the magic number / constant
  - Their meaning is not obvious
    - _Example_: what the number 1024 means?

## The Evil Magic Numbers

```cs
public class GeometryUtils
{
  public static double CalcCircleArea(double radius)
  {
    double area = 3.14159265 * radius * radius;
    return area;
  }
  public static double CalcCirclePerimeter(double radius)
  {
    double perimeter = 6.28318531 * radius;
    return perimeter;
  }
  public static double CalcElipseArea(double axis1, double axis2)
  {
    double area = 3.14159265 * axis1 * axis2;
    return area;
  }
}
```

## Turning MagicNumbers into Constants

```cs
public class GeometryUtils
{
   public const double PI = 3.14159265;
   public static double CalcCircleArea(double radius)
   {
      double area = PI * radius * radius;
      return area;
   }
   public static double CalcCirclePerimeter(double radius)
   {
      double perimeter = 2 * PI * radius;
      return perimeter;
   }
   public static double CalcElipseArea(
    double axis1, double axis2)
   {
      double area = PI * axis1 * axis2;
      return area;
   }
}
```

## Constants in C#
- There are two types of constants in C#
  - Compile-time constants:

```cs
public const double PI = 3.14159206;
```

- Replaced with their value during compilation
- No field stands behind them
  - Run-time constants:

```cs
public static readonly string ConfigFile = "app.xml";
```

- Special fields initialized in the static constructor
- Compiled into the assembly like any other class member

## Constants in JavaScript
- JS does not support constants
  - Simulated by variables / fields in **ALL_CAPS**:

```cs
var PI = 3.14159206;

var CONFIG =
{
  COLOR : "#AF77EE",
  DEFAULT_WIDTH : 200,
  DEFAULT_HEIGHT : 300
};

document.getElementById("gameField").style.width =
  CONFIG.DEFAULT_WIDTH;
document.getElementById("gameField").style.
  backgroundColor = CONFIG.COLOR;
```

## When to Use Constants?
- Constants should be used in the following cases:
  - When we need to use numbers or other values and their logical meaning and value are not obvious
  - File names

```cs
public static readonly string SettingsFileName =
"ApplicationSettings.xml";
```

  - Mathematical constants

```cs
public const double E = 2.7182818284;
```

  - Bounds and ranges

```cs
public const int READ_BUFFER_SIZE = 5 * 1024 *1024;
```

## When to Avoid Constants?
- Sometime it is better to keep the magic values instead of using a constant
  - **Error messages** and **exception descriptions**
  - **SQL commands** for database operations
  - Titles of **GUI elements**(labels, buttons, menus, dialogs, etc.)
- For internationalization purposes use **resources**, not constants
  - Resources are special files embedded in the assembly / JAR file, accessible at runtime

