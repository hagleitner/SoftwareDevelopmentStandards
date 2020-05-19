# Code comments

Note: We intentionally differentiate between [code documentation](Documentation) and code comments

> Commenting should be minimal. However, minimalism is not the same as nihilism. Code should be made self-documenting not so much by the omission of comments but by the adoption of practices that make intent clear and code brief. (Prefer code to comments, Kevlin Henney)

Following rules apply to using code comments:
* We do not use copyright and other legal header-comments
* Generally we prefer code do comments
* Comments that describe what a piece of complex code does are often a hint that we need a better structure of code.
* Commented-out code is bad. Remove commented-out code before committing. If you want to keep the code idea, write an issue in your issue management tool. 
* Comments on who changed the code at what time are useless, this information is provided by the repository

## TODO comments
* TODO comments are not allowed in  code in the _Master_ or the _Development_ branch and also not in any _Release_  branch. The same goes for `throw new NotImplementedException()`
* Within _Feature_ branches and _Hotfix_ branches TODO comments are allowed
* When sketching out code use `throw new NotImplementedException()` instedad of using TODO comments wherever possible.
* TODO comments in code reviews: Code reviews are conducted on separate branches. Todo comments can mark the places where additional work is needed. 
When merging the review branch back to a feature branch all those Todo comments shall be resolved/removed. Bigger issues shall be recorded in the issue management instead of TODO comments.
* All other TODO comments are usually candidates for issues in your issue management tool.
 
 