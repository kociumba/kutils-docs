---
icon: link
---

# Interacting with Java and Kotlin

#### How To Interact With Java and Kotlin classes in Lua ?

It's pretty simple, first you import and load the class with `requireJVM`:

```lua
someClass = requireJVM("dev.gabagool.important.SomeClass")
```

After importing our class we can access fields in it using `.` and methods or functions with `:`

```lua
-- we get the value of the variable in a class
local theFunny = someClass.theFunnyVariable
-- we invoke a method or a function and retrive the result
local funnyMachineResult = someClass:funnyMachine()
```

Additionally you should always use the `isEnabled()` and `onDisable()`lua built-ins, they allow you to properly manage cleanup when the user turns off your script, technically you can ignore it, but that results in your script not being able to be turned off by the user 🤷

```lua
local updateThread = Thread(function()
    -- only run the job on the thread if the lua module is enabled
    while isEnabled() do
        counter = counter + 1
        Thread:sleep(1000)
    end
end)
updateThread:start()
```

```lua
onDisable(function()
    counter = 0
    -- if we check in the thread like above, we should close the thread like this
    -- but if the thread has no checks you can close it in the onDisable hook
    updateThread:interrupt()
end)
```
