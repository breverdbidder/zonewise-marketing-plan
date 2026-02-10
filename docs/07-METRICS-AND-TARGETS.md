# 07 — Metrics & Targets: KPIs, Conversion Ratios, Revenue Model

## North Star Metric

**Monthly Recurring Revenue (MRR)**

Everything else is a leading indicator to MRR growth.

---

## Funnel Metrics

### Acquisition Funnel

```
Website Visitors
    │ (target: 5,000/month by month 6)
    ▼
Landing Page → Registration: 15-25% conversion
    │ (target: 750-1,250 registrations/month)
    ▼
Registration → Activation (view 1st property): 80%+
    │ (target: 600-1,000 activated users/month)
    ▼
Activation → Trial Engagement (3+ properties): 50%
    │ (target: 300-500 engaged trial users/month)
    ▼
Trial → Paid Conversion: 8-12% (B2C) / 20-30% (B2B)
    │ (target: 40-80 new paid users/month)
    ▼
Paid User → Month 3 Retained: 70% (B2C) / 85% (B2B)
    │
    ▼
Paid User → Month 12 Retained: 40% (B2C) / 70% (B2B)
```

### Key Conversion Benchmarks

| Stage | B2C Target | B2B Target | Industry Avg |
|-------|-----------|-----------|--------------|
| Visit → Register | 15-25% | 5-10% (demo request) | 2-5% |
| Register → Activate | > 80% | > 90% | 40-60% |
| Activate → Engaged | > 50% | > 70% | 20-40% |
| Trial → Paid | 8-12% | 20-30% | 3-8% (freemium) |
| Month 1 → Month 3 | 70% | 85% | 60-70% |
| Month 1 → Month 12 | 40% | 70% | 25-35% |

Our targets are above industry average because of the natural urgency of auction deadlines — users have external pressure to keep using the tool.

---

## Revenue Model

### Unit Economics

| Metric | B2C PRO | B2B Enterprise |
|--------|---------|---------------|
| ARPU (Monthly) | $49 | $299 |
| CAC | < $50 | < $500 |
| Payback Period | 1 month | 1.7 months |
| Gross Margin | > 85% | > 80% |
| Monthly Churn | < 8% | < 3% |
| Average Lifetime | 8-12 months | 24-36 months |
| LTV | $390-590 | $7,200-10,800 |
| LTV:CAC Ratio | 8-12x | 14-22x |

### MRR Growth Model (12-Month Projection)

**Conservative:**
| Month | New B2C | New B2B | Churned | Net New | Total Paid | MRR |
|-------|---------|---------|---------|---------|-----------|------|
| 1 | 20 | 2 | 0 | 22 | 22 | $1,578 |
| 2 | 25 | 3 | 2 | 26 | 48 | $3,249 |
| 3 | 30 | 3 | 4 | 29 | 77 | $5,120 |
| 4 | 35 | 4 | 6 | 33 | 110 | $7,286 |
| 5 | 40 | 5 | 8 | 37 | 147 | $9,748 |
| 6 | 50 | 5 | 10 | 45 | 192 | $12,813 |
| 7 | 50 | 6 | 12 | 44 | 236 | $15,558 |
| 8 | 55 | 7 | 14 | 48 | 284 | $18,759 |
| 9 | 60 | 7 | 16 | 51 | 335 | $22,134 |
| 10 | 65 | 8 | 18 | 55 | 390 | $25,779 |
| 11 | 70 | 8 | 20 | 58 | 448 | $29,716 |
| 12 | 75 | 10 | 22 | 63 | 511 | $34,007 |

**Year 1 ARR (Conservative): ~$408K**

### Cost Structure

| Cost Category | Monthly | Notes |
|-------------|---------|-------|
| Supabase | $25 | Pro plan |
| Render | $50-100 | Backend hosting (scales with traffic) |
| Cloudflare | $20 | Pages + Workers |
| LLM API (LiteLLM) | $100 | Smart Router with DeepSeek |
| AgentQL | $50 | Scraping API |
| Domain + DNS | $5 | Annual amortized |
| Email (Resend/Postmark) | $20 | Transactional emails |
| Analytics | $10 | Plausible/PostHog |
| Stripe fees | 2.9% + $0.30 | Per transaction |
| **Total Fixed** | **~$280-330/month** | |
| **Break-even** | **~7 paid users** | Mixed B2C+B2B |

---

## Engagement Metrics

### Daily Active Users (DAU)
| Segment | Target DAU/MAU |
|---------|---------------|
| Free | > 10% |
| PRO | > 30% |
| Enterprise | > 50% |

### Feature Adoption (Paid Users)
| Feature | Target Monthly Usage |
|---------|---------------------|
| Property view | > 95% of users |
| ML score check | > 80% of users |
| Max Bid Calculator | > 60% of users |
| Report download | > 40% of users |
| Alert setup | > 50% of users |
| Multi-county browse | > 30% of users |

### Session Metrics
| Metric | Target |
|--------|--------|
| Avg session duration | > 8 minutes |
| Properties viewed per session | > 4 |
| Sessions per week (paid) | > 3 |
| Return within 7 days | > 70% (paid) |

---

## Marketing Channel Metrics

### SEO (Organic)
| Metric | Month 3 | Month 6 | Month 12 |
|--------|---------|---------|----------|
| Organic visitors/month | 500 | 2,000 | 5,000 |
| Ranking keywords | 50 | 200 | 500 |
| Domain authority | 15 | 25 | 35 |
| Organic registrations | 50 | 200 | 500 |

### Paid Acquisition (Google Ads)
| Metric | Target |
|--------|--------|
| CPC (foreclosure keywords) | $2-5 |
| Click → Register | 15-25% |
| Register → Paid | 8-12% |
| CPA (paid user) | < $50 |
| Monthly ad budget | $500-1,000 |
| ROAS target | > 3x |

### Direct Outreach (B2B)
| Metric | Target |
|--------|--------|
| LinkedIn messages/week | 50 |
| Response rate | > 10% |
| Response → Demo | > 30% |
| Demo → Trial | > 50% |
| Trial → Paid | > 25% |
| Monthly B2B deals | 3-5 |

---

## Reporting Cadence

**Daily:** MRR, new registrations, trial starts, conversions (automated dashboard)
**Weekly:** Funnel analysis, churn events, feature adoption, support tickets
**Monthly:** Revenue report, cohort retention analysis, channel ROI, cost analysis
**Quarterly:** Business review, pricing evaluation, competitive analysis, roadmap alignment

---

## Data Infrastructure

All metrics tracked in Supabase tables:
- `user_events` — funnel events (registration, activation, conversion, churn)
- `subscription_metrics` — MRR, ARPU, LTV calculations
- `feature_usage` — which features each user accesses
- `paywall_interactions` — which paywalls trigger and convert
- `marketing_attribution` — source tracking for each registration
