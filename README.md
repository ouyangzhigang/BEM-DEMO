# Stub to start a new [BEM](https://bem.info) project

Project-stub is a template project repository used for BEM projects creation. It contains the minimal configuration files and folders you will need for quick start from scratch.

There are two main BEM libraries are linked here by default:

* [bem-core](https://en.bem.info/libs/bem-core/)
* [bem-components](https://en.bem.info/libs/bem-components/)

## Installation requirements

* [Node.js 0.10+](http://nodejs.org) is a platform built on Chrome JavaScript runtime for easily building fast, scalable network applications. Or you could use [io.js](https://iojs.org/en/) as an alternative platform to Node.js.
* [Git Bash](http://msysgit.github.io/) if you use Windows OS.

## Supported browsers

The list of supported browsers depends on the [bem-core](https://en.bem.info/libs/bem-core/current/#supported-browsers) and [bem-components](https://en.bem.info/libs/bem-components/current/#supported-browsers) library versions.

>**NB** Internet Explorer 8.0 is not supported by default. To support IE8 you must follow the [recomendations](https://en.bem.info/libs/bem-components/current/#support-for-internet-explorer-8) or use the alternative way — a [generator-bem-stub](https://en.bem.info/tools/bem/bem-stub/) that ensures an optimal config file for your project creation.

## Installation

So, how easy is it to get started with BEM? — *Super easy!*

It's as easy as...

```
git clone https://github.com/bem/project-stub.git --depth 1 --branch v1.3.1 my-bem-project
cd my-bem-project
npm install # Do not use root privilege to install npm and bower dependencies.
```

`bower` dependencies are installed in the `libs` directory by `npm postinstall`.

## Usage

You could use the following tools to build the project: [ENB](https://ru.bem.info/tools/bem/enb-bem-techs/)(only in Russian) or [bem-tools](https://bem.info/tools/bem/bem-tools/). The result files are the same in both cases as `bem-tools` just calls `ENB` under the hood.

You can run any `enb` commands from a `node_modules/.bin/enb` directory and the `bem-tools` commands from `node_modules/bem/bin/bem`.

### Build the project

```bash
node_modules/.bin/enb make
```
or
```bash
node_modules/.bin/bem make
```

To be able to run commands without typing a full path to an executable file (`node_modules/.bin/enb`), use:

```
export PATH=./node_modules/.bin:$PATH`
```

Now you can use `enb` or `bem` from any point of your project.

```
enb make
```

### The basic commands

>Execute the following commands in your terminal.

You could use help option to get information about the basic commands of `enb` and `bem-tools`:

```
enb -h
```
and

```
bem -h
```

**Start the dev server**

```bash
node_modules/.bin/enb server
```
or
```bash
node_modules/.bin/bem server
```

You could use the `npm start` command to start the `enb server` without specifying the full path to the `node_modules`.

```bash
npm start
```

The `bem server ` is running. To check it out, navigate to `http://localhost:8080/desktop.bundles/index/index.html`.

**Stop the server**

Press `Ctrl` + `C` or `⌘` + `C` (for MAC devices) while the terminal is your active window to stop the server.

**Add a block**

```bash
bem create -l desktop.blocks -b newBlock
```

**Add a page**

```bash
bem create -l desktop.bundles -b page
```

>You could add aliases for super easy use:<br>
```
echo "alias 'bemblock'='bem create -l desktop.blocks -b'" >> ~/.bashrc
echo "alias 'bempage'='bem create -l desktop.bundles -b'" >> ~/.bashrc
```

## Generator of BEM projects for Yeoman

`project-stub` is a multipurpose template project that covers the most common tasks of the BEM project. If you want to create the most suitable configuration to build your project, use the [generator-bem-stub](https://en.bem.info/tools/bem/bem-stub/).

This generator provides you the ability to get the base of BEM project in few minutes by answering the simple questions.
- [generator-bem-stub](https://en.bem.info/tools/bem/bem-stub/)

## Docs

- [Full stack quick start](https://en.bem.info/articles/start-with-project-stub/)
- [Static quick-start](https://en.bem.info/tutorials/quick-start-static/)
- [Tutorial for BEMJSON template-engine](https://en.bem.info/technology/bemjson/current/bemjson/)
- [Tutorial on BEMHTML](https://en.bem.info/libs/bem-core/2.0.0/bemhtml/reference/)
- [Tutorial on i-bem.js](https://en.bem.info/tutorials/bem-js-tutorial/)
- [JavaScript for BEM: main terms](https://en.bem.info/articles/bem-js-main-terms/)
- [Commands bem-tools](https://en.bem.info/tools/bem/bem-tools/commands/)

## Project-stub based projects

- [Creating BEM application on Leaflet and 2GIS API](https://en.bem.info/tutorials/firm-card-story/)
- [Creating a menu of geo objects collections with Yandex.Maps API and BEM](https://en.bem.info/tutorials/yamapsbem/)
- [SSSR (Social Services Search Robot)](https://github.com/bem/sssr) — study app with BEM full-stack

## Useful tools

- [borschik](https://en.bem.info/tools/optimizers/borschik/) — borschik is a simple but powerful builder for text-based file formats

## Videos
- [BEM for JavaScript Talk on Camp JS](https://en.bem.info/talks/campjs-melbourne-2014/)
=======
# BEM-demo
BEM代表块（Block），元素（Element），修饰符（Modifier）。这些术语的含意将在本文进一步阐述。
Preliminary steps

Minimal requirements

Node.js 0.10+ or io.js.
Git Bash if you use Windows OS.
A local copy and environment setting

A template repository is the quickest and easiest way to start your BEM project. It contains the minimal configuration files and folders.

NB If your operating system is Windows, you must run the following commands in Git Bash with administrator rights.

Make a local copy of project-stub.

NB Do not use root rights to install npm and bower dependencies. bower dependencies are installed in the libs directory by npm postinstall.

git clone https://github.com/bem/project-stub.git --depth 1 --branch v1.3.1 start-project
cd start-project
npm install
Run the server using ENB (this article is available only in Russian).

npm start
Check the result on http://localhost:8080/desktop.bundles/index/index.html.

A page with library blocks examples should open:

A main page

Steps for creating the project

Create a page
1.1 Describe the page in a BEMJSON file
Create a block
Implement the hello block
3.1 Use JavaScript technology
3.2 Use BEMHTML technology
3.3 Use CSS technology
When all steps have been completed you can watch the result.


1. Create a page

Source code of pages is stored in the start-project/desktop.bundles directory. The main page index contains implementations of blocks for the bem-components library.

Create a new page to start your own project.

Create the hello directory in the desktop.bundles.
Add the hello.bemjson.js file to the hello directory.

1.1 Describe the page in a BEMJSON file

A BEMJSON file describes a page structure in BEM terms: blocks, elements and modifiers.

Add a description of the hello block in the desktop.bundles/hello/hello.bemjson.js file.
hello block is an entity that will contain all necessary elements for the project.

 ({
     block : 'page',
     title : 'hello',
     head : [
         { elem : 'css', url : 'hello.min.css' }
     ],
     scripts : [{ elem : 'js', url : 'hello.min.js' }],
     mods : { theme : 'islands' },
     content : [
         {
             block : 'hello'
         }
     ]
 })
Place the greeting element with the greeting text (content field) into the hello block.

 content : [
     {
         block : 'hello',
         content : [
             {
                 elem : 'greeting',
                 content : 'Hello, %user%!'
             }
         ]
     }
 ]
To create an input field and a button, use input and button blocks from the bem-components library. Add these blocks to the hello block`.

 content : [
     {
         block : 'hello',
         content : [
             {
                 elem : 'greeting',
                 content : 'Hello, %user%!'
             },
             {
                 block : 'input',
                 mods : { theme : 'islands', size : 'm' },
                 name : 'name',
                 placeholder : 'User name'
             },
             {
                 block : 'button',
                 mods : { theme : 'islands', size : 'm', type : 'submit' },
                 text : 'Click'
             }
         ]
     }
 ]
Code sample hello.bemjson.js.

To verify that the page shows all necessary objects, open http://localhost:8080/desktop.bundles/hello/hello.html.

You can make additional changes to existing blocks on your redefinition level.


2. Create a block

In order for all objects on the page to work correctly, it is necessary to specify additional functionality of the hello block on your redefinition level.

Create a directory of the hello block on the desktop.blocks level.
Create the implementation technology files (CSS, JS, BEMHTML) required by the block in the hello directory. The block directory name and its nested files must coincide with the block name specified in the BEMJSON file.

hello.js – describes dynamic page functionality.
hello.bemhtml – a template for generation of the block HTML representation.
hello.css – changes the design on the page.

3. Implement the hello block

To implement the block in BEM terms, use the created technology files.


3.1 Implement the hello block in JavaScript technology

Describe the block reaction to a user's action using the onSetMod property in the desktop.blocks/hello/hello.js file. A click on the button adds the user name from the input field to the greeting phrase.
JavaScript code is written using i-bem.js (this article is available only in Russian) declarative JavaScript framework.

 onSetMod: {
     'js': {
         'inited': function() {
             this._input = this.findBlockInside('input');

             this.bindTo('submit', function(e) {
                 e.preventDefault();
                 this.elem('greeting').text('Hello, ' + this._input.getVal() + '!');
             });
         }
     }
 }
To represent the current JavaScript code, use the YModules modular system .

 modules.define(
     'hello', // a block name
     ['i-bem__dom'], // dependence connection
     function(provide, BEMDOM) { // a function that received names of the used modules
         provide(BEMDOM.decl('hello', { // a block declaration
             onSetMod: { // a constructor that describes reaction on an event
                 'js': {
                     'inited': function() {
                         this._input = this.findBlockInside('input');

                         this.bindTo('submit', function(e) { // the event that causes reaction
                             e.preventDefault(); // prevention of event triggering by default (form data sending to the server with page reload)
                             this.elem('greeting').text('Hello, ' + this._input.getVal() + '!');
                         });
                     }
                 }
             }
         }));
     });

3.2 Implement the hello block in BEMHTML technology

BEMHTML is a technology that processes BEMJSON declarations to create HTML layout of a web page.

Write a BEMHTML template and specify that the hello block has JavaScript implementation.
Implement the hello block with form, adding tag mode.
block('hello')(
    js()(true),
    tag()('form')
);

3.3 Implement the hello block in CSS technology

Create your own CSS rules for the hello block. For example:

.hello
{
    color: green;
    padding: 10%;
}

.hello__greeting
{
    margin-bottom: 12px;
}

.hello__input
{
    margin-right: 12px;
}
To add to input block the CSS rules that are already implemented in the input element of hello block, mix element using the field mix in the input data (BEMJSON).

{
    block : 'input',
    mods : { theme : 'islands', size : 'm' },
    mix : { block : 'hello', elem : 'input' }, // mix element to add CSS rules
    name : 'name',
    placeholder : 'User name'
}
Code sample hello.bemjson.js.


The final result

To see the result of the project, please refresh the page:

http://localhost:8080/desktop.bundles/hello/hello.html
Since the project consists only of one page, there is no need for a full build. Description of a more complex project is in Starting your own project article.

If you've spotted a typo or a mistake, or wish to add something on, you could write about it.
a1b51e3646432
