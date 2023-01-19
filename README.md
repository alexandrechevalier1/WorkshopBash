# WorkshopBash

For all this Workshop, don't forget to "chmod +x" all your script 

# Step 1 : Basic bash
(5/10 min)

- Create a bash script named "step1.sh" that print it's given arguments

for exemple :
```bash
./step1.sh "Hello World"
```

The output should be:
```bash
> Hello World
```

# Step 2 : Handling file
(10 min)

Create a bash script named "step2.sh" that :
- create a file named "test"
- insert "Hello World" in the file "test"
- print the content of this file

The output should be:
```bash
$ Hello World
```
# Step 3 : Check file content
(10/15 min)

Content of the file "File1" :

```bash
84
```

Content of the file "File2" :

```bash
42
```

Create a bash script named "Step3.sh" that take a filepath as argument.
Whenever the content of the file is "42" print "Good File" else print "Wrong File"

For the fisrt file the output should be :

```bash
$ Wrong File
```

For the second file the output should be :

```bash
$ Good File
```

# Step 4 : Make a prefabricated file :
(30 min)

Create a script Bash named "Bash4.sh" that :
- Take a "File_Prefab" file as arguments
- Use it to Préfabricate a file

the Content of the "File_Prefab" is :

```txt
FILE_NAME:
main.c
INC:
#include <unistd>
#include <string.h>
FNC: 
void main(int argc, char **argv) {
  write(1, argv[1], strlen(argv[1]));
  return 0;
}
```

The file created should be "main.c" and is content should be :

```c
/*
** EPITECH PROJECT, 2023
** main
** File description:
** main file
*/

#include <unistd.h>
#include <string.h>

int main(int argc, char **argv)
{
    write(1, argv[1], strlen(argv[1]));
    return (0);
}
```

# Step 5 : Make a architecture constructor :
(45 min)

In a Folder "step5" create a script Bash named "step5.sh" that :
- Take a "config_file" as argument (the "config file" represent the folder architecture off a project).
- Create the architecture represented in "Config_File".

The content off "Config_File" is :

```bash
/src
  -main.c
  -calculus.c
  -error_managment.c
/inc
  -calculus.h
```

Your tree should look like :

```bash
.
├── inc
│   └── calculus.h
└── src
    ├── calculus.c
    ├── error_managment.c
    └── main.c

3 directories, 4 files
```

# Step 6 : Make a Makefile constructor :
(45 min)

Create a Bash script named "stap6.sh" that :
- Take a "config" file
- Create a Makefile with the content off the "config" file

The Content of the "config" file is :

```txt
EXEC_NAME
basic
SOURCES_DIR
/src/main.c
/src/calculus.c
/src/error_managment.c
PROJECT_DIR
.
CC
gcc -o $(EXEC_NAME) $(SOURCES_DIR)
LIBS_DIR
-lcsfml-graphics -lcsfml-window
CLEAN

rm -f *.o
FCLEAN
clean
rm -f $(EXEC_NAME)
RE
fclean all
```

The Makefile created should look, like :

```Makefile
##
## EPITECH PROJECT, 2023
## Makefile
## File description:
## Makefile with makefile constructor
##

SOURCES_DIR	= 	src/main.c 	\
			src/calculus.c 	\
			src/error_management.c 	\

OBJ	=	$(SRC)

EXEC_NAME	=	basic

all: 		$(NAME)

$(NAME):
		gcc -o -lcsfml-graphics -lcsfml-window

clean:
  rm -f *.o

fclean:		clean
  rm -f $(NAME)

re:		fclean all
```



