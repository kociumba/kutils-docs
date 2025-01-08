---
icon: wrench
---

# Built-ins

#### Built-in Functions Available in kutils Lua Modules

Kutils provides a few built in functions that are available at runtime from Lua. These are some functions the are necessary for being able to do anything in the lua script, like `requireJVM` or just utility to make life easier, like `registerHudRenderer`. These are the currently available built-ins in the kutils runtime:

| Function              | Description                                                                            |
| --------------------- | -------------------------------------------------------------------------------------- |
| `requireJVM`          | Imports Java and Kotlin classes into the Lua script.                                   |
| `createLogger`        | Initializes a Minecraft logger with a custom prefix.                                   |
| `registerHudRenderer` | Registers a HUD render callback to draw custom UI.                                     |
| `runOnMain`           | Executes code on the main Minecraft thread.                                            |
| `isEnabled`           | Returns true if the current script is enabled by the user.                             |
| `onDisable`           | Takes in a function that will be called as cleanup when the user disables this module. |

*   #### **`requireJVM`**

    Imports Java and Kotlin classes:

    ```lua
    -- import the minecraft client class
    MinecraftClient = requireJVM("net.minecraft.client.MinecraftClient")
    -- import the jvm Thread class for threading management
    Thread = requireJVM("java.lang.Thread")
    ```
*   #### **`createLogger`**

    Initializes a Minecraft logger with a custom prefix:

    ```lua
    -- crates a logger with the supplied prefix
    log = createLogger("built-in showcase")
    -- the retuned logger implements 4 logging levels
    log.info("This is typical info")
    log.warn("Something shouldn't have happened")
    log.error("We messed up big time")
    log.debug("Only visible in the seperate debug.log")
    ```
*   #### **`registerHudRenderer`**

    Registers a HUD render callback to draw anything to the HUD, more info on how to draw UI in Minecraft [here](https://docs.fabricmc.net/develop/rendering/basic-concepts):

    ```lua
    local function renderHud(drawContext, tickDelta)
        -- Draw like you would in a normal mod
    end
    registerHudRenderer(renderHud) -- register the rendering callback
    ```
*   #### **`runOnMain`**

    Executes the provided function on the main Minecraft thread, which is required for rendering. If you are going to do any threading, this will be immensely useful:

    ```lua
    local function taskForTheMainThread()
        -- Any code really 🤷
    end
    runOnMain(taskForTheMainThread)
    ```
* #### For `isEnabled` and `onDisable` look in [interacting-with-java-and-kotlin.md](interacting-with-java-and-kotlin.md "mention"), for an overview.
