### Project Overview
This project developed and validated a data-driven promotional strategy to increase beer category profits at Lakeview Market, Store 257871, using 2009 transaction and loyalty data. The work combined advanced modeling of shopper and product behavior with scenario simulations and uplift targeting to deliver actionable recommendations that maximize profit and return on promotional investments.

### Objectives
The primary goal was to identify intervention strategies to grow beer sales and profits through evidence-based levers, including:
- Predicting beer trip incidence and brand choice
- Testing pricing and feature tactics for major brands
- Optimizing promotion target segments to ensure efficient, positive-ROI campaigns.

### Data Sources & Preparation
Six complementary datasets were integrated, including detailed item-level transactions, customer trip records, demographic profiles, and in-store display and pricing audits. Extensive preprocessing—data merging, cleaning, categorical encoding, and dimensionality reduction—enabled a unified, analytically ready database spanning over 11,000 beer transactions made by 332 customers.

### Modeling and Analysis Approach
- **Purchase Incidence Model:** Logistic regression identified key drivers (loyalty, basket size, season, day-of-week, promotion, and demographics) for beer purchase on each trip.
- **Brand Choice Model:** Multinomial logit analyzed brand selection, finding that Miller Lite is sensitive to features and price, Michelob Golden Draft Light is price-inelastic but placement-sensitive, and Milwaukees Best Light responds best to subtle discounts.
- **Uplift Modeling:** Estimated incremental purchase lift from joint promo exposure, optimizing segment targeting for highest ROI.
- **Scenario Simulations:** Combined model coefficients to test potential outcomes under various promo mixes, quantifying revenue and profit effects.

### Strategic Recommendations
- **Miller Lite:** Use feature promotions with modest price cues mainly in high-traffic weeks.
- **Michelob Golden Draft Light:** Rely on placement/premium positioning without discounting.
- **Milwaukees Best Light:** Apply quiet, shallow discounts while minimizing advertising.
- **Customer Targeting:** Focus contacts on the top 30% most responsive customers, with email outreach concentrated in the highest-traffic weeks.

### Financial Results
The recommended strategy is projected to increase annual category net profit by about $3,705 (+1.15%) compared to 2009, despite a reduced promotional budget. Improved profit is achieved through both targeted outreach and brand-specific tactics rather than broad, undifferentiated discounts.

### Conclusion
A data-driven promotion strategy leveraging incidence, choice, and uplift modeling yields positive, scalable profit gains for Lakeview Market’s beer category. Targeted and brand-specific tactics maximize ROI while minimizing wasted spend, providing a robust template for ongoing optimization.


Dataset: https://drive.google.com/drive/folders/1D32NXl2-F5kIRSYTmha0bxsfU3VsvNz0?usp=sharing
- BeerEnvECPF2009.xlsx — 109,616 rows, item-level store transactions with pricing and promo flags (e.g., UNITS, PURCHASE_PRICE/UNIT_PRICE, FEATURE, DISPLAY, PRICE_REDUCTION), mapped to weeks (2008-12-29 to 2009-12-21).
- trips9 may13.csv — 47,947 rows, customer trip records (PANID, IRI_KEY, WEEK_DATE, MINUTE, TRIP_COST) over the same 2009 calendar window.
- beer_PANEL_GK_1531_1582.dat — 5,424 rows, beer-specific transactions at the PANID-trip level (BEER_PURCHASED, BEER_UNITS, UPC, IRI_KEY, timing), also 2008-1229 to 2009-12-21.
- ads demos9.csv — 4,607 rows, household-level demographics keyed by PANID (education, occupation, income bands, residence type, age/race codes).
- prod11_beer.xlsx — 16,758 rows, product master by UPC (brand, package/size/volume, parent company).
- IRI week translation_2008_2017.xls — calendar map for WEEK → WEEK_DATE (and SEASON where present), used to align all datasets on time.
