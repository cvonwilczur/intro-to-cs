#Python Basics

Even with fast computers, we need cleverness and good algorithmic thinking to be efficient. We can't just use brute force or pre-compute.

Some problems are still, at least at the moment, too complex for our compute power and data to solve. This also works in our favor (encryption schemes, for instance).

##Knowledge

Computers know what you tell them.

Declarative knowledge is statements of fact.
For example, we declare that the candy is under a specific chair.

Imperative knowledge is a recipe or "how-to", or computation.
In this example, we give a sequence of steps that will eventually discover the candy under a chair.

A classic example of imperative knowledge is below:

1) Start with a guess, g.
2) If g*g is close enough to X, stop and say g is the answer.
3) Otherwise make a new guess by averaging g and x/g
4) Using the new guess, repeat the process until close enough.

An algorithm is a sequence of simple steps, a flow of control process that specifies when each step is executed and a means of determining a stopping point.

##Machines

Computers are machines.

A fixed program computer has a single, fixed purpose. An example would be a calculator, or Alan Turing's Bombe.

A stored program computer is a machine that can store multiple programs and execute instructions. A special program inside the computer, called an interpreter, will walk through the steps of the programs, emulating a fixed program computer.

###Basic Machine Architecture

Memory - Data, a sequence of instructions, etc.

Input - A way to load things into the machine.

Output - A way to print things out of the machine.

Arithmetic Logic Unit - ALU, does primitive operations.

Control Unit - Program counter, keeps track of what specific operation you want the ALU to do. When you load a program into a machine, it's a sequence of instructions, and the program counter reads through the instructions, moving in sequence.

###Basic Primitives
Turing showed you can compute anything using 6 primitives (move left, move right, scan, read, right, do nothing).

Modern programming languages have a more convenient set of primitives. They can abstract methods to create new primitives.

Anything computable in one language is computable in any other programming language. This is a property called Turing Complete.

##Semantics

A programming language provides a set of primitive operations. Numbers, strings, simple operators.

Expressions are complex but legal combinations of primitives in a programming language. "hi"5 would not be valid, but 3.2*5 would be syntactically valid.

Expressions and computations have values and meanings in a programming language. Static semantics is which syntactically valid strings have meaning (whether or not it's put together properly). 3.2*5 is syntactically valid, but 3+"hi" produces a static semantic error. Semantics is the meaning associated with that syntactically correct string of symbols.

Syntactic errors are common and easily caught. State semantic errors can cause unpredictable behavior and are sometimes caught by the language.

No semantic errors but different meaning than what the programmer intended can cause the program to crash, run forever or give an answer that is different than expected.

##Python programs

A program is a sequence of definitions and commands. Definitions are evaluated and commands are executed by the Python interpreter in a shell.

Commands instruct the interpreter to do something. They can be typed directly into the shell or can be stored in a file that the shell reads and evaluates.

###Objects
Programs manipulate data objects. These objects have a type that defines the kinds of things program can do with them.

Objects are scalar (cannot be subdivided) and non-scalar (have internal structure that can be accessed).

Scalar Objects: Ints (5, 17), Floats (3.27), Bool (True/False), NoneType (special and has one value, None). We can use type() to see the type of an object.

###Type Conversions (CAST)
We can cast types, such as converting ints into floats and vice versa using float() and int().

###Expressions
<object><operator><object>

Any expression like this that is syntactically valid has a value.

i+j -- the sum
i - j -- the difference
i * j -- the product
i / j -- the quotient, returning a float
i // j -- the quotient, returning only an int
i ** j -- i to the power of j
i % j -- the remainder of i when divided by j

Operator precedence without parentheses:
- **
- *
- /
- + and -
- executed left to right


### Variables
The equal sign is an assignment of a value to a variable name.

pi = 3.14159
pi_approx = 22/7

The value is stored in computer memory.

The assignment binds name to value, and you can retrieve the value by invoking the name. Binding names enables reusability, and makes it easier to change code later.

We can rebind variable names using new assignment statements; the previous value may still be stored in memory, but we've lost the handle for it.

### Comparison and Logical Operators
i > j
i >= j
i < j
i <= j
i == j
i != j

not a

a and b

a or b

The simplest branching statement is a conditional. A test for true or false, with a block of code executing if the test is true and an optional block of code to execute if the test is false.

if x%2 == 0:
  print('')
  print('Even')
else:
  print('')
  print('Odd')
print ('Done with conditional')

if x < y and x < z:
  print('x is least')
elif y < z:
  print('y is least')
else:
  print('z is least')

These are examples of control flow. These programs run in constant time, as the maximum time to run the program depends only on the length of the program.

### Strings

Strings are a sequence of letters, special characters, spaces and digits. They are all enclosed within double or single quotes.

We can concatenate strings, for example:

name = "eric"

greet = "hi" + " " + name

We can also ask for the length of a string:

len("eric")

We can also index elements at a specific space, such as:

"eric"[2]


We can also slice items out using the same notation:

"eric"[2:3]

### IDEs  

It's often painful to just type things into a shell. It's preferable to use a text editor or integrated development environment.


### While Loops and For Loops

n = 0
while n < 5:
  print(n)
  n = n + 1


for n in range(5):
  print(n)

## Iteration

- the concept of iteration lets us extend branching algorithms to be able to write programs of arbitrary complexity

### Guess and Check methods

 - one example of an algorithm. we come up with a way of systematically making guesses and checking if they are correct.

 
