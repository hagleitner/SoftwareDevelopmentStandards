---
layout: default
title: Type design guidelines
parent: CSharp
nav_order: 30
---

# Type design guidelines
## Choosing between class and struct
As a rule of thumb, the majority of types in a framework should be classes. There are, however, some situations in which the characteristics of a value type makes it more appropriate to use structs.

Consider defining a struct instead of a class if instances of the type are small and commonly short-lived or are commonly embedded in other objects.

Avoid defining a struct unless the type has _all_ of the following characteristics:

* It logically represents a single value, similar to primitive types (int, double, etc.).
* It has an instance size under 16 bytes.
* It is immutable.
* It will not have to be boxed frequently.

