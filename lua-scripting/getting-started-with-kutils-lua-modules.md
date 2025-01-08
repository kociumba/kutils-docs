---
icon: circle-info
---

# Getting started with kutils lua modules

To get started with writing kutils lua modules, you can use the basic in game editor, or a separate editor like vscode with a lua-lsp plugin. To learn how kutils lua modules work just follow these docs, in their written order.

***

If you have any standard lua lsp pluign for vscode/intelij/other editors, kutils provides definitions for the built-in runtime functions covered in more detail here: [built-ins.md](built-ins.md "mention").

The definitions are provided using `.luarc.json` and `kutils.lua` in this file tree:

{% code fullWidth="false" %}
```
config/kutils/lua/
├── types/
│   └── kutils.lua
├── .luarc.json
├── your scripts
└── ...
```
{% endcode %}

This means that is you open your editor of choice on the `$minecraft_dir/config/kutils/lua/` path, your lua plugin should automatically detect the built in kutils functions.

***

kutils lua modules are stored as `.lua` files in `config/kutils/lua/` any files in there can be loaded and executed in game in the Lua Modules Editor, by default bound to `,`&#x20;
