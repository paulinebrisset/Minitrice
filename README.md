# Minitrice

- [Minitrice](#minitrice)
    - [Presentation](#presentation)
        - [Context](#context)
        - [Regular examples of use](#regular-examples-of-use)
        - [Stress the program](#stress-the-program)
    - [Installation](#installation)
        - [Install dependencies](#install-dependencies)
        - [Steps](#steps)
    - [Documentation](#documentation)
        - [Gource project's video](#gource-projects-video)
        - [Useful links](#useful-links)
    - [Contributors](#contributors)

## Presentation

### Context
University python project. The minitrice performs basic operations from command line. 

It can be used interactively in a terminal, but also coupled with other programs to send data through a pipe. Test files of example expressions as well as an expression generator are provided in this repository.

### Regular examples of use
- Interactive case
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
Exit from the program using the shortcut Cntrl + D

- No interactive case 
The code must be executed using either an "echo" or a "cat" following an expression or a file, depending on the command used.

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
or : 

```bash
1. $ echo "9+1" | ./minitrice
```

To save the results in a text file, make sure you have a repository called "results".
Then, give the file name as an argument to the minitrice program : 

```bash
1. $ cat my-file.txt | ./minitrice my-file
```
This command creates a file named my-file-results.txt, with all the results of the expressions contained in my-file.

- Generate expressions (Generator)
You can generate random expressions involving figures from the interval [1, 1000] for the minitrice to compute it. Just call the generator with the desired expressions number : 

```bash
1. $ ./generator 2 | ./minitrice
2. -2
3. 7.0
4. $
```

You can also generate an example file to store a bunch of expressions : 
```bash
1. $ touch my-file
2. $ ./generator 10 >> my-file touch my-file
3. $
```

### Stress the program 

- Division by zero
The minitrice will raise an alert if you try to divide by zero
```bash
1. $ ./minitrice 
2. > 6/0
3. Erreur de calcul: division by zero
4. >
```
- Syntax error
The minitrice will raise an alert if you make a syntax mistake
```bash
1. $ ./minitrice 
2. > 8+/9
3. Erreur de syntaxe pour le calcul: 8+/9
4. >
```


- Generator errors 
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
2. I'm not sure I can perform so many computations
```
The expected range is between 1 and 500.

## Installation

### Install dependencies
- Linux environement
This project is intended to operate within a Linux environment. If you are under Windows, you may wan to install WSL2 to access a linx terminal and run the program ([see here](https://code.visualstudio.com/docs/remote/wsl) for VSCode)

- Python, v3.9.9 <br>
You will also need the Python programming language installed. Download it [here](https://www.python.org/).

### Steps 
- Download the project using the following command line

```bash
git clone https://github.com/paulinebrisset/git-evaluation_groupe-2
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

Without setting thes permissions, the files won't be recognized as executable scripts, and you would need to call them with `python3 generator.py [arg]` and `python3 minitrice.py`  instead of `./generator [arg]` and `./minitrice`.


<b>Note:</b>  To permit this behaviour for both the minitrice and the generator we wrote on the first line of the files: <br>

```bash
#!/usr/bin/env python3
```
This will let the system know how to execute the files, as python scripts, and we don't need to put ".py" as extension for the file name.

## Documentation
### Gource project's video
You can watch the progress of the construction of this projet at this link : [Gource video on Youtube](https://youtu.be/wL6XTHdgqfU)

### Useful links
- [Install WSL in Visual Studio Code](https://code.visualstudio.com/docs/remote/wsl)
- [import sys](https://docs.python.org/fr/3/library/sys.html)
- [Tutorial for Gource use](https://dev.to/voieducode/my-gource-video-production-pipeline-5eb0)
- [Create read and write to a file in python](https://python.doctor/page-lire-ecrire-creer-fichier-python)
- [Errors and Exceptions](https://docs.python.org/fr/3/tutorial/errors.html)

## Contributors
- [Beriche Chahalane](https://github.com/Beriche)
- [Lenaic Honorine](https://github.com/LenaicHnr)
- [Alexandre Tam-Hui](https://github.com/Alextmh)
- [Pauline Moncoiffé-Brisset](https://github.com/paulinebrisset)
