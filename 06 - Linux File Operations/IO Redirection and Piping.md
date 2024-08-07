# Redirection and Piping

## 1. **I/O Redirection**:
   - **Standard Input (stdin)**, **Standard Output (stdout)**, and **Standard Error (stderr)** are essential file descriptors for communication between programs and the outside world.
   - **stdin**: Default input source (usually keyboard input).
   - **stdout**: Default output destination (typically the terminal).
   - **stderr**: Alternative output for errors.
   - We can redirect these streams to/from files or other commands.

## 2. **Redirection Operators**:
   - `>`: Redirects stdout to a file (overwrites existing content).
     ```
     ls > files
     ```
   - `>>`: Appends stdout to a file.
     ```
     ls -1 *.txt >> files
     ```
   - `2>`: Redirects stderr to a file.
     ```
     command_that_might_fail 2> error.log
     ```

## 3. **Piping (`|`)**:
   - Connects the stdout of one command to the stdin of another.
   - Useful for chaining commands:
     ```
     ls | grep "pattern"
     ```


- [(1) Pipes and Redirection in Linux | Baeldung on Linux.](https://www.baeldung.com/linux/pipes-redirection.)
- [(2) Learn The Basics of How Linux I/O (Input/Output) Redirection ... - Tecmint.](https://www.tecmint.com/linux-io-input-output-redirection-operators/.)
- [(3) Basic Guide to Input Output (I/O) Redirection in Linux - OperaVPS.](https://operavps.com/docs/input-output-redirection-in-linux/.)
