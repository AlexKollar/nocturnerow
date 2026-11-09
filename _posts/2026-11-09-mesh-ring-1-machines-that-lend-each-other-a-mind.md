---
layout: post
title: "Mesh, Ring 1: Machines That Lend Each Other a Mind"
date: 2026-11-09
tags: [apex, navi-mesh]
---
Apex machines can pool inference: a stronger box answers whole chat requests for a weaker one, and the reply says which machine wrote it. Ring 1 is deliberately narrow — whole requests only, no streaming — because the consent model matters more than the throughput.

Pairing is a physical act. Two machines exchange pairing cards — name, addresses, public key, certificate fingerprint, capabilities — and carrying that card across is the consent. Requests are signed, with a two-minute replay window. Lending can only be switched *on* in person, from the lender's own dashboard; a "stop lending" aborts both ends. The fully assembled prompt travels to the lender, and that is stated before the first borrow, in plain language. Files, stores, credentials and the command line never travel.

Ring 1 shipped in Edge v0.1.8e Build 1. The remaining proof is a real pair of machines in the field — that test is scheduled, and this note gets its second half when it happens. The full specification lives in [issue #78](https://github.com/AlexKollar/Apex/issues/78).
