# Missed Call Revenue Calculator

A one-page calculator that shows a service business how much revenue it loses to unanswered calls each month, and what a typical week of those missed calls looks like.

**Live:** https://xschaudhry.github.io/missed-call-revenue-calculator/

## The problem

Most service businesses (clinics, med spas, HVAC, plumbing, auto repair, roofing) miss calls after hours, at lunch and when the line is busy. Each missed new-customer call usually dials the next business on Google. Owners rarely see the cost because it never shows up as a bill.

## What it does

- Presets for 7 niches, all editable: missed calls per week, share of new customers, booking rate, average job value
- Monthly and yearly revenue lost, plus jobs lost per month
- A simulated week of missed calls, with the ones that would have booked marked in red and valued
- What an AI receptionist recovering 70% of those calls would be worth
- The full calculation, shown step by step
- Shareable links: inputs are kept in the URL (`?niche=dental&calls=15&newp=60&book=50&value=600`), so a prospect's own numbers can be sent in an outreach email
- Works on mobile, supports dark mode, no tracking, nothing stored or sent

## The math

```
lost jobs per month = missed calls/week × % new customers × % booking rate × 4.3
revenue lost/month  = lost jobs per month × average job value
```

Example (dental): 15 × 60% × 50% × 4.3 × $600 = **$11,610 / month**

Only the first job is counted. Repeat visits, referrals and reviews are left out on purpose, to keep the estimate conservative.

## Use it in outreach

1. Call a prospect after 5 pm. If it rings out, note the time.
2. Open the calculator with their niche and a fair estimate of their numbers.
3. Click **Copy link to these numbers** and put the link in your email or Loom video.

## Run locally

It's a single static file with no build step.

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy on GitHub Pages

Repo **Settings → Pages → Deploy from a branch → `main` / root**.

---

Built by [Chaudhry Usman](https://linkedin.com/in/chaudhryusmantrx) at [TRXmode](https://trxmode.com): AI receptionists, speed-to-lead and follow-up systems for service businesses. [Book a free Revenue Leak Audit](https://www.trxmode.com/booking-page).
