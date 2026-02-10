# Trial Onboarding Email Sequence (B2C — 7 Days)

## Sequence Overview
- **Trigger:** User completes B2C registration
- **Duration:** 7 days (trial period)
- **Emails:** 6 emails
- **Goal:** Drive activation, engagement, and conversion
- **Sender:** "Ariel from ZoneWise" <ariel@zonewise.ai>
- **Platform:** Resend or Postmark (transactional)

---

## Email 1: Welcome (Immediate — Day 0)

**Subject:** Your ZoneWise trial is live — here's what to do first
**Preview:** {{county}} has {{count}} properties going to auction this month

```
Hey {{first_name}},

You're in. Your 7-day full access trial starts now.

Here's what's waiting for you in {{county}}:
• {{auction_count}} properties going to auction this month
• {{bid_count}} scored as BID by our AI
• Next auction date: {{next_auction_date}}

Your first step: Open your dashboard and click on any property
to see the full AI analysis — ML prediction, lien analysis,
max bid calculation, everything.

[Open Your Dashboard →]

You have 7 days of unrestricted access to every feature.
Make it count.

— Ariel
Founder, ZoneWise.AI
```

**Notes:**
- Dynamic variables pulled from Supabase at send time
- County-specific data makes it immediately relevant
- Clear single action: open dashboard

---

## Email 2: First Insight (Day 1)

**Trigger:** Sent Day 1, only if user has NOT logged in since registration
**If user HAS logged in:** Skip this email

**Subject:** {{county}} auctions this month — our AI found something
**Preview:** {{bid_count}} properties worth investigating

```
{{first_name}},

You registered yesterday but haven't checked your dashboard yet.

Quick update: Our AI just finished analyzing {{auction_count}}
properties in {{county}} for upcoming auctions.

Here's one that stood out:

📍 {{top_property_address}}
   Auction: {{auction_date}}
   Judgment: ${{judgment_amount}}
   AI Score: High (full details on your dashboard)

Your trial is running whether you use it or not.
6 days left.

[See Full Analysis →]

— Ariel
```

**Notes:**
- Only for non-activated users (activation = first property view)
- Shows specific property to create curiosity
- Urgency: trial is counting down

---

## Email 3: Intelligence Report (Day 3)

**Subject:** Your 3-day ZoneWise report
**Preview:** You've analyzed {{properties_viewed}} properties so far

**Variant A: Active User (3+ properties viewed)**
```
{{first_name}},

3 days in. Here's your activity:

📊 Properties analyzed: {{properties_viewed}}
🎯 BID opportunities found: {{bid_count}}
⚠️ SKIP warnings: {{skip_count}}
⏱️ Est. time saved: {{hours_saved}} hours

The AI keeps working. New filings are added daily.
4 days left on your trial.

[View Latest Properties →]

— Ariel
```

**Variant B: Low Activity (0-2 properties viewed)**
```
{{first_name}},

Your trial is half over and you've only viewed
{{properties_viewed}} properties.

{{county}} has {{total_available}} properties in the pipeline
right now. Investors who use ZoneWise daily catch opportunities
others miss.

Here's what you're missing:
• {{new_filings}} new filings since you registered
• {{upcoming_auctions}} auctions in the next 30 days

[Explore Now — 4 Days Left →]

— Ariel
```

---

## Email 4: Countdown Warning (Day 5)

**Subject:** 48 hours left on your trial
**Preview:** Here's exactly what changes when it expires

```
{{first_name}},

Your ZoneWise trial expires on {{expiry_date}}.

After that, your account downgrades to Free:

What stays:
✅ Auction calendar (dates and case numbers)
✅ Basic property details
✅ 5 property views per day
✅ {{county}} only

What you lose:
🔒 ML predictions and AI scores
🔒 Max Bid Calculator
🔒 BID/REVIEW/SKIP recommendations
🔒 Report downloads
🔒 Daily alerts
🔒 Multi-county access

Your analysis history is saved for 30 days.
Upgrade now to keep everything.

[Upgrade to PRO — $49/month →]

No contract. Cancel anytime.

— Ariel
```

---

## Email 5: Final Day (Day 7 — Morning)

**Subject:** Last day: your ML scores go dark tonight
**Preview:** {{active_auctions}} auctions coming up — will you be ready?

```
{{first_name}},

This is it. Your trial ends tonight at midnight.

Since signing up, you've:
• Viewed {{properties_viewed}} properties
• Found {{bid_count}} BID opportunities
• Calculated {{max_bids_used}} max bids

Tomorrow, those ML scores disappear. The max bid calculator
locks. The BID/REVIEW/SKIP labels vanish.

{{county}} has {{active_auctions}} auctions in the next 30 days.
Your competitors will have this intelligence. Will you?

[Keep Full Access — $49/month →]

— Ariel
```

---

## Email 6: Trial Expired (Day 8 — Morning)

**Subject:** Trial over — your data is saved
**Preview:** Upgrade anytime to pick up where you left off

```
{{first_name}},

Your trial ended last night. Your account is now on the Free plan.

Everything you analyzed is saved for 30 days.
Upgrade anytime to restore full access instantly.

Quick reminder of what PRO gives you:
• AI predictions on every property
• Max Bid Calculator
• 5 counties instead of 1
• Daily alerts and report downloads
• Unlimited property views

$49/month. One good decision pays for a decade of ZoneWise.

[Upgrade to PRO →]

— Ariel

P.S. If $49/month doesn't work right now, reply to this email.
I'll see what I can do.
```

**Notes:**
- The P.S. invites negotiation — captures price-sensitive leads
- Responses go to Ariel's inbox for personal follow-up
- This opens the door to the trial-expired win-back sequence

---

## Sequence Automation Rules

1. All emails suppressed if user upgrades to paid (any point in sequence)
2. Email 2 skipped if user activated on Day 0
3. Email 3 has two variants based on engagement level
4. All emails include unsubscribe link (CAN-SPAM compliance)
5. Send time: 8:00 AM in user's timezone (default EST)
6. From: ariel@zonewise.ai with "Ariel from ZoneWise" display name
7. Reply-to: ariel@zonewise.ai (real inbox, not no-reply)
