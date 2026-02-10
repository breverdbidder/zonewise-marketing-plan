# 02 — Freemium Funnel: Registration → Trial → Conversion

## Registration-First Architecture

**Rule: No anonymous access. Every user registers before seeing any data.**

### Why Registration-First
- Capture leads immediately (email = retargeting asset)
- Segment B2B vs B2C from signup
- Control onboarding flow per user type
- Enable 7-day trial tracking
- Build email nurture list from day zero

### Registration Flow

```
Landing Page
    │
    ├─── "I'm an individual investor" ──→ Cloud Registration
    │       │
    │       ├── Email
    │       ├── Name
    │       ├── Password
    │       ├── "Which county do you invest in?" (dropdown: 67 FL counties)
    │       ├── "How do you invest?" (Solo / Agent / Wholesaler / Other)
    │       └── [Start Free Trial] ──→ Cloud Dashboard (7-day PRO access)
    │
    └─── "I represent a company" ──→ B2B Registration
            │
            ├── Work Email
            ├── Name + Title
            ├── Company Name
            ├── Company Type (Title Co / Law Firm / Fund / Other)
            ├── "How many people would use this?" (1-5 / 5-20 / 20+)
            └── [Request Demo] ──→ Demo Scheduling + Desktop Trial Link
```

---

## The 7-Day Trial Experience (B2C)

The trial is NOT a limited preview. It's **full PRO access** for 7 days. This is intentional — the goal is maximum value delivery so the loss feels real when it expires.

### Day-by-Day Trial Design

**Day 0: Activation (First 10 Minutes)**
- Dashboard loads with their selected county's upcoming auctions
- Guided walkthrough: "Here are 12 properties going to auction this month"
- First ML score visible: "Our AI rates this property as BID — here's why"
- Hook: Show them something they didn't know about a property in their county
- Email: Welcome + Quick Start Guide

**Day 1-2: Discovery Phase**
- User explores auction calendar, property details, ML predictions
- System tracks which properties they view, save, or analyze
- In-app: "You've viewed 8 properties. 2 scored as BID. Want alerts for new ones?"
- Email (Day 1): "Your county has X auctions coming up — here's what our AI found"

**Day 3-4: Intelligence Phase**
- User runs Max Bid Calculator on properties of interest
- BID/REVIEW/SKIP recommendations become part of their workflow
- In-app: "You've calculated max bids for 3 properties. Want to compare?"
- Email (Day 3): "You've analyzed X properties — here's your weekly insight report"
- Push: Behavioral trigger if user hasn't logged in for 24hrs

**Day 5-6: Dependency Phase**
- User has integrated ZoneWise into their research workflow
- Historical data shows patterns they rely on
- In-app: "Trial ending in 48 hours. Here's what you'll lose access to:" + specific list
- Email (Day 5): Countdown + summary of their activity + what they'll lose

**Day 7: Conversion or Loss**
- Trial expires at end of day
- Dashboard transforms: property list visible but ML scores blurred, calculator locked
- In-app: Full-screen upgrade prompt with personalized stats
- Email: "Trial expired. Your data is saved for 30 days. Upgrade to continue."

---

## Post-Trial Free Tier (The Ongoing Tease)

After trial expiration, users don't lose their account. They downgrade to FREE with these carefully designed limitations:

### What FREE Users CAN See
- Foreclosure auction calendar with dates and case numbers
- Property addresses and basic details (beds, baths, sqft)
- Number of properties in upcoming foreclosure auctions
- That ML scores EXIST (blurred numbers with lock icon)
- That Max Bid Calculator EXISTS (grayed out with lock icon)
- That Tax Deed Sales EXIST (locked tab with "Upgrade to PRO for tax deed data")
- Other users' aggregated activity ("47 investors are watching this property")

### What FREE Users CANNOT Do
- View ML prediction scores (blurred)
- Use Max Bid Calculator (locked)
- See BID/REVIEW/SKIP recommendations (hidden)
- Access ANY tax deed sale data (entire section locked — PRO feature)
- Download reports
- Set alerts
- View more than 5 properties/day
- Access more than 1 county

### Design of Locked Elements
Every locked element includes:
1. **Visual indicator** — Lock icon or blur overlay
2. **Specific value hint** — "This property scored 78/100" (but can't see details)
3. **Upgrade CTA** — "Unlock full analysis — $49/month"
4. **Social proof** — "342 PRO users analyzed this property today"

---

## Conversion Psychology

### Loss Aversion > Feature Selling
Don't sell features. Sell the loss of not having them.

**Wrong:** "Upgrade to PRO for ML predictions and Max Bid Calculator"
**Right:** "This property has a 78% third-party purchase probability and a recommended max bid of $142,000. Upgrade to see the full analysis before the auction on March 5th."

### Urgency Mechanics
- Auction dates create natural deadlines
- "This auction is in 3 days. You've analyzed 0 of 15 properties. PRO users have analyzed all 15."
- "Last month, PRO users identified $2.3M in equity opportunities in your county"

### Social Proof Integration
- "127 investors in Brevard County use ZoneWise PRO"
- "This property was flagged as SKIP by our AI — 94% of our correct predictions saved investors an average of $23K"
- Real testimonials from beta users once available

---

## Funnel Metrics & Tracking

### Key Funnel Events to Track
```
1. landing_page_visit
2. registration_started (which path: B2C or B2B)
3. registration_completed
4. first_property_viewed
5. first_ml_score_viewed
6. first_max_bid_calculated
7. third_property_viewed (engagement threshold)
8. trial_day_3_active (still using)
9. trial_day_5_active (likely to convert)
10. trial_expired
11. first_paywall_hit (which feature triggered it)
12. upgrade_clicked
13. payment_completed
14. day_30_retained
15. day_90_retained
```

### Aha Moment Identification
Track which action most strongly correlates with conversion:
- Viewing ML score for a specific property they're considering bidding on?
- Running Max Bid Calculator for the first time?
- Seeing a SKIP recommendation on a property they were interested in?
- Receiving an alert about a new auction in their county?

The action that most strongly predicts conversion becomes the **North Star activation metric** — then optimize the entire onboarding to get every user to that action as fast as possible.

---

## Upgrade Paths

### In-App Upgrade Triggers
1. **Paywall hit** — Any locked feature click → Upgrade modal with relevant context
2. **Usage limit** — 5th property view of the day → "You've hit your daily limit"
3. **Trial countdown** — Banner at top of dashboard during days 5-7
4. **Post-trial dashboard** — Persistent upgrade CTA replacing locked features

### External Upgrade Triggers
1. **Email sequence** — Automated emails tied to trial timeline
2. **Retargeting ads** — Facebook/Google ads to registered non-paying users
3. **Push notifications** — "New auction in your county — upgrade to see ML analysis"
4. **SMS (opt-in)** — Day 7 trial expiry reminder

### Upgrade Friction Removal
- One-click upgrade from any paywall
- Pre-filled payment form (Stripe)
- Monthly billing by default (lower commitment)
- Annual option visible but not pushed initially
- 30-day money-back guarantee to reduce risk perception
