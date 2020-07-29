# word-pictionary-list 

> List of [Pictionary words](http://www.classywish.com/pictionary-words/)

A package that will be useful if you're creating a word game like pictionary.

Used by [`sketchy`](https://github.com/engichang1467/Sketchy)

One-letter words are not included. Many common bad words are also filtered out.

Cryptographic-quality randomness is NOT the goal, as speed matters for generating sample text and security does not. `Math.random()` is used.

Installation:
```
    npm install word-pictionary-list
```

Examples:
```
    var randomPictionaryWords = require('word-pictionary-list');

    console.log(randomPictionaryWords());
    'ceiling'

    console.log(randomPictionaryWords(5));
    [ 'baby-sitter', 'Cake', 'curtain', 'Bonnet', 'Pose' ]

    console.log(randomPictionaryWords({ min: 3, max: 10 }));
    [ 'Strawberry', 'Duck', 'Mailman', 'Teacher' ]

    console.log(randomPictionaryWords({ exactly: 2 }));
    ['beside', 'between']

    console.log(randomPictionaryWords({ exactly: 5, join: ' ' }))
    'beggar boring Deep Popsicle Deep'
    
    console.log(randomPictionaryWords({ exactly: 5, join: '' }))
    'KiwiSand castleLoveafraidPacifier'

    console.log(randomPictionaryWords({exactly: 5, maxLength: 4}))
    [ 'Rug', 'Text', 'Nose', 'Crib', 'Egg' ]

    console.log(randomPictionaryWords({exactly:5, wordsPerString:2}))
    [ 'Mom Teacher', 'bubble Megaphone', 'Tourist afraid', 'Pirate Sun', 'computer monitor Rug' ]

    console.log(randomPictionaryWords({exactly:5, wordsPerString:2, separator:'-'}))
    [ 'Hug-blinds', 'computer monitor-Cake', 'comfy-Baseball', 'pole zoo sushi-Black Panther', 'laugh-Love' ]

    console.log(randomPictionaryWords({exactly:5, wordsPerString:2, formatter: (word)=> word.toUpperCase()}))
    [ 'MUSIC SPITBALL', 'PEANUT NURSE', 'BURP RUN', 'BIRD CHANNEL', 'BRAND PAIL BASEBALL' ]

    console.log(randomPictionaryWords({exactly:5, wordsPerString:2, formatter: (word, index)=> {
        return index === 0 ? word.slice(0,1).toUpperCase().concat(word.slice(1)) : word;
    }}))
    [ 'Pinwheel Egg', 'Honk Lighthouse', 'Cliff Game', 'Back seat sandbox', 'Mount Rushmore Buckle' ]
```