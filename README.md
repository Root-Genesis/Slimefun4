# Slimefun 4 (English fork)

An English translation of the [SlimefunGuguProject](https://github.com/SlimefunGuguProject/Slimefun4) fork of [Slimefun 4](https://github.com/Slimefun/Slimefun4), maintained by [@SaanPrasanna](https://github.com/SaanPrasanna).

[![Latest release](https://img.shields.io/github/v/release/SaanPrasanna/Slimefun4)](https://github.com/SaanPrasanna/Slimefun4/releases/latest)
[![Issues](https://img.shields.io/github/issues/SaanPrasanna/Slimefun4.svg?style=popout)](https://github.com/SaanPrasanna/Slimefun4/issues)
[![Downloads](https://img.shields.io/github/downloads/SaanPrasanna/Slimefun4/total)](https://github.com/SaanPrasanna/Slimefun4/releases)
[![License: GPL v3](https://img.shields.io/badge/license-GPLv3-blue.svg)](LICENSE)

**[Download the latest release](https://github.com/SaanPrasanna/Slimefun4/releases/latest)** · [Changelog](CHANGELOG.md) · [Report a bug](https://github.com/SaanPrasanna/Slimefun4/issues) · [Original Chinese version](https://github.com/SlimefunGuguProject/Slimefun4)

> [!IMPORTANT]
> This is an **unofficial, modified build**. It isn't made, endorsed or supported by the Slimefun team or by SlimefunGuguProject.
> Please report problems with this build **here**, not to either upstream project. If a bug turns out to come from upstream, it will be passed on to them.

## About this fork

SlimefunGuguProject maintains a Chinese fork of Slimefun 4 with its own features and fixes, such as database storage and newer Minecraft support. This fork keeps all of that and translates it into English:

- Messages, menus, item lore and console output are in English, and English is the default language.
- New upstream updates are synced regularly and translated before each release. See the [changelog](CHANGELOG.md).
- Game behaviour isn't changed on purpose. Fixes made here are listed in the changelog.

Download [SlimeGlue](https://github.com/Xzavier0722/SlimeGlue/) for compatibility between Slimefun and protection plugins.

## What is Slimefun?

Slimefun is a plugin that aims to provide a modding-like experience. It offers everything you can imagine, from jetpacks to magic altars!

Slimefun lets every player decide whether to develop in magic or technology.
From wands to nuclear reactors, it has it all.
There are also magic altars, energy networks, and even item transportation systems.

The project started in 2013 and is still evolving today.
It has grown from a small independent plugin into a community with thousands of participants and hundreds of contributors.
Slimefun adds more than **500 new items and crafting recipes**
([learn about the history of Slimefun](https://github.com/Slimefun/Slimefun4/wiki/Slimefun-in-a-nutshell)).

Slimefun also has a wide variety of addons. Check out the [Addon List](https://github.com/Slimefun/Slimefun4/wiki/Addons) to find the ones you want.

## :floppy_disk: Download and install

Download the jar from the [Releases page](https://github.com/SaanPrasanna/Slimefun4/releases/latest) and put it in your server's `plugins/` folder.
(See also: [How to install Slimefun](https://github.com/Slimefun/Slimefun4/wiki/Installing-Slimefun))

| | This English fork |
|---|---|
| **Server software** | Paper, or a fork of Paper such as Purpur or Leaves (recommended). CraftBukkit isn't supported. |
| **Minecraft version** | 1.18.x – 26.3.x |
| **Java version** | Java 21 or newer |
| **Updates** | Manual: download new versions from the Releases page. Each release lists its changes in the [changelog](CHANGELOG.md). |

Builds from this fork **don't update themselves**. The plugin's built-in updater only downloads the Chinese upstream builds, so it is switched off for these builds. That way your server never replaces the English jar with a Chinese one.

**Before updating, back up `plugins/Slimefun/`** (and your MySQL/PostgreSQL database, if you use one). Some updates convert stored data.

Hybrid servers that run plugins and mods together (Arclight, CatServer and similar) aren't supported.

## :computer: Building from source

You need [Git](https://git-scm.com/) and Java 21.

```bash
git clone https://github.com/SaanPrasanna/Slimefun4.git --depth=1
cd Slimefun4
```

- On Windows: `.\gradlew.bat build`
- On Linux and macOS: `./gradlew build`

The plugin jar is written to `build/libs/`.

## :jigsaw: Developing addons

This fork only changes text and fixes bugs. The API is the same as upstream's. Build your addon against the upstream SlimefunGuguProject artifact, and it will work with both the Chinese and the English builds.

<details>
<summary>How to add Slimefun 4 as a dependency (upstream artifacts)</summary>

Repository, Maven:

```xml
<!-- Releases -->
<repository>
    <id>gugu-maven-repo</id>
    <url>https://maven.norain.city/releases</url>
</repository>

<!-- Development builds (Slimefun Insider / dev branch) -->
<repository>
    <id>gugu-maven-repo-snapshots</id>
    <url>https://maven.norain.city/snapshots</url>
    <snapshots>
        <enabled>true</enabled>
    </snapshots>
</repository>
```

Repository, Gradle (`build.gradle.kts`):

```kotlin
repositories {
    maven { url = uri("https://maven.norain.city/releases") }
    // Development builds:
    maven { url = uri("https://maven.norain.city/snapshots") }
}
```

Dependency, Maven:

```xml
<dependency>
    <groupId>com.github.SlimefunGuguProject</groupId>
    <artifactId>Slimefun4</artifactId>
    <version>DEV-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

Dependency, Gradle:

```kotlin
dependencies {
    compileOnly("com.github.SlimefunGuguProject:Slimefun4:DEV-SNAPSHOT")
}
```

These repositories and artifacts are run by SlimefunGuguProject, not by this fork.

</details>

## :framed_picture: Screenshots

Screenshots from the official [Slimefun Wiki](https://github.com/Slimefun/Wiki), taken by members of the Slimefun community:

| Reactors and Energy | Amazing Automation Factory | Magic Laboratory |
| :-------------------------------------------: | :--------------------------------------: | :----------------------------------------: |
| ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase1.png) | ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase6.png) | ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase5.png) |
| *Screenshot by HamtaBot#0001* | *Screenshot by Piͭxͪeͤl (mnb)#5049* | *Screenshot by Kilaruna#4981* |
| ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase4.png) | ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase3.png) | ![](https://raw.githubusercontent.com/Slimefun/Slimefun-Wiki/master/images/showcase2.png) |
| *Screenshot by GalaxyKat11#3816* | *Screenshot by TamThan#7987* | *Screenshot by Kilaruna#4981* |

## :open_book: Wiki and help

- **This fork:** [Issues](https://github.com/SaanPrasanna/Slimefun4/issues) for bugs, translation mistakes and questions about this build.
- **Official Slimefun Wiki:** https://github.com/Slimefun/Slimefun4/wiki ([FAQ](https://github.com/Slimefun/Slimefun4/wiki/FAQ), [Common Issues](https://github.com/Slimefun/Slimefun4/wiki/Common-Issues), [Addon Developer Guide](https://github.com/Slimefun/Slimefun4/wiki/Developer-Guide)). Most of it applies here too. Features that only exist in the Chinese fork, such as database storage, aren't covered.
- **Chinese Wiki** (maintained by [@ybw0014](https://github.com/ybw0014)): https://slimefun-wiki.guizhanss.cn/. It covers the Chinese fork's own features.

Community spaces run by others:

- The official [Slimefun Discord](https://discord.gg/slimefun) is for the original Slimefun. Please don't ask there for help with this build, and follow its [rules](https://github.com/Slimefun/Slimefun4/wiki/Discord-Rules).
- The SlimefunGugu community (Chinese): QQ group 807302496, addon QQ group 205679802, and [KOOK](https://kook.top/oqZwh8).

## :handshake: Contributing

Pull requests are welcome, especially translation fixes. See [CONTRIBUTING.md](CONTRIBUTING.md).
Code changes that aren't about translation are best sent to [SlimefunGuguProject](https://github.com/SlimefunGuguProject/Slimefun4) first, so every user benefits. They reach this fork with the next sync.

By contributing, you agree that your contribution is licensed under the GNU GPLv3, the same as the rest of the project.

## :shield: Privacy and network use

The plugin connects to these services. It doesn't collect personal information such as player names, IP addresses or chat.

<details>
<summary>bStats (anonymous usage statistics): on by default</summary>

On first start, Slimefun downloads its metrics module from [Slimefun/MetricsModule2](https://github.com/Slimefun/MetricsModule2) on GitHub and runs it. The module sends anonymous statistics about the server and the plugin to [bStats](https://bstats.org/plugin/bukkit/Slimefun/4574), where they appear on the original Slimefun project's public statistics page.

To turn it off, set `enabled: false` in `plugins/bStats/config.yml`. See the [bStats privacy policy](https://bstats.org/privacy-policy).

</details>

<details>
<summary>GitHub and Minecraft skins (for the in-game credits)</summary>

To show contributors in the Slimefun Guide, the plugin reads public data from the [GitHub API](https://api.github.com/): contributor usernames and commit counts, open issues, pull requests, stars, forks and the date of the last commit. It reads these from `SlimefunGuguProject/Slimefun4`, `Slimefun/Wiki` and `Slimefun/Resourcepack`. It loads the contributors' Minecraft skins from Mojang's servers. Nothing about your server is sent.

</details>

<details>
<summary>Updates and analytics: off in these builds</summary>

- **Auto-update:** The built-in updater only works for the official Chinese builds, so it does nothing in this fork, whatever `options.auto-update` says in `config.yml`.
- **Slimefun analytics** (`analytics.slimefun.dev`): only sent by official Slimefun builds, never by this one.

</details>

## :scroll: License and credits

### License

Slimefun 4, the SlimefunGuguProject fork and this English fork are free software, licensed under the **[GNU General Public License v3.0](LICENSE)**. You may use, share and modify them. If you distribute a modified version, it has to stay under the GPLv3, keep these copyright notices, and come with its source code.

**This is a modified version.** It is based on [SlimefunGuguProject/Slimefun4](https://github.com/SlimefunGuguProject/Slimefun4), which is itself based on [Slimefun/Slimefun4](https://github.com/Slimefun/Slimefun4). Since November 2025 it has been translated into English and changed as described in the [changelog](CHANGELOG.md). The git history records every change. The source code for every release is available from its tag on the [Releases page](https://github.com/SaanPrasanna/Slimefun4/releases).

The [`NOTICE`](NOTICE) file holds this attribution and is packaged inside every plugin jar, next to the license text (`META-INF/NOTICE-Slimefun.txt` and `META-INF/LICENSE-Slimefun.txt`). If you redistribute this plugin or build on it, keep both files and the credits below.

```
Slimefun 4
Copyright (C) 2013-2026 TheBusyBiscuit and the Slimefun contributors
Copyright (C) SlimefunGuguProject and its contributors (Chinese fork)
Copyright (C) 2025-2026 Sandun Prasanna (English translation and modifications)

This program is free software: you can redistribute it and/or modify it under the
terms of the GNU General Public License as published by the Free Software Foundation,
either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.
```

### Credits

This fork exists thanks to the people who built Slimefun:

- **Slimefun:** created by [TheBusyBiscuit](https://github.com/TheBusyBiscuit) in 2013 and maintained by the [Slimefun team](https://github.com/Slimefun), including [WalshyDev](https://github.com/WalshyDev) and [LinoxGH](https://github.com/LinoxGH), with [hundreds of contributors](https://github.com/Slimefun/Slimefun4/graphs/contributors).
- **SlimefunGuguProject (Chinese fork):** maintained by [StarWishsama](https://github.com/StarWishsama), with [Xzavier0722](https://github.com/Xzavier0722) (database storage and SlimeGlue), [ybw0014](https://github.com/ybw0014) (updater, GuizhanLib and the Chinese Wiki) and [all their contributors](https://github.com/SlimefunGuguProject/Slimefun4/graphs/contributors).
- **English translation fork:** [Sandun Prasanna (@SaanPrasanna)](https://github.com/SaanPrasanna).
- **Translations into other languages:** the Slimefun translators listed in [`translators.json`](src/main/resources/languages/translators.json).
- **Screenshots:** the community members credited under each image above.

The Slimefun Guide in game also lists upstream contributors under **Settings & Info → Slimefun4 Contributors**.

### Third-party libraries

The plugin jar bundles these libraries, each under its own license:

| Library | License |
|---|---|
| [dough](https://github.com/Slimefun/dough) | MIT |
| [Unirest for Java](https://github.com/Kong/unirest-java) | MIT |
| [HikariCP](https://github.com/brettwooldridge/HikariCP) | Apache-2.0 |
| [PostgreSQL JDBC Driver](https://github.com/pgjdbc/pgjdbc) | BSD-2-Clause |
| [Apache Commons Lang](https://github.com/apache/commons-lang) | Apache-2.0 |
| [GuizhanLib](https://github.com/ybw0014/guizhanlib) | GPL-3.0 |
| [SlimefunCompLib](https://github.com/Xzavier0722/SlimefunCompLib) | No license file published. Bundled as in the upstream build, by an upstream contributor. |

### Trademarks

"Slimefun" refers to the original project by TheBusyBiscuit and the Slimefun team. This fork uses the name only to say what it is based on, and doesn't claim to be the official version.
Minecraft is a trademark of Mojang Studios / Microsoft. This project isn't affiliated with or endorsed by Mojang Studios or Microsoft.
This fork is free. It isn't connected to the paid subscription offered by SlimefunGuguProject for its Chinese builds.

### No warranty

This plugin is provided "as is", without warranty of any kind, as described in sections 15 and 16 of the GPLv3. Back up your server before installing or updating.
