# 05 — Retention Strategy: Reducing Churn & Building Stickiness

## Churn Risk by Segment

| Segment | Monthly Churn Target | Primary Churn Risk | Mitigation |
|---------|---------------------|-------------------|------------|
| B2C PRO | < 8% | "No auction this month in my county" | Multi-county access, content between auctions |
| B2B Enterprise | < 3% | Champion leaves the company | Multi-seat, workflow integration |
| B2C Free → PRO converts | < 12% (first 90 days) | Didn't see enough value in month 1 | Aggressive onboarding, early wins |

---

## Stickiness Mechanics

### 1. Data Accumulation (Both Channels)
The longer they use ZoneWise, the more valuable their account becomes:
- **Saved properties** — their watchlist grows
- **Analysis history** — past auction results linked to ML predictions
- **Performance tracking** — "Your BID accuracy over 6 months: 73%"
- **Custom settings** — county preferences, alert filters, saved searches
- **Notes and annotations** — personal notes on properties

**Switching cost:** Leaving means losing all of this. No competitor has their history.

### 2. Desktop Installation (B2B)
Desktop-specific stickiness factors:
- Local data cache (works offline)
- IT approval already obtained (re-approval for new tool = painful)
- Staff trained on the interface
- Integrated into daily workflow
- Custom configurations per user

**Switching cost:** Uninstalling, re-training staff, getting IT to approve a replacement.

### 3. Workflow Integration (B2B)
- Report templates customized to their branding
- CRM integration configured
- Alert schedules matching their team's workflow
- Data exports feeding their existing systems

**Switching cost:** Rebuilding all integrations from scratch.

### 4. ML Learning Loop (Both)
The system gets smarter about THEIR preferences:
- Counties they care about
- Property types they analyze most
- Price ranges they target
- Bid patterns and outcomes

"ZoneWise learns your investment style. The longer you use it, the better it gets at finding YOUR deals."

---

## Monthly Value Reinforcement

### Weekly Intelligence Report (PRO + Enterprise)
Every Monday morning, paid users receive:
```
Subject: Your Weekly ZoneWise Intelligence Report — [County]

This week in [County]:
• [X] new foreclosure filings
• [Y] upcoming auctions
• [Z] properties scored as BID
• Top opportunity: [Address] — Score: [X]/100, Est. equity: $[Y]

Your activity:
• Properties analyzed: [N]
• Auctions tracked: [N]
• Reports generated: [N]

[View Full Report in Dashboard →]
```

This email serves two purposes:
1. Reminds them the product exists and is working for them
2. Delivers value even if they haven't logged in

### Monthly ROI Summary (PRO + Enterprise)
End of each month:
```
Subject: Your ZoneWise ROI This Month

[Name], here's your October summary:

📊 Properties analyzed: 47
🎯 BID recommendations: 8
⚠️ SKIP warnings: 12
⏱️ Estimated time saved: 23 hours
💰 Total equity in BID properties: $412,000

Your ZoneWise investment: $49
Your potential return: $412,000 in identified opportunities

[View Full Monthly Report →]
```

### Quarterly Business Review (Enterprise Only)
Scheduled call with Enterprise accounts:
- Review usage metrics
- Gather feedback
- Discuss upcoming features
- Identify expansion opportunities (more seats, more counties)
- Proactively solve problems before they become churn reasons

---

## Churn Prevention Triggers

### Early Warning: Usage Drop
**Trigger:** User's weekly logins drop by 50%+ vs previous 4-week average
**Action (Week 1):** In-app: "We miss you! Here are [X] new properties in [County] since your last visit."
**Action (Week 2):** Email: "Your county has [X] upcoming auctions. Don't miss these opportunities."
**Action (Week 3):** Email from "founder": Personal note asking if everything is okay + offer to help

### Early Warning: Feature Disengagement
**Trigger:** User stops using a key feature they previously used regularly
**Action:** In-app tooltip: "You haven't used [feature] in 2 weeks. Need help?" + link to guide

### Cancellation Intercept
**Trigger:** User clicks "Cancel Subscription"
**Step 1: Survey** — "We're sorry to see you go. What's the main reason?"
  - Too expensive
  - Not enough auctions in my area
  - Too complicated
  - Found a better alternative
  - No longer investing in foreclosures
  - Other

**Step 2: Tailored Save Offer based on reason:**
- **Too expensive:** "Would $29/month work? We can offer that for the next 3 months."
- **Not enough auctions:** "We're expanding to [X] more counties next month. Stay for 1 more month free?"
- **Too complicated:** "Our team can walk you through the platform. [Schedule a free session]"
- **Found alternative:** "We'd love to understand what they offer that we don't. [Quick feedback form]"
- **No longer investing:** "We'll pause your account. Your data stays for 6 months. Resume anytime."

**Step 3: If they still cancel:**
- Confirm cancellation gracefully
- "Your account and data are saved for 90 days. Come back anytime."
- Add to win-back email sequence (triggers at 30, 60, 90 days)

---

## Win-Back Campaigns

### 30-Day Win-Back
```
Subject: [X] properties you would have seen this month

[Name], since you left ZoneWise:

• [County] had [X] new foreclosure filings
• [Y] went to auction
• Our AI identified [Z] BID opportunities

Your data is still saved. Pick up where you left off.

[Reactivate — First Month Free]
```

### 60-Day Win-Back
```
Subject: We've added [new feature] since you left

[Name], here's what's new at ZoneWise:

• [New feature/improvement]
• [X] more counties now available
• [Performance improvement]

Come back and try it — 14-day free trial of everything new.

[Restart Free Trial]
```

### 90-Day Win-Back (Final)
```
Subject: Your ZoneWise data expires in 7 days

[Name], your saved properties, analysis history, and
settings will be permanently deleted on [date].

If you ever want to return, reactivate now to
preserve your data.

[Reactivate Account]
[Delete My Data]
```

---

## Feature Gating for Retention

### PRO-Only Features Released Quarterly
Keep PRO users engaged by adding value they can't get elsewhere:
- Q1: Comparative auction analysis (this property vs similar past sales)
- Q2: Investment portfolio tracker (aggregate ROI across all bids)
- Q3: Market trend reports (county-level foreclosure trends)
- Q4: AI-powered property condition estimates from photos

Each new feature is:
1. Announced to PRO users first ("exclusive early access")
2. Shown to Free users as locked (another conversion trigger)
3. Highlighted in the monthly ROI email

### Enterprise-Only Features
- Custom API endpoints
- Dedicated account manager
- Custom ML model training on their historical data
- White-glove onboarding for new team members
- Priority feature requests

---

## Retention Metrics Dashboard

Track weekly:
| Metric | B2C Target | B2B Target |
|--------|-----------|-----------|
| DAU/MAU ratio | > 30% | > 50% |
| Weekly active users | > 60% of paid | > 80% of paid |
| Features used per session | > 3 | > 5 |
| Reports generated/month | > 2 per user | > 10 per user |
| NPS score | > 40 | > 50 |
| Month 3 retention | > 70% | > 85% |
| Month 12 retention | > 40% | > 70% |
| Expansion revenue (upsell) | 5% MRR growth | 10% MRR growth |
