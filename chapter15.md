#  Development Tools

## Introduction
  Chapter 15 of Brian Ward's book How Linux Works What Every Super User Shoud Know talks about development tools
  in the Linux Environment. Knowing how to run the C programming language compiler can help you better understand
  the origin of the programs that you see on your Linux system. The source code for most Linux utilities and for many
  applications on Linux systems is written in C or C++.This is the reason why you should be familiar with 
  programming tools. The most important thing to know is about shared libraries. 
  
  C programs follow a traditional development process: You write the programs, you compile them and they run. To run a
  program write in C first you must **compile** the source code that you wrote into a binary low-level form that the compter 
  can understand. The C compiler executable on most Unix systems is the GNU C compiler. C source code files end with .c
  The command *cc -o file file.c* gives the name file to the executable that the C compiler should spit out after you
  run the previuos command. 
  
  C **header files** are additional source code files that usually contain type and library function declarations. Most 
  glitches occur when the compiler can't find header files and libraries. The C compiler does not do all the work of looking 
  for the of the include files. That task falls to the **C preprocessor**, a program that the compiler runs on your source 
  code before parcing the actual program. It's a tool for making the source code eeasier to read (and for proving shortcuts).
  Preprocessor comamnds in source code are called **directives** and they start with the # character. The three basic types
  are: *Include files* *Macro definitions* *Conditionals* 
  **The C processor does not know anything about C syntax, variables, functions, and other elements. It understands only
  its own macros and derectives**
  
  You need ** libraries ** to build complete programs. A C library is a collection of common precompiled funtions that you can
  build into your program. A library file ending in .a is called a ** static library **. When you link a program against a static
  library, the linker copies machine code from the library file into the executable. Therefore, the final executable does not need
  the original library file to run and the execuable's behavior never changes. 
  The four things you need to know to bring shared libraries under control:
  1. How to list the shared libraries that executable needs.
  2. How an executable looks for shared libraries.
  3. How to link a program against a shared library.
  4. The common shared library pitfalls.
  
  The two standard library directories on a Linux system are */lib* and */usr/lib*. The */lib* directory should not contain static 
  libraries. A shared library has a suffix that contains .so (shared object).
  To see what shared libraries a program uses run the command *ldd prog* where *prog* is the executable name.
  A small program call *ld.so* finds and loads shared libraies for a program at runtime. 
  
  Shared libraries provide remarkable flexibility and incrediable hacks, but it's also possible to abuse them to the point where
  your system becomes a mess. These are the three things that could happen:
  1. Missing libraries
  2. Terrible performance
  3. Mismatched libraries
  
  The number one cause of all shared library problems is the environment variable named *LD_LIBRARY_PATH*. Never set LD_LIBRARY_PATH
  in shell startup files or when compiling software. Avoiding LD_LIBRARY_PATH prevents most shared library problems. 
  
  *Make* is a traditional Unix compile management utility that compiles source code for more than one file. Rather than you doing it 
  by hand this program eases that trouble. The basic idea behind make is the *target*, a goal you want to achive. A target can be a
  file (a .o file, and executable and so on) or a label. Some targets depend on other targets. These requirements are called *dependencies*
  The most common macros: 
  
  1.**CFLAGS** C compiler options. When creating object code from a .c file, make passes this as an argument to the compiler.
  2.**LDFLAGS** Like CFLAGS, but they're for the linker when creating an executable from object code.
  3.**LDLIBS** If you use LDFLAGS but do not want to combine the library name options with the search path, put the library name 
  options in this file.
  4.**CC** The C compiler. The default is cc.
  5.**CPPFLAGS** C *preprocessor* options. When make runs the C preprocessor in some way, it passes this macro's expansion on as argument
  6.**CXXFLAGS** GNU make uses this for C++ compile flags.
  
  A make *variable* changes as you build targets. You never set make varables by hand. 
  **$@** When inside a rule, this expands to the current target.
  **$*** Expands to the basename of the current target. 
 
  The standard debugger on Linux systems is gdb. to start gdb on an executable run *gdb program_name*
  
  ### Scripting Languages 
  
  The first thing to note about scripting languages is that the first line of a script looks like the shebang of a Bourne 
  shell script. For example a Python script starts like this: *#!/usr/bin/python*. In Unix any executable that starts with 
  #! is a script. Python is a scripting language with a strong following and an array of powerfeatures, such as text processing,
  database access, networking, and multithreading. Python's executable is python and it's usually found in */usr/bin*. 
  

#### Thanks for reading! 
