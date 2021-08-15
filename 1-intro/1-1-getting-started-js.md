# Getting Started with JavaScript

In this article i will walk you through the basics needed to write execute JavaScript on your computer. It is recommended that you read the [previous article](1-programming-intro.md) if you haven't already.

Lets get some things straight. We will be learning and writing [JavaScript](https://en.wikipedia.org/wiki/JavaScript) throughout this series because it is a versatile language with a very common syntax. Nowadays it is used for both frontend and backend programming and learning it will certainly not do any harm. If you can get used to writing JavaScript (sometimes just called JS) you will have an easy time quickly learning the syntax of a ton of other languages.

For this article we will keep it short and stop when we have succecfully written and executed some code on your computer.

## Table of contents

- [1 Getting setup](#1-getting-setup)
  - [1.1 Visual Studio Code](#11-visual-studio-code)
  - [1.2 Terminal](#12-terminal)
  - [1.3 NodeJS](#13-nodejs)
- [2 Writing code](#2-writing-code)

## 1 Getting setup
To get started you will to have the following installed.

### 1.1 [Visual Studio Code](https://code.visualstudio.com/) 
You already have this because you are not a slacker and read the previous article, right?

### 1.2 Terminal
If you are using a Mac you already have this AS YOU ALREADY KNOW FROM THE PREVIOUS ARTICLE.

### 1.3 NodeJS 
This one is new! [NodeJS](https://nodejs.org/) is the [interpreter](1-programming-intro.md#12-how-does-a-computer-understand-and-execute-code) for JavaScript. Yes, you are correct, JavaScript is **not** a compiled language and it requires this to execute on your computer. Just visit [this download page](https://nodejs.org/) and download and install the `LTS` version on the frontpage.

Well, that is actually everything we need to get started. 

## 2 Writing code
Now we are ready! Since you obviously read the [previous article](1-programming-intro.md) i assume you have already created a `programming` folder inside of your Documents folder. Well, we might as well use that as our base for this series. Here we will create our projects and all of our files will be contained in this folder.

Fire up a terminal and lets jump right into it:

`cd ~/Documents/programming`
> You know this command from before, but i just want to point out that `~/` has a special meaning when used in a path: its the logged in users 'home directory'. Now you know. Don't stress about it.

Lets create a new folder in here for this small demo. We can call it `first-js-project`

`mkdir first-js-project`
> Since we used `cd` to navigate our terminal into the `programming` folder the `first-js-project` folder will be created inside of this. You can always run `pwd` in a terminal to see where you are. Come on, try it.

Yay, so we set up a folder for our first project. Lets navigate into it:

`cd first-js-project`

Cool, so now we have an empty folder, what now? Well lets create our first JavaScript file:

`touch app.js`

Nice! To verify that it was created you can use the following command to list the contents of the folder that your terminal are in:

`ls`

You see it right? Nice, now lets boot up that Visual Studio Code (VS Code from now on) that you have installed.

When opened, you should be presented with some kind of 'Welcome' screen. Fuck that, we will just use the application menus at the top (Code, File, Edit, Selection, View, etc.). Click `File -> Open...` and a typical 'browse' window will be opened. Here we need to select a 'project folder' (and not a file). Remember we just created one? `first-js-project`. See if you can find it. It should be easy to locate if you can navigate to your *Documents* folder.

After opening our project folder in VS Code we are ready to begin! But before we do that, lets take some time to look around and see the structure of this text editor. To the left you can probably see your `app.js` file listed. This is where you can see, add, select and remove files (try right clicking in this section, right below your file). Doing this is no different than doing it in Finder or a terminal, but it is very handy to be able to do that without leaving your editor.

Now try to click on `app.js`. An empty text editor should show up, taking most of your screen. This is where the magic happens. Now write (you can copy paste but you will feel cooler if you write it out) the following to the file:

```javascript
let name = 'Robert'
let lastName = 'Marley'
let nickName = 'Lil Bob'

let fullName = name + ' ' + lastName

console.log('My name is ' + fullName + ' but you can just call me ' + nickName)
```

Now press ⌘S to save the file (alternatively go to `File -> Save` but who does not like hotkeys).

You just saved your first JavaScript file! Let verify that it actually got saved and you did not fuck up saving the file (in which case you are in for a long one). Go back to your terminal, still open and navigated to your project folder, and type:

`cat app.js`
> `cat` simply displays the content of a file.

Did your code show up? If it did then you actually managed to save the file, nice. Lets see if it runs! Type the following into your terminal:

`node app.js`
> `node` is a command that was installed when you installed NodeJS earlier. This is how you make it run your code. Big and important step!

If you did everything correctly, you should now see the expected output in your terminal:

> `My name is Robert Marley but you can just call me Lil Bob`

Congratulations! It might seem useless (and it is) but if you made it this far we are actually ready to begin the journey. We passed the bumps of setting everything up and we are live and running with all the required tools and some basic usage of the terminal. 
