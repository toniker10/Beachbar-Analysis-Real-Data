# Beach Bar Seasonal Analytics

**Headline: peak-weekend sunbeds are almost full (94.4%), but a +5% sunbed price rise on those days is worth only about €272 a season. Test it on a few weekends, do not roll it out blindly.**

---

## 1. Company Context

|                            |                                                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Business**               | Small beach bar in Greece: 40 sunbeds plus a food & beverage (F&B) bar, open May to September 2025 (153 days)           |
| **Stakeholder**            | The bar owner                                                                                                           |
| **My role**                | Data analyst reporting to the owner                                                                                     |
| **Business question**      | Does the data justify raising sunbed prices on peak-season weekends?                                                    |
| **Decision this supports** | Whether to raise sunbed prices next season, and where else the day-to-day operation can improve                         |
| **Data source**            | Sales records provided by the bar's owner (an acquaintance) for academic coursework. See the data notes in the Appendix |

Sunbed price was **€8 on every one of the 153 days**. It never changed, so the data cannot show how customers react to a price change.

---

## 2. North Star Metrics and Dimensions

| Metric             | Season value                                                  | Why it matters                                            |
| ------------------ | ------------------------------------------------------------- | --------------------------------------------------------- |
| **Total revenue**  | €111,342.50 (sunbeds €36,432 = 32.7%, F&B €74,910.50 = 67.3%) | The bar's overall result                                  |
| **Occupancy rate** | 74.4% average (booked / 40 sunbeds)                           | Shows when capacity, not demand, limits sales             |
| **F&B revenue**    | €74,910.50                                                    | Two thirds of revenue comes from the bar, not the sunbeds |

**Dimensions used to slice them:** month, weekend vs weekday, product and time of day.

---

## 3. Executive Summary

1. **Season shape:** occupancy climbs from 60.0% in May to 87.8% in August, then drops to 64.7% in September.
2. **Peak weekends are nearly full:** July and August weekends average **94.4%** occupancy, against 83.4% on weekdays in the same months. 13 of the 18 peak weekend days reached 95% or more. No day was fully booked (maximum 39 of 40).
3. **The price lever on sunbeds is small:** a +5% increase (€8.00 to €8.40) on the 18 peak weekend days adds about **€272** if no customers are lost. The widely quoted €5,567 figure applies +5% to all revenue on all days. That is a ceiling for a different question.
4. **F&B:** Draft Beer is the top product (€7,530, 10.1% of F&B). 18:00 to 21:00 is the weakest time slot (16.2% of F&B).
5. **A data lesson:** Mojito sales dropped to exactly zero for 10 days in August while overall traffic stayed normal. The most likely cause is a supply problem, not weak demand.

---

## 4. Insights Deep Dive

### 4.1 Occupancy rises from 60% in May to 88% in August

| Month     | Days | Avg occupancy | Total revenue |
| --------- | ---- | ------------- | ------------- |
| May       | 31   | 60.0%         | €18,191       |
| June      | 30   | 73.8%         | €22,604       |
| July      | 31   | 85.4%         | €25,096       |
| August    | 31   | 87.8%         | €26,148       |
| September | 30   | 64.7%         | €19,304       |

*(Revenue rounded to the nearest euro.)*

- **What:** revenue and occupancy peak together in July and August.
- **Why:** the sunbed price and the number of sunbeds were constant, so the monthly change comes from demand: season and weather.
- **So what:** capacity only becomes a limit in two months. May, June and September have spare sunbeds.

### 4.2 Peak weekends are almost full: 94.4% vs 83.4% on weekdays

| Peak period (Jul + Aug) | Avg occupancy | Avg total revenue / day | Avg F&B revenue / day |
| ----------------------- | ------------- | ----------------------- | --------------------- |
| Weekend (18 days)       | **94.4%**     | €957.30                 | €655.10               |
| Weekday (44 days)       | 83.4%         | €773.00                 | €506.10               |

- **What:** 13 of 18 peak weekend days were at 95% or more, and 10 were at exactly 39 of 40 sunbeds. Across the season, 15 days reached 95% (13 weekend days and 2 August weekdays).
- **Why:** the price never changed, so occupancy is the only thing that varied.
- **So what:** the bar is close to full on these days, but "close to full" is not the same as "turning customers away". There are no waitlist or refused-booking records, and no day sold out. The data supports a test, not a conclusion.

*Definition used throughout: peak weekend occupancy is the average over the 18 Saturdays and Sundays in July and August.*

### 4.3 A +5% rise is worth €272 on peak-weekend sunbeds, not €5,567

| Scenario (volume unchanged)                | Actual          | +5%          | Uplift     |
| ------------------------------------------ | --------------- | ------------ | ---------- |
| Sunbeds, all season                        | €36,432         | €38,254      | €1,822     |
| F&B, all products                          | €74,910.50      | €78,656      | €3,746     |
| **Total**                                  | **€111,342.50** | **€116,910** | **€5,567** |
| *Sunbeds on the 18 peak weekend days only* | *€5,440*        | *€5,712*     | ***€272*** |

- **What:** the +5% scenario on all revenue gives €5,567. The same rise on peak-weekend sunbeds only (the actual question) gives €272, or €0.40 per sunbed.
- **Why the big gap:** peak-weekend sunbeds are only 14.9% of season sunbed revenue (€5,440 of €36,432) and 4.9% of total revenue (€111,342.50). Most of the €5,567 comes from F&B, which is not the subject of the sunbed price question.
- **So what:** the sunbed price rise only pays off if the bar loses fewer than about 4.8% of bookings on those days (1 − 1/1.05), roughly 1.8 of the 37.8 sunbeds booked on an average peak weekend day. The potential gain is small, and so is the room for error.
- **Important:** every scenario figure assumes volume stays exactly the same. Price never varied historically, so the real customer response is unknown. These are ceilings, not forecasts.

### 4.4 Mojito sales hit zero for 10 days while traffic stayed normal

- **What:** Mojito revenue is exactly €0 from 10 to 19 August. In the rest of the season Mojito sold 559 units (€5,590, 7.5% of F&B).
- **Why:** during those 10 days sunbed bookings stayed between 30 and 39 and total daily orders between 40 and 65. Aperol Spritz averaged 4.4 units a day in the gap (3.4 the five days before, 4.2 the five days after) and Margarita 3.1 (2.6 before and after). The substitution is modest and based on a small sample.
- **So what:** this looks like a stock-out, not falling demand. The wrong reaction would be to discount or remove Mojito. The data cannot prove the cause. A stock record would.

### 4.5 The evening slot is the weakest: 16.2% of F&B

| Time slot       | Orders    | F&B revenue | Share     | Avg per day |
| --------------- | --------- | ----------- | --------- | ----------- |
| 09:00–12:00     | 1,926     | €21,396     | 28.6%     | €139.80     |
| 12:00–15:00     | 2,096     | €23,469     | 31.3%     | €153.40     |
| 15:00–18:00     | 1,596     | €17,895     | 23.9%     | €117.00     |
| **18:00–21:00** | **1,063** | **€12,152** | **16.2%** | **€79.40**  |

- **What:** 18:00–21:00 is the lowest-revenue slot on 74.5% of days. It is the weakest slot most days, not every day.
- **Why:** unknown. The data has no information on guest numbers by hour or on opening hours.
- **So what:** the evening has the most room to grow, but any explanation is a hypothesis.

### 4.6 What sells: beer leads revenue, water leads volume

- Top products by revenue: Draft Beer €7,530 (10.1%), Mojito €5,590 (7.5%), Freddo Espresso €5,400 (7.2%), Aperol Spritz €5,210 (7.0%).
- Small Water is the most-sold item by units (5,479) but only 3.7% of F&B revenue (€2,740). Volume leaders and revenue leaders are different products.

---

## 5. Recommendations

| # | Action | Owner | Expected impact | Metric to track |
| --- | --- | --- | --- | --- |
| 1 | **Run a controlled price test next season:** raise sunbeds from €8 to €8.40 on a randomly chosen half of the 9 peak weekends, and keep the other half at €8 as a comparison | Bar owner | Up to about +€15 per test day (+€272 over all 18 days) if bookings hold | Peak-weekend occupancy vs the 94.4% baseline, and sunbed revenue per day vs €302.20 |
| 2 | **Track daily stock for key cocktail ingredients** so a stock-out is spotted the same day | Bar manager | Avoids silent sales gaps like the 10 Mojito days | Days with zero sales of an item that normally sells (target: 0) |
| 3 | **Test an evening offer on weekdays, 18:00–21:00,** for a few weeks (this is a hypothesis, not a proven fix) | Bar manager | Closes part of the gap to the €117.00 slot before it | 18:00–21:00 F&B revenue per day vs the €79.40 baseline |
| 4 | **Start recording refused bookings and every price change** | Owner / analyst | Makes a real demand and price-response analysis possible next year | Number of customers turned away on peak days |

---

## 6. Limitations

- **Price never varied (always €8):** customer reaction to a price change cannot be estimated from this data.
- **No turn-away data:** high occupancy shows the bar is busy, not that demand is going unmet.
- **Short history:** one season, 153 days. Weather affects occupancy and is not controlled for.
- **Time-slot figures are indicative:** the zone-level amounts include cents that cannot be rebuilt from the catalogue prices, and order counts by slot do not match daily totals on 54 of 153 days. Zone revenue does match daily F&B revenue (within 5 cents).
- **Mojito explanation is an inference:** the stock-out is the most likely cause, not a proven one.

---

## Appendix

### A. Files

| File                               | Contents                                                                                                                |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `beach_bar_seasonal_analytics.sql` | Schema, data and 7 business queries (SQLite)                                                                            |
| `beachbar_analysis.xlsx`           | Excel workbook with formulas: Overview, Monthly & Occupancy, Products, Time of Day, Price Scenario (data sheets hidden) |
| `beachbar_dashboard.pbix`          | Power BI dashboard: Overview, Capacity & Pricing, Products, Time of Day                                                 |

### B. Data structure

| Table            | One row represents       | Rows              |
| ---------------- | ------------------------ | ----------------- |
| `daily_sales`    | One day                  | 153               |
| `products`       | One product (catalogue)  | 21 (8 categories) |
| `product_sales`  | One product on one day   | 3,213             |
| `timezone_sales` | One time slot on one day | 612               |

### C. Method

- **SQL:** monthly summary (Q1), capacity check (Q2), product revenue (Q3), Mojito investigation (Q4), time of day (Q5), +5% scenario (Q6), peak weekend vs weekday comparison and peak-weekend price effect (Q7).
- **Excel:** formula-driven summary sheets. The figures in this README match the SQL and the Excel. The peak-weekend occupancy (94.4% vs 83.4%), the days at 95% or more (15, of which 13 weekend days) and the peak-weekend sunbed figures (€5,440, €272) are in the Excel (Monthly & Occupancy and Price Scenario sheets). The average revenue per day figures in section 4.2 (€957.30, €773.00) are reproduced by SQL query Q7.
- **Power BI:** measures for total revenue, average occupancy, peak weekend occupancy, days near capacity, the +5% scenario on all revenue, the peak-weekend sunbed uplift (€272), product revenue and units, and zone revenue.

### D. Data checks and change log

| Check | Result |
| --- | --- |
| SQL data vs Excel data | Identical, row by row |
| Sunbed revenue | Equals sunbeds booked × €8 on every day |
| Total revenue | Equals sunbed revenue + F&B revenue on every day |
| Daily F&B vs sum of product sales | Equal on every day |
| Daily F&B vs sum of time-slot revenue | Equal within 5 cents |
| Daily orders vs sum of time-slot orders | **Differ on 54 of 153 days** (limitation noted above) |
| Peak weekend occupancy | One definition used: average over the 18 days = **94.4%**. An earlier Excel version averaged two monthly averages (94.56%) and was aligned |

### E. How to run

Run the `.sql` file in a new, empty SQLite database. It drops and recreates its own tables, so do not run it against a database that already contains tables named `daily_sales`, `products`, `product_sales` or `timezone_sales`.

*The data was provided by the bar owner for voluntary basis. It should be read as a worked analysis on one season of a single small business.*
