# Trial Expired — Win-Back Email Sequence

## Sequence Overview
- **Trigger:** User's trial expired AND they did NOT upgrade
- **Duration:** 90 days post-expiry
- **Emails:** 5 emails
- **Goal:** Reactivate lapsed trial users
- **Sender:** "Ariel from ZoneWise" <ariel@zonewise.ai>

---

## Email 1: 7 Days Post-Expiry

**Subject:** {{county}} had {{auction_count}} auctions since your trial ended
**Preview:** Here's what our AI found

```
{{first_name}},

It's been a week since your ZoneWise trial ended.

Since then, {{county}} had {{auction_count}} properties go to
auction. Our AI analyzed all of them:

• {{bid_count}} scored as BID
• {{skip_count}} scored as SKIP
• {{total_equity}} in estimated equity across BID properties

You missed all of it.

Your data is still saved. Upgrade to pick up where you left off.

[Upgrade to PRO — $49/month →]

— Ariel
```

---

## Email 2: 14 Days Post-Expiry (Discount Offer)

**Subject:** 50% off your first month — limited time
**Preview:** $24.50 instead of $49

```
{{first_name}},

I noticed you didn't upgrade after your trial. Wanted to
make this easier.

Here's a one-time offer: First month of PRO at 50% off.
That's $24.50 for full access to everything.

• AI predictions on every {{county}} property
• Max Bid Calculator
• BID/REVIEW/SKIP recommendations
• Daily alerts
• Report downloads

[Claim 50% Off — $24.50 →]

This link expires in 72 hours.

— Ariel
```

**Notes:**
- Discount link auto-expires (Stripe coupon with expiry)
- Creates urgency without being pushy

---

## Email 3: 30 Days Post-Expiry (Data Warning)

**Subject:** Your ZoneWise data expires in 7 days
**Preview:** Analysis history, saved properties — gone in 7 days

```
{{first_name}},

Your ZoneWise account data — saved properties, analysis
history, custom settings — will be permanently deleted
on {{deletion_date}}.

This includes:
• {{properties_viewed}} properties you analyzed
• {{saved_count}} properties you saved
• All your Max Bid calculations
• Your alert preferences

If you want to keep this data, upgrade before {{deletion_date}}.
If not, no action needed — we'll clean it up automatically.

[Upgrade & Keep My Data →]
[Delete My Data Now →]

— Ariel
```

---

## Email 4: 60 Days Post-Expiry (New Feature)

**Subject:** New: {{new_feature_name}} — want to try it?
**Preview:** Free 7-day trial restart

```
{{first_name}},

We've been building since you left. Here's what's new:

🆕 {{new_feature_name}}: {{one_line_description}}
🆕 {{improvement}}: {{one_line_description}}
📊 Now covering {{county_count}} Florida counties

Want to see it? I'll restart your trial — 7 more days,
no commitment.

[Restart My Free Trial →]

— Ariel
```

**Notes:**
- This email only sends if there IS a new feature to highlight
- Trial restart is a proven reactivation tactic

---

## Email 5: 90 Days Post-Expiry (Final)

**Subject:** Last check-in from ZoneWise
**Preview:** Unsubscribing you from updates unless you want to stay

```
{{first_name}},

This is my last email. I don't want to clutter your inbox.

If you're still interested in foreclosure investing and
want to hear from us when we launch something big,
click below to stay on the list.

[Keep Me Updated →]

Otherwise, I'll remove you from our emails. No hard feelings.

If you ever want to come back, zonewise.ai is always there.

— Ariel
```

**Notes:**
- Respectful close — builds goodwill
- "Keep Me Updated" moves them to a low-frequency newsletter list
- No response = auto-unsubscribe after 14 days
