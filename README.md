# The Compiler and the JVM

## Learning Goals

- Explain compilation process
- Explain JVM

## Compilation

In the previous unit, we learned how to run a sample Java program. As you saw,
it took two steps:

1. Compile the program
2. Run the program

If we go back to our chef example and consider our `makeBreakfast()` set of
instructions, you can imagine that chefs and cooks have their own shorthand to
communicate with each other. So they might have terms like **whip** that have
specific meaning to that profession. If you wanted to make the `makeBreakfast()`
instructions understandable by someone who is not a professional chef, you might
need to translate those specialized terms into more basic instructions.

That is essentially what the compiler does. It takes language-specific (in our
case, Java) instructions and turns them into something that your computer can
execute.

For a lot of programming languages, the output of the compiler is something that
your computer can run directly.

## JVM

Java, however, is an **interpreted** language, which means that instead of
compiling code to be run on a specific machine, the Java compiler compiles code
to be run by the **Java Virtual Machine**. The JVM then interprets that code and
runs it on a specific machine.

The discussion of the pros and cons of this approach is outside the scope of this
unit, but we should note that Java's main goal with the JVM is to make Java's
compiled code (called **Java bytecode**) executable on any platform that
supports the JVM without the need for the original source code to be re-compiled.

Let's summarize the lifecycle of our instructions:

1. We write our program instructions in a programming language called Java (using
   an Integrated Development Environment, or IDE for short like IntelliJ).
   This set of instructions is referred to as our **source code** and is
   "human-readable", which means you and me, with some training, can read it and
   understand its intent.
2. We then **compile** our **source code** (using the `javac` command) in order
   to turn it into something that the **Java Virtual Machine** (JVM) can execute.
   This is called **Java bytecode** and is not intended to be "human-readable".
3. Finally, we execute the compiled code using the `java` command, which runs
   our instructions and displays the corresponding output

Here is a table view of this summary

|                | Step 1      | Step 2                  | Step 3                        |
|----------------|-------------|-------------------------|-------------------------------|
| Tool           | IntelliJ    | Java compiler (`javac`) | Java Virtual Machine (`java`) |
| File generated | Source code | Bytecode                | Program output                |

## Conclusion

You should now understand how a Java program is compiled and run by your
machine.
