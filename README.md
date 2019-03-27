# README

NOTE: To get the most out of this short tutorial, please make sure that you are familiar with the command line and with using NPM.

## Goal

In this tutorial we're going to talk about how to begin using Webpack. Webpack is a "bundler." A bundler  is a piece of softare that takes the assets that make up a site or application and "bundles" them together into one or just a few files, performing a series of optimizations in the process. The assets in question are often JavaScirpt files, but can also include HTML, CSS, images, and other assets. Webpack is the most popular bundler out there right now, although there are many others, e.g. Parcel, Rollup, Browserify, etc.

Once you've completed this and the following tutorials, check out the [webpack docs](https://webpack.js.org/).

## Setup Your Project

This repo contains the completed project. You can fork it and clone it to see it in action, but you'll also want to create a fresh project as you follow along with this README.

Create a new directory for your project and after cd'ing into that directory, run the following command:

```bash
npm init -y
```

This command will create a package.json file in your  project directory with some default settings. Don't worry about it right now.

This is also a good time to initialize git, and make your first commit.

```git
git init
git add .
git commit -m "Initial commit"
```

Don't forget to make regular commits as you progress.

## Install Webpack
Now you can install webpack, and webpack-cli.

```bash
npm install --save-dev webpack webpack-cli
```

When the installation completes, you'll notice that you now have a node_modules folder in your directory and a package-lock.json file. Don't worry about those.

## Create index.html File

Once you have a project in which you've installed Webpack and the Webpack CLI, you're ready to create an index.html file.

Our HTML file should look something like this:

```HTML
    <!DOCTYPE html>
    <html lang="en">
    
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <meta http-equiv="X-UA-Compatible" content="ie=edge">
            <title>Webpack Test</title>
        </head>
        
        <body>
            <h1>Hello, world!</h1>
        </body>
        
    </html>
```            

## Create a src Directory, index.js, and hello.js Files

The final pieces that you'll need are a 'src' directory, an 'index.js' file inside of that directory, and a second file called 'hello.js.' Open these files in this repository now and take a look. index.js imports hello.js and calls it from within a console.log statement. hello.js returns a greeting, e.g. "Hello, Julian". 

## Run 'npx webpack'
Now enter the command 'npx webpack' on the command line. This command will create a new 'dist' directory containing a file called 'main.js' that in turn contains all of your  processed and bundled JavaScript. 'main.js' is the default name that webpack gives your  bundled JS.

We're only using two scripts in our example, but you could have any number of scripts and as long as they're imported into index.js, Webpack will bundle them together.

## Add the script to index.html
In order to see your  script in action, we'll need to return to index.html and insert a script tag before the closing body tag in order to import main.js. The src path is 'dist/main.js'. 

That's it! you can serve index.html via a development server or just open the file in your browser.

Right now, you'll need to re-run 'npx webpack' each time you make any changes to your files. You'll also notice that by default, Webpack only bundles and minifies your JavaScript files. We'll address those things in the next few exercises.

[Next exercise](https://github.com/Code-with-Us/webpack-test-2)
