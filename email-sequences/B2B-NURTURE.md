# B2B Enterprise Nurture Sequence

## Sequence Overview
- **Trigger:** User completes B2B registration (company path)
- **Duration:** 21 days
- **Emails:** 6 emails + demo scheduling
- **Goal:** Demo → Desktop Trial → Enterprise subscription
- **Sender:** "Ariel Shapira" <ariel@zonewise.ai>

---

## Email 1: Immediate — Demo Confirmation

**Subject:** Demo scheduled — what to expect
**If demo scheduled:**
```
{{first_name}},

Great — you're booked for {{demo_date}} at {{demo_time}} EST.

Here's what we'll cover in 30 minutes:
1. Your current foreclosure workflow and pain points
2. Live walkthrough with real {{county}} auction data
3. AI predictions vs your recent experience
4. Enterprise features: white-label reports, multi-seat, API
5. Pricing and trial setup

I'll pull data for {{county}} specifically so you see
exactly what the platform does for your market.

Calendar invite attached. See you then.

— Ariel Shapira
Founder, ZoneWise.AI / Everest Capital USA
```

**If demo NOT yet scheduled:**
```
{{first_name}},

Thanks for your interest in ZoneWise for {{company_name}}.

I'd love to show you how our AI analyzes foreclosure auctions
and how the desktop application fits into your workflow.

Quick 30-minute demo — I'll use real data from your county.

[Schedule Your Demo →]

In the meantime, here's a 2-minute overview:
{{link_to_product_video}}

— Ariel Shapira
```

---

## Email 2: Day 2 — Pre-Demo Prep (if demo scheduled)

**Subject:** Before our demo: a quick question
**Preview:** This helps me customize the walkthrough

```
{{first_name}},

Quick question before {{demo_date}}:

What's the biggest headache in your current foreclosure
analysis workflow? Pick one:

A) Manual title searches take too long
B) Missing liens or issues that surface after the auction
C) No way to predict auction outcomes
D) Generating reports for clients is tedious
E) Something else (just reply)

This helps me focus the demo on what matters to you.

— Ariel
```

**Notes:**
- Reply creates engagement and provides sales intelligence
- Single-question email = high response rate

---

## Email 3: Day 3 — Post-Demo Follow-Up (if demo completed)

**Subject:** Your ZoneWise desktop trial is ready
**Preview:** 14-day full access — installation takes 5 minutes

```
{{first_name}},

Thanks for the demo today. Here's everything to get started:

📥 Desktop Download: {{download_link}}
🔑 License Key: {{license_key}}
📖 Installation Guide: {{guide_link}}
⏰ Trial: 14 days full Enterprise access

Quick start:
1. Download and install (5 minutes)
2. Enter your license key
3. Select your counties
4. Start analyzing — your data loads automatically

I'll check in on Day 3 to see how it's going.

Any issues? Reply to this email or call me at {{phone}}.

— Ariel
```

---

## Email 4: Day 6 — Trial Check-In

**Subject:** How's the first week going?
**Preview:** Your team has analyzed {{count}} properties so far

```
{{first_name}},

Your team's first week with ZoneWise Desktop:

• Properties analyzed: {{count}}
• Reports generated: {{report_count}}
• Users active: {{active_users}} of {{total_seats}}

Quick questions:
1. Is the team using it? If not, I can help with internal rollout.
2. Any integration needs? (CRM, case management, etc.)
3. Anything broken or confusing?

Happy to jump on a 15-minute call if easier.

[Schedule Quick Check-In →]

— Ariel
```

---

## Email 5: Day 12 — Pre-Expiry Pricing

**Subject:** Your trial ends in 2 days — let's talk next steps
**Preview:** Pricing details + annual discount inside

```
{{first_name}},

Your ZoneWise Desktop trial ends on {{expiry_date}}.

Here's what Enterprise looks like:

Monthly: $299/month
  • All 67 Florida counties
  • 5 user seats included
  • White-label reports
  • API access
  • Priority support

Annual: $2,990/year (2 months free)
  • Everything above
  • Locked-in pricing for 12 months
  • Priority feature requests

Special: Commit to annual before your trial ends and
I'll add 2 extra seats (7 total) at no extra cost.

Want to discuss? Reply or grab time on my calendar.

[Schedule Call →]

— Ariel
```

---

## Email 6: Day 21 — Final Follow-Up (if not converted)

**Subject:** Still thinking about ZoneWise?
**Preview:** No pressure — just wanted to check in

```
{{first_name}},

Your trial ended {{days_ago}} days ago. Wanted to check in
one last time.

If the timing isn't right, no worries. A few options:

1. **Budget issue?** I can work with you on pricing.
2. **Need more time?** I'll extend your trial 7 days.
3. **Not the right fit?** Tell me why — it helps us improve.
4. **Ready to go?** [Activate Enterprise →]

Either way, I appreciate you trying ZoneWise.

— Ariel
```

---

## Sequence Automation Rules

1. All emails suppressed immediately on Enterprise subscription
2. Demo scheduling uses Calendly or Cal.com integration
3. Post-demo emails only trigger if demo was marked "completed"
4. Usage data pulled from Supabase at send time
5. All replies go to Ariel's real inbox
6. Follow-up calls logged in Supabase for tracking
7. If no demo scheduled after 7 days, user enters low-touch drip (monthly newsletter)
