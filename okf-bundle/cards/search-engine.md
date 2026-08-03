---
type: "lbr8 Protocol Card"
title: "Private Search Engine"
description: "Replace Google Search with a search engine that doesn't track, profile, or sell your search history."
tags:
  - "phase-1"
  - "network"
  - "basic"
  - "p1"
  - "tracking"
  - "ad-targeting"
  - "big-tech-surveillance"
---

## Context for the Agent

This card helps the user replace Google Search with a search engine that doesn't track, profile, or sell their search history. Use it when the user is ready to stop Google from logging every search query they make.

## Why This Matters

Every search query reveals intent — what you're researching, what you're worried about, where you want to go, what you might buy. Google processes over 8 billion searches per day and logs every one tied to your account: search terms, location, ads clicked, and now images (Lens), voice recordings, and video [2]. In July 2026, Google quietly opted all users into AI training on search data — images uploaded to Lens, voice searches, and Translate audio are saved and used to train Google's AI models by default under a new "Search Services History" setting [1]. Google's own engineers demonstrated they could re-identify individuals from "anonymized" search query data in hours — granular search history contains enough biographical detail to unmask anyone [2]. Your search history is the most intimate dataset Google holds on you, and it never expires unless you manually delete it.

## Coaching Flow

### Step 1: Choose a Private Search Engine
Based on the user's priorities, recommend one of these:

- **Brave Search** (recommended for most users): Independent index, ~40B pages, zero Bing fallback. Goggles let you create custom ranking rules. No tracking, no profiling. Works well out of the box.
- **DuckDuckGo** (best for simplicity): Bing-dependent index, but strips all identifying information from queries. Bangs (!w, !a, !yt) are the killer feature. No account needed, no search history logged.
- **Startpage** (best for Google results without Google): Returns Google search results through a privacy proxy under Netherlands/GDPR jurisdiction. Anonymous View feature lets you browse result pages through their proxy. If the user "needs" Google results, this is the option.
- **SearXNG** (self-hosted, for technical users): Metasearch engine aggregating 70+ search engines. You host it yourself — full control, no third-party. Good for users who want to escape any single search engine dependency.

### Step 2: Set as Default Browser Search Engine
Guide the user to change their browser's default search engine:
- **Brave:** Settings → Search Engine → Select Brave Search or DuckDuckGo
- **Firefox/LibreWolf:** Settings → Search → Default Search Engine → Select
- **Chrome (if they haven't switched yet):** Settings → Search Engine → Manage Search Engines
- Walk them through making the switch in the browser's address bar search

### Step 3: Delete Google Search History
Tell the user to export their Google search history first (if they want a local copy) via Google Takeout at takeout.google.com, then delete it at myactivity.google.com. Explain that this is a one-time cleanup — going forward, their queries will not be logged by the new search engine.

### Step 4: Test the New Search Engine
Ask the user to try a few searches they normally do. Compare the results to what they used to get from Google. Most private search engines produce comparable results for everyday searches. If they find a specific query that yields poor results, suggest trying a different engine or using the `!g` bang (DuckDuckGo) to temporarily fall back to Google.

## Decision Points

Ask the user: "How important is it to you that your search results come from Google's index?" If they rely on Google's search quality (e.g., for research, local business discovery), recommend Startpage (Google results via privacy proxy). If they want independence from Google entirely, recommend Brave Search. If they want the simplest possible switch, recommend DuckDuckGo.

Ask the user: "Do you want to self-host your own search engine?" Only for technical users. If yes, guide them to SearXNG.

## Pitfalls

- DuckDuckGo's results depend on Bing. If Bing changes its policy or API terms, DuckDuckGo is affected. The user should understand this dependency.
- Brave Search uses a mix of its own index, Bing, and (for some queries) Google. It has a "Goggles" feature that lets users filter results, but the default experience is still partially dependent on other indexes.
- Startpage's Anonymous View proxies web pages through their servers — this adds latency and may break JavaScript-heavy sites. Most users should use the standard search results (not Anonymous View) for daily use.
- Changing the default search engine in Chrome is possible, but Chrome still sends some data to Google (autocomplete, spellcheck) even if the default search is changed. Recommend switching browsers entirely for full privacy.
- Some private search engines (DuckDuckGo, Startpage) show ads — but they are based on the search query, not on your profile or history.

## Sources

1. techcrunch.com/2026/07/06/if-you-use-google-youre-training-its-ai-heres-how-to-opt-out/ — TechCrunch: Google quietly opted all users into AI training on search data — images, voice recordings, and video from Lens, Translate, and Search Live saved and used to train AI models by default
2. politico.eu/article/google-says-its-protecting-our-privacy-the-eu-thinks-its-guarding-its-monopoly/ — Politico: EU DMA fight revealed Google can re-identify users from "anonymized" search query data in hours
3. policies.google.com/privacy — Google Privacy Policy: explicitly collects search terms, views/interactions with content and ads, Chrome browsing history, location data, and media including images, files, audio, and video
4. english.elpais.com/technology/2025/12/15/shoshana-zuboff-philosopher-ai-is-surveillance-capitalism-continuing-to-evolve-and-expand.html — El País: Shoshana Zuboff explains how Google discovered that search queries reveal behavioral surplus — "predictions of human behavior could be sold"

## Guides

1. search.brave.com — Brave Search: independent index, 40B pages, zero Bing fallback, Goggles for custom ranking
2. duckduckgo.com — DuckDuckGo: privacy-focused search, Bing-dependent index, no search history logging
3. startpage.com — Startpage: Google results through a privacy proxy, Netherlands/GDPR jurisdiction, Anonymous View feature
4. docs.searxng.org — SearXNG: self-hosted metasearch engine aggregating 70+ engines, AGPL-3.0
5. mojeek.com — Mojeek: independent UK search engine with own crawler and index, no-tracking policy since 2006
6. privacyguides.org/en/search-engines/ — PrivacyGuides: search engine recommendations with privacy policy analysis, Tor hidden service support, and index independence comparison
7. eylenburg.github.io/ai_search_maps.htm — Eylenburg: knowledge provider comparison — 39 AI, search, and map services with index source, originality, and feature analysis