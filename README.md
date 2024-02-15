# Jet
Jet is a cross-platform scripting language for text manipulation

## Examples

```sh
# Output all lines from input.txt that contain "banana"
cat input.txt | jet 'filter /banana/' 
```

## Motivation

The motivation for Jet is that I want a cross-platform scripting language which can be used for a variety of text manipulation tasks.

When I used to program Perl I realized that I could use it replace most of my uses of `grep`, `sed`, etc. While having a single program that does a lot of different things goes pretty hard against the Unix philosophy, I would say it has its benefits. Having a single tool that does everything means you don't have to remember the command line options and quirks of a collection of disparate tools. 

Also, if the single tool is portable it means it will work the same anywhere; for example, you won't have to ask yourself questions like "does this system have the GNU or BSD version of `sed`?"

## Types

Under the hood, Jet is a statically typed functional programming language. All Jet programs should have the function signature `(List String) -> a`.

Having Jet being a statically typed langauge brings certain benefits:

 - Incorrect programs will not start, as opposed to crashing in the middle of a long run
 - As Jet doesn't allow recursion it is *total*, ie if the program compiles it will never crash or hang
 - Type inference allows automatic coercion of input arguments and automatic generation of help messages 

## Safety

Jet scripts are more secure than e.g. Bash or Python as they only operate on string streams; a script can't "shell out" or otherwise touch other parts of the operating system.
