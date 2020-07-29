# word-pictionary-list 

> List of [Pictionary words](http://www.classywish.com/pictionary-words/)

A package that will be useful if you're creating a word game like pictionary.

Used by [`sketchy`](https://github.com/engichang1467/Sketchy)

One-letter words are not included. Many common bad words are also filtered out.


## Install

```
$ npm install word-pictionary-list
```


## Usage

```js
const fs = require('fs');

// Returns the path to the word list which is separated by `\n`
const wordListPath = require('word-pictionary-list');

const wordArray = fs.readFileSync(wordListPath, 'utf8').split('\n');
//=> […, 'abmhos', 'abnegate', …]
```
