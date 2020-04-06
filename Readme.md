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

    function multiply(int x, int y) {
        ...
    }

    function main() {
        ...
    }

**Bad function separation**

    function multiply(int x, int y) {
        ...
    }
    function main() {
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


# Blog **Posts**

https://medium.com/@marilu597/general-coding-guidelines-clean-code-from-day-1-9ab0804e5d91

https://www.geeksforgeeks.org/coding-standards-and-guidelines/

https://levelup.gitconnected.com/write-better-code-with-coding-standards-546faf3fd4d1

https://medium.com/level-up-web/what-is-a-programming-style-guide-and-why-should-you-care-9019e51bb7ad