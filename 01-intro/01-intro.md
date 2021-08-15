# Intro
Welcome! This short introduction will help you understand the most basic concepts required to get started programming.

## Table of contents
- [1 Programming](#1-programming)
  - [1.1 What is aprogramming language](#11-what-is-a-programming-language)
  - [1.2 How does a computer understand and execute code](#12-how-does-a-computer-understand-and-execute-code)
  - [1.3 Code example](#13-code-example)
- [2 Basic Tools](#2-basic-tools)
  - [2.1 Terminal / Shell](#21-terminal--shell)
  - [2.2 IDE](#22-ide)


## 1 Programming
Before we dive into the basic concepts of programming, let me start by warning you that i will be somewhat simplifying some of the stuff. 

### 1.1 What is a programming language
So what actually are programming languages? Programming languages are actually just a way for humans to interact with a computer. They are defined by a set of rules (syntax) and conventions (variable naming, common patterns), totally made up whenever they were 'invented'. There is nothing magical about how you write in a specific language and when you start coding and have questions to why something in a specific language is some way, the answer will most often be: because someone decided so at some point (probably with good reason and after heavy discussion). 

It is also important to understand that programming languages are **not** understood by a computer. For a computer to execute **anything** it must first be translated into what we call *bytecode*. This means that code you write in a programming language is actually undergoing some steps before the computer actually executes it. This translation **is what defines the programming language**: for a programming language to exist, someone must first create a program that can do this translation. So different programming languages are actually just different ways to end up exactly the same, bytecode.

Now that we understand what a programming language is, lets zoom out again and look at it from a programmers perspective. Programming is nothing more than writing text into a file and having a program translate/run it. The file is not special. There is nothing special about it. It could be written in notepad (thats actually how i started). The reason i point this out is just because i don't want you to be overwhelmed. It is just one or more text files being fed into another program. Thats it. You might have seen screenshots of code with fancy colors in fancy text-editors, but the only thing those fancy text-editors do is provide some readability and utility to the process. In the end it just manipulates files in the same way that TextEdit or notepad does it.

### 1.2 How does a computer understand and execute code
As we just went over, a computer does not instinctively understand your code. I mentioned before that code needs to be translated into bytecode before it can run. That is actually not always the case. Some languages are what we call **interpreted** languages. These languages does not bother with translation into bytecode, but are actually read by another program line-by-line, understood and executed directly by that other program. So to summarize we have 2 types of languages:
- Compiled languages - these are translated into bytecode once by another program (a compiler) and can then be run without relying on another program being present on the computer that needs to run it.
  - Examples: C, C++, Rust, Go
- Interpreted languages - these are understood line-by-line by another program (an interpreter) in real time and executed and therefore requires this program to be present on the computer that needs to run it.
  - Examples: JavaScript, Python, PHP

So what is bytecode actually? Why don't we just write directly in bytecode, and skip this whole thing? Well, you can, and some do but it is an incredibly non-human thing to do and does not take our human abstractions into consideration. This type of code is 1-1 with how a CPU operates with its electrical circuits and binary (voltage) representation of numbers. 

Now that we know that we should not care about bytecode and accept that we **rely** on existing tools (programming languages) to get something done, lets dive straight into a couple of code examples to give you an idea on what programming looks like.

### 1.3 Code example
Lets take a look at some actual code. I have written the same code in two different languages to show that a language is just syntax and conventions while the basic concepts remain the same across both. I kind of want you to look at the examples and understand them yourself (and the similarity between them), without me guiding you through them. 

**JavaScript**
```javascript
let name = 'Robert'
let lastName = 'Marley'
let nickName = 'Lil Bob'

let fullName = name + ' ' + lastName

console.log('My name is ' + fullName + ' but you can just call me ' + nickName)
```
**Bash**
```bash
name="Robert"
last_name="Marley"
nick_name="Lil Bob"

full_name="$name $last_name"

echo "My name is $full_name but you can just call me $nick_name"
```
Output:

`> My name is Robert Marley but you can just call me Lil Bob`

I don't believe the logic in this program requires too much explanation but it might be worth pointing out some of the syntatic differences that sets them apart. Lets also touch on some conventions for both of those languages.

- **JavaScript**
  - We use the `let` keyword to define a *variable*. This is a syntax thing related to the language.
  - We typically name *variables* `inThisManner` ([camelCase](https://en.wikipedia.org/wiki/Camel_case)). This is a conventional thing. We don't **have to**, but everyone else is doing it so you might aswell.
  - To make the program write text to the screen we use `console.log('some text')` which is the way to do that in JavaScript
- **Bash**
  - In Bash we dont have a keyword for defining a variable. We simply go `VARIABLE="VALUE"`. Again, this is a syntax thing specific to this language.
  - Here we name variables `like_this` ([snake_case](https://en.wikipedia.org/wiki/Snake_case)). This is by convention and the program will not break if we don't.
  - When we want to write text to the screen we use `echo "some text"` which is how you do that in Bash

You might notice some patterns here. We can basically do the same things in both languages, we just have to abide to different syntaxes for the compiler or interpreter to understand what we mean. These rules are part of what defines a language and sets them apart from eachother.

Well, how does one go from here - this is just some text on a webpage, it does not do anything - lets talk about some tools that will get us started.

## 2 Basic Tools
What are the basic tools we need to get started? It differs alot from programmer to programmer what tools to have in the belt, but i will explain a few that should be enough to get started.

### 2.1 Terminal / Shell
Yes, a terminal. You might have seen it a billion times in pictures and movies (and maybe on your own computer). If you didn't know any better you might think they are boring, complicated and/or useless. Turns out, they are very useful for programmers because they provide a simple textual way of using a computer. They are actually not complicated, they just kind of do what you normally do on a computer but without using a mouse. Why is this good? Because it also allows us to execute our programs without thinking about implementing complicated visuals (windows) and mouse-logic. Actually when working in a backend setting, you will probably never write anything with a real [GUI](https://en.wikipedia.org/wiki/Graphical_user_interface).

There's absolutely no reason to be scared about learning to use a terminal. If you are on a Mac, you actually already have one installed. You can open it with spotlight (⌘-space) by typing `terminal` into it and pressing enter. We will go through the important stuff later, but to 'de-scare' you a bit, try writing out the following commands (execute each one by pressing enter - after the command i will add my comments, dont try to execute those, idiot):

`mkdir ~/Documents/programming`

> This command creates a new folder in your Documents folder (yes, the one you know from Finder). See if you can guess what `mkdir` stands for.

`open ~/Documents/programming`

> Now we use the `open` command. This is basically the same as double-clicking something in Finder. In this example we 'double-click' the new folder which then should open Finder directly inside your newly created folder.

`cd ~/Documents/programming`

> `cd` stands for 'change directory' and puts your terminal into the context of the newly created folder. This means that commands we execute from here on out takes place in this folder. It will make sense in the next few commands, but its worth pointing out that your terminal always are 'somewhere on your system', just like a Finder window. 

`touch hello`

> This command (`touch`) is a command that creates empty files. We name the file `hello` and since we are in your new folder (remember from previous command?) it will be created there. We opened the Finder window earlier with the `open` command, so you should be able to see a new file in there. Try to keep Finder open next to your terminal so you can see your changes in real time while you execute commands.

`mv hello helloNewName`

> `mv` means 'move' and is the command used for moving files. Actually what we just did was rename the file from `hello` to `helloNewName`. Think about it for a second and realize that renaming a file is actually just moving it. You should see the change in your Finder window - wow

`rm helloNewName`

> This command deletes our new file (RIP). You can probably figure out what `rm` means.

Stop for a moment now and look at your terminal and all the commands you just executed. Functionally it's all pretty familiar stuff. Creating files/folders, renaming them, deleting them. This is the point. A terminal is not magical, its a textual way to control a computer. Even if you think it's useless at this point, it will become **very** useful when programming and you will find out why down the road.

### 2.2 IDE
What is an IDE? IDE stands for "Integrated Development Environment" and it's just a overly fancy word for "text editor with colors, file management and useful tools". You do not actually need one but i would **not** advise you to not use one. Even if we are only going to be using simple features (managing and writing files) they provide a ton of help by simply coloring your code and helping you 'space it out' to make it way cleaner to comprehend when writing and reading it. 

The thing about IDE's is that there exists a ton of them. Some free, some paid, some only supporting writing a single language, heavy ones with tons of tools, light ones with support for extensions. I personally prefer the latter, and for the remainder of this guide-series i will recommend that you download and install [Visual Studio Code](https://code.visualstudio.com/). I use this for everything both comercially and privately. It's free, open source, well-supported (created by Microsoft) and very extensible when specific needs arises.


