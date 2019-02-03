# Documentation for TextEngine

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

# Language

## Functions

### loadDictionaries:

> Syntax:
>
> *loadDictionaries(**dictionaryFiles**)*

For every *Object* in `dictionaryFiles` loads file from *path*
then parses its value as **dictLine**s and saves to
`Lang`.*name*.(**dictLine**`.name`)
