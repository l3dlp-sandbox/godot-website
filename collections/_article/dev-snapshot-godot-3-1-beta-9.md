---
title: "Dev snapshot: Godot 3.1 beta 9"
excerpt: "The previous beta had some GLES2/Android regressions which, along with several other issues, has been fixed in Beta 9. Please go forth and test! Assuming no new regressions are found we are likely going to move to *release candidate* state soon."
categories: ["pre-release"]
author: HP van Braam
image: /storage/app/uploads/public/5c7/818/df2/5c7818df2369c923755927.jpg
date: 2019-02-28 00:00:00
---

As bugfixing is going at a steady pace towards Godot 3.1 stable, we plan to release beta builds frequently to have broad testing on the latest fixes and spot any regression. So we're now publishing Godot 3.1 **beta 9** with close to 50 commits made since beta 8 a few days ago.

See the changes between [3.1 beta 8 and 3.1 beta 9](https://github.com/godotengine/godot/compare/a32b26dfa26f2a039bf9c84b90d10666bcf785c9...a5370b1b1bed3744941c90b4a05d4516aabd4c67). This beta is built from commit [a5370b1](https://github.com/godotengine/godot/commit/a5370b1b1bed3744941c90b4a05d4516aabd4c67).

The ETC issue on GLES2/Android has been fixed in this release.

A big change since 3.1 beta 6 is that the Windows binaries are now **properly code signed**. Our release manager [HP van Braam](https://github.com/hpvb) is now signing binaries with their own company's certificate. From now on, you should thus expect (and can trust) our official binaries signed by **[Prehensile Tales B.V.](https://www.prehensile-tales.com/)**. macOS binaries will be signed at a later time.

Contrarily to our [3.0.x maintenance releases](/article/maintenance-release-godot-3-0-6), which include only thoroughly reviewed and backwards-compatible bug fixes, the 3.1 version includes all the new features (and subsequent bugs!) merged in the *master* branch since January 2018, and especially all those showcased on [our past devblogs](/devblog). It's been over a year since the 3.0 release and over 6,500 commits, so expect a lot of nice things in the final 3.1 version!

## Disclaimer

**IMPORTANT: This is a [*beta*](https://en.wikipedia.org/wiki/Software_release_life_cycle#Beta) build, which means that it is *not suitable* for use in production, nor for press reviews of what Godot 3.1 would be on its release.**

There will still be various fixes made before the final release, and we will need your [detailed bug reports](https://github.com/godotengine/godot/issues) to debug issues and fix them.

## The features

Release notes are drafted already, but we don't want to spoil the surprise of the 3.1 release announcement ;)
In the meantime, you can read the [preliminary changelog](https://github.com/godotengine/godot/blob/master/CHANGELOG.md#unreleased), as well as [past devblogs](/devblog).

Documentation writers are hard at work to catch up with the new features, and the [*latest* branch](http://docs.godotengine.org/en/latest/) should already include details on many of the new 3.1 features.

## Downloads

The download links are not featured on the [Download](/download) page to avoid confusion for new users. Instead, browse our download repository and fetch the editor binary and export templates that matches your platform and Godot flavour:

- [Classical build](https://github.com/godotengine/godot-builds/releases/3.1-beta9) (GDScript, GDNative, VisualScript)
- [Mono build](https://github.com/godotengine/godot-builds/releases/3.1-beta9) (C# support + all the above). You need to have MSbuild installed to use the Mono build. However, this build no longer mandates a specific Mono SDK version; it comes bundled with Mono 5.18.

**Important:** As mentioned above, Windows binaries are now signed by **Prehensile Tales B.V.**, the company of our release manager [HP van Braam](https://github.com/hpvb). You can trust this signature and accept any warning that Windows may issue due to the novelty of this certificate. As more users accept it, the certificate will be recognized as trusted for future releases.

## Bug reports

There is still a couple hundreds of open [bug reports for the 3.1 milestone](https://github.com/godotengine/godot/issues?q=is%3Aopen+is%3Aissue+milestone%3A3.1+label%3Abug), which means that we are aware of many bugs already. Yet, many of those issues are not critical for the 3.1 release and will end up retargeted to a later milestone.

As a tester, you are encouraged to open bug reports if you experience issues with 3.1 beta. Please check first the [existing issues](https://github.com/godotengine/godot/issues), using the search function with relevant keywords, to ensure that the bug you experience is not known already.

At this stage, we are mostly interested in critical bugs which could be showstoppers in Godot 3.1 stable. Yet feel free to report non-critical issues and enhancement proposals that will be worked on once 3.1 has been released.

**Known issues:**

- [GH-26359](https://github.com/godotengine/godot/issues/26359): Previous scenes/scripts and project layout not loading up (fixed in *master*)

*The illustration picture is from [HeartBeast Studios](http://twitter.com/uheartbeast/)' byte-sized roguelike *Endhall*, released in December on [itch.io](https://uheartbeast.itch.io/endhall) and [Steam](https://store.steampowered.com/app/838990/Endhall/?curator_clanid=41324400).*
