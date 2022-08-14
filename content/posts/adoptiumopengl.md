---
title: "Getting Minecraft to run on a legacy Intel iGPU with Adoptium/Temurin JRE"
date: 2022-07-04T16:44:44+02:00
draft: false
readingTime: true
tags: ["minecraft", "tweak"]
author: Odyssey346
---
## So... why?
I was checking out my ThinkPad, and I was trying to run Minecraft on it. To my surprise, apparently it did not support OpenGL! But, it does support OpenGL... what's going on?
## Let's blame Intel
Intel's graphic drivers were, obviously, legacy. This is a laptop from 2012. The drivers weren't intended to run on Windows 10, but it does... here's where it messes up though: Windows 10 and newer change the NT kernel version from 6 to 10. Huge step, and this causes some applications to not want to load OpenGL drivers.. here's the fix!
## Compatability Assistant is cool
What I did was trick Temurin/Adoptium that it's running on Windows 8.1, and then I load the OpenGL driver from Intel. Instead of you needing do to this all yourself, I've put it all in a GitHub repository that explains everything further [here](https://github.com/Odyssey346/AdoptiumOpenGLonLegacyIntel).
## Does it work?
![Yes](https://github.com/Odyssey346/AdoptiumOpenGLonLegacyIntel/raw/master/assets/minecraft1165.png)
## What versions can you run using this?
Anything less than or equal to 1.16.5. Newer versions of Minecraft require a version of OpenGL the chip does not support.
<script src="https://giscus.app/client.js"
        data-repo="Odyssey346/Odyssey346.github.io"
        data-repo-id="R_kgDOHZ_ETQ"
        data-category="General"
        data-category-id="DIC_kwDOHZ_ETc4CQ0mr"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="dark_dimmed"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>