# Hi, I'm Jason 👋

**Product leader. Enterprise application builder. Meteorologist. Mountain Biker. Surfer.**

I've spent 25 years leading product, customer experience, and enterprise application strategy at companies like **Yahoo** and **Salesforce** — implementing and evolving platforms that improve adoption, reduce churn, and create new revenue across global teams. Before that I was deploying enterprise software to Fortune 500 clients around the world at **Kana Software**, where I learned that the gap between a good implementation and a failed one is almost always about requirements, relationships, and follow-through.

Before all of that, I was a kid who learned to surf and became obsessed with understanding how waves were created. I didn't want to be the one who heard about the swell after it happened — I wanted to forecast it myself and paddle out first. That obsession led me to the **U.S. Coast Guard** (weather program at 19), then to **San Francisco State University** where I earned my **B.S. in Meteorology** in 1997.

I thought I'd become a professional forecaster or broadcast meteorologist. Instead, I took the programming, data modeling, and systems thinking from that degree and pivoted into tech — and spent the next 25 years building products, leading enterprise application implementations, and running teams across the industry.

I never stopped caring about weather. Now I'm building the thing I've been thinking about since I first paddled out.

---

## 🌦️ What I'm Building

### Epic Forecast — Weather with a Personality and a Brain

Most weather apps are broken in two ways. They're **inaccurate where it matters** — forecasts pinned to a regional grid point miles from where you actually are, ignoring elevation, terrain, and microclimate. And they're **lifeless** — no personality, no context for what you're actually doing, no reason to trust or engage.

Epic Forecast is an intelligent weather broadcasting platform that fixes both. We combine **hyperlocal, elevation-corrected forecast data** with **broadcast-style delivery that adapts to your personality preference and life context**. The result is weather that's accurate enough to trust and engaging enough to remember.

**What makes it different:**

- 🎯 **Terrain-aware accuracy** — NWS data enriched with USGS elevation and terrain classification, because valley fog and ridge sunshine are two different forecasts
- 🎙️ **Selectable broadcaster personalities** — choose the voice that fits your mood, from clever and scientific to bombastic and cantankerous
- 🏔️ **Built by a meteorologist** — not a team that treats weather as a generic data feed, but someone who reads NWS forecast discussions for fun and knows where models break down
- 🔄 **Resilient architecture** — tiered caching, circuit breakers, and graceful degradation so you always get a forecast, even when upstream data sources go down

### The Technical Foundation

The platform is built on a Node.js/TypeScript backend with a Next.js 15 frontend. The data pipeline ingests from the National Weather Service API, enriches it with USGS elevation data and Census geocoding, and serves it through a tiered Redis cache with type-specific TTLs (observations refresh faster than extended forecasts). When upstream APIs fail, the system serves stale data with transparency flags rather than returning errors — because people rely on weather for real decisions and a slightly stale forecast beats no forecast.

Key architecture decisions:

| Decision | What we chose | Why |
|----------|--------------|-----|
| Data source | NWS over commercial APIs | Free, high-quality, full US coverage — removes per-request cost as a scaling constraint |
| Failure mode | Stale cache with `isStale` flag | Users need weather even when upstream is down |
| Upstream protection | Circuit breaker pattern | Prevents request floods during NWS outages |
| Elevation data | Additive enrichment, not silent correction | Transparency over magic — users see the context |
| Frontend state | TanStack Query + Zustand | Clean separation of server cache vs. UI state |

---

## 🏢 Enterprise Application Work

Most of my career has been spent at the intersection of product thinking and enterprise application delivery — not just defining what to build, but making sure implementations actually work for the people who depend on them.

At **Kana Software** I led dozens of global enterprise software deployments for Fortune 500 clients, serving as the primary relationship owner from requirements through go-live across Customer Service, Sales, Marketing, and Support functions. I learned early that the hardest part of enterprise application work is never the technology — it's translating what business leaders actually need into something a system can reliably deliver.

At **Yahoo** I implemented and administered both **Inquira** (enterprise knowledge management) and **Kana CRM** for Yahoo's Global Customer Support Organization, supporting over 80 million monthly users across 100+ products and 32 languages. I also standardized the content architecture and governance workflows that kept the platform coherent across a massively distributed team.

At **Salesforce** I owned product and application strategy for the digital customer success ecosystem, led the evaluation and selection of **Coveo** as the enterprise search platform of record across all customer-facing properties, and launched **Cloudpulse** — Salesforce's first customer health scoring and adoption intelligence platform — in partnership with engineering and BI teams.

More recently through **Epic Forecast Consulting** I have implemented **Birdeye** (AI-powered reputation and client experience management) and **Hona** (client communication portal) for a legal services firm, working directly with leadership to assess the environment, define requirements, and drive adoption.

The common thread across all of it: understanding what organizations actually need, selecting or building the right platform, and ensuring the implementation delivers real value rather than just going live.

---

## 💡 What I Think About

- How product, operations, and go-to-market converge to drive real outcomes
- The gap between data available and data useful — in weather and in everything else
- Why enterprise application success depends more on requirements and relationships than technology selection
- Building AI-powered experiences that feel human, not robotic
- The transition from project-based delivery to product-centric operating models — and why it matters
- Waves, swells, buoy data, and when to paddle out

---

## 🧭 Where I've Been

| | |
|---|---|
| **Epic Forecast** | Founder and Principal Consultant — building the weather platform I've wanted to create for 25 years, and helping organizations modernize their enterprise application environments |
| **Salesforce** | Product and application strategy across platform initiatives, M&A integration, and enterprise search and intelligence systems |
| **Yahoo** | Enterprise application implementation and digital engagement at global scale |
| **Kana Software** | Managing Consultant — led dozens of global enterprise software deployments for Fortune 500 clients |
| **U.S. Coast Guard** | Operational weather program · California coast |
| **San Francisco State** | B.S. Meteorology, 1997 |

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/jasonsclark/)
[![Email](https://img.shields.io/badge/Email-jason@epicforecast.com-green?style=flat&logo=gmail)](mailto:jason@epicforecast.com)
