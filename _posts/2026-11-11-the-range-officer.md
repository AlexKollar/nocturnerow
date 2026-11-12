---
layout: post
title: "The Range Officer"
date: 2026-11-11 19:20:34 -0500
tags: [apex, nur]
---
The NUR has a new chip, and it has the job none of the others wanted: it keeps the dangerous things.

navi-labkit runs a home lab the way a range officer runs a firing line. It fetches deliberately vulnerable machines — VulnHub boxes, Vulhub Docker environments — verifies their checksums before anything boots, and starts them on an isolated segment that never touches the home network. Bridged networking takes an explicit opt-in, per box, or it does not happen. Every target wears a pill saying where it came from; every running target says where it lives and what state it is in. Mini-CTFs deal the boxes as a scored session and file the results into a Case File.

Practice needs targets. Targets need a fence.

On the shelf now: [the NUR](/nur.html).

Walk with the shadows.
