# Coding Standard

## Introduction

The Coding Standard also know as Coding Stlye is a set of rules, guidelines and programming conventions created within the company to build software uniformly. It helps other developers to understand code regardless of his author and it allows smoother code reviews.

In other words, standardization of code facilitate :

- Readability
- Debuging
- Maintenance
- Business Logic
- Reusability
- Testing

## Scope of execution

The following coding style applies to every program inside the company written in C. No matter which product or service you are working on, you should follow the guideline.

# Company Coding Style

The following parties explain how you should write and organize your code.

## 1. Files Organization

#### 1.1. Delivery folder content

Your delivery folder should only contains file required for compilation. Any post-compilation generated file and temporary file should not be inclued in your delivery folder.

**Good delivery folder tree**

    main.c
    src/
        print.c
        strings.c
        format.c
        compute.c
    headers/
        print.h
        strings.h
        format.h
        compute.h

**Bad delivery folder tree**

    main.c
    main.o
    ~main.tmp
    src/
        print.c
        print.o
        ~print.tmp
        strings.c
        strings.O
        ~strings.tmp
        format.c
        format.o
        ~format.tmp
        compute.c
        compute.o
        ~compute.tmp
    headers/
        print.h
        strings.h
        format.h
        compute.h

#### 1.2. File extension

Sources in your program, should only have file with `.c` and `.h` extension.

#### 1.3. File coherence

A source file should match a logic, and group all the functions associated.

    /!\ You should consider subdivide your code in multiple files if you have more than 5 functions.

#### 1.4. Naming and folders

The name of the file should represent the logical entity it defines, and thus be clear, precise and explicit.

**Clear, precise and explicit filename**

    get_articles.c
    get_comments.c
    get_authors.c

**Unclear filename**

    write.c
    find.c
    algo.c

Every folders and filenames should be in English and formatted according to the snake_case convention (composed only of lowercase, numbers, and underscores).

**good filename**

    get_articles.c
    get_comments.c
    get_authors.c

**bad filename**

    GetArticles.c
    GetComments.c
    GetAuthors.c

## 2. Global Organization

#### 2.1. File Header

The source files (`.c`, `.h`) must always start with the formatted header of the company. A Visual Studio Code extension is available to automatically generate the header.

    **************************************
    @company - company.io
    @project - Computer Vision Toolbox
    @author  - john@company.io
    @updated - 2020-04-05 18:35:02
    **************************************

#### 2.2. Functions separator

Each function inside a file should be separated by one empty line.

**Good function separation**

    int multiply(int x, int y) {
        ...
    }

    int main() {
        ...
    }

**Bad function separation**

    int multiply(int x, int y) {
        ...
    }
    int main() {
        ...
    }

#### 2.3. Global Variables

You should only use global variables when it comes to constant variable. Any non-constant variable should not be global.

Global variable should follow SNAKE_CASE (ALL CAPS) standard.

**Good Global Variable**

    const float VALIDITY_THRESHOLD=70.5

**Bad Global Variable**

    const int AGE=20
    const int threshold=20

## 3. Functions

#### 3.1. Functions coherence

A function should only do one thing and should not mix functionality.

**Good function**

    int multiply(int x, int y) {
        return(x * y);
    }

**Bad function**

    int compute(int x, int y) {
        int b = x + y
        int c = b + y

        for (i = 1; i < 11; ++i) {
            printf("%d ", i);
        }

        i = b + x
        for (b = 1; i < 11; ++i) {
            printf("%d ", i);
        }
    }

#### 3.2. Naming convention

A function should describe what it does. It must contains a verb and be explicit.

All function names should be in English, according to the snake_case convention (meaning that it is composed only of lowercase, numbers, and underscores).

**Good function name**

    int create_user(int age, char **name) {
        ...
    }

**Bad function name**

    int usr(int a, char** n) {
        ...
    }

    INT USR(INT A, CHAR **N) {

    }

    int CREATE_USER(int AGE, char **NAME) {
        ...
    }

#### 3.3. Number of lines

A function should be as small as possible. The longer the function is the most difficult testing will be difficult.

#### 3.4. Functions arguments

A function taking no parameters should take `void` as unique argument.
A function should not need more than 4 arguments

**\*Good functions arguments**

    int get_timestamp(void) {
        return date.now()
    }

    int multiply(int x, int y) {
        return(x * y);
    }

**\*Bad functions arguments**

    int create_user(int age, char **firstname, char **email, char **lastname, char **phone_number) {
        ...
    }

#### 3.5. Comments

There should be no comment within a function.
The function should be readable and self-explanatory but comment are allowed above the function to explain it.

#### 3.6. Nested functions

Nested functions are not allowed because it increase com- plexity.

## 4. Layout inside a function

#### 4.1 Line content

A line should correspond to only one statement.

Avoid to :

- have several assignments on the same line
- have several semi-colons on the same line, used to separate several codesequences
- a condition and an assignment on the same line

for exemple, avoid :

```
a = b = c = 0;
```

or

```
a++; b++;
```

## 4. Layout inside a function

#### 4.1 Line content

A line should correspond to only one statement.

Avoid to :

- have several assignments on the same line
- have several semi-colons on the same line, used to separate several codesequences
- a condition and an assignment on the same line

for exemple, avoid :

```
a = b = c = 0;
```

or

```
a++; b++;
```

#### 4.2 Indentation

All files in the project must have the same indentation

#### 4.3 Spaces

Always place a space after a comma or a keyword

for exemple :

```
return(1); => KO
return (1); => OK
```

#### 4.4 Brackets

Opening curly brackets should be at the end of their line.
Closing curly brackets should always be alone on their line, except in the case of an else statement.

for exemple :

```
if (cond) {
    ...
} else {
    ...
}
```

# Blog **Posts**

https://medium.com/@marilu597/general-coding-guidelines-clean-code-from-day-1-9ab0804e5d91

https://www.geeksforgeeks.org/coding-standards-and-guidelines/

https://levelup.gitconnected.com/write-better-code-with-coding-standards-546faf3fd4d1

https://medium.com/level-up-web/what-is-a-programming-style-guide-and-why-should-you-care-9019e51bb7ad
