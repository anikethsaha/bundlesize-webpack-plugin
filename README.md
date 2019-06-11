<p align="center" >
    <img src="https://imgur.com/Djb5EXk.png" width="200px" />
</p>
<h2 align="center">:zap: Webpack-docs :zap:</h2>

<p align="center" >
Webpack documentation on your terminal on go
</p>


# `$ webpack-docs [propertyname]`



### :warning: This package is still not published

## Why
Webpack is a awesome bundler which comes with handy configurations. Refering to docs for details about each confgi property is pretty common and frequent step. 

**Currently**, if we are in terminal and not sure about what a particular webpack config property does then we need to check the docs and other sites.

This is the command which will work similar to **man command in linux**.
The command will print the details of a particular webpack config property in the terminal on a go. the command will look like this
```bash
 $ node index man [property-name]
```
Here in the terminal itself, the user can write a command like
```bash
# example
$ node index man loaders
```
and then it will print the details along with the code supporting the `loader` property of the config file.

It will show the most and minimum details required to implement it not deep details.

**Describe the solution you'd like**

Below is what the feature I am expecting to look like

<img src="https://imgur.com/XLRcQlo.gif" />

I have implemented this feature in this just for demo purpose and we don't need to add any other extra dependency it works fine with the existing one

**Usage**

*This will print when no argument is passed that is ` $ node index man `*

```bash

    This Is a Manual For webpack config file

    $ node index man [webpack config name]

    example command:-

    $ node index man plugin


```

## Alternatives

Checking the docs :laughing:

## Current Implementation

The implementation can be improved as I have manually extracted the points from the docs. Also, I have made a curated list of command in a js object where its `propertyname : explaination `
In order to highlight the code and any notes or quotes, created a utility method to implement markdown like support for the explanation
Like for code its
```
---
INSIDE HERE ALL THE CODE
---

```
for quotes
```
>>> QUOTES OR NOTES HERE >>>
```

## How the commands will
### ` $ webpack-doc [The-config-property-you-want-to-know]  `
### ` $ webpack-doc --list `
List down all the properties whose docs are available in this package

### ` $ webpack-doc --i `
To search and get the docs in an interactive way


### **For On the go without installing the package**

### ` $ npx webpack-doc  [The-config-property-you-want-to-know]  `
