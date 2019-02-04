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

><script src='TextEngine.js'></script>

What it provides?
-----------------

*TGJS* (TextGameJS) provides 3 variables, which contains a set of functions to make your life with showing your text in your game easier.

### Lang

First variable you should know is **Lang**.

It has functions, that helps you to make changing languages
less of a pain to programmer.

So how to use it? [Add main file to your project](#how-to-use)
and use it's functions typing prefix `Lang.`
for example:

>Lang.getFrom('x',0,0,'span');

### Lang Function List

|Name|Function|
|----|--------|
|[loaded](#langloaded)|Returns `true` if all dictionaries has been loaded correctly|
|[getFrom](#langgetfrom)|Returns innerHTML of given element with given *Line* properties|
|[getSpan](#langgetspan)|`getFrom(,,,'span')`|
|[getCenter](#langgetcenter)|`getFrom(,,,'center')`|
|[loadDictionary](#langloaddictionary)|Loads a single dictionary from file to `Lang` variable.|
|[loadDictionaries](#langloaddictionaries)|Loads an array of dictionaries from files.|
|[setLangToLines](#langsetlangtolines)|Sets language of every *Line* in given array|
|[setLangToLinesFrom](#langsetlangtolinesfrom)|Sets language to all *Lines* in array past given index|
|[translate](#langtranslate)|Translate given name. Loads its value to **innerHTML**|
|[reTranslate](#langretranslate)|Changes *Line* language to given new and `translate(*Line*)`.|

## Object Definitions

### Main Objects

|Name|Definition|
|----|----------|
|`Line`|*DOMElement* (often *DIV*) with some(or every) of [`LineDOMArgs`](#line-dom-arguments)|
|`LineArray`|*Array* of `Line`s|
|`typeElement`|*Object* with `Typer Arguments`|
|`typeFunctions`|*Object* with functions (from `functionList`)|
|`functionList`|*Array* containing `functionStringN`s for functions used in `Typer.typeClick` and `Typer.type` and `Typer.typeAll`|
|`functionStringN`|*String* formatted as `<functionStage>: <functionName>`|
|`functionStage`|*String* that marks stage when function is invoked {**ignite**:`'i'`, **before**:`'b'`, **after**:`'a'`}|
|`functionName`|*String* name of function|
|`dictionaryFiles`|*Array* of *Object*s containing *langCode*(`lang`) and *path* to file containing `dictLine`s|
|`dictLine`|*String* Line formatted as follows: ```<NAME>:{`<TEXT>`}```|

### Typer Arguments

|Argument|Explanation|
|--------|----------|
|`tF`|`functionList`|
|`charInterval`|*Number* delay in showing time between letters (**ms**)|
|`typeTo`|*DOMElement* typing destination|

### Line Arguments

|Argument|Explanation|
|--------|---|
|`Type`|*Object* with **clickPass**(`cp`), **tF**, **wait**, **charInter**(`inter`)|
|`get`|*String* **get**|
|`lang`|*String* **lang**|

### Line DOM Arguments

|Argument|Explanation|
|--------|-----------|
|*lang*|Language of `Line`|
|*clickPass*|Marks `Line` in `Typer.typeAll` to *proceed after mouse click*.|
|*tF*|`functionStringN`|
|*wait*|Delay between **ignite()** and **before()** in `Typer.type`/`Typer.typeClick` (**ms**)|
|*charInter*|**`charInterval`**|

# Lang

## Functions

### loadDictionaries:

> Syntax:
>
> *loadDictionaries(**dictionaryFiles**)*

For every *Object* in `dictionaryFiles` loads file from *path*
then parses its value as **dictLine**s and saves to
`Lang`.*name*.(**dictLine**`.name`)