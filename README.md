c-lib-template
==============

This repository is a project template including files and directories used to create
C libraries. A script is provided in order to create the project, which will be
done over a git repository. The basic structure of the new project is represented
below.

    project dir
    |-- Makefile
    |-- LICENSE
    |-- src
    |    |-- c files
    |    `-- h files
    `-- test
        |-- Makefile
        `-- test files (c files)


The Makefile in the root of the project will build all C files inside of **src**,
while the Makefile inside of **test** will build all C files in its directory.

The tests run through valgrind and it's expected to have one test per C file.
To start the tests execute `make run-tests` inside of **test** directory.


How to use
---

Execute the script `create-library` using the following syntax.

    ./create-library <library_name> <destination_path>

A new git repository containing the project will be created at destination path.

You can specify the license to be used on your project, in this case a file named
**LICENSE** is created on the root of the project and the license information is
added to the header of the C files.

    ./create-library <library_name> <destination_path> --license=MIT
