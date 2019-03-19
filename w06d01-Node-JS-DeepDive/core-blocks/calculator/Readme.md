# Calculator

## IO operations
How to perform IO operations in node? There are several modules available for doing that. Read through [process], [readline](https://www.npmjs.com/package/readline), [readline-sync](https://www.npmjs.com/package/readline-sync) and [readline-stream](https://www.npmjs.com/package/readline-stream).

## Release 0
Create a simple node application which does the following operations.
- Addition
- Subtraction
- Multiplication
- Division

The program runs on console. It takes input from the console.

## Release 1
Now, seperate the calculation part and IO operations. Make a module named `calculator`

What's a module?
A module *generally* is 
>a folder containing a program described by a package.json file 

Now, install the module in your application which performs all the tasks of [Release 0](#release-0)

Note: Your application will now have 2 package.json files. One of them belongs to the calculator module which the second package.json belongs to the entire application.

## Release 2
Create a github repository which will host your calculator module. You can include that module in your application.

Use this command to install a github module in your application. 
`npm install --save <github username>/<github repository name>`


## Release 3
Add more functionality to your module.
- power
- Square root
- factorial


