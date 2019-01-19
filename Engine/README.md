# Documentation for TextEngine

## Object Definitions

|Name|Definition|
|----|----------|
|`Line`|*DOMElement* (often *DIV*) with `LineDOMArgs`|
|`LineArray`|*Array* of `Line`|
|`typeElement`|*Object* with `TypeArgs`|
|`typeFunctions`|*Object* with functions (from `functionList`)|
|`functionList`|*Array* containing `functionStringN`s of **ignite**, **before**, **after** functions|
|`functionStringN`|*String* formatted as `<functionStage>: <functionName>`|
|`functionStage`|*String* that marks stage when function is invoked {**ignite**:`'i'`, **before**:`'b'`, **after**:`'a'`}|
|`functionName`|*String* name of function|

## Typer Arguments

|Argument|Explanation|
|-------|----------|
|`tF`|`functionList`|