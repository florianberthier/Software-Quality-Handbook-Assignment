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


# Blog **Posts**

https://medium.com/@marilu597/general-coding-guidelines-clean-code-from-day-1-9ab0804e5d91

https://www.geeksforgeeks.org/coding-standards-and-guidelines/

https://levelup.gitconnected.com/write-better-code-with-coding-standards-546faf3fd4d1

https://medium.com/level-up-web/what-is-a-programming-style-guide-and-why-should-you-care-9019e51bb7ad