# Part E — The 11 AM Ops Review

**Audience:** VP and regional managers
**Rules:** No "model", no "algorithm", no "null", no "feature importance". Every sentence contains a number or a named location.

---

## The 5-Sentence Verbal Brief

1. Today's 150-order file is ready to act on, with one data flag: 6 orders arrived without a `delivery_time_mins` value and were patched with the zone median before scoring.

2. The one combination Ops must own this week is **Burger Hub in Central**, where 8 of 10 orders are flagged high cancellation risk — an **80% risk rate** against our 30% hotspot threshold, with an average delivery time of 67 minutes versus roughly 50 minutes in healthy zones.

3. From tomorrow, the automated **07:30 morning brief** will land in Discord and Gmail with the day's cancellation rate, worst zone, worst restaurant, and top restaurant-zone pair, and will escalate to a Red Alert whenever the daily cancellation rate crosses **20%**.

4. What the 07:30 brief cannot yet tell you is the rider side of the story — we hold no rider ID, shift, weather, or traffic signal for the 67-minute Central delays, so we can name the hotspot but not separate kitchen prep from dispatch.

5. The single number to watch over the next **4 weeks** is **Burger Hub – Central's high cancel-risk rate falling from 80% to under 30%**.

---

## Supporting Numbers (for Q&A only — not part of the verbal brief)

| Item | Value |
|---|---|
| Orders scored today | 150 |
| Orders missing `delivery_time_mins` | 6 (patched with zone median) |
| Hotspot threshold | >30% high-risk rate |
| #1 hotspot | Burger Hub – Central, 80% (8/10 orders) |
| #2 / #3 hotspots | Burger Hub – West 75%; Wrap & Roll – Central 75% |
| Highest single-order risk | ORD00091, Sushi Bay / Central, p = 0.91 |
| Brief delivery time | 07:30 local, daily |
| Brief channels | Discord webhook + Gmail (`dogalife4@gmail.com`) |
| Red Alert trigger | Daily cancellation_rate > 20% |
| 4-week target KPI | Burger Hub – Central risk rate < 30% |
| Secondary watch | Overall daily cancellation_rate held under 20% |
