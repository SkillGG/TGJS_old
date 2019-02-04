Documentation Of This Engine
=============================

This is _para engine_ which means, that it does not really
have too much functions.
I hope it will change and in some time this _para engine_ will become full
JS **engine**.

This is my first big project so this documentation will not
be best you've ever seen.
Please be aware of this.

How to use?
-----------

So first thing you want to do is to download newest release or 
just [TextEngine.js](TextEngine.js).

Then add it to your HTML project with this line and start using it in your code!

```javascript
<script src='TextEngine.js'></script>
```

What it provides?
-----------------

*TGJS* (TextGameJS) provides 3 variables, which contains a set of functions to make your life with showing your text in your game easier.

## Coder

Coder is a basic tool to make all code elements trigger a callback after click.

It adds a mouse command clicking which makes playing game much more easy.

You just have to put into your HTML &lt;code&gt; element
with class `.codeIn`.

Coder has 4 basic functions:

|Name|Function|
|----|--------|
|[processLineE(*line*, *element*)](#coderprocesslinee)|Sets callback of `code.codeIn`s in *line* to [__inputonkeyup13__](#inputonkeyup13)|
|[processLineC(*line*, _element_)](#coderprocesslinec)|Sets callback of `code.codeIn`s in *line* to given *callback*|
|[processLinesE(*lines*, *element*)](#coderprocesslinese)|`Coder.processLineE` for more input Elements|
|[processLinesC(*lines*, *element*)](#coderprocesslinesc)|`Coder.processLineC` for more input Elements|
|[multiprocessLine(*line*, *elemets*)](#codermultiprocessLine)|`Coder.processLineE` for more output Elements|

You can check out how it works in this example: [here](Examples/RWCoder/CoderShow.html)


Now time too explain more deeply those commands.

### Coder.processLineE

>Syntax:
>>```javascript
processLine()
```