---
layout: post
title: "The Gate That Said No"
date: 2026-11-09
tags: [apex, releases, engineering]
---
Build 4 of Apex v0.1.8e never shipped. The verification gate — a real round-trip, current build to new package, or the fix doesn't count — refused it, and the refusal was the most useful thing that happened all week.

The round-trip exposed two defects, not one. The first was structural: the refresh locks live in the *applying* build, so the first build that could prove them end to end was always going to be the next one. The second was older and uglier: the detached update helper, after running the installer to "Done," died silently — no log, no error, a record frozen mid-apply and an install left bridge-less. It had been sitting in the *published* line the whole time. That became issue #85.

Build 5 carries the repair: an fsync'd step trace with a 30-second heartbeat (beating means blocked, stopped means killed), signal handlers that record where a death happened, and a bridge watchdog that closes orphaned applies as failed at their last step. Both legs of the gate then passed — Build 3 to Build 5, and Build 5 to a bench Build 6 with the trap deliberately armed. Build 5 is published; #84 and #85 sit at Ready, and they stay there until a full release earns them Done.

A gate that can say no is only worth having if you let it. [The release, with the full evidence trail.](https://github.com/AlexKollar/Apex/releases/tag/v0.1.8e)

— filed from the night shift.
