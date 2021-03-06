+++
title = "PPL"
description = ""
date = 2010-03-30T17:52:32Z
aliases = []
[extra]
id = 6670
[taxonomies]
categories = []
tags = []
+++

{{language
|untyped=yes
|site=http://www.ppl-lang.com}}
{{language programming paradigm|object-oriented}}
ArianeSoft PPL is a fast and easy-to-learn programming language that is fully [[object-oriented]]. PPL runs on [[Windows]] (XP and up) and Windows Mobile phones. Programs written for one system are 100% compatible with each supported platforms. PPL comes with a complete development environment on Windows.

PPL has been in active development for more than six years now. It has been used by thousands of people all over the world. PPL has proven to be very stable, many projects have been developed with it.


'''PPL 2 (Pocket Programming Language version 2)''' is an object-oriented programming language designed from the ground-up for Windows and Windows Mobile phones. It features:

The PPL language syntax is a mixture of [[C]], [[Pascal]] and [[Basic]]. There are no variable types in PPL. Everything is fully transparent, from string to char to integer or double. Multi-dimensional arrays and multi-level matrices are supported while structures can be defined with specific fields sizes. Pointers can be used the same way the C language handles them. String manipulation is done transparently and allocated dynamically just like in Pascal or Basic. Linked-lists are an integral part of the variable system in PPL. You can easily create linked-list variables with arrays of different size or different structures in each element. Windows [[API]] functions are easy to access. Simply define the function, the number of input and output parameters and the interpreter will do all the necessary work including WideChar conversions.

*Object Oriented framework
*Temporary object creation and method calling (ex: PDialog("Hello World!").Message)
*Syntax borrows the best from commonly used languages like C, [[C Sharp|C#]], Pascal and BASIC, so it's easy for all levels of developer to understand
*Implements advanced constructs like Arrays, Linked Lists and Matrices
*100% compatible with PPL v1.x procedural's syntax
*Regular expressions



```pascal
#class test
  Private(a$, b$);

  nproc Create
    Dim(b$, 10);
  end;

  property read a a$;
  property write a a$;

  property read b b$;
  property write b b$;

#endclass

proc main
  o$ = new test;
  o.a = 10;
  o.a += 15;
  ShowMessage(o.a++);
  (o$).a = 20;
  (o$).a += 25;
  o.b[0] = 50;
  ShowMessage(o.b[0]);
  Dim(l$, 10);
  l$[0] = o$;
  l$[0].b[1] = 60;
  ShowMessage(l$[0].b[1]);
end;
```


'''PPL Assembler:'''

PPL comes with a fully integrated assembler that uses an easy syntax. Results are super-fast and instant. Assembling is dynamic, therefore you don't need to compile your code in advance, you can do it on the fly. You write the code once and the assembler generate the binary code for each target platforms supported by PPL.


'''The PPL 2 IDE (Integrated Development Environment):'''

*Design your application visually using our new visual coding technology
*Inter-platform development - design the application on Windows and run it, without any modifications, on Windows Mobile
*Use our high-level source code editor, with code completion, syntax highlighting and code templates to greatly simplify your programming. Spend less time finding what is required to accomplish a task and get the results faster.
*Visual debugger.
*Code profiler to help you make your code the fastest possible.
*Memory leak analyzer.
*Create native stand-alone executable files for Windows and Windows Mobile.


'''Advanced Help System:'''

Providing help for the components you design has never been easier. PPL 2 comes fully loaded with an incredibly easy-to-use help editor and help viewer. Never worry about the layout of your help documents anymore, PPL takes care of it for you. The help engine, allows for fast searching and a uniform layout for all the help topics. The help engine also supports classes, properties, methods and events. It will create links to inherited classes, create topics for properties, methods and events. Get the professional help files without the work load.


'''The Tag Search System:'''

Have you ever waste valuable minutes trying to remember what was the name of that function that does what you were looking for but were not able to find it? This is a situation from the past now, PPL 2, offers a powerful tag search engine, that accept English-like search text and finds all functions, properties, methods, events, etc... that are related to that text. For example, if you are looking for a way to display some text in a dialog box on the screen, simply type: "display some text", you will get a list of all functions that relates to displaying text. That easy!


'''The PPL Control Library:'''

*All standard [[Microsoft]] controls are bundled in easy to use object oriented libraries
*Easily create your own controls using PCL (PPL Control Library) which provides an excellent framework to develop your applications.
*Package your components, help files and project templates in an easy to distribute format.
*Download and purchase components or component packages from our PPL Store.
*Easily install new components at the click of a button.


'''The Database library:'''

*[[SQLite]] v2 and v3 support (read here http://blog.gobansaor.com/2009/03/14/sqlite-as-the-mp3-of-data why we chose SQLite)
*Visual data grid and data controls
*Orion database engine
*Secure SSL encryption package


'''Advanced Game Engine to build 2D games for Windows and Windows Mobile:'''

*WYSIWYG game level editing - design your game levels visually
*Object-Oriented framework
*2D graphics support
**Drawing primitives (lines, boxes, circles)
**Image loading and manipulation (.BMP, .JPG, .PNG)
**Extensive support for sprites
*Isometric viewpoint support
*Particle engine
*Physics engine
*Sound engine
