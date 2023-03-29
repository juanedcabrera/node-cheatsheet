# node-cheatsheet

How to Make a New Node/npm Project
So you want to make a new Node/npm project? It's not as hard as it sounds! Here are the steps you need to follow:

# What You'll Need
Before you start, you need to make sure you have Node.js installed on your computer. If you don't have it yet, you can download it from the Node.js website.

# Creating Your Project
Open up your terminal (that's like a command prompt for Mac and Linux) and navigate to the folder where you want to put your project.
Type npm init and hit Enter. This will ask you a bunch of questions about your project, like what you want to name it, what version number you want to give it, and what the entry point should be (that's the file that gets run when you start your project).
After you've answered all the questions, hit Enter again. This will create a package.json file in your project folder. This file keeps track of all the dependencies your project needs.

# Installing Dependencies
Now that you've created your project, it's time to install some packages! A package is like a bundle of code that someone else has written that you can use in your project.

Open up your terminal again (if you closed it) and navigate to your project folder.
Type npm install followed by the name of the package you want to install. For example, if you want to install the express package, you would type npm install express.
Hit Enter, and npm will download and install the package for you.
Using Packages in Your Project
Once you've installed a package, you can use it in your project! To do that, you need to require the package in your code. Here's an example:

const express = require('express');
const app = express();

// do some stuff with the express app here
This code imports the express package and assigns it to the express variable. Then, it creates a new Express app and assigns it to the app variable. You can use the app variable to create routes and do other things with your web app.

# Creating Your Own Modules
Sometimes you'll want to write your own code that you can use in multiple places in your project. You can do this by creating a module!

Create a new JavaScript file in your project folder. Let's call it math.js.
In math.js, write the code you want to export. For example:

function addNumbers(a, b) {
  return a + b;
}

module.exports = {
  addNumbers: addNumbers
};
This code defines a function called addNumbers that takes two arguments and returns their sum. Then, it exports that function using the module.exports object.

In your main JavaScript file (the one that's the entry point for your project), you can use the addNumbers function like this:

const math = require('./math');
const result = math.addNumbers(3, 5);
console.log(result); // outputs 8
This code imports the math.js module and assigns it to the math variable. Then, it calls the addNumbers function with the arguments 3 and 5 and assigns the result to the result variable. Finally, it logs the result to the console.

