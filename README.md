# Minitrice

## Presentation

### Context
University python project. The minitrice performs basic operations from command line. 

It can be used interactively in a terminal, but also coupled with other programs to send data through a pipe. Test files of example expressions as well as an expression generator are provided in this repository.

### Regular examples of use

- Interactive usage
```bash
1. $ ./minitrice
2. > 3+9
3. 12
4. > 
5. Fin des calculs :)
6. $ echo $?
7. 0
8. $ 
```
Interactive case : <br>
Simply run the script :

```bash
1. $ ./minitrice
```

- Usage with cat
```bash
 1. $ cat good-expression.txt | ./minitrice
 2. 4
 3. 11
 4. 35
 5. -4
 6. 12
 8. 90
 9. 4.0
10. 8.0
11. 10
12. 4
13. $ echo $?
14. 0
15. $ 
```
No interactive case : <br>
The code must be executed using either an "echo" or a "cat" following an expression or a file, depending on the command used.

```bash
1. $ echo "9+1" | ./minitrice
```
ou 
```bash
1. $ cat good-expression.txt | ./minitrice
```

- Usage with an expression generator
```bash
1. $ ./generator 2 | ./minitrice
2. -2
3. 7.0
4. $
```
### Stress the program 
- 
- Division by zero
- Generator
A few errors are handled by the generator. 

No-argument case : 
You can call it with no argument like following :
```bash
1. $ ./generator
```
It will help you to use it properly. 
Also, you can call it with an out-of-the-range argument number :
```bash
1. $ ./generator 8000
```
It will ask you to be more reasonable. The expected range is between 1 and 500.


## Installation

### Install dependencies
- Linux environement
This project is intended to operate within a Linux environment. If you are under Windows, you may wan to install WSL2 to access a linx terminal and run the program. ([See here](https://code.visualstudio.com/docs/remote/wsl) for VSCode)

- Python, v3.9.9
You will also need the Python programming language installed. Download it [here](https://www.python.org/)

### Steps 
- Download the project using the following command line

```bash
git clone https://github.com/paulinebrisset/minitrice
``` 
- Then go in the new folder
```bash
cd minitrice
``` 
- Set the executable permissions on the files
```bash
chmod +x generator
``` 
and
```bash
chmod +x minitrice
```

Without setting this permission, the files would not be recognized as executable scripts, and you would need to call them with `python3 generator.py 3` and `python3 minitrice.py`  instead of `./generator.py 3` and `./minitrice`.


<b>Note:</b>  To permit the minitrice file to be call like "./minitrice" we put on the first line of the file: <br>

```bash
#!/usr/bin/env python3
```
This will let the system know to execute the file as a python script and we don't need to put ".py" at the end of the file.




## Gourse project's video
## Useful links
-[Install WSL in Visual Studio Code](https://code.visualstudio.com/docs/remote/wsl)
-[import sys](https://docs.python.org/fr/3/library/sys.html)
## Contributors
- [Beriche Chahalane](https://github.com/Beriche)
- [Lenaic Honorine](https://github.com/LenaicHnr)
- [Alexandre Tam-Hui](https://github.com/Alextmh)
- [Pauline Moncoiffé-Brisset](https://github.com/paulinebrisset)
