
> [!IMPORTANT]
> **dough is SHADED inside Slimefun, not shipped as a standalone jar.** The source
> lives in the `dough-core` repo, but Slimefun consumes it as a Maven dependency
> (`com.github.drakescraft_labs:dough-core`) and relocates it when packaging to
> `com.github.drakescraft_labs.slimefun4.libraries.dough`. **There is no
> `dough.jar` in production.** Therefore, any change to `dough-core` requires:
> `mvn install` in dough-core -> **rebuild Slimefun** (and every plugin that
> shades it) -> upload those jars. Uploading dough on its own has no effect.

<div align="center">

  <img src="https://raw.githubusercontent.com/SlimefunNewHorizons/dough-core/main/banner.svg" alt="dough-core Banner" width="920" />

# ⚡ dough-core

**SLIMEFUN4 ADDON · DRAKES EDITION**

<p>
  <a href="https://github.com/SlimefunNewHorizons/dough-core"><img src="https://img.shields.io/badge/GitHub-dough-core-181717?style=for-the-badge&logo=github" alt="GitHub"/></a>
  <img src="https://img.shields.io/badge/Slimefun4-Drake_Edition-22C55E?style=for-the-badge&logo=curseforge&logoColor=white" alt="Slimefun4"/>
  <img src="https://img.shields.io/badge/Paper-1.21.11-38BDF8?style=for-the-badge&logo=minecraft&logoColor=white" alt="Paper 1.21.11"/>
  <img src="https://img.shields.io/badge/Java-21-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21"/>
</p>

</div>

> ### 🏰 Join the Official DrakesCraft Community!
> 
> * 🎮 **Server IP**: `play.drakescraft.net` *(Java 1.21.11 & Bedrock)*
> * 💬 **Official Discord**: [discord.gg/drakescraft](https://discord.gg/rv3vtXZTk7)
> * 🌐 **Web & Guide**: [drakescraft.net](https://drakescraft.net) — 🛒 **Store**: [tienda.drakescraft.net](https://tienda.drakescraft.net)
> 
> *Play with this addon and 80+ more optimized expansions live on our technical survival network!*

---

---

## 📖 Detailed Description

**dough-core** is a modular library of the **DrakesCraft Labs** ecosystem for **Paper / Purpur 1.21.11** Minecraft servers.

A Slimefun addon library maintained and optimized by DrakesCraft Labs for Paper 1.21.11.

All content, recipes and machinery are unlocked and researched directly from the **Slimefun Guide (`/sf guide`)** with no special commands.

---

## ⚙️ Main Features and Systems

* 🚀 **Optimized performance**: Fully prepared for Java 21 on Paper 1.21.11, with no Garbage Collector pauses or external telemetry.
* 🛡️ **Safety and integrity**: Atomic storage transactions and strict inventory protection.
* 🎮 **Full integration**: Compatible with Slimefun4-Drake, NetworksV6 logistics networks, heavy machinery and the global economy.

---

## Version compatibility

| Line | Branch | Artifact version | Minecraft | Java | Compile-time Paper API | Status |
|---|---|---|---|---|---|---|
| Production | `main` | 1.21.11 line | Paper/Purpur/Folia 1.21.11 | 21 | `1.21.11-R0.1-SNAPSHOT` | production |
| Universal 26.x | `port-26x` | `1.3.1-Universal-26.x-SNAPSHOT` | Paper/Purpur 26.2 (same codebase as production 1.21.11) | 21 bytecode; runs on 21+ | `1.21.11-R0.1-SNAPSHOT` (via the Slimefun core build) | test (verified on Paper/Purpur 26.2) |

**Minecraft versions older than 1.21.11 are not supported and not tested.**

| Parameter | Requirement |
|---|---|
| **Server** | Paper / Purpur / Folia **1.21.11** (26.2 on the Universal line) |
| **Java** | **Java 21** LTS |
| **Core** | [Slimefun4-Drake](https://github.com/SlimefunNewHorizons/Slimefun4-Drake) |
| **Side** | 100% server-side |

---

## 🌐 Universal 26.x line (branch `port-26x`)

* **Version:** `1.3.1-Universal-26.x-SNAPSHOT` (separate from the 1.21.11 version on `main`).
* **Upstream namespace restored:** back to `io.github.bakedlibs.dough` (commit `69e6dbf`), which fixes `CustomGameProfile` against the final Authlib of 26.x.
* **Publishing:** `mvn deploy` uploads the artifact to `https://maven.drakescraft.cl/` (`maven-repo` repo); `Slimefun4-Drake` (`port-26x`) consumes it from there. After publishing, rebuild Slimefun (dough is shaded).

---

## 📥 Installation

1. Download the `.jar` of the latest version from the Releases tab or Modrinth.
2. Place it in the server's `plugins/` folder next to `Slimefun4-Drake.jar`.
3. Start or restart the server.

---

<div align="center">

**Developed and maintained by [DrakesCraft Labs](https://github.com/SlimefunNewHorizons)**  
License **GPL-3.0-only** / **MIT**.

</div>

---

## Using maven.drakescraft.cl

Release and snapshot builds of this project are published at **https://maven.drakescraft.cl** (a static Maven repository served from GitHub Pages; sources in [SlimefunNewHorizons/maven-repo](https://github.com/SlimefunNewHorizons/maven-repo)). The full matrix lives in [`docs/COMPATIBILITY.md`](https://github.com/SlimefunNewHorizons/maven-repo/blob/main/docs/COMPATIBILITY.md).

> **Warning:** the 1.21.11 and 26.x lines are **not binary-interchangeable** (different Java release, Paper API, and Java packages). Pick one line per server/addon and recompile your addon against the matching line.

| Artifact (`com.github.drakescraft_labs`) | Version | Minecraft | Java | Source branch |
|---|---|---|---|---|
| `slimefun-core` | `11.0-Drake-1.21.11-SNAPSHOT` | 1.21.11 | 21 | `main` of Slimefun4-Drake |
| `slimefun-core` | `11.0-Universal-26.x-SNAPSHOT` | 26.2 | 25 | `port-26x` of Slimefun4-Drake |
| `dough-core` | `1.3.1-DRAKE-v11-SNAPSHOT` | 1.21.11 | 21 | `main` of dough-core |
| `dough-core` | `1.3.1-Universal-26.x-SNAPSHOT` | 26.2 | 25 | `port-26x` of dough-core |
| `SefiLib` | `0.3.0-Drake-1.21.11` | 1.21.11 | 21 | `main` of SefiLib |
| `SefiLib` | `0.3.1-Universal-26.x-SNAPSHOT` | 26.2 | 25 | `port-26x` of SefiLib |

### Maven

```xml
<repositories>
  <repository>
    <id>drakescraft-labs</id>
    <url>https://maven.drakescraft.cl/</url>
    <snapshots><enabled>true</enabled></snapshots>
  </repository>
</repositories>

<dependencies>
  <!-- 26.2 line (Java 25) -->
  <dependency>
    <groupId>com.github.drakescraft_labs</groupId>
    <artifactId>slimefun-core</artifactId>
    <version>11.0-Universal-26.x-SNAPSHOT</version>
    <scope>provided</scope>
  </dependency>
  <dependency>
    <groupId>com.github.drakescraft_labs</groupId>
    <artifactId>dough-core</artifactId>
    <version>1.3.1-Universal-26.x-SNAPSHOT</version>
  </dependency>
  <dependency>
    <groupId>com.github.drakescraft_labs</groupId>
    <artifactId>SefiLib</artifactId>
    <version>0.3.1-Universal-26.x-SNAPSHOT</version>
  </dependency>
</dependencies>
```

For the **1.21.11 line (Java 21)** use instead `slimefun-core:11.0-Drake-1.21.11-SNAPSHOT`, `dough-core:1.3.1-DRAKE-v11-SNAPSHOT` and `SefiLib:0.3.0-Drake-1.21.11`.

### Gradle (Kotlin DSL)

```kotlin
repositories {
    maven("https://maven.drakescraft.cl/")
}

dependencies {
    // 26.2 line (Java 25)
    compileOnly("com.github.drakescraft_labs:slimefun-core:11.0-Universal-26.x-SNAPSHOT")
    implementation("com.github.drakescraft_labs:dough-core:1.3.1-Universal-26.x-SNAPSHOT")
    implementation("com.github.drakescraft_labs:SefiLib:0.3.1-Universal-26.x-SNAPSHOT")

    // 1.21.11 line (Java 21) -- do not mix with the lines above
    // compileOnly("com.github.drakescraft_labs:slimefun-core:11.0-Drake-1.21.11-SNAPSHOT")
    // implementation("com.github.drakescraft_labs:dough-core:1.3.1-DRAKE-v11-SNAPSHOT")
    // implementation("com.github.drakescraft_labs:SefiLib:0.3.0-Drake-1.21.11")
}
```

### Fallback: GitHub Packages

If `maven.drakescraft.cl` is unreachable, the same builds are mirrored in GitHub Packages under `SlimefunNewHorizons` (repositories `Slimefun4-Drake`, `dough-core`, `SefiLib`). Differences from the main repository:

- GitHub Packages **requires authentication even for public packages**: use a personal access token (classic) with at least `read:packages`. Never commit it; read it from an environment variable.
- GitHub Packages rejects uppercase artifact ids, so `SefiLib` is published there as **`sefilib`** (same version strings).
- The mirror carries the jars only (generated minimal POMs for the 1.21.11 line); transitive dependencies still resolve from `https://maven.drakescraft.cl/`, so keep both repositories declared.

`~/.m2/settings.xml` (placeholders only):

```xml
<settings>
  <servers>
    <server>
      <id>github-slimefun</id>
      <username>YOUR_GITHUB_USERNAME</username>
      <password>${env.GITHUB_TOKEN}</password> <!-- token with read:packages -->
    </server>
  </servers>
</settings>
```

and in your `pom.xml` (one `<repository>` per mirrored repo you need; the `id` must match the `<server>` id):

```xml
<repository>
  <id>github-slimefun</id>
  <url>https://maven.pkg.github.com/SlimefunNewHorizons/dough-core</url>
  <snapshots><enabled>true</enabled></snapshots>
</repository>
```

Package pages: `slimefun-core` and `drakes-slimefun-labs` (parent POM) under [Slimefun4-Drake](https://github.com/SlimefunNewHorizons/Slimefun4-Drake/packages), `dough-core` under [dough-core](https://github.com/SlimefunNewHorizons/dough-core/packages), `sefilib` under [SefiLib](https://github.com/SlimefunNewHorizons/SefiLib/packages).

## 📄 License & Upstream Attribution

This project is a sovereign fork maintained by [**JackStar6677-1**](https://github.com/JackStar6677-1) under [**DrakesCraft Labs**](https://github.com/SlimefunNewHorizons).

- **Original Project:** Created by the upstream authors and the open-source community.
- **DrakesCraft Optimizations:** Modernized for Paper/Purpur 1.21.11+, Java 21, high concurrency, asynchronous safety, and exploit/duplication prevention.
- **License:** Distributed under the original **GNU General Public License v3.0 (GPLv3)** (or original upstream license). See the [LICENSE](LICENSE) file for complete terms.
