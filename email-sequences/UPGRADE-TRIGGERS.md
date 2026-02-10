# Behavior-Triggered Upgrade Emails

## Overview
These emails fire based on specific user actions, NOT a time-based schedule. They supplement the trial sequence by targeting moments of peak intent.

---

## Trigger 1: Repeated Paywall Hits

**Condition:** Free user hits 3+ paywalls in a single session
**Delay:** 2 hours after session ends
**Subject:** You hit the wall {{paywall_count}} times today
**Preview:** Here's what you were trying to see

```
{{first_name}},

You tried to access locked features {{paywall_count}} times today.

Here's what was behind those locks:

{{#each paywall_hits}}
• {{property_address}}: {{locked_feature}} {{teaser_value}}
{{/each}}

You clearly need this information. $49/month unlocks everything.

[Upgrade to PRO →]

— Ariel
```

**Notes:** Maximum 1 per week to avoid spam feel.

---

## Trigger 2: Auction Eve (Properties Viewed)

**Condition:** Free user viewed properties for an auction happening tomorrow
**Timing:** 6:00 PM the evening before auction
**Subject:** Tomorrow's auction — are you going in blind?
**Preview:** {{auction_count}} properties, 0 AI analysis

```
{{first_name}},

{{county}} auction is tomorrow at {{auction_time}}.

You viewed {{viewed_count}} of {{total_count}} properties
but couldn't see any ML predictions or max bid calculations.

PRO users going to this auction have:
✅ AI scores on every property
✅ Max bid calculations ready
✅ BID/REVIEW/SKIP recommendations
✅ Full lien analysis

You have: property addresses.

There's still time.

[Upgrade Now — Be Ready Tomorrow →]

— Ariel
```

---

## Trigger 3: Post-Auction Results

**Condition:** Auction results published for properties the free user viewed
**Timing:** 24 hours after auction results are recorded
**Subject:** Yesterday's auction results — our AI called it
**Preview:** See how the predictions matched reality

```
{{first_name}},

Yesterday's {{county}} auction results are in.

{{#if correct_predictions}}
Our AI correctly predicted:
{{#each correct_predictions}}
• {{property_address}}: Predicted {{prediction}}, Result: {{result}}
{{/each}}
{{/if}}

You viewed {{viewed_count}} of these properties but couldn't
see the predictions.

Next auction: {{next_auction_date}}.
Will you be ready this time?

[Upgrade to PRO — $49/month →]

— Ariel
```

**Notes:** Only sends if we have verified correct predictions to show. Never send with inaccurate data.

---

## Trigger 4: Daily Limit Reached (Repeated)

**Condition:** Free user hits daily 5-property limit for 3rd time in a week
**Timing:** Immediately after 3rd limit hit
**Subject:** You've maxed out 3 times this week
**Preview:** Unlimited access is $49/month

```
{{first_name}},

This is the 3rd time this week you've hit the 5-property
daily limit. You're clearly doing serious research.

At 5 properties per day, it would take you {{days_needed}} days
to review all {{total_available}} properties in {{county}}.

PRO users see everything, instantly, with AI analysis.

$49/month. Unlimited properties. Full AI predictions.

[Remove the Limits →]

— Ariel
```

---

## Trigger 5: County Expansion Attempt

**Condition:** Free user tries to access a second county
**Timing:** Immediately (in-app + email within 1 hour)
**Subject:** Expanding beyond {{home_county}}? Good move.
**Preview:** PRO covers 5 counties for $49/month

```
{{first_name}},

You tried to access {{requested_county}} — smart.

Multi-county investors consistently find better deals because
they're not limited to one market.

{{requested_county}} has:
• {{auction_count}} upcoming auctions
• {{bid_count}} properties our AI scored as BID
• Average judgment: ${{avg_judgment}}

PRO gives you 5 counties. Enterprise gives you all 67.

[Upgrade to PRO — $49/month →]

— Ariel
```

---

## Trigger 6: High-Value Property View

**Condition:** Free user views a property with estimated equity > $50K
**Timing:** Immediately (in-app notification + email within 30 min)
**Subject:** That property at {{address}} — there's more to know
**Preview:** Our AI has a detailed analysis ready

```
{{first_name}},

You just looked at {{property_address}}.

There's more to this property than what you can see on Free:
• ML prediction score: [locked]
• Max bid calculation: [locked]
• Lien priority analysis: [locked]
• BID/REVIEW/SKIP recommendation: [locked]

This property has an estimated judgment of ${{judgment}}.
At these stakes, you want the full picture.

[See Full Analysis — Upgrade to PRO →]

— Ariel
```

---

## Trigger 7: PRO → Enterprise Upsell

**Condition:** PRO user accesses 4+ counties regularly OR generates 10+ reports/month
**Timing:** End of billing month
**Subject:** You're outgrowing PRO
**Preview:** Enterprise might be a better fit

```
{{first_name}},

Your usage this month:
• Counties accessed: {{county_count}} (PRO limit: 5)
• Reports generated: {{report_count}}
• Properties analyzed: {{property_count}}

You're a power user. Enterprise would give you:
• All 67 Florida counties (not just 5)
• Desktop app for faster workflows
• White-label reports with your branding
• API access for custom integrations
• Bulk export

$299/month — and if you're a company, it's a business expense.

Want to see a demo of Enterprise features?

[Schedule Enterprise Demo →]

— Ariel
```

---

## Global Email Rules

1. **Frequency cap:** Max 2 triggered emails per user per week (across all triggers)
2. **Suppression:** All triggers suppressed for 48 hours after any upgrade email
3. **Paid users:** Never receive upgrade triggers (auto-suppressed)
4. **Unsubscribe:** Every email includes one-click unsubscribe
5. **Tracking:** Every email logs to Supabase: trigger_type, user_id, sent_at, opened, clicked, converted
6. **A/B testing:** Subject lines tested in cohorts of 100+ before full rollout
