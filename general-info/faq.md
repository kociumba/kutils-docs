---
icon: comments-question-check
---

# FAQ

These are general questions someone might have about kutils, these would land on the github README, but the wiki exists, so they ended up here.

#### <mark style="background-color:red;">Q:</mark> Why is everything from kutils stored in the `config` folder?

<mark style="background-color:blue;">A:</mark> Everything including the lua modules and notes is stored in the `config` folder, for ease of migration, when you change the instance of Minecraft you play on, or even the version it's easier to copy over just the `config` folder, instead of some cherry picked files and folders in different places. Also it adds transparency, since you can see every file kutils has and will ever interact with in there.

#### <mark style="background-color:red;">Q:</mark> Is kutils cross platform?

<mark style="background-color:blue;">A:</mark> kutils should be cross platform, but is only tested on windows right now, if you don't know why kutils could have cross platform issues you should check out the UI library kutils uses: [https://github.com/ocornut/imgui](https://github.com/ocornut/imgui). ImGui is written in C++  which inherently isn't cross platform in the same way java or kotlin is, so kutils distributes with ImGui compiled for windows, linux and macos to get around this issue, which unfortunately adds around 7mb to the release jar.



If you have a question you'd like to see answered here,  please ask it in the kutils thread: [https://hypixel.net/threads/kutils](https://hypixel.net/threads/kutils-client-side-qol-features-and-tweaks-from-older-mods-but-for-1-21-with-very-unique-skyblock-features.5817712/), or file and issue on one of these github repos:

* the docs repo(this site) - [https://github.com/kociumba/kutils-docs](https://github.com/kociumba/kutils-docs)
* the kutils repo - [https://github.com/kociumba/kutils](https://github.com/kociumba/kutils)
