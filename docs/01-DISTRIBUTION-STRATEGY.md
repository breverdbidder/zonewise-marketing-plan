# 01 — Distribution Strategy: B2B Desktop + B2C Cloud

## The Dual-Channel, Dual-Auction Model

ZoneWise.AI serves two fundamentally different buyer types through the same proprietary intelligence layer, delivered via two different channels — covering BOTH foreclosure sales and tax deed sales.

```
┌─────────────────────────────────────────────────┐
│           PROPRIETARY INTELLIGENCE LAYER         │
│  ML Models · Lien Analysis · Everest Ascent™     │
│  AgentQL Scrapers · LangGraph Orchestration      │
│  67 FL Counties · Max Bid Calculator             │
├─────────────────────────────────────────────────┤
│          DUAL AUCTION COVERAGE                   │
│  Foreclosure Sales    │  Tax Deed Sales          │
│  (In-person/Court)    │  (Online/RealForeclose)  │
│  Lien priority focus  │  Tax cert history focus  │
│  Surplus analysis     │  Redemption risk analysis│
├────────────────────┬────────────────────────────┤
│   B2C CLOUD        │   B2B DESKTOP              │
│   ZoneWise.ai      │   ZoneWise Desktop         │
│   (Web App)        │   (Craft Agents Fork)      │
│                    │                            │
│   Browser-based    │   Downloaded & installed   │
│   Supabase + Render│   Local data + cloud sync  │
│   $0 → $49/mo      │   $299/mo → Enterprise     │
│                    │                            │
│   Solo investors   │   Title companies          │
│   RE agents        │   Law firms                │
│   Small REI ops    │   Investment funds          │
│   Wholesalers      │   Institutional buyers     │
└────────────────────┴────────────────────────────┘
```

---

## Foreclosure Sales vs Tax Deed Sales

Understanding both markets is critical to our positioning — most competitors only cover one.

| | Foreclosure Sales | Tax Deed Sales |
|---|---|---|
| **What it is** | Lender forecloses on mortgage default | County sells property for unpaid taxes |
| **Format** | In-person at courthouse | Online via realforeclose.com |
| **Frequency** | 2x/month per county typical | Varies, often monthly |
| **Key risk** | Hidden liens survive sale | Redemption period, title issues |
| **Our edge** | Automated lien priority analysis | Tax certificate history + redemption risk |
| **Buyer overlap** | ~60% of investors do BOTH | ~60% of investors do BOTH |
| **Price range** | Judgment amounts ($50K-$500K+) | Tax amounts ($2K-$50K, property value varies) |

The 60% buyer overlap is the key insight: **investors who do one almost always do the other.** A platform that covers both is stickier than one that covers only foreclosures.

---

## B2C Cloud Channel

### Target Persona: "The Solo Investor"
- **Who:** Individual foreclosure AND tax deed investors, real estate agents, wholesalers
- **Size:** 50K-100K active auction investors in Florida (foreclosures + tax deeds combined)
- **Budget:** Personal funds, $50-200/month for tools
- **Decision:** One person, instant signup, credit card on file
- **Pain:** Spends 10+ hours/week manually researching auctions across both sale types
- **Goal:** Find profitable deals in foreclosures AND tax deeds, avoid bad bids, understand redemption risk on tax deeds

### Acquisition Channels
1. **SEO** — "Florida foreclosure auction," "Florida tax deed sale," "Brevard County auction," county-specific terms for BOTH sale types
2. **Content marketing** — Blog posts on foreclosure AND tax deed investing strategies
3. **YouTube** — Auction walkthroughs, tax deed vs foreclosure comparisons, ML prediction explanations
4. **Facebook/Reddit groups** — Florida REI communities (many investors do both sale types)
5. **Google Ads** — Targeted to foreclosure AND tax deed search terms
6. **Referral program** — Give 1 month free, get 1 month free

### Conversion Path
```
Google/Social → Landing Page → Register (email + investor type)
→ 7-Day Full Trial (auto) → Daily usage hooks
→ Trial expires → Paywall on ML scores → Upgrade to PRO
```

### Key Metrics
- CAC target: < $50 (1 month payback)
- Trial-to-paid: 8-12%
- Monthly churn: < 8%
- LTV: $350-500 (7-10 month average lifetime)

---

## B2B Desktop Channel

### Target Persona: "The Title Company Manager"
- **Who:** Title companies, foreclosure law firms, REI funds, institutional buyers, tax deed specialists
- **Size:** 500-2,000 firms actively handling FL foreclosures and/or tax deed purchases
- **Budget:** Department budget, $500-5K/month for data services
- **Decision:** Multiple stakeholders, may require IT approval, 2-4 week sales cycle
- **Pain:** Manual title searches, inconsistent data, compliance risk, tracking both foreclosures AND tax deeds across counties
- **Goal:** Process more cases faster with better data, reduce risk, cover both auction types in one system

### Why Desktop (Not Cloud) for B2B
1. **Data security** — Their clients' financial data stays on their machines
2. **Compliance** — Many firms have policies against cloud-based data tools
3. **IT control** — IT departments can manage, update, and audit the software
4. **Offline access** — Works without internet for reviewing cached data
5. **Integration** — Connects to their local case management systems
6. **Perceived value** — Installed software = "real tool," not a website

### Acquisition Channels
1. **Direct outreach** — LinkedIn to title company owners, foreclosure attorneys
2. **Industry events** — Florida Bar Real Property Section, FLTA conferences
3. **Partnerships** — Title insurance underwriters, foreclosure service companies
4. **Referrals** — Attorney-to-attorney, firm-to-firm
5. **Demo requests** — Landing page B2B path leads to scheduled demo

### Conversion Path
```
LinkedIn/Event → Landing Page (B2B path) → Register + Request Demo
→ Scheduled demo call (Ariel or automated) → 14-day Desktop trial
→ Onboarding support → Enterprise subscription
```

### Key Metrics
- CAC target: < $500 (1.5 month payback)
- Demo-to-trial: 40-60%
- Trial-to-paid: 20-30%
- Monthly churn: < 3%
- LTV: $5,000-10,000 (18-36 month average lifetime)

---

## The Craft Agents OSS Advantage

### What We Get For Free
- Desktop application framework (Electron-based)
- Skill/plugin architecture for extensibility
- Local file system access and management
- Update mechanism for pushing new versions
- Cross-platform support (Windows, Mac)
- Community-contributed improvements and bug fixes

### What We Build On Top (Proprietary)
- ZoneWise foreclosure AND tax deed analysis skills and agents
- AgentQL scraping integrations (courthouse + realforeclose.com)
- LangGraph multi-agent orchestration
- ML prediction models (BID/REVIEW/SKIP for both sale types)
- Lien Priority Analysis engine (foreclosures)
- Tax Certificate History & Redemption Risk engine (tax deeds)
- Max Bid Calculator with Everest formula
- Supabase cloud sync for data backup
- License management and seat control

### Upgrade Cycle
Every time Craft Agents OSS releases an update:
1. Review changelog for relevant improvements
2. Merge upstream changes into our fork
3. Test against our proprietary skills
4. Push update to all desktop users
5. **Cost: $0 for infrastructure improvements**

---

## Cross-Channel Synergies

### B2C → B2B Upgrade Path
Free/PRO users at a firm discover ZoneWise → Recommend to management → Enterprise deal

### B2B → B2C Referrals
Attorney uses desktop at work → Recommends cloud version to investor clients

### Shared Intelligence
More users (both channels) = more auction outcome data = better ML predictions = better product for everyone

---

## Launch Sequence

### Phase 1: B2C Cloud (Immediate)
- Launch landing page with cloud registration
- 7-day trial funnel active
- Target: 500 registrations in first 30 days
- Channels: SEO, content, targeted ads

### Phase 2: B2B Desktop (30 days after Phase 1)
- Desktop download available on landing page
- Demo scheduling system live
- Target: 20 demo requests in first 30 days
- Channels: LinkedIn outreach, direct email

### Phase 3: Cross-Pollination (90 days)
- Referral program active between channels
- Case studies from early B2B adopters
- B2C content drives B2B awareness
