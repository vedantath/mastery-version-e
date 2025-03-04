# cs429-mastery-assignment

# What this repo contains:
- `main.c`, `reader.c`, `calculator.c` and their corresponding header files.
- A Makefile
- Some testcases in the `testcases` folder
- a reference executable called `mini_ci_reference`

# What this code does:
The given code reads in a string representing a postfix operation, evaluates the value of the operation,
and prints the result, notifying the user if the operation was invalid.
A postfix operation is defined by `<operand1> <operand2> <binary operator>` eg. `1 2 +` which evaluates to 3.
These operations can be chained together `8 1 - 2 +` = `7 2 +` = `9`;
Similarly `8 1 2 - +` = `8 -1 +` = `7`
If at any point the Reader encounters an error, the final result should be set to -1 and the Reader's had_error field
should be set to true. If no error occurs, the Reader's had_error field should be false.
The given program uses a greedy stack based approach to evaluate valid operations as soon as they appear.
Unfortunately, this program may be wrong!

# Instructions:
1. create a file `~/.gdbinit`
2. Add the line `set history save on` to `~/.gdbinit`
3. ssh into your favorite UTCS lab machine
4. git clone this repository
5. read then use the Makefile
6. debug the test cases using GDB
7. Ensure your output matches the reference exactly.
8. commit and push your changes
9. use git log and show proctor

To run an individual testcase use 
`mini_ci <file>`. Use `mini_ci_reference <file>` for the reference output.
