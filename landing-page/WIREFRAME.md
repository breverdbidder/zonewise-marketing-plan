# Landing Page Wireframe

## URL: https://zonewise.ai

## Page Flow (Top to Bottom)

---

### Section 1: HERO
**Height:** Full viewport (100vh)
**Layout:** Left text, right product mockup

```
┌──────────────────────────────────────────────────────────┐
│ [Logo] ZoneWise.AI                    [Login] [Sign Up]  │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  Know Every Auction              ┌──────────────────┐   │
│  Before You Bid.                 │  [Dashboard       │   │
│                                  │   Screenshot      │   │
│  AI-powered foreclosure          │   with blurred    │   │
│  intelligence across all         │   ML scores and   │   │
│  67 Florida counties.            │   visible BID/    │   │
│  Desktop or Cloud.               │   SKIP badges]    │   │
│                                  │                   │   │
│  [Start Free — 7 Days Full ←]   │                   │   │
│  [Request Demo — Companies →]    └──────────────────┘   │
│                                                          │
│  No credit card required                                 │
└──────────────────────────────────────────────────────────┘
```

**Design notes:**
- Primary CTA (green): Individual registration
- Secondary CTA (blue outline): B2B demo request
- Dashboard screenshot is real, with strategic blurring
- Mobile: Stack vertically, CTAs full-width

---

### Section 2: PROOF BAR
**Height:** ~60px
**Layout:** Horizontal strip, dark background

```
┌──────────────────────────────────────────────────────────┐
│  67 Counties  •  12,000+ Analyzed  •  AI Predictions  •  │
│                Desktop & Cloud                            │
└──────────────────────────────────────────────────────────┘
```

**Design notes:**
- Numbers animate on scroll (count-up effect)
- Pull real numbers from Supabase when available
- Pre-launch: use Brevard County data as proof point

---

### Section 3: THE PROBLEM
**Height:** ~400px
**Layout:** Three columns

```
┌──────────────────────────────────────────────────────────┐
│            The Old Way vs. The ZoneWise Way               │
│                                                          │
│  ❌ Manual Research      ❌ Guesswork       ❌ Blind Bids │
│  Hours on BCPAO,         No way to predict   Overbidding │
│  clerk records,          auction outcomes    on bad deals  │
│  tax collector           or assess risk      or missing   │
│                                              good ones     │
│                          ↓                                │
│                                                          │
│  ✅ AI analyzes every property automatically              │
│  ✅ ML predicts outcomes before you bid                   │
│  ✅ Max Bid Calculator tells you your safe number         │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

### Section 4: PRODUCT FEATURES
**Height:** ~600px
**Layout:** Alternating left/right with screenshots

```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│  [Screenshot: ML Score]     AI-Powered Predictions       │
│                             Our ML models analyze every  │
│                             property and predict auction │
│                             outcomes. BID, REVIEW, or    │
│                             SKIP — know before you go.   │
│                                                          │
│  Max Bid Calculator         [Screenshot: Calculator]     │
│  Never overbid again.                                    │
│  Our formula factors in                                  │
│  ARV, repairs, liens, and                                │
│  market conditions.                                      │
│                                                          │
│  [Screenshot: Lien View]    Automated Lien Analysis      │
│                             We search actual recorded    │
│                             documents — mortgages, tax   │
│                             certs, HOA liens. No         │
│                             guesswork.                   │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

### Section 5: TWO PATHS
**Height:** ~500px
**Layout:** Two cards side by side

```
┌──────────────────────────────────────────────────────────┐
│              Built for How You Invest                     │
│                                                          │
│  ┌────────────────────┐  ┌────────────────────────┐     │
│  │  ☁️ CLOUD           │  │  🖥️ DESKTOP            │     │
│  │  For Individuals    │  │  For Companies          │     │
│  │                     │  │                         │     │
│  │  • Browser-based    │  │  • Downloaded app       │     │
│  │  • Any device       │  │  • Data stays local     │     │
│  │  • 1-5 counties     │  │  • All 67 counties      │     │
│  │  • $0 → $49/mo      │  │  • Multi-user seats     │     │
│  │                     │  │  • White-label reports   │     │
│  │  Solo investors     │  │  • API access            │     │
│  │  RE agents          │  │  • $299/mo               │     │
│  │  Wholesalers        │  │                         │     │
│  │                     │  │  Title companies         │     │
│  │  [Start Free →]     │  │  Law firms               │     │
│  │                     │  │  Investment funds         │     │
│  └────────────────────┘  │                         │     │
│                          │  [Schedule Demo →]       │     │
│                          └────────────────────────┘     │
└──────────────────────────────────────────────────────────┘
```

---

### Section 6: PRICING
**Height:** ~600px
**Layout:** Three pricing cards

```
┌──────────────────────────────────────────────────────────┐
│                    Simple Pricing                         │
│             [Monthly] / [Annual — Save 17%]              │
│                                                          │
│  ┌──────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │  FREE     │  │  PRO ⭐      │  │  ENTERPRISE   │      │
│  │  $0/mo    │  │  $49/mo      │  │  $299/mo      │      │
│  │           │  │  ($490/yr)   │  │  ($2,990/yr)  │      │
│  │  1 county │  │  5 counties  │  │  67 counties  │      │
│  │  5/day    │  │  Unlimited   │  │  Unlimited    │      │
│  │  Basic    │  │  Full AI     │  │  Full AI      │      │
│  │  No ML    │  │  ML Scores   │  │  ML Scores    │      │
│  │  No calc  │  │  Calculator  │  │  Calculator   │      │
│  │  No alerts│  │  Alerts      │  │  Desktop app  │      │
│  │           │  │  Reports     │  │  White-label  │      │
│  │           │  │              │  │  API + Export  │      │
│  │           │  │              │  │  5 seats       │      │
│  │           │  │              │  │                │      │
│  │ [Sign Up] │  │ [Start       │  │ [Schedule     │      │
│  │           │  │  Free Trial] │  │  Demo]        │      │
│  └──────────┘  └──────────────┘  └──────────────┘      │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

### Section 7: FAQ
**Height:** Variable (accordion)
**Layout:** Centered, expandable questions

```
┌──────────────────────────────────────────────────────────┐
│                 Frequently Asked Questions                │
│                                                          │
│  ▶ Is my data secure?                                    │
│  ▶ How accurate are the AI predictions?                  │
│  ▶ Which Florida counties are covered?                   │
│  ▶ Can I try before I buy?                               │
│  ▶ What's the difference between Cloud and Desktop?      │
│  ▶ Can I cancel anytime?                                 │
│  ▶ Do I need technical knowledge?                        │
│  ▶ How is this different from PropertyOnion?             │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

### Section 8: FINAL CTA
**Height:** ~300px
**Layout:** Full-width dark background

```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│         Stop guessing. Start knowing.                    │
│                                                          │
│    Every Florida foreclosure auction, analyzed by AI.    │
│                                                          │
│         [Start Free — 7 Days Full Access]                │
│                                                          │
│         No credit card required. Cancel anytime.         │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

### Section 9: FOOTER

```
┌──────────────────────────────────────────────────────────┐
│  ZoneWise.AI          Product        Company     Legal   │
│  AI Foreclosure       Cloud App      About       Terms   │
│  Intelligence         Desktop App    Blog        Privacy │
│                       Pricing        Contact     DMCA    │
│  © 2026 Everest       API Docs       Careers             │
│  Capital USA                                             │
└──────────────────────────────────────────────────────────┘
```

---

## Implementation Notes

**Framework:** React/Next.js (zonewise-web repo, deployed on Vercel)
**Styling:** Tailwind CSS
**Animations:** Framer Motion for scroll-triggered animations
**Forms:** Supabase Auth + custom registration handler
**Analytics:** PostHog for funnel tracking + A/B tests
**Performance:** Target Lighthouse score > 90
**Responsive:** Mobile-first, tested on iPhone SE through 4K
