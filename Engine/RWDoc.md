Documentation Of This Engine
=============================
![](https://img.shields.io/badge/code--coverage-1%25-red.svg)

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
just [RWTextEngine.js](RWTextEngine.js) (ReWorked).

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

```javascript
//Syntax:
Coder.processLineE(line, element)
```

It 'extracts' every `code.codeIn` element from *line*
and then sets its `onclick` value to [__inputonkeyup13__](#inputonkeyup13).

|Parameter|Element|
|--|--|
|*line*|DOMElement which holds at least one `code.codeIn` element inside|
|*element*|InputDOMElement that has `onkeyup` function.|

```javascript
// Returns: 
			undefined // if everything went smoothly
			null // if error occured
```

But what is __inputonkeyup13__?

###### inputonkeyup13

It is a function, that converts given parameter to string and then

changes *element*.`value` to it. Then it invokes *element*.`onkeyup` with 
```javascript
{which: 13, keyCode: 13, target: element}
```

### Coder.processLineC
```javascript
// Syntax:
		Coder.processLineC(line, callback)
```

Essentially it is _Coder.processLineE_ just instead of setting callback to __[inputonkeyup13](#inputonkeyup13)__ you can choose a callback.

|Parameter|Description|
|--|--|
|*line*|Line same as in **[Coder.processLineE](#coderprocesslinee)**|
|*callback*|Function that will be called after player clicks on found element |

```javascript
// Returns: 
			undefined // if everything went smoothly
			null // if error occured
```

Your callback should look like this:
```javascript
callback = (event)=>{}
```
where *event*&nbsp; has:
```javascript
event.target;				// code.codeIn clicked
```




