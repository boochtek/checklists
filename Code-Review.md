NOTE: The rules can be broken, but you have to give a good reason, and convince your pair.

- [ ] The story makes sense, and it's clear how it can be tested.
- [ ] The specs show that the right problem is being solved, as per the story.
- [ ] The specs are easily readable/understandable.
- [ ] The specs (new and old) are passing locally.
    * For projects with slow specs/tests:
        * Find a useful subset that can be run quickly; tag them; run those every time
        * Make sure the *new* specs are passing locally.
- [ ] The specs are passing on the CI server.
- [ ] Any new behavior has been manually tested (locally).
- [ ] All publicly-exposed changes to code have associated specs.
- [ ] Security concerns have been considered and addressed.
- [ ] The code is something that is worth maintaining.
- [ ] The code has a neutral or positive impact on Code Climate.
    - [ ] Any negative impact has been justified (preferably in a commit message).
- [ ] The code that has been added or changed is well-factored.
- [ ] Rake tasks of more than a few lines have been extracted into a class, with specs.
- [ ] There are no glaring errors, omissions, or poor-quality code.
    - [ ] Classes and method names make their intentions clear.
    - [ ] There are no spelling errors.
    - [ ] There are no magic numbers in the code.
    - [ ] Exceptions are not being caught and ignored.
    - [ ] Comments cannot be easily replaced by coming up with better names or better code.
    - [ ] Methods are private if they’re used only from within the class.
    - [ ] Methods are protected only if they’re used only by subclasses.
        * Nobody's ever seen this in the wild in Ruby.
    - [ ] Any `if` statements with no `else` clause don’t need to handle the `else` case.
    - [ ] The impact of `nil` values have been considered.
    - [ ] Floats are used only where appropriate.
- [ ] The code conforms to the team style guide.
    - [ ] The code passes RuboCop.
    - [ ] The code passes ESLint.
    - [ ] There are no issues with any non-automated style guide items.

