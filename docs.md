# bb00 guidelines

## Versioning
Versioning of releases uses semantic versioning 2.0.0 as specified at [semver.org](https://semver.org/).

Versioning of snapshots and development builds uses the following format:

```
22w21c
| | ||
| | ||-- revision letter for snapshot released in that week
| | |--- two-digit week of the year
| |----- letter w (for week)
|------- two-digit year
```
This example is third build ("**c**") released in the **21**st **w**eek of 20**22**.
If there are more than **a**-**z** releases in one week it continues with **aa**-**zz**.

## Coding Guidelines and Philosophy
### Writing minimalist code
I want to write code with a big focus on simplicity and clarity.
Writing simple code, that only does what it needs to do, makes it easier to maintain and more reliable.
Code is art. Code is telling a story. You are writing the story. Write it well. If your code doesn't spark joy, it is time to clean it up.
#### Less is more
Functions and methods should not be more than 10 lines. If possible use functional-programming style code.
#### Accurate meaningful naming
Code is words and words tell a story. Make it easy to the reader and to your future self. If you don't write out words use common abbreviations.
If your function name is too long and contains the word 'and', you probably have too much functionality inside. Apply the max. 10 lines principle described above.
#### Meaningful comments
First of all, good code shouldn't need any comments. Avoid them, especially if the don't add any value.
Tell your story using proper function and variable names.

### Coding Style
#### General rules
- Use english names and text for all code.
- Do not use tabs, use spaces.
- Use 2 or 4 spaces per indent level.
- Use 1 space between keywords and opening brackets.
- Do not use spaces between function names and opening brackets.
- Never use `__` or `_` as prefix as it is reserved for internal use with some programming languages.
- Use only lowercase characters for variables/functions/macros/types with an optional underscore character.
- Opening curly brackets are always at the same line as the keyword (`for`, `while`, `switch`, `if`, ...).
- Use single space before and after comparison and assignment operators.
- Use single space after every comma.
- Declare counter variables in `for`-loop (`for(size_t i = 0; i < 10; i++)`) if you don't need it later.
- Always use the types declared in `<stdint.h>` eg. `uint8_t`, `uint32_t` etc.
- Never compare against `true`.
- Always compare pointers against the `NULL` value.
- Always use `size_t` for length and size variables.
- Always use `const` for pointers if the function is not supposed to change the variable or parameter.
- When accepting a pointer of any type, use `void *`.
- Always use brackets with the `sizeof` operator.
- Always align asteriks to the type in pointer types, eg. `uint8_t*`.
