Antitrust case studies: cartel damages and merger review

Two small competition-economics case studies in Python, on simulated or illustrative data. They follow the logic of work done for competition authorities and courts: build the "but-for" world (what would have happened without the conduct), measure the gap, and test how robust the answer is.


How to run

Open antitrust_case_studies.ipynb in Google Colab and choose Runtime, then Run all. No installation is needed.


Case 1: Cartel overcharge and damages
A simulated 25-year monthly market with a 14-year cartel (the structure is inspired by the European trucks cartel), cost and regulation shocks, and persistent errors. The true cartel effect is 6.0%.

Naive before/during comparison: 13.3%, biased because costs rose faster during the cartel
Regression with cost and demand controls and robust standard errors: 6.2% (s.e. 0.6%)
Counterfactual forecast from non-cartel months: 5.9%
Regression that omits the cost control: 14.7% (omitted-variable bias)

The overcharge is then converted to direct-purchaser damages with a pass-on (price) effect and a quantity effect. Net damages fall from EUR 5.97m to EUR 1.34m as the pass-on rate rises from 0% to 90%. Pass-on, elasticity, margin and price are illustrative assumptions.



Case 2: Merger review across local markets
Eight illustrative local markets for a retail merger. For each: overlap, pre- and post-merger HHI, upward pricing pressure from share-based diversion, and a screen. Six of eight markets overlap and all six are flagged. Selling the smaller party's store to the smallest rival leaves all six above the screen; selling to a new entrant clears them all.

Supporting models
Cournot competition (a 4-to-3 merger raises price from 36 to 40) and collusion stability (critical discount factor 0.571 with three firms, 0.643 with five).


Limits
Simulated data; linear demand and identical products in the supporting models; diversion assumed proportional to share; screen thresholds are illustrative parameters rather than any authority's rules. A real case needs transaction data, cost data, diversion evidence and a court-ready robustness analysis.


Possible extensions
A difference-in-differences estimate using a comparator market unaffected by the cartel.
Survey-based diversion ratios instead of share-based.
Calibration to a public cartel decision.
