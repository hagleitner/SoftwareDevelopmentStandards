---
layout: default
title: Code documentation
parent: CSharp
nav_order: 50
---

# Code documentation

Note: We intentionally differentiate between [code comments](CodeComments.md) and code documentation.

We document our code to make it more usable to the outside world and to keep it maintenable. We keep our code documentation as short a possible but as long as needed. 

## XML documentation comments
C# XML documentation can be added to any user-defined type or member. XML comments are different from regular comments as they can be processed by a compiler. XML documentation feeds IntelliSense and therefore helps developers with quick information on types and members. XML documentation can be processed by tools like GhostDoc or Docfx to produce documentation like that found on MSDN.

XML documentation is therefore the perfect way to communicate important information about a type or member.

Documentation on XML comments can be found at: https://docs.microsoft.com/en-us/dotnet/csharp/codedoc

### Where and how to use XML documentation comments
We comment all publicly visible types and their members. Documentation text should be written using complete sentences ending with full stops.

For types we document:
* `<summary>`: Brief description of the type

For method members we document:
* `<summary>`: Brief description of the intent of the method
* `<returns>`: Brief description what the method returns
* `<param>`: Brief description of every parameter
* `<typeparam>`: For generic types the type prarameter shall be described
* `<exception>`: Type of exception and brief description when it is raised (if any). Exceptions are part of the methods interface to the outside world.

### Use of other XML documentation comment tags
Using special XML tags within the XML documentation can save a lot of time and helps us to keep the documentation consistent.

* Never write the name of a type in a comment use `<seealso cref=""/>` instead
* Never write the name of parameters in a comment use `<paramref name="a"/>` instead 	
* Never write the name of type parameter in a comment use `<typeparamref name="T">` instead 	

### Using `<inheritdoc>`
`<inheritdoc>` can be used to inherit documentation from base classes, interfaces. Use `<inheritdoc>` instead of copy-pasting XML documentation.

## Other documentation
Sometimes the XML documentation comments are not enough to document our code. When more voluminous textual documentation, diagrams etc. are needed, we need different ways for documenting our code.

### Markdown documents
When necessary markdown documents should be used for more extensive code documentation. The markdown files shall be part of the solution.