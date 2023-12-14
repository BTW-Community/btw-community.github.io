---
title: MultiMC/Prism Installation Guide
categories: [Installation]
tags: [guide, MultiMC]
---

Installation on [MultiMC](https://multimc.org/) or forks like [Prism Launcher](https://prismlauncher.org/) is really easy.

## Import the instance

Download the [**latest MultiMC instance**]({% link _tabs/download.md %}) from our download page.

Next, in your launcher, **add a new instance** and [**import the zip file**](https://github.com/MultiMC/Launcher/wiki/Import-Instance) we just downloaded.

![The 'Import from Zip' screen]({% link /posts/installation-multimc/import-instance.png %})

## Optional: change your Java version

First of all, [download the right version of Java]({% post_url 2023-12-14-java-installation %}).

Go to **Edit Instance -> Settings -> Java** and select the **Java Installation** box.

Press the **Auto-detect** button, refresh, and select the version of Java you want.

![The instance's Java settings]({% link /posts/installation-multimc/java-settings.png %})

If your installation doesn't appear on the list, try refreshing. If that fails, you'll need to locate the Java executable yourself, within the root Java directory. This is `./bin/java` on Unix systems, and `.\bin\javaw.exe` on Windows.
