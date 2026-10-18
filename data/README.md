# Assignment 2 data dictionary

This is a fictional pilot inspired by Nicholas Ryan (2018), NBER Working Paper 24619, https://doi.org/10.3386/w24619. It contains no real observations from his experiment. The synthetic time path illustrates model counterfactuals, not a replicated empirical event study.

File: `data/energy_firms.csv`. 480 plants x 16 months = 7,680 rows. Key: firm_id + month. No missing observations. Consulting starts in month 1; months -3 through 0 are baseline. Treatment is randomized equally within sector x adjustment-month cells. Adjustment months were independently scheduled before assignment.

| Field | Description / units |
|---|---|
| firm_id | Persistent plant identifier |
| sector | Textiles or Chemicals; fictional groups |
| treated | 1 consulting assignment; 0 control, constant across panel |
| month | Integer -3,...,12; monthly totals |
| adjust_month | 4, 6, or 8; first post-intervention month with freely adjustable labor |
| labor_adjustable | 1 before treatment and from adjust_month onward; otherwise 0 |
| output | Standardized batches of unchanged quality per month |
| labor | Blocks of 100 paid worker-hours per month; continuous |
| electricity | MWh per month |
| output_price | CU per standardized output batch |
| wage | CU per block of 100 worker-hours, not CU per hour |
| energy_price | CU per MWh |

Prices are plant-specific, constant over time and unchanged by consulting. Physical input and output units are standardized for teaching, so technological indices depend on the chosen units. No other variable inputs, exits, spillovers, inventories or product-quality changes are included. Quantities contain small independent multiplicative recording errors. Differences in firm scale, prices and productivity are persistent. Random assignment does not make baseline sample means identical. Sector is a descriptive label, not a separate production function.

Labor is a paid commitment while labor_adjustable=0. Electricity can always adjust. A_i and eta_it are unobserved. Consulting is assigned; its realised efficiency effect is not a known treatment dose. Recovering technological quantities requires the model and its assumptions. Recorded prices have no measurement error. Profits reconstructed from recorded quantities inherit their errors and exclude consulting-delivery costs and environmental damages.

Repeated months are not independent treatment assignments: the plant is the assignment unit.
