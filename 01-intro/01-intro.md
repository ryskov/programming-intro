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

Now that we understand what a programming language is, lets zoom out again and look at it from a programmers perspective. Programming is nothing more than writing text into a file and having a program translate/run it. The file is not special. There is nothing special about it. It could be written in notepad (thats actually how i started). The reason i point this out is just because i don't want you to be overwhelmed. It is just one or more text files being fed into another program. Thats it. You might have seen screenshots of code with fancy colors in fancy text-editors, but the only thing those fancy text-editors do is provide some readability and utility to the process. In the end it just manipulate files in the same way that TextEdit or notepad does it.

### 1.2 How does a computer understand and execute code
As we just went over, a computer does not instinctively understand your code. I mentioned before that code needs to be translated into bytecode before it can run. That is actually not always the case. Some languages are what we call **interpreted** languages. These languages does not bother with translation into bytecode, but are actually read by another program line-by-line, understood and executed directly by that other program. So to summarize we have 2 types of languages:
- Compiled languages - these are translated into bytecode once by another program (a compiler) and can then be run without relying on another program being present on the computer that needs to run it.
  - Examples: C, C++, Rust, Go
- Interpreted languages - these are run line-by-line by another program (an interpreter) in real time and therefore requires this program to be present on the computer that needs to run it.
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
NAME="Robert"
LAST_NAME="Marley"
NICK_NAME="Lil Bob"

FULL_NAME="$NAME $LASTNAME"

echo "My name is $FULL_NAME but you can just call me $NICK_NAME"
```
Output:

`> My name is Robert Marley but you can just call me Lil Bob`

How does one go from here - this is just some text on a webpage, doesnt do anything - lets talk about tools

## 2 Basic Tools
What are the basic tools we need to get started? It differs alot from programmer to programmer what tools to have in the belt, but i will explain a few that should be enough to get started.

### 2.1 Terminal / Shell
- Dont be scared, just a textual way of doing things you already do
  - Examples, going to a folder, doubleclicking something, creating files, moving them, executing applications
- Similarity between unix / linux / macos - why mac is popular among developers

### 2.2 IDE
- A tool to create the text file
- Practically nothing stopping you from using something like notepad, but IDE's just have useful tools and features designed for programming




## Notes
- line-by-line - udspecificér
- go through conventions in examples
