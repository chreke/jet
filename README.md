# kjell
Kjell is a cross-platform scripting language for text manipulation

## Examples

```bash
# Output all lines that contain "banana" in the input stream
cat input.txt | kj 'filter /banana/' 
```

## Safety

Kjell scripts are more secure than e.g. Bash or Python as they only operate on string streams; a script can't "shell out" or otherwise touch other parts of the operating system.
