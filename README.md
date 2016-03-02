# Kickstart with Express.js and Node

This document describes the initial steps to get started with Node.js and ultimately with Express.js

## Introduction

### What is Node.js?

Node.js is an open-source, cross-platform runtime environment for developing server-side Web applications. Although Node.js is not a JavaScript framework, many of its basic modules are written in JavaScript, and developers can write new modules in JavaScript.

For more information visit [Node.js Official Site](https://nodejs.org).

### What is Express.js?

Express.js is a web application server framework built on top of Node.js, designed for building single-page, multi-page, and hybrid web applications. It is the de facto standard server framework for node.js.

## Getting started with Node.js

This is really easy. Hit the [Node.js website](http://nodejs.org/) and click the big green Install button. It'll detect your OS and give you the appropriate installer (if for some reason it doesn't, click the downloads button and grab the one you need). Run the installer. That's it, you have installed Node.js and, equally important, NPM – Node Package Manager – which lets you add all kinds of great stuff to Node quickly and easily.

Open a command prompt
cd to the directory in which you wish to keep your test apps

To check the version of node you just installed, fire below command:

```bash
> node --version
```

## Install Express Generator

Now that we have Node running, we need the rest of the stuff we're going to actually use to create a working website. To do that we're going to install Express, which is a framework that takes Node from a barebones application and turns it into something that behaves more like the web servers we're all used to working with (and actually quite a bit more than that). We need to start with Express-Generator, which is actually different than Express itself ... it's a scaffolding app that creates a skeleton for express-driven sites. In your command prompt, type the following:

```bash
C:\node>npm install -g express-generator
```

The generator should auto-install, and since it (like all packages installed with -g) lives in your master NPM installation directory, it should already be available in your system path. So let's use our generator to create the scaffolding for a website.


## Create an Express Project

As we are going to use Express, we need to keep in mind that it uses Jade as its template engine. Jade or another templating engine is used to gain access to our Node/Express-based data. For more information on Jade refer [Jade Official Website](http://jade-lang.com/).

Now, In c:\node or wherever you're storing your node apps, type this:

```bash
C:\node>express nodetest1
```


This will create a skeleton express application which will have directory structure something like below:

```
create : nodetest1
create : nodetest1/package.json
create : nodetest1/app.js
create : nodetest1/public
create : nodetest1/public/javascripts
create : nodetest1/public/images
create : nodetest1/public/stylesheets
create : nodetest1/public/stylesheets/style.css
create : nodetest1/routes
create : nodetest1/routes/index.js
create : nodetest1/routes/users.js
create : nodetest1/views
create : nodetest1/views/index.jade
create : nodetest1/views/layout.jade
create : nodetest1/views/error.jade
create : nodetest1/bin
create : nodetest1/bin/www
```

Now, at the root of the Express project we have `package.json` file. Basically, this file holds various metadata relevant to the project. This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies. Basic structure of `package.json` looks somewhat like below:

```json
{
    "name": "nodetest1",
    "version": "0.0.0",
    "private": true,
    "scripts": {
        "start": "node ./bin/www"
    },
    "dependencies": {
        "body-parser": "~1.12.4",
        "cookie-parser": "~1.3.5",
        "debug": "~2.2.0",
        "express": "~4.12.4",
        "jade": "~1.9.2",
        "morgan": "~1.5.3",
        "serve-favicon": "~2.2.1"
    }
}
```

The dependencies that we have defined for our project can be installed using command below:

```bash
C:\node\nodetest1>npm install
```

Where `nodetest1` is our `Express` project directory. All the installed dependencies will reside in the folder `node_modules`. One can use the dependency in `.js` file using function `require()`.

e.g. 
```javascript
require('morgan');
```

Now, our Express project gets setup. It's time now to run the project. Head over to project directory and fire below command:

```bash
C:\node\nodetest1>node ./bin/www
```

OR

```bash
C:\node\nodetest1>node app.js
```

As entry point for any Express project is `app.js`

Everything working? Awesome! Open a browser and head for [http://localhost:3000](http://localhost:3000) where you will see a welcome to Express page.

so folks! That's about setting up Node.js and making Express.js up and running.

Let me know if you find any issues with this document. Suggestions are welcomed.

Happy node-ing!
