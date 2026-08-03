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
related:
  - "cards/privacy-browser.md"
  - "cards/dns-blocking.md"
  - "cards/anonymous-browsing.md"
  - "cards/google-privacy-settings.md"
---

## Why

Every search query reveals intent — what you're researching, what you're worried about, where you want to go, what you might buy. Google processes over 8 billion searches per day and logs every one tied to your account: your search terms, location, the ads you click, and now your images (Lens), voice recordings, and video. In July 2026, Google quietly opted all users into AI training on this data — images uploaded to Lens, voice searches, and Translate audio are saved and used to train Google's AI models by default, under a new 'Search Services History' setting that auto-enabled even if you'd previously disabled Web & App Activity. Google's own engineers demonstrated they could re-identify individuals from 'anonymized' search query data in a matter of hours — granular search history contains enough biographical detail to unmask anyone. Your search history is the most intimate dataset Google holds on you, and it never expires unless you manually delete it.

## Steps

### General

Set as default in your browser's settings. The key question for any search engine is: does it crawl and index the web itself, or does it just repackage Google/Bing results? Independence matters — if your engine depends on a Big Tech index, your queries still reach the mothership. After migrating, delete your existing Google search history at myactivity.google.com — export it first via Google Takeout (takeout.google.com) if you want a local copy.

<strong>Brave Search</strong> (recommended for most) — one of only three independent web-scale indexes in the world (alongside Google and Bing), and the only one outside Big Tech. Now serves 100% of queries from its own index of 40 billion pages — zero Bing fallback. Privacy is architectural: no user profiling, no identity-bound queries, no ad-profile feedback into ranking. Goggles feature lets you apply custom ranking rules (e.g., prioritize tech blogs, demote SEO spam). Available at search.brave.com or as a default engine in any browser. The trade-off: Brave Search includes an AI answer feature (opt-out), and image/video search still relies on third-party sources.

<strong>DuckDuckGo</strong> — reliable results, familiar interface, but entirely dependent on Microsoft's Bing index. Your queries reach Microsoft's infrastructure. In 2022, security researcher Zach Edwards found DuckDuckGo's mobile browser allowed Microsoft tracking scripts on third-party sites while blocking Google and Facebook trackers — their Microsoft syndication contract explicitly prevented blocking Microsoft-owned scripts. DuckDuckGo removed this restriction in August 2022, but the nondisclosure damaged trust. Good for onboarding (familiar, zero-config), but it's a façade over Bing, not a true alternative.

<strong>Startpage</strong> — acts as a privacy proxy for Google results. Strips your IP address and identifying metadata before sending your query to Google, then returns results without building a profile. Based in the Netherlands under GDPR. Includes Anonymous View, which opens search results through Startpage's proxy so destination sites don't see your IP. The concern: System1, a US ad-tech company, acquired a majority stake in 2019. No evidence of privacy violations, but governance opacity prompted PrivacyTools to temporarily delist Startpage. Good for users who want Google-quality results without Google tracking, but you're trusting a proxy operated by an ad-tech parent.

<strong>Mojeek</strong> — a truly independent search engine based in the UK. Own crawler (MojeekBot), own index (9 billion pages), own ranking algorithm — zero dependency on Google or Bing. First search engine with a no-tracking privacy policy (2006). Results ranked by objective factors, not behavioral profiling — two people searching the same query get the same results. Smaller index (9B vs Brave's 40B) means less comprehensive for obscure or long-tail queries. Good as a secondary engine or for users who value index independence above result completeness.

## Self-Hosted

<strong>SearXNG</strong> (AGPL-3.0, 34,598★) — a metasearch engine, not a search engine. It has no index of its own — instead it aggregates results from 70+ upstream engines (Google, Bing, Brave, DuckDuckGo, Wikipedia, Reddit) simultaneously. Privacy comes from architecture: upstream engines see your server's IP, not yours. No cookies, no profile, no fingerprint. Self-host via Docker Compose in 5 minutes, or use a public instance (with the trust caveat that the operator could log queries). Run behind Tailscale for personal use — no public exposure needed. The most private option if you're willing to self-host.

## Going Further

<strong>Multi-engine strategy</strong>
Use Brave Search as your daily driver, and run a self-hosted SearXNG instance for sensitive queries — health, financial, legal research. SearXNG behind Tailscale gives you results from 70+ engines with zero tracking, and your queries are invisible to every upstream provider.

<strong>Brave Goggles</strong>
Goggles are user-created ranking rules that override Brave's default algorithm. For example, a "tech blogs" Goggle prioritizes results from independent tech publications and demotes SEO-optimized content farms. Create your own or use community Goggles at search.brave.com/goggles.

<strong>Disable Google's AI training</strong>
If you still use any Google services, disable Search Services History → Save Media, and set auto-delete to 3 months. Visit myactivity.google.com to review and delete existing search history. Note: Google separated this setting from Web & App Activity in 2026, so turning off the old setting no longer protects your search data. See the <a href="/cards/google-privacy-settings">Google Account Lockdown</a> card for a full privacy settings walkthrough.

## Sources

1. techcrunch.com/2026/07/06/if-you-use-google-youre-training-its-ai-heres-how-to-opt-out/ (TechCrunch: Google quietly opted all users into AI training on search data — images, voice recordings, and video from Lens, Translate, and Search Live are saved and used to train AI models by default under a new Search Services History setting)
2. politico.eu/article/google-says-its-protecting-our-privacy-the-eu-thinks-its-guarding-its-monopoly/ (Politico: EU DMA fight revealed Google can re-identify users from "anonymized" search query data in hours — granular queries contain enough biographical detail to unmask individuals)
3. policies.google.com/privacy (Google Privacy Policy: explicitly collects search terms, views/interactions with content and ads, Chrome browsing history, location data, and media including images, files, audio, and video)
4. english.elpais.com/technology/2025-12-15/shoshana-zuboff-philosopher-ai-is-surveillance-capitalism-continuing-to-evolve-and-expand.html (El País: Shoshana Zuboff explains how Google discovered that search queries reveal behavioral surplus — "predictions of human behavior could be sold" — and how Larry Page insisted on hiding this from users: "We can never tell them")

## Guides

1. search.brave.com (Brave Search: independent index, 40B pages, zero Bing fallback, Goggles for custom ranking)
2. duckduckgo.com (DuckDuckGo: privacy-focused search, Bing-dependent index, no search history logging)
3. startpage.com (Startpage: Google results through a privacy proxy, Netherlands/GDPR jurisdiction, Anonymous View feature)
4. docs.searxng.org (SearXNG: self-hosted metasearch engine aggregating 70+ engines, AGPL-3.0, 34,598★)
5. mojeek.com (Mojeek: independent UK search engine with own crawler and index, no-tracking policy since 2006)
6. privacyguides.org/en/search-engines/ (PrivacyGuides: search engine recommendations with privacy policy analysis, Tor hidden service support, and index independence comparison — recommends Brave Search, DuckDuckGo, Startpage, and SearXNG; does not list Mojeek)
7. eylenburg.github.io/ai_search_maps.htm (Eylenburg: knowledge provider comparison — 39 AI, search, and map services with index source, originality, and feature analysis)
