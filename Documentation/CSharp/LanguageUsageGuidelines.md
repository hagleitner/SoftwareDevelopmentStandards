# C# Lanugage usage guidelines

## Using implicitly typed variables (var)
Using var keyword can significantly improve the code, not just save some typing. We therefore use ´var´in all places.

Motivation: 
* It induces better naming for local variables. When you read local variable declaration with explicit type, you have more information at that moment and something like `IUnitTestElement current` makes sense. However, when this local variable is used later, you read `current` which takes some time to figure out the meaning. Using `var currentElement` makes it easier to read at any place.

* It induces better API. When you let compiler deduce type from method return type or property type, you have to have good types in the first place. When you don't have explicit type in the initialization expression, you have to have best names for members.

* It induces variable initialization. It is generally a good practice to initialize variable in the declaration, and compiler needs initializer to infer type for local variable declared with `var` keyword.

* It removes code noise. There are a lot of cases, when implicitly typed local will reduce amount of text developer needs to read, or rather skip. Declaring local variable from new object expression or cast expression requires specifying type twice, if we don't use `var`. With generics it can lead to a lot of otherwise redundant code. Another example would be iteration variable in foreach over Dictionary<TKey,TValue>`.


## Exceptions
### Exceptions vs. Special values
* We prefer exceptions over special return values
* Use the `bool TrySomething(inputParameter, out OutputParameter)` pattern for 'Expected' exceptional circumstances

### NotImplementedException
We treat NotImplementedExceptions as TODOs therefore the same rules apply. See [Todo comments](CodeComments.md#todo-comments) for more details