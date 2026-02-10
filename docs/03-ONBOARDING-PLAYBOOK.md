# 03 — Onboarding Playbook: First 7 Days

## Onboarding Philosophy

The trial period has ONE job: get the user to their **Aha Moment** as fast as possible. Everything else is secondary.

**Aha Moment (B2C):** The user sees an ML prediction on a property they care about and realizes this would have taken them hours to figure out manually — or they would have gotten it wrong.

**Aha Moment (B2B):** The firm realizes they can process 10x more properties with higher accuracy than their current manual workflow.

---

## B2C Cloud Onboarding

### First Session (0-10 Minutes)

**Step 1: Personalized Dashboard Load**
User selected their county at registration. Dashboard immediately shows:
- "Welcome to ZoneWise! Here's what's happening in [County Name]"
- Next foreclosure auction date with countdown timer
- Next tax deed sale date with countdown timer
- Number of properties going to auction (both types)
- Top 3 properties by ML score (with full details visible during trial)

**Step 2: Guided First Action**
Interactive tooltip sequence (max 4 steps):
1. "This is your auction calendar. [County] has [X] auctions this month."
2. "Click any property to see our AI analysis."
3. "This ML Score predicts the likelihood of third-party purchase. Higher = more competitive."
4. "Use the Max Bid Calculator to know your safe maximum. Never overbid again."

**Step 3: First Property Deep Dive**
Auto-open the highest-scoring property in their county:
- Full property details (BCPAO data)
- ML prediction with explanation
- BID/REVIEW/SKIP recommendation with reasoning
- Max bid calculation breakdown
- Lien priority analysis
- Neighborhood demographics

**Goal:** User sees the full depth of intelligence on a real property in under 5 minutes.

### Day 1-2 Engagement Hooks

**In-App:**
- Progress bar: "You've explored 3 of 15 auction properties. Keep going!"
- Badge: "First Analysis Complete" (gamification light — not overdone)
- Suggestion: "Based on your activity, you might also want to look at [nearby county]"

**Email (Day 1):**
```
Subject: Your county has [X] auctions coming up

[Name], here's what our AI found in [County]:

• [X] properties going to auction on [date]
• [Y] scored as BID (worth investigating)
• [Z] scored as SKIP (we'd avoid these)

Your trial gives you full access to every analysis.
[View Your Dashboard →]
```

### Day 3-4 Intelligence Hooks

**In-App:**
- "You've analyzed [X] properties this week. Here's your insight summary:"
  - Properties viewed
  - BID opportunities identified
  - Estimated total equity in BID properties
  - Time saved vs manual research (calculated from average)

**Email (Day 3):**
```
Subject: Your first weekly intelligence report

[Name], in 3 days with ZoneWise you've:

✅ Analyzed [X] properties
✅ Found [Y] BID opportunities worth ~$[Z] in potential equity
✅ Saved approximately [N] hours of manual research

You still have 4 days of full access.
[Continue Analyzing →]
```

### Day 5-6 Urgency Hooks

**In-App:**
- Yellow banner: "Your trial ends in [48/24] hours"
- Dashboard shows: "After trial: ML scores hidden, calculator locked, alerts disabled"
- Side-by-side comparison: "PRO vs FREE — here's what changes"

**Email (Day 5):**
```
Subject: 48 hours left — here's what you'll lose

[Name], your ZoneWise trial ends on [date].

After that, you'll lose access to:
🔒 ML predictions on [X] upcoming properties
🔒 Max Bid Calculator
🔒 BID/REVIEW/SKIP recommendations
🔒 Daily alerts for new auctions

Your analysis history is saved for 30 days.
Upgrade now to keep full access.

[Upgrade to PRO — $49/month →]
```

### Day 7 Conversion Point

**In-App:**
- Full-screen modal on login:
  ```
  Your trial has ended.

  In 7 days, you:
  • Analyzed [X] properties
  • Found [Y] BID opportunities
  • Saved ~[N] hours of research

  Keep your edge. Upgrade to PRO.

  [$49/month — Upgrade Now]
  [Continue with Free — Limited Access]
  ```

- If they choose Free: Dashboard loads with locked elements visible
- Every locked element is a conversion opportunity

---

## B2B Desktop Onboarding

### Pre-Installation (Demo Call)

**Demo Structure (30 minutes):**
1. (5 min) Understand their current workflow and pain points
2. (10 min) Live walkthrough of desktop app with their county's real data
3. (5 min) Show ML predictions vs a property they recently worked on
4. (5 min) Show enterprise features: white-label reports, multi-seat, bulk export
5. (5 min) Pricing, trial offer, next steps

**Post-Demo:**
- Send desktop download link + license key (14-day trial)
- Send installation guide PDF
- Schedule Day 3 check-in call

### Installation & First Session

**Installer includes:**
- One-click setup (no technical knowledge required)
- Auto-configures for their selected counties
- Pre-loads upcoming auction data
- Walks through connecting to their existing workflow

**First session guided tour:**
1. "Here's your dashboard — all [County] auctions in one place"
2. "Click a property for full lien analysis — no manual title search needed"
3. "Generate a white-label report for your client in one click"
4. "Set up alerts so your team never misses a new filing"

### Day 3 Check-In Call

**Agenda:**
- Are they using it? If not, troubleshoot immediately
- Have they shown it to their team? If not, help them demo internally
- Any integration questions? (CRM, case management)
- Reinforce value: "How long would this property analysis have taken manually?"

### Day 7 Mid-Trial Check

**Email with usage report:**
- Properties analyzed by their team
- Reports generated
- Time saved estimate
- "Your team is on track. Full pricing details for continued access below."

### Day 12 Closing Conversation

**Call or email:**
- Trial ends in 2 days
- Pricing proposal with annual discount option
- Ask: "What would make this a yes today?"
- Offer: First month free if they commit to annual before trial expires

---

## Onboarding Failure Recovery

### If User Doesn't Log In After Registration (Day 1-3)

**Day 1 (no login):**
```
Subject: Your ZoneWise dashboard is ready

[Name], you registered but haven't logged in yet.

There are [X] properties going to auction in [County] this month.
Our AI has already analyzed them for you.

[See Your Dashboard →]
```

**Day 3 (still no login):**
```
Subject: [X] auctions in [County] — are you missing them?

[Name], [County] has [X] properties going to auction on [date].

[Y] of them scored as potential BID opportunities.
Your 7-day trial is running — don't waste it.

[Log In Now →]
```

**Day 5 (still no login):**
```
Subject: Your trial expires in 2 days (unused)

[Name], your ZoneWise trial is almost over and you haven't used it.

Want to restart your trial? Reply "restart" and we'll give you
a fresh 7 days starting from your next login.

[Restart My Trial →]
```

### If User Logs In Once Then Disappears

**Day 3 (single session):**
```
Subject: You left off at [last property viewed]

[Name], you looked at [Property Address] on [date].

Since then, [X] new properties have been added to [County] auctions.
Our AI scored [Y] of them as BID opportunities.

[Pick Up Where You Left Off →]
```

### If User Is Active But Doesn't Convert at Day 7

This user WANTS the product but hasn't committed. They need a push:

**Day 8:**
```
Subject: Your ML scores are now hidden — but your data is safe

[Name], your trial expired yesterday.

Your 30-day data history is still saved.
Upgrade anytime to instantly restore full access.

As a trial user, here's a special offer:
First month at 50% off — $24.50 instead of $49.

[Claim Your Discount →]
(Offer expires in 72 hours)
```

---

## Onboarding Metrics

| Metric | Target | Action If Below |
|--------|--------|-----------------|
| Day 0 activation (view 1 property) | > 80% | Simplify dashboard, add auto-open |
| Day 1 return rate | > 60% | Improve Day 1 email hook |
| Day 3 still active | > 40% | Add in-app engagement triggers |
| Properties analyzed during trial | > 5 avg | Improve property discovery UX |
| Max Bid Calculator used | > 30% | Make calculator more prominent |
| Trial → Paid conversion | > 8% (B2C) | Test paywall messaging and pricing |
| Trial → Paid conversion | > 20% (B2B) | Improve demo and follow-up process |
