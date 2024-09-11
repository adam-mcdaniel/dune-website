+++
title = 'Showcase'
date = 2024-09-11T01:55:12-04:00
author = "Adam McDaniel"
+++

# PIPING AND REDIRECTION

Piping and redirection are done with the `|`, `>>`, and `>>>` operators. Here's some example uses!

{{< image src="/piping.png" alt="Piping and redirection" position="center" >}}

| Operator | Description |
|----------|-------------|
| `\|`      | Pipe the output of the left command to the input of the right command. |
| `>>`     | Write the output of the left command to a file. |
| `>>>`    | Append the output of the left command to a file. |

# STANDARD LIBRARY

Dune offers an extensive standard library, and also provides a pretty interface to see all the functions available in each module!

{{< image src="/math.png" alt="Math Library" position="center" >}}

To see the entire standard library available to you, simply enter `std` into the command line. This will print out the entire set of nested standard library modules and their functions plus constants!

# CREATING ALIASES FOR PROGRAMS

Dune allows you to create aliases for programs through the `let` keyword and a quoted symbol. Below, we bind the quoted symbol `'bat` to the symbol `cat`. So, whenever we use the symbol `cat`, it will evaluate to the symbol `bat`.

{{< image src="/alias.png" alt="Alias" position="center" >}}

# MACROS IN DUNE

To write functions that modify your shell's environment and act like commands, use a macro!

{{< image src="/macros.png" alt="Macros" position="center" >}}

Macros, when called with zero arguments, are passed the current working directory. When invoked, they assume the environment of the callee: if you execute macro, it will execute as if you executed the contents of the macro itself with the parameter defined as the argument passed.

# FUNCTIONAL PROGRAMMING

Dune supports functional programming! You can use functions like `map`, `filter`, and `reduce` to manipulate lists and other data structures. Dune also supports anonymous functions and closures with a concise syntax.

{{< image src="/functional.png" alt="Functional Programming" position="center" >}}

# OPERATOR OVERLOADING

All of the operators in Dune are implemented as function applications on the symbols that represent them. This means that you can overload operators to do whatever you want!

{{< image src="/operators.png" alt="Operator Overloading" position="center" >}}