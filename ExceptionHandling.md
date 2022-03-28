# Exception Handling
Exception Handling is a way to Handle an error happend while runnig our code without stop the run.
we can do that by two ways: 
## 1. Debugging
Debugging means to track our code line by line to exactly know where is the error, we could use a depugger to do that, but before you start debugging, make sure you've identified the problem you're trying to solve by asking yourself these quastions:

- What did you expect your code to do?

- What happened instead?

to start debugging in Visual Studio as example you have to click the start debugging button ![Start Debugging](https://docs.microsoft.com/en-us/visualstudio/debugger/media/dbg-tour-start-debugging.png?view=vs-2019).

## 2. Try/Catch and Finally block
try and catch is a common way test code if we are worried that an error will happend to use it we can:
> Place any code statements that might raise or throw an exception in a try block, and place statements used to handle the exception or exceptions in one or more catch blocks below the try block. Each catch block includes the exception type and can contain additional statements needed to handle that exception type.
[try/catch block (Microsoft article)](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/how-to-use-the-try-catch-block-to-catch-exceptions)

we use finnaly to do some code either the error happend or not. it is placed after the catch block.