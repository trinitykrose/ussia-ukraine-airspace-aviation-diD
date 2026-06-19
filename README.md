The Impact of the Russia-Ukraine War on European Aviation: A Difference-in-Differences Approach

Question

Did the 2022 closure of Russian and Ukrainian airspace cause a measurable decline in European aviation activity — and did the resulting rerouting offset any of the associated emissions reduction?

Approach


Design: Two-Way Fixed Effects (TWFE) difference-in-differences, exploiting the geographic discontinuity created by the airspace closure. Routes are classified as "treated" if their great-circle path transits Russian or Ukrainian Flight Information Region (FIR) boundaries.
Data: Route-month panel from Eurostat's Aviation Passenger Transport dataset, January 2015 – December 2024, covering 31 European countries, ~9,800 origin-destination pairs, and 783,057 route-month observations (COVID years excluded from the main specification).
Identification: Route and month-year fixed effects absorb time-invariant route heterogeneity and common aggregate trends; standard errors clustered at the route-pair level.
Validation: Event-study specification confirms flat, insignificant pre-trends ahead of the February 2022 closure; a placebo test using a false February 2019 treatment date returns near-zero effects on the main outcomes.

Key results

Flights: −7.4% 
Passengers: −15.1% 
Seat capacity: −9.9% 
Load factor: No significant change
CO2 emissions (estimated): −2.7% (not statistically significant)

The unchanged load factor suggests airlines cut capacity roughly in proportion to falling demand rather than flying emptier planes. The smaller, statistically weaker decline in estimated CO2 relative to the decline in flights is consistent with rerouting over longer alternative corridors partially offsetting the emissions benefit of fewer flights — though this estimate should be treated as imprecise.

Heterogeneity: Effects are concentrated on routes with direct exposure to Russian airspace (rather than Ukrainian-only exposure) and on very long-haul routes, consistent with their greater historical reliance on Russian overflight corridors. We also find a significant increase in activity on medium-haul routes (under ~3,000km), suggestive of demand substitution toward shorter, lower-cost intra-European and West Asian corridors.

Robustness

Results hold under three checks: including COVID-period observations, excluding Finland (the country most exposed to Russian overflight restrictions), and varying the rerouting-multiplier assumptions used to estimate CO2 emissions.

Limitations


Treatment is inferred from route geography (great-circle path intersecting FIR boundaries) rather than observed actual flight paths.
CO2 estimates rely on distance-band fuel-burn averages and assumed rerouting multipliers, not directly observed fuel consumption.
The placebo test returns small but statistically significant coefficients for flights, seats, and CO2 (though far smaller in magnitude than the post-closure estimates), indicating some residual pre-trend variation that should temper confidence in the exact point estimates.


Data sources

All data used are public and require no registration:

Eurostat Aviation Passenger Transport (avia_paoc) and aircraft-type datasets (avia_tf_aca) — ec.europa.eu/eurostat
ICAO FIR boundary polygons — gis.icao.int/icaofir
ICAO Carbon Emissions Calculator methodology — icao.int
OurAirports airport coordinate database — ourairports.com


Sonnet 4.6 LowClaude is AI and can make mistakes. Please double-check responses.Readme airspace · MDCopyThe Impact of the Russia-Ukraine War on European Aviation: A Difference-in-Differences Approach

Group project — three contributors (collaborator names withheld for privacy; this repo reflects joint work across data construction, modelling, and write-up).

Question

Did the 2022 closure of Russian and Ukrainian airspace cause a measurable decline in European aviation activity — and did the resulting rerouting offset any of the associated emissions reduction?

Approach


Design: Two-Way Fixed Effects (TWFE) difference-in-differences, exploiting the geographic discontinuity created by the airspace closure. Routes are classified as "treated" if their great-circle path transits Russian or Ukrainian Flight Information Region (FIR) boundaries.
Data: Route-month panel from Eurostat's Aviation Passenger Transport dataset, January 2015 – December 2024, covering 31 European countries, ~9,800 origin-destination pairs, and 783,057 route-month observations (COVID years excluded from the main specification).
Identification: Route and month-year fixed effects absorb time-invariant route heterogeneity and common aggregate trends; standard errors clustered at the route-pair level.
Validation: Event-study specification confirms flat, insignificant pre-trends ahead of the February 2022 closure; a placebo test using a false February 2019 treatment date returns near-zero effects on the main outcomes.


Key results

OutcomeEffectFlights−7.4%Passengers−15.1%Seat capacity−9.9%Load factorNo significant changeCO2 emissions (estimated)−2.7% (not statistically significant)

The unchanged load factor suggests airlines cut capacity roughly in proportion to falling demand rather than flying emptier planes. The smaller, statistically weaker decline in estimated CO2 relative to the decline in flights is consistent with rerouting over longer alternative corridors partially offsetting the emissions benefit of fewer flights — though this estimate should be treated as imprecise.

Heterogeneity: Effects are concentrated on routes with direct exposure to Russian airspace (rather than Ukrainian-only exposure) and on very long-haul routes, consistent with their greater historical reliance on Russian overflight corridors. We also find a significant increase in activity on medium-haul routes (under ~3,000km), suggestive of demand substitution toward shorter, lower-cost intra-European and West Asian corridors.

Robustness

Results hold under three checks: including COVID-period observations, excluding Finland (the country most exposed to Russian overflight restrictions), and varying the rerouting-multiplier assumptions used to estimate CO2 emissions.

Limitations


Treatment is inferred from route geography (great-circle path intersecting FIR boundaries) rather than observed actual flight paths.
CO2 estimates rely on distance-band fuel-burn averages and assumed rerouting multipliers, not directly observed fuel consumption.
The placebo test returns small but statistically significant coefficients for flights, seats, and CO2 (though far smaller in magnitude than the post-closure estimates), indicating some residual pre-trend variation that should temper confidence in the exact point estimates.


Data sources

All data used are public and require no registration:


Eurostat Aviation Passenger Transport (avia_paoc) and aircraft-type datasets (avia_tf_aca) — ec.europa.eu/eurostat
ICAO FIR boundary polygons — gis.icao.int/icaofir
ICAO Carbon Emissions Calculator methodology — icao.int
OurAirports airport coordinate database — ourairports.com


Repo structure


notebook1_data.ipynb — data construction, route classification, FIR-transit logic
notebook2_co2.ipynb — CO2 emissions estimation from flight counts and distance-band fuel burn
notebook3_analysis.ipynb — TWFE estimation, event study, heterogeneity analysis, robustness checks
