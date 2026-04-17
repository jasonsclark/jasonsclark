# Hi, I'm Jason 👋

**Product leader. Customer experience architect. Enterprise application builder. Meteorologist. Mountain Biker. Surfer.**

I've spent 25 years at the intersection of product management, customer experience, and enterprise application strategy — building platforms, designing journeys, and implementing systems that help organizations understand and serve their customers better. At **Yahoo** and **Salesforce** I owned product roadmaps, built customer health scoring platforms, designed lifecycle programs, and led enterprise application implementations across global teams. Before that I was deploying enterprise software to Fortune 500 clients around the world at **Kana Software**, where I learned that the gap between a good implementation and a failed one is almost always about requirements, relationships, and follow-through.

Before all of that, I was a kid who learned to surf and became obsessed with understanding how waves were created. I didn't want to be the one who heard about the swell after it happened — I wanted to forecast it myself and paddle out first. That obsession led me to the **U.S. Coast Guard** at 19, where I served as a Fireman aboard the USCGC Blackhaw stationed at Yerba Buena Island in San Francisco, then to **San Francisco State University** where I earned my **B.S. in Meteorology** in 1997.

I thought I'd become a professional forecaster or broadcast meteorologist. Instead, I took the programming, data modeling, and systems thinking from that degree and pivoted into tech — and spent the next 25 years building products, designing customer experiences, leading enterprise application implementations, and running teams across the industry.

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

## 🏢 The Work

Three threads have run through my career simultaneously — product management, customer experience design, and enterprise application implementation. Most of the time they happened inside the same role, which is what makes the combination unusual.

### Kana Software (1999–2003)

I started in enterprise software implementations, leading dozens of global deployments of Kana's customer communications and CRM platform for Fortune 500 clients. I owned the client relationship from requirements through go-live, translating what business leaders across Customer Service, Sales, Marketing, and Support actually needed into configured solutions that worked. I learned early that the hardest part of enterprise application work is never the technology — it's understanding what people actually need before you build anything.

### Yahoo (2003–2013)

At Yahoo I did all three things at once. On the **enterprise application** side I implemented and administered **Inquira** (enterprise knowledge management) and **Kana CRM** for Yahoo's Global Customer Support Organization, supporting over 80 million monthly users across 100+ products and 32 languages. On the **product management** side I owned the roadmap and strategy for Yahoo's global Help platform, partnering directly with engineering and data teams to ship improvements at consumer internet scale. On the **customer experience** side I designed self-service journeys, ran A/B testing and content optimization programs, and standardized content architecture and governance across a massively distributed global team — because 80 million users experiencing fragmentation across 32 languages is a CX problem, not just an operational one.

### Salesforce (2013–2023)

Ten years, three roles, all three threads running in parallel.

On the **product management** side I owned the strategy, roadmap, lifecycle, and financial performance of Salesforce's Success Plans portfolio — from concept through launch, optimization, and renewal. I incubated the Accelerator Program from scratch, built business cases, defined value propositions, and scaled a new engagement model across all customer segments. I selected and implemented **Coveo** as the enterprise search platform of record across all customer-facing properties after rigorous vendor evaluation. I extended the Admin Services managed services offering across 15+ M&A integrations, and launched the EU Premier Success Plan as a compliance-aligned service for regulated markets.

On the **customer experience** side I led user research and persona development to build **Cloudpulse** — Salesforce's first customer-facing health scoring platform. The research uncovered that customers had widely varying levels of technical competency and business context, so we designed visualization frameworks and simplified dashboards that gave every customer clear visibility into their own engagement and adoption gaps. I designed customer journey frameworks, lifecycle programs, and proactive engagement systems that reduced attrition and improved retention across hundreds of thousands of customers. I redesigned the end-to-end Help and Training navigation and search experience using behavioral data and iterative user feedback.

On the **enterprise application** side I implemented Salesforce on Salesforce internally, owned the Help and Training platform as a product, and partnered with BI Engineering to build the telemetry systems and behavioral scoring models that powered Cloudpulse.

### Epic Forecast Consulting (2024–Present)

All three threads continue in consulting form. On the **enterprise application** side I evaluated and remediated a **Birdeye** implementation for a legal services firm and implemented **Hona** as a client communication portal, working directly with leadership to assess the environment, define requirements, and drive adoption. On the **customer experience** side I mapped the client journey, identified moments of truth across the case lifecycle, and designed the communication frameworks and feedback systems that improved client confidence and retention. On the **product** side I am building Epic Forecast from the ground up — data architecture, LLM orchestration, prompt engineering, agentic workflows, and evaluation frameworks.

The common thread across all of it: understanding what people actually need, building or implementing the right solution, and ensuring it delivers real value rather than just going live.

---

## 💡 What I Think About

- How product, customer experience, and enterprise application work converge — and why separating them creates worse outcomes
- The gap between data available and data useful — in weather and in everything else
- Why journey mapping and moments of truth matter more than satisfaction scores
- Building AI-powered experiences that feel human, not robotic
- The transition from project-based delivery to product-centric operating models — and why it matters
- Waves, swells, buoy data, and when to paddle out

---

## 🧭 Where I've Been

| | |
|---|---|
| **Epic Forecast** | Founder and Principal Consultant — product management, CX strategy, and enterprise application consulting while building the weather platform I've wanted to create for 25 years |
| **Salesforce** | Product management, CX design, and enterprise application strategy across Success Plans, Cloudpulse, Coveo, and M&A integration |
| **Yahoo** | Product management, CX design, and enterprise application implementation at global consumer internet scale |
| **Kana Software** | Managing Consultant — led dozens of global enterprise software deployments for Fortune 500 clients |
| **U.S. Coast Guard** | Fireman (E3) · USCGC Blackhaw · Yerba Buena Island, San Francisco |
| **San Francisco State** | B.S. Meteorology, 1997 |

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/jasonsclark/)
[![Email](https://img.shields.io/badge/Email-jason@epicforecast.com-green?style=flat&logo=gmail)](mailto:jason@epicforecast.com)
