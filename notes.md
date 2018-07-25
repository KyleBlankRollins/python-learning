# Notes

## Python3 overview
Python is a dynamically typed language, as opposed to statically typed.
type() allows you to check the type of variables.

### Python types
+ integers
+ floating point
+ strings
+ lists
+ dictionaries
+ tuples
+ sets
+ booleans

### Variable names
+ cannot start with a number
+ no spaces in names - use _ instead
+ cannot use the following symbols: ``:'"<>/?|\!@#$%^&*~-+``
+ should be lowercase
+ global variables often uppercase

### Strings
+ are ordered sequences, meaning each character has a specified positions
- this enables indexing and slicing
+ Python allow reverse indexing of strings
+ len() returns the length of a string
+ step size format: "mystring[::3]" takes mystring "abcdefghijk" and returns every third position.

### String properties and string methods
+ Can't reassign positions in strings.
- Instead, need to slice relevant parts, then concatenate with new values.
+ Be wary of concatenating different data types.

### String formatting for printing
+ String interpolation.
- Adding variables to strings.
+ Float formatting, .format(): {value:width.precision f} - print("The result was {r:1.3f}".format(r=result)) returns 0.129.
- Alternate approach, f-string literals: print(f"The result was {result:1.3}") also returns 0.129.

### Lists
+ Lists are mutable.
+ list.append() adds items to a list.
+ list.pop() removes items from a list.
+ list.sort() sorts list items. Doesn't return anything - is noneType. Can't reassign.
+ list.reverse() reverse sorts list items. Doesn't return anything - is noneType. Can't reassign.
+ nested lists: How do I index a nested list? For example if I want to grab 2 from [1,1,[1,2]]? You would just add another set of brackets for indexing the nested list, for example: my_list[2][1] . We'll discover later on more nested objects and you will be quizzed on them later!

### Dictionaries
+ Are unordered mappings that store objects with key:value pairs.
+ Defined with curly braces {} instead of brackets [], which define lists.
+ When to use a list vs dictionary?
- Dictionaries are not sortable, but have known locations thanks to the key.

### Tuples
+ Similar to lists, but they're immutable - they don't support reassignment.
+ Defined by parenthesis ().
+ tuple.count() returns number of times something appears in a tuple.
+ tuple.index() returns the location of the first instance of something in a tuple.
+ Tuples protect data integrity - preventing critical static elements from being reassigned.

### Sets
+ Are unordered collections of unique elements. Only one representative of each object.
+ Useful for filtering out repeat items.

### Booleans
+ Critical for control flow and logic
+ Python requires capital True and False to recognise them.

### I/O with basic files in Python
+ Jupyter can create new text files with %%writefile name.txt
+ pwd command prints current directory - useful for figuring out where your Jupyter notebook is located.
+ txtFile.read() returns a string that contains all of the text file's characters. Includes formatting escape characters like /n.
- .read() needs to be reset to read the same file again. Use .seek(0) to return to beginning of doc.
+ .readlines() returns a list with each line as its own object.
+ Filepaths: need double \ to escape \ in the file path - myfile = open("C:\\Users\\UersName\\Folder\\test.txt")
+ Need to close files or you'll run into errors.
- to avoid needing to use txtFile.close(), use this construction:
    with open('myfile.txt') as my_new_file:
        contents = my_new_file.read()
+ Use Shift + Tab to get information about opened functions.
#### Reading, Writing, Appending Modes
+ mode='r' is read only
+ mode='w' is write only - overwrites files or creates new files
+ mode='a' is append only - adds to the end of files
+ mode='r+' is reading and writing
+ mode='w+' is writing and reading - overwrites existing files or creates new files
