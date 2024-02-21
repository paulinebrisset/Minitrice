# Minitrice

## Presentation

### Context
University python project. The minitrice performs basic operations from command line. 

It can be used interactively in a terminal, but also coupled with other programs to send data through a pipe. Test files of example expressions as well as an expression generator are provided in this repository.

### Example of use

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

- Usage with an expression generator
```bash
1. $ ./generator 2 | ./minitrice
2. -2
3. 7.0
4. $
```
### Errors and generator

## Installation
### Requirements
- This project is intended to operate within a Linux environment. If you are under Windows, you should 
### Steps 

## Gourse project's video
## Usefull links

## Contributors
- [Beriche Chahalane](https://github.com/Beriche)
- [Lenaic Honorine](https://github.com/LenaicHnr)
- [Alexandre Tam-Hui](https://github.com/Alextmh)
- [Pauline Moncoiffé-Brisset](https://github.com/paulinebrisset)
