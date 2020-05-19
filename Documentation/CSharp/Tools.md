# Tools
Where possible we enforce our coding guidelines with software tools. These tools give the developers immediate feedback on the conformity of written code with the coding guidelines and provide Hagleitner a way to assess the quality of code in an automated way (e.g. in a build pipeline).

## Nuget packages
We use nuget packages to install some common tool configuration helping us to stick to the coding guidelines. For all newly created C# projects the installation of these packages is mandatory.

### Hagleitner.CSharpCodingGuidelines

This package installs following
* StyleCop.Analyzers
* FxCop Analyzers
* .editorconfig to that configures Analyzers 
* User dictionary

## Visual Studio Analyzers
[StyleCop Analyzers](https://github.com/DotNetAnalyzers/StyleCopAnalyzers)
[FxCop Analyzers](https://docs.microsoft.com/en-us/visualstudio/code-quality/install-fxcop-analyzers?view=vs-2019)

## Code coverage
**
## Visual Studio Spell Checker
Visual Studio Spell Checker is a Visual Studio editior extension that allows us to check the spelling of comments, strings and plain text as we type. It provides a user dictionary where new entries can easily be added by using 'Quick Actions and Refactorings...' and selecting 'Add to Dictionary'. The extension also supports configuration such as 'Detect doubled words' and 'Ignore words in mixed/camel case' by opening the 'VsSpellChecker.vsspell' file.
It can be installed from within Visual Studio from the Visual Studio Marketplace. Select the online marketplace and search for "Visual Studio Spell Checker". Once found, you can download and install the extension.