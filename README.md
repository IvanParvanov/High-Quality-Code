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

<div class="fragment balloon" style="top:26.58%; left:67.72%; width:30.28%">Better code &rarr; less comments</div>

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




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # C# XML Documentation Comments -->


<!-- attr: { id:'xml-docs', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="xml-docs"></a>C# XML Documentation
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


<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size:0.95em' } -->
# XML Documentation Tags
- **&lt;summary>**
  - A summary of the class / method / object
- **&lt;param>**

    `<param name="name">description</param>`
  - Describes one of the parameters for a method
- **&lt;returns>**
  - A description of the returned value
- **&lt;remarks>**
  - Additional information (remarks)


<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size:0.9em' } -->
<!-- # XML Documentation Tags -->

- **&lt;c>** and **&lt;code>**
  - Gives you a way to indicate code
- **&lt;see>** and **&lt;seealso>** and cref
  - Code reference `<seealso cref="TestClass.Main"/>`
- **&lt;exception>**

    `<exception cref="type">description</exception>`
  - Lets you specify which exceptions can be thrown
- All tags: http://msdn.microsoft.com/en-us/library/5ast78ax.aspx

<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size:0.9em' } -->
# XML Documentation Example

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


