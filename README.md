# kjell
Kjell is a cross-platform scripting language for text manipulation

## Examples

```sh
# Output all lines that contain "banana" in the input stream
cat input.txt | kj 'filter /banana/' 
```

## Motivation

## Types

Under the hood, Kjell is a statically typed functional programming language. But thanks to type inference, Kjell still has a dynamic feel.


Having Kjell being a statically typed langauge brings certain benefits:

 - Incorrect programs will not start, as opposed to crashing in the middle of a long run
 - As Kjell doesn't allow recursive definitions it is *total*, ie if the program compiles it will never crash or hang
 - Type inference allows automatic coercion of input arguments and automatic generation of help messages 

## Safety

Kjell scripts are more secure than e.g. Bash or Python as they only operate on string streams; a script can't "shell out" or otherwise touch other parts of the operating system.
