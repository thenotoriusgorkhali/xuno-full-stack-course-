# xuno-full-stack-course-
Basic Introduction of Computer Programming

Computer Programming
             Computer programming is the process of designing, writing, testing, debugging, and maintaining the code that allows computers to perform specific tasks. It involves creating a set of instructions (a program) for a computer to follow, using a programming language.
Key Concept 
•	Algorithm
•	Data Structure
•	Control Structure
•	Functions
•	Variable
•	Object Oriented Programming
Types Of Computer Programming
 Software Programming: 
                Web Programming:
•	Purpose: Build websites and web apps.
•	Languages: HTML, CSS, JavaScript (Frontend); Python, Node.js, PHP (Backend).
•	Example: E-commerce site.
Mobile Programming:
•	Purpose: Develop apps for smartphones.
•	Languages: Java, Kotlin (Android); Swift (iOS); React Native (Cross-platform).
•	Example: Fitness app.

Server Programming:
•	Purpose: Backend services and APIs.
•	Languages: Python, Node.js, Java, Ruby.
•	Example: REST API for mobile app.
  PC Programming:
•	Purpose: Build software for personal computers.
•	Languages: C++, Java, Python.
•	Example: Desktop app like a text 
 
Hardware Programming
Embedded Systems:
•	Purpose: Control specific devices (e.g., washing machines, cars).
•	Languages: C, C++, MicroPython.
•	Example: Arduino controlling sensors.
IoT (Internet of Things):
•	Purpose: Connect devices to the internet.
•	Languages: C, Python, JavaScript.
•	Example: Smart home devices like thermostats.


Programming Language
•	Compiler
•	Interpreter
Compiler: A compiler translates code from a high-level programming language into machine code before the program runs. Language like C, C++, C#, and Java.
Interpreter: An interpreter translates code written in a high-level programming language into machine code line-by-line as the code runs. Language like Python, JavaScript, Perl, and BASIC.
How Python Works:
Python is an interpreted language, meaning it doesn’t require a separate compilation step. Here's a simplified flow of how Python works:
1.	Write Python Code:
You write your Python code in a .py file (e.g., script.py).
2.	Python Interpreter:
When you run the Python code, the Python interpreter processes it. The interpreter is a program that reads your code line by line and converts it into machine code that the computer can understand.
3.	Lexical Analysis:
The Python interpreter first breaks the code into tokens (small pieces like keywords, operators, etc.).
4.	Bytecode Compilation:
The interpreter converts the tokens into bytecode, a low-level, platform-independent representation of the code.
5.	Execution:
The Python Virtual Machine (PVM) executes the bytecode. The PVM runs the bytecode instructions and interacts with the operating system and hardware to produce results (e.g., printing text, performing calculations).
6.	Libraries & Modules:
If your code uses external libraries (e.g., math, numpy), the interpreter loads and executes them when needed.

Python Process Summary:
•	Write Code → Interpreter → Tokens → Bytecode → Python Virtual Machine (PVM) → Execution





Erro Type 
•	Compile Time Error
•	Run Time Error

In Python, compile-time errors are errors that occur when the Python interpreter encounters problems while trying to compile your code before execution. These errors prevent the code from running.
Syntax Errors:
•	Occur when the Python code is not written in a valid syntax.
•	Example: Missing a colon, unmatched parentheses, or improper indentation.
Indentation Errors:
•	Occur when the indentation is not consistent (Python is sensitive to indentation).
•	4 space should be left ….
Import Errors:
•	Occur when you try to import a module that doesn’t exist or isn’t installed.
import nonexistent_module  # Module not found error
Name Errors:
•	Occur when you try to use a variable or function before it is defined.
print(x) # NameError: name 'x' is not defined
Type Errors (In some cases):
•	Occur when there’s a mismatch between the expected type and the type used (e.g., trying to add a string to an integer).
x = "hello" + 5  # TypeError: can only concatenate str (not "int") to str

How Python Handles Compile-Time Errors:
When the Python interpreter detects a compile-time error, it stops and displays an error message, pointing out the type of error and its location in the code (line number).
Runtime Errors in Python
Runtime errors occur during the execution of the program. These errors are not detected by the Python interpreter during the compilation (or parsing) phase, but they happen when the code is running and something unexpected occurs.

Types of Runtime Errors in Python:
1.	Division by Zero:
o	Trying to divide a number by zero causes a ZeroDivisionError. 
o	x = 10 / 0   # ZeroDivisionError: division by zero

2.	 File Not Found:
•	Trying to open a file that doesn't exist causes a FileNotFoundError.
•	with open("nonexistent_file.txt", "r") as file:  # FileNotFoundError
    content = file.read()

3. Index Out of Range:
•	Accessing an index in a list that is out of range causes an IndexError.
      lst = [1, 2, 3]
     print(lst[5])  # IndexError: list index out of   range

4.Type Mismatch:
•	Performing operations on incompatible data types can cause a TypeError.
x = "hello" + 5  # TypeError: can only concatenate str (not "int") to str

5.Value Error:
•	Trying to convert a string to a number when the string isn't a valid number results in a ValueError.
x = int("abc")  # ValueError: invalid literal for int() with base 10: 'abc'

KeyError:
•	Trying to access a dictionary key that doesn't exist results in a KeyError.
my_dict = {'name': 'Alice'}
print(my_dict['age'])  # KeyError: 'age'

AttributeError:
•	Occurs when trying to access an attribute or method that doesn't exist on an object.
obj = 5
obj.append(3)  # AttributeError: 'int' object has no attribute 'append'

Memory Errors:
•	Running out of memory (e.g., when creating a huge list) can cause a MemoryError.
lst = [1] * (10**10)  # MemoryError


How Python Handles Runtime Errors:
When a runtime error occurs, Python will stop executing the program and print an error message along with the type of error and the line number where the error occurred.

Example of a Runtime Error:
x = 10
y = 0
print(x / y)  # Will raise ZeroDivisionError during runtime

Error Message : 
ZeroDivisionError: division by zero


What is Memory Allocation?
Memory allocation is the process of assigning specific portions of a computer's memory (RAM) to variables, objects, or data so they can store and manage values while a program runs.
In simple terms:
•	Memory allocation is like giving your data a "space" in the computer's brain (RAM) to live and operate.
•	This space is identified by a memory address, which is like a unique "house address" for your data in the RAM.


How Does Python Handle Memory Allocation?
Python abstracts away many low-level memory management tasks. It has two main components for memory allocation:
1.	Stack Memory:
o	Used for managing function calls, variables, and references.
o	It’s smaller and operates faster.
o	Example: When you assign a variable (x = 10), the reference to the value 10 is stored in stack memory.
2.	Heap Memory:
o	Used for storing actual objects and data.
o	It’s larger and dynamically managed.
o	Example: If you create a list (my_list = [1, 2, 3]), the list is stored in heap memory, and the variable my_list is just a reference to that object.

Key Terms in Memory Allocation
1.	Memory Address:
o	Every object in memory has a unique identifier (its memory address).
o	You can check it using Python’s id() function:
x = 10
print(id(x))  # e.g., 140437267276368

2.Reference:
•	Variables in Python don’t store data directly; they store a reference to the memory address of the object.
x = [1, 2, 3]
y = x  # Both x and y point to the same list object
print(id(x), id(y))  # Same memory address

Garbage Collection:
•	Python automatically removes unused objects from memory when no variables are referencing them (using a mechanism called garbage collection).
x = [1, 2, 3]
x = None  # The list [1, 2, 3] is now "orphaned" and will be deleted from memory.


Mutable Objects
Mutable objects can be modified after their creation. Their contents can be changed in place without changing their identity (memory address).
Examples of Mutable Objects
1.	List
my_list = [1, 2, 3]
print("Before modification:", my_list)
print("Memory address before:", id(my_list))

my_list.append(4)  # Modify the list
print("After modification:", my_list)
print("Memory address after:", id(my_list))  # Same memory address


Output 
Before modification: [1, 2, 3]
Memory address before: 140438612346496
After modification: [1, 2, 3, 4]
Memory address after: 140438612346496


2 .Dictionary
my_dict = {"a": 1, "b": 2}
print("Before modification:", my_dict)
print("Memory address before:", id(my_dict))

my_dict["c"] = 3  # Modify the dictionary
print("After modification:", my_dict)
print("Memory address after:", id(my_dict))  # Same memory address


 Output:
Before modification: {'a': 1, 'b': 2}
Memory address before: 140438612346880
After modification: {'a': 1, 'b': 2, 'c': 3}
Memory address after: 140438612346880


3.Set
my_set = {1, 2, 3}
print("Before modification:", my_set)
print("Memory address before:", id(my_set))

my_set.add(4)  # Modify the set
print("After modification:", my_set)
print("Memory address after:", id(my_set))  # Same memory address

output :
Before modification: {1, 2, 3}
Memory address before: 140438612347648
After modification: {1, 2, 3, 4}
Memory address after: 140438612347648


Immutable Objects
Immutable objects cannot be modified after their creation. Any modification creates a new object with a different memory address.
Examples of Immutable Objects
1.	Integer
x = 10
print("Before modification:", x)
print("Memory address before:", id(x))

x = x + 5  # This creates a new integer object
print("After modification:", x)
print("Memory address after:", id(x))  # Different memory address


Output
Before modification: 10
Memory address before: 140438612346816
After modification: 15
Memory address after: 140438612346912

String
  my_string = "hello"
print("Before modification:", my_string)
print("Memory address before:", id(my_string))

my_string = my_string + " world"  # Creates a new string object
print("After modification:", my_string)
print("Memory address after:", id(my_string))  # Different memory address


Tuples 
my_tuple = (1, 2, 3)
print("Before modification:", my_tuple)
print("Memory address before:", id(my_tuple))

new_tuple = my_tuple + (4,)  # Creates a new tuple object
print("After modification:", new_tuple)
print("Memory address after:", id(new_tuple))  # Different memory address


Output 
Before modification: (1, 2, 3)
Memory address before: 140438612347712
After modification: (1, 2, 3, 4)
Memory address after: 140438612347856



Comparison Table
Feature	Mutable	Immutable
Can be modified?	Yes	No
Examples	list, dict, set	int, str, tuple
Memory address changes?	No	Yes (new object is created)
Performance	Slower for frequent changes	Faster for fixed values
Hashable?	No	Yes



Why it Matters
1.	Hashing: Immutable objects are hashable and can be used as keys in dictionaries or elements in sets, while mutable objects cannot.
# Example with immutable tuple (hashable)
my_dict = {(1, 2): "value"}
print(my_dict[(1, 2)])  # Output: value

# Example with mutable list (not hashable)
# my_dict = {[1, 2]: "value"}  # Raises TypeError: unhashable type: 'list'

Thread-Safe: Immutable objects are safer in multi-threaded environments since their value cannot change unexpectedly.

Noted
In mutable objects, the memory allocation does not change even when their content is modified. This means the object is updated in-place without creating a new memory address.
In immutable objects, any change creates a new object in memory (i.e., a new memory address), as their content cannot be altered in place.

Let’s Summarize:
Object Type	Content Change	Memory Address	Examples
Mutable	Yes (In-Place)	Stays the Same	list, dict, set
Immutable	No (New Object Created)	Changes	int, str, tuple





Why Memory Allocation Matters
Efficiency:
Mutable objects save memory by modifying data in place, while immutable objects ensure data integrity by creating new objects.
Debugging:
Knowing how memory works helps you debug issues like unintended changes to mutable objects shared across references.
Optimization:
Understanding memory allocation allows you to write better code, e.g., avoiding unnecessary new object creation for immutable types.


JavaScript 
JavaScript is a high-level, interpreted programming language that works as the core scripting language for web browsers

How does JavaScript actually work?

1.	Write Code:
o	You write JavaScript code in a .js file or embed it directly into an HTML file using <script> tags.
2.	JavaScript Engine:
o	The JavaScript Engine (e.g., V8 in Chrome, SpiderMonkey in Firefox) takes the JavaScript code and prepares to execute it. The engine is responsible for parsing, compiling, and executing JavaScript.
3.	Parsing:
o	The JavaScript Engine reads the code and breaks it down into tokens. This is called lexical analysis, where the raw code is split into smaller pieces like keywords, identifiers, and operators.
4.	Abstract Syntax Tree (AST):
o	The tokens are organized into an Abstract Syntax Tree (AST), which represents the hierarchical structure of the program. This step is part of syntactical analysis, where the engine understands the program’s logic.
5.	Bytecode / Machine Code:
o	The engine then converts the AST into bytecode or directly into machine code (depending on the engine). In modern engines like V8, this is done using Just-In-Time (JIT) compilation, which compiles code as it runs to make it more efficient.
6.	Execution:
o	The JavaScript Engine begins executing the bytecode/machine code. The code is executed line by line in a single thread, following the sequence of statements.
7.	Event Loop:
o	JavaScript uses an event-driven, non-blocking model, where tasks (like handling user clicks or responding to network requests) are handled by the event loop. The event loop checks for tasks waiting to be executed and places them in the call stack.
8.	Execution of Async Code:
o	For asynchronous operations (e.g., setTimeout, fetch requests), the event loop handles tasks that are offloaded to the Web APIs (in browsers) or external systems (like Node.js). Once the task completes, the callback is placed in the task queue, waiting for the event loop to push it to the call stack.
 
Error Type in JS:
                     It is same as python as above.

Compile time error vs Runtime error

Aspect	Compile-Time Errors	Runtime Errors
When they occur	During the compilation (before the program runs)	During the execution (while the program is running)
Cause	Syntax issues, type mismatches, missing imports, etc.	Invalid operations (e.g., dividing by zero, null references)
Effect	The program doesn't compile, and you can’t run it at all	The program runs but crashes or behaves incorrectly at runtime
Example	Syntax error: missing semicolon, wrong variable type	Runtime error: null pointer dereference, array out of bounds
Solution	Fix the syntax or type issues and recompile	Handle exceptions, correct logic, and ensure valid inputs


Memory Allocation In JavaScript:
In JavaScript, memory allocation is primarily handled automatically through a process known as garbage collection. This means that JavaScript developers generally don't need to manually allocate or deallocate memory.

Primitive Types and Memory Allocation
•	Number
•	String
•	Boolean
•	Undefined
•	Null
•	Symbol (in newer JavaScript versions)
•	BigInt (for large integers)

For these types:
•	Value is stored directly in memory.
•	Immutable: Once assigned, the value cannot be changed. If you change a primitive variable, a new memory location is created for the new value.

Example :
            let a = 10;   // Memory is allocated for the number 10
let b = a;    // b gets a copy of the value of a (not a reference)
a = 20;       // a now points to a new memory location, but b still holds 10




2. Reference Types and Memory Allocation
•	Objects
•	Arrays
•	Functions
•	Dates
•	Regular expressions
For these types:
•	Memory is allocated dynamically (at runtime), and the variable holds a reference to the memory location, not the actual value.
•	When you assign one reference type variable to another, they both point to the same memory location.

Example:
  let obj1 = { name: "Alice" }; // obj1 holds a reference to the object in memory
let obj2 = obj1;              // obj2 now also refers to the same object as obj1
obj1.name = "Bob";            // Both obj1 and obj2 refer to the same object, so the change is reflected in both



FEATURE	STACK	HEAP
WHAT IT STORES	Primitive values	Objects, arrays, functions
SIZE	Fixed size, fast access	Dynamically allocated, slower
ACCESS PATTERN	   LIFO	Random access
LIFETIME	Cleared when function ends	 Cleared via Garbage Collection


Garbage Collection in JavaScript
JavaScript uses garbage collection to manage memory automatically. The garbage collector tracks which objects are no longer accessible (i.e., when there are no references to them) and frees up that memory.
Key Points:
•	Mark-and-Sweep Algorithm: JavaScript uses this algorithm to mark objects that are no longer referenced by any variable, then "sweeps" through memory to deallocate them.
•	Reachability: Objects that are still referenced by other objects or variables are considered reachable and will not be collected by the garbage collector.
•	Memory Leaks: These can occur if references to objects are unintentionally kept alive, causing memory that is no longer needed to stay allocated.

Example
function createObject() {
  let obj = { name: "Alice" };
  // After this function call, obj is no longer accessible
}
// obj is removed from memory once the function scope ends (if there are no other references to it)





Summary Table of Memory Allocation : Python vs. JavaScript

Type	Python (Stack or Heap)	JavaScript (Stack or Heap)
Primitive values	Stack	Stack
Class instances	Heap	Heap
Dictionaries/Sets	Heap	Heap
Objects	Heap	Heap
Function calls	Stack	Stack
References	Stack (to point to heap memory)	Stack (to point to heap memory)




ASCII VS UTF -8

ASCII (American Standard Code for Information Interchange):
ASCII is a character encoding standard that was originally designed for telecommunication and computer systems in the 1960s. It defines a set of 128 characters that includes:
•	Uppercase and lowercase English letters (A-Z, a-z)
•	Digits (0-9)
•	Basic punctuation marks (.,?!, etc.)
•	Control characters (such as carriage return, tab, etc.)
Example:
•	ASCII value of 'A' = 65
•	ASCII value of 'a' = 97
•	ASCII value of '1' = 49


 Character Range: ASCII can represent only 128 characters (0–127), which covers basic English letters, numbers, and a limited set of special characters and control codes.
Storage Size: Each ASCII character is stored in 1 byte (8 bits), but since only 7 bits are used (the highest bit is 0), it is often described as a 7-bit encoding.
Limitations: It cannot represent characters from other languages or symbols beyond the English alphabet (e.g., Chinese characters, accented characters, etc.).


UTF-8 (Unicode Transformation Format - 8-bit)
                   UTF-8 is a variable-length character encoding scheme used to encode all characters in the Unicode character set. Unicode aims to include every character from all writing systems in the world, including ancient scripts, emojis, symbols, and more.
Key Points:
•	Character Range: UTF-8 can represent all Unicode characters, including characters from virtually every language, mathematical symbols, emojis, and more. It is capable of encoding over 1 million characters (more than the ASCII set).
•	Storage Size: UTF-8 is a variable-length encoding, meaning the number of bytes used to represent a character depends on the character:
o	For characters in the ASCII range (0–127), UTF-8 uses 1 byte (same as ASCII).
o	For characters outside the ASCII range, UTF-8 uses 2, 3, or 4 bytes depending on the specific character.
•	Backward Compatibility: UTF-8 is backward compatible with ASCII. This means that any valid ASCII text is also valid UTF-8 text, because UTF-8 uses the same encoding for the first 128 characters (0–127), which correspond to ASCII.
Example:
•	'A' in UTF-8 = 0x41 (1 byte)
•	'€' (Euro symbol) in UTF-8 = 0xE2 0x82 0xAC (3 bytes)
•	'😊' (Emoji) in UTF-8 = 0xF0 0x9F 0x98 0x8A (4 bytes)

















Findings.
What I found is that in computer programming, memory allocation plays a vital role. Memory allocation provides data with a space in RAM to function and operate. Memory allocation has two main components: Stack memory and Heap memory.
•	In Stack memory, primitive data is used. It has a fixed size and allows fast access. Stack memory follows the LIFO (Last In, First Out) principle.
•	In Heap memory, objects, arrays, and functions are stored, and memory is allocated dynamically (randomly). Heap memory is cleared through garbage collection.
I also found that mutable and immutable types are similar in Python and JavaScript:
•	Mutable types are those whose memory address doesn’t change when the value is modified. Examples of mutable types include list, dict, and set.
•	Immutable types are those whose memory address changes when the value is modified. Examples of immutable types include int, str, and tuple.
I also found that error types are similar in both Python and JavaScript:
•	Compile-time errors occur when there are syntax errors, such as missing commas or indentation errors (e.g., missing spaces). In Python, indentation should generally have 4 spaces. Compile-time errors occur before running the program.
•	Run-time errors occur when there are mathematical or logical issues, such as dividing by zero. Run-time errors occur when the program is executed.
I also found that:
•	Primitive data types are the most basic predefined data types. They store simple values directly in memory, are immutable, and are stored in the stack. When a primitive type is passed to a function, a copy of the value is passed, so the original value remains unchanged.
•	Reference data types, on the other hand, store a reference to the value's memory location rather than the value itself. They are more complex data structures, stored in heap memory, and are mutable. When a reference type is passed to a function, the memory reference is passed, so modifying the object inside the function affects the original value.

I also found that the data types in both Python and JavaScript are similar; only their use cases or implementation differ.So there memory allocation are also similar in both
•	Memory Allocation: Stack Memory → Fixed Size → LIFO → Fast Access
Heap Memory → Dynamic Objects/Arrays/Functions → Random Memory → Garbage Collection

Lastly, I found that ASCII code uses only 128 characters, while UTF-8 supports 1.1 million characters. UTF-8 is more advanced because it supports special characters and various languages.

