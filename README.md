# High-Quality-Code
## Any fool can write code that a computer can understand. Good programmers write code that humans can understand.  

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
  - Is the software UI easy-to-use?
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

  # <a id="complexity"></a>Managing Complexity
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

#   Code Formatting
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

# Keys to being an effective programmer: - Maximizing the portion of a program that you can **safely ignore** - While working on any one section of code - Most practices discussed later propose ways to achieve this important goal
