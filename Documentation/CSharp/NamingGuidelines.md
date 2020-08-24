---
layout: default
title: Naming Guidelines
parent: CSharp
nav_order: 10
---

# Naming Guidelines

> Code is made up of three things: names, spacing and punctuation. With these three tools a programmer needs to communicate intent, and not simply instruct. A good name is more than a label; a good name should change the way the reader thinks. Good naming is part of good design. (Kevlin Henney, Giving Code a Good Name, Dot Net South West in July, 2017).

Good naming makes code readable and understandable and therefore maintainable. While we cannot formalize all aspects of good naming, these naming guidelines at least give us a framework for consistent naming.

### Capitalization Styles
Camel case: `systemEnvironment` [Definition on Wikipedia](https://en.wikipedia.org/wiki/Camel_case)\
Pascal Case: `SysxtemEnvironment` [Definition on Wikipedia](https://en.wikipedia.org/wiki/Camel_case)

* Pascal: Assemblies, Namespace, Type, Interface, Method, Property, Event, Field, Enum value, Nuget Package-Ids
* Camel: private Field, parameter, variables
* Uppercase: never. Except for 2 letter abbreviations

So even: 
* IoT is written as Iot
* HsM is written as Hsm
* ASCII is writen as Ascii

### Case Sensitivity
Even if C# supports case sensitivity, other languages that might access your framework do not. Any APIs that are externally accessible, therefore cannot rely on case alone to distinguish between two names in the same context.

### Word choice
* Choose easily readable identifier names. For example, a property named `HorizontalAlignment` is more English-readable than `AlignmentHorizontal`.
* Do favor readability over brevity. The property name `CanScrollHorizontally` is better than ScrollableX (an obscure reference to the X-axis).
* Do not use underscores, hyphens, or any other nonalphanumeric characters. The only exception to this is naming of test methods.
* Do not use Hungarian notation. ([Definition on Wikipedia](https://en.wikipedia.org/wiki/Hungarian_notation))
* Avoid using identifiers that conflict with keywords of widely used programming languages.

### Language 
Use US English language for naming identifiers. Use proper English ortography.

### Abbreviations & Acronyms
Abbreviations are dangerous because they can easily lead to confusion and can hide the real semantics of an identifier.

* Do not use abbreviations or contractions as parts of identifier names. For example, use `GetWindow` instead of `GetWin`. If you must use abbreviations, use Camel Case for abbreviations that consist of more than two characters, even if this contradicts the standard abbreviation of the word.   
* Where appropriate, use well-known acronyms to replace lengthy phrase names. You can use acronyms that are generally accepted in the computing field. I.e. XML, DNS, UI, IP and IO. Avoid all other abvreviations!
* When using Acronyms with more than two letters use Camel or Pascal case(even if this contradicts the standard Acronym). For Acronyms with one or two letters use Uppercase. E.g. 
  * `public string HtmlString` not `public string HTMLString`
  * `public void QueryDns` not `public void QueryDNS`
  * `public class IO` not `public class Io`

## Assemblies
[Names of assemblies and dlls](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-assemblies-and-dlls)

## Namespaces
The following template specifies the general rule for naming namespaces:

`Hsm.(<Product>|<Technology>)[.<Feature>][.<Subnamespace>]`

Following rules apply:
[Names of namespaces](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-namespaces)

Namespaces and solution structure must match. While not every solution folder must imply a separate sub-namespace it must not be that items belonging to the same namespace are distributed to different project folders.

### Classes, Structs
Use nouns or noun phrases for class names.
Avoid names and suffixes like Utils, Shared, Common, General. Rather search for descriptive names. 

### Interfaces
Prefix interface names with the letter I, to indicate that the type is an interface.

If an interface declares only one key method, such as `Draw()`, the interface name is formed as an adjective by adding the "...able" suffix. So, the interface name could be `IDrawable`.

For all other interface use either a descriptive noun (e.g. `IComponent`) or a descriptive noun-phrase (e.g. `ICustomAttributeProvider`). As with other type names, avoid abbreviations. 

Do ensure that the names differ only by the "I" prefix on the interface name when you are defining a class–interface pair where the class is a standard implementation of the interface.

### Enumerations
Enums are named in singular not in plural, i.e. `public enum Color` and NOT `public enum Colors`.

Do not suffix enums with `...Enum`.

## Projects
Avoid names and suffixes like Utils, Shared, Common, General, Library. These names usually have a bad smell and call for a restructuring of the solution.

### Test projects
#### Test project naming
Test projects are named like the project under test with following suffixes:
* `<ProjectUnderTest>.UnitTests` for Unit test projects
* `<ProjectUnderTest>.PerformanceTests` for performance tests (unit or integration)
* `<ProjectUnderTest>.IntegrationTests` for integration tests

#### Naming test classes
`<name of the tested class>Test`  -- mind singular here

#### Naming of test methods
`[the name of the tested method]_[expected input / tested state]_[expected behavior`]

Examples:
* `Sum_NegativeNumberAs1stParam_ExceptionThrown()`
* `Sum_SimpleValues_Calculated ()`
* `Sum_NegativeNumberAs2ndParam_ExceptionThrown`