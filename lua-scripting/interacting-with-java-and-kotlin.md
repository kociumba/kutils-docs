---
icon: link
---

# Interacting with Java and Kotlin

#### How To Interact With Java and Kotlin classes in Lua ?

It's pretty simple, first you import and load the class with `requireJVM`:

```lua
someClass = requireJVM("dev.gabagool.important.SomeClass")
```

After importing our class we can access variables in it using `.` and methods or functions with `:`

```lua
-- we get the value of the variable in a class
local theFunny = someClass.theFunnyVariable
-- we invoke a method or a function and retrive the result
local funnyMachineOutput = someClass:funnyMachine()
```

This is literally it, there is nothing more to this, go and code something :clap:
