---
title: Java Installation Guide
categories: [Installation]
tags: [guide, Java]
---

### What version of Java should I use?

We recommend you use Java 8. Java 8 is LTS (long-term support), which means it's every bit as secure as later versions. If you use version 17 or higher, addons will not work and you might encounter other issues.

### Wait, does that mean everything else will also be stuck with Java 8?

No, you can install Java 8 without making it your main Java install and launchers will generally let you choose per modpack which Java to use.

### Where do I get Java 8? Do I need an Oracle account?

No, in fact we recommend [Adoptium](https://adoptium.net/), which is open-source, free and requires no account. You want to go to [other platforms and versions](https://adoptium.net/temurin/releases/) and then select:
* Operating System: your OS, probably Windows
* Architecture: x64
* Package Type: JRE
* Version: 8 - LTS

![A picture of the settings]({% link /posts/java-installation/adoptium-settings.png %})

If you are on Windows, you want the MSI installer, not the zip file, unless you know what you're doing.
