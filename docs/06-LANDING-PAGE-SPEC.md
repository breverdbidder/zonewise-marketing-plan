# 06 — Landing Page Specification

## Page Architecture

Single landing page with two clear funnels. No separate pages for B2B/B2C — one page serves both with branching CTAs.

```
┌──────────────────────────────────────────────────┐
│                    HERO SECTION                    │
│  Headline + Sub + Dual CTAs                       │
├──────────────────────────────────────────────────┤
│                  PROOF BAR                         │
│  Counties · Properties Analyzed · Accuracy         │
├──────────────────────────────────────────────────┤
│               PRODUCT PREVIEW                      │
│  Dashboard screenshot with blurred ML scores       │
├──────────────────────────────────────────────────┤
│              HOW IT WORKS (3 Steps)                │
│  Register → Analyze → Bid Smart                    │
├──────────────────────────────────────────────────┤
│             TWO PATHS SECTION                      │
│  Individual Investor | Company / Institution       │
├──────────────────────────────────────────────────┤
│               FEATURE BREAKDOWN                    │
│  Cloud vs Desktop comparison                       │
├──────────────────────────────────────────────────┤
│                PRICING TIERS                       │
│  Free · PRO · Enterprise                           │
├──────────────────────────────────────────────────┤
│              SOCIAL PROOF / FAQ                    │
│  Testimonials + Common Questions                   │
├──────────────────────────────────────────────────┤
│               FINAL CTA                            │
│  "Start Free — 7 Days Full Access"                │
└──────────────────────────────────────────────────┘
```

---

## Section-by-Section Spec

### 1. Hero Section

**Headline (Primary — A/B test):**
- A: "Florida Auction Intelligence. AI-Powered."
- B: "Know Every Auction Before You Bid."
- C: "Foreclosures. Tax Deeds. One AI Platform."
- D: "Stop Guessing at Florida Auctions."

**Subheadline:**
"ML-powered analysis on every Florida foreclosure AND tax deed sale. Desktop or cloud. 7 days free."

**Dual CTAs (Side by side):**
```
[Start Free Trial — Individual]    [Request Demo — Companies]
     (Green, primary)                  (Blue, secondary)
```

**Background:**
Split-screen or gradient. Left side: clean cloud dashboard mockup. Right side: desktop app on a monitor.

### 2. Proof Bar (Horizontal Strip)

Real-time (or near-real-time) stats from Supabase:
```
67 FL Counties  |  Foreclosures + Tax Deeds  |  12,000+ Analyzed  |  AI Predictions  |  Desktop & Cloud
```

These numbers should update from actual platform data. Even before launch, show the Brevard County data as proof.

### 3. Product Preview

**Full-width dashboard screenshot** showing:
- Auction calendar with upcoming dates (foreclosure AND tax deed tabs)
- Property list with addresses visible
- ML scores **partially blurred** (showing the score exists but teasing the value)
- BID/REVIEW/SKIP badges visible on some, blurred on others
- Max Bid Calculator in sidebar (output blurred)
- Toggle between "Foreclosure Sales" and "Tax Deed Sales" visible

**Caption:** "Every auction. Every property. Foreclosures and tax deeds. One AI-powered dashboard."

**Interactive element (optional):** Let visitors hover over blurred areas to see "Register to unlock" tooltip.

### 4. How It Works (3 Steps)

```
Step 1: Register           Step 2: Analyze              Step 3: Bid Smart
[Icon: User + Key]         [Icon: Chart + AI]           [Icon: Gavel + Check]

Create your free           Our AI analyzes every        Go to auction knowing
account. Pick your         property — liens, value,     your max bid, which
county. Get instant        demographics, and            to pursue, and which
access.                    predicts outcomes.            to skip.
```

### 5. Two Paths Section

**Header:** "Built for How You Invest"

```
┌─────────────────────────┐  ┌─────────────────────────┐
│   INDIVIDUAL INVESTOR    │  │   COMPANY / INSTITUTION  │
│                          │  │                          │
│   Cloud-based platform   │  │   Desktop application    │
│   Access from any device │  │   Install on your systems│
│   Start with 1 county    │  │   All 67 FL counties     │
│   Perfect for solo       │  │   Multi-user seats       │
│   investors & agents     │  │   White-label reports    │
│                          │  │   API access & export    │
│   Free → $49/month       │  │   $299/month             │
│                          │  │                          │
│  [Start Free Trial →]    │  │  [Schedule a Demo →]     │
└─────────────────────────┘  └─────────────────────────┘
```

### 6. Feature Breakdown

**Header:** "One Intelligence Layer. Two Delivery Options. Both Auction Types."

Visual comparison table:

| Capability | Cloud (B2C) | Desktop (B2B) |
|-----------|-------------|---------------|
| Foreclosure Sale Analysis | ✅ | ✅ |
| Tax Deed Sale Analysis | ✅ (PRO+) | ✅ |
| AI Auction Analysis | ✅ | ✅ |
| ML Predictions | ✅ | ✅ |
| Max Bid Calculator | ✅ | ✅ |
| Lien Priority Analysis | ✅ | ✅ |
| Tax Cert History | ✅ (PRO+) | ✅ |
| Redemption Risk Score | ✅ (PRO+) | ✅ |
| Works Offline | ❌ | ✅ |
| Data Stays Local | ❌ | ✅ |
| White-Label Reports | ❌ | ✅ |
| API Access | ❌ | ✅ |
| Multi-User | ❌ | ✅ |
| Install Required | No | Yes |

### 7. Pricing Section

Three-column pricing cards (see PRICING.md for full details).

**Toggle:** Monthly / Annual (Annual selected by default, showing savings)

**FREE card** highlighted as "Start Here"
**PRO card** highlighted as "Most Popular"
**ENTERPRISE card** highlighted as "For Teams"

Each card includes a primary CTA:
- FREE: "Create Free Account"
- PRO: "Start 7-Day Free Trial"
- ENTERPRISE: "Schedule Demo"

### 8. Social Proof / FAQ

**Testimonials (Pre-Launch):**
Use Ariel's own Brevard County case studies as proof:
- "We identified $X in equity opportunities across Y properties using our ML analysis"
- Specific auction results where AI prediction matched outcome
- Time savings calculation: "What took 10 hours now takes 10 minutes"

**FAQ:**
- "Is my data secure?" → Cloud: encrypted. Desktop: stays on your machine.
- "How accurate are the ML predictions?" → Share accuracy metrics from training data.
- "Can I try before I buy?" → 7-day full trial, no credit card required.
- "What counties are covered?" → All 67 Florida counties.
- "Can I cancel anytime?" → Yes, no contracts, cancel from your dashboard.
- "Do I need technical knowledge?" → No, designed for investors not engineers.

### 9. Final CTA

**Full-width banner:**
```
Stop guessing. Start knowing.
Every Florida foreclosure and tax deed sale, analyzed by AI.

[Start Free — 7 Days Full Access]

No credit card required. Cancel anytime.
```

---

## Technical Implementation

**Stack:** React (JSX artifact) or Next.js on Vercel (zonewise-web repo)
**Styling:** Tailwind CSS
**Analytics:** Plausible or PostHog (privacy-friendly)
**Forms:** Direct to Supabase Auth + custom signup table
**A/B Testing:** Split headline variants with cookie-based assignment
**Performance:** Target < 2s load time, < 100KB initial bundle

---

## Mobile Responsiveness

- Hero: Stack CTAs vertically on mobile
- Two Paths: Full-width cards, swipeable
- Pricing: Horizontally scrollable cards
- Product Preview: Simplified mobile screenshot
- All CTAs: Full-width buttons on mobile with thumb-friendly sizing

---

## SEO Configuration

**Title:** ZoneWise.AI — Florida Foreclosure & Tax Deed Intelligence | AI-Powered Auction Analysis
**Meta Description:** AI-powered auction intelligence for Florida foreclosures AND tax deed sales. ML predictions, max bid calculator, lien analysis. Desktop or cloud. Start free.
**H1:** [Hero headline — matches A/B test variant]
**URL:** https://zonewise.ai
**Schema:** SoftwareApplication + Organization markup
