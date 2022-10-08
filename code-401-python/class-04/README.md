# class 04

## Read & Write Files in Python

----------------

### A file is a sequence of bytes used to store data. This information is stored in a specific format and can be as simple as a text file or as complex as a program executable. Finally, these byte files are translated into binary 1 and 0 for easier computer processing

### A file path is required when accessing a file on an operating system. The file path is a string that represents a file's location. It is divided into three major sections:

1. Folder Path: the file system location where subsequent folders are separated by a forward slash / (Unix) or backslash / (Windows) (Windows)

2. File Name: the file's actual name

3. Extension: the end of the file path prefixed with a period (.) to indicate the file type

### The representation of a new line or line ending is a common issue when working with file data. Line endings have their origins in the Morse Code era, when a specific pro-sign was used to communicate the end of a transmission or line. According to the ASA standard, line endings should be composed of the Carriage Return (CR or r) and Line Feed (LF or n) characters (CR+LF or rn). The ISO standard, on the other hand, allowed for either CR+LF characters or just the LF character

### The first thing you should do when you want to work with a file is to open it. This is accomplished by calling the built-in function open(). The path to the file is the only required argument for open(). open() has a single return value

### For reading and writing binary files, a buffered binary file type is used. When dealing with these files, open() will return either a BufferedReader or a BufferedWriter file object.

### A raw file type is commonly used as a foundation for binary and text streams. When dealing with these files, open() will return a FileIO file object.

### Iterating over each line is a common practice when reading a file.

### You may need to work with files using byte strings on occasion. This is accomplished by appending the character 'b' to the mode argument. All of the file object's methods are applicable. However, each method expects and returns a bytes object.

## Exceptions in Python

----------------

### When a Python program encounters an error, it terminates. An error in Python can be either a syntax error or an exception.

### When the parser detects an incorrect statement, syntax errors occur.

### Exception error: This type of error occurs when otherwise correct Python code produces an error. The message's final line indicated the type of exception error you encountered.

### Instead of displaying the message exception error, Python provides information about the type of exception error encountered. It was a ZeroDivisionError in this case. Python includes a number of built-in exceptions as well as the ability to create custom exceptions.

### Rather than waiting for a program to crash in the middle, you can begin by making an assertion in Python. We assert that a specific condition has been met. If this condition turns out to be true, that is fantastic! The program can go on. If the condition is found to be false, the program can throw an AssertionError exception.

### In Python, the try and except block is used to catch and handle exceptions. Python executes the code following the try statement as part of the "normal" program. The code following the except statement represents the program's response to any exceptions raised in the preceding try clause.

### Python will throw an exception error if syntactically correct code encounters an error. If this exception error is not handled, the program will crash. The except clause specifies how your program handles exceptions.

### Here are the key takeaways:

- A try clause is executed up until the point where the first exception is encountered.

- Inside the except clause, or the exception handler, you determine how the program responds to the exception.

- You can anticipate multiple exceptions and differentiate how the program should respond to them.
Avoid using bare except clauses.

### Using the else statement in Python, you can instruct a program to execute a specific block of code only if there are no exceptions.

### Assume you had to always implement some sort of cleanup action after executing your code. The finally clause in Python allows you to do so.

- raise gives you the ability to throw an exception at any time.
- assert allows you to check if a condition is met and throw an exception if it is not.
- All statements in the try clause are executed until an exception is encountered.
- except is used to catch and handle the exception(s) raised by the try clause.
- else allows you to write sections that should be executed only if no exceptions are encountered in the try clause.
- Finally, it allows you to run sections of code that should always be executed, with or without previously encountered exceptions.
